---
layout: post
title: "Week 5 of Real Analysis"
author: "Addison Okell"
categories: Real Analysis
tags: [Real Analysis]
---

We started this week finishing off the series unit of the course. We looked at an exmaple and showed the weirdness of infite series by showing the same sequence, summed in different orders produces two different answer depsite summing the same terms. This then motivated the defintion of types of convergent series. We say a series is absolutely convergent if $\sum_{i=0}^{\infty} \|a_i\|$ is convergent. If a series $\sum_{i=0}^{\infty} a_i$ converges but does not absolutewly converge, we say it is conditionally convergent. We then defined the rearangment of a series, which is where we change the order of the sequence we are summing with a permuation $\sigma$ where that $\sigma : \mathbb{N} \to \mathbb{N}$ is a bijection. This leads us to a Theorem about the rearrangement of series that states if a series is absolutely convergent any rearrangemnt of that series is equal to the same value as the sum of the orginal sequence. The proof is as follows, 

Assume $\sum_{n=1}^{\infty} a_k = L$ and is absouletly convergent. Then we can use the Cuachy crieation, for some $\epsilon > 0$ we have $\|\sum_{k=N+1}^{\infty} \|a_k\|\| < \epsilon$, and since we have a absolute value on this inside we can drop it on the outside. Now we can choose $\epsilon = \frac{\epsilon}{2}$. We also can say that for large enough N $\|\sum_{k=1}^{N} a_k - L\| < \frac{\epsilon}{2}$. Now for the first $N$ terms we can always find a point $M$ in the rearranged series such that all the term up to $N$ will appear in the rearrnaged series. So for any $m \geq M$ we have,

$$|\sum_{k=1}^{m} a_{\sigma(k)}-L| = |\sum_{k=1}^{m} a_{\sigma(k)}-\sum_{k=1}^{N} a_k+\sum_{k=1}^{N} a_k-L| \leq |\sum_{k=1}^{m} a_{\sigma(k)}-\sum_{k=1}^{N} a_k|+|\sum_{k=1}^{N} a_k-L|$$

But notice $\|\sum_{k=1}^{m} a_{\sigma(k)}-\sum_{k=1}^{N} a_k\|$ is nothing but the Cauchy criterion for our $\|a_k\|$ sequence so we have,

$$|\sum_{k=1}^{m} a_{\sigma(k)}-\sum_{k=1}^{N} a_k|+|\sum_{k=1}^{N} a_k-L\| < |\sum_{k=N+1}^{\infty} a_k| + \frac{\epsilon}{2} < \epsilon $$

Thus $\sum_{k=1}^{\infty} a_{\sigma(k)} = L$.

We then stated the Rearragnemnt Rheorem that says if a series is condionally convergent then for every real number $L$ there is a rearrganment of the series that converges to L.

We then moved to the basic topology of $\mathbb{R}^n$ (The section I was mostg excited for), starting with a review of Linear Algebra. The main points we discussed were the eculdiean norm, Cauchy-Schwarz ineqauilty, the triangle ineqauilty and orthonormal sets. Breifly, the eculdian norm is the regular norm to mesure distance in a vector space. It is the equation 

$$\|\vec{v}\|=(\sum_{i=1}^{n} \|v_i\|^2)^{\frac{1}{2}}$$ 

where $v_i$ is the componets of the vector $\vec{v}$. This norm mesures the length of a vector. An important property of the norm is 

$$< \vec{x},\vec{x} > =\|\vec{x}\|^2$$ 

where $<\vec{x},\vec{x}>$ is the dot product of $\vec{x}$ with itself. The Cuachy-Shwarz inequailty then says that for any two vectors $\vec{x}, \vec{y}$ we have 

$$\|<\vec{x},\vec{y}>\| \leq \|\vec{x}\|\|\vec{y}\|$$ 

The proof of this is quite simple, square both sides and multiple them by two. Then we can write,

$$0 \leq 2\|\|\vec{x}\|\|\|\|\vec{y}\|\|^2-2\|<\vec{x},\vec{y}>\|^2$$ 

expanding this to summation notation we have,

$$2(\sum_{i=1}^{n} x_i^2) (\sum_{i=1}^{n} y_i^2)-2(\sum_{j=1}^{n} x_jy_j)^2$$

$$=2\sum_{i=1}^{n}\sum_{j=1}^{n} x_i^2 y_j^2-2(\sum_{i=1}^{n} x_iy_i)^2$$

$$=\sum_{i=1}^{n}\sum_{j=1}^{n} x_i^2 y_j^2+x_j^2 y_i^2-\sum_{i=1}^{n}\sum_{j=1}^{n} 2x_iy_ix_jy_j$$

$$=\sum_{i=1}^{n}\sum_{j=1}^{n} x_i^2 y_j^2-2x_iy_ix_jy_j+x_j^2 y_i^2$$

$$=\sum_{i=1}^{n}\sum_{j=1}^{n} (x_iy_j-x_jy_i)^2 \geq 0$$

Thus we have proved the statement through a tutology.

We then quickly stated the trinagle ineqaulity in $\mathbb{R}^n$, which is as we expect $\|\|\vec{x}+\vec{y}\|\| \leq \|\|\vec{x}\|\|\|\|\vec{y}\|\|$. Next, the defintion of a orthonormal set was reviewed. A set of vectors $\{\vec{v_1}, \vec{v_2}, ... , \vec{v_n}\}$ is orthonormal is the norm of every vector with another is the kroncker delta. A quick lemme was presented about orthonormal sets that says the norm of a othronormal set where every vector is multipled by a constant is the root of the sum of the square of each constant (Try toi say that 10 times fast!). We then started to generalize our previous results. Of course we started with the convergence of a sequence in $\mathbb{R}^n$. The basic idea is the same, the distance (or norm) between the limit and the sequence gets very small. Formally we say for some sequence $\vec{a_n}$ that $\vec{a_n}$ converges if for some $\epsilon > 0$ there exists an $N$ such that for all $k\geq N$ we have $\|\|\vec{a_k}-\vec{L}\|\| < \epsilon$. Then a very useful Lemma, that is if the sequence converges if and only if every sequence of each coordinate converges to the corrosponding component of the limit vector. This makes sense inuititvely since we expect that if a sequence converges the parts that build that sequence also converge. 

We then began to alk about closed sets. We first defined a limit points of a set. A point of a set A, which is a subset of $\mathbb{R}^n$, is a limit point if there exists a sequence in A such that it converges to that point. A set is then closed if it contains all of its limit points. 


