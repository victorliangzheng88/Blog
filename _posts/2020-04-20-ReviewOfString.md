---
layout: post
title: "Review of String"
date: 2020-04-20 12:00:00 -0500
---

Generally, variables declared by strings are immutable in length, which is one of the most intuitive differences between StringBuffer and StringBuilder. General initialization method: String s = "hello world"; With this statement, an s variable is generated in the JVM's stack memory and a hello world string object is generated in the heap memory. S points to the address of the hello world. The strings produced in this way are direct string objects, which the JVM caches when it processes them, pools them when they are generated, and when the program needs to use them again, instead of recreating a new string, it points directly to an existing string. When you set equals “==” to the two variables of strings, they point to the same address. Now I'm going to list the methods in the string that I’ve used a lot.

public int length() - This method is used to get the length of the string

public boolean equals(Object anObject) - a method compares the two given strings based on the data/content of the string. If all the contents of both the strings are the same then it returns true. If all characters are not matched then it returns false.

These are the considerations for overriding equals() :
1. Use the == operator to check whether an argument is a reference to an object.
2. Use the instanceof operator to check whether the arguments are of the correct type.
3. Convert arguments to the correct type.
4. Check whether the field in the argument matches the corresponding field value in the current object.

public int compareTo(String anotherString) - a method used for comparing two strings lexicographically.

public char charAt(int index) - a method that returns a char value at the given index number. 

public String substring(int beginIndex) - a method that returns a new string that is a substring of this string.

One new concept that I’ve learned while reviewing String is the existence of the constant pool. The Java string constant pool is an area in heap memory where Java stores literal string values. The heap is an area of memory used for run-time operations. When a new variable is created and given a value, Java checks to see if that exact value exists in the pool. The constant pool is generally referred to a String constant pool, it is used as a mechanism of String buffer, when we wrote in the application form, such as String s = "ABC" after such a statement, the JVM will allocate space for us, on the stack to store variable and object "ABC", when we need to ABC object again, if we write down: String s1 = "ABC" statement, the JVM will be to find in the constant pool, if not, create a new object. If so, point s1 directly to the previous object "ABC". At this point, if we use == to judge, it will return true. The benefit of this is that memory is saved and the system responds faster (because it saves object creation time), which is why the caching system exists. Constant pools are for constants that are determined at compile-time, as described above for objects in the String class.
