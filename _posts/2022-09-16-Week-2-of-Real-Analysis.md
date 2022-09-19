---
layout: post
title: "Week 2 of Real Analysis"
author: "Addison Okell"
categories: Real Analysis
tags: [Real Analysis]
---

This week we started with the definition of a limit. A limit can be defined by taking some boundary we would like to keep the error within of the limit and defining a way to find a point in the sequence such that at this point and every point after is within this error. More formally we say the limit of a sequence exists and coverges to a limit $L$ if for any $\epsilon > 0$ there is a $n \geq N$ such that $\|a_n-L\|< \epsilon \ \forall n \geq N$. This formal definition although extremely precise turns out to be difficult to work with in some situations. So after introducing the formal definition the idea was to build up a set of Theorems and Lemmas to make calculating limits easier. 

The first of these was the Squeeze Theorem. The idea of the Squeeze Theorem is to take two sequences that bound the sequence we are interested in and sequences that have equal limits. If we can find sequences with these two properties then we may take $\lim_{n\to\infty} a_n \leq \lim_{n\to\infty} b_n \leq \lim_{n\to\infty} c_n$ and since $a_n, c_n$ bound the sequence $b_n$ and both equal the same limit say $L$ then $L \leq \lim_{n\to\infty} b_n \leq L$ and thus $\lim_{n\to\infty} b_n=L$.

Next, we talked about the relationship between bounded sets and convergent sequences. Mainly, a Theorem that says if a sequence $a_n$ converges in the real numbers then the set { $a_n:n\in \mathbb{N}$ } is bounded. This is an interesting Theorem, but it turns out its contrapositive is more useful. The contrapositive says if a sequence is unbounded it does not converge. This may be useful in determining whether a sequence of numbers converges since we have a good idea about what bounded sets look like from the previous week. 

We then started to develop some algebraic rules for limits. Assuming $a_n,b_n$ converge to $L,M$ respectively and $\alpha \in \mathbb{R}$, the four we covered in class were 

$$
\tag{1}
\lim_{n\to\infty} a_n+b_n=L+M 
$$

$$
\tag{2}
\lim_{n\to\infty} \alpha a_n=\alpha L 
$$

$$
\tag{3}
\lim_{n\to\infty} a_n b_n=LM
$$

$$
\tag{4}
\lim_{n\to\infty} \frac{a_n}{b_n}=\frac{L}{M}
$$

for $M \neq 0$. These rules make it much easier for us to calculate limits and negate the requirement of using the definition, but must still be proven using the definition. A proof of the ones not done in class are,

proof of (1):

We know $\|a_n-L\|<\epsilon_1$ for all $n \geq N_1$ and we know $\|b_n-M\|<\epsilon_2$ for all $n \geq N_2$. 
Then we know $\|a_n-L\|+\|b_n-M\|<\epsilon_1+\epsilon_2$. 
We also know by the triangle inequality $|(a_n-L)+(b_n-M)\| \leq \|a_n-L\|+\|b_n-L\|<\epsilon_1+\epsilon_2$ thus $\|(a_n-L)+(b_n-M)\|=\|(a_n+b_n)-(L+M)\|<\epsilon_1+\epsilon_2$ for some $n \geq max(N_1,N_2)$ and thus $a_n+b_n$ converges to $L+M$. This completes the proof.

proof of (2):

We want $\|\alpha a_n-\alpha L\|<\epsilon$ for all $n \geq N$.
So consider $\|\alpha a_n-\alpha L\|<\epsilon$.
We can say $\|\alpha a_n-\alpha L\|= \|\alpha \| \|a_n-L\|<\epsilon \implies \|a_n-L\|< \frac{\epsilon}{\|\alpha \|}$ for all $n \geq N$
since we know $a_n$ has limit $L$.
So we can say $\|\alpha a_n-\alpha L\|=\|\alpha\|\|a_n-L\|<\|\alpha\|\frac{\epsilon}{\|\alpha\|}=\epsilon$ for all $n \geq N$ as we wanted. This completes the proof.

proof of (4):

We want $\|\frac{a_n}{b_n}-\frac{L}{M}\|<\epsilon$ for all $n \geq N$. 

Now we can write this as $\|\frac{a_n}{b_n}-\frac{L}{M}\|=\|\frac{a_n}{b_n}-\frac{L}{b_n}+\frac{L}{b_n}-\frac{L}{M}\|$. Now by the triangle inequailty we have,
$\|\frac{a_n}{b_n}-\frac{L}{b_n}+\frac{L}{b_n}-\frac{L}{M}\| \leq \|\frac{1}{b_n}\|\|a_n-L\|+\|-L\|\|\frac{1}{b_n}-\frac{1}{M}\|=\|\frac{1}{b_n}\|\|a_n-L\|+\|\frac{L}{b_nM}\|\|b_n-M\|$. Since we know $b_n$ is a bounded sequence by the earlier Theorem we know there is some $b$ that is a upper bound for the sequence so that $\|\frac{1}{b_n}\|\|a_n-L\|+\|\frac{L}{b_nM}\|\|b_n-M\|< \|\frac{1}{b}\|\|a_n-L\|+\|\frac{L}{bM}\|\|b_n-M\|$$

Now since we know $a_n$ and $b_n$ converge and there limits are $L$ and $M$ we can say, $\|\frac{1}{b}\|\|a_n-L\|<\frac{\epsilon}{2} \implies \frac{\epsilon}{2\|\frac{1}{b}\|}$ for all $n \geq N_1$ and $\|\frac{L}{bM}\|\|b_n-M\|<\frac{\epsilon}{2} \implies \frac{\epsilon}{2\|\frac{L}{bM}\|}$ for all $n \geq N_2$.

Knowing this, we can write,

$$\|\frac{a_n}{b_n}-\frac{L}{M}\| \leq \|\frac{1}{b_n}\|\|a_n-L\|+\|-L\|\|\frac{1}{b_n}-\frac{1}{M}\|$$

$$=\|\frac{1}{b_n}\|\|a_n-L\|+\|\frac{L}{b_nM}\|\|b_n-M\|$$

$$< \|\frac{1}{b}\|\|a_n-L\|+\|\frac{L}{bM}\|\|b_n-M\|$$

$$<\|\frac{1}{b}\|\frac{\epsilon}{2\|\frac{1}{b}\|} + \|\frac{L}{bM}\|\frac{\epsilon}{2\|\frac{L}{bM}\|}$$

$$=\frac{\epsilon}{2} + \frac{\epsilon}{2}=\epsilon$$

As we requried. This completes the proof.

Finally, we defined monotone sequences. A monotone increasing sequence is a sequence such that $a_{n+1} \geq a_n \forall n\in \mathbb{N}$. A strictly monotone increasing sequence is a sequence such that $a_{n+1} > a_n \forall n\in \mathbb{N}$. We can analogously define monotone decreasing sequences. We then quickly stated a Theorem about monotone sequences, which is a monotone increasing sequence that is bounded converges and a monotone decreasing sequence that is bounded converges. 
