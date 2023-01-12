---
title: 'Derivatives of trig functions'
date: 2023-01-11 ::00 +0900
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

# Prerequisite
 - Limit
 - Power Rule
 - Chain Rule
 - Implicit Differenciation
 - [Trig Identities](https://www2.clarku.edu/faculty/djoyce/trig/identities.html)

# Key Points

 - Any trignometric functions that starts with c will be negative
   - cos, csc, cot (same in arc functions) 

# Basic Trigonometric Functions

## sin 

$$
\begin{align}
y &= \sin (x) \\
\frac{dy}{dx} &= \lim_{h \to 0}{ \frac{\sin(x+h) - \sin (x)}{h} } \\
&= \lim_{h \to 0}{ \frac{2 \sin(\frac{x + h - x}{2})\cos(\frac{x + h + x}{2})}{h} } \\
&= \lim_{h \to 0}{ \frac{2 \sin(\frac{h}{2})\cos(\frac{2x + h}{2})}{h} } \\
&= \lim_{h \to 0}{ \frac{\sin(\frac{h}{2})\cos(x + \frac{h}{2})}{h/2} } \\
&= \lim_{h \to 0}{ \frac{\sin(\frac{h}{2})}{h/2} \cos\left(x + \frac{h}{2}\right)} \\
&= \lim_{h \to 0}{ 1 \times \cos\left(x + 0\right)} \\
&= \cos(x)
\end{align}
$$

## cos

$$
\begin{align}
y &= \cos (x) \\
\frac{dy}{dx} &= \lim_{h \to 0}{ \frac{\cos(x+h) - \cos (x)}{h} } \\
&= \lim_{h \to 0}{ \frac{\cos(x)\cos(h)-\sin(x)\sin(h)-\cos(x)}{h} } \\
&= \lim_{h \to 0}{ \frac{\cos(x)(\cos(h)-1)-\sin(x)\sin(h)}{h} } \\
&= \lim_{h \to 0}{ \frac{\cos(x)(\cos(h)-1)}{h} - \frac{\sin(x)\sin(h)}{h} } \\
&= \lim_{h \to 0}{ \cos(x)\frac{(\cos(h)-1)(\cos(h)+1)}{h(\cos(h)+1)} - \sin(x)\cdot\frac{{\sin(h)}}{{h}} } \\
&= \lim_{h \to 0}{ \cos(x)\frac{\cos^2(h)-1}{h(\cos(h)+1)} - \sin(x)\cdot\frac{{\sin(h)}}{{h}}} \\
&= \lim_{h \to 0}{ \cos(x)\frac{-\sin^2(h)}{h(\cos(h)+1)} - \sin(x)\cdot\frac{{\sin(h)}}{{h}}} \\
&= \lim_{h \to 0}{ \cos(x)\frac{{\sin(h)}}{{h}} \cdot \frac{-\sin(h)}{(\cos(h)+1)} - \sin(x)\cdot\frac{{\sin(h)}}{{h}}} \\
&= \lim_{h \to 0}{ \cos(x) \cdot 1 \cdot \frac{0}{2} - \sin(x) \cdot 1 } \\
&= \lim_{h \to 0}{ 0 - \sin(x) } \\
&= - \sin(x)
\end{align}
$$

## tan

$$
\begin{align}
y &= \tan (x) = \frac{\sin(x)}{\cos(x)}=\sin(x)(\cos(x))^{-1} \\
\frac{dy}{dx} &= \frac{d}{dx}\bigg[\sin(x)\bigg]\cdot(\cos(x))^{-1} + \sin(x)\cdot\frac{d}{dx}\bigg[(\cos(x))^{-1}\bigg] \\
&= \cos(x)\cdot(\cos(x))^{-1} + \sin(x)\cdot(-1)(\cos(x))^{-2}\frac{d}{dx}\bigg[\cos(x)\bigg] \\
&= 1 + \sin(x)\cdot(-1)(\cos(x))^{-2}\cdot(-\sin(x)) \\
&= 1 + \sin^2(x)\cdot(\cos(x))^{-2} \\
&= 1 + \frac{\sin^2(x)}{\cos^2(x)} \\
&= 1 + \tan^2(x) \quad \leftarrow \text{trig identity}\\
&= \sec^2(x)
\end{align}
$$

#  Reciprocal Trigonometric Functions

## csc

$$
\begin{align}
y &= \csc (x) = \frac{1}{\sin(x)}=(\sin(x))^{-1} \\
\frac{dy}{dx} &= \frac{d}{dx}\bigg[(\sin(x))^{-1}\bigg]\\
&= (-1)(\sin(x))^{-2}\frac{d}{dx}\bigg[\sin(x)\bigg] \\
&= -(\sin(x))^{-2}\cos(x) \\
&= -\frac{\cos(x)}{\sin^2(x)} \\
&= -\frac{1}{\sin(x)}\cdot\frac{\cos(x)}{\sin(x)} \\
&= -\csc(x)\cot(x) \\
\end{align}
$$

## sec

$$
\begin{align}
y &= \sec (x) = \frac{1}{\cos(x)}=(\cos(x))^{-1} \\
\frac{dy}{dx} &= \frac{d}{dx}\bigg[(\cos(x))^{-1}\bigg]\\
&= (-1)(\cos(x))^{-2}\frac{d}{dx}\bigg[\cos(x)\bigg] \\
&= -(\cos(x))^{-2}\cdot(-\sin(x)) \\
&= \frac{\sin(x)}{\cos^2(x)} \\
&= \frac{1}{\cos(x)}\cdot\frac{\sin(x)}{\cos(x)} \\
&= \sec(x)\tan(x) \\
\end{align}
$$

## cot

$$
\begin{align}
y &= \cot (x) = \frac{\cos(x)}{\sin(x)}=\cos(x)(\sin(x))^{-1} \\
\frac{dy}{dx} &= \frac{d}{dx}\bigg[\cos(x)\bigg]\cdot(\sin(x))^{-1} + \cos(x)\cdot\frac{d}{dx}\bigg[(\sin(x))^{-1}\bigg] \\
&= - \sin(x)\cdot(\sin(x))^{-1} + \cos(x)\cdot(-1)(\sin(x))^{-2}\frac{d}{dx}\bigg[\sin(x)\bigg] \\
&= -1 + \cos(x)\cdot(-1)(\sin(x))^{-2}\cos(x) \\
&= -1 - \cos^2(x)\cdot(\sin(x))^{-2} \\
&= -1 - \frac{\cos^2(x)}{\sin^2(x)} \\
&= -1 - \cot^2(x) \\
&= -(1 + \cot^2(x)) \quad \leftarrow \text{trig identity} \\
&= -\csc^2(x)
\end{align}
$$

# Inverse Trigonometric Functions

## arcsin

$$
\begin{align}
y &= \sin(\theta) \\
x &= \cos(\theta) \\
x&^2+y^2=1 \\
y^2 &= 1 - x^2 \\
y &= \sqrt{1 - x^2} \\
\frac{dy}{dx} &= \frac{\cancel{2}x}{\cancel{2}\sqrt{1-x^2}} \\
\frac{dy}{d\theta}\cdot\frac{d\theta}{dx} &= \frac{x}{\sqrt{1-x^2}} \\
\frac{d\sin(\theta)}{d\theta}\cdot\frac{d\theta}{dx} &= \frac{x}{\sqrt{1-x^2}} \\
\cancel{\cos(\theta)}\cdot\frac{d\theta}{dx} &= \frac{\cancel{\cos(\theta})}{\sqrt{1-x^2}} \\
\frac{d\theta}{dx} &= \frac{1}{\sqrt{1-x^2}} 
\end{align}
$$

## arccos

$$
\begin{align}
y &= \sin(\theta) \\
x &= \cos(\theta) \\
x&^2+y^2=1 \\
x^2 &= 1 - y^2 \\
x &= \sqrt{1 - y^2} \\
\frac{dx}{dy} &= \frac{\cancel{2}y}{\cancel{2}\sqrt{1-y^2}} \\
\frac{dx}{d\theta}\cdot\frac{d\theta}{dy} &= \frac{y}{\sqrt{1-y^2}} \\
\frac{d\cos(\theta)}{d\theta}\cdot\frac{d\theta}{dy} &= \frac{y}{\sqrt{1-y^2}} \\
(-1)(\cancel{\sin(\theta)})\cdot\frac{d\theta}{dy} &= \frac{\cancel{\sin(\theta})}{\sqrt{1-y^2}} \\
\frac{d\theta}{dy} &= -\frac{1}{\sqrt{1-y^2}} 
\end{align}
$$

## arctan

$$
\begin{align}
\theta &= \tan^{-1}(x) \\
\tan(\theta) &= x \\
\frac{d}{dx}\bigg[\tan(\theta)\bigg]&=1 \\
\sec^2(\theta)\frac{d\theta}{dx}&=1 \\
\frac{d\theta}{dx}&=\frac{1}{\sec^2(\theta)} \\
&=\frac{1}{1+\tan^2(\theta)} \\
&=\frac{1}{1+x^2} \\
\end{align}
$$

## arccsc

$$
\begin{align}
\cos^2(\theta) + \sin^2(\theta) &= 1 \\
\cos^2(\theta) &= 1 - \sin^2(\theta) \\
\cos^2(\theta) &= 1 - \frac{1}{\csc^2(\theta)} \\
\cos(\theta) &= \sqrt{1 - \frac{1}{\csc^2(\theta)}} \\
\end{align}
$$

manipulate trig

$$
\begin{align}
\theta &= \csc^{-1}(x) \\
\csc(\theta) &= x \\
\frac{d}{dx}\bigg[\csc(\theta)\bigg]&=1 \\
-\csc(\theta)\cot(\theta)\frac{d\theta}{dx}&=1 \\
\frac{d\theta}{dx}&=-\frac{1}{\csc(\theta)\cot(\theta)} \\
&=-\frac{1}{\csc(\theta)\cos(\theta)\csc(\theta)} \\
&=-\frac{1}{\csc^2(\theta)\cos(\theta)} \\
&=-\frac{1}{x^2\cos(\theta)} \\
&=-\frac{1}{x^2\sqrt{1 - \frac{1}{\csc^2(\theta)}}} \\
&=-\frac{1}{x^2\sqrt{1 - \frac{1}{x^2}}} \\
&=-\frac{1}{x^2\sqrt{1 - x^{-2}}} \\
\end{align}
$$

## arcsec

$$
\begin{align}
\cos^2(\theta) + \sin^2(\theta) &= 1 \\
\sin^2(\theta) &= 1 - \cos^2(\theta) \\
\sin^2(\theta) &= 1 - \frac{1}{\sec^2(\theta)} \\
\sin(\theta) &= \sqrt{1 - \frac{1}{\sec^2(\theta)}} \\
\end{align}
$$

manipulate trig

$$
\begin{align}
\theta &= \sec^{-1}(x) \\
\sec(\theta) &= x \\
\frac{d}{dx}\bigg[\sec(\theta)\bigg]&=1 \\
\sec(\theta)\tan(\theta)\frac{d\theta}{dx}&=1 \\
\frac{d\theta}{dx}&=\frac{1}{\sec(\theta)\tan(\theta)} \\
&=\frac{1}{\sec(\theta)\sin(\theta)\sec(\theta)} \\
&=\frac{1}{\sec^2(\theta)\sin(\theta)} \\
&=\frac{1}{x^2\sin(\theta)} \\
&=\frac{1}{x^2\sqrt{1 - \frac{1}{\sec^2(\theta)}}} \\
&=\frac{1}{x^2\sqrt{1 - \frac{1}{x^2}}} \\
&=\frac{1}{x^2\sqrt{1 - x^{-2}}} \\
\end{align}
$$

## arccot

$$
\begin{align}
\theta &= \cot^{-1}(x) \\
\cot(\theta) &= x \\
\frac{d}{dx}\bigg[\cot(\theta)\bigg]&=1 \\
-\csc^2(\theta)\frac{d\theta}{dx}&=1 \\
\frac{d\theta}{dx}&=-\frac{1}{\csc^2(\theta)} \\
&=-\frac{1}{1+\cot^2(\theta)} \\
&=-\frac{1}{1+x^2} \\
\end{align}
$$