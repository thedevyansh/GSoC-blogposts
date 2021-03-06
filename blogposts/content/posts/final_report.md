---
title: "Adieu, Google Summer of Code 2021"
date: 2021-08-20T16:31:14+05:30
author: "Devyansh"
description: It has been a wonderful journey that has taught me how collaboration in an open-source community leads to remarkable results. It's time to wrap up my GSoC '21 project. But the community of Wikimedia Foundation is what I'll cherish for a lifetime.
---
{{< figure src="/img/final/GSoC-logo-horizontal.png" alt="Google Summer of Code Logo" style="margin: 25px 0;">}}
## ✨ About
Google Summer of Code is a global program focused on bringing more student developers into open source software development. Students work with an open-source organization on a 10-week programming project during their break from school. 

It matches students with open source, free software, and technology-related organizations to write code and become part of these communities.

## ✨ Wikimedia Foundation
Wikimedia Foundation provides the essential infrastructure for free knowledge. The Foundation hosts Wikipedia, the free online encyclopedia, created, edited, and verified by volunteers around the world, as well as many other vital community projects. It is the same organization that has helped us in our school projects by providing us legitimate information about any topic we can think of, by gifting us the mighty **Wikipedia**!

When somebody asks me, *"Hey, what made you write the proposal to Wikimedia Foundation?"*, I smile and ask back another question, *"Could you imagine somebody, living, that works every single day with the sole purpose of providing educational content to the entire world for free?"*

That's the organization I got the opportunity to contribute to this summer.

## ✨ What is my GSoC project all about?
**MediaWiki** is the free and open-source wiki software that powers some of the well-known wikis - Wikipedia, Wikimedia Commons, Meta-Wiki, to name a few. MediaWiki is at the core of what Wikimedia Foundation does every day to reinforce its very mission to empower every individual on the planet with the sum of free knowledge.

Thus, to get a good view of how things work in the community, it won't be bad to look at how MediaWiki functions. One of the easiest ways to get involved in the community is by creating userscripts. Do you know JavaScript? Very good! You can begin contributing to the organization right away.

**But what's a userscript?**

A userscript is a public JavaScript program that provides Wikimedia users the ability to change the behavior of their user accounts. Hmm, quite powerful. A userscript is very versatile in the sense that whatever you can do by clicking a ton of buttons on the websites, you can do the same and even more with userscripts. Whether it is the creation of a page, authentication, change the appearance of the wiki, etc., userscripts have got you covered.

**My [GSoC project](https://phabricator.wikimedia.org/T279849) was about developing a Userscript Tour for seamless onboarding of new developers on mediawiki.org.** Even though MediaWiki has exhaustive documentation on userscripts (of course!), it is not interactive. Since userscripts come with powerful functionalities, one should be able to get started with them easily. The advantage of a Userscript Tour is just that. It ensures that whenever someone outreaches then every participant will go in the same flow.

## ✨ The Userscript Tour

The developed userscript tour consists of four missions:
- Mission 1: Let's begin the journey
- Mission 2: Developing with ResourceLoader
- Mission 3: Strengths of the Action API
- Mission 4: Novelty of OOUI

The fundamental constructs required to build useful and complex userscripts have been introduced incrementally in each mission. The transition between any two missions is smooth. Thus, they do not look disoriented.

{{< figure src="/img/final/f1.png" alt="Landing page of The Userscript Tour" position="center" style="width: 550px;">}}

### Mission 1: Let's begin the journey
The users will gain practical knowledge of what userscripts/gadgets are and how the existing userscripts are loaded in common.js. They will be made to write a basic yet interesting userscript and import it into their common.js page.

**Userscripts involved:**
- **Invert.js:** Adds an Invert link to the top toolbar. It allows inverting the page color and the color of images.

- **zoom.js:** Adds two buttons (to zoom-in and zoom-out)) on the right of the page heading.

{{< figure src="/img/final/f2.png" alt="Mission 1 starts" position="center" style="width: 550px;">}}

### Mission 2: Developing with ResourceLoader
ResourceLoader is the delivery system in MediaWiki for JavaScript, CSS, interface icons, and localisation text. It oads script and style resources on-demand and only for browsers that are capable of running them.

In this mission, the users will gain practical knowledge of ResourceLoader and the core modules available.

**Userscripts involved:**
- **toggleFontColor.js:** Adds a link to the p-personal portlet area, which when clicked toggles the font color of the content. It is created to depict the use of mediawiki.util module.

- **userEditCount.js:** Shows the count of edits made by the logged-in user on the current wiki beside the username.

{{< figure src="/img/final/f3.png" alt="Mission 2 starts" position="center" style="width: 550px;">}}

### Mission 3: Strengths of the Action API
The MediaWiki Action API is a web service that allows access to some wiki-features like authentication, page operations, and search. It can provide meta information about the wiki and the logged-in user.

In this mission, the users will gain practical knowledge of MediaWiki Action API, endpoints, modules, submodules, parameters, and API Sandbox.

**Userscripts involved:**
- **basicPageInfo.js:** Shows the basic information about the current page (number of bytes/characters) at the top of the content area. This userscript is written to help users get started with making API calls to the Wikimedia servers.

- **quickChangeLog.js:** Adds a link to the Toolbox portlet area, that when clicked shows the 25 most recent changes on MediaWiki in the form of a jQuery dialog box. 

{{< figure src="/img/final/f4.png" alt="Mission 3 starts" position="center" style="width: 550px;">}}

### Mission 4: Novelty of OOUI
OOUI allows developers to create responsive web user-interfaces and applications. It is internationalization ready with full support of right-to-left languages, is accessible complying to Web Content Accessibility Guidelines and operates consistently across a multitude of browsers.

In the final mission, the users will gain practical knowledge of Object-Oriented User Interface (OOUI), OOUI elements, widgets, dialogs, custom user interface, etc.

**Userscripts involved:**
- **showAlertBox.js:** Appends an OOUI button to the portlet area that when clicked, shows an OOUI Message Dialog (a simple alert box).

- **guessRandomNumber.js:** One of the cool userscripts which makes use of custom widgets. It prepends a tiny random game at the top of the wiki page. The OOUI widgets used are: *MessageWidget, LabelWidget, TextInputWidget, ButtonWidget and Simple Message Dialog Box.*

{{< figure src="/img/final/f5.png" alt="Mission 4 starts" position="center" style="width: 550px;">}}

{{< figure src="/img/final/f6.png" alt="Mission 4 ends" position="center" style="width: 550px;">}}

## ✨ Other hightlights

- A welcome message is sent to the Talk page when the user initiates The Userscript Tour (Mission 1).

{{< figure src="/img/final/f7.png" alt="Welcome message on Talk page" position="center" style="width: 550px;">}}

- For further engagement, the user is awarded badges for small accomplishments; for example, a badge for loading the first userscript, another badge for completing a Mission, etc.

{{< figure src="/img/final/f8.png" alt="A badge awarded in Mission 1" position="center" style="width: 550px;">}}

- The badges are sent to a subpage of the user. The user consent is taken before writing anything to the pages of the User namespace.

{{< figure src="/img/final/f9.png" alt="All badges awarded in The Userscript Tour" position="center" style="width: 550px;">}}

## ✨ Work Product
Since this project is a standalone project, it doesn't involve any contributions or patches to existing repositories of the organization. I have created a dedicated GitHub repository that includes all my work.

GitHub repository link: https://github.com/thedevyansh/the-userscript-tour

This repo will also serve as a guide to developers who wish to run The Userscript Tour on their local installation of MediaWiki.

As per the suggestions of my mentors, I have created all the required templates, wiki pages, and userscripts on mediawiki.org. To run The Userscript Tour, an interface administrator only needs to create the following pages in the MediaWiki namespace: 
- [Guidedtour-tour-tut1.js](https://mediawiki.org/wiki/User:Novusistic/Guidedtour-tour-tut1.js)
- [Guidedtour-tour-tut2.js](https://mediawiki.org/wiki/User:Novusistic/Guidedtour-tour-tut2.js)
- [Guidedtour-tour-tut3.js](https://mediawiki.org/wiki/User:Novusistic/Guidedtour-tour-tut3.js)
- [Guidedtour-tour-tut4.js](https://mediawiki.org/wiki/User:Novusistic/Guidedtour-tour-tut4.js)

Visit [The_Userscript_Tour](https://www.mediawiki.org/wiki/The_Userscript_Tour) and enjoy the tour :P

## ✨ Final words
The past three months as a student developer at Wikimedia Foundation have been nothing short of excitement. I have learned a lot of things along the way by being in an inclusive and diverse community. It's a  community that encourages every member to speak up and feels welcomed.

I am thankful to my GSoC mentors: [Krishna Chaitanya Velaga](https://meta.wikimedia.org/wiki/User:KCVelaga_(WMF)) (**volunteer account:** [KCValega](https://meta.wikimedia.org/wiki/User:KCVelaga)), [Jay Prakash](https://meta.wikimedia.org/wiki/User:Jayprakash12345), and [Enterprisey](https://en.wikipedia.org/wiki/User:Enterprisey), for their constant support throughout the Program. The project would not have been completed without their invaluable guidance, encouragement, and impeccable knowledge. I hope to keep in touch with these guys even after GSoC ❤️

Also, special thanks to the organization's admins: [Gopa Vasanth](https://www.mediawiki.org/wiki/User:Gopavasanth) and [Srishti Sethi](https://www.mediawiki.org/wiki/User:SSethi_(WMF)) for maintaining a welcoming environment in the community and being such humble people.

## ✨ Special mentions
In the initial days of GSoC, an unofficial Discord server was made that includes GSoC 2021 participants (great idea!). It's been consequential to be in that community as well. I got to learn about their experiences and varied perspectives. These students have a knack for what they do. Their passion and expertise have been a source of motivation for me throughout the Program.

I am glad to interact with some of the most competitive yet super helpful and generous peeps! 

**.**

**.**

Thank you! I'll see you again pretty soon :)