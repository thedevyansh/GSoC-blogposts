---
title: "Community Bonding Period: Two weeks down"
date: 2021-05-30T15:05:53+05:30
author: "Devyansh"
# cover: "img/<img_name>"
description: "The first two weeks of the Community Bonding Period as a Google Summer of Code 2021 intern at Wikimedia Foundation were filled with loads of excitement as I stepped forward to become a part of an open source community."
---

{{< figure src="/img/wmf-logo.png" alt="WMF logo" caption="Wikimedia Foundation" position="center" >}}

Soon after I got to know that I've been accepted to Google Summer of Code '21, there were several occasions of celebration. It gives me immense pleasure to have the opportunity coming my way to contribute to Wikimedia Foundation by working on an
exciting project: To develop a UserScript/Gadget tutorial on MediaWiki.org similar to The Wikipedia Adventure ([T274635](https://phabricator.wikimedia.org/T274635)).

### Wikimedia Hackathon and Interns Welcome Party
The [Wikimedia Hackathon 2021](https://www.mediawiki.org/wiki/Wikimedia_Hackathon_2021) took place as a remote event from May 21 to May 23. Since it was open to all people who are interested in discovering the technical aspects of Wikimedia projects and socializing with other participants, I found it a key event that helped me with the onboarding process. On May 23, a [GSoC and Outreachy Welcome Call](https://www.mediawiki.org/wiki/Google_Summer_of_Code/2021#/media/File:Google_Summer_of_Code_2021_and_Outreachy_Round_22_Welcome_Call.png) was conducted in which we interns interacted with each other & Foundation's administrators. The call concluded with one of the talented peeps playing the guitar :) It was quite a warm welcome!

Two weeks down, one left, I focused on the tools and technologies which are going to be of utmost importance while implementing the project. These are described below:

### Phabricator and Gerrit
The terms themselves really fascinated me. Before digging deep into Phabricator and Gerrit, I had a vague idea of them. I had an intuition that I am going to be using them a lot during the Coding Period and it seems like the intuition is correct.

- [Phabricator](https://phabricator.wikimedia.org/) is a collaboration platform open to all Wikimedia contributors. It is mostly used for managing work in software projects. I got myself familiar with it by looking at the various projects and tasks (also called tickets) that the community collaborates on. The general idea I developed is that people use Phabricator to manage their entire project workflow such as bug fixes, feature requests, etc.

- [Gerrit](https://gerrit.wikimedia.org/r/q/status:open+-is:wip) is a code review tool used by Wikimedia. It basically acts as a bridge between writing code and merging the code with the official repos. I guess I am going to be using Gerrit for hosting the code and getting it reviewed by the mentors, instead of GitHub as mentioned in my Proposal

### ResourceLoader, MediaWiki Action API, OOUI
The Missions of the Guided Adventure Tour involve the use of Javascript constructs: ResourceLoader, Action API, and OOUI. Thus, it was important for me to get sufficiently well versed with their usage in user scripts/gadgets.

- [ResourceLoader](https://www.mediawiki.org/wiki/ResourceLoader) is a mechanism to intelligently deliver the assets (JS, CSS, interface icons, localization text) in wikis. It's highly performant. I started with the core modules that ship with MediaWiki by default i.e, mediawiki and jquery. These two modules are always present and thus can't be declared as dependencies. It took me some time to get familiar with their properties and methods such as the stable config keys that could be read from **mw.config**. Later, I looked up the documentation of other ResourceLoader modules useful for the project such as  ooui-js-core, ooui-js-widgets, oojs-ui.styles.icons-*, etc. Major insights were gained when I studied gadget-definitions (which showed gadgets are bound to interact with ResourceLoader).

- Initially, I was a bit overwhelmed by the realm of [MediaWiki Action API](https://www.mediawiki.org/wiki/API:Main_page). As I went forward, I could make sense of all the use cases. The modules, submodules, and parameters of the web service and how they can be used for authentication, accounts & users, page operations, and other wiki operations became clear.

- [OOUI](https://www.mediawiki.org/wiki/OOUI) is the widget-based UI library that caught my attention the most. The fact that DOM and data flow concerns are kept separate, makes it really flexible to handle complex interfaces. I was able to get a clear intuition of the base principles of classes and widgets (represent DOM elements). Creating DOM elements easily using base widgets, custom widgets and internationalization are some of the features which make it very powerful.

### GuidedTour Extension
The [GuidedTour](https://www.mediawiki.org/wiki/Extension:GuidedTour#:~:text=The%20GuidedTour%20extension%20provides%20a,interactive%20tutorials%20for%20MediaWiki%20features.) extension provides a framework to create interactive tutorials or guided tours for MediaWiki features. Guided tours can be created by editing the wiki (the logic resides in the MediaWiki namespace) or by bundling the tour with the extension. Since my project demands the development of an interactive tutorial, GuidedTour extension is the key to the entire project. All the missions will be on-wiki tours.

To get a solid understanding of GuidedTour, I consulted the design recommendations and the [API documentation](https://doc.wikimedia.org/GuidedTour/master/#!/api/mw.guidedTour). I went through the `test` and `first edit` tours which are packaged with the extension, to gain practical insights into how guiders are defined, created, and linked together. Guiders' customizations are of interest as well.

### The Wikipedia Adventure
I completed [The Wikipedia Adventure](https://en.wikipedia.org/wiki/Wikipedia:The_Wikipedia_Adventure) to get the experience of being guided by walkthroughs and understand the creative process of the Adventure's developers. Then I looked at the implementation of the 1st mission of TWA to get acquainted with various API parameters of **mw.guidedTour** and applications of the Action API used, such as sending messages to our own user page on Wikipedia.

To change the default styling of the steps/guiders, I had initially thought of overriding `custom.css` in the MediaWiki namespace. However, TWA gave me a better idea to write the guider description using wikitext and parse it. After all, deciding the look of elements on a guider has a huge impact on how it will look irrespective of the default styling like the font, buttons, etc. I went further to analyze the Adventure's story and its user satisfaction statistics. This truly helps in identifying the overall UX which could point out the loopholes in the tour. Moreover, I liked the very idea of event logging and *"Hang out in the Interstellar Lounge"* in the tour.