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
B(x, r) = \lbrace y \in X : d(x, y) < r \rbrace
\\]
\\[
\overline{B}(x, r) = \lbrace y \in X : d(x, y) \leq r \rbrace
\\]

</div>

These are called the _open ball_ and _closed ball_ respectively.

<div class="definition">

We say a set \\(U \subseteq X\\) is _open_ if \\(\forall x \in U\\), \\(\exists r > 0\\) such that \\(B(x, r) \subseteq U\\).

</div>

<div class="definition">

We say a set \\(C\subseteq X\\) is _closed_ if \\(C^c\\) is open.

</div>

It's important to note that not being open does not imply being closed. In fact,

<div class="remark">

The sets \\(\emptyset\\) and \\(X\\) are both open and closed.

</div>

<div class="exampleblock">

With \\(X=\mathbb{R}\\) and \\(d(x,y)=|x-y|\\), we have the following examples of open and closed sets:

1.  \\((-\infty, a)\\), \\((a,b)\\), and \\((a, \infty)\\) are open.
2.  \\((-\infty, a]\\), \\([a,b]\\), and \\([a, \infty)\\) are closed.

</div>

The proof for this is relatively straightforward using the definitions.

<div class="proposition">

1.  If \\(\lbrace U\_{\alpha} \rbrace\_{\alpha \in A}\\) is a collection of open sets, then \\(\bigcup\_{\alpha \in A} U\_{\alpha}\\) is open.
2.  If \\(U\_1, U\_2, \ldots, U\_n\\) are open sets, then \\(\bigcap\_{i=1}^n U\_i\\) is open
3.  If \\(\lbrace C\_{\alpha} \rbrace\_{\alpha \in A}\\) is a collection of closed sets, then \\(\bigcap\_{\alpha \in A} C\_{\alpha}\\) is closed.
4.  If \\(C\_1, C\_2, \ldots, C\_n\\)

</div>

The idea here is that an infinite union of open sets or a **finite** intersection of open sets is open.
Similarly, an infinite intersection of closed sets or a **finite** union of closed sets is closed.

A simple counterexample for finiteness are the sets \\(U\_n = (-1/n, 1/n)\\) whose intersection is \\(\\{0\\}\\), which is not open.


## Closure, Interior, and Boundary {#closure-interior-and-boundary}

<div class="definition">

We say \\(N\\) is a _neighborhood_ of \\(x\\) if \\(x \in N\\) and \\(N \subseteq X\\) is open.

</div>

That is to say, any open set containing \\(x\\) is a neighborhood of \\(x\\).

<div class="definition">

Let \\(E \subseteq X\\). We say the _boundary_ of \\(E\\), denoted \\(\partial E\\), is defined as
\\[
\partial E = \lbrace x \in X : \forall \text{ neighborhoods } N \text{ of } x, N \cap E \neq \emptyset \text{ and } N \cap E^c \neq \emptyset \rbrace
\\]
\#+begin_definition
Basically, the boundary is the set of points such that no matter how small a ball you take around it, it will always intersect both \\(E\\) and its complement.
\#+begin_definition
We say the _closure_ of \\(E\\), denoted \\(\overline{E}\\) is defined as
\\[
\overline{E} = \bigcap\_{C \supseteq E, C \text{ closed}} C
\\]

</div>

Similarly, we say the _interior_ of \\(E\\), denoted \\(E^{\circ}\\) is defined as

<div class="definition">

\\[
\mathring{E} = \bigcup\_{U \subseteq E, U \text{ open}} U
\\]

</div>

One way of thinking about these definitions is that the closure is the smallest closed set containing \\(E\\), while the interior is the largest open set contained in \\(E\\).

<div class="proposition">

\\(\partial E = \overline{E} \setminus \mathring{E}\\)

</div>

This statement is not too hard to prove using the definitions.
