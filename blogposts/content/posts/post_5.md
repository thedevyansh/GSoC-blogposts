---
title: "Sixth and Seventh Week into the Coding Period"
date: 2021-07-29T22:50:12+05:30
author: "Devyansh"
# cover: "img/<img_name>"
description: "The sixth and seventh week of the Coding period involved implementing Mission 3 of The Userscript Tour."
---

### Summary of the third report

In the past two weeks,  I have worked on Mission 3 of The Userscript Tour i.e. Strengths of the MediaWiki Action API, and made some amendments in the order of guiders and demo userscripts as per the suggestions from the mentors.

Mission 3 introduces the users to the MediaWiki Action API, which is a web service that facilitates wiki operations such as editing a page, deleting a page, getting information about a page, authenticating the user and so much more. This mission gives users the base required to start using the API in userscripts.

### Pages created on MediaWiki
- TUT/3/Start
- TUT/Badge/3
- TUT/Badge/3template
- TUT/Badge/3template1
- TUT/3/End

### Userscripts created 
- **basicPageInfo.js:** Shows the basic infomation about the current page (number of bytes/characters) at the top of the content area. This userscript is written to help users get started with making API calls to the Wikimedia servers.

- **quickChangeLog.js:** Adds a link to the Toolbox portlet area, which when clicked shows 25 most recent changes on MediaWiki in the form of a jQuery dialog box. Initially, I added this userscript in Mission 2. However, it didn't fit well in the context of what I was trying to demonstrate, thus it was replaced.


### Sequence of steps in Mission 3
1. Welcome back!
2. MediaWiki Action API
3. What can it be used for?
4. Interesting use case
5. Hands-on
6. Your subpage
7. Sneak Peek
8. The Rationale
9. Edit common.js
10. Load the userscript
11. Edit summary and Save Changes
12. Number of bytes
13. Endpoints
14. Module, submodule, parameter
15. Where to go for reference?
16. Lots of use cases!
17. Your subpage
18. Check it out
19. The Rationale
20. Load Quick ChangeLog
21. Edit summary and Save Changes
22. Play around
23. Congrats!
24. Mission 3 complete!


### Issues faced
I had decided to tell users how to test their API calls in the API Sandbox, since Sandbox is a great place to customize requests and analyze the response. However, I soon realized that while navigating to different sections, the page doesn't reload.

This means that the chainable **transition()** method of the GuidedTour extension won't run at all since it doesn't listen to events such as onclick, onmouseover, etc. And thus the guiders will not change on their own in the API Sandbox. I looked up for stuff like mediawiki hooks, but it didn't work. I am yet to figure out the possible solution.
