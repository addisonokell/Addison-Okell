---
layout: post
title: "Week 2 of Real Analysis"
author: "Addison Okell"
categories: Real Analysis
tags: [Real Analysis]
---

This week we started with the definition of a limit. A limit can be defined by taking some boundary we would like to keep the error within of the limit and defining a way to find a point in the sequence such that at this point and every point after is within this error. More formally we define say the limit of a function exists and coverges to a limit $L$ if for any $\epsilon > 0$ there is a $N \geq$ such that $\|a_n-L\|< \epsilon$. This formal definition although extremely precise turns out to be difficult to work with in some situations. So after introducing the formal definition the idea was to build up a set of Theorems and Lemmas to make calculating limits easier. 

The first of these was the squeeze Theorem. The idea of the squeeze Theorem is to take two sequences, that bound the sequence we are interested in and already know the limits of. If we can find sequences with these two properties we may then we may take $\lim_{n\to\infty} a_n \leq \lim_{n\to\infty} b_n \leq \lim_{n\to\infty} c_n$ and since $a_n, c_n$ bound the sequence $b_n$ and both equal the same limit say $L$ then $L \leq \lim_{n\to\infty} b_n \leq L$ and thus $\lim_{n\to\infty} b_n=L$.

Next, we talked about the relationship between bounded sets and convergent sequences. Mainly, a Theorem that says if a sequence $a_n$ converges in the real numbers then the set $$\{a_n:n\in \mathbb{N}\}$$ is bounded. This is an interesting Theorem, but it turns out its contrapositive is more useful. The contrapositive says if a sequence is unbounded it does not converge. This may be useful in determining whether a sequence of numbers converges since we have a good idea about what bounded sets look like from the previous week. 

We then started to develop some algebraic rules for limits. Assuming $a_n,b_n$ converge to $L,M$ respectively and $\alpha \in \mathbb{R}$, the four we covered in class were $\lim_{n\to\infty} a_n+b_n=L+M$, $\lim_{n\to\infty} \alpha a_n=\alpha L$, $\lim_{n\to\infty} a_n b_n=LM$, and $\lim_{n\to\infty} \frac{a_N}{b_n}=\frac{L}{M}$ for $M \neq 0$. These rules make it much easier for us to calculate limits and negate the requirement of using the definition, but must still be proven using the definition. A proof of the first is,

proof of (1):

We know $\|a_n-L\|<\epsilon_1$ for all $n \geq N_1$ and We know $\|b_n-M\|<\epsilon_2$ for all $n \geq N_2$. 
Then we know $\|a_n-L\|+\|b_n-M\|<\epsilon_1+\epsilon_2$. 
We also know by the triangle inequality $|(a_n-L)+(b_n-M)\| \leq \|a_n-L\|+\|b_n-L\|<\epsilon_1+\epsilon_2$ thus $\|(a_n-L)+(b_n-M)\|=\|(a_n+b_n)-(L+M)\|<\epsilon_1+\epsilon_2$ for some $n \geq max(N_1,N_2)$ and thus $a_n+b_n$ converge to $L+M$. This completes the proof.

Finally, we defined monotone sequences. A monotone increasing sequence is a sequence such that $a_{n+1} \geq a_n \forall n\in \mathbb{N}$. A strictly monotone increasing sequences is a sequence such that $a_{n+1} > a_n \forall n\in \mathbb{N}$. We can analogously define monotone decreasing sequences. We then quickly stated a Theorem about monotone sequences, which is a monotone increasing sequence that is bounded converges and a monotone decreasing sequence that is bounded converges. 
