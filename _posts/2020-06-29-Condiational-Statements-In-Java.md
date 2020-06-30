---
layout: post
title:  "Condiational statements in Java"
categories: Java
tags: Java-tutorials
comments: true
---

**If statement in Java:**

	public class IfStatement {
		public static void main(String[] args) {
			int a = 20, b = 10;
			if (a > b) {
				System.out.println("a is bigger than b");
			}
		}
	}


**Output:**

	a is bigger than b

**If else statement in Java:**

	public class IfElseStatement {
		public static void main(String[] args) {
			int a = 100, b = 200;
			if (a > b) {
				System.out.println("a is bigger than b");
			}
			else {
				System.out.println("b is bigger than a");
			}
		}
	}


**Output:**

	b is bigger than a

**If else if statement in Java:**

	public class IfElseStatement {
		public static void main(String[] args) {
			int a = 200, b = 200;
			if (a > b) {
				System.out.println("a is bigger than b");
			} 
			else if (a < b) {
				System.out.println("b is bigger than a");
			}
			else {
				System.out.println("a and b are eual");
			}
		}
	}


**Output:**

	a and b are eual
