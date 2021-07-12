---
title: "Fourth and Fifth Week into the Coding Period"
date: 2021-07-12T18:43:06+05:30
author: "Devyansh"
# cover: "img/<img_name>"
description: "The fourth and fifth week of the Coding period involved implementing Mission 2 of The Userscript Tour completely, and fine tuning of Mission 1."
---

### Summary of the third report
In the previous report, I had provided a detailed walkthrough of implementation of Mission 1 of The Userscript Tour. Since then, I have been working on Mission 2: Developing with ResourceLoader along with fine tuning Mission 1. As my GSoC project is more design-oriented, it certainly requires amendments at various stages. I consult with my mentors every week to bring some changes to already created features.

In these two weeks,  I have completely implemented Mission 2. With that, 50% of the project is done (Phew!). 

Mission 2 is all about making the new developers familiar with **ResourceLoader**, which is MediaWiki's delivery mechanism for assets (JavaScript, Styles, and Localisation text). After going through this mission, the users will gain insights on ResourceLoader and hands-on experience of using RL core modules in userscripts.

### Pages created on MediaWiki
- TUT/2/Start
- TUT/2/Question1
- TUT/2/Question1/1
- TUT/2/Question1/2
- TUT/2/Question1/3
- TUT/2/ResourceLoader/CoreModules
- TUT/Badge/2
- TUT/Badge/2template
- TUT/Badge/2template1
- TUT/2/End

### Userscript created 
- **toggleFontColor.js:** Adds a button to the p-personal portlet area, which when clicked toggles the font-color of the content. It's created to show the use of **mediawiki.util** module.

- **quickChangeLog.js:** Adds a link to the Toolbox portlet area, which when clicked shows 25 most recent changes on MediaWiki in the form of a OOUI message dialog.


### Sequence of steps in Mission 2
1. Developing with ResourceLoader
2. ResourceLoader
3. Are these resources requested separately
4. Module
5. Do I have to request all modules?
6. Hands-On
7. Edit common.js
8. mw.notify()
9. Edit summary and Save Changes
10. Good work!
11. Challenge yourself above
12. mw.loader.using()
13. Toggle font color
14. Play around
15. Sneak Peek
16. All the core modules!
17. Your subpage
18. Check it out
19. The Rationale
20. Load Quick ChangeLog
21. Edit summary and Save Changes
22. Play around
23. Congrats!
24. Mission 2 complete!

Moreover, I have deployed these two missions on **test.wikipedia.org** which is highly convenient as I can ascertain its behaviour when it would be deployed on **mediawiki.org**.

### Glimpses of Mission 2

{{< figure src="/img/Mission 2 example 1.png" alt="A guider showing ResourceLoader definition" caption="A guider showing ResourceLoader definition" position="left" style="border-radius: 6px;">}}

{{< figure src="/img/Mission 2 example 2.png" alt="Quick Changelog dialog" caption="One of the userscripts in Mission 2" position="left" style="border-radius: 6px;">}}