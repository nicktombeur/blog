---
layout: post
title: "Scala Introduction"
date:   2015-11-30 20:18:12
categories: scala basic
img: img/scala.png
author: "Nick Tombeur"
meta: "Scala Core"
tags:
 - Scala
---

This blog post is an introduction to Scala. In the upcoming posts, we will look further into the fundamentals of Scala.

Scala is a multi-paradigm programming language. This means that it supports more than one programming paradigm.  
In this case, object-oriented and functional.

History
=======
Scala is the brainchild of Martin Odersky. His objective, with creating Scala, was to improve Java.
Previously he had worked on Generic Java and javac.  
In 2011 he was named Top Java Ambassador.  
Scala was publicly released early 2004. In 2006, Scala has become stable and mature, after a considerable revision.  
In 2011, Odersky founded [Typesafe Inc.](https://www.typesafe.com/), a company to support and promote Scala.

Why Scala?
==========

- JVM
------
Scala is a programming language that is built on the JVM (Java Virtual Machine). This ensures that you get the advantages that Java has immediately in Scala.  
These are, for example, platform independence, security, performance, and much more.

- Statically typed
----------------
In short: static typing helps the programmer by detecting errors at compile time.
Scala supports type inference (ability to detect types) which reduces verbosity.  
[Learn more.](https://en.wikipedia.org/wiki/Type_system#Static_type-checking)

- Mixed paradigm
---------------
  - ### OOP
You are likely to be familiar with object-oriented programming, if you have any experience in a programming language, for instance, like Java or C#.  
Unlike Java (primitives or not objects, for instance), Scala is a pure object-oriented language. Every value is an object.  
Object-oriented mainly ensures readable and maintainable code.

  - ### FP
Functional programming is the same as mathematical functions and avoids changing-state. Programming is done with expressions.  
With functional programming we try to avoid mutable data, side effects.  
In later blog posts, we will look further into Functional Programming with Scala.  
[Learn more.](https://en.wikipedia.org/wiki/Functional_programming)

- Sophisticated type system
---------------------------
- Elegant, flexible syntax
-------------------------
- Scalable
--------

What about Java 8?
==================
Java 8 has introduced some great new features likes:

- lambda's, real anonymous functions.
- Interfaces allow "default" implementations. Making them more usable as composable mixins, like Scala traits.
- ...

But Scala adds many improvements that Java may never have, or may eventually have, but not until years from now, due to backward compatibility.  
An other benefit is that you can use Scala starting from JDK 6.

REPL
====
The Scala interpreter is also called the REPL (Read Evaluate Print Loop).  
The REPL is a great way to learn Scala or learn a certain library without all the boilerplate of creating a project.  
After you successfully installed Scala, you type **_scala_** on the command line and you will get the REPL.  

Try the following:

{% highlight scala %}
scala> "Hello World!"
res0: String = Hello World!
{% endhighlight %}

Use **_:help_** to learn more and **_:quit_** to exit the REPL.

Worksheet
=========
If you use an IDE like [IntelliJ](https://www.jetbrains.com/idea/) or [Eclipse](https://eclipse.org/home/index.php), you can make use of Worksheets instead of the REPL.
It allows you to experiment with Scala like the REPL.  
The main difference is that a worksheet evaluates on save and the result of each expression is shown to the right.

API
====
The [Scala API](http://www.scala-lang.org/api) is a great place to learn Scala. 
The most important thing to notice is that for some classes there is also an object (learn more about this in later posts). 
You can change from the class to the object or vice versa, by click on the green “C” or blue “O” at the top of the page.

![Scala API]({{ site.baseurl }}/assets/img/scalaAPI.png)

Learn more about using the API [here](http://docs.scala-lang.org/overviews/scaladoc/interface.html).

**_Tip_**: There are some useful applications offline documentation browsers.
[Dash](https://kapeli.com/dash) for OS X and iOS, [Zeal](https://zealdocs.org/) for Linux and Windows, 
[Velocity](https://velocity.silverlakesoftware.com/) for Windows.