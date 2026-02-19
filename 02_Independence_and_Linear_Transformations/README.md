---
tags:
    - Linear Independence
    - Trivial Solution
    - Linear Transformations
    - Matrix Transformations
    - Domain
    - Codomain
    - Range
    - Standard Matrix
    - One-to-one
    - Onto
    - Geometric Transformations
    - Mapping
    - Identity Matrix
    - 
---

<h1 align="center">Independence and Linear Transformations</h1>

## Session Material:

Lay: 1.7-1.9

[Recap and Exercises](https://drive.google.com/file/d/1_aHnlC2IPgOTFjrrnDDP6XUhd8sFX5FK/view?usp=sharing)

[Session Notes](https://drive.google.com/file/d/1iay_Pb-DYwuGgQFLcbb6zguk-qt9FtBm/view?usp=sharing)

[Session Material](https://viaucdk-my.sharepoint.com/:f:/g/personal/rib_viauc_dk/IgD8E9yY5zG2TYxEPAmsTjPqAYdwJC5-9hWMgMukRQfxVlY?e=FQ58l2)

### Session Recording

<div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%; overflow: hidden;">
    <iframe 
        src="https://drive.google.com/file/d/1SUlZFvz54YYPjrx7p3Za5_ev6UDZFJts/preview" 
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
        allow="autoplay; encrypted-media" 
        allowfullscreen>
    </iframe>
</div>

---

## Session Description

In this session, we move from solving static equations to understanding the dynamic behavior of vector sets and matrices. We begin with **Linear Independence**, a cornerstone concept that determines whether a set of vectors contains redundant information. You will learn to identify independence by testing for the trivial solution and understanding how it relates to the presence of pivots in a matrix.

Next, we reframe the matrix $A$ not just as a table of numbers, but as a **Linear Transformation** which isa rule that maps vectors from one space to another. We will explore the geometry of these transformations, visualizing how they rotate, reflect, and shear space. You will learn how to "build" a transformation by constructing its **Standard Matrix** using the unit vectors ($e_1, \dots, e_n$). Finally, we define the properties of **onto** and **one-to-one** mappings, which link back to our fundamental questions of existence and uniqueness.

### Key Concepts

- Linear Independence
- Redundancy and Pivots
- Linear Transformations ($T: \mathbb{R}^n \to \mathbb{R}^m$)
- Domain, Codomain, and Range
- The Standard Matrix
- Geometric Transformations (Rotations, Reflections)
- Onto and One-to-one Mappings

!!! tip "Learning Objectives"

    - Analyze sets of vectors to determine linear independence and identify redundant vectors.
    - Define and interpret linear transformations as mathematical mappings between vector spaces.
    - Construct the standard matrix of a linear transformation using the images of the identity matrix columns.
    - Visualize and describe the geometric effects of transformations like rotations, shears, and reflections.
    - Determine if a transformation is one-to-one or onto based on the pivot positions of its matrix.

## Exercises

<!-- 
1.7: 11, 15-20, 41​​​  
1.8: 3-6, 10  
1.9: 15      
2.1: 1, 2, 10, 13, 40, 41   
2.2: 9, 30, 31, 32   
​2.3: 11, 12, 15, 17  
-->
<style type="text/css">
    ol { list-style-type: lower-alpha; }
</style>

**Exercise 1** (1.7.11)

Find the value(s) of $h$ for which the vectors are linearly dependent. Justify your answer.

$\left[\begin{array}{r}2 \\ -2 \\ 4\end{array}\right],\left[\begin{array}{r}4 \\ -6 \\ 7\end{array}\right],\left[\begin{array}{r}-2 \\ 2 \\ h\end{array}\right]$

??? answer "&nbsp;"
    The vectors are linearly dependent if and only if $h=-4$.

**Exercise 2** (1.7.15-1.7.20)

Determine by inspection whether the vectors in Exercises a-f are linearly independent. Justify each answer.

1. $\left[\begin{array}{l}5 \\ 1\end{array}\right],\left[\begin{array}{l}2 \\ 8\end{array}\right],\left[\begin{array}{l}1 \\ 3\end{array}\right],\left[\begin{array}{r}-1 \\ 7\end{array}\right]$
2. $\left[\begin{array}{r}2 \\ -4 \\ 8\end{array}\right],\left[\begin{array}{r}-3 \\ 6 \\ -12\end{array}\right]$
3. $\left[\begin{array}{r}5 \\ -3 \\ -1\end{array}\right],\left[\begin{array}{l}0 \\ 0 \\ 0\end{array}\right],\left[\begin{array}{r}-7 \\ 2 \\ 4\end{array}\right]$
4. $\left[\begin{array}{l}3 \\ 4\end{array}\right],\left[\begin{array}{r}-1 \\ 5\end{array}\right],\left[\begin{array}{l}3 \\ 5\end{array}\right],\left[\begin{array}{l}7 \\ 1\end{array}\right]$
5. $\left[\begin{array}{r}-8 \\ 12 \\ -4\end{array}\right],\left[\begin{array}{r}2 \\ -3 \\ -1\end{array}\right]$
6. $\left[\begin{array}{r}1 \\ 4 \\ -7\end{array}\right],\left[\begin{array}{r}-2 \\ 5 \\ 3\end{array}\right],\left[\begin{array}{l}0 \\ 0 \\ 0\end{array}\right]$

??? answer "&nbsp;"
    15. The set is linearly dependent, by Theorem 8, because there are four vectors in the set but only two entries in each vector.
    16. The set is linearly dependent because the second vector is $-3 / 2$ times the first vector.
    17. The set is linearly dependent, by Theorem 9, because the list of vectors contains a zero vector.
    18. The set is linearly dependent, by Theorem 8, because there are four vectors in the set but only two entries in each vector.
    19. The set is linearly independent because neither vector is a multiple of the other vector. [Two of the entries in the first vector are -4 times the corresponding entry in the second vector. But this multiple does not work for the third entries.]
    20. The set is linearly dependent, by Theorem 9, because the list of vectors contains a zero vector.

**Exercise 3** (1.7.41)

[M] Use as many columns of $A$ as possible to construct a matrix $B$ with the property that the equation $B \mathbf{x}=\mathbf{0}$ has only the trivial solution. Solve $B \mathbf{x}=\mathbf{0}$ to verify your work.

$A=\left[\begin{array}{rrrrr}3 & -4 & 10 & 7 & -4 \\ -5 & -3 & -7 & -11 & 15 \\ 4 & 3 & 5 & 2 & 1 \\ 8 & -7 & 23 & 4 & 15\end{array}\right]$

??? answer "&nbsp;"
    $$
    B=\left[\begin{array}{rrr}
    3 & -4 & 7 \\
    -5 & -3 & -11 \\
    4 & 3 & 2 \\
    8 & -7 & 4
    \end{array}\right] . \text { Other choices are possible. }
    $$

**Exercise 4** (1.8.3-1.8.6)

In Exercises a-d, with $T$ defined by $T(\mathbf{x})=A \mathbf{x}$, find a vector $\mathbf{x}$ whose image under $T$ is $\mathbf{b}$, and determine whether $\mathbf{x}$ is unique.

1. $A=\left[\begin{array}{rrr}1 & 0 & -3 \\ -3 & 1 & 6 \\ 2 & -2 & -1\end{array}\right], \mathbf{b}=\left[\begin{array}{r}-2 \\ 3 \\ -1\end{array}\right]$
2. $A=\left[\begin{array}{rrr}1 & -2 & 3 \\ 0 & 1 & -3 \\ 2 & -5 & 6\end{array}\right], \mathbf{b}=\left[\begin{array}{l}-6 \\ -4 \\ -5\end{array}\right]$
3. $A=\left[\begin{array}{rrr}1 & -5 & -7 \\ -3 & 7 & 5\end{array}\right], \mathbf{b}=\left[\begin{array}{l}-2 \\ -2\end{array}\right]$
4. $A=\left[\begin{array}{rrr}1 & -3 & 2 \\ 3 & -8 & 8 \\ 0 & 1 & 2 \\ 1 & 0 & 8\end{array}\right], \mathbf{b}=\left[\begin{array}{r}1 \\ 6 \\ 3 \\ 10\end{array}\right]$

??? answer "&nbsp;"
    1. $\mathbf{x}=\left[\begin{array}{l}7 \\ 6 \\ 1\end{array}\right]$, unique solution
    2. $\mathbf{x}=\left[\begin{array}{r}-17 \\ -7 \\ -1\end{array}\right]$, unique solution
    3. The general solution is $\mathbf{x}=\left[\begin{array}{c}x_1 \\ x_2 \\ x_3\end{array}\right]=\left[\begin{array}{c}3-3 x_3 \\ 1-2 x_3 \\ x_3\end{array}\right]=\left[\begin{array}{l}3 \\ 1 \\ 0\end{array}\right]+x_3\left[\begin{array}{r}-3 \\ -2 \\ 1\end{array}\right]$. For a particular solution, one might choose $x_3=0$ and $\mathbf{x}=\left[\begin{array}{l}3 \\ 1 \\ 0\end{array}\right]$.
    4. The general solution is $\mathbf{x}=\left[\begin{array}{c}x_1 \\ x_2 \\ x_3\end{array}\right]=\left[\begin{array}{c}10-8 x_3 \\ 3-2 x_3 \\ x_3\end{array}\right]=\left[\begin{array}{r}10 \\ 3 \\ 0\end{array}\right]+x_3\left[\begin{array}{r}-8 \\ -2 \\ 1\end{array}\right]$. For a particular solution, one might choose $x_3=0$ and $\mathbf{x}=\left[\begin{array}{c}10 \\ 3 \\ 0\end{array}\right]$.

**Exercise 5** (1.8.7)

Let \(A\) be a \(6 \times 5\) matrix. What must \(a\) and \(b\) be in order to define \(T: \mathbb{R}^a \rightarrow \mathbb{R}^b\) by \(T(\mathbf{x})=A \mathbf{x}\) ?

??? answer "&nbsp;"
    \(a = 5\) and \(b = 6\).

**Exercise 6** (1.8.8)

How many rows and columns must a matrix \(A\) have in order to define a mapping from \(\mathbb{R}^5\) into \(\mathbb{R}^7\) by the rule \(T(\mathbf{x})=A \mathbf{x}\) ?

??? answer "&nbsp;"
    \(A\) must have 7 rows and 5 columns.

**Exercise 7** (1.8.9-1.8.12)
Consider the matrix:

$$
A=\left[\begin{array}{rrrr}
3 & 2 & 10 & -6 \\
1 & 0 & 2 & -4 \\
0 & 1 & 2 & 3 \\
1 & 4 & 10 & 8
\end{array}\right]
$$

1. For the matrix above, find all \(\mathbf{x}\) in \(\mathbb{R}^4\) that are mapped into the zero vector by the transformation \(\mathbf{x} \mapsto A \mathbf{x}\) for the given matrix \(A\).
   
    ??? answer "&nbsp;"
        $\left\{\begin{array}{l}x_1=-2 x_3+4 x_4 \\ x_2=-2 x_3-3 x_4 \\ x_3 \text { is free } \\ x_4 \text { is free }\end{array} \quad \quad \mathbf{x}=\left[\begin{array}{c}-2 x_3 \\ -2 x_3 \\ x_3 \\ 0\end{array}\right]+\left[\begin{array}{c}4 x_4 \\ -3 x_4 \\ 0 \\ x_4\end{array}\right]=x_3\left[\begin{array}{r}-2 \\ -2 \\ 1 \\ 0\end{array}\right]+x_4\left[\begin{array}{r}4 \\ -3 \\ 0 \\ 1\end{array}\right]\right.$


2. Let \(\mathbf{b}=\left[\begin{array}{r}-1 \\ 3 \\ -1 \\ 4\end{array}\right]\), and let \(A\) be the matrix above. Is \(\mathbf{b}\) in the range of the linear transformation \(\mathbf{x} \mapsto A \mathbf{x}\) ? Why or why not?

    ??? answer "&nbsp;"
        $\mathbf{b}$ is not in the range of the linear transformation $\mathbf{x} \mapsto A \mathbf{x}$ because the equation $A \mathbf{x}=\mathbf{b}$ has no solution.

**Exercise 8** (1.9.15)

Fill in the missing entries of the matrix, assuming that the equation holds for all values of the variables.

$\left[\begin{array}{lll}? & ? & ? \\ ? & ? & ? \\ ? & ? & ?\end{array}\right]\left[\begin{array}{l}x_1 \\ x_2 \\ x_3\end{array}\right]=\left[\begin{array}{c}2 x_1-4 x_2 \\ x_1-x_3 \\ -x_2+3 x_3\end{array}\right]$

??? answer "&nbsp;"
    By inspection, $\left[\begin{array}{rrr}2 & -4 & 0 \\ 1 & 0 & -1 \\ 0 & -1 & 3\end{array}\right]\left[\begin{array}{l}x_1 \\ x_2 \\ x_3\end{array}\right]=\left[\begin{array}{c}2 x_1-4 x_2 \\ x_1-x_3 \\ -x_2+3 x_3\end{array}\right]$

**Exercise 9** (1.9.37-40)

[M] In Exercises (a)-(d)), let \(T\) be the linear transformation whose standard matrix is given. In Exercises (a)-(b), decide if \(T\) is a one-to-one mapping. In Exercises (&#8203;c)-(d), decide if \(T\) maps \(\mathbb{R}^5\) onto \(\mathbb{R}^5\). Justify your answers.

1. \(\left[\begin{array}{rrrr}-5 & 6 & -5 & -6 \\ 8 & 3 & -3 & 8 \\ 2 & 9 & 5 & -12 \\ -3 & 2 & 7 & -12\end{array}\right]\)
2. \(\left[\begin{array}{rrrr}7 & 5 & 9 & -9 \\ 5 & 6 & 4 & -4 \\ 4 & 8 & 0 & 7 \\ -6 & -6 & 6 & 5\end{array}\right]\)
3. \(\left[\begin{array}{rrrrr}4 & -7 & 3 & 7 & 5 \\ 6 & -8 & 5 & 12 & -8 \\ -7 & 10 & -8 & -9 & 14 \\ 3 & -5 & 4 & 2 & -6 \\ -5 & 6 & -6 & -7 & 3\end{array}\right]\)
4. \(\left[\begin{array}{rrrrr}9 & 43 & 5 & 6 & -1 \\ 14 & 15 & -7 & -5 & 4 \\ -8 & -6 & 12 & -5 & -9 \\ -5 & -6 & -4 & 9 & 8 \\ 13 & 14 & 15 & 3 & 11\end{array}\right]\)

??? answer "&nbsp;"
    1. \(T\) is not a one-to-one mapping.
    2. \(T\) is a one-to-one mapping.
    3. \(T\) does not map \(\mathbb{R}^5\) onto \(\mathbb{R}^5\).
    4. \(T\) maps \(\mathbb{R}^5\) onto \(\mathbb{R}^5\).