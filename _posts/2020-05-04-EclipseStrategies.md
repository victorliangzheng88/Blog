---
layout: post
title: "Strategies On Using Eclipse"
date: 2020-05-04 12:00:00 -0500
---

Eclipse is an artifact of the Java development community, occupying most of the Java development market, and its official support for other languages, such as C++, Ruby, JavaScript, and so on. Some of the benefits of Eclipse are that the development interface is simple with rich plug-in support and is customized for Java with its humanized design. Eclipse is a widely recognized tool in the industry, so for such a software, we must learn to use it. Eclipse offers a wealth resource of shortcuts, many by default, and you can set them manually. Some of the skills at using Eclipse that I would introduce are: 

1. Viewing Source Code: When we are on the way to a press F3 or press CTRL + left mouse button, we will follow the codes. When we are in a class for the operation, we can trace to the source of this class, but sometimes, the source class may not cited in, and that in most of the time we need to manually introduce it. For example, when we want to look at the source of the String class, we press F3 on the String. If it have introduced the source code, it will jump straight to the source code, but without introduction, it will appear saying that source not found. Therefore, one of the solution is to click Attach Source, External File, and click on the file of the Source Code. By then, the source code will be introduce manually.

2. Using Java Decompiler plug in: The JD plug in was use to check the Java source code directly. The reason why we use JD is that not all source code in Java classes can be found easily.Some of the individual programs, they do not include their source code, with just the.class file. If we want to see the source code, we can only decompile the.class file. This plugin makes it easy to view the source code of Java classes when you don't have the source code. It's just decompiled the file and with a little different from the original source code, but because Java bytecode is easy to decomcompile, it's good to use JD to view the source code when you don’t have the original source code.
