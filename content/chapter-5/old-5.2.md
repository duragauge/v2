---
title: "5.2 Complex Numbers and The Fundamental Theorem of Algebra"
description:
slug:
image: "venice.jpg"
draft: true
---
{{% imgcap file="/img/chapter-5/venice.jpg" title="Venice, Italy.  Photo by Damiano Baschiera on Unsplash" source="https://unsplash.com/photos/hFXZ5cNfkOk" %}}

## Introduction
During the 1500's Italian mathematicians held public contests as a way to gain notoriety and supplement their income.  Since anyone could be challenged at any time, most mathematicians kept their discoveries secret.

Antonio Fior was an inexperienced mathematician who learned a secret for solving one type of cubic equation from his dying master.  Anxious to make a name for himself, Fior traveled to Venice and challenged Niccolò Tartaglia, one of the most gifted mathematicians of the day, to solve 30 cubic equations.

Working day and night, Tartagia found what no one though possible: a general process for solving all cubic equations, not just the ones Fior had asked.

With this new technique Tartaglia solved all of Fior's problems in 2 hours and easily won the contest.  But what cemented Tartaglia's place in history is that his solution involved square roots of negative values, what we now call *imaginary numbers*.







## Determine the Number of Real & Imaginary Zeros
We will use the Fundamental Theorem of Algebra to help us identify the number of real and imaginary zeros of a polynomial when a domain coloring graph is unavailable.

Consider, for instance, the polynomial $p(x)=x^5+1$ whose graph is given below.

![](/img/chapter-5/poly_turns_6.svg#center)

We can see from the graph that it has just one real zero, corresponding to the x-intercept at $x=-1$.  Since it is a 5th degree polynomial, the Fundamental Theorem of Algebra tells us that it must have 5 zeros total, so the remaining 4 zeros must be imaginary.  

{{% check %}}
Find the number of real and imaginary zeros of each polynomial.

1. &nbsp; ![](/img/chapter-5/FTA_4c.png#center) {{% answer %}}This is a 4th degree polynomial with 2 real zeros (x-intercepts), so there must be 2 imaginary zeros.{{% /answer %}}
1. &nbsp; ![](/img/chapter-5/FTA_3b.png#center) {{% answer %}}This is a 3rd degree polynomial with 3 real zeros (x-intercepts), so there are no imaginary zeros.{{% /answer %}}
1. &nbsp; ![](/img/chapter-5/FTA_5b.png#center) {{% answer %}}This is a 5th degree polynomial with 3 real zeros (x-intercepts), so there are 2 imaginary zeros.{{% /answer %}}
{{% /check %}}


## Conjugate Zeros Theorem
You may have noticed a curious fact about the number of imaginary zeros.  In every example we've looked at so far, the number of imaginary zeros has always been even, and there's a very good reason for that.

The **conjugate zeros theorem** says that if the coefficients of your polynomial are real numbers, and $a+bi$ is a zero, then its *conjugate* $a-bi$ is also a zero.  In other words, imaginary zeros always come in pairs, which means there must always a even number of them.

You can see the conjugate pairs in a domain coloring graph.  For instance, look at the domain coloring graph of $f(z)=z^2-4z+5$.

![](/img/chapter-5/domain_coloring_z2-4z+5.png#center)

There are two imaginary zeros, $2+i$ and $2-i$, corresponding to the points $(2, 1)$ and $(2, -1)$ on the graph.  As expected, these two imaginary zeros are conjugates.  The only difference between them is that one has a positive imaginary part while the imaginary part of the other is negative.

{{% check %}}
1. Suppose you know that $4+3i$ is an imaginary zero of some a a polynomial with real valued coefficients.  Which other imaginary number must also be a zero? {{% answer %}}Its conjugate $4-3i$ must also be a zero.{{% /answer %}}
1. Is it possible for a polynomial with real valued coefficients to have exactly one imaginary zero? {{% answer %}}No, the conjugate zeros theorem says they only come in pairs.{{% /answer %}}
{{% /check %}}


## Multiple Zeros
When using the Fundamental Theorem of Algebra to count the number of real and imaginary zeros of a polynomial, we must be mindful of multiple zeros.

For instance, when looking at the graph of $p(x)=x^4-3x^{2}$

![](/img/chapter-5/FTA_4b.png#center)

it would be easy to mistakenly say that since it has $3$ x-intercepts, it must have $3$ real zeros and only $1$ imaginary zero.  Clearly this cannot be the case; the conjugate zeros theorem tells us that having only $1$ imaginary zero is impossible.

Taking another look at the graph we notice that the real zero at $x=0$ has a multiplicity of $2$, since it touches the x-axis and bounces off.  This means that $p(x)=x^4-3x^{2}$ actually has $4$ real zeros and $0$ imaginary zeros.

{{% check %}}
State the degree of each polynomial.  Then give the number of real zeros and the number of imaginary zeros.

1. &nbsp; ![](/img/chapter-5/poly_graph_real_imaginary_zeros_3.png#center) {{% answer %}}It is a 3rd degree polynomial.  The real zero at $x=2$ has a multiplicity of $3$, giving us $3$ real zeros and no imaginary zeros.{{% /answer %}}
1. &nbsp; ![](/img/chapter-5/poly_graph_real_imaginary_zeros_2.png#center) {{% answer %}}It is a 5th degree polynomial.  It has x-intercepts (real zeros) at $x=-1$, $x=0$ and $x=1$. The zeros at $x=-1$ and $x=1$ both have a multiplicity of $2$ since they bounce off the x-axis like a parabola.  This means there are $5$ real zeros total and none that are imaginary.{{% /answer %}}
1. &nbsp; ![](/img/chapter-5/poly_graph_real_imaginary_zeros_1.png#center) {{% answer %}}This is a 6th degree polynomial, so there must be $6$ zeros total.  We can see $4$ real zeros (two each at $x=-2$ and $x=2$) which leaves $2$ more zeros that must be imaginary and cannot be seen on the graph.{{% /answer %}}
{{% /check %}}


## Looking Ahead
After Tartaglia's work, a method was quickly found for finding all 4 zeros of any 4th degree polynomial by Cardano's assistant, Ferrari.  Mathematicians all over the world felt that it was just a mater of time before they would have formulas for not only any 5th degree polynomial, but for every polynomial.  In the next section we will see the end result of their efforts.
