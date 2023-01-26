---
title: 'Integration by Partial Fraction'
date: 2023-01-16 17:40:00 +0900
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

# Method

Partial Fraction is thinking one fraction as a sums of multiple fractions.

$$
\begin{gather}
\frac{f(x)}{g(x)h(x)} = \frac{a}{g(x)} + \frac{b}{h(x)} \\\\
\implies f(x) = a \cdot h(x) + b \cdot g(x)
\end{gather}
$$

So it becomes easier to integrate with sums.

$$
\begin{gather}
\int \frac{f(x)}{g(x)h(x)} \,dx = \int \frac{a}{g(x)} + \frac{b}{h(x)} \,dx
\end{gather}
$$

# Plug in values to isoalte the variable

$$
\begin{gather}
a \cdot g(x) + b \cdot h(x) = f(x)
\end{gather}
$$

We can let
$$x = k$$
 which makes
$$ g(k) = 0 $$
.

So the equation becomes

$$
\begin{gather}
a \cdot g(k) + b \cdot h(k) = f(k) \\
\implies a \cdot 0 + b \cdot h(k) = f(k)
\end{gather}
$$

# Systems of equation

We can also use systems of equation to solve for `a` and `b`.

$$
\begin{gather}
\text{let } g(x) = x+2 \,, h(x) = x+3 \,, f(x) = 2x+5\\
a \cdot g(x) + b \cdot h(x) = f(x) \\
= a (x+2) + b (x+3) = 2x+5 \\
= ax + 2a + bx + 3b =2x + 5 \\
= (a+b)x + 2a + 3b = 2x + 5 \\
\implies a+b = 2 \\
\implies 2a + 3b = 5
\end{gather}
$$

Then we can solve for `a` and `b`.

$$
\begin{gather}
a+b = 2 \\
2a + 3b = 5 \\\\
2a + 3b = 5 \\
2a + 2b = 4 \\\\
2a - 2a + 3b - 2b = 1 \\
b = 1 \,, a=1
\end{gather}
$$

# Example

$$
\begin{align}
\int \frac{x}{x^2 -4} \,dx &= \int \frac{x}{(x+2)(x-2)} \,dx \\
&= \int \frac{a}{x+2} + \frac{b}{x-2} \,dx \\
\because x &= a(x-2) + b(x+2)
\end{align}
$$

Then [plug in values to isolate the variable](#plug-in-values-to-isoalte-the-variable).


$$
\begin{gather}
\text{let} \, x=2 \\
x = a(x-2) + b(x+2) \\
2 = a(2-2) + b(2+2) \\
2 = a \cdot 0 + b\cdot 4\\
2= 4b\\
\therefore b=\frac{1}{2}\\
\text{let} \, x= -2 \\
x = a(x-2) + b(x+2) \\
-2 = a(-2-2) + b(-2+2) \\
2 = a \cdot (-4) + b\cdot 0\\
-2= -4a\\
\therefore a=\frac{1}{2}
\end{gather}
$$

Plug `a` and `b` into original equation,

$$
\begin{align}
\int \frac{a}{x+2} + \frac{b}{x-2} \,dx &= \int \frac{1/2}{x+2} + \frac{1/2}{x-2} \,dx \\
&= \frac{1}{2} \int \frac{1}{x+2} + \frac{1}{x-2} \,dx \\
&= \frac{1}{2} \left( \ln|x+2|+ \ln|x-2|  \right) \\
&= \frac{1}{2} \ln|(x+2)(x-2)| \\
&= \frac{1}{2} \ln|x^2 -4|
\end{align}
$$
