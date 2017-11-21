---
title: "Of Matrices and Men (pt. 2)"
date: 2017-10-22T20:35:21+02:00
draft: true
tags: ["linear algebra", "18.06", "matrices"]
---

In my (put link) last post we saw how a matrix could operate on a vector to produce a result:

\\[ 
\begin{bmatrix}
  1 & 0 & 0 \newline
  -1 & 1 & 0 \newline
  0 & -1 & 1
 \end{bmatrix}
%
\\begin{bmatrix}
 1 \newline
 4 \newline
 9
\\end{bmatrix}
%
&#61;
%
\\begin{bmatrix}
1 \newline
3 \newline
5
\\end{bmatrix}
\\]

The matrix used above is a $3 \times 3$ _difference matrix_. The general form for this type of operation is:

\\[
Ax = b
\\]

From the above equation, you can see that vector $b$ is produced by applying matrix $A$ to vector $x$. This $Ax = b$ is pretty much the central equation of linear algebra.

Say you now know what $b$ is and you wish to recover $x$. That is, given $Ax = b$, which is: 

\\[ 
\begin{bmatrix}
  1 & 0 & 0 \newline
  -1 & 1 & 0 \newline
  0 & -1 & 1
 \end{bmatrix}
%
\\begin{bmatrix}
 x_1 \newline
 x_2 \newline
 x_3
\\end{bmatrix}
%
&#61;
%
\\begin{bmatrix}
 b_1 \newline
 b_2 \newline
 b_3
\\end{bmatrix}
\\]

We can write this out as the system of linear equations which it is:

\\[
\begin{equation}
1 \cdot x_1 + 0 \cdot x_2 + 0 \cdot x_3 = b_1 
\end{equation}
\\]
\\[
\begin{equation}
-1 \cdot x_1 + 1 \cdot x_2 + 0 \cdot x_3 = b_2 
\end{equation}
\\]
\\[
\begin{equation}
0 \cdot x_1 -1 \cdot x_2 + 1 \cdot x_3 = b_3
\end{equation}
\\]
