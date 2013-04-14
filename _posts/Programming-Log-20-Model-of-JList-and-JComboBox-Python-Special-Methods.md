---
title: Programming Log 20: Model of JList and JComboBox, Python Special Methods
date: '2013-3-4'
categories: Learning
tags: [Learning, Java, python]
---

Today morning I took a quick view of the *JList* and *JComboBox*. It's seems similar to JSpinner I have learned yesterday, so I decide to learn its detail when I use it.

I dived into python this afternoon, I think the special method of class is similar to the concept of operator overloading. Some questions:

+ The differences between "*is*" and "*==*" ("*is not*" and  "*!=*")
+ p55, the section about function override, confused me
+ What should I do when I need *overloading*?
+ Why this happened?

	>>> d=UserDict(a)
	>>> d
	{1: 1, 2: 2}
	>>> d.__class__
	<class UserDict.UserDict at 0x7f8a96db63f8>	# ?
	>>> dd=d.copy()
	>>> ddd=d.data.copy()
	>>> dd.__class__
	<class UserDict.UserDict at 0x7f8a96db63f8>	# ?
	>>> dd[1]=3
	>>> dd
	{1: 3, 2: 2}
	>>> d
	{1: 1, 2: 2}
	>>> dd.__class__
	<class UserDict.UserDict at 0x7f8a96db63f8>	# ?
	>>> d.__class__
	<class UserDict.UserDict at 0x7f8a96db63f8>	# ?
	>>> ddd.__class__
	<type 'dict'>


The answer of the first: "*is*" judges if the reference is equal, and not recommand to compare number, there is a example code:

	 a=0
	 b=0
	 while a is b:
	 	a+=1
	 	b+=1

	 print id(a),a
	 print id(b),b

print out

	14642224 257
	14642296 257

because "this is really hardcoded limit in the current CPython implementation. The interpreter preallocates numbers from 0 to 256."

in the *intobject.c*:

	#ifndef NSMALLPOSINTS
	#define NSMALLPOSINTS		257
	#endif
	#ifndef NSMALLNEGINTS
	#define NSMALLNEGINTS		5
	#endif
	#if NSMALLNEGINTS + NSMALLPOSINTS > 0
	/* References to small integers are saved in this array so that they
	   can be shared.
	   The integers that are saved are those in the range
	   -NSMALLNEGINTS (inclusive) to NSMALLPOSINTS (not inclusive).
	*/
	static PyIntObject *small_ints[NSMALLNEGINTS + NSMALLPOSINTS];
	#endif
	#ifdef COUNT_ALLOCS
	int quick_int_allocs, quick_neg_int_allocs;
	#endif


To sum up, I spent **3 hours** on programming today, and totally **78 hours**.