<h1 align="center">Determinants</h1>


## Session Material:

Lay: 3.1-3.3

[Recap and Exercises](https://drive.google.com/file/d/1AaUzMugj40HYyCZAiS2O1ZvOGGJNqg6o/view?usp=sharing)

[Session Notes](https://drive.google.com/file/d/13yh_oxGsW-aWL_f0YgXhUQo3399X88GD/view?usp=sharing)

[Session Material](https://viaucdk-my.sharepoint.com/:f:/g/personal/rib_viauc_dk/EqnOhUdCrwBLpZNg2NSxmaUBIxBFaoMXe4X_erAXqiUJFA?e=CVLt0G)

---

## Session Description

This session introduces the concept of the **determinant** of a matrix. We will start by defining and learning how to compute the determinant for **$2 \times 2$ matrices**, and then extend this to **$3 \times 3$ matrices** and  **$n \times n$ matrices**, using a systematic method.

We will explore the **basic properties** of the determinant, including how row operations affect its value. A central result that will be highlighted is the **relationship between the determinant and a matrix's invertibility** – a matrix is invertible if and only if its determinant is non-zero.

Depending on the precise content of the sections, we may also touch upon the **geometric interpretation** of the determinant, such as its connection to **area** or volume.

### Key Concepts

*   Determinant
*   Calculating 2x2 Determinants
*   Calculating 3x3 Determinants
*   Properties of Determinants
*   Determinant and Invertibility
*   Geometric Interpretation (Area/Volume)

!!! tip "Learning Objectives"

    - Compute determinants of $2 \times 2$, $3 \times 3$, and $n \times n$ matrices using systematic methods.
    - Apply properties of determinants to simplify calculations and understand matrix behavior.
    - Relate the determinant to matrix invertibility and solve related problems.
    - Interpret the geometric meaning of determinants in terms of area and volume.
    - Analyze the effect of row operations on the determinant.

## Exercises

<!--
​​​3.1: 1, 2, 9, 43   
3.2: 1, 2, 15-20, 25 
-->
<style type="text/css">
    ol { list-style-type: lower-alpha; }
</style>

**Exercise 1** (3.1.1-3.1.2)

Compute the determinants using a cofactor expansion across the first row. Then compute the determinant also by a cofactor expansion down the second column.

1. $\left|\begin{array}{rrr}3 & 0 & 4 \\ 2 & 3 & 2 \\ 0 & 5 & -1\end{array}\right|$
2. $\left|\begin{array}{rrr}0 & 5 & 1 \\ 4 & -3 & 0 \\ 2 & 4 & 1\end{array}\right|$

??? answer "&nbsp;"
    1. 1
    2. 2

**Exercise 2** (3.1.9)

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

**Exercise 3** (3.1.43)

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


**Exercise 4** (3.2.1-3.2.2)

Both equations illustrate a property of determinants. State the property.

1. $\left|\begin{array}{rrr}0 & 5 & -2 \\ 1 & -3 & 6 \\ 4 & -1 & 8\end{array}\right|=-\left|\begin{array}{rrr}1 & -3 & 6 \\ 0 & 5 & -2 \\ 4 & -1 & 8\end{array}\right|$
2. $\left|\begin{array}{rrr}2 & -6 & 4 \\ 3 & 5 & -2 \\ 1 & 6 & 3\end{array}\right|=2\left|\begin{array}{rrr}1 & -3 & 2 \\ 3 & 5 & -2 \\ 1 & 6 & 3\end{array}\right|$

??? answer "&nbsp;"
    1. Rows 1 and 2 are interchanged, so the determinant changes sign (Theorem 3b.).
    2. The constant 2 may be factored out of the Row 1 (Theorem 3c.).

**Exercise 5** (3.2.15-3.2.20)

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

**Exercise 6** (3.2.25)

Use the determinant to decide if the set of vectors is linearly independent.

<div align="center">
$\left[\begin{array}{r}7 \\ -4 \\ -6\end{array}\right],\left[\begin{array}{r}-8 \\ 5 \\ 7\end{array}\right],\left[\begin{array}{r}7 \\ 0 \\ -5\end{array}\right]$
</div>

??? answer "&nbsp;"
    The columns of the matrix form a linearly independent set.