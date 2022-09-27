---
description: You should know what these are already
---

# Modules

Modules are the features of your client. Killaura? Module. Clickgui? That's also a module. Everything your client does that the user can control is a module.

## Module class

This is where you need background knowledge of Java or OOP (object-oriented programming).&#x20;

You can really do this any way you'd like, but people do it certain ways for good reason. You should usually prioritize code cleanliness and readability over minor speed improvements/optimizations. The structure this section describes is the way I personally structure my mods.

#### Abstract parent class/interface

You should first make an abstract `ClientModule` class or interface. This is providing a common parent class and functionality to all of the modules you make. This allows for the Java complier to know what you're on about when you cast things and also lets you not code the same thing over and over again. For example, if you want to change what a method of your modules do by default, you only need to change it once in one spot rather then once for every one of your modules, everywhere.

#### Default implementations and Overriding

An example of a method I usually have is `loadSettings`. This method only needs to be implemented once in the `ClientModule` class, if you do it in an abstract way. If you are particularly generic about it, you won't even need to change this method when you add a new type of setting. This is a default implementation and can be called on all inheritors of `ClientModule` without issue (visibility allowing).

But let's say you want to change `loadSettings`, for some odd reason. To do this you simply override the method. You should look up how to do this for a proper explanation, but essentially you put `@Override` above a method with a signature that exists in a parent class and then implement as you wish. If you wanted to call the parent's implementation, you can do `super.<method>` and it'll be called. You cannot override final methods.

## Where to put your modules (file structure)

There are any number of ways to place your modules in your mod. You could stick them all in random directories with the name of the folder being a hashed string you made up, if you really wanted to.

The way I do this is have a `module` package containing a `ClientModule` class, `ClientModuleManager` class, and another package `modules` containing the implementations of the modules.
