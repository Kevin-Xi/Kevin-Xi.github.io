---
title: Programming Log 54: Iteration 0 on Our Project, Finished Learning HTML Processing with Python
date: '2013-4-12'
categories: Learning
tags: [Learning, project, HTML, python]
---

Today morning we had a 15-min meeting to ensure everyone's mission till next iteration.

And once again, I try to establish my github page using *Jekyll*. I really like ruhoh, but it stop working for a long time.

I try to our team to use git+github, and now I'm reviewing and learning about it.

*Dive into Python* is indeed a considerate book. It show me *SGMLParser* when I wonder how it works. And my guess is confirmed, *getattr* play the role.

And since I know the principle, I fixed my spider days ago and make my *BaseHTMLProcessor.py* ran. There are still some questions:

+ What *verbatim* for? Is *is_TD* necessary? Why

	if self.verbatim<=1:

function in the same way as 

	if self.is_TD>=1:

?

+ Why in my *dialect.py* it should be 

	if self.is_TD>=1:

to make it run?

The *globals()[parserName]* is really an intriguting usage of *global*.

With *dynamic importing*, it's easy to make plug-ins for python code.

Finally I finished chapter 8.

To sum up, I spent **3 hours** on programming today, and totally **164 hours**.