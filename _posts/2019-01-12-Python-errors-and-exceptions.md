---
layout: post
title:  "Python errors, exceptions and handling"
categories: Python3-Tutorial
tags: Python3-tutorials
comments: true
---

Hi There, In this post we will learn about python errors, execptions and will learn how to handle these exceptions.


Three kinds of errors can occur in a program: syntax errors, runtime errors, and semantic errors. It is useful to distinguish between them in order to track them down more quickly.


1. **Syntax errors**

* **Ans:** Python can only execute a program if the syntax is correct; otherwise, the interpreter displays an error message. Syntax refers to the structure of a program and the rules about that structure

		>>> print "Hello world"
		  File "<stdin>", line 1
		    print "Hello world"
		                      ^
		SyntaxError: Missing parentheses in call to 'print'. Did you mean print("Hello world")?
		>>>

2. **Runtime errors**

* **Ans:** The second type of error is a runtime error, so called because the error does not appear until after the program has started running. These errors are also called exceptions because they usually indicate that something exceptional (and bad) has happened.

		>>> assert 2 > 7
		Traceback (most recent call last):
		  File "<stdin>", line 1, in <module>
		AssertionError
		>>>
		>>> 2 / 0
		Traceback (most recent call last):
		  File "<stdin>", line 1, in <module>
		ZeroDivisionError: division by zero
		>>>

3. **Semantic errors**

* **Ans:** The third type of error is the semantic error. If there is a semantic error in your program, it will run successfully in the sense that the computer will not generate any error messages, but it will not do the right thing. It will do something else. Specifically, it will do what you told it to do.



These errors can be handled in python using the try except block, The exceptions that are caught in 
try blocks and handled in except blocks. 

* **syntax:**

		try:
			statement 1
			
			statement n
		except <ExceptionName>:
			statement 1
			
			statement n
		else:
			statement 1
			
			statement n
		finally:
			statement 1
			
			statement n


* If an error is encountered, a try block code execution is stopped and transferred
down to the except block.

* The <span style="color:red">`except`</span> block will execute only if <span style="color:red">`try`</span> block has encountered an exception that is capturing at except block.

* The <span style="color:red">`else`</span> block will execute only if <span style="color:red">`try`</span> block executed successfully.

* The code in the <span style="color:red">`finally`</span> block will be executed regardless of whether an exception
occurs.


* **Example-1**

		>>> try:
		...     res = 2 / 0
		...     print(res)
		... except ZeroDivisionError:
		...     print("2 can't be divided by 0")
		... else:
		...     print('Im else block')
		... finally:
		...     print('Im finally block')
		...
		2 can't be divided by 0
		Im finally block
		>>>

* In the above example print statement in <span style="color:red">`try`</span> block and <span style="color:red">`else`</span> block were not executed due to ZeroDivisionError exception.
* <span style="color:red">`finally`</span> block executed regardless of block executions

* **Example-2**

		>>> try:
		...     res = 2 + 3
		...     print(res)
		... except Exception:
		...     print('Im except block')
		... else:
		...     print('Im else block')
		... finally:
		...     print('Im finally block')
		...
		5
		Im else block
		Im finally block
		>>>

* In the above example all blocks executed successfully except <span style="color:red">`except`</span> block because there is no exception in <span style="color:red">`try`</span> block execution
* **`Exception`** is the generlised excetion which can catch all python exception.
* we can also handle multiple exceptions by using defining exceptions in tuple form in except block

		except (ZeroDivisionError, AssertionError, TypeError):
			statements


