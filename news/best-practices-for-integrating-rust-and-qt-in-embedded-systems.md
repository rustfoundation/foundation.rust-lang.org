---
title: Best Practices for Integrating Rust and Qt in Embedded Systems
byline:
description: >
  Rust Foundation Guest Blog Series: Silver Member, KDAB, featuring Andrew
  Hayzen, Leon Matthes, and Be Wilson.
date: 2023-03-03T12:30:00Z
tags:
  - guest blog series
index: false
layout: layouts/news.njk
---
<img width="580" height="326" alt="[Heading 1] Guest Blog Series: KDAB (Silver Member) [Heading 2] Best practices for integrating Rust and Qt in embedded systems] Headshots of Leon Matthes, Andrew Hazen, &amp; Be Wilson underneath)" title="KDAB Guest Blog" src="/img/news/2023-03-07-kdab-guest-post/kdab-guest.png" />

*Welcome to another installment in the Rust Foundation&nbsp;*[*guest blog series*](https://foundation.rust-lang.org/tags/guest%20blog%20series/)*, written by members of the Rust Foundation and/or community. Today, we are pleased to have a post written by Andrew Hayzen (Qt developer), Leon Matthes (Software Engineer), and Be Wilson (Software Engineer) of KDAB— a Rust Foundation <a target="_blank" rel="noopener" href="https://foundation.rust-lang.org/members/">Silver Member</a>&nbsp;organization. Read on to discover KDAB’s recommended principles for achieving the best of both the Rust and Qt worlds for embedded applications.*

***This post originally appeared on&nbsp;*[*<u>embedded.com</u>*](https://www.embedded.com/best-practices-for-integrating-rust-and-qt-in-embedded-systems/) *and is being republished with permission from KDAB.***

---

Rust offers high performance, high reliability, and strong security for embedded software and helps developers check for and reduce memory and threading errors common to complex, low-level applications. With these clear benefits, Rust is gaining popularity among embedded software developers.&nbsp;

Similarly, as one of the most popular frameworks for cross-platform embedded applications, Qt brings powerful business logic features to the embedded sphere. As Rust doesn’t yet have a leading graphical user interface (GUI), this means that Rust-Qt integration is becoming increasingly interesting for embedded developers and has become one of the key methods for adding a GUI to embedded Rust applications.

The challenge comes when integrating the two. Without careful planning and effort, a combined Rust-Qt application falls prey to the weakest attributes of either language. Calls from Qt/C++ to Rust may be unsafe, concurrency issues may occur between domains, and Rust’s high performance and portability may be compromised.

This article walks through recommended principles to achieve the best of both the Rust and Qt worlds for embedded applications.

## Background on Rust and Qt

Rust has a rich ecosystem of libraries for serialization and deserialization, asynchronous operations, parsing unsafe inputs, threading, static analysis, and more, while Qt is a C++ toolkit that supports rich, GUI-based applications across a variety of platforms, from iOS to Embedded Linux. Qt applications include C++ plugins that represent business logic, QML to define GUI components and layout, and JavaScript for GUI scripting.

Integrating Rust libraries into a Qt framework gives developers a robust mechanism to deliver a high-performance and secure foundation that drives sophisticated user experiences. Consider an agricultural instrument panel application that requires safe access to a backend I/O microcontroller or an airplane cockpit display that pulls data from an RTOS-based single-board computer.

One recommended application architecture is to keep the business logic within the Rust backend and use Qt/C++ plugins for the user interface. This decouples the two domains and separates the fast iteration speed and flexibility of Qt/QML for GUI development from the business-level code.

## How to integrate Rust and Qt for embedded software

The most common method for integrating Qt with Rust is for Rust to call Qt’s C++ libraries.&nbsp;

While there are several binding methods out there, these are typically not idiomatic to Rust and tend to lose the safety benefits, as shown in Figure 1. Furthermore, most Rust bindings for Qt do not expose Rust code to C++, making them difficult to integrate into existing C++ codebases.

<img width="580" height="288" alt="Figure 1. Challenges with Rust-Qt bindings (Source: KDAB)" title="Traditional Approach: Rust bindings for Qt" src="/img/news/2023-03-07-kdab-guest-post/fig-1.png" />

*Figure 1. Challenges with Rust-Qt bindings (Source:&nbsp;<a target="_blank" rel="noopener" href="https://www.kdab.com/cxx-qt/">KDAB</a>)*

A more effective approach is to bridge the two languages in a safe way, preserving as much of Rust’s inherent safety benefits as possible. For this to work, Rust needs to be able to extend the Qt object system with its own QObject subclasses and instances with minimal compromise.

An example of this latter approach is the open-source library [<u>CXX-Qt</u>](https://github.com/KDAB/cxx-qt) that KDAB initiated and manages its ongoing development and improvements. This library combines Qt’s strong object orientation and meta-object system with Rust and builds upon and extends [<u>CXX</u>](https://cxx.rs/index.html), another open-source Rust/C++ interoperability library. In CXX-Qt, new QObject subclasses are composed of items in a Rust module to perform the bridging functions. These subclasses are instantiated just like any other QObject in QML and C++, exposing Rust features to Qt.

### **Every QObject defined by CXX-Qt includes two components:**

* A C++-based object that is a wrapper that exposes properties and invokable methods
* A Rust struct that stores the properties, implements invokables, manages internal state and handles change requests from properties and background threads

CXX-Qt automatically generates code to transfer data between the Rust and Qt/C++ domains and uses a library called [<u>CXX</u>](https://cxx.rs/) to communicate between the two.

## Key principles of the CXX-Qt bridging approach

To explain how an effective Rust-Qt bridge works, we’ll describe several key principles behind the CXX-Qt library.

### Declaring QObjects in Rust

Qt’s design is inherently object-oriented, which is true for both C++ and QML, while Rust doesn’t support the usual class features like inheritance and polymorphism. To overcome this limitation, CXX-Qt extends the Qt object system within Rust to provide a natural way to integrate the two languages while maintaining idiomatic Rust code.

A CXX-Qt bridge can include these parts:

* A macro around the module that indicates the contents are CXX-Qt related
* A struct to define the QObject, any properties for Qt, and any private state
* An optional impl of the Qobject struct where functions can be marked as qinvokable which allows them to be called from QML and C++
* An enum to define the signals for a QObject
* Normal CXX blocks

CXX-Qt expands this Rust module during code generation into a C++ subclass of QObject and the RustObj struct, as shown in Figure 2.

<img width="580" height="250" alt="Figure 2. How CXX-Qt expands QObjects for runtime use (Source: KDAB)" title="CXX-Qt: QObject Definition" src="/img/news/2023-03-07-kdab-guest-post/fig-2.png" />

*Figure 2. How CXX-Qt expands QObjects for runtime use (Source: KDAB)*

Here’s an example of a QObject with three invokable methods for operations across domains and one Rust-only method:

```
[cxx_qt::bridge]
mod my_object {
    unsafe extern "C++" {
        include!("cxx-qt-lib/qstring.h");
        type QString = cxx_qt_lib::QString;
        include!("cxx-qt-lib/qurl.h");
        type QUrl = cxx_qt_lib::QUrl;
    }
    #[cxx_qt::qobject]
    #[derive(Default)]
    pub struct MyObject {
        #[qproperty]
        is_connected: bool,
        #[qproperty]
        url: QUrl,
    }
    #[cxx_qt::qsignals(MyObject)]
    pub enum Connection {
        Connected,
        Error { message: QString },
    }
    impl qobject::MyObject {
        #[qinvokable]
        pub fn connect(mut self: Pin<&mut Self>, url: QUrl) {
            self.as_mut().set_url(url);
            if self
              .as_ref()
                .url()
              .to_string()
                .starts_with("https://kdab.com")
            {
                self.as_mut().set_is_connected(true);
                self.emit(Connection::Connected);
            } else {
                self.as_mut().set_is_connected(false);
                self.emit(Connection::Error {
                    message: QString::from("URL does not start with https://kdab.com"),
                });
            }
        }
    }
}[
```

Methods declared with the \#\[qinvokable\] attribute (e.g., connect above) are exposed to QML and C++, with parameters and return type matched on the Qt side. Fields in the QObject struct declared with the \#\[qproperty\] attribute (such as is\_connected above) are exposed to QML and C++ as a Q\_PROPERTY. The enum marked with a \#\[cxx\_qt::qsignals(T)\] attribute defines the signals that are declared on the QObject T. Note that CXX-Qt automatically converts between snake\_case (Rust) and CamelCase (Qt) naming.

In this example, the connect method is used to mutate the URL and connected properties of the QObject from Rust. Then a signal is emitted indicating whether the connection was successful or if an error occurred.

Methods or fields not tagged with an attribute are considered private to Rust and useful to manage internal states or to use as thread instance data.

Since the QObject is a constructed Qt object owned by the C++ side of the bridge, it will be destroyed when the C++ object is destroyed at runtime.

### Declaring common data types across the bridge

Primitive data types and CXX types can be used across the bridge and don’t require conversion between Rust and Qt. The library cxx\_qt\_lib provides Rust types that represent common Qt types (e.g. QColor, QString, QVariant etc) for use across the bridge.

As the project evolves, we plan to add more commonly used Qt types to cxx\_qt\_lib, such as Qt container types (eg QHash and QVector) and other types useful for Qt C++ or QML. Then we want to enhance these types by adding conversions to and from established crates in the Rust ecosystem. For example, we plan to support conversion from a QColor to a color crate type or a QDateTime to a datetime crate type, or to (de)serialise Qt types using a Rust crate, etc.

### Keeping threads safe

The general concept behind safe threading in a Rust-Qt application is to acquire a lock on the C++ side whenever Rust code executes, to prevent the execution of this code by multiple threads. This means all Rust code directly called from C++, such as invokables, execute on the Qt thread only.

To allow developers to synchronize state from a background Rust thread to Qt, CXX-Qt provides a helper that allows you to queue a Rust closure from the background thread. The closure is then executed from the Qt event loop.

```
// In an invokable, request a handle to the qt thread
let qt_thread = self.qt_thread();
// Spawn a Rust thread
std::thread::spawn(move || {
    let value = compute_value_on_rust_thread();
    // Use a closure to move the value and run the task on the Qt event loop
    qt_thread
      .queue(move |mut qobject| {
            // Happens on the Qt event loop
            qobject.set_value(value);
        })
      .unwrap();
});
```

### Exposing Rust QObjects to QML

To use the Rust code within the Qt application, Rust QObject must be exported to QML. CXX-Qt simplifies this process by generating a C++ class for every QObject subclass defined in Rust – the developer just needs to include two statements in main.cpp:

1\. Include the QObject class, e.g.,

```rust
#include "cxx-qt-gen/my_object.h"
```

2\. Export the QObject class to QML, e.g.,

```rust
qmlRegisterType("com.kdab.cxx_qt.demo", 1, 0, "MyObject");
```

## Build system

CXX-Qt has support for being built using either CMake or Cargo.

With CMake, [<u>Corrosion</u>](https://github.com/corrosion-rs/corrosion) (formerly known as cmake-cargo) is used to import the Rust crate as a static library which is then linked to your Qt application executable or library. This allows for easy integration of CXX-Qt in existing CMake Qt applications. When the Rust crate is built the build.rs file compiles any C++ code that CXX-Qt generates.

For projects using Rust’s Cargo build system CXX-Qt can also be used from Cargo without CMake. With this method, the build.rs file for the Rust project also triggers the building of Qt resources, compiling of any additional C++ files, and linking to any additional Qt modules.

## **Conclusion**

As the use cases for integrating Rust and Qt grow, development teams should know their options beyond one-to-one direct binding. The CXX-Qt library provides a viable bridging mechanism that preserves the thread safety and performance benefits of Rust in an idiomatic way while also allowing developers to work with normal Qt and Rust code.

By understanding the concepts here, including the mapping between Qt objects and Rust QObject, common Qt types for Rust, and macros and code generation to define the runtime interoperability, developers can better choose the right Rust-Qt integration mechanism for their application development.

To use CXX-Qt or contribute to its development, the library is available [<u>on GitHub</u>](https://github.com/KDAB/cxx-qt) and its samples and documentation are found [<u>here</u>](https://kdab.github.io/cxx-qt/book/). For information on all kinds of leading-edge embedded technologies, visit [<u>kdab.com</u>](https://www.kdab.com/).

---

*Thank you for reading this post in the Rust Foundation&nbsp;[guest blog series](https://foundation.rust-lang.org/tags/guest%20blog%20series/). Stay tuned for more installments in the future!*