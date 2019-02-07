---
layout: post
title:  "Python object oriented programming (OOP)"
categories: Python3-Tutorial
tags: Python3-tutorials
comments: true
---

Hi There, In this post we will learn about python Object oriented programming (OOP).

Object oriented programming was developed in the 1960's for a language called samula67 and later used for smalltalk language.

* OOP is a paradigm (a pattern or model) for code organization and design

+ The OOP paradigm:
	- Organizes data into objects and functionality into methods
	- Defines object specifications (data and methods) in classes
+ Promotes collaboration, code extension and maintenance
+ OOP is the primary paradigm for software design worldwide


##### Procedural Vs Object(OOP) paradgim:

+ Procedural paradigm:


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

##### Three pillars of OOP:

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

**Encapsulation:** Encapsulation is grouping of public and private attributes and methods into a class, making abstraction possible.

**Abstraction:** Exposing only relevant data in a class interface, hiding private attributes and methods from user

* In object oriented programming, you can restrict access to methods and variables. This can prevent the data from being modified by accident and is known as encapsulation.

* Python does not have the private keyword, unlike some other object oriented languages, but encapsulation can be done.

**Encapsulation implimentation example:**

Imagine we have created a banking program for a an ATM which has the attribute 'current_balance'

we don't want the user of the ATM to be able to access this variable directly because they might be able to overwrite it with a huge amount of money.

* In order to make it in-acceable to the user direcly we need to make 'current_balance' attribute as private


        class BankAccount(object):

            def __init__(self, account_name='Current Account', balance=300):
                self.account_name = account_name
                self.balance = balance
                
        account = BankAccount()
        print(account.account_name)
        print(account.balance)
        account.balance = 2000000
        print(account.balance)

        #Program output
        $ python encapsulation.py
        Current Account
        300
        2000000

* As you can see in the above program output the user was able to access and rewrite account.balance attribute.

* To make balance as private we need to add double underscore to that variable as follows


        class BankAccount(object):

            def __init__(self, account_name='Current Account', balance=300):
                self.__account_name = account_name
                self.__balance = balance
                
        account = BankAccount()
        print(account.__account_name)
        print(account.__balance)
        account.__balance = 2000000
        print(account.__balance)

        #Program output
        $ python encapsulation.py
        Traceback (most recent call last):
          File ".\encapsulation.py", line 12, in <module>
            print(account.__account_name)
        AttributeError: 'BankAccount' object has no attribute '__account_name'

* By adding __ to the balance and account_name varibale we are making these variables as private. with this the user won't be able to access these attributes.

* But when user withdraw some money from balace we need to reduce/change the balance value. this can be achived by using setter method inside the class because methods inside the class can access the private attributes.

        class BankAccount(object):

            def __init__(self, account_name='Current Account', balance=300):
                self.__account_name = account_name
                self.__balance = balance

            def balance_getter(self):
                print(f'Your current balance is: {self.__balance}')

            def balance_setter_withdraw(self, value):
                if value <= self.__balance:
                    self.__balance = self.__balance - value
                    print(f'New balance is {self.__balance}')
                else:
                    print('You don\'t have enough funds')

        account = BankAccount()

        while True:
            print('====Select your optiion====')
            print('1. Check account balance')
            print('2. Withdraw funds')
            option = int(input(''))
            if option == 1:
                account.balance_getter()
            elif option == 2:
                value = int(input('Enter withdraw amount: '))
                account.balance_setter_withdraw(value)
            else:
                print('plz choose valid choice')

        #Sample execution output for above program
        ====Select your optiion====
        1. Check account balance
        2. Withdraw funds
        1
        Your current balance is: 300
        ====Select your optiion====
        1. Check account balance
        2. Withdraw funds
        2
        Enter withdraw amount: 50
        New balance is 250
        ====Select your optiion====
        1. Check account balance
        2. Withdraw funds
        2
        Enter withdraw amount: 300
        You don't have enough funds
        ====Select your optiion====
        1. Check account balance
        2. Withdraw funds