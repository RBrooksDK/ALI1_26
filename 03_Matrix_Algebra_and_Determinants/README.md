---
tags:
    - Matrix Algebra
    - Matrix Multiplication
    - Matrix Inverse
    - Determinants
    - Invertible Matrix Theorem
    - Matrix Transpose
    - Identity Matrix
    - Diagonal Matrix
    - Cofactor Expansion
    - Area and Volume
    - Row Operations
---

<h1 align="center">Matrix Algebra and Determinants</h1>

## Session Material:

Lay: 2.1-2.3 + 3.1-3.2

[Recap and Exercises](https://drive.google.com/file/d/11ALtM3NUj5bDszkDrpZYXnIGE4x9XN6f/view?usp=sharing)

[Session Notes](https://drive.google.com/file/d/1RFqxjjNa1tlmauS49Okw-IoVQvn8jexk/view?usp=sharing)

[Session Material](https://viaucdk-my.sharepoint.com/:f:/g/personal/rib_viauc_dk/IgAMEID2phisS4KUfj2Mf0gqAXEysLn5lVSLconixqB5aek?e=cY8imK)

### Session Recording

<div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%; overflow: hidden;">
    <iframe 
        src="https://drive.google.com/file/d/1mZlcVegx2PilAabkX9QiwKwHjZDFnUUT/preview" 
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
        allow="autoplay; encrypted-media" 
        allowfullscreen>
    </iframe>
</div>

---

## Session Description

In this session, we transition from using matrices as tools for solving systems to studying them as algebraic objects in their own right. We begin with **Matrix Algebra**, mastering operations such as addition, scalar multiplication, and the row-column rule for matrix multiplication. You will learn to navigate the unique rules of matrix arithmetic, including the properties of identity, diagonal, and transpose matrices.

A central focus of this session is the **Matrix Inverse**. You will learn how to determine if a matrix is invertible and how to compute $A^{-1}$ using row reduction. We then introduce the **Determinant**, a powerful scalar value that acts as a "diagnostic tool" for a matrix. We will cover systematic methods for calculating determinants of any $n \times n$ matrix and explore how row operations influence their values. Finally, we unite these concepts through the **Invertible Matrix Theorem (IMT)**, which connects algebra, determinants, and row reduction into one of the most important theoretical frameworks in linear algebra.

### Key Concepts

* Matrix Operations (+, −, and scalar multiplication)
* Matrix Multiplication (Row-Column Rule)
* Transpose and Powers of Matrices
* Invertible Matrices and the Matrix Inverse ($A^{-1}$)
* Determinants (Calculation for $2 \times 2$, $3 \times 3$, and $n \times n$)
* Properties of Determinants and Row Operations
* The Invertible Matrix Theorem (IMT)
* Geometric Interpretation (Area and Volume)

!!! tip "Learning Objectives"

    - Perform matrix arithmetic and matrix multiplication using the row-column rule.
    - Compute and interpret matrix inverses and transposes.
    - Calculate determinants for $n \times n$ matrices using cofactor expansion.
    - Analyze how row operations affect the determinant of a matrix.
    - Apply the Invertible Matrix Theorem to relate invertibility, determinants, and row reduction.
    - Interpret the geometric meaning of determinants in terms of area and volume.

---

## Exercises

<!--     
2.1: 1, 2, 10, 13, 40, 41   
2.2: 9, 30, 31, 32   
​2.3: 11, 12, 15, 17  
-->
<style type="text/css">
    ol { list-style-type: lower-alpha; }
</style>


**Exercise 1** (2.1.1-2.1.2)

Compute each matrix sum or product if it is defined. If an expression is undefined, explain why. Let

$$
\begin{aligned}
& A=\left[\begin{array}{rrr}
2 & 0 & -1 \\
4 & -5 & 2
\end{array}\right], \quad B=\left[\begin{array}{rrr}
7 & -5 & 1 \\
1 & -4 & -3
\end{array}\right], \\
& C=\left[\begin{array}{rr}
1 & 2 \\
-2 & 1
\end{array}\right], \quad D=\left[\begin{array}{rr}
3 & 5 \\
-1 & 4
\end{array}\right], \quad E=\left[\begin{array}{r}
-5 \\
3
\end{array}\right]
\end{aligned}
$$

1. $-2 A, B-2 A, A C, C D$
2. $A+3 B, 2 C-3 E, D B, E C$

??? answer "&nbsp;"
    1. The product $A C$ is not defined because the number of columns of $A$ does not match the number of rows of $C. 
    C D=\left[\begin{array}{rr}1 & 2 \\ -2 & 1\end{array}\right]\left[\begin{array}{rr}3 & 5 \\ -1 & 4\end{array}\right]=\left[\begin{array}{rr}1 \cdot 3+2(-1) & 1 \cdot 5+2 \cdot 4 \\ -2 \cdot 3+1(-1) & -2 \cdot 5+1 \cdot 4\end{array}\right]=\left[\begin{array}{rr}1 & 13 \\ -7 & -6\end{array}\right]$. For mental computation, the row-column rule is probably easier to use than the definition.
    2. The sum $2C-3E$ is not defined because the entries do not match. The product $E C$ is not defined because the number of columns of $E$ does not match the number of rows of $C$.

**Exercise 2** (2.1.10)

Assume that each matrix expression is defined. That is, the sizes of the matrices (and vectors) involved "match" appropriately.

Let $\quad A=\left[\begin{array}{rr}3 & -6 \\ -1 & 2\end{array}\right], \quad B=\left[\begin{array}{rr}-1 & 1 \\ 3 & 4\end{array}\right], \quad$ and $\quad C=$ $\left[\begin{array}{rr}-3 & -5 \\ 2 & 1\end{array}\right]$. Verify that $A B=A C$ and yet $B \neq C$.

??? answer "&nbsp;"
    $A B=\left[\begin{array}{rr}3 & -6 \\ -1 & 2\end{array}\right]\left[\begin{array}{rr}-1 & 1 \\ 3 & 4\end{array}\right]=\left[\begin{array}{rr}-21 & -21 \\ 7 & 7\end{array}\right], A C=\left[\begin{array}{rr}3 & -6 \\ -1 & 2\end{array}\right]\left[\begin{array}{rr}-3 & -5 \\ 2 & 1\end{array}\right]=\left[\begin{array}{rr}-21 & -21 \\ 7 & 7\end{array}\right]$


**Exercise 3** (2.2.9)

Mark each statement True or False. Justify each answer.

1. In order for a matrix $B$ to be the inverse of $A$, the equations $A B=I$ and $B A=I$ must both be true.
2. If $A$ and $B$ are $n \times n$ and invertible, then $A^{-1} B^{-1}$ is the inverse of $A B$.
3. If $A=\left[\begin{array}{ll}a & b \\ c & d\end{array}\right]$ and $a b-c d \neq 0$, then $A$ is invertible.
4. If $A$ is an invertible $n \times n$ matrix, then the equation $A \mathbf{x}=\mathbf{b}$ is consistent for each $\mathbf{b}$ in $\mathbb{R}^n$.
5. Each elementary matrix is invertible.

??? answer "&nbsp;"
    1. True, by definition of invertible.
    2. False. See Theorem 6(b).
    3. False. If $A=\left[\begin{array}{ll}1 & 1 \\ 0 & 0\end{array}\right]$, then $a b-c d=1-0 \neq 0$, but Theorem 4 shows that this matrix is not invertible, because $a d-b c=0$.
    4. True. This follows from Theorem 5, which also says that the solution of $A \mathbf{x}=\mathbf{b}$ is unique, for each $\mathbf{b}$.
    5. True, by the box just before Example 6 .

**Exercise 4** (2.2.30-2.2.32)

Find the inverses of the matrices, if they exist. Use the algorithm introduced in this section.

1. $\left[\begin{array}{ll}3 & 6 \\ 4 & 7\end{array}\right]$
2. $\left[\begin{array}{rrr}1 & 0 & -2 \\ -3 & 1 & 4 \\ 2 & -3 & 4\end{array}\right]$
3. $\left[\begin{array}{rrr}1 & 2 & -1 \\ -4 & -7 & 3 \\ -2 & -6 & 4\end{array}\right]$

??? answer "&nbsp;"
    1. $A^{-1}=\left[\begin{array}{rr}-7 / 3 & 2 \\ 4 / 3 & -1\end{array}\right]$
    2. $A^{-1}=\left[\begin{array}{ccc}8 & 3 & 1 \\ 10 & 4 & 1 \\ 7 / 2 & 3 / 2 & 1 / 2\end{array}\right]$
    3. The matrix $A$ is not invertible.

**Exercise 5** (2.3.11)

The matrices are all $n \times n$. Each part of the exercises is an implication of the form "If 〈statement 1〉, then $\langle$ statement 2$\rangle$." Mark an implication as True if the truth of〈statement 2〉 always follows whenever 〈statement 1〉 happens to be true. An implication is False if there is an instance in which 〈statement 2 〉 is false but $\langle$ statement 1$\rangle$ is true. Justify each answer.

1. If the equation $A \mathbf{x}=\mathbf{0}$ has only the trivial solution, then $A$ is row equivalent to the $n \times n$ identity matrix.
2. If the columns of $A$ span $\mathbb{R}^n$, then the columns are linearly independent.
3. If $A$ is an $n \times n$ matrix, then the equation $A \mathbf{x}=\mathbf{b}$ has at least one solution for each $\mathbf{b}$ in $\mathbb{R}^n$.
4. If the equation $A \mathbf{x}=\mathbf{0}$ has a nontrivial solution, then $A$ has fewer than $n$ pivot positions.
5. If $A^T$ is not invertible, then $A$ is not invertible.

??? answer "&nbsp;"
    1. True, by the IMT. If statement (d) of the IMT is true, then so is statement (b).
    2. True. If statement (h) of the IMT is true, then so is statement (e).
    3. False. Statement (g) of the IMT is true only for invertible matrices.
    4. True, by the IMT. If the equation $A \mathbf{x}=\mathbf{0}$ has a nontrivial solution, then statement (d) of the IMT is false. In this case, all the lettered statements in the IMT are false, including statement (c), which means that $A$ must have fewer than $n$ pivot positions.
    5. True, by the IMT. If $A^T$ is not invertible, then statement (1) of the IMT is false, and hence statement (a) must also be false.

**Exercise 6** (2.3.12)

The matrices are all $n \times n$. Each part of the exercises is an implication of the form "If 〈statement 1〉, then $\langle$ statement 2$\rangle$." Mark an implication as True if the truth of〈statement 2〉 always follows whenever 〈statement 1〉 happens to be true. An implication is False if there is an instance in which 〈statement 2 〉 is false but $\langle$ statement 1$\rangle$ is true. Justify each answer.

1. If there is an $n \times n$ matrix $D$ such that $A D=I$, then $D A=I$.
2. If the linear transformation $\mathbf{x} \mapsto A \mathbf{x}$ maps $\mathbb{R}^n$ into $\mathbb{R}^n$, then the row reduced echelon form of $A$ is $I$.
3. If the columns of $A$ are linearly independent, then the columns of $A$ span $\mathbb{R}^n$.
4. If the equation $A \mathbf{x}=\mathbf{b}$ has at least one solution for each $\mathbf{b}$ in $\mathbb{R}^n$, then the transformation $\mathbf{x} \mapsto A \mathbf{x}$ is not one-to-one.
5. If there is a $\mathbf{b}$ in $\mathbb{R}^n$ such that the equation $A \mathbf{x}=\mathbf{b}$ is consistent, then the solution is unique.

??? answer "&nbsp;"
    1. True. If statement $(\mathrm{k})$ of the IMT is true, then so is statement $(\mathrm{j})$. Use the first box after the IMT.
    2. False. Notice that (i) if the IMT uses the work onto rather than the word into.
    3. True. If statement (e) of the IMT is true, then so is statement (h).
    4. False. Since (g) if the IMT is true, so is (f).
    5. False, by the IMT. The fact that there is a $\mathbf{b}$ in $\mathbb{R}^n$ such that the equation $A \mathbf{x}=\mathbf{b}$ is consistent, does not imply that statement (g) of the IMT is true, and hence there could be more than one solution.

**Exercise 7** (2.3.15)

Is it possible for a $4 \times 4$ matrix to be invertible when its columns do not span $\mathbb{R}^4$ ? Why or why not?

??? answer "&nbsp;"
    Part (h) of the IMT shows that a $4 \times 4$ matrix cannot be invertible when its columns do not span $\mathbf{R}^4$.

**Exercise 8** (2.3.17)

Can a square matrix with two identical columns be invertible? Why or why not?

??? answer "&nbsp;"
    If $A$ has two identical columns then its columns are linearly dependent. Part (e) of the IMT shows that $A$ cannot be invertible.

**Exercise 9** (3.1.1-3.1.2)

Compute the determinants using a cofactor expansion across the first row. Then compute the determinant also by a cofactor expansion down the second column.

1. $\left|\begin{array}{rrr}3 & 0 & 4 \\ 2 & 3 & 2 \\ 0 & 5 & -1\end{array}\right|$
2. $\left|\begin{array}{rrr}0 & 5 & 1 \\ 4 & -3 & 0 \\ 2 & 4 & 1\end{array}\right|$

??? answer "&nbsp;"
    1. 1
    2. 2

**Exercise 10** (3.1.9)

Compute the determinant by cofactor expansions. At each step, choose a row or column that involves the least amount of computation.

<div align="center">
$\displaystyle \left|\begin{array}{rrrr}
6 & 0 & 0 & 5 \\
1 & 7 & 2 & -5 \\
2 & 0 & 0 & 0 \\
8 & 3 & 1 & 8
\end{array}\right|$
</div>

??? answer "&nbsp;"
    10

**Exercise 11** (3.1.43)

$[\mathbf{M}]$ Is it true that $\operatorname{det}(A+B)=\operatorname{det} A+\operatorname{det} B ?$ To find out, generate random $5 \times 5$ matrices $A$ and $B$, and compute $\operatorname{det}(A+B)-\operatorname{det} A-\operatorname{det} B$. (Refer to Exercise 37 in Section 2.1.) Repeat the calculations for three other pairs of $n \times n$ matrices, for various values of $n$. Report your results.

??? answer "&nbsp;"
    Here are sample results testing whether $\det(A+B)=\det A+\det B$ for random integer matrices $A,B$ of sizes $n=5,2,3,10$:

    |  n |     det(A) |     det(B) | det(A + B) | det(A + B) − det(A) − det(B) |
    | -: | ---------: | ---------: | ---------: | ---------------------------: |
    |  5 |        668 |      −1077 |       2765 |                         3174 |
    |  2 |        −22 |          0 |        −26 |                           −4 |
    |  3 |        −93 |         28 |        −27 |                           38 |
    | 10 | 3.11 × 10⁶ | 3.35 × 10⁷ | 3.28 × 10⁸ |                   2.92 × 10⁸ |

    In every case, $\det(A+B)-\det A-\det B\neq0$, demonstrating that $\det(A+B)\neq\det A+\det B$. In general, determinant is **not** an additive function of matrices.


**Exercise 12** (3.2.1-3.2.2)

Both equations illustrate a property of determinants. State the property.

1. $\left|\begin{array}{rrr}0 & 5 & -2 \\ 1 & -3 & 6 \\ 4 & -1 & 8\end{array}\right|=-\left|\begin{array}{rrr}1 & -3 & 6 \\ 0 & 5 & -2 \\ 4 & -1 & 8\end{array}\right|$
2. $\left|\begin{array}{rrr}2 & -6 & 4 \\ 3 & 5 & -2 \\ 1 & 6 & 3\end{array}\right|=2\left|\begin{array}{rrr}1 & -3 & 2 \\ 3 & 5 & -2 \\ 1 & 6 & 3\end{array}\right|$

??? answer "&nbsp;"
    1. Rows 1 and 2 are interchanged, so the determinant changes sign (Theorem 3b.).
    2. The constant 2 may be factored out of the Row 1 (Theorem 3c.).

**Exercise 13** (3.2.15-3.2.20)

Find the determinants in the following exercises, where

$$
\left|\begin{array}{lll}
a & b & c \\
d & e & f \\
g & h & i
\end{array}\right|=7 .
$$

1. $\left|\begin{array}{ccc}a & b & c \\ d & e & f \\ 5 g & 5 h & 5 i\end{array}\right|$
2. $\left|\begin{array}{ccc}a & b & c \\ 3 d & 3 e & 3 f \\ g & h & i\end{array}\right|$
3. $\left|\begin{array}{lll}a & b & c \\ g & h & i \\ d & e & f\end{array}\right|$
4. $\left|\begin{array}{lll}g & h & i \\ a & b & c \\ d & e & f\end{array}\right|$
5. $\left|\begin{array}{ccc}a & b & c \\ 2 d+a & 2 e+b & 2 f+c \\ g & h & i\end{array}\right|$
6. $\left|\begin{array}{ccc}a+d & b+e & c+f \\ d & e & f \\ g & h & i\end{array}\right|$

??? answer "&nbsp;"
    1. 35
    2. 21
    3. -7
    4. 7
    5. 14
    6. 7

**Exercise 14** (3.2.25)

Use the determinant to decide if the set of vectors is linearly independent.

<div align="center">
$\left[\begin{array}{r}7 \\ -4 \\ -6\end{array}\right],\left[\begin{array}{r}-8 \\ 5 \\ 7\end{array}\right],\left[\begin{array}{r}7 \\ 0 \\ -5\end{array}\right]$
</div>

??? answer "&nbsp;"
    The columns of the matrix form a linearly independent set.