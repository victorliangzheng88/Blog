---
layout: post
title: "Review on Exception"
date: 2020-04-30 12:00:00 -0500
---

An exception is something that we always encounter when we are writing our codes. Although we don’t want to see it, from a different perspective, the existence of exception indicates that there is something wrong with the program, which can help up to correct it. There are many errors that a program can have, such as illegal input or types, null pointer, and even out of memory. We only know that it has an error, but we do not know where the error locates. So many things can go wrong on a program, grammatical problems are easier to solve but for logical error, we have to check the whole program to locate the error and that takes lots of effort to do so. The existence of exception can help us to locate the error by adding an exception block to handle the exception and that can help us to reduce errors. It is significant to add exception block as you never know what kinds of problems your program can have. Java provides us with a very perfect exception handling mechanism so that we can pay more attention to write programs, sometimes when we need to add an exception handling block, IDE program such as eclipse will automatically prompt you, which is very nice.

There are two major categories starting at the root: Error and Exception. An Error is an Error that a program cannot handle, such as OutOfMemoryError, ThreadDeath, etc. When these exceptions occur, the Java virtual machine (JVM) typically selects thread termination. Exceptions are exceptions that the program itself can handle. There are two main types of exceptions: non-runtime exceptions (called check exceptions when they occur at compile time) and run-time exceptions (called unchecked exceptions when they occur while the program is running).

Checked exceptions are generally code that does not conform to the Java language specification, they are easy to see, and are easy to resolve.

Unchecked exceptions are those exceptions generated in the process of program operation, such as the null pointer exception, etc.. There are many reasons for the null pointer, so the unchecked exception has uncertainty and it is often difficult to troubleshoot. There are also logic errors in the program, which can't be seen from one piece of code, you need to check the whole program to find the error.

This requires us to pay more attention while writing the program and take every step as possible to handle the exception when the exception occurs and hope that the program can run towards the ideal aspect.

One method to eliminate exceptions in the program is to add exception handling blocks to the program. Such as using a try/catch/finally statement block. Each try block contains statements that can cause exceptions and every catch block contains a program that handles exceptions.

Common exceptions:

ArithmeticException - It is thrown when an exceptional condition has occurred in an arithmetic operation.
ArrayIndexOutOfBoundsException - It is thrown to indicate that an array has been accessed with an illegal index. The index is either negative or greater than or equal to the size of the array.
ClassNotFoundException - This Exception is raised when we try to access a class whose definition is not found
FileNotFoundException - This Exception is raised when a file is not accessible or does not open.
IOException - It is thrown when an input-output operation failed or interrupted
NoSuchFieldException - It is thrown when a class does not contain the field (or variable) specified
NullPointerException - This exception is raised when referring to the members of a null object.
NumberFormatException - This exception is raised when a method could not convert a string into a numeric format.

