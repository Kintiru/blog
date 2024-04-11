---
title: 'AP Statistics Chapter 7: Sampling Proportions'
date: -- ::00 +0900
author: kintiru
categories: [English, Statistics]   # [TOP_CATEGORIE, SUB_CATEGORIE]
tags: [English, Statistics, AP Statistics, Math]     # TAG names should always be lowercase
math: true
mermaid: true
#img_path: 
#image: #preview image
    #path:
    #alt:
    #lqpq:
#pin: true
---

# 7.1 Sampling Distribution

Statistic - a number that describes some characteristic of a sample

Parameter - a number that describes some characteristic of a population

Sampling variability - different random samples of the same size from the same population produce different statistics

Sampling distribution - distribution of values taken by the statistic in all possible samples of the same size from the same population

Approximate sampling distribution - 

Unbiased estimator 
-  a statistic used to estimate a parameter (if mean of its sampling distribution = parameter)

Variability
- Less if $n$ is larger for each $\overline{x}$ as long as it meets 10% condition

# 7.2 Sample Proportion

Sampling Distribution of the Sample Proportion p ̂  - describes the distribution of values taken by the sample proportion p ̂  in all possible samples of the same size from the same population
* Shape
  * $p$ is close to $0$ - skewed to the right
  * $p$ is close to $1$ - skewed to the left
  * $p$ is close to $0.5$ - more normal (symmetry)
  * Approximately Normal when np≥10 and $n(1−p)≥10$

Center
$$
\mu_{\hat{p}} = p = \frac{1}{n}\mu_X = \frac{1}{n}np
.$$

Variability

As long as 10% condition is satisfied ($n<0.1N$),
$$
\sigma_{\hat{p}} = \sqrt{\frac{p(1-p)}{n}} = \frac{1}{n}\sigma_X = \frac{1}{n}\sqrt{np(1-p)}
.$$
Otherwise, multiply Finite Correction Factor
$$
\sqrt{\frac{N-n}{N-1}}d
.$$

# 7.3 Sample mean