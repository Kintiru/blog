---
title: 'Basic Circuits: Volts, Amphere, and Resistance'
date: -- ::00 +0900
author: kintiru
categories: []   # [TOP_CATEGORIE, SUB_CATEGORIE]
tags: []     # TAG names should always be lowercase
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

# Basic units

$$
V=IR \\
V = \text{Energy/Coulomb} = J/C \\
I \text{ (a.k.a Amphere)} = \text{Coulomb/sec} = C/s \\
R = \Omega = \text{Voltage/Amphere} = \frac{J/C}{C/s} = J \cdot s/C^2
$$

Since Voltage is Energy per coulomb, it is similar to pressure to some extent. 

# Watt

Watt is Energy per time. $W = E/t$

$$
V \cdot I = \frac{J}{\cancel C} \cdot \frac{\cancel C}{s} = J/s \\
$$

Or using $V=IR$,

$$
\because I = V/R \\
\implies V \cdot I = V \cdot \frac{V}{R} = V^2/R
$$