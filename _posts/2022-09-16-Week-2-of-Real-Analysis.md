---
layout: post
title: "Week 2 of Real Analysis"
author: "Addison Okell"
categories: Real Analysis
tags: [Real Analysis]
---

This week we started with the defintion of a limit. A limit can be defined by taking some boundary we would like to keep the error within of the limit and defining a way to find a point in the sequence such that at this point and every point after is within this error. More formally we define say the limit of a function exists and coverges to a limit $L$ if for any $\epsilon > 0$ there is a $N \geq$ such that $\|a_n-L\|< \epsilon$. This formal defintion although exteremely percise turns out to be difficult to work with in some situations. So after introducing the formal defintion the idea was to buiild up a set of Thereoms and Lemmas to make calculating limits easier. 

The first of these was the squeeze Theorem. The idea of the squeeze Theorem is to take two sequences, that bound the sequence we are interested in anb already know the limits of. If we can find sequences with these two properties we may then we may take $\lim_{n\to\infty} a_n \leq \lim_{n\to\infty} b_n \leq \lim_{n\to\infty} c_n$ and since $a_n, c_n$ bound the sequence $b_n$ and both equal the same limit say $L$ then $L \leq \lim_{n\to\infty} b_n \leq L$ and thus $\lim_{n\to\infty} b_n=L$.

Next, we talked about the relation between bounded sets and convergent sequences. Mainly, a Theorem that says if a sequence $a_n$ converges in the real numbers than the set $\{a_n:n\in \mathbb{N}\}$ is bounded. This is a interesting Theorem, but it turns out its contrapositive is more useful. The contrapositive says if a sequence is unbounded it does not converge. This may be useful in determining whether a sequence of numbers converges since we have a good idea about what bounded sets look like from the previous week. 

We then started to devolp some algebraic rules for limits. Assuming $a_n,b_n$ converge to $L,M$ resprectively and $\alpha \in \mathbb{R}$, the four we covered in class were $\lim_{n\to\infty} a_n+b_n=L+M$, $\lim_{n\to\infty} \alpha a_n=\alpha L$, $\lim_{n\to\infty} a_n b_n=LM$, and $\lim_{n\to\infty} \frac{a_N}{b_n}=\frac{L}{M}$ for $M \neq 0$.
