---
layout: post
title:  "Python lambda and other built-in functions"
categories: Python3-Tutorial
tags: Python3-tutorials
comments: true
---

Hi There, In this post we'll learn about lambda and other built-in functions in pytrhon.

##### Lambda functions:

* A lambda function is a small anonymous function (function without a name).
* A lambda function can take any number of arguments, but can only have one expression.
* As we already know that def keyword is used to define the normal functions and the lambda keyword is used to create anonymous functions. It has the following syntax:

		lambda arguments: expression

* **Example usage:**

		>>> def add(a, b, c):
		...     return a + b + c
		...
		>>> add(1, 2, 3)
		6
		>>>


* The above example is a normal function which is having only return statement. We can implement the above add operation using labmada function.


		>>> add = lambda a, b, c: a + b + c
		>>>
		>>> add(1, 2, 3)
		6
		>>>

* In the above example a, b, c before ':' are the parameters and a + b + c is the expression.

##### Why to use lambda functions?

* The power of lambda is better shown when you use them as an anonymous function inside another function.

##### map function:

* map is a standard function that accepts at least two arguments, a function and an iterable (list, sring).
* **Syntax:**
		
		res = map(function, iterable)

* **Example usage:**

		#Printing the names in all capital letters

		>>> avengers = ['tony', 'star loard', 'thor', 'steve', 'groot']
		>>>
		>>> result = map(lambda name: name.upper(), avengers)
		>>>
		>>> result
		<map object at 0x00680CB0>
		>>>
		>>> list(result)
		['TONY', 'STAR LOARD', 'THOR', 'STEVE', 'GROOT']
		>>>


##### filter function:

* The **filter()** method filters the given sequence with the help of a function that tests each element in the sequence to be true or not.

* **Syntax:**

		filter(function, iterable)

* **function** - function that tests if elements of an iterable returns true or false If None, the function defaults to Identity function - which returns false if any elements are false
* **iterable** - iterable which is to be filtered, could be sets, lists, tuples, or containers of any iterators

* **Example usage:**

		#Printing the names that starts with letter a

		>>> a_names  = filter(lambda name: name[0] == 'a', names)
		>>>
		>>> a_names
		<filter object at 0x00680E90>
		>>>
		>>> list(a_names)
		['alex', 'akon', 'aviry']
		>>>


##### any() and all():

* **any()**

* Takes one argument and the argument should be an iterable i.e list, tuple
* Returns True if any item in the list is True
* Returns False if all items in list are False

* **Example usage:**

		>>> any([True, False, True])
		True
		>>>
		>>> any((False, False, False))
		False
		>>>


* **all()**

* Takes one argument and the argument should be an iterable i.e list, tuple
* Returns True if all item in the list is True
* Returns False if any items in list are False

* **Example usage:**

		>>> all([True, False, True])
		False
		>>> all((True, True, True))
		True
		>>>


##### sorted():

* The sorted() method sorts the elements of a given iterable in a specific order - Ascending or Descending.

* **syntax:**

		sorted(iterable[, key][, reverse])

+ **sorted()** takes two three parameters and returns a sorted list from the given iterable:
- **iterable** - sequence (string, tuple, list) or collection (set, dictionary, frozen set) or any iterator 
- **reverse** (Optional) - If true, the sorted list is reversed (or sorted in Descending order)
- **key** (Optional) - function that serves as a key for the sort comparison


* **Example usage-1:**

		>>> a = [1, 3, 4, 6, 7]
		>>>
		>>> sorted(a)
		[1, 3, 4, 6, 7]
		>>> sorted(a, reverse=True)
		[7, 6, 4, 3, 1]

* **Example usage-1:**


		#Sorting by key name in list of dict
		>>> names = [{'name': 'rock'}, {'name': 'aviry'}, {'name': 'ellen'}]
		>>>
		>>> sorted(names, key=lambda name: name['name'])
		[{'name': 'aviry'}, {'name': 'ellen'}, {'name': 'rock'}]
		>>>

