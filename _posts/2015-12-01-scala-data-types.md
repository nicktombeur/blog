---
layout: post
title:  "Scala data types"
date:   2015-12-01 18:56:35
categories: scala basic
img: img/scala.png
author: "Nick Tombeur"
meta: "Scala Core"
tags:
 - Scala
---
In Scala, all values are objects. There are no primitives types like in Java.  
This implies that in Scala you can call methods/functions on for instance integers.

Available data types are:
<table class="pure-table pure-table-bordered">
    <thead>
        <tr>
            <th>Data type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr class="pure-table-odd">
            <td>Byte</td>
            <td>8 bit signed value</td>
        </tr>
        <tr>
            <td>Short</td>
            <td>16 bit signed value</td>
        </tr>
        <tr class="pure-table-odd">
            <td>Int</td>
            <td>32 bit signed value</td>
        </tr>
        <tr>
            <td>Long</td>
            <td>64 bit signed value</td>
        </tr>
        <tr class="pure-table-odd">
            <td>Float</td>
            <td>32 bit IEEE 754 single-precision float</td>
        </tr>
        <tr>
            <td>Double</td>
            <td>64 bit IEEE 754 double-precision float</td>
        </tr>
        <tr class="pure-table-odd">
            <td>Char</td>
            <td>16 bit unsigned Unicode character</td>
        </tr>
        <tr>
            <td>String</td>
            <td>A sequence of Chars</td>
        </tr>
        <tr class="pure-table-odd">
            <td>Boolean</td>
            <td>Either the literal true or the literal false</td>
        </tr>
        <tr>
            <td>Unit</td>
            <td>Corresponds to no value (void in Java)</td>
        </tr>
        <tr class="pure-table-odd">
            <td>Null</td>
            <td>null or empty reference</td>
        </tr>
        <tr>
            <td>Nothing</td>
            <td>The subtype of every other type; includes no values</td>
        </tr>
        <tr class="pure-table-odd">
            <td>Any</td>
            <td>The supertype of any type; any object is of type Any</td>
        </tr>
        <tr>
            <td>AnyRef</td>
            <td>The supertype of any reference type</td>
        </tr>
    </tbody>
</table>

Value declarations
------------------
{% highlight scala %}
val name: Type = initialization
var name: Type = initialization
{% endhighlight %}

The **_val_** keyword is used for immutable (constants) objects, where **_var_** is used for mutable objects.  
This means that the value of a **_var_** can be changed over time while a **_val_** can only be declared once.

Immutable objects are favored over mutable objects in Functional Programming.
This makes multi-threading easier but also prevents side-effects.

While setting a value you can define the type yourself or let Scala infer it. This is known as **_type inference_**.  
Examples:

{% highlight scala %}
val name: String = "Nick"
val name = "Nick" // inferred
{% endhighlight %}

# Best practices

Don't start your variable names with the dollar sign, it's used for internal use.

Constants
---------
Constant names should be in upper case. A constant in Scala is similar to Java's _static final_ members.  
Example: the value Pi in scala.math:

{% highlight scala %}
package object math {
  ...
  final val Pi = java.lang.Math.PI
  ...
}
{% endhighlight %}

_**Note**_: final in Scala is not the same is final in Java. In Scala it means that the definition may not be overridden in subclasses.

Values, variables
------------------
Value and variable names should be in lower camel case.

{% highlight scala %}
val myName = ...
var yourName = ...
{% endhighlight %}

Inference
---------
Make use of type inference, but put clarity first. Make your code readable for other people.  
All public methods should have explicit type annotations because otherwise you can break client code when altering your code.  
It can also help to improve compile times.

# Exercises

1. Create a value, "Hello World!" and try to change it to something else. What happens?
2. How would you make it possible to change the value?
3. Play around with all the data types. Make use of the Scala API.