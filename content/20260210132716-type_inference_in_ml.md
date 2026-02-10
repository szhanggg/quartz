---
title: "Type Inference in ML"
author: ["Stephen Zhang"]
date: 2026-02-10T13:27:00-05:00
publishDate: 2026-02-10T13:27:00-05:00
lastmod: 2026-02-10T13:27:00-05:00
tags: ["15-150"]
draft: false
---

Given an expression, SML determines the **most general type** for the expression consistent with all the constraints.

<div class="definition">

A _most general type_ for an expression `e` is a type `t` such that `e:t` follows from the typechecking rules
and if `e:t'` also follows from the typechecking rules, then `t'` is an instance of `t`.

</div>

We say that `t'` is an _instance_ of `t` if one can obtain `t'` from `t` by instantiating type variables in a consistent way.

```sml
fun fst (x, y) = x
```

This function would be of type `'a * 'b -> 'a`.

```sml
fun square x = x * x * 1
fun sqrf(f, x) = square( f(x) )
```

The type of `square` is `int -> int`. Thus, the type of `f` must be `'a -> int`. Therefore, the type of `sqrf` is `(('a -> int) * 'a) -> int`.

```sml
fun g x = g x
fun h x = h (h x)
```

The type of `g` is `'a -> 'b`. The type of `h` is `'a -> 'a`.

<div class="remark">

Function application in SML is _left associative_.
This means that `f g x` is parsed as `(f g) x` and not `f (g x)`.

</div>
