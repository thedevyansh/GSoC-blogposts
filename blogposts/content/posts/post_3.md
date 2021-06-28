---
title: "Second and Third Week into the Coding Period"
date: 2021-06-28T16:43:00+05:30
author: "Devyansh"
# cover: "img/<img_name>"
description: "The second and third week of the Coding Period involved implementing Mission 1 of The
Userscript Tour completely and working on Mission 2: Developing with ResourceLoader."
---

### Summary of the second report
In the previous report, I had described my experience of setting up the QUnit testing environment for JavaScript and creating the templates for Mission 1 of the Tour. The report also included details of the sequence of steps of guiders that were implemented by that time.

In these two weeks, I had two meetings with the mentors - on Tuesdays i.e. June 15 and June 22. The discussions mostly revolved around improving the landing interface and workflow of Mission 1. I was specifically told to use gender-neutral images in the interfaces that I create and how I could work on the missions to create a more solid learning experience for the users.

The following includes details of my complete work on **Mission 1: Let's get started** and partial work on **Mission 2: Developing with ResourceLoader** -

#### MISSION 1
I'm done with the main interface of The Userscript Tour. All the wikipages have been created using nested templates. The main motivation behind using the templates to the maximum possible extent is to facilitate easy picking & plugging of the templates to create the interfaces easily and without much of replication in the markup syntax.
The names of the templates and pages that I've made are listed below:
- MediaWiki:TUT/Navigation
- MediaWiki:TUT/Navigation1
- MediaWiki:TUT/Welcome
- MediaWiki:TUT/Logo/1
- MediaWiki:TUT/Logo/2
- MediaWiki:TUT/Logo/3
- MediaWiki:TUT/Background/1
- MediaWiki:TUT/Background/2
- MediaWiki:TUT/Background/3
- MediaWiki:TUT/Background/4
- MediaWiki:TUT/Message/1
- MediaWiki:TUT/Status
- MediaWiki:TUT/1/Userscript1
- MediaWiki:TUT/Badge
- MediaWiki:TUT/Badge/1
- MediaWiki:TUT/Badge/1template
- MediaWiki:TUT/Badge/1template1
- MediaWiki:TUT/1/Start
- MediaWiki:TUT/1/End
- MediaWiki:TUT/YouBeforeYouStart
- MediaWiki:TUT/Portal
- MediaWiki:The_Userscript_Tour

These pages (and templates) have been pretty much created to be used in multiple missions, and guess what, they are already proving useful in the initial stages of Mission 2 itself.

{{< figure src="/img/Landing interface.png" alt="Landing interface" caption="Landing interface of The Userscript Tour" position="left" style="border-radius: 6px;">}}

The first mission contains 24 steps to walk user through the process of understanding what userscripts are and how they can be created (using basic JavaScript/jQuery constructs only) and loaded in user's common.js file.

Sequence of steps in this mission:
1) Welcome to The Userscript Tour
2) Know before you go
3) What is a user script?
4) Gadgets
5) Please welcome common.js!
6) Login or create an account
7) What's this common.js?
8) Your common.js
9) Sneak Peek!
10) What's going on here?
11) Edit common.js
12) Let's load the user script
13) Edit summary and Publish
14) Congrats
15) Play around
16) Your user subpage
17) Sneak Peek!
18) The Rationale
19) What's next?
20) Edit common.js
21) Load the user script
22) Edit summary and Publish
23) You are impressive!
24) Mission 1 complete!

Glimpses of Mission 1 are shown below:

{{< figure src="/img/Mission 1 example 1.png" alt="Mission 1 example 1" position="left" style="border-radius: 6px;">}}

{{< figure src="/img/Mission 1 example 2.png" alt="Mission 1 example 2" position="left" style="border-radius: 6px;">}}


After the consultation with my mentors, I deployed the code of Mission 1 on **mediawiki.org** in the Main namespace. It won't work yet since the code of guided tour (MediaWiki:Guidedtour-tour-tut1.js) is not yet available in the MediaWiki namespace. Hope it gets deployed there soon. Fingers crossed!

#### MISSION 2
I've started working on Mission 2 of the Tour and till now created 7-8 guiders. These guiders explain the user about:
- what ResourceLoader is
- which resources can be shipped by ResourceLoader (i.e. JavaScript, styles, interface icons, and localisation text)
- what ResourceLoader Client is
- asking user a question regarding the properties of modules and awarding them a badge, should he/she answer it correctly

### Issue faced
In order to conform with the WikimediaUI, I decided to use the OOUI alert (**OO.ui.alert**) instead of the default browser alert, in case the problems arise while logging in or sending messages to personal MediaWiki pages. However, the OOUI alert was always beneath the guiders! The obvious reason was, ofcourse, the z-index of the guiders which was way too high than that of the alert (in this case, 100000004 against 101). I couldn't find any simple way to customize the properties of OO.ui.alert. 

Thus, I used the OOUI message dialogue (**OO.ui.MessageDialog**) as it provided me more flexibility in terms of APIs and available properties to change the very behaviour of alert widget.

It worked :P

