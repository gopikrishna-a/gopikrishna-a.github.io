---
layout: post
title:  "Python functions and usage part-1"
categories: Python3-Tutorial
tags: Python3-tutorials
comments: true
---

Hi There, In this post we'll learn about python functions.

##### Functions

 * Function is a named sequence of statements that performs a computation. When you define a function, you specify the name and the sequence of statements. Later, you can “call” the function by name.

##### Type conversion functions

* Python provides built-in functions that convert values from one type to another.

###### int()

* The **int()** function takes any value and converts it to an integer, if it can, or complains otherwise

		>>> int('32')
		32
		>>> int('hello')
		Traceback (most recent call last):
		  File "<stdin>", line 1, in <module>
		ValueError: invalid literal for int() with base 10: 'hello'
		>>>

* **int()** can convert floating-point values to integers, but it doesn’t round off; it chops off the
fraction part

		>>> int(13.999)
		13
		>>>

###### float()

* The **float()** function takes any value and converts it to an integer

		>>> float(32)
		32.0
		>>>
		>>> float("22")
		22.0
		>>>
		>>> float("hii")
		Traceback (most recent call last):
		  File "<stdin>", line 1, in <module>
		ValueError: could not convert string to float: 'hii'
		>>>

###### str()

* The **str()** function converts its argument to a string


		>>> str(123)
		'123'
		>>>


##### Adding new functions

* So far, we have only been using the functions that come with Python, but it is also possible to add new functions. A function definition specifies the name of a new function and the sequence of statements that execute when the function is called.

* **Example function:**

		>>> def print_hi():
		...     print("Hi")
		...
		>>> print_hi()
		Hi
		>>>

* **def** is a keyword that indicates that this is a function definition.
* The name of the function is **print_hi**.
* The rules for function names are the same as for variable names
* The empty parentheses after the name indicate that this function doesn’t take any arguments.
* The first line of the function definition is called the header, the rest is called the body.
* The header has to end with a colon and the body has to be indented (four spaces).
* The body can contain any number of statements.


##### The **return** key word

* The **return** statement causes your function to exit and hand back a value to its caller. The point of functions in general is to take in inputs and return something. The **return** statement is used when a function is ready to **return** a value to its caller.

* **Usage:**

		>>> def print_square_of_7():
		...     print(7**2)
		...
		>>> print_square_of_7()
		49
		>>>


		>>> def print_square_of_7():
		...     7**2
		...
		>>> res = print_square_of_7()
		>>> print(res)
		None
		>>>

		#Using return keyword
		>>> def print_square_of_7():
		...  return 7**2
		...
		>>> res = print_square_of_7()
		>>> print(res)
		49
		>>>


* Exits the function
* Outputs what ever value is placed after the return keyword 
* pops the function off the [call stack](https://cs.ucsb.edu/~pconrad/cs8/topics.beta/theStack/02/)

##### Parameters and arguments

* Some of the built-in functions we have seen require arguments. For example, list.append(item)
here item is an argument.
* Some functions take more than one arguments example list.insert(index, item)
* Inside the function, the arguments are assigned to variables called parameters

###### Here is an example of a user-defined function that takes an argument:
* **Example:**

		 >>> def add(num1, num2):
		...     return num1 + num2 #returningsum of num1 and num2
		...
		>>> add(2, 3) #num1 and num2 are parameters for add() function
		5
		>>>


###### **Parameter**: 
* A variable in method defination.
* A variable in the decleration of function

**Ex:**
* In the above add() function num1 and num2 in function defination are parameters

###### **Argument**: 
* When a method is called, the aurguments are the data you pass into the method's parameters
* Argument is the avtual value of the variable that gets passed to function.

**Ex:**
* When we call the add(2, 3) function in the above example 2, 3 are arguments.


##### Default Parameters

* **Usage:**

		>>> def exponent(num, power=2):
		...     return num ** power
		...
		>>> exponent(3, 3)
		27
		>>> exponent(5)
		25


+ In the above example function defination we have two parameters
  - **num** : parameter without default value
  - **powrer** : parameter with default value


##### Why to have default parameters

+ Allows you to be more defencive
+ Avoids errors with incorrect parameters
+ Makes the function more reliable


##### What can be default parameters

+ Default parameters can be of any datatype i.e lists, dictonaries, string, bool, int, float
+ Default parameters can also be a function

* **Example:**

		>>>
		>>> def add(a, b):
		...     return a + b
		...
		>>> def subtract(a, b):
		...     return a - b
		...
		>>> def math(a, b, fn=add): #making add() function as a default parameter
		...     return fn(a, b)
		...
		>>> math(2, 3) 
		5
		>>> math(2, 2, subtract) #passing function as a argument
		0
		>>>

##### Keyword arguments

* We can change the order of the arguments while calling a function with the help of keyword arguments

		>>> def full_name(first="Gopikrishna", last="A"):
		...     return f"{first} {last}"
		...
		>>> full_name(first="Tony", last="Stark")
		'Tony Stark'
		>>> full_name(last="Stark", first="Tony")
		'Tony Stark'
		>>>

* In the above example we can observe that even we change the order of the arguments the result will be same this is because of **Keyword** arguments


##### Variable scope


* Variables created in the function are scoped in that function

* **Example:**

		>>> def say_hello():
		...     name = "Tony Stark"
		...     return f"Hello {name}"
		...
		>>> say_hello()
		'Hello Tony Stark'
		>>>
		>>> print(name)
		Traceback (most recent call last):
		  File "<stdin>", line 1, in <module>
		NameError: name 'name' is not defined
		>>>

* In the above example we got **NameError** when we tried to print name variable which is defined inside the **say_hello()** function this is because varables defined inside a function are only aviliable inside the function.

* This can be handled by making the name variable as a global variable as follows

		>>> def say_hello():
		...     global name
		...     name = "Stark"
		...     return f"Hello {name}"
		...
		>>> say_hello()
		'Hello Stark'
		>>> name
		'Stark'
		>>>


