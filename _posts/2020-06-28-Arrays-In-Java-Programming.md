---
layout: post
title:  "Arrays in Java"
categories: Java
tags: Java-tutorials
comments: true
---

Java provides a data structure, the array, which stores a fixed-size sequential collection of elements of the same type. An array is used to store a collection of data, but it is often more useful to think of an array as a collection of variables of the same type.


**Premitive Arrays in Java:**

	public class Arrays {
		public static void main(String[] args) {
			//Array Of Type int
			int[] intValues = {2, 4, 6, 8, 10};
			System.out.println("Array one: of type int");
			System.out.println(intValues[0]);
			System.out.println(intValues[1]);
			System.out.println(intValues[2]);
			System.out.println(intValues[3]);
			System.out.println(intValues[4]);

			//Array Of Type double
			double[] floatValues = {1.2, 2.3, 3.1, 4.5};
			System.out.println("Array two: of type double");
			System.out.println(floatValues[0]);
			System.out.println(floatValues[1]);
			System.out.println(floatValues[2]);
			System.out.println(floatValues[3]);

			//Array Of Type String
			String[] stringValues = {"East",  "West", "North", "South"};
			System.out.println("Array three: of type string");
			System.out.println(stringValues[0]);
			System.out.println(stringValues[1]);
			System.out.println(stringValues[2]);
			System.out.println(stringValues[3]);

			//Array Of Type char
			char[] charValues = {'A', 'B', 'C', 'D'};
			System.out.println("Array three: of type string");
			System.out.println(charValues[0]);
			System.out.println(charValues[1]);
			System.out.println(charValues[2]);
			System.out.println(charValues[3]);

			//Array Of Type boolean
			boolean[] booleanValues = {true, false};
			System.out.println("Array three: of type string");
			System.out.println(booleanValues[0]);
			System.out.println(booleanValues[1]);

		}
	}


**Output:**

	Array one: of type int
	2
	4
	6
	8
	10
	Array two: of type double
	1.2
	2.3
	3.1
	4.5
	Array three: of type string
	East
	West
	North
	South
	Array three: of type string
	A
	B
	C
	D
	Array three: of type string
	true
	false


**List Type Array in Java:**
