---
title: "Polymorphism in ML"
author: ["Stephen Zhang"]
date: 2026-02-10T13:23:00-05:00
publishDate: 2026-02-10T13:23:00-05:00
lastmod: 2026-02-10T13:23:00-05:00
tags: ["15-150"]
draft: false
---

We want to have generic functions that work no matter the datatype.
For example, maybe we want a list length function that works no matter `int list`, `int list list`, etc.

What we can do for this is by using _type variables_.

<div class="definition">

A type variable is a type that is quantified over types. They are enumerated as `'a`, `'b`, `'c`, and so on.
However they are pronounced alpha, beta, etc.

</div>

Thus, we can write the length function as

```sml
fun length ([] : 'a list) : int = 0
  | length (x::xs : 'a list) : int = 1 + length xs
```
