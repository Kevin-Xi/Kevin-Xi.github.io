---
title: Programming Log 12: Restructuring
date: '2013-2-23'
categories: Learning
tags: [Learning, Java]
---

My program has some strange problem, and because I write it so "unrestrained", the code is dirty. So I decide to restruct my program. Actually, I don't know the exact meaning of "*restruct". I drain the anonymous class out as inner class, and some duplicate code as new methods. I have almost done. During this, I find the problem is not in the code, but in the chaos of the code(I run this web program in one computer, so the second client can't get a port which have been taken by the first one), which also, bring chaos to my brain. I now have more insight of my code, and bring out new questions that I have never considered about. It's a valuable experience.

+ When a component should be a member of a class? When the member should *new()*?
+ How to test web program in one computer?

And this is the minimap of Sublime Text before and after restructing:

![before][1]                             	![after][2]


To sum up, I spent **5 hours** on programming today, and totally **51 hours**.


[1]: {{urls.media}}/beforerestructuring.png
[2]: {{urls.media}}/afterrestructuring.png