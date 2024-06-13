---
title: "6.3 Series"
description:
slug:
image: "school-1689750_1280.jpg"
draft: true
---

{{% imgcap file="/img/chapter-6/school-1689750_1280.jpg" title="Image by Julia Schwab from Pixabay" source="https://pixabay.com/images/id-1689750/" %}}


## Introduction
When Carl Friedrich Gauss{{% sidenote "Gauss"%}}This is the same Gauss that gave us [Gauss-Jordan Elimination](/chapter-6/6.1) and the [Fundamental Theorem of Algebra](/chapter-5/5.2/#the-fundamental-theorem-of-algebra){{% /sidenote %}} was a young boy in Germany it was common for students to do their work on small slate chalkboards.  

The story is told that one day in 1786, when Gauss was just 9 years old, his teacher gave the class a challenging problem.  It was something along the lines of adding up all the whole numbers from $1$ to $100$, an exercise that would certainly take the entire class hour.

Almost as soon as the problem had been given, Gauss wrote down a single number and put his slate on the teacher's desk.

At the end of the hour, Gauss was one of the few students with the correct answer.  

So how did he do it?  That's what we'll look into in this section.


## What is a Series?
In the last section we learned that an ordered list of numbers is called a *sequence*.  If you add up the terms of a sequence you get something new that we call a **series**.  Here is a side by side comparison.

\[
\begin{align}
\text{Sequence: } & \thinspace 2, \thinspace 4, \thinspace 6, \thinspace 8 \newline
\text{Series: } & \thinspace 2 + 4 + 6 + 8 = 20
\end{align}
\]

Notice that the addition in the series simplifies to a single value.  Finding the sum of a series, if it exists, is one of the primary exercises with series.

The problem young Gauss was given was that of finding the value of a series, though it may not have been worded that way.

\[
\begin{align}
\text{Sequence: } & \thinspace 1, \thinspace 2, \thinspace 3, \thinspace \dots , \thinspace 100 \newline
\text{Series: } & \thinspace 1 + 2 + 3 + \cdots + 100 = \text{ ?}
\end{align}
\]

In English the words "sequence" and "series" are often used interchangeably without much difference.  For example, a "series of events" generally means the same as "a sequence of events".  In mathematics, however, they are different and we'll need to pay close attention to which word is used.


{{% check %}}
1. Is $17+27+37+47$ a sequence or a series? {{% answer %}}This is a series since we are adding up the numbers $17, 27, 37, 47$.
{{% /answer %}}
1. Write the series for the sequence $5, \thinspace 10, \thinspace 15, \thinspace 20, \thinspace 25$. {{% answer %}}\[5+10+15+20+25\]
{{% /answer %}}
1. Write a series for the sum of the first four terms of the sequence $a_n=2^n$. {{% answer %}}The first four terms of the sequence are $2^1, 2^2, 2^3, 2^4$, so the series would be \[2^1+2^2+2^3+2^4\].
{{% /answer %}}
{{% /check %}}


## Arithmetic Series
We are now at a point where we can start to think about how Gauss might have be able to find his sum.

\[\Large 1 + 2 + 3 + \cdots + 100\]

While we don't know for sure how Gauss pictured this problem in his mind, he certainly spotted a pattern and used that to his advantage.  

There are a number of ways to visualize it, but perhaps the simplest is to look at pairs of numbers.  If you choose the pairs carefully, they will all equal the same number!

![](/img/chapter-6/series_gauss_v3.svg#center)

In this case we end up with $50$ pairs that each equal $101$ so the total is $50 \times 101 = 5050$.

This same pattern occurs for every arithmetic series.  To find the sum of the first $n$ terms you add the first and last terms and multiply by the number of pairs.  So, whenever your sequence is arithmetic in the form $a_n=a_1+d(n-1)$, the sum of the first $n$ terms is given by this formula.

\[\Large S_n=\frac{n}{2} \bigl(a_1+a_n \bigr)\]

Let's walk through an example using this formula by evaluating the following series.

\[\Large 380 + 378 + 376 + \cdots + 252\]

We should start by making sure these numbers come from an arithmetic sequence.  If they don't, then we can't use our formula to find the sum.

The first term is $a_1=380$ and the spacing is $d=-2$, so this is an arithmetic series and the terms come from the equation $a_n=380-2(n-1)$.  

The arithmetic summation formula involves $n$, $a_1$ and $a_n$.  We know $a_1$ and $a_n$ but don't have a value for $n$.  However, if we put $a_n=252$ into the equation for the sequence we can solve for $n$.  

\[
\begin{align}
a_n &= 380-2(n-1) && \small \color{#5fa2ce}{\text{Sequence equation}} \newline
252 &= 380-2(n-1) && \small \color{#5fa2ce}{\text{Replace $a_n=252$}} \newline
-128 &= -2(n-1) && \small \color{#5fa2ce}{\text{Subtract $380$}} \newline
64 &= n-1 && \small \color{#5fa2ce}{\text{Divide by $-2$}} \newline
65 &= n && \small \color{#5fa2ce}{\text{Add $1$}}
\end{align}
\]

We now have all the pieces in place to find the sum of the $n=65$ terms of our series, starting with $a_1=380$ and ending at $a\_{65}=252$.

\[
\begin{align}
S\_{n} &= \frac{n}{2}\bigl(a_1+a_n\bigr) && \small \color{#5fa2ce}{\text{Arithmetic summation formula}} \newline
S\_{65}&= \frac{65}{2} \bigl(380+252\bigr) && \small \color{#5fa2ce}{\text{Insert values}} \newline
&= 20540 && \small \color{#5fa2ce}{\text{Evaluate}}
\end{align}
\]

One final note on this summation formula.  Gauss wasn't the first to discover how to add up an arithmetic series.  Fibbonacci, for one, published this method in 1202 and Archimedes probably knew of it by 200BC.  But the story of Gauss discovering the formula in school is famous and it would be breaking tradition not to relate it!{{% sidenote "Gauss" %}}Many retellings of this famous story exist.  The earliest version was written in 1856 by [Wolfgang Sartorius](https://archive.org/details/gauss00waltgoog/page/n15), who worked with Gauss at the University of Göttingen.  [Brian Hayes](http://bit-player.org/2007/a-mathematical-fable-revisited) compares many of them in this [Scientific American article](/img/chapter-6/Gauss's_Day_of_Reckoning_by_Brian_Hayes).{{% /sidenote %}}

{{% check %}}
1. If there are $30$ terms in the series $16+11+6+ \cdots -129$, what is the sum $S\_{30}$? {{% answer %}}Since $n=30$, $a_1=16$ and $a\_{30}=-129$, the sum is
\[ \begin{align}
S\_{30} &= \frac{30}{2} \bigl(16-129 \bigr)\newline
&= -1695
\end{align}
\]
{{% /answer %}}
1. Find the sum of the arithmetic series $\ 32,\ 36,\ 40,\ \dots,\ 80 \thinspace $. {{% answer %}} First find the equation for the sequence that creates the terms.
\[a\_{n}= 380-2(n-1)\]
Then use $a_n=80$ to find $n$.
\[ \begin{align}
a\_{n} &=  380-2(n-1) &&  \small \color{#5fa2ce}{\text{Sequence equation}} \newline
80  &=  32+4(n-1)  &&  \small \color{#5fa2ce}{\text{Replace $a\_{n}=80$}} \newline
48  &=  4(n-1)     &&  \small \color{#5fa2ce}{\text{Subtract $32$}} \newline
12  &=  n-1        &&  \small \color{#5fa2ce}{\text{Divide by $4$}} \newline
13  &=  n          &&  \small \color{#5fa2ce}{\text{Add $1$}}
\end{align}
\]
And finally use the summation formula.
\[
\begin{align}
S\_{n}  &= \frac{n}{2}\bigl(a_1+a_n\bigr) && \small \color{#5fa2ce}{\text{Arithmetic summation formula}} \newline
S\_{13} &= \frac{13}{2} \bigl(32+80\bigr) && \small \color{#5fa2ce}{\text{Insert values}} \newline
        &= 728                            && \small \color{#5fa2ce}{\text{Evaluate}}
\end{align}
\]
{{% /answer %}}
{{% /check %}}


## Finite Geometric Series
It bears repeating that the formula above only works if the sequence is arithmetic.  If we encounter a geometric series then there is a completely different formula.

To add up the first $n$ terms of a geometric sequence of the form $a_n=a_1 r^{n-1}$, use the following formula.

\[\Large S_n = \frac{a_1(1-r^n)}{1-r}\]

To show how this works let's look at an application.

### Finite Geometric Series - Example 1

{{% marnote "strawberries" %}}![](/img/chapter-6/johnny-martinez-lBIFDzYwbDo-unsplash.jpg) [Photo by Johnny Martínez on Unsplash](https://unsplash.com/photos/lBIFDzYwbDo) {{% /marnote %}}

In 1988 farmers in Oregon produced a record crop of 100 million pounds of strawberries. Since then strawberry production has dropped 7% annually.  Can we use that information to determine how many millions of pounds of strawberries grown over a 20 year period starting in 1998?

If you look closely at the summation formula, all we need are the first term $a_1$, the common ratio $r$, and the number of terms $n$.  Unlike the arithmetic series formula, we don't need to find the final term $a_n$.

Taking $a_1=100$, $r=0.93$ (since there is a 7% drop), and $n=20$, we can find the sum using the formula above.
\[
\begin{align}
S\_{n}  &= \frac{a_1(1-r^n)}{1-r} && \small \color{#5fa2ce}{\text{Geometric summation formula}} \newline
S\_{20} &= \frac{100 \bigl(1-(0.93)^{20}\bigr)}{1-(0.93)} && \small \color{#5fa2ce}{\text{Insert values}} \newline
        &= 1093.94 && \small \color{#5fa2ce}{\text{Evaluate}}
\end{align}
\]

This means Oregon produced around 1094 million total pounds of strawberries over that 20 year period.

When using a calculator to evaluate expressions like this, be very careful to put the exponent in the correct place and include parenthesis around the denominator.  The above calculation looks like this.

![](/img/chapter-6/geometric_sequence_calculator_eval.svg#center)

### Finite Geometric Series - Example 2

{{% marnote %}}![](/img/chapter-6/josh-appel-NeTPASr-bmQ-unsplash.jpg) [Photo by Josh Appel on Unsplash](https://unsplash.com/photos/NeTPASr-bmQ) {{% /marnote %}}

Suppose you put a penny on the first square of a chess board, two on the second, four on the third, eight on the
fourth and continued doubling until you got to the 64th square. How much money, in dollars, would it take to fill up the chess board?

In dollars $a_1=0.01$, since the amount is doubling $r=2$, and we know $n=64$.  So the sum is

\[
\begin{align}
S\_{n}  &= \frac{a_1(1-r^n)}{1-r} && \small \color{#5fa2ce}{\text{Geometric summation formula}} \newline
S\_{64} &= \frac{0.01 \bigl(1-(2)^{64}\bigr)}{1-(2)} && \small \color{#5fa2ce}{\text{Insert values}} \newline \newline
        &\approx 1.84467 \times 10^{17} && \small \color{#5fa2ce}{\text{Evaluate}} \newline \newline
        &\approx \$184,467,000,000,000,000
\end{align}
\]

To help put that in perspective, every person on Earth would need to contribute more than 20 million dollars each to fill the chess board with pennies!  


{{% check %}}
1. After college Bob got a job earning $25,000 with 3% raises each year. 50 years later he retired from that same job. How much money did he earn over his entire career? {{% answer %}}Use $a_1=25000$, $r=1.03$ and $n=50$ to evaluate the sum.
\[
\begin{align}
S\_{n}  &= \frac{a_1(1-r^n)}{1-r} && \small \color{#5fa2ce}{\text{Geometric summation formula}} \newline
S\_{50} &= \frac{25000 \bigl(1-(1.03)^{50}\bigr)}{1-(1.03)} && \small \color{#5fa2ce}{\text{Insert values}} \newline
        &= \$2,819,921.68 && \small \color{#5fa2ce}{\text{Evaluate}}
\end{align}
\]
{{% /answer %}}
{{% /check %}}


## Infinite Geometric Series
Not that long ago most music was sold on compact disks, or CDs.  {{% marnote %}}![](/img/chapter-6/cd-1003342_1280.jpg)[Photo by Bruno Glätsch on Pixabay](https://pixabay.com/images/id-1003342/) {{% /marnote %}}
According to data collected by the Recording Industry Association of America, 705.4 million CDs were sold in 2005 and that number has been declining by about $16.9\\%$ per year.  

Using the formula for a geometric series we can say that the cumulative total number of CDs sold (in millions) since 2005 is given by

\[
S\_{n}  = \frac{705.4(1-(0.831)^n)}{1-(0.831)}
\]

Let's chart those values for several years starting in 2005.

\[
\begin{array}{|c|c|c|}
\hline
  \text{Year} & n & \text{Millions of CDs Sold} \newline
\hline
   2005 & 1 & 705.4  \newline
\hline
   2010 & 6 & 2799.4 \newline
\hline
   2015 & 11 & 3629.3 \newline
\hline
   2020 & 16 & 3958.1 \newline
\hline
   2025 & 21 & 4088.4 \newline
\hline
   2030 & 26 & 4140.1 \newline
\hline
\end{array}
\]

Looking at these numbers it appears that the total number of CDs sold is growing more slowly as time progresses.  

And that seems reasonable.  Since fewer and fewer CDs are being sold we shouldn't expect the total to rise very much.  

In fact, if we compute the values for $2035$ and $2040$ they are nearly the same at $4160.5$ and $4168.6$.

But what would happen if we projected this process out further into the future?  Could it be that there is some limit to the number of CDs that will ever be sold no mater how much time passes?

Mathematically, what we are asking is if there is such a thing as an infinite sum that adds up to a fixed number.  Is it possible for something like $S_{\infty}$ to exist?

The answer lies hidden in our formula for the sum of the first $n$ terms of a geometric sequence.

\[\Large S_n = \frac{a_1(1-r^n)}{1-r}\]

As $n$ increases the only part that changes is the $r^n$.  So what happens to $r^n$ as $n$ gets larger?  In the figure below you can change $r$ and see how that impacts $r^n$.

{{% geogebra ratio="40%" id_1="D6uDhhnaO0kN7YDh" id_2="gwkjxypb" id_m="rpg8fm6k" %}}<br>

Notice that the values for $r^n$ drop toward $0$ whenever $-1<r<1$.  In other words, if $-1<r<1$ then $r^n \rightarrow 0$ as $n \rightarrow \infty$.  When this happens our summation formula becomes

\[\Large S_{\infty}=\frac{a_1}{1-r}\]

It might seem odd that you can add up infinitely many things and arrive at something other than infinity--but that's exactly what this formula says you can do, provided $-1<r<1$.  

We've already seen that the total number of CDs sold since 2005 appears to be leveling off.  Let's now use this infinite geometric series formula to find that limiting value.  

To do that we use infinite sum formula with $a_1=705.4$ million and, since there is a $16.9\\%$ decline, $r=0.831$.

 \[
 \begin{align}
 S\_{\infty}  &= \frac{a_1}{1-r} && \small \color{#5fa2ce}{\text{Infinite geometric summation formula}} \newline
  &= \frac{705.4}{1-(0.831)} && \small \color{#5fa2ce}{\text{Insert values}} \newline
         &= 4173.96 && \small \color{#5fa2ce}{\text{Evaluate}}
 \end{align}
 \]

This formula predicts that 4173.96 million CDs will be sold from 2005 to the end of time, if that $16.9\\%$ decline persists.


{{% check %}}
{{% imgcap file="/img/chapter-6/mick-haupt-fnKoW9mvgkA-unsplash.jpg" title="Photo by Mick Haupt on Unsplash" source="https://unsplash.com/photos/fnKoW9mvgkA" %}}
1. Before CDs there were cassette tapes, and they faced an even more rapid demise.  If 76 million cassettes were sold in 2000 and that amount decreases by 55% per year, how many cassette tapes will be sold from 2000 until the end of time? {{% answer %}}Using $a_1=76$ and $r=.45$ the infinite geometric series formula gives
\[
\begin{align}
S\_{\infty}  &= \frac{a_1}{1-r} && \small \color{#5fa2ce}{\text{Infinite geometric summation formula}} \newline
 &= \frac{76}{1-(0.45)} && \small \color{#5fa2ce}{\text{Insert values}} \newline
        &= 138.18 && \small \color{#5fa2ce}{\text{Evaluate}}
\end{align}
\]
and we conclude that the total number of cassette tapes sold from 2000 will be 138.18 million, assuming the 55% decline continues.
{{% /answer %}}
1.	Why is there no formula for an infinite arithmetic series? {{% answer %}}
An infinite geometric series only has a sum if each new value is sufficiently smaller than the previous number and eventually shrinks toward $0$ (that's why we need $-1<r<1$).  The terms in an arithmetic are evenly spaced, so shrinking towards $0$ is impossible.  If you add up an infinite number of terms from an arithmetic series you would approach $\infty$ or $-\infty$.
{{% /answer %}}
{{% /check %}}


## Summation Notation
When a series has more than a couple of terms there is a compact notation that helps us avoid having to write out a long string of sums.  

This new summation notation is sometimes called "sigma" notation, because the Greek letter $\Sigma$ (sigma) is used to represent summation.  Here's an example of what summation notation looks like.

\[\Large \sum_{k=1}^{8} k^2\]

This a very dense notation and there is a lot here for us to unpack.  

First note that the equation that generates the terms of the sequence is written to the right of the big $\Sigma \thinspace $.

Below the $\Sigma \thinspace $ we are told what the variable is and what its first value should be.

Above the $\Sigma \thinspace $ is the final value that gets put into the equation.  

![](/img/chapter-6/summation_notation.svg#center)

To expand this shorthand version back into a large sum we start by letting $k=1$ in the equation and keep going until $k=8$, all the while adding up the terms we create.  In the figure below you can see how this would work.

{{% geogebra ratio="20%" id_1="NscTHqSUr5DSOQ1W" id_2="kete4zs4" id_m="ekmgvmg8" %}}

{{% check %}}
Expand the series below.
\[\Large \sum\_{k=1}^{5} 3k\] {{% answer %}}
\[\sum\_{k=1}^{5} 3k=3(1)+3(2)+3(3)+3(4)+3(5)\]
{{% /answer %}}
{{% /check %}}

Now let's work in the other direction, turning a large sum into compact summation notation.  If we were to write the series connected to this sequence

\[3, \thinspace 5, \thinspace 7, \thinspace 9, \thinspace 11, \thinspace 13, \thinspace 15, \thinspace 17, \thinspace 19, \thinspace 21, \thinspace 23, \thinspace 25, \thinspace 27, \thinspace 29, \thinspace 31\]

then we would need to write out the sum of all fifteen terms.

\[3+5+7+9+11+13+15+17+19+21+23+25+27+29+31\]

To convert this to summation notation the first thing we need is an equation for the sequence that generates these terms.  The values appear to come from an arithmetic sequence with a starting value of $3$ and a spacing of $2$, so the equation is $a_n=3+2(n-1)=2n+1$.

All that's left is to determine the starting and ending values for $n$.

\[\Large \sum\_{n=?}^{?} (2n+1)\]

It's tempting to use $3$ as the starting value but, because $3=a_1$, we actually need to use $n=1$.  

The same holds true for the final value of $n$.  We don't use $31$ but instead use its location in the sequence, which is $15$.  

Inserting the starting and ending values for $n$ completes our summation notation for this example.

\[\Large \sum\_{n=1}^{15} (2n+1)\]

If we had wanted to skip the first three terms and start our series at $9$ then we would adjust the sigma notation so it begins at $n=4$.  And by changing the number on top of the $\Sigma$ we could end the series at a different term.  This makes summation notation extremely flexible.  

{{% check %}}
1. Write Gauss's series $ \thinspace 1 + 2 + 3 + \cdots + 100 \thinspace $ in summation notation. {{% answer %}}
\[\sum\_{n=1}^{100} n\]
{{% /answer %}}
1.  Adjust your answer above so that the series starts with the tenth term and ends on the 82nd. {{% answer %}}
\[\sum\_{n=10}^{82} n\]
{{% /answer %}}
{{% /check %}}
