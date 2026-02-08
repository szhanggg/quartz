---
title: "Typechecking in ML"
author: ["Stephen Zhang"]
date: 2026-02-08T14:18:00-05:00
publishDate: 2026-02-08T14:18:00-05:00
lastmod: 2026-02-08T14:18:00-05:00
tags: ["15-150"]
draft: false
---

An expression typechecks if it is well-typed.

-   SML will never evaluate any ill-typed expressions.
-   If an expression \\(e\\) is well-typed, then SML will reduce the expression.

`(e1, e2...): (t1, t2...)` if `(e1 : v1), (e2: v2)...` where `v1` is of type `t1` and so on.

```sml
let
    val polly = "polly"
in
    let
        fun polly x = x + 1
    in
        polly ^ "loves 150"
    end
end
```
