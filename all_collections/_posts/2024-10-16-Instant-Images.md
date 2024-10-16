---
layout: post
title: "One Question, One Answer"
date: 2024-10-9
categories: [Hendrix Arboretum]
---

The main project this week was calculating the ImageURLs in advance, instead of dynamically. 

At first, I created a seperate table where I wrote the ImageURLs, then I would search this table when I had a question of whether something existed in the DB. However, the relationship between URL and Tree is one-to-one, so I moved the TreeURL to be an aspect of the Tree class. 

The big result of this work, is for the first time, we have instant tree loading everywhere! 

Moving forward, there is one more task on the ImageURL front, there should be a button that gets the list of trees without images. I am thinking that this will be part of the Tree page in the admin section. 
