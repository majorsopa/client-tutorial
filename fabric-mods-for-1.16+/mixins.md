---
description: Injecting Java code at runtime with Fabric
---

# Mixins

## What is a mixin?

A mixin is "a language concept that allows a programmer to inject some code into a class. Mixin programming is a style of software development, in which units of functionality are created in a class and then mixed in with other classes. A mixin class acts as the parent class, containing the desired functionality."

## What's the point of mixins?

Mixins allow you to do is change existing code to call your own (or not) methods, instead of completely overriding everything. This allows for ease of development and better compatibility.

## How do I make a mixin?

For this question I will direct you to the [fabric wiki](https://fabricmc.net/wiki/tutorial:mixin\_introduction).

{% hint style="info" %}
To easily get the mixin signature in Intellij, you can:

* Hit the left shift button twice
* Search for your method/field/class
* Right-click the method/field/class
* Click "copy mixin target reference"
{% endhint %}
