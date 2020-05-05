---
layout: post
title: "Review of JVM Memory Management and Garbage Collection"
date: 2020-04-22 12:00:00 -0500
---

The Java Virtual Machine divides memory into several different administrative areas. Each of these areas has its own purpose, taking on different tasks and using different algorithms for garbage collection, depending on its characteristics. The whole is divided into the following parts: Program Counter Register, JVM Stacks, Native Method Stacks, Heap, Method Area.

1. Program Counter Register: This is a small piece of memory, not on the Ram, but direct division on the CPU, the programmer can't operate it directly. Its role is: when the JVM is explaining the bytecode file, it will store the number of rows in the bytecode to perform for the current thread. In a different way, adopted by the various JVM bytecode interpreter work, it works by changing the value of the program counter to select the next instructions to be executed, the basic function such as branches, loops, jumps, are dependent on the technology area.
2. JVM Stacks: The JVM stack of a thread is used by the thread to store local variables, partial results, and data for method invocations and returns. There are two possible Java exceptions in this memory area: StackOverFlowError and OutOfMemoryError.
3. Native Method Stacks: From the name, it can be seen that the local method stack is used to handle the local methods in Java.
4. Heap: The run time data area from which the memory for all java class instances and arrays is allocated. The heap is created when the JVM starts up and may increase or decrease in size while the application runs.
5. Method Area: An area of memory shared by all threads to store class information, constants, static variables, and so on that have been loaded by the JVM.

As Java programmers, it is difficult to control the memory recovery of the JVM, so we can only adapt to its principles and maximize the performance of the program. The reason that garbage collection exists is that as the program runs, the instance objects, variables, and other information in memory occupy more and more memory. If garbage collection is not carried out in time, the performance of the program will inevitably be reduced, and some unnecessary system exceptions will be caused because of insufficient available memory. Of the five areas we described above, three do not require garbage collection: the program counter, the JVM stack, and the local method stack. Because their life cycles are synchronized with the thread, the memory they occupy is automatically freed as the thread is destroyed, so only method areas and heaps require garbage collection. If an object no longer has any references, it can be recycled. The popular explanation is that if an object is no longer useful, it can be recycled as waste.
