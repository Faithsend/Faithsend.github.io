---
layout: post
title: "oop concepts"
description: "classes and modules"
category: technical
tags: [technical, phase 0]
---
{% include JB/setup %}

Ruby provides a variety of tools to its programmer to create its Object Oriented framework, and numerous different ways to share methods, objects, and variables between different aspects of a project. Classes and Modules are two of these different tools provided, both of which touch upon the idea of inheritance. Both of them in general provide a collection of related methods, variables, and constants for other objects to call upon.

A class, for example, is a set of rules and attributes and behaviors that work together to describe a certain object. For example, a `Table` class could possess attributes such as the number of sides, the height of the table, its weight, as well as behaviors such as how many people it can comfortably fit, how it might fold up if it were a portable table, and so on. What's important to keep in mind, though, is that all classes created in a program will be descendants of another class. In most cases, this would be the `Object` superclass, which provides a host of methods that all objects in Ruby would have in common. Otherwise, a class's superclass might be a more general type of class, such as in this case a ` Furniture` class, which might provide its own methods and attributes to the `Table`, in addition to the superclass methods it itself would pass down from its own superclass, like `Object`. This chain is called inheritance, and provides for a flow of these features throughout all related objects.

A Module is somewhat similar in that it is defined as a collection of related methods, constants, and even classes. These can usually be listed in a separate file, so that any other class can refer to those collected methods through the `require` method. When a module is introduced in this way, its contents may be accessed through its namespace, or however the module was called. Helpfully, this can prevent clashes in the names of methods or constants because it requires the namespace to be appended, so that a `Trail.length` might know to refer to a distance in kilometers, while a `Word.length` would know that its going to use a number of characters instead.

While this might seem very similar to the functioning of classes, the more important feature of Modules is to provide for Mixins. A class can use the method `include *Module*` to refer a required module, so that it can make use of the methods and constants provided by that module. Enumerables are a great example of this feature, as you can `include` to allow your class to make use of the the Enumerable methods for traversal and sorting.

Going back to the idea of inheritance as mentioned above, this allows for a further degree of inheritance of methods than is provided by just classes and super-classes alone. It becomes possible for classes to acquire features of other classes on an ad-hoc basis, rather than relying on simply a chain between `Object` and itself. It is still using the module classes and methods as dependencies, but it doesn't require the class to be explicitly *defined* as a subclass.