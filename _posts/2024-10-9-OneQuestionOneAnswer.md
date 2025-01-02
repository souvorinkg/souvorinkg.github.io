---
layout: post
title: "One Question, One Answer"
date: 2024-10-9
categories: [Hendrix Arboretum]
---

The main project of this week was refactoring the TreeURL to reduce complexity and make the site easier to manage. If we need oneURL, it should be calculated in a single place. 

At the beginning of this week, the treeURL was working, but still a mess, and it was missing lots of images. Now, it gets all of the images, once and doesn’t rely on each individual function to get the image. I removed a lot of duplicate code, and the logic of the site is much cleaner now. I did this by calculating and checking for a URL in the tree class itself, which then calls a function that gets its own URL. Then, you can access the URL anywhere, without worrying about how to calculate it. This has reduced the complexity of the site, and in doing so has made some older bugs clear, hence now all of the images are appearing. Moving forward, there are still some issues. Currently, the url is generated and checked when one asks for it, which is precisely the worst time, as then you don’t have a URL when you need one! It’d be excellent for site speed if all of the URLs were being built while you read through the site description, so that by the time you got around to asking for them they were in your hands. Second, there is a table that lists all of the trees, and whether those trees have valid URLs, ie not the stock photo. When you look at the table, the tree is always labeled “stock photo.jpg,” yet when you click the details of the tree, the correct photo is lying under the surface! This is quite bizarre, and could be fixed. These two issues are pretty related and are the last things standing in the way of all of the refactoring that needs to be done to achieve both speed and coverage. 

After some more work, all of the Trees in the tree table have a boolean checking whether the URL is valid for the given tree. This is very convenient! The table only checks the trees it needs to, which is a good time saver. However, it’d be nice if this information was already ready, since we tend to ask for this information a lot throughout the site. 