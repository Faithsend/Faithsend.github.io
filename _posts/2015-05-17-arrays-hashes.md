---
layout: post
title: "arrays hashes"
description: "making a hash of things"
category: technical
tags: [technical, phase 0]
---
{% include JB/setup %}

Arrays and hashes are two of the more important and versatile data structures available in Ruby, able to quickly and easily traverse and transform large quantities of objects at once..

An array, simply put, is an ordered list of objects. Each object in an array is referenced by an integer value, known as the index. Thus the first item in an array is array[0], the second array[1], and so on (computers count using 0 as the starting point, rather than 1). New objects can be inserted into this array at various points, and it keeps them in that same order based on where the new object was added in. This makes it relatively easy to pull objects out again, based on the sequence in which they were added.

```
numbers = [ 5, 6, 7, 8]
numbers[0] => 5
numbers[2] => 7
```

A hash is similar to an array in that it represents a list of objects, but unlike an array it isn't ordered by integer values. Rather, instead of an index, it uses keys to associate with each value. This key can be any object, such as a string or an integer, and it associated only with one value. This is usually helpful where the values are referenced by a name or a non-ordered set of integers, where it wouldn't be useful or sensible to keep them in an ordered form.

```
prices = {'cereal'=>3.95, 'chicken'=>6.75, 'milk'=>2.75}
prices[:cereal] => 3.95
prices[:milk] => 2.75
```