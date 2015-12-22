---
layout: post
title: "Scala Conditional Expressions"
date:   2015-12-22 10:40:00
categories: scala basic
img: img/scala.png
author: "Nick Tombeur"
meta: "Scala Core"
tags:
 - Scala
---

A condition is an expression that can be __*true*__ or __*false*__.  
The boolean expressions must be enclosed in parentheses.  

{% highlight scala %}
if (boolean_expression) {
  statement
} else if (boolean_expression) {
  statement
} else {
  statement
}
{% endhighlight %}

The entire __*if*__ itself is an expression. Which means it produces a result.
This allows you to write conditional expressions as followed:

{% highlight scala %}
val result = if (x > y) x else y

def biggestNumber(x: Int, y: Int): Int = if (x > y) x else y

val x: Boolean = { 10 > 2 }
{% endhighlight %}

__*Note:*__ notice that you don't have to write _return_ for returning a value, as compared to Java.  

<br />

# Best practices

Conditions should be written with a space following the defining keyword.

{% highlight scala %}
if (statement) ... else ...

// not
if(statement) ... else ...
{% endhighlight %}

When the expression is a pure-functional operation and all statements are single-line expressions you should omit the curly braces.
Keep the following in mind:
- If you have an __*else*__ clause, you should omit the braces.
- If you don't have an __*else*__ clause, surround the contents with curly braces even if the contents are only a single line.

{% highlight scala %}
val result = if (test)
  foo()
else
  bar()
  
if (test) {
  println("test is true")
}
{% endhighlight %}

<br />

# Exercises

1. Compare two integers. Display the larger number followed by "is larger". For equal numbers, print "These numbers are equal".
2. Calculate the BMI (Body Mass Index Calculator) of a person.
Formula:
  BMI = weightInPounds x 703 / heightInInches x heightInInches
  OR
  BMI = weightInKilograms / heightInMeters x heightInMeters
  
  Show the following messages:
  
| Result                | Message     |
| --------------------- | ------------|        |
| less than 18.5        | underweight |
| between 18.5 and 24.9 | normal      |
| between 25 and 29.9   | overweight  |
| 30 or greater         | obese       |