---
title: "Weekly Paper: Liberal Radicalism"
date: 2018-12-01T20:06:51+08:00
tags: [governance, economics]
series: ["Weekly Paper"]
draft: false
description: "Reading notes of paper: Liberal Radicalism"
comment: true
share: true
hljs: false
hljsLanguages: []
math: true
---

https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3243656

## Introduction

> (LR is) as flexible and responsive as the market, but avoids free-rider problems.  

- Flexible and responsive: any one can propose a new public good project, and the project can get enough fundings even when only a small community funds it.
- Subsidies create incentives for citizens to fund projects.

## Background
> (Free-rider problem is) due to the expense or inefficiency involved in excluding individuals from access.  

### Cons of Existing Solutions

- **1p1v**: oppress minorities.
- **Capitalism**: inefficiently exclude potential users.
- **Charitable organization**: difficult to closely align reliably with the common good.
- **QV**: it doesn’t solve the problem of flexibility, a.k.a., it requires a curated projects list.

## Model
### Assumptions

- We can verifiably distinguish among and identify these citizens.
- Any citizen may at any time propose a new public good.
- Our interest here is in maximization of dollar-equivalent value rather than achieving an equitable distribution of value.
- Utility function V is concave (国内的叫法一般是反的，即我们平常说的凸函数), smooth, increasing.
- The deficit is not bounded, a.k.a, the funding solution can collect unbounded taxes.

<!--more-->

### Optimization Target Function

Given:

- Let `$V_i^p(F^p)$` be the currency-equivalent utility function. It is the benefit that the citizen `i` can get when the project `p` is funded with `$F^p$` units of currency.
- The i x p contributions matrix `$\left\{c_i^p\right\}_i^p$`, where `$c_i^p$`  is the contribution citizen `i` makes to project `p`.

We need to find a funding distribution solution `$\left\{F^p\right\}^p$` which is a p-dimention vector. `$F^p$` is the funds allocated to project `p`. The solution maximize:

``` math
\[ \sum _ { p } \left(V _ { i } ^ { p } \left( F ^ { p } \right) - c _ { i } ^ { p }\right)  - t _ { i } \]
```

where

``` math
\[ \sum _ { i } t _ { i } = \sum _ { p } \left( F ^ { p } - \sum _ { i } c _ { i } ^ { p } \right) \]
```

Since V is concave, smooth and increasing, it is easy to find the maximum using the first order derivative, which gives

``` math
\[ V ^ { p ^ { \prime } } = 1 \]
```

### Capitalism

``` math
\[ F ^ { p } = \sum _ { i } c _ { i } ^ { p } \]
```

Result

``` math
\[ V ^ { p ^ { \prime } } = N \]
```

### 1p1v

``` math
\[ N \cdot \operatorname { Median } _ { i } V _ { i } ^ { p ^ { \prime } } \left( F ^ { P } \right) = 1 \]
```

The optimal solution requires mean, where median is absolutly different with mean.

### LR

``` math
\[ F ^ { p } = \left( \sum _ { i } \sqrt { c _ { i } ^ { p } } \right)
^ { 2 } \]
```


> (We) assume that citizens ignore their impact on the budget and costs imposed by it.  

After incorporating the deficit:

``` math
\[ V ^ { p ^ { \prime } } \approx 1 + \Lambda \]
```

It is assumed that `$\Lambda$` is on the order of 1/N.

## Extensions

### Budgeted matching funds

CLR: linear combine LR and Capitalism until the deficit is under the budget.

``` math
\[ F ^ { p } = \alpha \left( \sum _ { i } \sqrt { c _ { i } ^ { p } } \right) ^ { 2 } + ( 1 - \alpha ) \sum _ { i } c _ { i } ^ { p } \]
```

LR allows every project gets the optimal funding by incentivize citizens via the deficit. CLR is more practically, because in real world, there is always a budget.

### Collusion

**Coercion Resistance**: A voter cannot prove to anyone else who they voted for (or even, ideally, whether or not they voted) even if they wanted to.

### Negative contributions

> More broadly, negative contributions may be a quite powerful way to deter collusive schemes as they offer a way for any citizen to be a “vigilante enforcer” against fraud and abuse.  

On the other-side, it also can be used to attack and threaten other communities.
