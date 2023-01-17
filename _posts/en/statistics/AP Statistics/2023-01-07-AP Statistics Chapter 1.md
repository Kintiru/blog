---
title: 'AP Statistics Chapter 1: Data Analysis'
date: 2023-01-07 16:00:00 +0900
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

<!--- 
Include script per post to prevent version break and better per post management
-->
<script src="https://cdn.jsdelivr.net/npm/chart.js@4.1.2/dist/chart.umd.js"></script>

- [Vocabularies](#vocabularies)
- [1.1 Categorical Data Analysis](#11-categorical-data-analysis)
  - [Pie Chart](#pie-chart)
  - [Two Way Table](#two-way-table)
  - [Bar Graph](#bar-graph)
    - [Side by Side Bar Graph](#side-by-side-bar-graph)
    - [Segmented Bar Graph](#segmented-bar-graph)
- [Quantative Data Analysis](#quantative-data-analysis)
  - [Dotplots](#dotplots)
  - [Histogram](#histogram)
  - [Shape](#shape)
    - [Unimodal](#unimodal)
    - [Multimodal (2 or more peaks)](#multimodal-2-or-more-peaks)
  - [Stemplots](#stemplots)
  - [Boxplot](#boxplot)
- [Description of Quantitative Data](#description-of-quantitative-data)
  - [Center](#center)
    - [Mean](#mean)
    - [Median](#median)
  - [Shape](#shape-1)
  - [Variability](#variability)
    - [Range](#range)
    - [Standard Deviation](#standard-deviation)
    - [IQR](#iqr)
    - [Variance](#variance)
  - [Outliers](#outliers)

---

# Vocabularies

`Quantitative Data` : Data that represents amounts

`Categorical Data` : Data that represents groups (classifications)

`Frequency` : Actual count of data

`Relative Frequency` : Percentage of data

`Association` : Relativeness of two variables

# 1.1 Categorical Data Analysis

Since I think visual explains all of the charts, I will barely add explations in text for charts.

## Pie Chart

<div style="width:70%;"><canvas id="pieChartExample"></canvas></div>

<script>
    const pieChartExample = new Chart(document.getElementById('pieChartExample'),{
        type: 'pie',
        data: {
            labels: ['A', 'B', 'C', 'D'],
            datasets: [{
                label: "example dataset",
                data: [Math.random() * 100, Math.random() * 100, Math.random() * 100, Math.random() * 100],
                radius: '90%',
                borderColor: "rgba(0, 0, 0, 0)",
                borderWidth: 2,
                borderRadius: 7,
                backgroundColor: ['rgb(255, 99, 132)', 'rgb(255, 159, 64)', 'rgb(255, 205, 86)', 'rgb(54, 162, 235)'],
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
                    text: 'Example Pie Chart',
                },
            },
        },
    });
</script>

## Two Way Table

**Example Two Way Table**

|        | Company A | Company B | totals |
|--------|-----------|-----------|--------|
| Banana | 40        | 60        | 100    |
| Apple  | 40        | 60        | 100    |
| totals | 80        | 120       | 200    |


**Two Way Table in general**

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
    const barGraphExample = new Chart(document.getElementById('barGraphExample'),{
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
    const sideBySideBarGraphExample = new Chart(document.getElementById('sideBySideBarGraphExample'),{
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

<div><canvas id="segmentedBarGraphExample"></canvas></div>

<script>
    const segmentedBarGraphExample = new Chart(document.getElementById('segmentedBarGraphExample'),{
        type: 'bar',
        data: {
            labels: ['A', 'B', 'C', 'D'],
            datasets: [
                {
                    label: "example dataset 1",
                    data: [Math.random() * 100, Math.random() * 100, Math.random() * 100, Math.random() * 100],
                    borderColor: "rgba(255, 99, 132, 1)",
                    borderWidth: 0,
                    borderRadius: 5,
                    backgroundColor: "rgba(255, 99, 132, 0.5)",
                    stack: 'Stack 0',
                },
                {
                    label: "example dataset 2",
                    data: [Math.random() * 100, Math.random() * 100, Math.random() * 100, Math.random() * 100],
                    borderColor: "rgba(54, 162, 235, 1)",
                    borderWidth: 0,
                    borderRadius: 5,
                    backgroundColor: "rgba(54, 162, 235, 0.5)",
                    stack: 'Stack 0',
                }
            ],
        },
        options: {
            responsive: true,
            interaction: {
                intersect: false,
            },
            plugins: {
                legend: {
                    position: 'top',
                },
                title: {
                    display: true,
                    text: 'Example Side by Side Bar Graph',
                },
            },
            scales: {
                x: {
                    stacked: true,
                },
                y: {
                    stacked: true,
                },
            },
        },
    });
</script>

# Quantative Data Analysis

## Dotplots

## Histogram

## Shape

### Unimodal

### Multimodal (2 or more peaks)

## Stemplots

## Boxplot

Before going into boxplot, I recommend reading [Description of Quantitative Data](#description-of-quantitative-data) first.

# Description of Quantitative Data

## Center

### Mean

### Median

## Shape

## Variability

### Range

### Standard Deviation

### IQR

### Variance

## Outliers