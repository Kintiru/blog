---
title: 'AP Statistics Chapter 10: Mean Estimation with Confidence '
date: 2023-02-22 22:00:00 +0900
author: kintiru
categories: [English, Statistics]   # [TOP_CATEGORIE, SUB_CATEGORIE]
tags: [English, Statistics, AP Statistics, Math]     # TAG names 
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

# 10.1 Population Mean Estimation

## Confidence interval for $\mu$

$$
\begin{gather}
\text{point estimate } \pm \text{ margin of error} \\
= \bar x \pm z^* \frac{\sigma}{\sqrt{n}} \\
= \bar x \pm t^* \frac{s_x}{\sqrt{n}}
\end{gather}
$$

## t distribution

t distribution is used because parameter is unknown.

Therefore, we have to use sample standard deviation which is an estimation for the parameter.

Since estimations have uncertainties, t distriution has larger tails than smaller peak than normal distribution but it becomes closer to normal distribution as `degrees of freedom` increases. 

Corresponding t value of confidence level can be found in Table B. 

In one variable statistics, where degrees of freedom is $v = n-1$ .

Therefore,

$$
\begin{gather}
t= \frac{\text{error of point estimate }}{ \text{ standard error of statistic}} \\
= \frac{\bar X_i - \mu}{s_{\bar x - \mu}}\\
= \frac{\bar X_i - \mu}{\displaystyle\sqrt{\text{Var}(\bar X) + \text{Var}(\mu)}} \\
= \frac{\bar X_i - \mu}{\displaystyle\sqrt{s_x^2/n + 0}} \\
= \frac{\bar X_i - \mu}{s_x/\sqrt{n}}
\end{gather}
$$

Here, 
 * $\bar X_i$ is a random sample with size of $n$. $\bar X_i$ is used to indicate that it is one of the samples from sampling distribution of the mean.
 * $s_x$ is divided by $\sqrt{n}$ because $s_{\bar x - \mu}$ is a **standard deviation of sampling distribution of the mean**.

> In calculator you can get t* value from
> 
> VARS > DISTR > invT(area, df)
{: .prompt-info}

## Conditions for t distribution

 1. Random: Random Sample or Random Assignment
 2. Independence: 10% Condition ($n < 0.1N$)
 3. Normal (Large Counts): Central Limit Theorem ($n \geq 30$)

# 10.2 Difference in Means Estimation

## Conditions for difference in means using t distribution

 1. Random: Random Sample or Random Assignment
 2. Independence: 10% Condition ($n_1 < 0.1N_1$ and $n_2 < 0.1N_2$)
 3. Normal (Large Counts): Central Limit Theorem ($n_1 \geq 30$ and $n_2 \geq 30$)

## Confidence interval for $\mu$

Here is a simple recap of confidence interval and an equation using t distribution.

$$
\begin{gather}
\text{point estimate } \pm \text{ margin of error} \\
= \bar x \pm t^* \sqrt{\frac{s_1^2}{n_1} + \frac{s_2^2}{n_2}}
\end{gather}
$$

## t-value

This is a t value for two variable statistics.

$$
\begin{gather}
t= \frac{\text{error of point estimate }}{ \text{ standard error of statistic}} \\
= \frac{\bar X_1 - \bar X_2}{s_{\bar x - \mu}}\\
= \frac{\bar X_1 - \bar X_2}{\displaystyle\sqrt{\text{Var}(\bar X_1) + \text{Var}(\bar X_2)}} \\
= \frac{\bar X_1 - \bar X_2}{\displaystyle\sqrt{\frac{s_1^2}{n_1} + \frac{s_2^2}{n_2}}}
\end{gather}
$$

Remember again that $\text{Var}(\bar X)$ is variance of **sampling distribution**.

## Degrees of freedom

Smallest degrees of freedom among samples can be used to overestimate the margin of error for convenience.

Or, Welch–Satterthwaite equation is used to approximate the degrees of freedom

$$
\begin{gather}
\text{df} =  \frac{ \left( \displaystyle\sum_{i \leq n} \frac{1}{v_i + 1} \text{Var}(\bar X_i)\right)^2 }{ \displaystyle\sum_{i \leq n} \frac{\text{Var}(\bar X_i)^2}{v_i(v_i + 1)^2} } \\
\end{gather}
$$

Since in AP Statistics, degrees of freedom is $n-1$, the equation can be re written as below

$$
\begin{gather}
\text{df} =  \frac{ \left( \displaystyle\sum_{i \leq k} \frac{s_i^2}{n_i} \right)^2 }{ \displaystyle\sum_{i \leq k} \left(\frac{1}{n_i - 1} \left( \frac{s_i^2}{n_i} \right)^2\right)} \\
\end{gather}
$$

> For two samples, we can use calculator
>
> STAT > TESTS > 2-SampTInt
{: .prompt-info}

## Paired Data

`Paired Data`: two different data (values) of the same quantative variable for each individual or each pair of similar individuals.

### Conditions

 1. Random: Random Sample or Random Assignment
 2. Independence: 10% Condition ($n_{A-B} < 0.1N_{A-B}$)
 3. Normal (Large Counts): Central Limit Theorem ($n_{A-B} \geq 30$)

### Confidence Interval

$$
\begin{gather}
\bar x_{A-B} \pm t^* \frac{s_{A-B}}{\sqrt {n_{A-B}}}
\end{gather}
$$