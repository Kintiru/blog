---
title: 'AP Statistics Chapter 12: Chi Squared and Inferences for Slope'
date: 2023-03-28 20:00:00 +0900
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

<script src="https://cdn.jsdelivr.net/npm/chart.js@4.1.2/dist/chart.umd.js"></script>

# Prerequisite

[AP Statistics Chapter 9 : Hypothesis Testing For Proportions](/english/statistics/2023/01/31/AP-Statistics-Chapter-9/)


# 12.1 Chi Squared Test and Distribution 

## Chi Square

Chi squared is used to test categorical variables using their expected outcomes.

The expected outcome is as below.

$$
\tag{1} E(X_i)  = \sum_{i}np_i 
$$

where
 * $n$ is number of samples
 * $p_i$ is probability of getting outcome of $i$th category

and Chi Squared test statistics is as follows

$$
\tag{2} \chi^2 = \sum _i \frac{(O_i-E(X_i))^2}{E(X)}
$$

where
 * $O_i$ is actual outcome of $i$th category
 * $E(X_i)$ is expected outcome of $i$th category (see equation $(1)$)
  
## Chi Square Distribution

$n$ categorical variables follows chi squared distribution of $n-1$ degrees of freedom

This, we can get P-value of chi square test statistics using $\chi$cdf in calculator.

Chi square is always greater or equal to 0 because it is analysis of variances.

## Chi Square Test

We can carry out the test as we did in [Ch.9](/english/statistics/2023/01/31/AP-Statistics-Chapter-9/) and [Ch.11](/english/statistics/2023/03/08/AP-Statistics-Chapter-11/)

### Conditions

 1. Random (10% condition)
 2. Large Counts: Every $E(X_i)$ is greater than 5

# 12.3 Inference for Slope

## Population Regression Line

Population regression line is regression line for the entire population.

The Least Square Regression line for the population will be

$$
\mu_y = \alpha + \beta x
$$

This assumes that the $y$ variable will linearly depend on $x$

## Sample Regression Line

If we sample some portion of the population, the slope $\beta$ of regression line will also have sampling distribution. 

The Least Square Regression line for a sample will be

$$
\hat y = a + bx
$$

## Sampling distribution of Slope

Since we are randomly selecting sample from the population, the regression line will also vary depending on the sample we got.

This is similar to sampling distribution for means. 

 1. Center : Mean if sampling distribution of slopes is unbiased estimator for population slope. 

    $$\mu_b = \beta$$
 2. Variability :
    $$
    \sigma_b = \frac{\sigma}{\sigma_x \sqrt{n}}
    $$
    Where $\sigma$ is standard deviation of residuals and $\sigma_x$ is standard deviation of $x$
 3. Shape : Approximately Normal when conditions are met

Since we dont know the parameter, we estimate the variability with standard error

$$
SE_b = \frac{s}{s_x \sqrt{n-1}}
$$

## Conditions for Regression Inference

 1. Linear : y and x should have linear relationship
 2. Independent : 10% conditions, independent observations or treatments
 3. Normal : y should vary apporoximately normal for any x value in range
 4. Equal SD : $\sigma$ (residuals) are equal throughout the range of x <br>
   This also means that $\sigma_y$ is equal for any given x in range
 5. Random : random sample or random assignment


## Confidence Interval
Since it is similar to sampling distribution for means, we can think of constructing confidence interval for slopes too.

The t distribution follows n-2 degrees of freedom because we lost one degrees of freedom when constructing the regression line.

$$
b \pm t^*_{df=n-2} \cdot SE_b 
$$

## T-test
we can also perform t test with slopes.

The t distribution here also follows n-2 degrees of freedom.

$$
t = \frac{b - \beta_0}{SE_b}
$$