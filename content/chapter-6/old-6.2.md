---
title: "6.2 Sequences"
description:
slug:
image: "cookbook-746005_1280.jpg"
draft: true
---

{{% imgcap file="/img/chapter-6/cookbook-746005_1280.jpg" title="Image by RitaE from Pixabay" source="https://pixabay.com/images/id-746005/" %}}


## Introduction
When shopping at a grocery store it makes no difference if you grab eggs or flour first.  As long as you get everything on your list you'll be fine.

But a recipe is much different than a shopping list.  A recipe is an ordered list of instructions.  If you want the dish to turn out right, you have to do each step in the proper order.

In this section we are studying **sequences** which are more like recipes than shopping list.  With sequences, order matters.


## Sequence Notation
A sequence is generally thought of as any ordered list.   

Most of the time we will focus on sequences of numbers, but for the moment let's take a broad view and consider sequences of letters as well.  

The two sequences below both have the same letters, but the different order completely changes the meaning.

\[
\begin{array}{c}
D, E, S, S, E, R, T, S \newline \newline
S, T, R, E, S, S, E, D
\end{array}
\]

The same is true for sequences of numbers.  We cannot change the order of a sequence without affecting its meaning.  If you have ever typed a wrong digit in one of your PIN numbers then you've experienced this.

When we work with sequences it is important to be able to describe precisely where a particular term is located in a sequence.  Since each term has a unique position (first, second, third, etc.) we label each entry as $a_1, a_2, a_3$ and so on.

For instance, here is a sequence of multiples of $5$.

![](/img/chapter-6/sequence_terms.svg#center)

Notice that the label for each term gives its position, so that $a_1=5$ is the first term and $a_5=25$ is the fifth term, for example.  


{{% check %}}
1. In the sequence $ \thinspace  2, \thinspace  4, \thinspace  6, \thinspace  8, \thinspace  10, \thinspace \dots  \thinspace $ , identify the term $a_4$. {{% answer %}}$a_4$ is the label for the fourth term, so $a_4=8$.
{{% /answer %}}
1. In the sequence $ \thinspace  3, \thinspace  6, \thinspace  9, \thinspace  12, \thinspace  15, \thinspace \dots  \thinspace $ , what is the proper label for the number $9$? {{% answer %}}$9$ is the third term listed, so $a_3=9$.
{{% /answer %}}
{{% /check %}}


## Equations of Sequences
If the numbers in a sequence appear to follow some pattern, then it might be possible to find an equation that generates any term in the sequence.

An equation of sequence should return the value of a term based on its position.  Let's take another look at our sequence of multiples of $5$, this time listing the position of each term next to its value.

\[
\begin{array}{|c|c|}
\hline
  \text{Position} & \text{Value} \newline
\hline
   1 & 5  \newline
\hline
   2 & 10 \newline
\hline
   3 & 15 \newline
\hline
   4 & 20 \newline
\hline
   5 & 25 \newline
\hline
\end{array}
\]

It certainly appears that the value of each term is $5$ times its position.  In other words, to find the value of the $n$th term in the sequence we would just evaluate $5n$, which means the equation for this sequence is $a_{n}=5n$.

This looks similar to function notation, and that is not a coincidence.  In fact, it would not be incorrect to write it as $a(n)=5n$, provided we stipulate that $n$ can only be $1, 2, 3, \dots$ and so on.

So rather that thinking of a sequence only as an ordered list of numbers, we can equivalently think of it as any function whose domain is restricted to the natural numbers $1, 2, 3, \dots$.

With this new perspective in hand we can convert any function into a sequence just by changing the notation.  Instead of using $x$ (a generic real number) as the input variable we switch to $n$ (a generic natural number) and use $a_{n}$ to indicate the output rather than $f(x)$.

Aside from those notational differences, sequences are evaluated and manipulated exactly the same as regular functions.  

For instance, if $a_n = 2n + 6$ and we wanted to know the value of the $100$th term $a\_{100}$ the we evaluate it as follows.

\[
\begin{align}
a_n &= 2n+6 && \small \color{#5fa2ce}{\text{Original sequence}} \newline
a\_{100} &= 2(100)+6 && \small \color{#5fa2ce}{\text{Substitute $n=100$}} \newline
a\_{100} &= 206 && \small \color{#5fa2ce}{\text{Simplify}}
\end{align}
\]

The main difference, again, is that $a_n$ can only be evaluated for natural number inputs.  Expressions like $a\_{1/2}$ or $a\_{-3}$ or $a\_{2.6}$ are not allowed.

{{% check %}}
1. What is the 85th term of the sequence $ \thinspace  a\_n=2 n − 5(n−1)$? {{% answer %}}
\[
\begin{align}
a\_{n} &= 2 n − 5(n−1) && \small \color{#5fa2ce}{\text{Original sequence}} \newline
a\_{85} &= 2 (85) − 5(85−1) && \small \color{#5fa2ce}{\text{Substitute $n=85$}} \newline
a\_{85} &= 2 (85) − 5(84) && \small \color{#5fa2ce}{\text{Simplify $85-1$}} \newline
a\_{85} &= 170 − 420 && \small \color{#5fa2ce}{\text{Multiply $2(85)$ and $5(84)$}} \newline
a\_{85} &= − 250 && \small \color{#5fa2ce}{\text{Subtract}}
\end{align}
\]
{{% /answer %}}
{{% /check %}}


## Arithmetic Sequences
One common pattern that can emerge from sequences is that all the terms might be evenly spaced, as in this example below.

\[3, \thinspace 10, \thinspace 17, \thinspace 24, \thinspace \dots\]

Note that each term is $7$ larger than the previous one.

![](/img/chapter-6/sequence_arithmetic.svg#center)

If the terms are equally spaced then the sequence is called an **arithmetic** sequence.  The spacing between terms is called the *common difference* and can be found by taking any term and subtracting the one in front of it, so that $d=a_n - a\_{n-1}$.

All arithmetic sequences can be written using the following template

\[a_{n}=a_1+d(n-1)\]

where $a_1$ is the first term of the sequence and $d$ is the constant spacing between terms.

Using this pattern, the equation for the sequence above is

\[a_{n}=3+7(n-1)\]

since the first term is $3$ and the spacing is $7$.

{{% check %}}
1. Is $\ 5, \thinspace 9, \thinspace 13, \thinspace 19, \thinspace 25 \thinspace $ an arithmetic sequence?  If so, give its equation. {{% answer %}}No this is not an arithmetic sequence.  The spacing for the first few terms is $4$ but for the last few it is $6$.  Since the spacing is not constant it cannot be an arithmetic sequence.
{{% /answer %}}
1. Is $\ 72, \thinspace 63, \thinspace 54, \thinspace 45, \thinspace 36 \thinspace $ an arithmetic sequence?  If so, give its equation. {{% answer %}}Yes, this is an arithmetic sequence since the spacing between terms is always $-9$.  The equation is
\[a_n=72-9(n-1)\]
{{% /answer %}}
{{% /check %}}


## Geometric Sequences
The other common pattern we encounter with sequences occurs when each new value is a multiple of the previous one.  

Here is an example where each term is $2$ times the term in front of it.

\[11, \thinspace 22, \thinspace 44, \thinspace 88, \thinspace \dots\]

When there is a consistent multiplying factor between terms, the sequence is called a **geometric** sequence.  The multipling factor is called the *common ratio* and can be found by dividing any term by the one right in front of it, so that $r=\frac{a_n}{a\_{n-1}}$.

![](/img/chapter-6/sequence_geometric.svg#center)

All geometric sequences can be written using the following model

\[a_{n}=a_1 \cdot r^{n-1}\]

where $a_1$ is the first term of the sequence and $r$ is the common ratio between terms.

Using this pattern, the equation for the sequence above is

\[a_{n}=11(2)^{n-1}\]

since the first term is $11$ and the ratio is $2$.

{{% check %}}
1. Is $\ 64, \thinspace 32, \thinspace 16, \thinspace 8, \thinspace 4 \thinspace $ a geometric sequence?  If so, give its equation. {{% answer %}}Yes, each term is $1/2$ times the previous one, so this is geometric with a ratio of $r=1/2$.  The equation is
\[a_n=64 \left(\frac{1}{2}\right)^{n-1}\]
{{% /answer %}}
1. Is $\ \frac{-1}{3}, \thinspace \frac{2}{15}, \thinspace \frac{-4}{75}, \thinspace \frac{8}{375}, \thinspace \frac{-16}{1875} \thinspace $ a geometric sequence?  If so, give its equation. {{% answer %}}Yes, this is geometric with a ratio of $r=-2/5$.  The equation is
\[a_n=\frac{-1}{3}\left(\frac{-2}{5} \right)^{n-1}\]
{{% /answer %}}
{{% /check %}}
