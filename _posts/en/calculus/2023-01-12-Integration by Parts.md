---
title: 'Integration by Parts'
date: 2023-01-12 12:40:00 +0900
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

# Proof

$$
\begin{align}
\frac{d}{dx} \big[ fg \big] &= f' \cdot g + g' \cdot f \\
\int \frac{d}{dx} \big[ fg \big] dx &= \int f' \cdot g \,dx + \int g' \cdot f \,dx \\
fg &= \int f' \cdot g \,dx + \int g' \cdot f \,dx \\
\int f' \cdot g \,dx &= fg - \int g' \cdot f \,dx \\
\text{then} \\
g &= \, u \,, f = v \\
g' \,dx &= \, du \,, f' \,dx = dv \\
 \text{therefore, } \\
 \int u \,dv &= \,uv - \int v \,du \\
\end{align}
$$

But I prefer the form of

$$
\begin{alignat}{}
\int g \cdot f' \,dx = gf - \int g' \cdot f \,dx 
\end{alignat}
$$

or if we swich f and g,

$$
\begin{alignat}{}
\int f \cdot g' \,dx = fg - \int f' \cdot g \,dx 
\end{alignat}
$$

# LIPET

The preference of choosing g, or u which is
 - the part that are not integrating
 - In other words, the part we are taking derivative

L: Logrithm

I: Inverse

P: Polynomial

E: Exponential

T: Trigonometry

# Example

In here, I will use form of 

$$
\begin{alignat}{}
\int g \cdot f' \,dx = gf - \int g' \cdot f \,dx 
\end{alignat}
$$

and I will set e^x^ as g, the term we are going to take derivative,  following LIPET.

$$
\begin{align}
\int e^x \cos(x) \,dx &= e^x \sin(x) - \int e^x \sin(x)\, dx \\
\int e^x \cos(x) \,dx &= e^x \sin(x) - \left( -e^x\cos(x) - (-1) \int e^x  \cos(x)\, dx \right) \\
\int e^x \cos(x) \,dx &= e^x \sin(x) - \left( -e^x\cos(x) + \int e^x  \cos(x)\, dx \right) \\
\int e^x \cos(x) \,dx &= e^x \sin(x) + e^x\cos(x) - \int e^x  \cos(x)\, dx  \\
2 \int e^x \cos(x) \,dx &= e^x \sin(x) + e^x\cos(x) \\
\int e^x \cos(x) \,dx &= \frac{ e^x \sin(x) + e^x\cos(x) }{2} + C\\
\end{align}
$$

