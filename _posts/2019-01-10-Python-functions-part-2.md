---
layout: post
title:  "Python functions and usage Part-2"
categories: Python3-Tutorial
tags: Python3-tutorials
comments: true
---

Hi There, In this post we'll learn more about python functions.

##### Passing flexible number of arguments to a function

* In Python We can also pass N no. of arguments to a function as per our requirement. For this we have to use <span style="color:red">`*args`</span> as parameter to that function.

**Example:**

		>>> def sum_all_nums(*args):
		...     total = 0
		...     for num in args:
		...         total += num
		...     return total
		...
		>>> sum_all_nums(1, 2, 3, 4, 5)
		15
		>>> sum_all_nums(1, 2)
		3
		>>> sum_all_nums(2, 4, 5, 6, 7, 2, 3, 4, 5 , 5, 7)
		50
		>>>

* In the above example we can observe that we called <span style="color:red">`sum_all_nums`</span> function three time with different number of arguments this is because we have used <span style="color:red">`*args`</span> as a parameter.
* Here the word **args** can be of any name Ex: `*nums`, `*words`.


##### `**kwargs` in Python 

* The double asterisk form of <span style="color:red">`**kwargs`</span> is used to pass a keyworded, variable-length argument dictionary to a function. You should use <span style="color:red">`**kwargs`</span> if you want to handle named arguments in a function.

* Like <span style="color:red">`*args`</span>, <span style="color:red">`**kwargs`</span> can take however many arguments you would like to supply to it. However, <span style="color:red">`**kwargs`</span> differs from <span style="color:red">`*args`</span> in that you will need to assign keywords.

* <span style="color:red">`*args`</span> and <span style="color:red">`**kwargs`</span> make the function flexible.

* **Usage of `**kwargs`:**

		>>> def print_kwargs(**kwargs):
		...     return kwargs
		...
		>>> print_kwargs(name="Shark", age=24, weight=58)
		{'age': 24, 'name': 'Shark', 'weight': 58}
		>>>


##### Parameters ordering


* While passing the parameters to a function they should follow the below order if the function has below all arguments.

1. parameters
2. `*args`
3. default parameters
4. `**kwargs`


##### Tuple Unpacking

* **Using `*` as an argument**

		>>> def unpack(*args):
		...     return args
		...
		>>> nums = [1, 2, 3, 4, 5]
		>>>
		>>> unpack(nums)
		([1, 2, 3, 4, 5],)
		>>>
		>>>
		>>> unpack(*nums) #Tuple unpacking using *nums
		(1, 2, 3, 4, 5)
		>>>

* To unpack the values from a sequnce we need to pass <span style="color:red">`*`</span> infornt of the sequence variable.


##### Dictonary Unpacking

* **Using `**` as an argument**


		>>> def display_names(a, b, c):
		...     return a + b + c
		...
		>>> nums = {'a': 1, 'b': 2, 'c': 3}
		>>>
		>>> display_names(**nums)
		6


* To unpack the values from a dictonary we need to pass <span style="color:red">`**`</span> infornt of the dictonary variable.
