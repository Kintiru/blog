---
title: 'AP Statistics Chapter 11: Hypoethesis Testing for Means'
date: 2023-03-08 13:00:00 +0900
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

# Prerequisite

[AP Statistics Chapter 9 : Hypothesis Testing For Proportions](/english/statistics/2023/01/31/AP-Statistics-Chapter-9/)

# 11.1 Significance Test for Mean

Significance test for mean is testing the claim or the hypothesis about population parameter which is mean $\mu$.


## Standardized T Test

`Standardized Test Statistic` : How far a sample statistic is from the parameter in standardized unit, assuming the null hypothesis $H_0$ is true

$$
\begin{gather}
T = \frac{\bar{x}- \mu_0}{\displaystyle\frac{s_x}{\sqrt{n}}}
\end{gather}
$$


## Conditions for test

|              | Observational Study           | Experiment                 |
|--------------|-------------------------------|----------------------------|
| Random       | Random Sample                 | Random Assignment          |
| Independence | 10% Condition ($n\leq0.1N$)   | Independent Treatments     |
| Normality    | Large Counts ($n \geq 30$)    | Large Counts ($n \geq 30$) |


## Paired Data

`Paired Data`: two different data (values) of the same quantative variable for each individual or each pair of similar individuals.

Instead of doing two sample t test, we can just use the differences from the first place to reduce the work.

### Conditions

|              | Observational Study                  | Experiment                        |
|--------------|--------------------------------------|-----------------------------------|
| Random       | Random Sample                        | Random Assignment                 |
| Independence | 10% Condition ($n_{diff}\leq0.1N$)   | Independent Treatments            |
| Normality    | Large Counts ($n_{diff} \geq 30$)    | Large Counts ($n_{diff} \geq 30$) |


# 11.2 Difference in Mean Test

## Hypothesis

Since we are testing if there is difference in means,

$H_0$ : $\mu_1 - \mu_2= 0$

$H_a$ : $\mu_1 - \mu_2 > \text{or} < \text{or} \neq  0$

## Conditions

|              | Observational Study                               | Experiment                                        |
|--------------|---------------------------------------------------|---------------------------------------------------|
| Random       | Random Sample                                     | Random Assignment                                 |
| Independence | 10% Condition<br>($n<0.1N_1$ and $n_2<0.1N_2$)    | Independent Treatments                            |
| Normality    | Large Counts<br>($n_1 \geq 30$ and $n_2 \geq 30$) | Large Counts<br>($n_1 \geq 30$ and $n_2 \geq 30$) |

> In AP, you can plot the graph and see if there is any severe outliers or skew
>
> If not, you can say it is Normal. However, it is not safe in real world.
{: .prompt-warning }

## Standardized T Test

$$
\begin{gather}
T= \frac{\bar{x}_1 - \bar{x}_2 - (\mu_1-\mu_2)}{\displaystyle\sqrt{\frac{s^2_1}{n_1} + \frac{s^2_2}{n_2}}}
\end{gather}
$$


# Four step process of significance test

 1. State
    - State Hypothesis and significance level
    - Identify parameter
 2. Plan
    - Check conditions
 3. Do
    - Calculate
 4. Conclude
    - Make conclusion with correct inference and context
