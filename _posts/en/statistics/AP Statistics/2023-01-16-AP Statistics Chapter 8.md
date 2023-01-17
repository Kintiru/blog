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

`Point Estimator` : a statistic that provides an estimate of a population parameter.

`Point Estimate` : value of `Point Estimator` from a sample.

`Confidence Interval` : interval of plausible values for a parameter based on sample data.

`Confidence Level` : success rate of the method used to calculate the confidence interval. Usually expressed in %.

`Margin of Error` : How much the true parameter can vary from `Point Estimate`.

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

### Interpretaton of Confidence Interval

We are `C%` of confident that the interval from `a` to `b` would capture `parameter`

> Parameter should be in context
> 
> For example: the mean number of shoes students in the United States own
{: .prompt-info}

### Interpretaton of Confidence Level

In many random samples, about `C%` of confidence intervals would capture `parameter`

> Parameter should be in context here too
{: .prompt-info}

### Margin of Error

Margin of Error is related to standard deviation.

 - Within 1 standard deviation: 67%
 - Within 2 standard deviation: 95%
 - Within 3 standard deviation: 99.7%
  
It is because in sampling distribution, 67% of random samples would be in 1 standard devation, so 67% of random samples would capture parameter in their confidence interval.

Allowing more errors would have higher confidence interval.

For example, if we have confidence interval
$$[-\infty, \infty]$$ 
Then it would have 100% confidence level.

But, this won't explain anything.

So we have to trade off between `precision` and `confidence`.

# 8.2 Population Proportion Estimation

Will be added later

# 8.3 Proportion Difference Estimation

Will be added later

[^1]: https://en.wikipedia.org/wiki/Critical_value#Statistics