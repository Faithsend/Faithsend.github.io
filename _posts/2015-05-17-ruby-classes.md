---
layout: post
title: "ruby classes"
description: "a rpg character as a class"
category: technical
tags: [technical, phase 0]
---
{% include JB/setup %}

Classes are an extraordinarily powerful feature of Ruby, as befits its object-oriented design. Object-oriented languages create objects for the code to interact with, which include both variable attributes and methods which work together to define its function. Classes are a fairly standard approach to creating objects, where each class defines a set number of methods and variables, acting as a blueprint for further instances of that class to be created and manipulated with.

Classes are extremely useful when dealing with sets of data that all follow the same basic principles and can be used in the same ways, but which might be different in their individual variables or designations. They provide a catalog of methods based on these commonalities, but which might reveal the specifics of each version of the object.

While this may sound complicated in the abstract, it's a lot simpler to see how this works using a concrete example. Characters in role-playing games make for a good example of how these classes might work. Every character would be an object, which would be defined from the greater Class of `Character`. When we create a new character, we provide the class with a list of attributes, such as the character's `name`, `gender`, `level`, `species`, `profession`, `strength`, and so on. This new `Character` object would store all these variables as instance variables, which are constant for all methods that relate to this specific `Character` object. Anytime the `name` variable is referenced within the instance of `Character`, it will recall the same value.

Now, let's add a method for calculating the value of a character's attack, based on its `strength` and a modifier. This modifier can be stored as a class variable, so that every `character` features the same modifier. This might be useful if we wanted to apply sweeping changes across every character, or if we wanted to set some baseline attributes for certain variables. Essentially, the difference is that every instance of a class will use the same class variables, while they would have different instance variables based on their object.

With this class based construction, it can easily compare the outputs of the same methods from different ` Characters`. It may run the same method to calculate the value of an attack for two different characters, and then use the comparison between them to decide who is more powerful, or who would win in a fight. By storing these attributes and methods in a related class, it becomes trivial to access them once more, or modify them as a character grows and changes.