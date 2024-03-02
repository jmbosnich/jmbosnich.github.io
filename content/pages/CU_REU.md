---
title: "Searching for a relationship between integer and set partitions"
date: 2023-12-15T20:09:15-06:00
draft: false
math: true
---

## Overview
I was on a small team of undergraduates in the CU Mathematics [REU](https://www.colorado.edu/math/undergraduate-program/summer-research-undergraduate), where we worked on a project in the field of algebraic combinatorics under the mentorship of (then first year PhD student) [Lucas Gagnon](https://sites.google.com/view/lucas-gagnon/home) and Professor [Nathaniel Thiem](https://www.colorado.edu/math/nathaniel-thiem). 

The problem that we attempted to solve was this: *given a positive integer $n$, can we find a relationship between the integer partitions of $n$ and the set partitions of a set with $n$ elements.*

## Technical Overview
Let's start with some definitions.

(Def 1) An **integer partition** of a positive integer $n$ is a non-increasing sequence of positive integers $\lambda_1, \lambda_2, \ldots, \lambda_k$ whose sum is $n$, i.e., $\sum_{i=1}^k \lambda_i = n$.

*Example*: the integer partitions of $n=4$ are: $(1,1,1,1), (2,1,1), (2,2), (3,1), (4)$

(Def 2) A **set partition** of a set $X = \\{1, 2, \ldots, n\\}$ is a set of non-empty subsets of $X$ such that every element of $X$ is an element of only one of these subsets.

*Example*: the set partitions of $X = \\{1, 2, 3\\}$ are: $\\{ \\{1 \\}, \\{2 \\}, \\{ 3\\}\\}, \\{\\{1,2 \\}, \\{3 \\} \\}, \\{\\{ 1,3\\}, \\{2 \\} \\}, \\{\\{2, 3 \\}, \\{1 \\} \\}, \\{1,2,3 \\}$

The general question we were trying to answer was: *can we find an (algebraic) relationship between these two notions of partitioning*? To search for this algebraic relationship, we first encoded integer and set paritions as equivalence classes of particular matrices. But first, a few more definitions.

(Def 3) An **equivalence relation** $\sim$ on a set $X$ is a binary relation satisfying the following properties:
* (Reflexivity) for all $a \in X$, $a \sim a$
* (Symmertry) for all $a, b \in X$, $a \sim b \implies b \sim a$
* (Transitivity) for all $a, b, c \in X$, $a \sim b$ and $b \sim c \implies a \sim c$ 

(Def 4) An **equivalence class** is a subset $Y \subset X$ such that $a \sim b$ for all $a, b \in Y$. 

(Def 4) An $n \times n$ **unit triangular matrix** is a triangular diagonal matrix where all of the diagonal elements are equal to one.

Example:$$ \begin{pmatrix}
1 & * & * & * \\\ 0 & 1 & * & * \\\ 0 & 0 & 1 & * \\\ 0 & 0 & 0 & 1
\end{pmatrix},$$
where the * entries can be any real number.

(Def 4) Two $n \times n$ matrices $A$, $B$ are called **similar** if there exists an $n \times n$ matrix $P$ such that $B = P^{-1}AP$. Note that the transformation $A \mapsto P^{-1}AP$ is called a conjugation of $A$ by $P$, and so similar matrices $A$ and $B$ are also called **conjugate**. Finally, similarity/conjugacy is an equivalence relation on the set of all $n \times n$ matrices, and its associated equivalence class is called the **conjugacy class**.

Now we have enough building blocks to discuss our algebraic formulation of the problem.

## The Algebraic Approach
We introduce two classes of unit triangular matrices over some 


Now, that we have our integer and set partitions encoded into classes of matrices, we can make precise what we mean by the relationship between them, which is to ask when these matrices are similar.

## Concluding Remarks
Lucas was the one who did the vast majority of the work on this project, and while the majority of it went right over my head, it was super fun being able to see graduate mathematics research in action. Lucas confided in us that he was trying to impress Nat so that he would supervise his PhD, and that's exactly what ended up happening. Lucas received his PhD under Nat in 2022, and is now a post-doc at York University. All of this is to say, if you think this a super cool project and want to know more about it and its solution, you should definitly reach out to Lucas.
