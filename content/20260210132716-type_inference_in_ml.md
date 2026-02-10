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
