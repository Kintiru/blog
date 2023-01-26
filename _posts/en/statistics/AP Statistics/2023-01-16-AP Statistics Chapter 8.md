---
title: 'AP Statistics Chapter 8: Proportion Estimation with Confidence'
date: 2023-01-16 19:50:00 +0900
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

# 8.1 Confidence Interval

## Vocabulary

`Point Estimator` : a statistic that provides an estimate of a population parameter. (or the formula)

`Point Estimate` : value of `Point Estimator` from a sample. (or the value of the formula)

`Confidence Interval` : interval of plausible values for a parameter based on sample data.

`Confidence Level` : success rate of the method used to calculate the confidence interval. Usually expressed in `C%`.

> Confidence Level is not a probability when interpreting a single Confidence Interval
{: .prompt-danger}

`Margin of Error` : How much the true parameter can vary from `Point Estimate`.

> MOE accounts for sampling variability, not bias
{: .prompt-danger}

![Margin of Error Diagram](/assets/img/2023/01/margin-of-error-diagram.svg)
_Margin of Error Diagram_

`Critical Value` : Multiplier of standard deviation to define margin of error

$$
\begin{gather}
\text{point estimate } \pm \text{ margin of error} \\
\text{point estimate } \pm \text{ (critical value)} \cdot \text{(standard deviation of statistic)} \\
\mu_x \pm 2 \sigma_x
\end{gather}
$$

> This is AP definition of Critical Value
>
> The real definition is different: the boundaries of the acceptance region of the test. [^1]
{: .prompt-warning}

`Standard Error` : Variability across samples of a population (sampling distribution).

> `Standard Error` is used when population parameter is unknown.
>
> `Standard Deviation` describes variability within a sample, while `Standard Error` describes variability across samples.
{: .prompt-info}

## Interpretaton of Confidence Interval

We are `C%` of confident that the interval from `a` to `b` would capture `parameter in context`

> Parameter should be in context
> 
> For example: the mean number of shoes students in the United States own
{: .prompt-info}

Also, we cannot say that there is convincing evidence if the value is in the interval.

For example, there is no convincing evidence that the population proportion is over 0.5 when we have `[0.49,0.59]` Confidence Interval of proportion.

## Interpretaton of Confidence Level

In many random samples, about `C%` of confidence intervals would capture `parameter`

> Parameter should be in context here too
{: .prompt-info}

## Margin of Error

Margin of Error is related to standard deviation.

 - Within 1 standard deviation: 68%
 - Within 2 standard deviation: 95%
 - Within 3 standard deviation: 99.7%
  
It is because in sampling distribution, 68% of random samples would be in 1 standard devation, so 68% of random samples would capture parameter in their confidence interval.

Allowing more errors would have higher confidence interval.

For example, if we have confidence interval $[-\infty, \infty]$, then it would have 100% confidence level.

But, this won't explain anything.

So we have to trade off between `precision` and `confidence`.

### Reudicing Margin of Error

 1. Reduce sampling variability
    - Increase sample size
    - Better study design (startifying, blocking, etc)
 2. Reduce confidence level

## Conditions for Confidence Interval

 1. Random
 2. Normality
 3. Independence (`10% condition`)

### What if it is violated?

 1. Random - No other way than doing the study all over again
 2. Normality - affects the `Confidence Level` when we refer to emperical rule
 3. Independence - lose precision, so multiply `Finite Population Correction Factor` to the standard deviation.

# 8.2 Population Proportion Estimation

## Confidence Interval for p

### Equation

$$
\begin{align}
\hat p \pm z^* \sqrt{\frac{\hat p(1 - \hat p)}{n}}
\end{align}
$$

where z* is \|±z\|

Table b provides z* values for certain confidence intervals.

### Conditions for estimating p

 1. Random
 2. Independence (10% Condition)
 3. Normality (Large Counts)

When independence is met, the `standard error` is

$$
\text{SE}_p = \sqrt{\frac{\hat p(1 - \hat p)}{n}}
$$


### Calculating z-score values from given Confidence Level

$$
\begin{gather}
C \text{ - Confidence Level} \\
z^* = \text{invnorm}\left(1-\frac{C}{2}\right)
\end{gather}
$$

`Confidence Interval` can be calculate using the z* and the `standard error`

### Steps of solving AP Questions

 1. State - State what are you trying to do
 2. Plan - Check [condtitions](#conditions-for-estimating-p)
 3. Do - Perform calculations
 4. Conclude - Interpret

# 8.3 Proportion Difference Estimation

## Condtitions for inference of difference

### Observational Studies

 1. Random - Random Sampling
 2. Independence - 10% Condition, and the populations are independent of each other

    $$
    \begin{gather}
    n_1 \leq 0.1 \cdot N_1 \,, \, n_2 \leq 0.1 \cdot N_2 \\
    \implies \text{SE}_{\hat p_1 - \hat p_2} = \sqrt{\frac{\hat p_1(1 - \hat p_1)}{n_1} + \frac{\hat p_2(1 - \hat p_2)}{n_2}}
    \end{gather}
    $$

 3. Shape - Large Counts (for normality)

$$
\begin{gather}
n_1 \hat p_1 \geq 10 \,, \, n_2 \hat p_2 \geq 10 \\
n_1(1- \hat p_1) \geq 10 \,, \, n_2 (1- \hat p_2) \geq 10 \\
\implies \hat p_1 - \hat p_2 \sim N
\end{gather}
$$

### Experiments

 1. Random - Random Assignment (a.k.a. Random Allocation)
 2. Indpendence - 10% condition **ONLY IF** random sampling is used
 3. Shape - Large Counts (for normality)
 
$$
\begin{gather}
n_1 \hat p_1 \geq 10 \,, \, n_2 \hat p_2 \geq 10 \\
n_1(1- \hat p_1) \geq 10 \,, \, n_2 (1- \hat p_2) \geq 10 \\
\implies \hat p_1 - \hat p_2 \sim N
\end{gather}
$$


---

[^1]: [https://en.wikipedia.org/wiki/Critical_value#Statistics](https://en.wikipedia.org/wiki/Critical_value#Statistics)