---
layout: post
title: "Scala Methods and Functions"
date:   2015-12-22 15:26:00 +01:00
categories: scala basic
img: img/scala.png
author: "Nick Tombeur"
meta: "Scala Core"
tags:
 - Scala
---

### A method is attached to a class or object, while a function is its own object (this is why we can pass it around so easily).

# Method

A method is a block of statements that has a name and can be invoked from other places in your program.

{% highlight scala %}
def name(arg1: Type1, arg2: Type2): ReturnType = {
  /* ... */
}
{% endhighlight %}

__*Note:*__ In scala a method's name can have characters like +, ~, &, -, /, \, :, etc.

If you leave off the equals sign and method body, it will be declared _abstract_.

> Try the following in the REPL. What's the result?
>
>     class Foo {
>       def bar(): Boolean
>     }
>
> __*Note*__: we learn more about classes later on.

[ TODO: rewrite !!!]
The __*correct*__ use of methods can improve the quality of your program. In Scala you don't have to use the return keyword. A Scala method returns the last value computed by the method, in the absence of an explicit return statement. 
It is even recommended to avoid explicit and multiple return statements. You should aim to write quite small methods that yields one value, which will be returned.

[ TODO: rewrite !!!]

Methods with a result type of Unit, such as ChecksumAccumulator's add method, are executed for their side effects.
A side effect is generally defined as mutating state somewhere external to the method or performing an I/O action.

In add's case, for example, the side effect is that sum is reassigned. 
Another way to express such methods is to leave off the result type and the equals sign, and enclose the body of the method in curly braces. 
In this form, the method looks like a procedure, a method that is executed only for its side effects. The add method in Listing 4.1 illustrates this style:
Listing 4.1: · Final version of class ChecksumAccumulator.

// In file ChecksumAccumulator.scala
class  ChecksumAccumulator {
   private  var sum = 0
    def  add(b: Byte) { sum += b }
    def  checksum(): Int =  ~(sum & 0xFF) + 1
}

If you define a method return type Unit but you return a String, the value will be lost!

/* When we pass a method where a function is expected, Scala converts it
 * to a function. This is called 'lifting'.
*/

// Convert method to function
even _



## Style guide

* [Method declaration](http://docs.scala-lang.org/style/declarations.html#methods)
* [Method invocation](http://docs.scala-lang.org/style/method-invocation.html)


## Best practices

* Method without arguments can leave off the parentheses in the definition.
  * Leave parentheses on for mutating methods (methods that causes objects to change / side effects).
* You should make use of type inference for return types.
  * For public methods, you should define the return type. This makes their intent clear, to other developers, and enables the help of the compiler to detect errors.
* Curly braces are not needed for single result expressions. If the expressions is short, you can place it on the same line as the def itself.

# Function

[Cheatsheet](http://docs.scala-lang.org/cheatsheets/)

Functions are often quite small, and used once. A functions is also known as 'anonymous function' or 'function literal'.

[ TODO: rewrite !!! ]
- val is evaluated on initialization
- def is evaluated only when, and every time, the method is called.
lazy val will evaluate on first call; only once.

## Style guide

* [Function values](http://docs.scala-lang.org/style/declarations.html#function_values)
* [Function types](http://docs.scala-lang.org/style/types.html#functions)

## Best practices

* Single expression
  * drop curly braces
* Single argument
  *  drop the parentheses
* Zero arguments
  * needs empty parentheses




 TODO: REMOVE !!!
http://docs.scala-lang.org/cheatsheets/
http://docs.scala-lang.org/style/method-invocation.html
http://docs.scala-lang.org/style/