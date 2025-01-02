---
layout: post
title: Raking The Leaves
date: 2024-9-11 10:18:00
categories: [.NET, Community]
---

 The first task I worked on this week was improving the UI on the Admin page. I started by removing grammatical mistakes, as well as internal variable names that had worked their way into the view. I began separating the model and view of the data on the Admin page more, next I will continue to improve site color, make the buttons more intuitive. Then, I will work on adding sorting and searching features, what good is data if you can’t look at it?
The other project of this week has been refactoring. I’ve deleted 84 files, and 15,000 lines of code. I’ve noticed an immediate improvement in speed. Many of the old functions of the website have now been migrated to the current ly used indexing page. I deleted the remnants of the site built on HTML, CSS, JS, bootstrap, and query technologies, which were interfering with the sites current ASP.NET build. Also, I followed the old dependencies and removed them from the code. The next step will be refactoring individual pages to make the site more clear and able to be unit tested. 