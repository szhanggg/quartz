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
