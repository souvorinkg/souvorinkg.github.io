---
layout: post
title: Planting the First Seeds
date: 2024-9-4 10:18:00
categories: [.NET, Community]
---

This week, I opened up an old project, Hendrix Arboretum. I was horrified to realize that it used .NET 5, which hadn’t been supported in years! I found an old version to download, but after running into issues, I realized that .NET 5 was so out of date that it wasn’t compatible with the M1 chip in my Mac. First, we switched to a local DB over a server for our tree images, Our team began a race to update from 5 to 6, 6 to 7, and 7 to 8. It was impossible to have multiple versions on our system at a time, so we were constantly juggling distributions. Additionally, each version had different requiremnts for tasks.json and launch.json files. 

By the end of our meeting we were successful, the Hendrix Arboretum was loading on all of our computers using the .NET 8 SDKs!