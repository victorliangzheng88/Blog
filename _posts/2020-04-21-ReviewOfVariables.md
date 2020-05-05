---
layout: post
title: "Review of Types of Variables and Aspects of Method"
date: 2020-04-21 12:00:00 -0500
---

Static Variables: Are initialized only once in the entire process, allocated only one space in memory, and have the same value no matter where they are called. Once modified, all references to it will follow.

Instance Variables: Instance variable does not have to be initialized, such as an integer instance variable. If not initialized, the default value is 0. Local variables are syntactically passed if they are not assigned an initial value, but the program will report an error when using this variable. Instance variables allocate memory space in both the heap and the stack, where the object itself is allocated and the stack is a reference to the object.

Local Variables: Local variable is a variable declared in the method, the variable disappeared after the end of the method. Local variables must be initialized before they are used, otherwise, an error will be reported. That is, if you define a local variable in a method and do not assign a value to it, then you must assign a value to it while using the variable, otherwise, you will be reported with an error. In addition, when a local variable has the same name as one of the instance variable, the local variable shadows the instance variable inside the method block.

The method header consists of an access control character (public, private, etc.), a return type (the return type determines the type of result that the method will produce after being called), a method name, and a parameter list. A method declared void that returns an empty value. In special cases, we can add special keywords to methods to achieve special functionality, such as synchronized, final, static, abstract, and so on. In addition to method, I want to introduce two important aspects: overloading and overriding.

Overloading: A mechanism between methods with the same method name and different parameter lists in the same class. The different parameter lists can be in different types, different Numbers, different orders, as long as any one of them can be satisfied.
Example: 

```sh
public class AreaCal {
 
	/* Calculate Area of Rectangle */
	public int area(int width, int height) {
		return width * height;
	}
 
	/* Calculate Area of Square */
	public int area(int edge) {
		return edge * edge;
	}
 
	/* Calculate Area of Circle */
	public double area(float radius) {
		return 3.14 * radius * radius;
	}
}
```

As the example shows, the same method name area synchronously passes in different parameters to achieve different functions. This is called method overloading.

Overriding: Overrides exist in inheritance, a mechanism by which a subclass overrides a superclass method with the same method name and the same arguments in two classes. When a subclass inherits the parent class, we want to extend to the superclass method function, in this case, you can use the overriding. When you need to extend new functions, you don't need a new method, you can just override it to achieve your goal.
Example:

```sh
public class B extends A {
	
	public String a(String name) {
		return "Hello: " + name;
	}
}
class A {
	public String a(String name){
		return "Welcome: "+name;
	}
}
```
