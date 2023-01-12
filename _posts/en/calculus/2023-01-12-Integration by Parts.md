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

Integration by parts is a method to find a interal of product of functions

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

Often, It is also used as `ILATE` or `LIATE`. Here, `A` means `Algebraic function`

However, this does not always apply. For example, transcendental function would be more complicated when we integrate it.

In those cases, Fourier transform, Laplace transform, Taylor series, or gaussian integration (or etc) might be required, but I will not discuss it here.

# Example

In here, I will use form of 

$$
\begin{alignat}{}
\int g \cdot f' \,dx = gf - \int g' \cdot f \,dx 
\end{alignat}
$$

and I will set e<sup>x</sup> as `g`, the term we are going to take derivative,  following LIPET.

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

# Extra

There is a well know equation for solving the area using this technique and [beta function](https://mathworld.wolfram.com/BetaFunction.html).

$$
\begin{align}
y &= a(x - \alpha)^m(x - \beta)^n \\
S &= \left| a\int_\alpha^\beta (x - \alpha)^m(x - \beta)^n dx \right| \\
&= \left| a\frac{m!n!}{(m+n+1)}(\beta - \alpha)^{m+n+1} \right|
\end{align}
$$

## proof

$$
\begin{align}
y &= a(x - \alpha)^m(x - \beta)^n \\
S &= \left| a\int_\alpha^\beta (x - \alpha)^m(x - \beta)^n dx \right| \\

&t = x - \alpha \,, \quad dt = dx \\
&x \to \alpha \,, \text{ then } \quad t = \alpha - \alpha = 0 \\
&x \to \beta \,, \text{ then } \quad t = \beta - \alpha \quad \\
& \text{so, substitute upper and lower limit}\\

S &= \left| a\int_0^{\beta - \alpha} (t)^m(x - \alpha - \beta + \alpha)^n dt \right| \\
S &= \left| a\int_0^{\beta - \alpha} t^m[t + (\beta - \alpha)]^n dt \right| \\

u &= \frac{t}{\beta - \alpha} \,, \quad (\beta - \alpha)du = dt\\
&t \to 0 \,, \text{ then } \quad u = \frac{0}{\beta - \alpha} = 0\\
&t \to \beta - \alpha \,, \text{ then } \quad u = \frac{\beta - \alpha}{\beta - \alpha} = 1\\
& \text{substitute upper and lower limit again}\\

S &= \left| a\int_0^1 [(\beta - \alpha)u]^m[(\beta - \alpha)u - (\beta - \alpha)]^n (\beta - \alpha)du \right| \\
S &= \left| a\int_0^1 [(\beta - \alpha)u]^m[(\beta - \alpha)(u - 1)]^n (\beta - \alpha)du \right| \\
S &= \left| a\int_0^1 (\beta - \alpha)^mu^m(\beta - \alpha)^n(u - 1)^n (\beta - \alpha)du \right| \\
S &= \left| a\int_0^1 (\beta - \alpha)^m(\beta - \alpha)^n(\beta - \alpha)u^m(u - 1)^n du \right| \\
S &= \left| a\int_0^1 (\beta - \alpha)^{m+n+1}u^m(u - 1)^n du \right| \\
S &= \left| a(\beta - \alpha)^{m+n+1} \int_0^1 u^m(u - 1)^n du \right| \\

& \text{now use integration by parts until } u^m \text{ disappears} \\

S &= \left| a(\beta - \alpha)^{m+n+1} \cdot \left[ \frac{u^m}{n+1}(u-1)^{n+1} - \frac{m}{n+1} \int_0^1 u^{m-1}(u - 1)^{n+1} du \right] \right| \\
S &= \left| a(\beta - \alpha)^{m+n+1} \cdot \frac{1}{n+1} \left[\left[ u^m(u-1)^{n+1} \right]_0^1 - m \int_0^1 u^{m-1}(u - 1)^{n+1} du \right] \right| \\
S &= \left| a(\beta - \alpha)^{m+n+1} \cdot \frac{1}{n+1} \left[0 - m \int_0^1 u^{m-1}(u - 1)^{n+1} du \right] \right| \\
S &= \left| a(\beta - \alpha)^{m+n+1} \cdot \frac{-m}{n+1} \left[ \int_0^1 u^{m-1}(u - 1)^{n+1} du \right] \right| \\
S &= \left| a(\beta - \alpha)^{m+n+1} \cdot \frac{-m}{(n+1)(n+2)} \left[ \left[u^{m-1}(u-1)^{n+2}\right]_0^1 - (m-1)\int_0^1 u^{m-2}(u - 1)^{n+2} du \right] \right| \\
S &= \left| a(\beta - \alpha)^{m+n+1} \cdot \frac{-m}{(n+1)(n+2)} \left[0 - (m-1)\int_0^1 u^{m-2}(u - 1)^{n+2} du \right] \right| \\
S &= \left| a(\beta - \alpha)^{m+n+1} \cdot \frac{m(m-1)}{(n+1)(n+2)} \left[ \int_0^1 u^{m-2}(u - 1)^{n+2} du \right] \right| \\

& \qquad\qquad\qquad\qquad\qquad\qquad \vdots \\

S &= \left| a(\beta - \alpha)^{m+n+1} \frac{m!}{(n+1)(n+2)\cdots(n+m+1)} \right| \\
S &= \left| a(\beta - \alpha)^{m+n+1} \frac{n!m!}{n!(n+1)(n+2)\cdots(n+m+1)} \right| \\

&= \left| a\frac{m!n!}{(m+n+1)!}(\beta - \alpha)^{m+n+1} \right|
\end{align}
$$