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

## Two Way Table

> Example Two Way Table
{: .prompt-info} 

|        | Company A | Company B | totals |
|--------|-----------|-----------|--------|
| Banana | 40        | 60        | 100    |
| Apple  | 40        | 60        | 100    |
| totals | 80        | 120       | 200    |

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
                label: "example dataset",
                data: [Math.random() * 100, Math.random() * 100, Math.random() * 100, Math.random() * 100],
                borderColor: "rgba(255, 99, 132, 1)",
                borderWidth: 2,
                borderRadius: 10,
                backgroundColor: "rgba(255, 99, 132, 0.5)",
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
                    text: 'Example Bar Graph',
                },
            },
        },
    });
</script>

### Side by Side Bar Graph

<div><canvas id="sideBySideBarGraphExample"></canvas></div>

<script>
    new Chart(document.getElementById('sideBySideBarGraphExample'),{
        type: 'bar',
        data: {
            labels: ['A', 'B', 'C', 'D'],
            datasets: [
                {
                    label: "example dataset 1",
                    data: [Math.random() * 100, Math.random() * 100, Math.random() * 100, Math.random() * 100],
                    borderColor: "rgba(255, 99, 132, 1)",
                    borderWidth: 2,
                    borderRadius: 10,
                    backgroundColor: "rgba(255, 99, 132, 0.5)",
                },
                {
                    label: "example dataset 2",
                    data: [Math.random() * 100, Math.random() * 100, Math.random() * 100, Math.random() * 100],
                    borderColor: "rgba(54, 162, 235, 1)",
                    borderWidth: 2,
                    borderRadius: 10,
                    backgroundColor: "rgba(54, 162, 235, 0.5)",
                }
            ],
        },
        options: {
            responsive: true,
            plugins: {
                legend: {
                    position: 'top',
                },
                title: {
                    display: true,
                    text: 'Example Side by Side Bar Graph',
                },
            },
        },
    });
</script>
### Segmented Bar Graph

# Quantative Data Analysis

## Dotplots

## Histogram

## Shape

### Unimodal

### Multimodal (2 or more peaks)

## Stemplots

