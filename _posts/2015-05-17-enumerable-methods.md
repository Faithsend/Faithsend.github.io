---
layout: post
title: "enumerable methods"
description: "repetition through cycle"
category: technical
tags: [technical, phase 0]
---
{% include JB/setup %}

Enumerables as a class are an incredibly powerful tool to use when dealing with data structures, particularly for hashes and arrays. Enumerables are a sort of superclass, providing these extra methods for searching through and sorting these arrays and hashes.

As an example, one of the methods available for enumerables is the `cycle` method. This method runs through every element of the given data structure, and executes a block of code on each of these elements. This will repeat either infinitely, or for a given number of iterations. To do this otherwise, without using an enumerables, you'd have to nest loops in messy logic and multiple iterators to accomplish the same thing.

```
example = ["hip","hip","hooray"]

example.cycle {|element| puts element} # hip hip hooray hip hip hooray hip hip hooray hip hip hooray ... (repeated infinitely)

example.cycle(3) {|element puts element} # hip hip hooray hip hip hooray hip hip hooray
```

As the above code suggests, the original array isn't changed at all by the block of code, allowing it to be run repeatedly. A more complicated use of this could use `cycle` to populate an empty hash with the same set of filler values and keys, to be replaced later. Or it could be used to return the same countdown from 10 constantly, and have it reset to 10 upon reaching 0.