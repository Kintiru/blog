---
title: 'AP Statistics Chapter 1: Data Analysis'
date: 2023-01-07 16:00:00 +0900
author: kintiru
categories: [English, Statistics]   # [TOP_CATEGORIE, SUB_CATEGORIE]
tags: [English, Statistics, AP Statistics]     # TAG names should always be lowercase
math: true
mermaid: true
#img_path: 
#image: #preview image
    #path:
    #alt:
    #lqpq:
#pin: true
---

# Vocabularies

Quantitative Data : Data that represents amounts

Categorical Data : Data that represents groups (classifications)

Frequency : Actual count of data

Relative Frequency : Percentage of data

Association : Relativeness of two variables

# 1.1 Categorical Data Analysis

## Pie Chart

```mermaid
pie title Data
	"A" : 4
	"B" : 5
	"C" : 7
    "D" : 3
```

## Two way Table

|            | category A | category B | Totals |
|------------|------------|------------|--------|
| category 1 | J          | J          | M      |
| category 2 | J          | J          | M      |
| Totals     | M          | M          | Total  |

$$
\begin{aligned}
&J \text{ - Joint Frequency} \\
&M \text{ - Marginal Frequency}\\
&{\small \frac{J}{M}} \text{ - Conditional Frequency}
\end{aligned}
$$

## Bar Graph

<div><canvas id="barGraphExample"></canvas></div>

<script>
    new Chart(document.getElementById('barGraphExample'),{
        type: 'bar',
        data: {
            labels: ['A', 'B', 'C', 'D'],
            datasets: [{
                label: "test datasets",
                data: [10, 3, 30, 24],
                borderColor: "rgba(255, 201, 14, 1)",
                borderWidth: 2,
                backgroundColor: "rgba(255, 201, 14, 0.5)",
            }],
        },
        options: {
            responsive: true,
            plugins: {
                legend: {
                    position: 'top',
                },
                title: {
                    display: true,
                    text: 'Example Bar Graph'
                },
            },
        },
    });
</script>

### Side by Side Bar Graph

### Segmented Bar Graph

# Quantative Data Analysis

## Dotplots

## Histogram

## Shape

### Unimodal

### Multimodal (2 or more peaks)

## Stemplots

