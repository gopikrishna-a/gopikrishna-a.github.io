---
layout: post
title:  "Python 'is' versus 'equal'(==)"
categories: Python3-Tutorial
tags: Python3-tutorials
comments: true
---

Hi There, In this post we'll see some of the differances between is and equal (==) in python

##### Is Vs equal (==)


* **Example one:**
			
		>>> a = 1
		>>> a == 1
		True
		>>> a is 1
		True
		>>>


* **Example two:**

		>>> a = [1, 2, 3]
		>>> b = [1, 2, 3]
		>>>
		>>> a == b
		True
		>>> a is b
		False
		>>>

* <span style="color:red">`==`</span> : The equal (==) operator compars the values of a and b
* <span style="color:red">`is`</span> : The is keyword Compars the stored memory addresses