---
title: "Weierstrass Equations"
author: ["Stephen Zhang"]
tags: ["cryptography"]
draft: false
---

## Definition {#definition}

They take on the form
\\(E: Y^2 = X^3 + aX + b\\)


## ECC {#ecc}


### Point Addition {#point-addition}

Given two points \\(P\\),\\(Q\\) we define point addition \\(P+Q\\) as:
Take the line segment between \\(P\\),\\(Q\\) and find where it intersects the curve a third time.
Mark this intersection as point \\(R\\). Finally, take \\(R\\) and reflect it along the \\(y\\) direction to produce \\(R'\\).
\\(P+P\\) is similarly defined as the tangent line at point \\(P\\).
If there is no third intersection, then they intersect with \\(O\\), the point at infinity.
\\(O\\) acts as the identity operator, thus
\\(P+O=P\\) and \\(P+(-P)=O\\)


#### Properties {#properties}

1.  \\(P+O=O+P=P\\)
2.  \\(P+(-P)=O\\)
3.  \\((P+Q)+R = P+(Q+R)\\)
4.  \\(P+Q=Q+P\\)


#### Algorithm {#algorithm}

1.  If \\(P=O\\) then \\(P+Q=Q\\)
2.  Otherwise, write \\(P=(x\_1,y\_1)\\) and \\(Q=(x\_2,y\_2)\\)
3.  e1) If \\(P\neq Q\\): \\(\lambda = (y\_2-y\_1)/(x\_2-x\_1)\\)
    e2) Otherwise: \\(\lambda = (3x\_1^2+a)/2y\_1\\)
4.  \\(x\_3 = \lambda^2 - x\_1 - x\_2\\)
5.  \\(y\_3 = \lambda(x\_1-x\_3) - y\_1\\)
6.  \\(P + Q = (x\_3,y\_3)\\)


### Motivation {#motivation}

With this edition of point addition, it turns out that scalar multiplication, or repeated point addition, is actually a one-way function.
