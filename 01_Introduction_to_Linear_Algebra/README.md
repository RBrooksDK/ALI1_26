---
tags:
    - Linear Systems
    - Matrices
    - Row Reduction
    - Echelon Form
    - Reduced Row Echelon Form
    - Pivots
    - Basic Variables
    - Free Variables
    - Augmented Matrix
    - Vectors
    - Linear Combinations
    - Span
    - Consistency
    - Gaussian Elimination
---
<h1 align="center">Introduction to Linear Algebra</h1>

## Session Material:
Lay: 1.1-1.5 + 1.6. as self-study

[Session Notes](https://drive.google.com/file/d/1RdyO_y_bt37l4Q_Snxpcgs8_5uZW3JTE/view?usp=sharing)

[Session Material](https://viaucdk-my.sharepoint.com/:f:/g/personal/rib_viauc_dk/IgBv700AhGBXQ6TLy1kZVkh2AaJVBG6an8WKXvsvkwXXKxg?e=A3qaPu)

### Session Recording

<div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%; overflow: hidden;">
    <iframe 
        src="https://drive.google.com/file/d/1sOA7Z0JIRklYc3Qs1HKnxIe5scgNWaDY/preview" 
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
        allow="autoplay; encrypted-media" 
        allowfullscreen>
    </iframe>
</div>

---


## Session Description

We'll begin with systems of linear equations, what they are, how to represent them with matrices, and how to solve them using row reduction. You'll learn key row operations, how to reach echelon forms, identify pivots, and determine basic and free variables. We'll cover when systems have unique, infinite, or no solutions, revisiting concepts like Theorem 2.

Next, we introduce vectors: linear combinations, spans, and how vector equations relate to linear systems, with geometric intuition in 2D and 3D.

### Key Concepts

 - Linear Systems
 - Matrices
 - Row Reduction
 - Vectors
 - Span
 - Solutions sets and parametric vector form

!!! tip "Learning Objectives"

    - Identify and represent linear systems using matrices.
    - Apply row reduction techniques to solve linear systems.
    - Describe and construct vectors, spans, and linear combinations.
    - Move from systems of linear equations to vector equations to matrix equations and back again.
    - Solve systems of linear equations and determine the solutions sets in parametric vector form.


---

<!-- 
1.2: 1, 7, 9, 11, 33   
1.3: 11, 13, 14, 28     
1.4: 6, 8, 11, 17, 18​   
1.5: 7, 15, 23, 24 
-->
<style type="text/css">
    ol { list-style-type: lower-alpha; }
</style>

## Exercises

**Exercise 1** (1.2.1)

Determine which matrices are in reduced echelon form and which others are only in echelon form.

1. $\left[\begin{array}{llll}1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 1\end{array}\right]$
2. $\left[\begin{array}{llll}1 & 0 & 1 & 0 \\ 0 & 1 & 1 & 0 \\ 0 & 0 & 0 & 1\end{array}\right]$
3. $\left[\begin{array}{llll}1 & 0 & 0 & 0 \\ 0 & 1 & 1 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 1\end{array}\right]$
4. $\left[\begin{array}{lllll}1 & 1 & 0 & 1 & 1 \\ 0 & 2 & 0 & 2 & 2 \\ 0 & 0 & 0 & 3 & 3 \\ 0 & 0 & 0 & 0 & 4\end{array}\right]$

??? answer "&nbsp;"
    1. Reduced echelon form
    2. Reduced echelon form
    3. Not echelon form
    4. Echelon form

**Exercise 2** (1.2.7)

Find the general solution of the given system.

$\left[\begin{array}{llll}1 & 3 & 4 & 7 \\ 3 & 9 & 7 & 6\end{array}\right]$

??? answer "&nbsp;"
    $$
    \left\{
      \begin{array}{l}
        x_1 = -5 - 3 x_2 \\
        x_2 \text{ is free } \\
        x_3 = 3
      \end{array}
    \right.
    $$

**Exercise 3** (1.2.9)

Find the general solution of the given system.

$\left[\begin{array}{rrrr}0 & 1 & -2 & 3 \\ 1 & -3 & 4 & -6\end{array}\right]$

??? answer "&nbsp;"
    $$
    \left\{
        \begin{array}{l}
            x_1=3+2 x_3 \\
            x_2=3+2 x_3 \\
            x_3 \text { is free }
        \end{array}\right.
    $$

**Exercise 4** (1.2.11)

Find the general solution of the given system.

$\left[\begin{array}{rrrr}3 & -2 & 4 & 0 \\ 9 & -6 & 12 & 0 \\ 6 & -4 & 8 & 0\end{array}\right]$

??? answer "&nbsp;"
    $$
    \left\{
        \begin{array}{l}
            x_1=\frac{2}{3} x_2-\frac{4}{3} x_3 \\
            x_2 \text { is free } \\
            x_3 \text { is free }
        \end{array}\right.
    $$

**Exercise 5** (1.2.33)

Find the interpolating polynomial $p(t)=a_0+a_1 t+a_2 t^2$ for the data $(1,6),(2,15),(3,28)$. That is, find $a_0, a_1$, and $a_2$ such that

$$
\begin{aligned}
& a_0+a_1(1)+a_2(1)^2=6 \\
& a_0+a_1(2)+a_2(2)^2=15 \\
& a_0+a_1(3)+a_2(3)^2=28
\end{aligned}
$$

??? answer "&nbsp;"
    The polynomial is $p(t)=1+3 t+2 t^2$.

**Exercise 6** (1.3.11)

Determine if $\mathbf{b}$ is a linear combination of $\mathbf{a}_1, \mathbf{a}_2$, and $\mathbf{a}_3$.

$\mathbf{a}_1=\left[\begin{array}{r}1 \\ -2 \\ 0\end{array}\right], \mathbf{a}_2=\left[\begin{array}{l}0 \\ 1 \\ 2\end{array}\right], \mathbf{a}_3=\left[\begin{array}{r}5 \\ -6 \\ 8\end{array}\right], \mathbf{b}=\left[\begin{array}{r}2 \\ -1 \\ 6\end{array}\right]$

??? answer "&nbsp;"
    $\mathbf{b}$ is a linear combination of $\mathbf{a}_1, \mathbf{a}_2$, and $\mathbf{a}_3$.

**Exercise 7** (1.3.13)

Determine if $\mathbf{b}$ is a linear combination of the vectors formed from the columns of the matrix $A$.

$A=\left[\begin{array}{rrr}1 & -4 & 2 \\ 0 & 3 & 5 \\ -2 & 8 & -4\end{array}\right], \mathbf{b}=\left[\begin{array}{r}3 \\ -7 \\ -3\end{array}\right]$

??? answer "&nbsp;"
    $\mathbf{b}$ is not a linear combination of the columns of $A$.

**Exercise 8** (1.3.14)

Determine if $\mathbf{b}$ is a linear combination of the vectors formed from the columns of the matrix $A$.

$A=\left[\begin{array}{rrr}1 & 0 & 5 \\ -2 & 1 & -6 \\ 0 & 2 & 8\end{array}\right], \mathbf{b}=\left[\begin{array}{r}2 \\ -1 \\ 6\end{array}\right]$

??? answer "&nbsp;"
    $\mathbf{b}$ is a linear combination of the columns of $A$.

**Exercise 9** (1.3.28)

A steam plant burns two types of coal: anthracite (A) and bituminous (B). For each ton of A burned, the plant produces 27.6 million Btu of heat, 3100 grams (g) of sulfur dioxide, and 250 g of particulate matter (solid-particle pollutants). For each ton of B burned, the plant produces 30.2 million Btu, 6400 g of sulfur dioxide, and 360 g of particulate matter.

1. How much heat does the steam plant produce when it burns $x_1$ tons of A and $x_2$ tons of B ?
2. Suppose the output of the steam plant is described by a vector that lists the amounts of heat, sulfur dioxide, and particulate matter. Express this output as a linear combination of two vectors, assuming that the plant burns $x_1$ tons of A and $x_2$ tons of B .
3. $[\mathbf{M}]$ Over a certain time period, the steam plant produced 162 million Btu of heat, $23,610 \mathrm{~g}$ of sulfur dioxide, and 1623 g of particulate matter. Determine how many tons of each type of coal the steam plant must have burned. Include a vector equation as part of your solution.

??? answer "&nbsp;"
    1. The amount of heat produced when the steam plant burns $x_1$ tons of anthracite and $x_2$ tons of bituminous coal is $27.6 x_1+30.2 x_2$ million Btu.
    2. The total output produced by $x_1$ tons of anthracite and $x_2$ tons of bituminous coal is given by the vector $x_1\left[\begin{array}{c}27.6 \\ 3100 \\ 250\end{array}\right]+x_2\left[\begin{array}{c}30.2 \\ 6400 \\ 360\end{array}\right]$.
    3. The steam plant burned $3.9$ tons of anthracite coal and $1.8$ tons of bituminous coal.

**Exercise 10** (1.4.6)

Use the definition of $A \mathbf{x}$ to write the matrix equation as a vector equation, or vice versa.

6. $\left[\begin{array}{rr}2 & -3 \\ 3 & 2 \\ 8 & -5 \\ -2 & 1\end{array}\right]\left[\begin{array}{r}-3 \\ 5\end{array}\right]=\left[\begin{array}{r}-21 \\ 1 \\ -49 \\ 11\end{array}\right]$

??? answer "&nbsp;"
    $-3 \cdot\left[\begin{array}{r}2 \\ 3 \\ 8 \\ -2\end{array}\right]+5 \cdot\left[\begin{array}{r}-3 \\ 2 \\ -5 \\ 1\end{array}\right]=\left[\begin{array}{r}-21 \\ 1 \\ -49 \\ 11\end{array}\right]$

**Exercise 11** (1.4.8)

Use the definition of $A \mathbf{x}$ to write the matrix equation as a vector equation, or vice versa.

8. $z_1\left[\begin{array}{r}2 \\ -4\end{array}\right]+z_2\left[\begin{array}{r}-1 \\ 5\end{array}\right]+z_3\left[\begin{array}{r}-4 \\ 3\end{array}\right]+z_4\left[\begin{array}{l}0 \\ 2\end{array}\right]=\left[\begin{array}{r}5 \\ 12\end{array}\right]$

??? answer "&nbsp;"
    $\left[\begin{array}{rrrr}2 & -1 & -4 & 0 \\ -4 & 5 & 3 & 2\end{array}\right]\left[\begin{array}{l}z_1 \\ z_2 \\ z_3 \\ z_4\end{array}\right]=\left[\begin{array}{r}5 \\ 12\end{array}\right]$

**Exercise 12** (1.4.11)

Given $A$ and $\mathbf{b}$, write the augmented matrix for the linear system that corresponds to the matrix equation $A \mathbf{x}=\mathbf{b}$. Then solve the system and write the solution as a vector.

$A=\left[\begin{array}{rrr}1 & 3 & -4 \\ 1 & 5 & 2 \\ -3 & -7 & 6\end{array}\right], \mathbf{b}=\left[\begin{array}{r}-2 \\ 4 \\ 12\end{array}\right]$

??? answer "&nbsp;"
    $\mathbf{x}=\left[\begin{array}{l}x_1 \\ x_2 \\ x_3\end{array}\right]=\left[\begin{array}{r}-11 \\ 3 \\ 0\end{array}\right]$

**Exercise 13** (1.4.17, 1.4.18)

$[\mathbf{M}]$  Refer to the matrices $A$ and $B$ below. Make appropriate calculations that justify your answers and mention an appropriate theorem.

$$
A=\left[\begin{array}{rrrr}
1 & 3 & 0 & 3 \\
-1 & -1 & -1 & 1 \\
0 & -4 & 2 & -8 \\
2 & 0 & 3 & -1
\end{array}\right] \quad B=\left[\begin{array}{rrrr}
1 & 4 & 1 & 2 \\
0 & 1 & 3 & -4 \\
0 & 2 & 6 & 7 \\
2 & 9 & 5 & -7
\end{array}\right]
$$

1. How many rows of $A$ contain a pivot position? Does the equation $A \mathbf{x}=\mathbf{b}$ have a solution for each $\mathbf{b}$ in $\mathbb{R}^4$ ?
2. Can every vector in $\mathbb{R}^4$ be written as a linear combination of the columns of the matrix $B$ above? Do the columns of $B$ span $\mathbb{R}^3$ ?

??? answer "&nbsp;"
    1. $A \mathbf{x}=\mathbf{b}$ does not have a solution for each $\mathbf{b}$ in $\mathbb{R}^4$.
    2.  Not all vectors in $\mathbb{R}^4$ can be written as a linear combination of the columns of $B$. The columns of $B$ certainly do not span $\mathbb{R}^3$.

**Exercise 14** (1.5.7)

Describe all solutions of $A \mathbf{x}=\mathbf{0}$ in parametric vector form, where $A$ is row equivalent to the given matrix.

$\left[\begin{array}{llll}1 & 3 & -3 & 7 \\ 0 & 1 & -4 & 5\end{array}\right]$

??? answer "&nbsp;"
    $\mathbf{x}=\left[\begin{array}{l}x_1 \\ x_2 \\ x_3 \\ x_4\end{array}\right]=\left[\begin{array}{c}-9 x_3+8 x_4 \\ 4 x_3-5 x_4 \\ x_3 \\ x_4\end{array}\right]=\left[\begin{array}{c}-9 x_3 \\ 4 x_3 \\ x_3 \\ 0\end{array}\right]+\left[\begin{array}{c}8 x_4 \\ -5 x_4 \\ 0 \\ x_4\end{array}\right]=x_3\left[\begin{array}{r}-9 \\ 4 \\ 1 \\ 0\end{array}\right]+x_4\left[\begin{array}{r}8 \\ -5 \\ 0 \\ 1\end{array}\right]$

**Exercise 15** (1.5.15)

Describe and compare the solution sets of $x_1+5 x_2-$ $3 x_3=0$ and $x_1+5 x_2-3 x_3=-2$.

??? answer "&nbsp;"
    The solution set of the homogeneous equation is the plane through the origin in $\mathbf{R}^3$ spanned by $\mathbf{u}$ and $\mathbf{v}$. The solution set of the nonhomogeneous equation is parallel to this plane and passes through the point $\mathbf{p}=\left[\begin{array}{r}-2 \\ 0 \\ 0\end{array}\right]$.

**Exercise 16** (1.5.23)

Mark each statement True or False. Justify each answer.

1. A homogeneous equation is always consistent.
2. The equation $A \mathbf{x}=\mathbf{0}$ gives an explicit description of its solution set.
3. The homogeneous equation $A \mathbf{x}=\mathbf{0}$ has the trivial solution if and only if the equation has at least one free variable.
4. The equation $\mathbf{x}=\mathbf{p}+t \mathbf{v}$ describes a line through $\mathbf{v}$ parallel to $\mathbf{p}$.
5. The solution set of $A \mathbf{x}=\mathbf{b}$ is the set of all vectors of the form $\mathbf{w}=\mathbf{p}+\mathbf{v}_h$, where $\mathbf{v}_h$ is any solution of the equation $A \mathbf{x}=\mathbf{0}$.

??? answer "&nbsp;"
    1. True. See the first paragraph of the subsection titled Homogeneous Linear Systems.
    2. False. The equation $A \mathbf{x}=\mathbf{0}$ gives an implicit description of its solution set. See the subsection entitled Parametric Vector Form.
    3. False. The equation Ax =0 always has the trivial solution. The box before Example 1 uses the word nontrivial instead of trivial.
    4. False. The line goes through $\mathbf{p}$ parallel to $\mathbf{v}$. See the paragraph that precedes Fig. 5.
    5. False. The solution set could be empty! The statement (from Theorem 6) is true only when there exists a vector $\mathbf{p}$ such that $A \mathbf{p}=\mathbf{b}$.

**Exercise 17** (1.5.24)

Mark each statement True or False. Justify each answer.

1. A homogeneous system of equations can be inconsistent.
2. If $\mathbf{x}$ is a nontrivial solution of $A \mathbf{x}=\mathbf{0}$, then every entry in $\mathbf{x}$ is nonzero.
3. The effect of adding $\mathbf{p}$ to a vector is to move the vector in a direction parallel to $\mathbf{p}$.
4. The equation $A \mathbf{x}=\mathbf{b}$ is homogeneous if the zero vector is a solution.

??? answer "&nbsp;"
    1. False. The trivial solution is always a solution to a homogeneous system of linear equations.
    2. False. A nontrivial solution of $A \mathbf{x}=\mathbf{0}$ is any nonzero $\mathbf{x}$ that satisfies the equation. See the sentence before Example 2.
    3. True. See the paragraph following Example 3.
    4. True. If the zero vector is a solution, then $\mathbf{b}=A \mathbf{x}=A \mathbf{0}=\mathbf{0}$.