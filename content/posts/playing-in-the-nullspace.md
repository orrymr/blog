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



