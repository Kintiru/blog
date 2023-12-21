---
title: 'Preliminary of Linear Algebra'
date: 2023-08-16 16:00:00 +0900
author: kintiru
categories: [English, Linear Algebra]   # [TOP_CATEGORIE, SUB_CATEGORIE]
tags: [English, Linear Algebra, Math]     # TAG names should always be lowercase
math: true
mermaid: true
#img_path: 
#image: #preview image
    #path:
    #alt:
    #lqpq:
#pin: true
---

Here, I am going to go over set, real numbers, and complex numbers to prepare for Linear Algebra. It will be a quick review, some basic definitions and properties.

Definitions and properties will be important in linear algebra, since we have to know if certain operation is allowed. For instance, in Linear Algebra, division is not commonly defined, but it is also possible to create our own definition for division.

# Set
Set is a collection of objects (or elements).

Set is useful since we can clearly distinguish what is in the set or not in the set.

## Notation
For unordered set, which means a set that order does not matter, we use {} to denote a set.\
For example, $\{1,2,3\}$ is a set with 1, 2, and 3 as elements.

Other way to describe a set is using notation like following, A = { a | condition }\
For example, $S=\{s|s=2n, n\in\mathbb{N}\}$.\
Condition can be described in words too, $S=\{s| s \text{ is an even number}\}$

Here some common sets used frequently, 

| Sets |  Description |
|---|---|
| $\mathbb{N}$ | set of natrual numbers |
| $\mathbb{Z}$ | set of integers |
| $\mathbb{R}$ | set of real numbers |
| $\mathbb{C}$ | set of complex numbers |
| $\emptyset$ | empty set (set with no elements) |

And here are some common notations (assume $A$ and $B$ are sets)

| Notation |  Description |
|---|---|
  | $\in$ | element of ($1 \in \mathbb{N}$) |
  | $\cup$ | union, $A \cup B$ denotes a set of elements that are in $A$ or $B$ |
  | $\cap$ | intersection, $A \cap B$ denotes a set of elements that are in both $A$ and $B$ |
  | $\subset, \subseteq$ | subset, $A \subset B$ denotes all elements in A is in B. <br> $\subseteq$ implies $A$ and $B$ may be the same. (similar to $<, \leq$) |
  | $A=B$ | $A=B$ if $A \subseteq B$ and $B \subseteq A$ |

# Real Numbers



## Properties

Let $x, y, z$ be real numbers, which is $x, y, z \in \mathbb{R}$

| Property |  Description |
|---|---|
| Commutatitive Property of Addition | $x + y = y + x$ |
| Commutatitive Property of Mulitiplication | $x \times y = y \times x$ |
| Associative Property of Addition | $x + (y + z) = (x + y) + z$ |
| Associative Property of Multiplication | $x \times (y \times z) = (x \times y) \times z$ |
| Distributive Property | $x\times(y+z) = x \times y + x \times z$ |
| Additive Identity Property | $x + 0 = x$ |
| Multiplicative Identity Property | $x \times 1 = x$ |
| Additive Inverse Property | $x + (-x) = 0$ |
| Multiplicative Inverse Property | $x \times \frac{1}{x} = 1$ |
| Zero Property | $x \times 0 = 0$ |

These properties are important to prove basic properties in linear algebra.

