---
layout: post
title:  "Python object oriented programming (OOP)"
categories: Python3-Tutorial
tags: Python3-tutorials
comments: true
---

Hi There, In this post we will learn abot python Object oriented programming (OOP).

Object oriented programming was developed in the 1960's for a language called samula67 and later used for smalltalk language.

* OOP is a paradigm (a pattern or model) for code organization and design

+ The OOP paradigm:
	- Organizes data into objects and functionality into methods
	- Defines object specifications (data and methods) in classes
+ Promotes collaboration, code extension and maintenance
+ OOP is the primary paradigm for software design worldwide


##### Procedural Vs Object(OOP) paradgim:

+ procedural paradigm:


        def increment(arg):
            arg = arg + 1
            return arg


        this = 0
        this = increment(this)
        this = increment(this)
        print(this)

+ Object paradgim:


        class MyCustomInt(object):

            def __init__(self):
                self.arg = 0

            def increment(self):
                self.arg = self.arg + 1

            def __repr__(self):
                return str(self.arg)


        this = MyCustomInt()
        this.increment()
        this.increment()
        print(this)

##### Why we need Object oriented programming:

+ OOP organizes code so it is:
	- Easier to use
	- Easier to understand
	- Easier to mantain and extend
	- Easier to collaborate
+ Complexity must always be managed
+ OOP is a universal paradigm
+ Learning OOP is a necessary next step into larger world of software engineering

##### OOP three pillars of OOP:

* Encapsulation
* Inheritance
* Polymorphism

##### What is OOP?

Object oriented programming is a method of programming that attempts to model some process or thing in the world as **class** or **object**.

* Everything in Python is object
* Other languages employ primitives(Non-object data)

**Object**: Object is a piece of data (having one or more attributes) of a pirticular class or type with associated functionality.

**Class:** Class is a blue print for objects. classes can contain methods(functions) and attributes(similar to keys in dict).

**Instance:** Objects that are constructed from a class blue prints that contains their classes methods and properties.

**Method**: A callable attribute (function) defined inside a 


##### Defining Class and Object:

* An empity calss

        >>> class MyClass(object):
        ...     pass
        ...
        >>> this_obj = MyClass() #Instance of MyClass
        >>> that_obj = MyClass() #Another instance of MyClass
        >>>
        >>> print(this_obj)
        <__main__.MyClass object at 0x02130990>
        >>> print(that_obj)
        <__main__.MyClass object at 0x02130C70>
        >>>


* Variables defined inside the class are aviliable to the instance
* Variables defined inside the class are called class attributes

        >>> class MyClass(object):
        ...     message = "Hello World"
        ...
        >>> obj = MyClass()
        >>> obj.message
        'Hello World'
        >>>

* when we call a method on an instance the instance will get passed as the first argument 

        >>> class MyClass(object):
        ...     def say_hi(self):
        ...         print("Hi")
        ...         print(self)
        ...
        >>> obj = MyClass()
        >>> obj.say_hi()
        Hi
        <__main__.MyClass object at 0x02130CF0>
        >>> print(obj)
        <__main__.MyClass object at 0x02130CF0>
        >>>

Here in the above the **self** is an argument which takes the instance as argument, As we can see that the address of obj (instance of MyClass) and address of the self are same


##### Encapsulation:

