---
title: 'Definite Intergral Basics'
date: 2023-01-31 13:15:00 +0900
author: kintiru
categories: [English, Calculus]   # [TOP_CATEGORIE, SUB_CATEGORIE]
tags: [English, Calculus, Math, AP Calculus BC]     # TAG names should always be lowercase
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

# Prerequisite

 * Derivatives
 * AntiDifferentiation
 * Indefinite Integral

# Definite Integral

Definite Integral represents area between the function and x axis.

If the area is above the x axis, the result will be positive.

If the area is under the x axis, the result will be negative.

In other words, it means the total change of $F(x)$ from $a$ to $b$.

So if the derivative is at negative value, the fucntion $F(x)$ will decrease, and it is the reason why the integral or the area under x axis is negative. 

$$
\begin{gather}
\int_a^b f(x) \space dx = F(b) - F(a) \\
\text{where } f(x) = \frac{d}{dx}F(x)
\end{gather}
$$

When rearranged, we get

$$
\begin{gather}
F(b) = F(a) + \int_a^b f(x) \space dx
\end{gather}
$$

which means the value of $F(b)$ is $F(a)$ plus the accumulation of change from $a$ to $b$.

# Proporties of Definite Integral

$$
\begin{align}
&(1) \quad \int_a^b cf(x) \space dx = c \int_a^b f(x) \space dx \\
&(2) \quad \int_a^b f(x) \pm g(x) \space dx = \int_a^b f(x) \space dx \pm \int_a^b g(x) \space dx \\
&(3) \quad \int_a^b c \space dx = c(b-a) \\
&(4) \quad \int_a^a f(x) \space dx = 0 \\
&(5) \quad \int_a^b f(x) \space dx = - \int_b^a f(x) \space dx \\
\end{align}
$$

# Differentiating the integral

$$
\begin{align}
\frac{d}{dx} \left[ \int_a^x f(t) \space dt \right] &= \frac{d}{dx}F(x) - \frac{d}{dx}F(a) \\
&= f(x) - 0 \\
&= f(x)
\end{align}
$$