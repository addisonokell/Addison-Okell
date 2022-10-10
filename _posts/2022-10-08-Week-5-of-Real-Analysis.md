---
layout: post
title: "Week 5 of Real Analysis"
author: "Addison Okell"
categories: Real Analysis
tags: [Real Analysis]
---

We started this week finishing off the series unit of the course. We looked at an exmaple and showed the weirdness of infite series by showing the same sequence, summed in different orders produces two different answer depsite summing the same terms. This then motivated the defintion of types of convergent series. We say a series is absolutely convergent if $\sum_{i=0}^{\infty} \|a_i\|$ is convergent. If a series $\sum_{i=0}^{\infty} a_i$ converges but does not absolutewly converge, we say it is conditionally convergent. We then defined the rearangment of a series, which is where we change the order of the sequence we are summing with a permuation $\sigma$ where that $\sigma : \mathbb{N} \to \mathbb{N}$ is a bijection. This leads us to a Theorem about the rearrangement of series that states if a series is absolutely convergent any rearrangemnt of that series is equal to the same value as the sum of the orginal sequence. The proof is as follows, 

Assume $\sum_{n=1}^{\infty} a_k = L$ and is absouletly convergent. Then we can use the Cuachy crieation, for some $\epsilon > 0$ we have $\|\sum_{k=N+1}^{infty} \|a_k\|\| < \epsilon$. Now we can choose $\epsilon = \frac{\epsilon}{2}$. We also can say that for large enough N $\|\sum_{k=1}^{N} a_k - L\| < \frac{\epsilon}{2}$. Now for the first $N$ terms we can always find a point $M$ in the rearranged series such that all the term up to $N$ will appear in the rearrnaged series. So for any $m \geq M$ we have,

$$\|\sum_{k=1}^{m} a_k-L\| = \|\sum_{k=1}^{m} a_k-\sum_{k=1}^{N} a_k+\sum_{k=1}^{N} a_k-L\| \leq \|\sum_{k=1}^{m} a_k-\sum_{k=1}^{N} a_k\|+\|\sum_{k=1}^{N} a_k-L\|

We started this week with a brief summary of Linear Algebra. The main points we discussed were the eculdiean norm, Cauchy-Schwarz ineqauilty, the triangle ineqauilty and orthonormal sets. Breifly, the eculdian norm is the regular norm to mesure distance in a vector space. It is the equation 

$$\|\vec{v}\|=(\sum_{i=1}^{n} \|v_i\|^2)^{\frac{1}{2}})$$ 

where $v_i$ is the componets of the vector $\vec{v}$. This norm mesure the length of a vector. An important property of the norm is 

$$\< \vec{x},\vec{x} \> =\|\vec{x}\|^2$$ 

where $\<\vec{x},\vec{x}\>$ is the dot product of $\vec{x}$ with itself. The Cuachy-Shwarz inequailty then says that for any two vectors $\vec{x}, \vec{y}$ we have $$\|\<\vec{x},\vec{y}\>\| \leq \|\|\vec{x}\|\|\|\|\vec{y}\|\|$$ The proof of this is quite simple, consider the square of the 