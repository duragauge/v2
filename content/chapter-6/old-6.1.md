---
title: "6.1 Systems of Equations"
description:
slug:
image: "car-3075497_1280.jpg"
draft: true
---

{{% imgcap file="/img/chapter-6/car-3075497_1280.jpg" title="Image by Tayeb MEZAHDIA from Pixabay " source="https://pixabay.com/images/id-3075497/" %}}

## Introduction
Many of the images we see in movies, videos, games and in print are created and edited by computer graphics software.  Artists, designers, architects and engineers use computer generated images to make simulations, prototypes, animations, life-like models and stunningly realistic visual effects.

The shapes and surfaces that comprise computer generated images are created by mathematical equations.

In order for these shapes and surfaces to fit together seamlessly and move smoothly their equations often need to satisfy several parameters simultaneously.

Those parameters give us sets of two or more equations which are known as **systems of equations**.  


## Solutions to Systems of Equations
A system of equations is a list of equations that all need to be solved at the same time.  For instance, this is a system of two equations with two unknown values $a$ and $b$.

\[
\begin{align}
a + b &= 10 && \small \text{Equation #1} \newline
2b &= 6  && \small \text{Equation #2} \newline
\end{align}
\]

Solving a system of equations means finding values that satisfy every equation in the system.  

Equation \#2 above implies that $b=3$.  If we combine that with Equation \#1 it appears that $a$ must be $7$.  So the values $a=7$ and $b=3$ are a solution to this system.

{{% check %}}
1.  Is $a=5$, $b=2$ a solution to the system below?
\[
\begin{align}
a - b &= 3 && \small \text{Equation #1} \newline
a + b^2 &= 9 && \small \text{Equation #2} \newline
\end{align}
\] {{% answer %}}
Yes, since both equations are true when $a=5$ and $b=2$.
\[
\begin{align}
5 - 2 &= 3 && \small \text{Equation #1} \newline
5 + (2)^2 &= 9 && \small \text{Equation #2} \newline
\end{align}
\]
{{% /answer %}}
1.  Is $a=1$, $b=10$ a solution to the system below?
\[
\begin{align}
a + b &= 11 && \small \text{Equation #1} \newline
a \cdot b &= 7 && \small \text{Equation #2} \newline
\end{align}
\] {{% answer %}}
No.  If $a=1$ and $b=10$ then only the first equation is true.
\[
\begin{align}
1 + 10 &= 11 && \small \text{Equation #1} \newline
(1)(10) &\ne 7 && \small \text{Equation #2} \newline
\end{align}
\]
{{% /answer %}}
{{% /check %}}


## Methods for Solving Systems
The three most common methods for solving systems are substitution, elimination and matrix methods.

Small systems with just two or three variables can be solved by hand in not too many steps using substitution or elimination, so we will introduce those techniques first.  

Large systems are almost always solved by matrix methods using algorithms running in a calculator or on a computer, especially in applications where the number of unknowns is in the hundreds or thousands.  Obviously, we won't get to anything of that size, but we'll discuss some of the basic ideas that carry over to systems of any size.

Even though most all of the examples we will look at have solutions, it is important to keep in mind that systems do not always have solutions.  

However, generally speaking, the number of equations in a system should match the number of unknown values if we hope to solve the system.  To solve for $6$ values, for instance, you typically need $6$ equations.

We will start with systems of two equations with two variables and move up from there.


## Solve Systems by Substitution
Our first solving method is called **substitution**.  Substitution means replacing one thing with another equivalent object.  Substitution is used throughout all levels of mathematics and, in fact, we've already used it several times.  As a simple example, notice that when we evaluate the function $f(x)=x^2$ for $x=5$ then we *substitute* $5$ for every $x$ in the function.

When working with systems, substitution will involve solving one equation for one variable and then substituting that expression into the other equation.  Since this might be a new technique, we will look at an example.

### Substitution Example - Find an Exponential Function Given 2 Points
Suppose we are asked to find an exponential function $f(x)=a \thinspace b^{x}$ that passes through the points $(1, 12)$ and $(3, 27)$.  There are two values we don't know, $a$ and $b$, so we need a system of two equations.

To turn what we know into a system we need to remember that each point has an $x$ and a $y=f(x)$ coordinate.  Inserting those values into the exponential equation will give us two equations.   

![](/img/chapter-6/substitution_exponential.svg#center)

Those two equations are our system.

\[
\begin{align}
12 &= a  \thinspace  b^{1} && \small \text{Equation #1} \newline
27 &= a  \thinspace  b^{3} && \small \text{Equation #2} \newline
\end{align}
\]

To solve our system by substitution we should first solve one of these equations for one of the unknown values, either $a$ or $b$.  It makes no difference which equation or which value we pick, so look for the one that seems simplest.

Since Equation \#1 has the lower power, let's use it to solve for $a$.

\[
\begin{align}
12 &= a  \thinspace  b^{1} && \small \color{#5fa2ce}{\text{Equation #1}} \newline
\frac{12}{b} & = a  && \small \color{#5fa2ce}{\text{Divide by $b$}} \newline
\end{align}
\]

This next step is the key to substitution.  We take this expression for $a$ and substitute it into the other equation, Equation \#2.

\[
\begin{align}
27 &= a  \thinspace  b^{3} && \small \color{#5fa2ce}{\text{Equation #2}} \newline
27 & = \frac{12}{b}  \thinspace  b^{3}  && \small \color{#5fa2ce}{\text{Substitute $a=\frac{12}{b}$}} \newline
27 & = 12 b^{2}  && \small \color{#5fa2ce}{\text{Simplify powers of $b$}} \newline
\frac{27}{12} &= b^{2}   && \small \color{#5fa2ce}{\text{Divide by 12}} \newline
\frac{9}{4} &= b^{2}   && \small \color{#5fa2ce}{\text{Simplify fraction}} \newline
\pm \sqrt{\frac{9}{4}} &= b   && \small \color{#5fa2ce}{\text{Take $\pm \sqrt{\text{  }}$}} \newline
\pm \frac{3}{2} &= b  && \small \color{#5fa2ce}{\text{Simplify}} \newline
\end{align}
\]

Normally getting two answers could cause a problem, but in this case we know something extra.  We are trying to find the base of an exponential function, and the base of an exponential is never negative.  So the correct value must be $b=\frac{3}{2}$.

This is only half of the solution; we also need to know what $a$ is.  To find that, we'll substitute $b$ back into one of our equations.  As before, either one will work but we'll choose Equation \#1 since it is a bit simpler.

\[
\begin{align}
12 &= a  \thinspace  b^{1} && \small \color{#5fa2ce}{\text{Equation #1}} \newline
12 & = a \frac{3}{2} && \small \color{#5fa2ce}{\text{Substitute $b = \frac{3}{2}$}} \newline
\frac{2}{3} \cdot 12 &= a && \small \color{#5fa2ce}{\text{Multiply by $\frac{2}{3}$}} \newline
8 &= a && \small \color{#5fa2ce}{\text{Simplify}} \newline
\end{align}
\]

Now that we know the values for $a$ and $b$, we can finally say that

\[f(x)=8 \left(\frac{3}{2} \right)^{x}\]

is the exponential function that passes through the points $(1, 12)$ and $(3, 27)$.

{{% check %}}
1. If we had solved Equation \#2 for $a$ at the start, we would have gotten $a = \frac{27}{b^3}$.  Substitute that expression into Equation \#1. {{% answer %}}
\[
\begin{align}
12 &= a  \thinspace  b^{1} && \small \color{#5fa2ce}{\text{Equation #1}} \newline
12 & = \frac{27}{b^3} \cdot b^{1} && \small \color{#5fa2ce}{\text{Substitute $a = \frac{27}{b^3}$}} \newline
12 & = \frac{27}{b^{2}}  && \small \color{#5fa2ce}{\text{Simplify powers of $b$}} \newline
12 b^{2} &= 27   && \small \color{#5fa2ce}{\text{Multiply by $b^2$}} \newline
b^{2} &= \frac{27}{12} && \small \color{#5fa2ce}{\text{Divide by $12$}} \newline
b^{2} &= \frac{9}{4}  && \small \color{#5fa2ce}{\text{Simplify fraction}} \newline
b &= \pm \sqrt{\frac{9}{4}} && \small \color{#5fa2ce}{\text{Take $\pm \sqrt{\text{  }}$}} \newline
b &= \pm \frac{3}{2} && \small \color{#5fa2ce}{\text{Simplify}} \newline
\end{align}
\]
which is the same result we had when using Equation \#1.
{{% /answer %}}

1. Suppose you were looking for a power function through the points $(2, 5)$ and $(6,10)$.  Write the system of equations that would result from inserting the values from those points into the power function format $f(x)=k \thinspace x^{p}$ . {{% answer %}}
\[
\begin{align}
5 &= k \thinspace 2^{p} && \small \text{Equation #1} \newline
10 &= k \thinspace 6^{p} && \small \text{Equation #2}
\end{align}
\] {{% /answer %}}
{{% /check %}}


## Solve Systems by Elimination
Our second technique for solving systems is called **elimination**.  For elimination to work both equations must be written in the same format.  You then try to combine the equation in a way that eliminates one of the parameters.  Let's look at an example.

### Elimination Example - Find a Logarithmic Function Given 2 Points
Suppose we need to find a logarithmic function through the two points $(5, 3)$ and $(20, 9)$.  We'll use the format $f(x)=a+b \ln x$ so that we can use `LnReg` to double check our answer.

As we have done earlier, we begin by substituting the $x$ and $y=f(x)$ coordinates into the equation of our model to generate a system.

\[
\begin{align}
9 &= a+b \ln 20 && \small \text{Equation #1} \newline
3 &= a+b \ln 5 && \small \text{Equation #2}
\end{align}
\]

Notice that if we were to subtract the two equations then $a$ would be eliminated.  That is our elimination step.  

\[
\begin{array}{l r c l}
       & 9 & = &  a+b \ln 20 \newline
      -   & (3 & = & a+b \ln 5 ) \newline
           \hline
           & 6 & = &  b \ln 20 - b \ln 5
\end{array}
\]

The result of the elimination is a new equation that only has $b$ in it.  After we solve this for $b$ we can substitute that value back into one of our equations and find $a$.

\[
\begin{align}
6 &= b \ln 20 - b \ln 5 && \small \color{#5fa2ce}{\text{Original Equation}} \newline
6 &= b \left(\ln 20 - \ln 5 \right) && \small \color{#5fa2ce}{\text{Factor out $b$}} \newline
6 &= b \ln \left(\frac{20}{5} \right) && \small \color{#5fa2ce}{\text{Use Quotient rule for Logs}} \newline
6 &= b \ln 4 && \small \color{#5fa2ce}{\text{Simplify fraction}} \newline
\frac{6}{\ln 4} &= b && \small \color{#5fa2ce}{\text{Divide by $\ln 4$}} \newline
b &\approx 4.328 && \small \color{#5fa2ce}{\text{Decimal approximation}} \newline
\end{align}
\]

The next step is to find $a$ by substituting $b=\frac{6}{\ln 4}$ into one of our equations.  Either equation will work, but we'll pick Equation \#2 since it looks a bit simpler.

\[
\begin{align}
3 &= a+b \ln 5 && \small \color{#5fa2ce}{\text{Equation #2}} \newline
3 &= a + \frac{6}{\ln 4} \cdot \ln 5 && \small \color{#5fa2ce}{\text{Substitute $b = \frac{6}{\ln 4}$}} \newline
3 - \frac{6}{\ln 4} \cdot \ln 5 &= a && \small \color{#5fa2ce}{\text{Subtract $\frac{6}{\ln 4} \cdot \ln 5$}} \newline
a &\approx -3.966 && \small \color{#5fa2ce}{\text{Decimal approximation}} \newline
\end{align}
\]

Now that we have both $a$ and $b$, we can write out our function.  

\[f(x) =  -3.966+4.328 \ln x\]

A quick way to check this is to run logarithmic regression on the limited data set $(5, 3)$ and $(20, 9)$.

![](/img/chapter-6/log_regression_2_points.svg#center)

This gives the same values for $a$ and $b$ and the graph clearly goes through our two points.


## Identify Systems of Linear equations
One of the most powerful tools for solving systems is a matrix method called Gauss-Jordan Elimination, which is programed into most graphing calculators.  

Gauss-Jordan Elimination is designed to solve systems of *linear* equations.  You might assume this means it is only good for finding lines, but that is not the case.

The system we solved a moment ago was actually a linear system, even though the equations came from a logarithmic model.  Let's look at it again.

\[
\begin{align}
9 &= a+b \ln 20 && \small \text{Equation #1} \newline
3 &= a+b \ln 5 && \small \text{Equation #2}
\end{align}
\]

These equations are linear because $a$ and $b$ have a power of $1$ and are combined using only addition.  If the equations had powers/roots or exponents/logs or products of $a$ and $b$ then they would not be linear.  

In our first system the equations came from an exponential model.

\[
\begin{align}
12 &= a  \thinspace  b^{1} && \small \text{Equation #1} \newline
27 &= a  \thinspace  b^{3} && \small \text{Equation #2} \newline
\end{align}
\]

This is a system of *non-linear* equations because $b$ has a power of $3$ in the second equation and because the variables are multiplied together.

{{% check %}}
1.  Is this system linear or non-linear?
\[
\begin{array}{rcl}
y & = & x^2 + 1 \newline
y & = & x^3 + x^2 + 1
\end{array}
\] {{% answer %}}
This is a non-linear system.
{{% /answer %}}
1.  Is this system linear or non-linear?
\[
\begin{array}{rcl}
x - y & = & 4 \newline
2y & = & x \newline
\end{array}
\] {{% answer %}}
This system is linear.
{{% /answer %}}
1.  Is this system linear or non-linear?
\[
\begin{array}{rcl}
\sqrt x + 1 & = & y \newline
x \cdot y & = & 2 \newline
\end{array}
\] {{% answer %}}This is a non-linear system.
{{% /answer %}}
{{% /check %}}


## Converting Between Systems and Matrices
Systems of linear equations are easier to work with if we organize them by sorting the terms with variables on the left and putting the constant terms on the right, like in this example below.

\[
\begin{align}
3x + 4y &= 3 \newline
2x - 3y &= 2
\end{align}
\]

Once the equations are written in the same format we don't really need the variables or the equals sign anymore.  By stripping those away we are left with something called a **augmented matrix**.  In the figure below you can convert a linear system into a matrix and back again.

{{% geogebra ratio="25%" id_1="TIQ57dvm8gydTpfV" id_2="uwdgq9fy" id_m="vmkcyyt2" %}}

The matrix contains the same information as the original system, since knowing where a number is located is enough to tell us if it represents an $x$ or a $y$ or a constant.

{{% check %}}
1. Convert this system of linear equations into an augmented matrix.
\[
\begin{align}
2x + y &= 5 \newline
3x - 2y &= 4
\end{align}
\] {{% answer %}}
$$
\left[
\begin{array}{rr|r}
  2 & 1 & 5 \newline
  3 & -2 & 4
\end{array}\right]
$$ {{% /answer %}}
1. Convert this augmented matrix back to a system of equations.
$$
\left[
\begin{array}{rr|r}
  1 & 2 & 3 \newline
  2 & 0 & 2
\end{array}\right]
$$ {{% answer %}}
\[
\begin{align}
x + 2y &= 3 \newline
2x +0y &= 2
\end{align}
\]
{{% /answer %}}
{{% /check %}}


## Solve 2x2 Systems of Linear Equations with Technology
Once a system is represented by a matrix, we can enter the matrix into a calculator and let it run through all the steps of Gauss-Jordan Elimination for us.

To illustrate how this is done, let's use the system of from the first part of the last Quick Check.

\[
\begin{align}
2x + y &= 5 \newline
3x - 2y &= 4
\end{align}
\]

In matrix form this system becomes

$$
\left[
\begin{array}{rr|r}
  2 & 1 & 5 \newline
  3 & -2 & 4
\end{array}\right]
$$

To enter this matrix into a calculator press the `[2ND]` and `[x^-1]` keys to enter the `MATRIX` menu and choose the `EDIT` tab.

![](/img/chapter-6/matrix_edit.png#center)

At the top change the dimensions to `2 x3`, since our matrix has $2$ rows and $3$ columns, and type in all the values.  It should look like this.

![](/img/chapter-6/2x2_rref_1.png#center)

The next step requires us to go back to the home screen, so press `[2nd]` and `[MODE]` to `QUIT`.  

Then go back into the `MATRIX` menu and this time choose the `MATH` tab.  Scroll down to option `B: rref` and press `[ENTER]`.  That is the command that will run Gauss-Jordan Elimination.

![](/img/chapter-6/2x2_rref_2.png#center)

The `B: rref` command needs to know which matrix to work with, so return to the `MATRIX` menu a third time, stay in the `NAME` tab and press `[ENTER]` to select matrix `1: [A]`.  

![](/img/chapter-6/2x2_rref_3.png#center)

Press `[ENTER]` once again and the calculator will work through Gauss-Jordan Elimination.

![](/img/chapter-6/2x2_rref_4.png#center)

What we get back is a matrix that is in reduced row echelon form, which is why the command is called `rref`.  

$$
\left[
\begin{array}{rr|r}
  1 & 0 & 2 \newline
  0 & 1 & 1
\end{array}\right]
$$

Look what happens when we convert this reduced matrix back into a system.

\[
\begin{align}
x &= 2 \newline
y &= 1
\end{align}
\]

It's now obvious that the solution is $x=2$ and $y=1$.

{{% check %}}
1. What is the solution to the system whose reduced matrix is shown below?
$$
\left[
\begin{array}{rr|r}
  1 & 0 & -3 \newline
  0 & 1 & 4
\end{array}\right]
$$ {{% answer %}}The solution is $x=-3$ and $y=4$.{{% /answer %}}
{{% /check %}}


## Solve Larger Systems of Linear Equations with Technology
When solving a larger system on a calculator, the only thing that will change is the size of the matrix.  For instance, suppose we start with  this system of three linear equations each with three variables.

\[
\begin{array}{r c r c r c r}
3a & + & 2b & - & c & = & 5 \newline
a &  &  & + & 6c & = & 1 \newline
2a & + & b & - & 2c & = & 5 \newline
\end{array}
\]

Even though it has three unknows, $a$, $b$ and $c$, this is still a linear system since none of those unknowns are raised to power/roots, etc. or are multiplying each other.  

The matrix version of our system is

$$
\left[
\begin{array}{rrr|r}
  3 & 2 & -1 & 5 \newline
  1 & 0 & 6 & 1 \newline
  2 & 1 & -2 & 5
\end{array}\right]
$$

Notice that there are $3$ rows, one for each equation, and $4$ columns, one for each of the coefficients and a fourth for the constant.  Also note that when a value is missing from the system we put a $0$ into the matrix at the appropriate location.

Since this matrix has $3$ rows and $4$ columns we change the dimensions to `3 x4`, enter the values and run `rref`.

![](/img/chapter-6/3x3_rref_1.png#center)

We get back a reduced matrix with decimal values.  Sometimes the decimals can be converted to fractions by pressing `[2ND]`, `[MATH]` and choosing `1:Frac`.

![](/img/chapter-6/3x3_rref_2.png#center)

Our reduced matrix is

$$
  \left[\begin{array}{r r r | r}
    1 & 0 & 0 & \frac{11}{3} \newline
    0 & 1 & 0 & \frac{-29}{9} \newline
    0 & 0 & 1 & \frac{-4}{9}
  \end{array}\right]
$$

and the solution must be $a=\frac{11}{3}$, $b=\frac{-29}{9}$ and $c=\frac{-4}{9}$.


{{% check %}}
1. Use a calculator to solve the system below.  Convert your answers to fractions.
\[
\begin{align}
x+2y+3z&=4 \newline
5x+7z&=1 \newline
2x-y+z&=-2
\end{align}
\] {{% answer %}}
The matrix for this system is
\[
  \left[\begin{array}{r r r | r}
    1 & 2 & 3 & 4 \newline
    5 & 0 & 7 & 1 \newline
    2 & -1 & 1 & -2
  \end{array}\right]
\]
Entering this into the calculator and running `rref` gives
![](/img/chapter-6/3x3_rref_check_1.png#center)
Converting to fractions this becomes
![](/img/chapter-6/3x3_rref_check_2.png#center)
so the solution is $x=\frac{-1}{2}$, $y=\frac{3}{2}$ and $z=\frac{1}{2}$.
{{% /answer %}}
{{% /check %}}
