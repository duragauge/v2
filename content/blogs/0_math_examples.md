---
title: 0.0 Math Examples
description: Testing Math
image: pic10.jpg
noindex: true
draft: true
---

# Using MathJax for $\LaTeX$

## In-line equation

This is a formula $e=mc^2$ and parenthesis of different sizes $( \big( \Big( \bigg( \Bigg( $.  

## Display equation

Plain
$$\sum_{k=1}^{n} \left( \frac{1}{2} \right)^k$$

Boxed
$$\boxed{\pi=\frac c d}$$

## Currency

Hopefully you can use a dollar sign when discussing money:  $2.35.

## Sets

For sets you can try a double backslash before each brace $\\{ \\}$ or use lbrace $\lbrace$ and rbrace $\rbrace$.

$$\lbrace 1, 2, 3 \rbrace$$
$$\\{ 1, 2, 3 \\}$$

## Math inside HTML

{{% answer %}}This should show several equations.  Some inline $\frac{x^3}{8}$ and some as display
$$\sum_{k=1}^{n} \left( \frac{1}{2} \right)^k$$
$$e=mc^2$$
and cool nested parenthesis
$$( \big( \Big( \bigg( \Bigg($$
  {{% /answer %}}

## Aligned equations (inside a div)

Using **align** does not seem to work with KaTeX, but should work with MathJax as long as it is inside of a `<div>`.

<div>
$$\begin{align}
   a&=b+c \\
   d+e&=f
\end{align}$$
</div>

----
Using **aligned** works for KaTeX.

<div>
$$\begin{aligned}
   a&=b+c \\
   d+e&=f
\end{aligned}$$
</div>

Using newline instead of double backslash for new lines does not work for KaTex.

<div>
$$\begin{aligned}
(x+y)^3 &= (x+y)(x+y)^2 \newline
&= (x+y)(x^2+2xy+y^2) \newline
&= x^3+3x^2y+3xy^3+x^3
\end{aligned}$$
</div>


but looks like this using double backslashes


<div>
$$\begin{aligned}
(x+y)^3 &= (x+y)(x+y)^2 \\
&= (x+y)(x^2+2xy+y^2) \\
&= x^3+3x^2y+3xy^3+x^3
\end{aligned}$$
</div>


## Aligned Equation with steps using align and double backslash
<div>
$$\begin{aligned}
  ax^2+bx+c&=0 &&\text{Divide by $a$, the leading coefficient.}&\\[1.25ex]
  x^2+\frac{b}{a}x+\frac{c}{a}&=0 &&\text{Transpose the constant term to the RHS.}&\\[1.25ex]
  x^2+\frac{b}{a}x&=-\frac{c}{a}&&\text{Add $\left(\frac{1}{2}\left(\frac{b}{a}\right)\right)^2$ to both sides.}&\\[1.25ex]
  x^2+\frac{b}{a}x+\frac{b^2}{4a^2}&=-\frac{c}{a}+\frac{b^2}{4a^2}&&\text{Factor the LHS and simplify the RHS.}&\\[1.25ex]
  \left(x+\frac{b}{a}\right)^2&=\frac{b^2-4ac}{4a^2}&&\text{Take the square root of both sides.}&\\[1.25ex]
  x+\frac{b}{a}&=\pm\frac{\sqrt{b^2-4ac}}{2a}&&\text{Solve for $x$.}&\\[1.25ex]
  x&=\frac{-b\pm\sqrt{b^2-4ac}}{2a}&&\text{Quadratic Formula.}&
\end{aligned}$$
</div>
## Aligned Equation with steps using align and double backslash and no 1.25ex multiplier

<div>
$$\begin{aligned}
  ax^2+bx+c&=0 &&\text{Divide by $a$, the leading coefficient.}&\\
  x^2+\frac{b}{a}x+\frac{c}{a}&=0 &&\text{Transpose the constant term to the RHS.}&\\
  x^2+\frac{b}{a}x&=-\frac{c}{a}&&\text{Add $\left(\frac{1}{2}\left(\frac{b}{a}\right)\right)^2$ to both sides.}&\\
  x^2+\frac{b}{a}x+\frac{b^2}{4a^2}&=-\frac{c}{a}+\frac{b^2}{4a^2}&&\text{Factor the LHS and simplify the RHS.}&\\
  \left(x+\frac{b}{a}\right)^2&=\frac{b^2-4ac}{4a^2}&&\text{Take the square root of both sides.}&\\
  x+\frac{b}{a}&=\pm\frac{\sqrt{b^2-4ac}}{2a}&&\text{Solve for $x$.}&\\
  x&=\frac{-b\pm\sqrt{b^2-4ac}}{2a}&&\text{Quadratic Formula.}&
\end{aligned}$$
</div>

## Aligned Equation with steps using align-star and double backslashes
<div>
$$\begin{align*}
  ax^2+bx+c&=0 &&\text{Divide by $a$, the leading coefficient.}&\\
  x^2+\frac{b}{a}x+\frac{c}{a}&=0 &&\text{Transpose the constant term to the RHS.}&\\
  x^2+\frac{b}{a}x&=-\frac{c}{a}&&\text{Add $\left(\frac{1}{2}\left(\frac{b}{a}\right)\right)^2$ to both sides.}&\\
  x^2+\frac{b}{a}x+\frac{b^2}{4a^2}&=-\frac{c}{a}+\frac{b^2}{4a^2}&&\text{Factor the LHS and simplify the RHS.}&\\
  \left(x+\frac{b}{a}\right)^2&=\frac{b^2-4ac}{4a^2}&&\text{Take the square root of both sides.}&\\
  x+\frac{b}{a}&=\pm\frac{\sqrt{b^2-4ac}}{2a}&&\text{Solve for $x$.}&\\
  x&=\frac{-b\pm\sqrt{b^2-4ac}}{2a}&&\text{Quadratic Formula.}&
\end{align*}$$
</div>

## Colors

$\color{red}{e=}\color{blue}{mc}\color{green}{^2}$ using ```\color{}```

----
Using ```\textcolor{}{}```
$$\\{\textcolor{red}{\text{red}},  \textcolor{orange}{\text{orange}},  \textcolor{yellow}{\text{yellow}},  \textcolor{green}{\text{green}},  \textcolor{blue}{\text{blue}},  \textcolor{indigo}{\text{indigo}},  \textcolor{violet}{\text{violet}}\ \\}$$

## Matrices

<div>
$$\begin{pmatrix}
   a & b \\
   c & d
\end{pmatrix}$$
</div>

----

<div>
$$\begin{matrix}
    x_{11} & x_{12} & x_{13} & \dots  & x_{1n} \\
    x_{21} & x_{22} & x_{23} & \dots  & x_{2n} \\
    \vdots & \vdots & \vdots & \ddots & \vdots \\
    x_{d1} & x_{d2} & x_{d3} & \dots  & x_{dn}
\end{matrix}$$
</div>
