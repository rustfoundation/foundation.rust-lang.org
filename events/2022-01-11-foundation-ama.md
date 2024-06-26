---
title: "The Rust Foundation Ask Me Anything (AMA) - January 2022"
description: Rust Foundation Executive Director Bec Rumbul is joined by board member Nell Shamrell-Harrington in an Ask-Me-Anything (AMA) interactive webinar to share the latest updates of the Foundation and answer community questions. Moderated by Sage Griffin.
date: 2022-01-11
tags:
  - ama
  - live
  - webinar
layout: layouts/event.njk
---

<div class="video-holder">
    <div id="video-container">
        <iframe src="https://www.youtube.com/embed/C5JyXahfHw0" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>
</div>

- [Happy New Year Post](/posts/2022-01-06-happy-new-year-rustaceans-from-bec/)
- [Learn More about our AMAs](/posts/2021-11-04-rust-foundation-ama-launch/)

<h3>Transcript from the first Rust Foundation AMA with Bec Rumbul and Nell Shamrell-Harrington, moderated by Sage Griffin.</h3>
<h4>January 11, 2021</h4> 

<b>Table of Contents</b>

- <a href="#intro">Introduction</a>
- <a href="#governance">If Rust were to tweak its governance structure, what open source projects should we seek to emulate?</a>
- <a href="#inspiration">Are there any other open source foundations that you think the Rust Foundation should be looking at for inspiration?</a>
- <a href="#boundaries">What are the boundaries between the Foundation and the Rust project?</a>
- <a href="#sponsoring-maintainers">Is the Foundation going to be sponsoring key volunteer maintainers?</a>
- <a href="#diverse-interests">With respect to matching programmers with resources, how can Rust navigate such a divergent set of interests?</a>
- <a href="#next-focus">If there's one important thing the Foundation needs to focus on next, but only one to choose, what would that be?</a>
- <a href="#2022">What can we expect from the Foundation in 2022?</a>
- <a href="#cloud-compute">Have there been any more details that have come out on the free cloud compute and how folks can apply for that?</a>
- <a href="#turnover">How does the Rust Foundation plan to deal with the inevitable cycling of folks who are in very important key positions?</a>
- <a href="#community-impressions">What's something that has impressed Bec about the Rust community in Bec's first exposure to it?</a>
- <a href="#communication">How can folks who don't otherwise have a channel communicate with the Foundation?</a>
- <a href="#corporate-membership">How is the growth in the corporate membership of the Foundation changing the approach?</a>
- <a href="#project-directors">Are the number of project directors going to remain constant?</a>
- <a href="#newsletters">Are any weekly newsletters that I might not be subscribed to but you think I should be, what would those be?</a>
- <a href="#hot-dogs">Is a hot dog a sandwich?</a>
- <a href="#outside-sponsorships">Thoughts on some of the other programs that are trying to provide funding to Rust community members?</a>
- <a href="#conclusion">Any final thoughts?</a>

<b id="intro">Sage Griffin</b>: All right. Hello everybody, and welcome to the Rust Foundation Ask Me Anything session. My name is Sage Griffin and I will be moderating today. I'm joined by two wonderful panelists. We have a director of the Rust Foundation's board, the lead editor of <a href="https://this-week-in-rust.org/">This Week In Rust</a> and the bunniest Rustacean, Nell Shamrell-Harrington.

<b>Nell Shamrell-Harrington</b>: Hey, Sage. It's great to be here. I am one of the board directors on the Rust Foundation board. But yes, I am the lead editor of This Week In Rust, and I have three pet bunnies who are the Rust bunnies who make occasional appearances on Twitter and in conference talks.

<b>Sage Griffin</b>: And then we have the new executive director and CEO of the Rust Foundation, Bec Rumbul

<b>Bec Rumbul</b>: Hi Sage, hi Nell. Thank you very much for being here with me today, really looking forward to having a chat.

<b>Sage Griffin</b>: So, as we give the audience a minute to start asking their questions, Bec, this is the first time you've gotten to talk to the community since starting. So how have things been going?

<b>Bec Rumbul</b>: Great. Thank you. I've had such a warm welcome. People have been really, really great, really generous with their time, their advice, their guidance. It's been quite humbling, actually, spending so much time with so many amazing people who are so intelligent and so enthusiastic about what they do. So, yeah, the last few weeks have evaporated, and I'm just really excited to ramp up some of the work of the foundation and have lots more conversations with lovely people.

<b>Sage Griffin</b>: I can imagine it must be exhausting having to get to know such a widely spread-out group of people.

<b>Bec Rumbul</b>: Yeah, time zones are a thing. So, thank you to anyone here that's watching live that has taken time out to dial in early or late or whatever. But yeah, it's great. It's lovely to be working in such a truly global foundation with lots and lots of diverse people.

<b id="governance">Sage Griffin</b>: Absolutely. So let's jump into some of the question that we got. First question we got was, "If Rust were to tweak its governance structure, what open source projects should we seek to emulate?" So Nell, let's go to you first, or would either of you like to speak to what the Foundation's role in Rust's governance is or lack thereof?

<b>Nell Shamrell-Harrington</b>: Sure. I'll go ahead and take a stab at that. So while this is something I could certainly have personal opinions on, it's not the role of the Foundation to direct governance of the Rust Project. We are specifically separate from the Rust Project for that reason. I understand the Project itself is exploring its governance systems, how it could be improved, ways it may need to change. And while we are happy to provide resources and to provide support, both at a Foundation level and on a personal level, it's not something we as a Foundation have an opinion on. Bec, does that ring true to you?

<b>Bec Rumbul</b>: Yeah, definitely. I completely second everything there. There are obviously lots of other examples of other software foundations. I'm not sure anyone out there has completely 100% nailed it. It's a difficult thing and, again, as Nell said, just fully supportive of helping, supporting wherever we can as the Foundation, and if people have ideas, how they might want to approach those changes or reforms, then please do reach out to us.

<b id="inpiration">Sage Griffin</b>: I'm curious though, if we apply that to the Rust Foundation, as opposed to the Rust project itself, are there any other open source foundations that you think the Rust Foundation should be looking at for inspiration?

<b>Bec Rumbul</b>: Well, again, I think that they're all really different. There's no one open source model, is there? It's such an interesting, very, very complex, very fluid sector. There's obviously other foundations that have been around a lot longer than us, and they're very well established, they seem to work pretty well. Obviously Apache has been around for a long time. Linux foundation is a behemoth. So I think it's going to be a while before we get there. But these are foundations that have been very successful, so it would be foolish of us not to look at how they have made themselves a success. But again, we want to be very collaborative and consensus-based in terms of how we push forward with the Foundation. And again, if our governance structure is starting to look like it might not be fit for purpose, then we have to be open to criticism and open to changing that, as long as our lovely border directors, such as Nell, agree.

<b>Nell Shamrell-Harrington</b>: I'd like to add to that. When I was at Mozilla in the very, very early days of starting to discuss the Rust Foundation, we did speak to quite a few different open source foundations and learned a lot from them about what worked and what didn't work for them. Something else I personally learned is while we're not completely unique, the needs of our community and the needs of our users, they are different than other open source language ecosystems out there. So I know that we will be continuing to learn from our peers, and hopefully they're learning from us too.

<b>Sage Griffin</b>: Yeah, absolutely. I remember hearing, of course, early on when that work to start the Foundation was first starting, and it seems like there was a lot of very deliberate work, but so much of it was not particularly public. So it's easy for the community to sort of assume that it didn't happen. Is it fair to say that a lot of the folks who were involved in that early work are still heavily involved in the Foundation?

<b>Nell Shamrell-Harrington</b>: Some definitely are, and we are continuing to learn.

<b id="boundaries">Sage Griffin</b>: So, this ties into something that I've seen a lot in the community, in that it seems like a lot of folks are confused about where the boundaries between the Foundation and the Project are. Is this confusion something that the Foundation is working on addressing and hopefully making it more clear to the majority of the community what the different roles and responsibilities of each side of things are?

<b>Bec Rumbul</b>: Definitely. And it's something that in the conversations that I've managed to have with people thus far, so many people have said, "It'd be really great to know exactly where the boundaries are, what the scope is. What's in the scope, what's not in scope." And I think in the Foundation, I think we have a reasonable idea. I think people in the Project who are very, very involved have a reasonable idea where those boundaries are. But yeah, we have not communicated it well enough, clearly enough thus far. And I think obviously because it's taken some time to get some activities going, it's kind of just been a gray area for people. Hopefully now people will see the Foundation doing many more things that you can point to and say, "Well, that's what the Foundation's doing. And this is what the Project's doing and this is where the intersection is." I hope the more we continue to do things, continue to grow our activities, the more clarity there will be.

<b>Nell Shamrell-Harrington</b>: I'd like to call out Nick Cameron, a fantastic Rust Project member, who recently posted a blog post on what he wants to see from Rust in 2022. And one thing he mentioned was more communication between the Foundation and the community. That is heard loud and clear. And I know it's something Bec has ideas on how we can improve that. And we're looking forward to doing more.

<b id="sponsoring-maintainers">Sage Griffin</b>: Awesome. Well, I'm looking forward to hearing more about that as it happens. So moving on, we've got a few questions coming in from the audience. We've heard some things about a grant program, but nothing about sponsorship. Is the Foundation going to be sponsoring key volunteer maintainers?

<b>Bec Rumbul</b>: So, I think I <a href="https://foundation.rust-lang.org/posts/2022-01-06-happy-new-year-rustaceans-from-bec/">published a blog</a> last week talking about how there's going to be a consultation on the grants program. Grants is just a term for getting money from the Foundation to people, so there's literally been nothing decided yet, everything is on the table. I really, really want as many as people as possible to respond to that consultation once it opens and send us their thoughts, their ideas, their suggestions, anything that they think will make that program a success. So individual sponsorships, yeah, sure, they might be on the table. Everything's on the table at the moment, we're not saying no to anything right now. And we want the community to tell us what's most important to them in terms of where we direct our funds. Obviously, they're not infinite, we will need to make decisions on how to prioritize things. So yes, we want Rustaceans out there to tell us what they think is a priority, where they want that money to go, how that money should be given out. So yeah, maybe there will be one stream where it’s individual sponsorships, maybe there'll be another stream where it's specific kind of projects, events, scholarships, gosh, I don't know. It's all up for grabs right now.

<b>Nell Shamrell-Harrington</b>: We want your input, is my summary of it. If you want to have input on this, we want it. Please help us. And I know that sort of a, what did you call it? A consultation will be opening up soon. And please reach out to Bec, reach out to others. Let's talk, let's make this work.

<b>Bec Rumbul</b>: Sorry, I was just going to say, the 31st of January, that will go live on the website. We just need to obviously confirm what questions we need to ask, we need to get things translated so that people from all around the world can participate equally. So these things take a little time, but we want this to be a really great, successful program.

<b>Sage Griffin</b>: So, is it fair to say then that we'll be seeing some forward momentum on this sooner rather than later?

<b>Bec Rumbul</b>: Sure. Yes. Like I say, the consultation will open the 31st of January, it'll run for about three weeks to enable people to sit down and really think about what they want to tell us. We'll obviously take all those answers away, we'll figure them out, we'll have a look at what the results are. We will publish a high level blog on what those results are. We will use all of that information to figure out, "Okay, these are the priorities that the community has told us we should focus on for this year. This is the way that the majority of people feel that the money should be given out." Ideally, I would like for that whole grants program to open for applications on the 1st of April. So no April fool, just hot cash April 1st, hopefully.

<b>Nell Shamrell-Harrington</b>: Maybe April 2nd, just so there's no confusion.

<b>Sage Griffin</b>: Well, it's awesome to hear that that money will start going out the door soon, because I know ultimately when is that going to happen is sort of the question that's on everybody's minds right now.

<b>Bec Rumbul</b>: And that's fine. I totally understand that. We're not just sitting back and being chill about this and not caring, it's we really want to do it well, so we want to think about it, we want to put the right processes in place, we want to make sure that what people want we can deliver on and how that's going to work. Obviously there's financial admin and bureaucracy behind the scenes that we have to figure out than I'm sure no one else wants to have to worry about, but yeah, I don't want to say, for instance, "Oh yeah, totally, we'll give out loads and loads of grants to people," and it turns out that actually that's going to massively affect their tax status negatively or something. We need to figure these things out so that when it comes to actually being able to push that money out that no one is negatively affected by something that we failed to think about.

<b>Nell Shamrell-Harrington</b>: To just sum up what I'm hearing, we are being deliberate and making sure we set this up for success, and that does take time and effort.

<b id="diverse-interests">Sage Griffin</b>: Absolutely. This is a really hard problem to solve, and it's great to hear that the Foundation is being so thoughtful and deliberate in how they're going about doing it. So moving onto our next question, "This is a delicate ecosystem. Matching programmers with resources needs with tech companies that have their own self interests. How can Rust navigate such a divergent set of interests?" Nell, you in particular wear just absolutely so many hats, I'd love to hear from you first.

<b>Nell Shamrell-Harrington</b>: This honestly was one of my concerns when I was asked to represent Microsoft on the Foundation board of directors. I've been involved with the Rust Project quite some time, I was at Mozilla before I came to Microsoft. But my biggest question is, what am I going to do if Microsoft wants something for Microsoft's purposes but it isn't the best thing for the Rust community? And vice versa, what do I have to answer to if the Rust community wants something that may not be the best thing for Microsoft. And I cannot say that there won't ever be a conflict of interest, there probably will be at some point, to be frank. What I have been learning about is how to navigate that. Honestly, what's good, Microsoft has invested quite a bit in Rust, the thing that makes Rust successful is a thriving community of contributors, as all of us, I believe, on this call know. And in order for Rust to be successful, in order for Microsoft to be successful with Rust, it must have that successful community, that successful, not just technical decision making body, which I know the project is working on now, but also how do we onboard people to Rust, et cetera? 

So it's careful, I don't think a perfect balance is ever achievable, to be frank, because the thing is wavering constantly. But it is something that we are learning about. And having contributors working at different companies, having contributors who are not working at the major tech companies, of which there are many, I believe helps us maintain that balance.

<b>Sage Griffin</b>: Bec, do you have anything to add?

<b>Bec Rumbul</b>: Yeah. I think it's obviously a lot more acute for our member directors now who obviously you have two hats or various hats.

<b>Nell Shamrell-Harrington</b>: All the hats.

<b>Bec Rumbul</b>: All the hats. I think I'm very lucky because I have a plurality of voices that are guiding me. So at the Foundation, we're really, really lucky it's not just one really big corporate fish that's interested in Rust. Rust is so amazing that all of the big corporate players in this space are involved. And that gives us really good balance, certainly, in terms of corporate influence, because we have different voices, different experiences, balanced with project directors who are directly from the community and the teams and who have their own wealth of experience about how things go. So there is a balance, and Nell said it's not going to be 100% perfect every time, and certain issues, different people fall down on slightly either side of the line. But I think we're very, very, as I said, very lucky that we do have this wonderful plurality that can keep us on more of a balance than maybe some other open source communities have found in the past.

<b>Sage Griffin</b>: I guess you're in a unique position here since working for the Foundation is your full time job, you don't have another company that you have to answer to in addition to your responsibilities to the Foundation to the community as a whole.

<b>Bec Rumbul</b>: Sure. I am a servant to the Foundation and the Foundation's aims and goals. We are here to steward the language to support the community, that's my 100% goal. So I almost get to delegate responsibility for worrying about that balance to Nell and the rest of the board directors.

<b id="next-focus">Sage Griffin</b>: So if there's one important thing the Foundation needs to focus on next, but only one to choose, what would that be? Bec, let's hear from you first.

<b>Bec Rumbul</b>: That's hard because there's like 30 balls up in the air right now. How long do I get to choose to pick one before they just all fall down? I think we've already talked about the community grants program, about providing that financial support, I feel like that's the most pressing acute want from the community. I think that's really, really important. And that's kind of what I'm focusing on for the most part at the moment, that's the first three months of this year, is trying to get that properly sorted. That's a very external thing, that's a proper support thing. We have an awful lot of things that we need to sort out internally to make sure that we are an organization that's fit for purpose. We have legal obligations, financial obligations, tax bureaucracy and registration and trademark. So there's a lot of those really quite pressing things as well going on in the background that we're working on. But yeah, those aren't as exciting to most people, I guess, the community grants, that is what's taking most of my focus certainly at the moment. Nell, you might say something completely different.

<b>Nell Shamrell-Harrington</b>: There's two that come to mind. If you'd asked me this six months ago I would have said absolutely a paid on-call rotation for crates.io. That was maintained heroically, although heroically and infrastructure not always words you want to have together, but it was maintained by wonderful, incredible volunteers… that wasn't fair. It was not fair to expect someone who's volunteering to be able to answer a pager or answer a call at all hours of the night. So having that paid rotation, which we have now, for me that has eased my mind, and I think has eased the mind of a lot of users of Rust as well, knowing that crates.io is paid attention to, is being monitored, and if something goes wrong, someone is on duty to respond, who's being paid to do it. For right now, I would say continuing to improve our communication with the community, for me, is top of mind. And this AMA is an example of that, and there are other ways that we can do it too. But making sure, as we talked about before, the community understands the role of the Foundation as it relates to the project, as it relates to the community, et cetera, I think, for me, is the key thing that will allow us to execute all the tactical things that we really, really want to do.

<b id="2022">Sage Griffin</b>: Makes a ton of sense. And actually, that ties nicely into a question I've seen several variations of, so I'm just going to roll a bunch of these up into one. What can we expect from the Foundation in 2022?

<b>Bec Rumbul</b>: A lot of stuff, hopefully. So we do have some outlined plans of where we need to be, as I said, quarter one, January to end of March, beginning of April, we are very, very much focused on that community grant program, trying to get that in shape. Hopefully once that opens then that will roll along without quite so much administrative burden. Other than that, we are looking at, as Nell said, communication is something that we really, really want to get better at. It's a learning curve for all of us, I think, and it's definite something we want to improve our messages, we want to make sure that we are taking the right tone, we're saying the right things, we're consulting with people about the direction. So that's a big thing.

The other things, as I said, that's a lot of building the organization up in terms of getting the right people in to do the work. And really just trying to figure out, and this might sound really, really, a little bit daft, actually, but trying to figure out what the actual problems are that we're trying to solve. As something I think the other day asked me, "Okay, so what problems are you going to try and solve in 2022?" And I think it'd be really useful actually to have a step back from that a step and say, "okay, let's define the actual problems." Because I think there's a lot of symptoms that we can see, but I want to know what's creating those things as well. And again, that hopefully will help us to target what we're actually going to do and what kind of support and resources we can provide. Because obviously, we do have the community grant program, but that's just financial. I want to make sure that the Foundation is also able to put in place things that aren't just monetary, that are resources that people can call upon and drawn upon or services, whatever, that people feel that they need to enable them to do their work better, happier, whatever.

There's just an awful lot that, I have to admit, I don't know yet. And a big part of the first half of this year I think is trying to figure out exactly what those things are. Sorry, I've started rambling a little bit. Nell, take it away.

<b>Nell Shamrell-Harrington</b>: I largely agree with Bec in that we need to define the key problems we want to solve first. That's true of any technical organization or any organization whatsoever. If we try to solve everything at once, nothing gets solved completely. So I'd like us to define which problems we're trying to solve first. On a personal level, over 2021 I was doing some work on improving clarity around license obligations when contributing to the Rust compiler, which is getting very specific. That is something I personally would like to see finished in 2022, so expect more from that in the future. But largely I agree with Bec, defining the problems first and then working on solutions.

<b>Bec Rumbul</b>: It’d be great to hear about innovations from people as well. 

<b>Nell Shamrell-Harrington</b>: Oh, that too, yes.

<b>Bec Rumbul</b>: Yes, definitely defining problems. But if people want to come to us and say, "Do you know I have the beat idea for," I don't know, building or sustaining or improving education or anything. These are things that we want to hear about at well. So very, very, very open to positive innovation as well.

<b id="cloud-compute">Sage Griffin</b>: So we've got a very specific question that either will be very easy to answer or we just won't have an answer for. Have there been any more details that have come out about the free cloud compute stuff and how folks can apply for that?

<b>Bec Rumbul</b>: So, we are working on the details of this in the background. Not everything is ready to go yet. Again, things that we need to do to make this work, things like terms of use policies and those kinds of things. So we do have people working on that. I don't know, Nell, if you know of anything further than that.

<b>Nell Shamrell-Harrington</b>: No, other than that Amazon plus Microsoft plus Google are all donating compute resources, figuring out what compute goes in what cloud, we're solving a multi-cloud problem and I'm looking forward to writing up our use case once we do that. But more is coming. More is to be figured out and revealed. Again, just like the community grants program, we're doing this deliberately, making sure we fulfill legal and financial operations. Having worked at cloud computing providers before, there are legal things you have to consider. So more to be revealed, again, making sure we do it deliberately and set it up for success.

<b>Sage Griffin</b>: All right. I'm looking forward to hearing more about that soon, because this is a very interesting, unique thing that Rust seems to be giving to its contributors that hopefully will be enabling for a lot of folks. Especially just, the compiler compiles very compiley.

<b>Nell Shamrell-Harrington</b>: Yes, even on a very well-resourced laptop. It takes so long. And it's critical for people to be able to contributor to the compiler, especially for newer contributors who may not have access to very high resource work stations to be able to do those faster compiler times, get that feedback, iterate, and get those contributions in.

<b id="turnover">Sage Griffin</b>: Yeah. So back on the topic of project governance or really just the Foundation keeping in touch with the community. The Rust Project itself is primarily driven by volunteers, and volunteers don't last forever. Folks cycle in and out. And in the case of the Foundation, many of the board members are also volunteers. How does the Rust Foundation plan to deal with the inevitable cycling of folks who are in very important key positions, especially when it comes to communication between the project and the Foundation?

<b>Nell Shamrell-Harrington</b>: I think Bec's looking at me. It's hard to tell.

<b>Sage Griffin</b>: Sorry, I should have picked one of you to go first.

<b>Bec Rumbul</b>: We're too polite. It's like, "No you go. No you go."

<b>Nell Shamrell-Harrington</b>: No you go. Yeah, exactly.

<b>Sage Griffin</b>: Nell, you go first.

<b>Nell Shamrell-Harrington</b>: I would say, that in any volunteer led organization, I've been a part of many of them, burnout is a huge issue. I've suffered burnout myself, and it is awful. Also, burnout is not just something you can push through and come out on the other side okay. So part of the reason the Foundation was established, along with having a bank account, having a legal entity, was to directly support maintainers to help prevent exactly this sort of burnout. As things we've helped with immediately, obviously having the paid crates.io rotation we hope will assist with that, not having volunteers on call. That said, there are so many different volunteer roles in the Rust organization. Everything from compiler contributions, of course, but also things like community management, things like moderation, which I've also done those, they are brutal. So I don't have a direct answer on exactly the tactical things we're going to do to prevent that, we are aware it's an issue. There is support coming, and again, we want your input on what that support should be.

<b>Bec Rumbul</b>: Absolutely. I agree with everything Nell's just said there. But I think we need to remember as well that no volunteer should feel bad for reducing hours or just not sitting down at their laptop one day or anything like that. Most people come to this because they want to enjoy what they do with Rust.

<b>Nell Shamrell-Harrington</b>: And if you do feel bad, reach out to me, I'll help you work through it, because I've been there.

<b>Sage Griffin</b>: I can vouch for Nell as a great resource on that, as somebody who has personally done this.

<b>Bec Rumbul</b>: Great, well there's lots of lovely people in this community, so obviously, yeah, reach out to people. But there should never be a message that you should do this or you're obligated to spend another couple of hours doing something. So I just want to make sure that that's very, very clear.

The other thing is, the Foundation is, we're in our infancy, hopefully we can grow to provide the right kind of support so that volunteers don't become burnt out, they leave because they want to do other things. I don't really want volunteers to be leaving the project because they're burning out, I want them to be leaving because they're going on to something that they'd rather do with their time. And maybe that means that we look at different solutions in the future, like as Nell was talking about, crates.io. Do we need to put in place other contracts or other supports to take some of those high volume maybe low value pieces of work, often volunteered, that people don't particularly enjoy doing but someone's got to do them? Are there resources that we can provide so that people understand better how to manage workloads, for instance, or how to have, I don't know streamlined communication. One of the amazing things about Rust is how consensus based it is. But I think we all know as well that lots and lots and lots of communication all the time is pretty exhausting.

So just we are aware of lots of these things. I'm not saying we know right now exactly how we're going to fix them and we want to communicate with everyone on what they think might be best. But I think everything's still on the table here, we want to find the right solution. And I don't think there's a cookie cutter mold that's going to fit 100% first time. But yeah, I really want to keep volunteers in the project that want to stay in the project. And yeah, we'll do whatever we can and take whatever advice we can to try and make that a reality.

<b>Sage Griffin</b>: It is an interesting paradox that most people get into open source because they really like the engineering challenges that open source comes with, but so much of keeping an open source project running, especially a language as large as Rust, there's just so much work to do that has absolutely nothing to do with why most people get into open source in the first place. Obviously not all of that stuff that a Foundation's going to be able to take off people's plates.

<b>Rebecca Rumbul</b>: Certainly not, no, we can't do it all, but we do understand that that is a factor. So yeah, if we can look at certain things that we can take the pressure of then yeah, these are the things that we exist to try and solve. I'd say the other thing as well is, one of the things I really want to do is build a pipeline of new people coming into Rust that will become tomorrow's volunteers. As I say, we can't just rely on people to keep on trucking forever. It would be great to know that there were people are coming through that would be the project directors, members of the Foundation board, in two, three, four years time. And one of the problems I do want to solve is how to get those people without placing an enormous amount of work on existing people to get them there. If anyone has an answer to the postcard, because yeah, it's very, very difficult to figure out that pipeline without overburdening people that are here already.

<b>Sage Griffin</b>: Nell, do you have anything to add on the topic of onboarding new contributors?

<b>Nell Shamrell-Harrington</b>: As I accidentally hit my desk right when I unmute my mic. It's something I think every open source language ecosystem is exploring different ways of doing. And as open source has become more heavily used, I know a Rust community member expressed to me recently, it's great that Rust is being more heavily used by companies, by people, et cetera, but that's putting even more burden on the key maintainers of Rust because all of these pull requests are coming in and someone needs to review those pull requests. It's fantastic people are contributing. I think there's an idea sometime with open source people thinking, "Oh, well it's free labor if you have contributors contributing." No, it's not. We're grateful for those contributions, but someone needs to review them, someone needs to merge them, there might be community discussions, we might have final comment period on issues. We feature those threads in This Week In Rust every week. So there is no one good solution. I do say when I have worked in private teams, we need to consider onboarding a priority along with all our other priorities. And that might mean another priority needs to shift or it needs to be delayed because onboarding is so critical. So those are discussions I think the project will need to have. Again, the Foundation's happy to provide resources on that. Yeah, those are my thoughts on that topic.

<b id="community-impressions">Sage Griffin</b>: One of the other things I think has gotten a lot harder within the project as it's been growing is reaching consensus just in general. If you look at the volume of discussion that happens on an RFC today versus on an RFC that was submitted in, say, 2016, even though the RFC submitted back then might have had bigger implications for the language, it's just ridiculous the volume of communication you have to deal with today to get anything done.
All right, Bec, we got a question for you specifically. What's something that has impressed you about the Rust community in your first exposure to it?

<b>Bec Rumbul</b>:
It's quite two things rolled into one, actually, as I kind of said at the beginning, it's the passion and the commitment and honestly, the sheer intelligence of most people here. I am definitely the dumbest person in most rooms when I'm speaking to the Rust community. And as a community, the way people are so consensus based, they are so concerned about including other people in the decision making process and being thoughtful. I've worked for organizations in the past where they weren't thoughtful, should we say, it was more about just making a very quick decision with as few people around the table as possible and getting things out the door. Where this is really great because so many people have opinions, they're diverse, and I think that makes the final product better. It takes more time, as obviously, Sage, you were just saying about just the sure volume of communications, obviously, having lots of people having an opinion does take time to work through. But yeah, it's just quite inspiring working with people that have this kind of energy and this kind of commitment to what they're doing, and this kind of ownership as well. So many of the people that I've spoken to thus far really just Rust is their baby and it's just pretty awesome. Because, as I say, when you come from other organizations where people just don't care as much, it's really refreshing.

<b>Sage Griffin</b>: Nell, the question wasn't really directed at you, but is there anything you'd like to add?

<b>Nell Shamrell-Harrington</b>: What was the specific question, again?

<b>Sage Griffin</b>: It was what impressed Bec on her first exposure to the Rust community.

<b>Nell Shamrell-Harrington</b>: I can answer for my first exposure to the Rust community, which was 2015, 2016, in there. I was working at Chef Software and I had just started work on the habitat project, which was a distributed systems project that was written in Rust. As I was learning Rust, I ran into some difficulties as everyone does, and particularly a few years ago when there were less resources for learning Rust than there are now. And what I found was I reached out to the community on Discord, I asked questions, and I'm going to date myself a little bit, but when I keynoted RustConf I said, "All right, so something I noticed immediately was in the Rust community, no one calls you a noob." Those of you who weren't around in the '90s internet or weren't as aware of internet in the '90s, that was often a derogatory term used for someone who was new to a language, new to a game, et cetera. No one ever treated me like my concerns were trivial or like my question was stupid. I never felt stupid when I asked even a basic question. And sometimes the response was, "Oh yeah, that is confusing. Let's figure out how we can make that clearer in our docs or clearer in our tutorials."

So I found Rust because I needed to learn a language that was quite good for distributed systems. I stayed with Rust because of the warmth I felt from the community and that I still feel today.

<b id="communication">Sage Griffin</b>: Yeah, it really has been great to see the Rust community grow over the years and how welcoming the community has managed to remain in spite of that growth. So we've talked a little bit about how folks can give feedback on specifically the topic of grants or funding or sponsorships or whatever you want to call it, but more generally, if individuals who aren't part of a company that isn't a member of the Rust Foundation or aren't part of project leadership, how can folks who don't otherwise have a channel communicate with the Foundation?

<b>Bec Rumbul</b>: I'm open to having a chat with anyone. If someone would like to have a chat with me, then just drop me a line. My email is <a href="mailto:rebeccarumbul@rust-lang.org">rebeccarumbul@rust-lang.org</a>. Please reach out. Yeah, I'm trying to speak to as many people as I can anyway. And yeah, if people have specific things that they would like to raise, then I'm very, very happy to talk to them.

<b>Nell Shamrell-Harrington</b>: Your cat is adorable, Sage.

<b>Sage Griffin</b>: This is Murb. If you understand where the cat's name comes from, you have officially been in tech for a little bit too long. Nell, did you have anything you wanted to add on individuals communicating with the Foundation?

<b>Nell Shamrell-Harrington</b>: Reaching out to Bec is a great idea. You can reach out to individual members, depending on what's going on they might direct you to Bec. Bec is our non-partial channel for communications with the Rust community. So yeah, feel free to reach out to me, but if you're not comfortable talking to someone who's affiliated with Microsoft, reach out to someone else, but Bec really should be your first outreach point.

<b id="corporate-membership">Sage Griffin</b>: All right, well that's good to know. So how is the growth in the corporate membership of the Foundation changing the approach? And how is the Foundation ensuring that it remains in touch with the community's needs as the corporate membership grows?

<b>Bec Rumbul</b>: So, I'll jump in first and Nell can follow. We have 20 silver members now, which is wonderful. We obviously have our platinum members as well, who are on the board. Rather excitingly, we're running our first silver member election in a few weeks time, so we will be getting a new board member to represent the silver membership next month. So that's really exciting for us. I totally understand that a lot of people, we were talking a little bit about how people feel really strong ownership over Rust, totally understand how people are wary of corporates influencing the direction or trying to stamp their authority on it. But I'll kind of go back to what I said earlier, which is it's actually really, really useful to have this great group of different corporates that are interested in contributing and supporting the Rust community. A lot of these people, we haven't gone to them with our hands out, they've come to us and said, "We love Rust, we really want to support people. We really want to contribute. We want to help the Foundation. We want to help the community." So they are a huge resource, they bring a lot of expertise and a lot of knowledge into the Foundation, which we need. And yeah, obviously they bring financial resources as well. And they bring a lot of symbolic support, which is really good.

So our growth in membership I think is only a positive thing. And that plurality, I think, provides a really, really great mixing pot of ideas and advice for us. We have the project directors on the board as well though, and they are there to balance out the corporate voices and to make sure that everything we do is rooted in the needs of the community, not the needs of corporate members. So all of our top level decisions, the governance of the whole foundation, is a partnership between the corporate members and the project directors. And Nell, how has that been working over the last year or so? Over to you.

<b>Nell Shamrell-Harrington</b>: I do think it's been working well. There has been some confusion, I've seen the Reddit threads. Yes, I'm in the Rust subreddit, I've seen the threads.

<b>Sage Griffin</b>: I'm so sorry.

<b>Nell Shamrell-Harrington</b>: And I looked at them and they looked into me. But sometimes literally…well maybe not literally, but figuratively. So again, I know there's immense concern that one corporation or multiple corporations could exert too much technical influence on the project. I've heard that concern, I had that concern initially when I was still at Mozilla when just the bare beginnings of the Rust Foundation were being formed. We keep the Project and the Foundation separate for exactly that reason. Maybe this is too American centric, but separation of powers, it exists for a reason so that no one entity can ... And particularly so that the Foundation's members cannot exert undo influence on the technical direction of the Project. So if that is the concern, that's the reason it's set up that way. If the concern is that corporate members could have too much influence on where the Foundation's resources go, as Bec said, that's the reason the project directors are there.
	
Again, a perfect balance, I don't think is achievable, but ongoing, readjusting, shuffling balance, I do believe we have achieved that and will continue to do that. It will take work, but I believe we're well set up for that.

<b id="project-directors">Sage Griffin</b>: Are the number of project directors going to remain constant? Or are we going to see a growth in the number of project directors as the number of corporate directors grows?

<b>Nell Shamrell-Harrington</b>: I don't think that's addressed in the bylaws, that's a very interesting question. Bec, do you happen to know?

<b>Rebecca Rumbul</b>: No. I apologize, I do not know off the top of my head. I have read the bylaws quite a few times, more than is healthy I think. But yeah, there is a cap on the number of people that can be on the board. So it won’t just grow and grow, it's not like three years time everyone will be a member of the board. We are limited to one silver member on the board to represent the whole silver membership. So I think 15 members the cap is set at.

<b>Nell Shamrell-Harrington</b>: Yeah, one of my fellow board members just chimed it, there's a cap of 15 in the bylaws.

<b>Sage Griffin</b>: Shout out to Jane Lusby, one of the other board directors who is just a lovely human being.

<b>Nell Shamrell-Harrington</b>: Oh, she just sent me a heart back. Yay.

<b id="newsletters">Sage Griffin</b>: All right. Well, I've got another question for Nell, specifically. If there are any weekly newsletters that I might not be subscribed to but you think I should be, what would those be?

<b>Nell Shamrell-Harrington</b>: Definitely <a href="https://this-week-in-rust.org/">This Week In Rust</a>. So This Week In Rust, general Rust newsletter. Yes, there's things about specific topics, but it's supposed to be the general pulse of what the community is focused on. That said, there have been some newsletters that have grown around specific interest areas. And we do feature them in our newsletter section when they come out. There's Rust in Gaming, Building an OS with Rust, I think, Rust in OS Dev, Rust in Blockchain, there's several. So I'd say start with This Week in Rust, not just because I'm lead editor of it, though I have wonderful fellow editors who are the reason we get that thing out every single week. But start with This Week in Rust, keep an eye on the other newsletters that are available. And the language is evolving so, so much. And the way people use it is evolving so, so much. It's a wonderful way to get that new technical information, but also hear stories about how people are using Rust in their work and in their personal projects. So Google This Week in Rust, it'll come right up. Or DuckDuckGO, whatever search engine you feel appropriate.

<b id="hot-dogs">Sage Griffin</b>: And since this is an ask me anything, as we wind down I would like to throw both of you a classic ask me anything question. We'll start with Bec, is a hot dog a sandwich?

<b>Bec Rumbul</b>: So, I'm British, I might give a different answer to an American. A British person would say hell no. Hell no, that is an insult to what we understand is a sandwich. But you people in America, you have different understandings of what a sandwich should be. So I will bow to your preferences, being that I'm outnumbered here right now.

<b>Sage Griffin</b>: And Nell, how about you? Is a hot dog a sandwich?

<b>Nell Shamrell-Harrington</b>: The way you hold it is weird if it's a sandwich. But in terms of being things between two, and it's a roll, well then that makes me wonder is a hoagie a sandwich if it's in a roll, it's not two separate pieces of bread? Oh, this is going to go down rabbit holes really, really quickly. So I'd say if we classify it as toppings, or not toppings, but edible things surrounded by bread, I would say yes, a hot dog is a sandwich. But I also know, speaking of weird American sandwiches, there's a thing where people but a burger patty between two crispy cream donuts, I guess they're bread, they're bread-like, but two carbohydrates. And then we get into lettuce wraps and all that. So vaguely, yes, but there are plenty more discussion that could be had on this.

<b id="outside-sponsorships">Sage Griffin</b>: All right. We do have one more serious question that came in at the last moment to close us out. Do either of you have any thoughts on some of the other programs that are trying to provide funding to Rust community members? And do you see the Foundation, the sponsorships, as somehow in competition with them? Bec, let's go to you first.

<b>Bec Rumbul</b>: Not at all. Not at all. I think it's fantastic that there are other sources of funding out there for our fellow Rustaceans. And there is no competition here, we do not want to be a monopoly at the Foundation, I think it's fantastic that there are different sources of funding that people can apply to that work in different ways. So yeah, Devex, for instance, I think it's brilliant that they're providing funding. And yeah, I'm just happy that there are multiple players in this space now. We don't want to create dependencies or anything, so having different funders out there really helps, I think. I don't know, Nell, you're nodding I think you agree?

<b>Nell Shamrell-Harrington</b>: Yeah, the more funding the better. Different ways of accessing that funding, different application processes, different ways of granting it is fantastic. That means we will have more diverse ways of people getting that money they need to continue funding their work. And we have two models, or we will have two models going on with this. This is great, we can see what works for each model, what may not work, and then give that back to the entire open source ecosystem. We touched on this in the call, maintainer burnout, huge problem. Maintainers having money, being paid for their work fairly or at all, huge problem. Having multiple models within the Rust community gives us even more chance for experimentation to figure out what works and what doesn't, and then we can give that to the entire open source ecosystem. I think it's fantastic. And heart to Devex, I hope we can learn from each other. And heart to anyone else who's considering this, that's great.

<b id="conclusion">Sage Griffin</b>: Bec, do you have anything you want to say before we wrap this up?

<b>Bec Rumbul</b>: Yeah, I'd echo what Nell said there. Really chuffed. Sorry, Nell has just learned the British word chuffed today, we had this conversation just before we started. So, I am really chuffed that there are multiple sources, as Nell said, to fund our lovely maintainers. But no, thank you very much, Sage, for moderating this, and for Nell for all your wisdom, and to everyone else that was listening.

<b>Sage Griffin</b>: Nell, any closing remarks from you?

<b>Nell Shamrell-Harrington</b>: Again, thank you so much Sage for moderating. You are my favorite moderator I've ever worked with, and I can say that completely honestly, and I've worked with a lot of them in my speaking career and such. The Foundation is here to serve our maintainers, to serve our larger community. We can't be successful without your help, so please respond to Bec's call for, I keep forgetting what you call it, for input. Call for input that's starting on January 31st. And I'll use I guess maybe the American equivalent of well chuffed, I am ecstatic about what we as a community can do together. Thrilled to be a part of this community, thrilled to be a part of the Foundation, can't wait to keep working and seeing where we go, I think it's going to be someplace good.

<b>Sage Griffin</b>: All right. Well, I'd like to thank both of our panelists for spending the time, and also for the kind words. Thanks to the Foundation for inviting me back as moderator, this has been a blast. For those of you who joined late, this was recorded and the recording will be available on the Foundation's website in the near-ish future. And yeah, with that, I think we can go ahead and wrap this up. So thank you everybody for attending.