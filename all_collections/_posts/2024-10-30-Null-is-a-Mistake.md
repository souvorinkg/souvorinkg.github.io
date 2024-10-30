---
layout: post
title: "Null or Not"
date: 2024-10-30    
categories: [Hendrix Arboretum]
---

Tony Hoare, null's creator, regretted his decision. "I call it my billion-dollar mistake." "I couldn't resist the temptation to put in a null reference [to AGOL W], simply because it was so easy to implement." ISeeGreen was reeling from nullability in our database. At creation, the developers were not sure which values had been populated in the DB yet. Every database operation and it's dependencies couldn't be garunteed to even work. It would've been infeasible to wrap every function in a null check, and the constant warnings were causing our team to ignore genuine faults in the project. 

To solve this issue, I changed all of the variables in the model to required if I saw that every member of the database was populated for that column. Many of our model variables were calculated from other tables, if it depended entirely on other required columns, I switched the variable to required as well. For variables that sometimes had values, I set up null coalescing checks when loading them from the database, where I would set the variable with either the database value or a default value, such as "unknown," "0." Finally, many of the unknown variables in the model did not end up used in the final version of the model, so I deleted them to remove the final null dependencies. 



![Tony Hoare in 2009](https://www.infoq.com/presentations/Null-References-The-Billion-Dollar-Mistake-Tony-Hoare/)