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

Riemann Sum is approximating the area with the sum of areas.

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