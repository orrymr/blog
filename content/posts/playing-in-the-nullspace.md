---
title: "Playing in the Nullspace"
date: 2018-03-01T20:35:21+02:00
draft: true
tags: ["linear algebra", "18.06", "matrices", "nullspace"]
---

Have a look at this matrix:

\\[ 
A
%
&#61;
%
 \begin{bmatrix}
  1 & 1 & 2 & 3 \newline
  2 & 2 & 8 & 10 \newline
  3 & 3 & 10 & 13
 \end{bmatrix} 
\\]

We're interested in finding its nullspace: that is, all vectors such that when we multiply them by our matrix $A$, we get 0. Well, the zero vector, $ \begin{bmatrix} 0 \newline 0 \newline 0 \end{bmatrix} $.
I happen to know that $ \begin{bmatrix} -3 \newline 1 \newline -2 \newline 2 \end{bmatrix} $ is one such vector:

\\[
\begin{bmatrix}
  1 & 1 & 2 & 3 \newline
  2 & 2 & 8 & 10 \newline
  3 & 3 & 10 & 13
 \end{bmatrix}
%
\begin{bmatrix}
 -3 \newline
 1 \newline
 -2 \newline
 2
\end{bmatrix}
%
&#61;
%
%
\begin{bmatrix}
 -3 + 1 - 4 + 6 \newline
 -6 + 2 - 16 + 20 \newline
 -9 + 3 - 20 + 26
\end{bmatrix}
%
&#61;
%
\begin{bmatrix}
 0 \newline
 0 \newline
 0
\end{bmatrix}
\\]

What I'm going to describe is a systematic way by which to find all such vectors which will produce the zero vector; ie, I'll describe how to find the nullspace.
How we'll do this is by:

1. Using elimination to find our pivots
2. using back substitution to find our solutions

By elimination, we obtain the following matrix $U$:

\\[ 
U
%
&#61;
%
 \begin{bmatrix}
  1 & 1 & 2 & 3 \newline
  0 & 0 & 4 & 4 \newline
  0 & 0 & 0 & 0
 \end{bmatrix} 
\\]

Our pivot variables are $x_1$ and $x_3$ (since columns 1 and 3 contain pivots). Our free variables are $x_2$ and $x_4$ (since columns 2 and 4 have no pivots).

Note that there are 4 variables in total. This is because the nullspace vectors are in $\mathbb{R}^4$ in this case, since $A$ (and $U$) are $3 \times 4$ matrices. 

We now use back-substitution to find our __special solutions__ which we'll eventually use to yield a __complete solution__.

We can give $x_2$ and $x_4$, our free variables, any values we wish. Then back-substitution finds out pivot variables. The simples choice for our free variables are ones and zeroes.

Looking back to our matrix $U$, we can create equations out of our rows:

$x_1 + x_2 + 2x_3 + 3x_4 = 0$ 

$4x_3 + 4x_4 = 0$

We then set $x_2 = 1$ and $x_4 = 0$. Using back-substitution we get:

$x_3 = 0$

$x_1 = -1$

Next, we set $x_2 = 0$ and $x_4 = 1$. Again, using back-substitution we get:

$x_3 = -1$

$x_1 = -1$

Since we had 2 free variables, we get 2 special solutions:

$ \begin{bmatrix} -1 \newline 1 \newline 0 \newline 0 \end{bmatrix} $ and $ \begin{bmatrix} -1 \newline 0 \newline -1 \newline 1 \end{bmatrix} $.

These two special solutions are _in the nullspace_. Crucially - ___every combination of our special solutions is in the nullspace___. 