---
layout: post
title:  "Hello World in Java"
categories: Java
tags: Java-tutorials
comments: true
---

Java is a high-level programming language originally developed by Sun Microsystems and released in 1995. Java runs on a variety of platforms, such as Windows, Mac OS, and the various versions of UNIX.

**NOTE:** The class and and file name should be same while writing JAVA program. please make a note that in case you do not have a public class present in the file then file name can be different than class name. It is also not mandatory to have a public class in the file.

**My First Program in Java:**


	public class HelloWorld {
	    public static void main(String[] args) {
	        System.out.println("Hello World!!!!!");
	    }

	}

**Output:**

	Hello World!!!!!

**Explanation:**

1. ```public class HelloWorld```
	+ Class definition:This line uses the keyword class to declare that a new class is being defined.
2. ```public static void main(String[] args)```
	+ main method: In Java programming language, every application must contain a ```main``` method.
	+ public: So that JVM can execute the method from anywhere.
	+ static: Main method is to be called without object. The modifiers public and static can be written in either order.
	+ void: The main method doesn't return anything.
	+ main(): Name configured in the JVM.
	+ String[]: The main method accepts a single argument an array of elements of type String.
3. ```System.out.println("Hello World!!!!!");```
	+ This line outputs the string "Hello World!!!!!" followed by a new line on the screen. Output is actually accomplished by the built-in println() method. System is a predefined class that provides access to the system, and out is the variable of type output stream that is connected to the console.
