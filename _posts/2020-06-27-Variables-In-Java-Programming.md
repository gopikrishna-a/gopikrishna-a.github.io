---
layout: post
title:  "Variables in Java"
categories: Java
tags: Java-tutorials
comments: true
---

A variable provides us with named storage that our programs can manipulate. Each variable in Java has a specific type, which determines the size and layout of the variable's memory.


**Variables in Java:**

	public class Variables {

		public static void main(String[] args) {

			String name = "Gopirishna"; //Initialization of string variable value should be in double quotes
			int age = 26; //Initialization of int variable.
			double height = 5.3; //Initialization of floating point variable.a char variable should be in single quotes.
			char firstName = 'A'; //Initialization of char (single char) variable value should be in single quotes.
			boolean isMarried = false; //Initialization of boolean variable value
			
			//Printing the initialized variables values into console
			System.out.println("My name is " + name);
			System.out.println("My age is " + age);
			System.out.println("My height is " + height);
			System.out.println("My first name is " + firstName);
			System.out.println("Am I married: " + isMarried);

	}
	}


**Output:**

	My name is Gopirishna
	My age is 26
	My height is 5.3
	My first name is A
	Am I married: false