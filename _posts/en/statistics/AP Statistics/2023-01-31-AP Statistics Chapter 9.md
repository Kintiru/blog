---
title: 'AP Statistics Chapter 9: Testing Claims About Proportions'
date: 2023-01-31 13:00:00 +0900
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

# 9.1 Significance Test

Significance test is testing the claim or the hypothesis about population parameter such as proportion $p$ or mean $\mu$.

## Hypotheses

`Null Hypothesis` $(H_0)$ : Original claim; claim we are finding evidence **against**

> Example : A claim that a population parameter is certain value
{: .prompt-info} 

`Alternative Hypothesis` $(H_a)$ : Claim that original claim is wrong; A claim we are finding evidence **for**

> Example : A claim that a  (less or greater) than certain value
{: .prompt-info} 

 * One sided alternative hypothesis : Population parameter is less or greater null value (specifially less or greater; directional)



 * Two sided alternative hypothesis : Population parameter is not the null value (no matter greater or less)

`P-value` : probability of getting evidence for the alternative hypothesis $H_a$

`Significance Level` $\alpha$ : boundary value for deciding if observed result happened merely by chance or not

 * P-value $< \alpha \to$ reject $H_0$, Convincing evidence for $H_a$
 * P-value $> \alpha \to$ No convincing evidence for $H_a$
 * 0.05 (5%) is often used for `Significance Level` $\alpha$

## Interpretation of `P-value`

Assuming $H_0$ is true, There is `P-value`(actual value) probability of getting sample `statistic` (mean, proportion, etc) of `sample statistic`(actual value) or greater/less.

Example: Assuming that the true mean `in context` is 120, There is **0.1** probability of getting sample **mean** of **100** or **less**. 

## Errors

`Type I Error` : Rejected H<sub>0</sub> even though H<sub>0</sub> is true.

`Type II Error` : Fail to reject H<sub>0</sub> when H<sub>0</sub> is not ture (= when H<sub>a</sub> is true).

Requiring more evidence or having lower `significance level` means that it is less likely to find convincing evidence, which means it is more likely to have `Type II Error`.

The opposite will increase the chance of having `Type I Error`

# 9.2 Population Porportion Test

## Conditions

 1. Random - Random Sample
 2. Independence (10% Condition) - $n \leq 0.1N$
 3. Normality (Laege Counts) - $np \geq 10, \space n(1-p) \geq 10$

## Standardized Test

`Standardized Test Statistic` : How far a sample statistic is from the parameter in standardized unit, assuming the null hypothesis $H_0$ is true

$$
\begin{gather}
\text{standardized test statistic} = \frac{\text{statistic} - \text{parameter}}{\text{standard deviation/error of statistic}} \\
= \frac{\hat{p}-p_0}{\sqrt{\frac{p_0(1-p_0)}{n}}}
\end{gather}
$$

## Four step process of significance test

 1. State
 2. Plan
 3. Do
 4. Conclude

## Power

`Power` : Probability that the test will find convincing evidence for alternative hypothesis $H_a$ when alternative value for the parameter is true

In other words, the probability of finding convincing evidence assuming the true parameter is some other value than null value.

Power will be larger when
 * Sample size n is larger (less varibility)
 * Significance Level is larger (more chance to find convincing evidence)
 * The null and alternative parameter values are more farther apart

### Example: 
 - Let $H_0 : \mu = 1$
 - $H_a : \mu > 1$

the power will be the probability of finding convincing evidence for $H_a$ assuming the true mean is 2.

### Relationship with Type II Error

$$
\begin{gather}
\text{Power} = 1 - P(\text{Type II Error}) \\
\text{or} \\
P(\text{Type II Error}) = 1- \text{Power}
\end{gather}
$$


# 9.3 Population Proportion Difference Test

Will be added later