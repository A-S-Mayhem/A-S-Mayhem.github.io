---
title: 'An Introduction to Analysis of Variance (ANOVA)'
date: 2023-01-13
permalink: /posts/2023/01/what-is-anova/
tags:
  - statistics
  - analysis of variance
  - categorical variables
---

This post gives a brief introduction to the basics of analysis of variance and how it works. An overview of the oneway analysis of variance model is provided along with additional details regarding sums of squares. A simple example of analysis of variance can be found [here](https://trgrimm.github.io/posts/2023/01/oneway-anova-example/).

# What is Analysis of Variance (ANOVA)?

Analysis of variance (ANOVA) is a popular statistical method developed
by Ronald Fisher. ANOVA was initially used by Fisher to understand
variability in crop yield, but its applications are not limited to crop
science. In fact, ANOVA is easily applied to data from any field
provided certain assumptions (discussed below) are satisfied.

Generally speaking, ANOVA is used to determine if there are meaningful
differences in the means of a response variable across various
“treatment” groups. At its core, ANOVA is done by determining if the
variability among various groups is unlikely to occur solely because of
random chance.

## Oneway ANOVA Model and Assumptions

Let's consider the simplest ANOVA model: the "oneway" ANOVA. In oneway ANOVA, we have a single "treatment" with $i = 1,\ldots,k$ levels. Each treatment has $n_i$ subjects, and each subject is assigned to exactly one treatment group. The notation for the model is included below.

$$
y_{ij} = \theta_i + \epsilon_{ij}, \qquad i = 1,\ldots, k, \textrm{ and } j = 1,\ldots,n_i,
$$

where $y_{ij}$ denotes the observed response for subject $j$ within treatment $i$, $\theta_i$ is the mean of the response for treatment $i$, and $\epsilon_{ij}$ is random error for each subject and treatment.

In order to make valid inferences using ANOVA, there are some assumptions regarding the data that must be satisfied. These assumptions are:

* Independence - the observations are independent of one another
* Normality - the residuals are normally distributed
* Equal variance - the variance is (approximately) the same across treatment groups (also called homoscedasticity)

Once we've checked these assumptions and have determined that they are not violated, we can safely draw conclusions using ANOVA results. If any of these assumptions is violated, we must either make adjustments before using ANOVA or we must use a different method altogether.

A basic example and walkthrough of a oneway ANOVA analysis can be found [here](https://trgrimm.github.io/posts/2023/01/oneway-anova-example/). For the interested reader, additional technical details about how ANOVA works are included below.

<br>
<br>
<br>
<br>

# Additional Technical Details

## What are Sums of Squares?

ANOVA works by determining if variability in the response variable $y$ is due to significant differences between treatment groups or random chance. We can measure variability in the response variable by computing the *sum of squares*. Simply put, the sum of squares is a measure of distance between each observed response $y_{ij}$ and the overall mean of all observations $\bar{\bar{y}}$.

Consider the overall (total) sum of squares $\textrm{SST} = \sum_{i=1}^{k}\sum_{j=1}^{n_i}(y_{ij}-\bar{\bar{y}})^2.$

It can be shown that the total sum of squares (SST) can be partitioned
as follows:

$$
\begin{align*}
\textrm{SST} = \sum_{i=1}^{k}\sum_{j=1}^{n_i}(y_{ij}-\bar{\bar{y}})^2 = \sum_{i=1}^{k}n_i(\bar{y}_{i.}-\bar{\bar{y}})^2 + \sum_{i=1}^{k}\sum_{j=1}^{n_i}(y_{ij}-\bar{y}_{i.})^2,
\end{align*}
$$

where we define the sums of squares on the right side of the equality as
the sum of squares between groups (SSB), and sum of squares within
groups (SSW), respectively. Specifically, we have

$$
\begin{align*}
\textrm{SSB} = \sum_{i=1}^{k}n_i(\bar{y}_{i.}-\bar{\bar{y}})^2 \quad \textrm{and} \quad \textrm{SSW} = \sum_{i=1}^{n}(y_{ij}-\bar{y}_{i.})^2,
\end{align*}
$$

where $\bar{y}_{i.}$ denotes the mean of the response variable ($y$) for all observations corresponding to group $i$.

So, we have $\textrm{SST} = \textrm{SSB} + \textrm{SSW}$.

Each of the sums of squares can be viewed in the following way:

* SST is a measure of the total variability from each individual response to the overall mean of the responses (across all groups).
* SSB is a measure of variability in the average response from group to group ("between" groups).
* SSW is a measure of the variability for each response within its respective group (variability left over after adjusting for group).

## How are Sums of Squares Used?

The classical ANOVA hypothesis is that all $\theta_i$ are equal. In other words, the treatments are all the same.

Consider MSB, the mean of the between sum of squares (computed as $\text{SSB}/(k-1)$), and MSW, the mean of the within sum of squares (computed as $\text{SSW}/(n-k)$. Due to assumptions described above, it can be shown that the ratio MSB/MSW is distributed as a $\chi^2$ random variable with $k-1$ and $n-k$ degrees of freedom, where $n$ refers to the overall sample size.

So, we have

$$
\frac{\text{MSB}}{\text{MSW}} \sim \chi^2_{k-1,n-k},
$$

which allows us to test the classical ANOVA hypothesis. See [this](https://en.wikipedia.org/wiki/Statistical_hypothesis_testing) for more information about hypothesis testing.
