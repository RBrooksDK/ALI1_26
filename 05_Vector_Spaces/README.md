<h1 align="center">Vector Spaces</h1>

## Session Material:

[Recap and Exercises](https://drive.google.com/file/d/1aV4KGTyLo9xG6Nggc-_ITgNbp0LL-_XC/view?usp=sharing)

[Session Notes](https://drive.google.com/file/d/1xAHL9RSgd2lWDU-LaGRtwrbEG9U78h9m/view?usp=sharing)

[Session Material](https://viaucdk-my.sharepoint.com/:f:/g/personal/rib_viauc_dk/EgXzFwcFf_tBh8mwVvN0UycBh_gTnjRq8A5x15bFaLKCTg?e=eGwSEq)

---

## Session Description
Moving beyond just vectors in $\mathbb{R}^n$, this session introduces the more general idea of "vector spaces" – abstract collections of objects that behave like vectors. We'll look at special subsets within these spaces called "subspaces." A major focus will be on two important subspaces connected to any matrix: the "Null Space" (all the vectors that get mapped to zero) and the "Column Space" (everything that can be reached by combining the matrix's columns). We'll also touch on how these relate to linear transformations.

A crucial concept we'll build up to is finding the most efficient way to describe or generate a space – this leads us to the idea of a "basis," which is a minimal set of vectors that spans the entire space and is linearly independent. Once we have a basis, we can define unique "coordinate systems" within the space. We'll then use the basis to define the "dimension" of a vector space – essentially, how many independent directions you need to move within it. Finally, we'll define the "rank" of a matrix, which is closely tied to the dimension of its column space and tells us a lot about the structure of the matrix and related linear systems.

### Key Concepts

* Vector Spaces
* Subspaces
* Null Space
* Column Space
* Basis
* Coordinate Systems
* Dimension
* Rank

!!! tip "Learning Objectives"

    - Define and identify vector spaces and subspaces.
    - Determine and construct the null space and column space of a matrix.
    - Construct and use a basis to describe vector spaces and coordinate systems.
    - Calculate the dimension and rank of vector spaces and matrices.
    - Analyze the relationship between basis, dimension, and solutions to linear systems.

## Exercises

<!--
4.2.: 2-6, 17-20, 24
4.3.: 9-10, 13, 17, 18, 36        
4.5: 6, 11, 14, 17      
4.6: 2, 4, 35     
-->
<style type="text/css">
    ol { list-style-type: lower-alpha; }
</style>

**Exercise 1** (4.2.2)

Determine if $w=\left[\begin{array}{r}1 \\ -1 \\ 1\end{array}\right]$ is in $\operatorname{Nul} A$, where

$$
A=\left[\begin{array}{rrr}
2 & 6 & 4 \\
-3 & 2 & 5 \\
-5 & -4 & 1
\end{array}\right]
$$


??? answer "&nbsp;"
    $\mathbf{w}$ is in $\operatorname{Nul} A$

**Exercise 2** (4.2.3-4.2.6)

In the following exercises, find an explicit description of Nul A, by listing vectors that span the null space.

3. $A=\left[\begin{array}{rrrr}1 & 2 & 4 & 0 \\ 0 & 1 & 3 & -2\end{array}\right]$
4. $A=\left[\begin{array}{rrrr}1 & -3 & 2 & 0 \\ 0 & 0 & 3 & 0\end{array}\right]$
5. $A=\left[\begin{array}{rrrrr}1 & -4 & 0 & 2 & 0 \\ 0 & 0 & 1 & -5 & 0 \\ 0 & 0 & 0 & 0 & 2\end{array}\right]$
6. $A=\left[\begin{array}{rrrrr}1 & 3 & -4 & -3 & 1 \\ 0 & 1 & -3 & 1 & 0 \\ 0 & 0 & 0 & 0 & 0\end{array}\right]$

??? answer "&nbsp;"
    3. $\left\{\left[\begin{array}{r}2 \\ -3 \\ 1 \\ 0\end{array}\right],\left[\begin{array}{r}-4 \\ 2 \\ 0 \\ 1\end{array}\right]\right\}$
    4. $\left\{\left[\begin{array}{l}3 \\ 1 \\ 0 \\ 0\end{array}\right],\left[\begin{array}{l}0 \\ 0 \\ 0 \\ 1\end{array}\right]\right\}$
    5. $\left\{\left[\begin{array}{l}4 \\ 1 \\ 0 \\ 0 \\ 0\end{array}\right],\left[\begin{array}{r}-2 \\ 0 \\ 5 \\ 1 \\ 0\end{array}\right]\right\}$
    6. $\left\{\left[\begin{array}{r}-5 \\ 3 \\ 1 \\ 0 \\ 0\end{array}\right],\left[\begin{array}{r}6 \\ -1 \\ 0 \\ 1 \\ 0\end{array}\right],\left[\begin{array}{r}-1 \\ 0 \\ 0 \\ 0 \\ 1\end{array}\right]\right\}$

**Exercise 3** (4.2.17-4.2.20)

For the matrices in the following exercises, (a) find $k$ such that $\mathrm{Nul} A$ is a subspace of $\mathbb{R}^k$, and (b) find $k$ such that $\operatorname{Col} A$ is a subspace of $\mathbb{R}^k$.

17. $A=\left[\begin{array}{rr}6 & -4 \\ -3 & 2 \\ -9 & 6 \\ 9 & -6\end{array}\right]$
18. $A=\left[\begin{array}{rrr}5 & -2 & 3 \\ -1 & 0 & -1 \\ 0 & -2 & -2 \\ -5 & 7 & 2\end{array}\right]$
19. $A=\left[\begin{array}{rrrrr}4 & 5 & -2 & 6 & 0 \\ 1 & 1 & 0 & 1 & 0\end{array}\right]$
20. $A=\left[\begin{array}{lllll}1 & -3 & 2 & 0 & -5\end{array}\right]$

??? answer "&nbsp;"
    17. The matrix $A$ is a $4 \times 2$ matrix. Thus
        (a) $\operatorname{Nul} A$ is a subspace of $\mathbb{R}^2$, and
        (b) $\operatorname{Col} A$ is a subspace of $\mathbb{R}^4$.
    18. The matrix $A$ is a $4 \times 3$ matrix. Thus
        (a) $\operatorname{Nul} A$ is a subspace of $\mathbb{R}^3$, and
        (b) $\operatorname{Col} A$ is a subspace of $\mathbb{R}^4$.
    19. The matrix $A$ is a $2 \times 5$ matrix. Thus
        (a) $\operatorname{Nul} A$ is a subspace of $\mathbb{R}^5$, and
        (b) $\operatorname{Col} A$ is a subspace of $\mathbb{R}^2$.
    20. The matrix $A$ is a $1 \times 5$ matrix. Thus
        (a) $\operatorname{Nul} A$ is a subspace of $\mathbb{R}^5$, and
        (b) $\operatorname{Col} A$ is a subspace of $\mathbb{R}^1=\mathbb{R}$.

**Exercise 4** (4.2.24)

Let $A=\left[\begin{array}{rrrr}10 & -8 & -2 & -2 \\ 0 & 2 & 2 & -2 \\ 1 & -1 & 6 & 0 \\ 1 & 1 & 0 & -2\end{array}\right]$ and $\mathbf{w}=\left[\begin{array}{l}2 \\ 2 \\ 0 \\ 2\end{array}\right]$. Determine if $\mathbf{w}$ is in $\operatorname{Col} A$. Is $\mathbf{w}$ in $\operatorname{Nul} A$ ?

??? answer "&nbsp;"
    $\mathbf{w}$ is in $\operatorname{Nul} A$

**Exercise 5** (4.3.9-4.3.10)

Find bases for the null spaces of the given matrices. Refer to the remarks that follow Example 3 in Section 4.2.

9. $\left[\begin{array}{rrrr}1 & 0 & -2 & -2 \\ 0 & 1 & 1 & 4 \\ 3 & -1 & -7 & 3\end{array}\right]$
10. $\left[\begin{array}{rrrrr}1 & 1 & -2 & 1 & 5 \\ 0 & 1 & 0 & -1 & -2 \\ 0 & 0 & -8 & 0 & 16\end{array}\right]$

??? answer "&nbsp;"
    9. $\left\{\left[\begin{array}{r}2 \\ -1 \\ 1 \\ 0\end{array}\right]\right\}$
    10. $\left\{\left[\begin{array}{r}-2 \\ 1 \\ 0 \\ 1 \\ 0\end{array}\right],\left[\begin{array}{r}9 \\ -10 \\ 2 \\ 0 \\ 1\end{array}\right]\right\}$

**Exercise 6** (4.3.13)

Assume that $A$ is row equivalent to $B$. Find the base for $\operatorname{Nul} A$ and $\operatorname{Col} A$.

$A=\left[\begin{array}{rrrr}-2 & 4 & -2 & -4 \\ 2 & -6 & -3 & 1 \\ -3 & 8 & 2 & -3\end{array}\right], B=\left[\begin{array}{llll}1 & 0 & 6 & 5 \\ 0 & 2 & 5 & 3 \\ 0 & 0 & 0 & 0\end{array}\right]$

??? answer "&nbsp;"
    $\left\{\left[\begin{array}{r}-6 \\ -5 / 2 \\ 1 \\ 0\end{array}\right],\left[\begin{array}{r}-5 \\ -3 / 2 \\ 0 \\ 1\end{array}\right]\right\}$

**Exercise 7** (4.3.17-4.3.18)

Find a basis for the space spanned by the given vectors, $\mathbf{v}_1, \ldots, \mathbf{v}_5$.

17. $[\mathbf{M}]\left[\begin{array}{r}2 \\ 0 \\ -4 \\ -6 \\ 0\end{array}\right],\left[\begin{array}{r}4 \\ 0 \\ 2 \\ -4 \\ 4\end{array}\right],\left[\begin{array}{r}-2 \\ -4 \\ 0 \\ 1 \\ -7\end{array}\right],\left[\begin{array}{r}8 \\ 4 \\ 8 \\ -3 \\ 15\end{array}\right],\left[\begin{array}{r}-8 \\ 4 \\ 0 \\ 0 \\ 1\end{array}\right]$
18. $[\mathbf{M}]\left[\begin{array}{r}-3 \\ 2 \\ 6 \\ 0 \\ -7\end{array}\right],\left[\begin{array}{r}3 \\ 0 \\ -9 \\ 0 \\ 6\end{array}\right],\left[\begin{array}{r}0 \\ 2 \\ -4 \\ 0 \\ -1\end{array}\right],\left[\begin{array}{r}6 \\ -2 \\ -14 \\ 0 \\ 13\end{array}\right],\left[\begin{array}{r}-6 \\ 3 \\ 0 \\ -1 \\ 0\end{array}\right]$

??? answer "&nbsp;"
    17. $\left\{\left[\begin{array}{r}2 \\ 0 \\ -4 \\ -6 \\ 0\end{array}\right],\left[\begin{array}{r}4 \\ 0 \\ 2 \\ -4 \\ 4\end{array}\right],\left[\begin{array}{r}-2 \\ -4 \\ 0 \\ 1 \\ -7\end{array}\right],\left[\begin{array}{r}-8 \\ 4 \\ 0 \\ 0 \\ 1\end{array}\right]\right\}$
    18. $\left\{\left[\begin{array}{r}-3 \\ 2 \\ 6 \\ 0 \\ -7\end{array}\right],\left[\begin{array}{r}3 \\ 0 \\ -9 \\ 0 \\ 6\end{array}\right],\left[\begin{array}{r}0 \\ 2 \\ -4 \\ 0 \\ -1\end{array}\right],\left[\begin{array}{r}-6 \\ 3 \\ 0 \\ -1 \\ 0\end{array}\right]\right\}$

**Exercise 8** (4.3.36)

[M] Let $H=\operatorname{Span}\left\{\mathbf{u}_1, \mathbf{u}_2, \mathbf{u}_3\right\}$ and $K=\operatorname{Span}\left\{\mathbf{v}_1, \mathbf{v}_2, \mathbf{v}_3\right\}$, where

$$
\begin{aligned}
\mathbf{u}_1 &= \begin{bmatrix}1\\2\\0\\-1\end{bmatrix}, &
\mathbf{u}_2 &= \begin{bmatrix}0\\2\\-1\\1\end{bmatrix}, &
\mathbf{u}_3 &= \begin{bmatrix}3\\4\\1\\-4\end{bmatrix},\\
\mathbf{v}_1 &= \begin{bmatrix}-2\\-2\\-1\\3\end{bmatrix}, &
\mathbf{v}_2 &= \begin{bmatrix}2\\3\\2\\-6\end{bmatrix}, &
\mathbf{v}_3 &= \begin{bmatrix}-1\\4\\6\\-2\end{bmatrix}.
\end{aligned}
$$


Find bases for $H, K$, and $H+K$. (See Exercises 33 and 34 in Section 4.1.)

??? answer "&nbsp;"
    $\left\{\mathbf{u}_1, \mathbf{u}_2\right\}$ is a basis for $H$

    $\left\{\mathbf{v}_1, \mathbf{v}_2, \mathbf{v}_3\right\}$ is a basis for $K$

    $\left\{\mathbf{u}_1, \mathbf{u}_2, \mathbf{v}_2, \mathbf{v}_3\right\}$ is a basis for $H+K$

**Exercise 9** (4.5.6)

1. find a basis for this subspace, and 
2. state the dimension.

$\left\{\left[\begin{array}{c}3 a-c \\ -b-3 c \\ -7 a+6 b+5 c \\ -3 a+c\end{array}\right]: a, b, c\right.$ in $\left.\mathbb{R}\right\}$

??? answer "&nbsp;"
    $\left\{\mathbf{v}_1, \mathbf{v}_2, \mathbf{v}_3\right\}$ is linearly independent and is thus a basis for $H$. Hence the dimension of $H$ is 3.

**Exercise 10** (4.5.11)

Find the dimension of the subspace spanned by the given vectors.

$\left[\begin{array}{l}1 \\ 0 \\ 2\end{array}\right],\left[\begin{array}{l}3 \\ 1 \\ 1\end{array}\right],\left[\begin{array}{r}-2 \\ -1 \\ 1\end{array}\right],\left[\begin{array}{l}5 \\ 2 \\ 2\end{array}\right]$

??? answer "&nbsp;"
    3

**Exercise 11** (4.5.14, 4.5.17)

Determine the dimensions of $\operatorname{Nul} A$ and $\operatorname{Col} A$ for the following matricies.

14. $A=\left[\begin{array}{rrrrrrr}1 & 2 & -4 & 3 & -2 & 6 & 0 \\ 0 & 0 & 0 & 1 & 0 & -3 & 7 \\ 0 & 0 & 0 & 0 & 1 & 4 & -2 \\ 0 & 0 & 0 & 0 & 0 & 0 & 1\end{array}\right]$
17. $A=\left[\begin{array}{rrr}1 & -1 & 0 \\ 0 & 1 & 3 \\ 0 & 0 & 1\end{array}\right]$

??? answer "&nbsp;"
    14. The matrix $A$ is in echelon form. There are four pivot columns, so the dimension of $\operatorname{Col} A$ is 4 . There are three columns without pivots, so the equation $A \mathbf{x}=\mathbf{0}$ has three free variables. Thus the dimension of $\operatorname{Nul} A$ is 3 .
    17. The matrix $A$ is in echelon form. There are three pivot columns, so the dimension of $\operatorname{Col} A$ is 3 . There are no columns without pivots, so the equation $A \mathbf{x}=\mathbf{0}$ has only the trivial solution $\mathbf{0}$. Thus Nul $A=\{\mathbf{0}\}$, and the dimension of $\operatorname{Nul} A$ is 0.

**Exercise 12** (4.6.2, 4.6.4)

Assume that the matrix $A$ is row equivalent to $B$. Without calculations, list $\operatorname{rank} A$ and $\operatorname{dim} \operatorname{Nul} A$. Then find bases for $\operatorname{Col} A, \operatorname{Row} A$, and $\operatorname{Nul} A$.

2. $\begin{aligned} A & =\left[\begin{array}{rrrrr}1 & 3 & 4 & -1 & 2 \\ 2 & 6 & 6 & 0 & -3 \\ 3 & 9 & 3 & 6 & -3 \\ 3 & 9 & 0 & 9 & 0\end{array}\right], \\ B & =\left[\begin{array}{rrrrr}1 & 3 & 4 & -1 & 2 \\ 0 & 0 & 1 & -1 & 1 \\ 0 & 0 & 0 & 0 & -5 \\ 0 & 0 & 0 & 0 & 0\end{array}\right],\end{aligned}$
4. $\begin{aligned} A & =\left[\begin{array}{rrrrrr}1 & 1 & -2 & 0 & 1 & -2 \\ 1 & 2 & -3 & 0 & -2 & -3 \\ 1 & -1 & 0 & 0 & 1 & 6 \\ 1 & -2 & 2 & 1 & -3 & 0 \\ 1 & -2 & 1 & 0 & 2 & -1\end{array}\right], \\ B & =\left[\begin{array}{rrrrrr}1 & 1 & -2 & 0 & 1 & -2 \\ 0 & 1 & -1 & 0 & -3 & -1 \\ 0 & 0 & 1 & 1 & -13 & -1 \\ 0 & 0 & 0 & 0 & 1 & -1 \\ 0 & 0 & 0 & 0 & 0 & 1\end{array}\right]\end{aligned}$

??? answer "&nbsp;"
    2. 
        The matrix $B$ is in echelon form. There are three pivot columns, so the dimension of $\operatorname{Col} A$ is 3 . There are three pivot rows, so the dimension of Row $A$ is 3 . There are two columns without pivots, so the equation $A \mathbf{x}=\mathbf{0}$ has two free variables. Thus the dimension of $\operatorname{Nul} A$ is 2 . A basis for $\operatorname{Col} A$ is the pivot columns of $A$ :

        $\left\{\left[\begin{array}{l}1 \\ 2 \\ 3 \\ 3\end{array}\right],\left[\begin{array}{l}4 \\ 6 \\ 3 \\ 0\end{array}\right],\left[\begin{array}{r}2 \\ -3 \\ -3 \\ 0\end{array}\right]\right\}$

        A basis for Row $A$ is the pivot rows of $B:\{(1,3,4,-1,2),(0,0,1,-1,1),(0,0,0,0,-5)\}$.

        A basis for $\operatorname{Nul} A$ is $\left\{\left[\begin{array}{r}-3 \\ 1 \\ 0 \\ 0 \\ 0\end{array}\right],\left[\begin{array}{r}-3 \\ 0 \\ 1 \\ 1 \\ 0\end{array}\right]\right\}$
    
    4. 

        The matrix $B$ is in echelon form. There are five pivot columns, so the dimension of $\operatorname{Col} A$ is 5 . There are five pivot rows, so the dimension of Row $A$ is 5 . There is one column without a pivot, so the equation $A \mathbf{x}=\mathbf{0}$ has one free variable. Thus the dimension of $\operatorname{Nul} A$ is 1 . A basis for $\operatorname{Col} A$ is the pivot columns of $A$ :

        $\left\{\left[\begin{array}{l}1 \\ 1 \\ 1 \\ 1 \\ 1\end{array}\right],\left[\begin{array}{r}1 \\ 2 \\ -1 \\ -2 \\ -2\end{array}\right],\left[\begin{array}{r}-2 \\ -3 \\ 0 \\ 2 \\ 1\end{array}\right],\left[\begin{array}{r}1 \\ -2 \\ 1 \\ -3 \\ 2\end{array}\right],\left[\begin{array}{r}-2 \\ -3 \\ 6 \\ 0 \\ -1\end{array}\right]\right\}$

        A basis for Row $A$ is the pivot rows of $B$ : $\{(1,1,-2,0,1,-2),(0,1,-1,0,-3,-1),(0,0,1,1,-13,-1),(0,0,0,0,1,-1),(0,0,0,0,0,1)\}$

        Thus a basis for $\operatorname{Nul} A$ is

        $\left\{\left[\begin{array}{r}-1 \\ -1 \\ -1 \\ 1 \\ 0 \\ 0\end{array}\right]\right\}$
        

**Exercise 13** (4.6.35)

[M] Let $A=\left[\begin{array}{rrrrrrr}7 & -9 & -4 & 5 & 3 & -3 & -7 \\ -4 & 6 & 7 & -2 & -6 & -5 & 5 \\ 5 & -7 & -6 & 5 & -6 & 2 & 8 \\ -3 & 5 & 8 & -1 & -7 & -4 & 8 \\ 6 & -8 & -5 & 4 & 4 & 9 & 3\end{array}\right]$.

1. Construct matrices $C$ and $N$ whose columns are bases for $\operatorname{Col} A$ and $\operatorname{Nul} A$, respectively, and construct a matrix $R$ whose rows form a basis for Row $A$.
2. Construct a matrix $M$ whose columns form a basis for $\operatorname{Nul} A^T$, form the matrices $S=\left[\begin{array}{ll}R^T & N\end{array}\right]$ and $T=\left[\begin{array}{ll}C & M\end{array}\right]$, and explain why $S$ and $T$ should be square. Verify that both $S$ and $T$ are invertible.

??? answer "&nbsp;"
    1. 

        $C=\left[\begin{array}{rrrr}7 & -9 & 5 & -3 \\ -4 & 6 & -2 & -5 \\ 5 & -7 & 5 & 2 \\ -3 & 5 & -1 & -4 \\ 6 & -8 & 4 & 9\end{array}\right]$.

        $R=\left[\begin{array}{rrrrrrr}1 & 0 & 13 / 2 & 0 & 5 & 0 & -3 \\ 0 & 1 & 11 / 2 & 0 & 1 / 2 & 0 & 2 \\ 0 & 0 & 0 & 1 & -11 / 2 & 0 & 7 \\ 0 & 0 & 0 & 0 & 0 & 1 & 1\end{array}\right]$.
        
        $N=\left[\begin{array}{rrr}-13 / 2 & -5 & 3 \\ -11 / 2 & -1 / 2 & -2 \\ 1 & 0 & 0 \\ 0 & 11 / 2 & -7 \\ 0 & 1 & 0 \\ 0 & 0 & -1 \\ 0 & 0 & 1\end{array}\right]$.

    2. 

        $M=\left[\begin{array}{r}2 / 11 \\ 41 / 11 \\ 0 \\ -28 / 11 \\ 1\end{array}\right]$

        The matrix $S=\left[\begin{array}{ll}R^T & N\end{array}\right]$ is $7 \times 7$ because the columns of $R^T$ and $N$ are in $\mathbb{R}^7$ and $\operatorname{dimRow} A$ $+\operatorname{dimNul} A=7$. The matrix $T=\left[\begin{array}{ll}C & M\end{array}\right]$ is $5 \times 5$ because the columns of $C$ and $M$ are in $\mathbb{R}^5$ and $\operatorname{dimCol} A+\operatorname{dimNul} A^T=5$. Both $S$ and $T$ are invertible because their columns are linearly independent. This fact will be proven in general in Theorem 3 of Section 6.1.