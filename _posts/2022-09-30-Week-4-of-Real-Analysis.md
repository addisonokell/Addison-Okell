---
layout: post
title: "Week 4 of Real Analysis"
author: "Addison Okell"
categories: Real Analysis
tags: [Real Analysis]
---
This week we started by introducing series. For a sequence $a_n$ we can define a series by summing each term in the sequence to infinity. We represent this a 
$\sum_{n=1}^{\infty} a_n$. We can also talk about partial sums of series, which we denote $S_n=\sum_{i=1}^{n}a_i$. These series are obviously very closely related to sequences and this is because we can talk about convergence and divergence of these series. We say a series converges if the summation of all points in the sequence equal a finite number, otherwise it diverges. 

Next we have a small Theorem which says that if $\sum_{n=1}^{\infty} a_n$ converges then, $\lim_{n \to \infty} a_n=0$. The contrapostive ends up being more useful, that is if $\sum_{n=1}^{\infty} a_n$ diverges then, $\lim_{n \to \infty} a_n \neq 0$. Next we state another Theorem, mainly the three statements are equivlent,

1. The series converges.
2. For every $\epsilon > 0$ there is an $N \in \mathbb{N}$ such that for all $n \geq N$ we have $\| \sum_{k=n+1}^{\infty} a_k \| < \epsilon$.
3. For every $\epsilon > 0$ there is an $N \in \mathbb{N}$ such that for all $n,m \geq N$ we have $\| \sum_{k=n+1}^{m} a_k \| < \epsilon$.

We then stated a propisiton, that is if $a_k \geq 0$ for $k \geq 1$ and $S_n=\sum_{k=1}^{n} a_k$ then $S_n$ is bounded above so $\sum_{k=1}^{\infty} a_k$ converges or $S_n$ is not bounded above so $\sum_{k=1}^{\infty} a_k$ diverges.

We then moved on to types of series and how to show series are convergent or not. First we defined the geometric series, which has form $\sum_{n=0}^{\infty} ar^n$ when $a \neq 0$. When $\|r\|<1$ we have the series is convergent and equals $\frac{a}{1-r}$. Next, we talked about the comparison test, which lets us comape a series to an already knwon series. For exmaple if we have,

$$|\sum_{n=1}^{\infty} a_n| \leq \sum_{n=0}^{\infty} b_n$$

then if $a_n$ diverges $b_n$ diverges and if $b_n$ converges then $a_n$ converges. We then stated the Root test, which says suppose $a_n \geq 0$ and let $\ell = \lim sup (a_n)^{\frac{1}{n}}$. If $\ell < 1$ then $\sum_{n=1}^{\infty} a_n$ converges, if $\ell > 1$ then $\sum_{n=1}^{\infty} a_n$ diverges and if $\ell = 1$ the test is inconclusive. 

We then defined an alternating series, which has the form $(-1)^na_n$ or $(-1)^{n+1}a_n$ for $a_n \geq 0$. We then have the Leibniz Alternating Series Theorem that states if $a_n$ is a monotone decreasing, alternating sequence, with $\lim_{n \to \infty} a_n =0$ then the series $\sum_{n=1}^{\infty} a_n$ converges.
