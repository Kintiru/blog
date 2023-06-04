---
title: 'Rimann Sum'
date: 2023-01-26 11:40:00 +0900
author: kintiru
categories: [English, Calculus]   # [TOP_CATEGORIE, SUB_CATEGORIE]
tags: [English, Calculus, AP Calculus BC, Math]     # TAG names should always be lowercase
math: true
mermaid: true
#img_path: 
#image: #preview image
    #path:
    #alt:
    #lqpq:
#pin: true
---
<!--- 
Include script per post to prevent version break and better per post management
-->
<script src="https://cdn.jsdelivr.net/npm/chart.js@4.1.2/dist/chart.umd.js"></script>

# Prerequisites

* Sequences
* Basic Integration

---

Riemann Sum is approximating the area with the sum of smaller areas.

There are various types of Riemann sums, but here are some well known ones
 1. Left Riemann Sum
 2. Right Riemann Sum
 3. Midpoint Riemann Sum
 4. Trapazoid Riemann Sum

# Geometric Meaning

Most common shapes used in Riemman sum are trapezoid and square.


![Right Riemann Sum](https://upload.wikimedia.org/wikipedia/commons/8/82/Riemann-Sum-right-hand.png)
_Right Riemann Sum_

# Equation

This is general form of Riemman Sum.

$$
\begin{gather}
\sum f(x) \Delta x
\end{gather}
$$


$$
\begin{gather}
\int_a^b f(x) \space dx = \lim_{n \to \infty } \sum^n_{k=1} f \left( a + \frac{b-a}{n}k \right) \frac{b-a}{n}
\end{gather}
$$

This equation is using right riemman sum.

The left riemman sum will be

$$
\begin{gather}
\int_a^b f(x) \space dx = \lim_{n \to \infty } \sum^{n-1}_{k=0} f \left( a + \frac{b-a}{n}k \right) \frac{b-a}{n} \\
= \lim_{n \to \infty } \sum^n_{k=1} f \left( a + \frac{b-a}{n}(k-1) \right) \frac{b-a}{n}
\end{gather}
$$

Note that the bound changes (or the k inside sum notation).

If you do not change accordingly, it causes subtle error.

However, in most of the cases does not matter when computing, but it is an important concept.