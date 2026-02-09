---
title: "Open and Closed Sets"
author: ["Stephen Zhang"]
date: 2026-02-09T17:56:00-05:00
publishDate: 2026-02-09T17:56:00-05:00
lastmod: 2026-02-09T17:56:00-05:00
tags: ["21-269"]
draft: false
---

Let \\((X, d)\\) be a metric space.

<div class="definition">

For \\(x \in X\\) and \\(r > 0\\), define

\\[
B(x, r) = \lbrace y \in X : d(x, y) < r \rbrace \text{ and } \overline{B}(x, r) = \lbrace y \in X : d(x, y) \leq r \rbrace
\\]

</div>

These are called the _open ball_ and _closed ball_ respectively.

<div class="definition">

We say a set \\(U \subseteq X\\) is _open_ if \\(\forall x \in U\\), \\(\exists r > 0\\) such that \\(B(x, r) \subseteq U\\).

</div>

<div class="definition">

We say a set \\(C\subseteq X\\) is _closed_ if \\(C^c\\) is open.

</div>

<div class="remark">

The sets \\(\emptyset\\) and \\(X\\) are both open and closed.

</div>

<div class="exampleblock">

With \\(X=\mathbb{R}\\) and \\(d(x,y)=|x-y|\\), we have the following examples of open and closed sets:

1.  \\((-\infty, a)\\), \\((a,b)\\), and \\((a, \infty)\\) are open.
2.  \\((-\infty, a]\\), \\([a,b]\\), and \\([a, \infty)\\) are closed.

</div>
