---
title: Programming Log 7: Breakthrough with Tutorial, Disturbing I/O problem of Python
date: '2013-2-18'
categories: Learning
tags: [Learning, Java, Swing, python, i/O]
---

First I searched the API doc of Java but I could't find appropriate listener, but I have noticed a new component called *JTextPane*. I turned to *Java Tutorial* to get some informations of it. I gladly find some descriptions about *JTextPane* and in the sample code below, I find *DocumentListener* is what I want. It's cool learning by API doc and tutorial.


But there are still some questions remained:

+ How to judge the source of *DocumentEvent*?
+ Again, am I use a screwdriver as a hammer(by asking the first question)?
+ Why I add *invokeLater()*, the program become worse?
+ Now the GUI is lazy to refresh itself. (Try to put GUI in a new thread.)


Something is so disturbing about python I/O. When I write a "*\n*" to a file and use *readline()*, a redundant breakline will be read in. And when I try to use another *read(1)* to compensate it, it will lost one character.

+ How to print "%"?
+ How to get float result of division?
+ How to get int when input?


Python is not so highlevel and no need to process with details as I though. Also, my skill is poor:(


My answer after dinner(*rest&eat* will help):

+ "%%"
+ print "%.2lf" %float(100)
+ To the I/O question: yes, I use a screwdriver as a hammer again. When you try to make a log file, why don't use *Pickle*? For example:

	import cPickle as p

	class Log:
		time=6
		path="\nabc"

	log=Log()

	f=file("logfile",'w')
	p.dump(log,f)
	f.close

	f=file("logfile")
	newlog=p.load(f)

	print newlog.time,newlog.path


To sum up, I spent **7 hours** on programming today, and totally **29 hours**.