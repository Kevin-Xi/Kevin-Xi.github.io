---
title: Programming Log 52: Division in Relational Algebra, String Formatting in Python
date: '2013-4-10'
categories: Learning
tags: [Learning, database, python]
---

Division in relational algebra is a great magic. I believe the teacher's answer is wrong(In ppt "Relational Algebra Ref Answer"), question 4, it should be *pid* but not *aid*.

In breif, R(x,y)/S(x) is all that kind of y in R which match all x in S.

For python, I can answer question #2 yesterday, it's a stuff called "dictionary-based string formatting". But new problem occured: 

+ Why

	strattrs = *"".join*([' %s="%s"' % (key, value) for key, value in attrs])

in *unknown_starttag*.

I think the answer is turn a list to string for string formatting var *locals()*. So is there any way to format string directly with a list?

To sum up, I spent **1 hours** on programming today, and totally **158 hours**.