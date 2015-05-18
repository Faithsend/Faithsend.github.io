---
layout: post
title: "javascript"
description: "Javascript Objects and Ruby Hashes"
category: technical
tags: [technical, phase 0]
---
{% include JB/setup %}

One of the more curious examples of differences between Ruby and Javascript is the Hash data structure. While Ruby officially supports a Hash structure, the same can't be said of Javascript. Instead, the implementation of Objects in Javascript serves the same function, though phrased and with slightly different features.

Hashes in Ruby are an explicit data structure, storing values within it that correspond to specific keys. every key can be something different, like a string, an integer, an object, and so on. each key maps to a value, and the data structure as a whole can be traversed and iterated over using different Hash or enumerable methods.

Javascript Objects work somewhat similarly, where Objects hold a collection of properties that each have their own value associated with it. This essentially works the same way as the key-value pairs in Ruby Hashes, where the value doesn't exist in the object until its assigned a valid property. Objects are slightly different though, in that they can incorporate their own methods as well as the data it includes. This means you can call included methods within the object if it doesn't need to be used with any other data structures or elsewhere in the program, so long as its associated with the Object itself. The Object can also easily be traversed and iterated over using their own methods, such as ForEach, or In, which iterate over property within the Object.