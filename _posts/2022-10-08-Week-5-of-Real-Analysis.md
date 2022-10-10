---
layout: post
title: "Week 5 of Real Analysis"
author: "Addison Okell"
categories: Real Analysis
tags: [Real Analysis]
---

We started this week finishing off the series unit of the course. We looked at an exmaple and showed the weirdness of infite series by showing the same sequence, summed in different orders produces two different answer depsite summing the same terms. This then motivated the defintion of types of convergent series. We say a series is absolutely convergent if $\sum_{i=0}^{\infty} \|a_i\|$ is convergent. If a series $\sum_{i=0}^{\infty} a_i$ converges but does not absolutewly converge, we say it is conditionally convergent. We then defined the rearangment of a series, which is where we change the order of the sequence we are summing with a permuation $\sigma$ where that $\sigma : \mathbb{N} \to \mathbb{N}$ is a bijection. This leads us to a Theorem about the rearrangement of series that states if a series is absolutely convergent any rearrangemnt of that series is equal to the same value as the sum of the orginal sequence. The proof is as follows, 

Assume $\sum_{n=1}^{\infty} a_k = L$ and is absouletly convergent. Then we can use the Cuachy crieation, for some $\epsilon > 0$ we have $\|\sum_{k=N+1}^{\infty} \|a_k\|\| < \epsilon$, and since we have a absolute value on this inside we can drop it on the outside. Now we can choose $\epsilon = \frac{\epsilon}{2}$. We also can say that for large enough N $\|\sum_{k=1}^{N} a_k - L\| < \frac{\epsilon}{2}$. Now for the first $N$ terms we can always find a point $M$ in the rearranged series such that all the term up to $N$ will appear in the rearrnaged series. So for any $m \geq M$ we have,

$$\|\sum_{k=1}^{m} a_{\sigma(k)}-L\| = \|\sum_{k=1}^{m} a_{\sigma(k)}-\sum_{k=1}^{N} a_k+\sum_{k=1}^{N} a_k-L\| \leq \|\sum_{k=1}^{m} a_{\sigma(k)}-\sum_{k=1}^{N} a_k\|+\|\sum_{k=1}^{N} a_k-L\|$$

But notice $\|\sum_{k=1}^{m} a_{\sigma(k)}-\sum_{k=1}^{N} a_k\|$ is nothing but the Cauchy criterion for our $\|a_k\|$ sequence so we have,

$$\|\sum_{k=1}^{m} a_{\sigma(k)}-\sum_{k=1}^{N} a_k\|+\|\sum_{k=1}^{N} a_k-L\| < \|\sum_{k=N+1}^{\infty} a_k\| + \frac{\epsilon}{2} < \epsilon $$

Thus $\sum_{k=1}^{\infty} a_{\sigma(k)} = L$.

We then stated the Rearragnemnt Rheorem that says if a series is condionally convergent then for every real number $L$ there is a rearrganment of the series that converges to L.

We then moved to the basic topology of $\mathbb{R}^n$, starting with a review of Linear Algebra. The main points we discussed were the eculdiean norm, Cauchy-Schwarz ineqauilty, the triangle ineqauilty and orthonormal sets. Breifly, the eculdian norm is the regular norm to mesure distance in a vector space. It is the equation 

$$\|\vec{v}\|=(\sum_{i=1}^{n} \|v_i\|^2)^{\frac{1}{2}}$$ 

where $v_i$ is the componets of the vector $\vec{v}$. This norm mesures the length of a vector. An important property of the norm is 

$$< \vec{x},\vec{x} > =\|\vec{x}\|^2$$ 

where $<\vec{x},\vec{x}>$ is the dot product of $\vec{x}$ with itself. The Cuachy-Shwarz inequailty then says that for any two vectors $\vec{x}, \vec{y}$ we have 

$$\|<\vec{x},\vec{y}>\| \leq \|\|\vec{x}\|\|\|\|\vec{y}\|\|$$ 

The proof of this is quite simple, square both sides and multiple them by two. Then we can write,

$$0 \leq 2\|\|\vec{x}\|\|\|\|\vec{y}\|\|^2-2\|<\vec{x},\vec{y}>\|^2$$ 
