---
title: "Young's Inequality"
author: ["Stephen Zhang"]
date: 2026-02-07T15:42:00-05:00
publishDate: 2026-02-07T15:42:00-05:00
lastmod: 2026-02-07T15:42:00-05:00
tags: ["21-269"]
draft: false
---

Suppose \\(p\in[1,\infty]\\) and \\(1/p + 1/q = 1\\). Then \\(\forall a,b \ge 0\\),
\\[
ab \le \frac{a^{p}}{p} + \frac{b^{q}}{q}
\\]

<div class="proof">

Consider \\(f(x) = \frac{x^{p}}{p} - xb\\). Following this, we get that \\(f'(x) = x^{p-1} - b\\). Thus,

1.  \\(x < b^{1/p-1} \implies f'(x) < 0\\)
2.  \\(x > b^{1/p-1} \implies f'(x) > 0\\)

Thus, we have that \\(x = b^{1/p-1}\\) is a minimum. Plugging in, we have
\\[

\begin{aligned}

\end{aligned}

\\]
Since this is the minimum point, we have that \\(f(x) \ge -\frac{b^{q}}{q}\\). So

\\[

\begin{aligned}
f(b^{1/p-1}) &= \frac{b^{p/(p-1)}}{p} - (b^{1/(p-1)})b \\\\
&= \frac{b^{q}}{p} - b^{q} \\\\
&= b^{q} \left( \frac{1}{p} - 1 \right) = -\frac{b^{q}}{q}
\end{aligned}

\\]

\\[
\frac{x^{p}}{p} + \frac{b^{q}}{q} \ge xb
\\]

</div>
