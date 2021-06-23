---
title: "A week into the Coding Period"
date: 2021-06-15T14:51:10+05:30
author: "Devyansh"
# cover: "img/<img_name>"
description: "First week of the Coding Period was occupied with a lot of insights into the project, and initiating the coding of the landing interface & first mission of The Userscript Tour."
---

### Summary of the first report
In the previous report, I had talked about getting familiar with Phabricator, Gerrit, recipes of user script development i.e. ResourceLoader, Action API, and OOUI. I was involved into understanding the intricacies of the GuidedTour extension and analyzing The Wikipedia Adventure.

On the next day of writing the first report, I had a formal meeting with all the mentors in which we got to know about each other and had a detailed discussion regarding MediaWiki in general and revamping the project milestones.

### Final week of the Community Bonding Period
After the meeting with the mentors, I was left with setting up the testing framework that MediaWiki uses for its JavaScript testing: **QUnit**, and researching the game themes for the Tour. Although it's simple enough to view the tests' results in the browser by navigating to **Special:JavaScriptTest**, it took a while to understand the pipeline of MediaWiki modules' testing in CLI.

Before conducting the tests in CLI, I installed a **Fresh** environment which is a fast and ready-to-use Docker container with various developer tools pre-installed including Node.js, and headless browsers. Fresh basically ensures running npm packages on our machine, without putting our personal data at risk.

{{< figure src="/img/qunit-testing.png" alt="QUnit testing results in the browser" caption="QUnit testing results in the browser" position="left" style="border-radius: 6px;">}}

I researched various game designs to incorporate in the Tour. My search was filtered based on the following parameters: consistency with the interface of MediaWiki, engaging, and not so overwhelming.

### First week of the Coding Period
I again had a meeting with mentors on 8th July in which I presented a prototype of the landing page of The Userscript Tour which I made, and proposed the workflow of how the things would come together in Mission 1. There were discussions on the design, color palette, sequence of guiders, and more. One crucial advice given to me was to only use Creative Commons licensed resources as those are the ones accepted on Wikimedia Commons.

#### Coding begins
**Templates:**

I initiated by designing the interface of the main Tour page based on the feedbacks, followed by creating various wiki pages relevant to the first mission. It includes wiki pages to ask questions from the user, to show the sample user scripts, and to show the final page when a mission concludes.
Before creating any of the wiki pages, I planned ways to avoid duplicating the wikitext in the current and in other missions.

To handle this, I created templates first. So now I have templates for navigation links, different headers, different backgrounds, tour status, badges, user script questions etc. This has and will facilitate me to transclude the templates and pass the required data as parameters to these templates, thus making it easier to manage changes in different wiki pages and avoiding redundancy & reproducibility.\
Following shows few names of the templates that I've created:
- MediaWiki:TUT/Navigation
- MediaWiki:TUT/Logo/1
- MediaWiki:TUT/Background/1
- MediaWiki:TUT/Status
- MediaWiki:TUT/1/UserscriptQuestion
- MediaWiki:TUT/1/End and more...

**Guiders and the GuidedTour Extension:**

After creating the wiki pages, I went forward to create the guiders/steps which are the foundation of the Tour. The following shows the sequence of guiders, I have developed till now, for Mission 1:
1. Welcome to The Userscript Tour
2. Know before you go
3. What is a user script?
4. Gadgets
5. Please welcome common.js!
6. Login or create an account
7. What's this common.js?
8. Your common.js!
9. Sneak Peek!
10. What's going on here?
11. Edit common.js
12. Let's load the user script
13. Edit summary and Publish
14. Congrats on earning a badge!

A typical guider is implemented as shown

```javascript
tour.step({
		name: '3',
		title: 'What is a user script?',
		description: 'Put your description here.',
		onShow: gt.parseDescription,
		overlay: false,
		closeOnClickOutside: false,
		buttons: [ {
			name: '<big>←</big>',
			action: 'externalLink',
			url: mw.util.getUrl( 'MediaWiki:TUT/1/Start' ) + '?tour=tut1&step=2'
		}, {
			name: 'And gadgets?',
			action: 'next',
		} ],
		allowAutomaticOkay: false

	})
	.next('4');
```

which results in
{{< figure src="/img/guider-example.png" alt="A guider example" position="left" style="border-radius: 6px;">}}

### Issues faced
1. When I was importing certain templates from English Wikipedia such as Template:Center, Template:Clear, etc. I ran into an error which stated **'sanitized-css' content model was not registered.** This happened specifically due to a template - Clickable Button 2, which depends on various modules containing sanitized-css, and there was no extension available in my MediaWiki-Docker to handle this content model. So I installed TemplateStyles extensions to have the required content model registered.

2. To parse the wikitext in guiders' description, **mw.guidedTour.parseDescription** works like a charm, but it has been deprecated for a while now. So I tried replacing  it with **mw.guidedTour.WikitextDescription** or **mw.Title** object, however, the images on the guiders aren't showing. I'm still to figure out the solution to this.

### What's next?
For the upcoming two weeks, I plan to complete the implementation of Mission 1, followed by its unit testing and writing its story on MediaWiki. Further, I'll try to implement Mission 2 completely. 

Wish me luck :)