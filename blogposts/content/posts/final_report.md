---
title: "Adieu, Google Summer of Code 2021"
date: 2021-08-20T16:31:14+05:30
author: "Devyansh"
description: It has been a wonderful journey that has taught me how collaboration in an open-source community leads to remarkable results. It's time to wrap up my GSoC '21 project. But the community of Wikimedia Foundation is what I'll cherish for a lifetime.
---

## About
Google Summer of Code is a global program focused on bringing more student developers into open source software development. Students work with an open source organization on a 10 week programming project during their break from school. 

It matches students with open source, free software and technology-related organizations to write code and become part of these communities.

![Google Summer of Code Logo](/img/final/GSoC-logo-horizontal.png)

## Wikimedia Foundation
Wikimedia Foundation provides the essential infrastructure for free knowledge. The Foundation hosts Wikipedia, the free online encyclopedia, created, edited, and verified by volunteers around the world, as well as many other vital community projects. It is the same organization that has helped us in our school projects by providing us legitimate information of about any topic we can think of, by gifting us the mighty **Wikipedia**!

When somebody asks me, *"Hey, what made you write the proposal to Wikimedia Foundation?"*, I smile and ask back another question, *"Could you imagine somebody, living or dead, that works every single day with the sole purpose of providing educational content to the entire world for free?"*

That's the organization I got the opportunity to contribute to this summer.

## What is my GSoC project all about?
**MediaWiki** is the free and open-source wiki softwares that powers some of the well-known wikis - Wikipedia, Wikimedia Commons, Meta-Wiki, to name a few. MediaWiki is at the core of what Wikimedia Foundation does everyday to reinforce its very mission to empower every individual on the planet with the sum of free knowledge.

Thus, to get a good view of how things work in the community, it won't be bad to look at how MediaWiki functions. Infact, one of the easiest ways to get involved in the community is by creating userscripts. You know JavaScript? Very good! You can begin contributing to the organization right away.

**But what's a userscript?**

A userscript is a public JavaScript program that provides Wikimedia users the ability to change the behaviour of their user accounts. Hmm, quite powerful. A userscript is very versatile in a sense that whatever you can do by clicking a ton of buttons on the websites, you can do the same and even more with userscripts. Whether it is creation of a page, authentication, change of appearance of the wiki, etc., userscripts have got you covered.

**My [GSoC project](https://phabricator.wikimedia.org/T279849) was about developing a Userscript Tour for seamless onboarding of new developers on mediawiki.org.** Even though MediaWiki has an exhaustive documentation on userscripts (ofcourse!), it is not interactive. Since userscripts comes with powerful functionalities, one should be able to get started with them easily. The advantage of a Userscript Tour is just that. It ensures that whenever someone outreaches then every participant will go in the same flow.

## The Userscript Tour

The developed userscript tour consists of four missions:
- Mission 1 : Let's begin the jouney
- Mission 2 : Developing with ResourceLoader
- Mission 3 : Strengths of the Action API
- Mission 4 : Novelty of OOUI

The fundamental constructs required to build useful and complex userscripts have been introduced incrementally in each mission. The transition between any two missions is smooth. Thus, they do not look disoriented.

{{< figure src="/img/final/f1.png" alt="Landing page of The Userscript Tour" position="center" style="width: 550px">}}

### Mission 1 : Let's begin the journey
The users will gain practical knowledge of what userscripts/gadgets are and how the existing user scripts are loaded in common.js. They will be made to write a basic yet interesting userscript and import it into their common.js page.

{{< figure src="/img/final/f2.png" alt="Mission 1 starts" position="center" style="width: 550px">}}

### Mission 2 : Developing with ResourceLoader
In this mission, the users will gain practical knowledge of ResourceLoader and the useful core modules available.

{{< figure src="/img/final/f3.png" alt="Mission 2 starts" position="center" style="width: 550px">}}

### Mission 3 : Strengths of the Action API
In this mission, the users will gain practical knowledge of MediaWiki Action API, endpoints, modules, submodules, parameters, and API Sandbox.

{{< figure src="/img/final/f4.png" alt="Mission 3 starts" position="center" style="width: 550px">}}

### Mission 4 : Novelty of OOUI
In the final mission, the users will gain practical knowledge of Object-Oriented User Interface (OOUI), OOUI elements, widgets, dialogs, custom user interface, etc.

{{< figure src="/img/final/f5.png" alt="Mission 4 starts" position="center" style="width: 550px">}}

{{< figure src="/img/final/f6.png" alt="Mission 4 ends" position="center" style="width: 550px">}}

## Work Product
Since this project is a standalone project, it doesn't involve any contributions or patches to existing repositories of the organization. I have created a dedicated GitHub repository that includes all my work.

GitHub repository link: https://github.com/thedevyansh/the-userscript-tour

This repo will also serve as a guide to developers who wish to run The Userscript Tour on their local installation of MediaWiki.

As per the suggestions of my mentors, I have created all the required templates and wikipages on mediawiki.org. To run The Userscript Tour, the interface administrator only needs to create the following pages in the MediaWiki namespace: 
- https://mediawiki.org/wiki/User:Novusistic/Guidedtour-tour-tut1.js
- https://mediawiki.org/wiki/User:Novusistic/Guidedtour-tour-tut2.js
- https://mediawiki.org/wiki/User:Novusistic/Guidedtour-tour-tut3.js
- https://mediawiki.org/wiki/User:Novusistic/Guidedtour-tour-tut4.js

Visit https://www.mediawiki.org/wiki/The_Userscript_Tour, and enjoy the tour :P

## Final words
The past three months as a student developer at Wikimedia Foundation has been nothing short of excitement. I have learned a lot of things along the way by being in an inclusive and diverse community. It's a  community that encourages every member to speak up and feel welcomed.

I am really thankful to my GSoC mentors: [Krishna Chaitanya Velaga](https://meta.wikimedia.org/wiki/User:KCVelaga_(WMF)), [Jay Prakash](https://meta.wikimedia.org/wiki/User:Jayprakash12345), and [Enterprisey](https://en.wikipedia.org/wiki/User:Enterprisey), for their constant support throughout the Program. The project would not have been completed without their invaluable guidance, encouragement, and impeccable knowledge. I hope to keep in touch with these guys even after GSoC ❤️

Also, special thanks to the organization's admins: [Gopa Vasanth](https://www.mediawiki.org/wiki/User:Gopavasanth) and [Srishti Sethi](https://www.mediawiki.org/wiki/User:SSethi_(WMF)) for maintaining a welcoming environment in the community and being such humble people.

## Special mentions
In the initial days of GSoC, an unofficial Discord server was made that includes GSoC 2021 participants (great idea!). It's been consequential to be in that community as well. I got to learn about varied perspectives of other students. These students are some of the best in India.They have a knack of what they do. Their passion and expertise has been a source of motivation for me throughout the Program.

Highly competitive and helpful peeps! 

Thank you readers! I'll see you again pretty soon :)
