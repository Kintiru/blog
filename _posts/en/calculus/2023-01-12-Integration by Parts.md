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
\end{align}
$$
Then, we can set g and f to other variable.
$$
\begin{align}
g &= \, u \,, f = v \\
g' \,dx &= \, du \,, f' \,dx = dv \\
\end{align}
$$

then we can rewrite the equation like below.

$$
\begin{align}
\int u \,dv = \,uv - \int v \,du \\
\end{align}
$$

But I prefer the form of because we are not farmilar with `udv`, `uv`, or `vdu`.  

$$
\begin{align}
\int g \cdot f' \,dx = gf - \int g' \cdot f \,dx 
\end{align}
$$

or if we swich f and g, we can also write like below.

$$
\begin{align}
\int f \cdot g' \,dx = fg - \int f' \cdot g \,dx 
\end{align}
$$

# LIPET

The preference of choosing g, or u which is
 - the part that are not integrating
 - In other words, the part we are going to differentiate

`g(x)`, or `u` (to be differentiated)

L: Logrithm

I: Inverse

P: Polynomial

E: Exponential

T: Trigonometry

`f(x)`, or `v` (to be integrated)

However, this does not always apply. For example, transcendental function would be more complicated when we integrate it.

In those cases, Fourier transform, Laplace transform, Taylor series, or gaussian integration (or etc) might be required, but I I do not think it would be assessed in Calc BC.

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

