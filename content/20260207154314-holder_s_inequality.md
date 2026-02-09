---
title: "Holder's Inequality"
author: ["Stephen Zhang"]
date: 2026-02-07T15:43:00-05:00
publishDate: 2026-02-07T15:43:00-05:00
lastmod: 2026-02-07T15:43:00-05:00
tags: ["21-269"]
draft: false
---

Suppose \\(p \in [1, \infty]\\) and \\(1/p + 1/q = 1\\). Then \\(\forall x,y\in\mathbb{R}^{d}\\),

\\[
\left|x\cdot y\right| \leq \left|x\right|\_p \left|y \right|\_q
\\]

<div class="proof">

We consider each component separately, and apply [Young's Inequality]({{< relref "20260207154203-young_s_inequality.md" >}}) to each component.

\\(a = \frac{|x\_{i}|}{|x|\_{p}}\\), \\(b = \frac{|y\_{i}|}{|y|\_{q}}\\)

From Young's we get
\\[
\frac{|x\_{i}||y\_{i}|}{|x|\_{p}|y|\_{q}} \le \frac{|x\_{i}|^{p}}{p|x|^{p}\_{p}} + \frac{|y\_{i}|^{q}}{q|y|^{q}\_{q}}
\\]

Summing over all components yields

\\[
\sum\_{i=1}^{d} \frac{|x\_{i}||y\_{i}|}{|x|\_{p}|y|\_{q}} \leq \frac{1}{p} + \frac{1}{q} = 1
\\]

Furthermore, by Triangle Inequality, we see that
\\[
\lvert x \cdot y \rvert \leq \sum\_{i=1}^d |x\_i| \cdot |y\_i| \leq \lvert x \rvert\_{p} \lvert y \rvert\_{q}
\\]

</div>
