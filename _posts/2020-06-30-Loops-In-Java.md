---
layout: post
title:  "Loops in Java"
categories: Java
tags: Java-tutorials
comments: true
---

**While Loop in Java:**

	public class WhileLoop {
		public static void main(String[] args) {
			int count = 0;

			// while loop
			while (count <= 10) {
				System.out.println(count);
				count++; //count = count + 1;
			}
		}
	}

**Output:**

	0
	1
	2
	3
	4
	5
	6
	7
	8
	9
	10



**Find even number using wile loop and if statement:**

	public class WhileLoop {
		public static void main(String[] args) {
			int count = 1;
			while (count <= 10) {
				if ((count % 2) == 0) {
					System.out.println("Number: " + count +  " is even number");
				}
				count++; //count = count + 1;
			}
		}
	}

**Output:**

	Number: 2 is even number
	Number: 4 is even number
	Number: 6 is even number
	Number: 8 is even number
	Number: 10 is even number



**For Loop in Java:**

	public class ForLoop {
		public static void main(String[] args) {
			int count;
			for (count = 1; count <= 10; count++)  {
				System.out.println(count);
			}
		}
	}

**Output:**

	0
	1
	2
	3
	4
	5
	6
	7
	8
	9
	10



**Find even number using for loop and if statement:**

	public class ForLoop {
		public static void main(String[] args) {
			int count;
			for (count = 1; count <= 10; count++)  {
				if ((count % 2) == 0) {
					System.out.println("Number " + count + " is even");
				}
			}
		}
	}

**Output:**

	Number 2 is even
	Number 4 is even
	Number 6 is even
	Number 8 is even
	Number 10 is even


**For loop using arrays:**

	public class ForLoopArray {
		public static void main(String[] args) {
			String[] colourNames = {"Red", "Green", "Yellow", "Blue"};
			for (String colour : colourNames) {
				System.out.println(colour);
			}
		}
	}

**Output:**

	Red
	Green
	Yellow
	Blue


**For loop using ListArray:**

	import java.util.ArrayList;
	import java.util.List;

	public class ForLoopArray {
		public static void main(String[] args) {

			List<String> colourNames = new ArrayList<String>();
			colourNames.add("Red");
			colourNames.add("Yellow");
			colourNames.add("Green");
			colourNames.add("Blue");

			for (String colour : colourNames) {
				
				System.out.println(colour);

			}

		}
	}

**Output:**

	Red
	Yellow
	Green
	Blue





