---
layout: post
title: "Week 3 of Real Analysis"
author: "Addison Okell"
categories: Real Analysis
tags: [Real Analysis]
---

We started off this week with the Nested Interveral Lemma, which essentially states that any intersection of closed subsets is non-empty. This is useful because we can use this in a later Theorem to show every bounded sequence has a convergent subsequence.

This leads us to the defintion of a subsequence. If we have a sequence $a_n, n\in\mathbb{N}$ then ${a_n}_k, k\in \mathbb{N}$ is a subsequence of $a_n$. We can now define the Bolzano–Weierstrass Theorem. This states that every bounded sequence of real numbers has a convergent subsequence. To prove this we take a bound of the sequence and break it up into two intervals. We then take the interval with infinite points of the sequence and split it up into two intervals. We continue in this fashion and the Nested Interval Lemma tells us none of these intervals will ever be empty. Doing this we converge on a limit and picking a point in the sequence at each stage gives us a subsequence to the limit we converge to. 

We finally stated a tiny Theoreom that will prove to be useful in proving sequences dont converge and that is, every subsequence of a convergent sequence converge to the same limit as the orginal sequence. So we could show subsequences of a sequence converge to different limits telling us the orginal sequence does not converge.

Our next topic was a pretty popular subject Cauchy Sequences. Cauchy sequences are so fundemental because they allow us to fully understand the convergence of a sequence without trying to pick a candiate limit before hand. When using the defintion of a limit one must first make a educated guess about what they beleive the limit of the sequence should be. Instead we define a Cauchy sequence as 

$$|a_n-a_m|<\epsilon,  \forall n,m \geq N$$

With $n,m,N \in \mathbb{N}$. So instead of looking at how a sequence converges to a limit, we are looking at the difference between terms in the sequence and asking if we can always find a point in the sequence such that we will always be within $\epsilon$ of another point in the sequence. We then stated a Theorem about Cuachy sequences, mainly every Cauchy sequence is bounded. 

Finally we defined what a complete subset is of $\mathbb{R}$ is. A complete subset is one that for every Cuachy sequence in the subset, it converges to a point in the subset. We then stated in a Theorem that every Cuachy sequence of the real numbers converges and therefore $\mathbb{R}$ is complete.
