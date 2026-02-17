---
title: "Higher-Order Functions in ML"
author: ["Stephen Zhang"]
date: 2026-02-17T12:44:00-05:00
publishDate: 2026-02-17T12:44:00-05:00
lastmod: 2026-02-17T12:44:00-05:00
tags: ["15-150"]
draft: false
---

## Curried Functions {#curried-functions}

```sml
fun add (x: int, y: int): int = x + y

fun plus (x : int): int -> int = fn (y: int) => x + y

val incr3: int -> int = plus 3
```

The idea here is that with a function like `add` that takes in two arguments, we can make
another function that sets one of the two.

We can write this with some syntatic sugar

```sml
fun plus x = fn y => x + y
val sum = fn x => fn y => fn z => x + y + z;

fun plus x y = x + y
fun sum x y z = x + y + z
```

Example: `filter`

```sml
fun filter p [] = []
  | filter p (x::xs) =
    if
        p(x)
    then
        x :: (filter p xs)
    else
        filter p xs
```

Thus, `filter` is of type `('a -> bool) -> 'a list -> 'a list`

If we define

```sml
val keepevens = filter (fn n => n mod 2 = 0)
```

`keepevens` will be of type `int list -> int list`.
