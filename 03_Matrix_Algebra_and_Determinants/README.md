<h1 align="center">Matrix Algebra</h1>

## Session Material:

Lay: 2.1-2.7 (2.4 + 2.6-2.7 self-study)

[Recap and Exercises](https://drive.google.com/file/d/1kPmXMfygFPIiEaka_L3amf9x1tgVFg1I/view?usp=sharing)

[Session Notes](https://drive.google.com/file/d/1EbLmjsCjzl_-HmPwmdwT_uVLzA6rPWbo/view?usp=sharing)

[Session Material](https://viaucdk-my.sharepoint.com/:f:/g/personal/rib_viauc_dk/EgCkADot6NBNgecwld6KLpwBki3OkF32RFBmtB_xbwSBoQ?e=DY1uNJ)

---

## Session Description

Now that we’ve learned to represent and solve systems with matrices, this session focuses on doing algebra with matrices themselves. We’ll start with basic operations like addition, scalar multiplication, and then tackle matrix multiplication — both its definition and the practical row-column rule.

We’ll explore special matrices (zero, identity, diagonal), powers, and transposes, and discuss how matrix operations differ from regular arithmetic. Key theorems (1–3 for operations, 5–7 for inverses) will guide us through the rules. A central idea is the invertible matrix and to find it using row reduction.

We’ll finish with the Invertible Matrix Theorem (Theorem 8), which ties together many core ideas.

### Key Concepts

* Matrix Operations
* Matrix Multiplication
* Special Matrices: Zero, Identity, Diagonal
* Matrix Powers
* Matrix Transpose
* Invertible Matrices
* Invertible Matrix Theorem
* Matrix Algebra
  
!!! tip "Learning Objectives"

    - Perform matrix addition, scalar multiplication, and matrix multiplication using the row-column rule.
    - Identify and use special matrices (zero, identity, diagonal) and their properties.
    - Compute and interpret matrix inverses and transposes.
    - Apply the Invertible Matrix Theorem
    - Analyze and solve problems using matrix algebra concepts.

---

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

**Exercise 5** (1.8.10)

Find all $\mathbf{x}$ in $\mathbb{R}^4$ that are mapped into the zero vector by the transformation $\mathbf{x} \mapsto A \mathbf{x}$ for the given matrix $A$.

$A=\left[\begin{array}{rrrr}3 & 2 & 10 & -6 \\ 1 & 0 & 2 & -4 \\ 0 & 1 & 2 & 3 \\ 1 & 4 & 10 & 8\end{array}\right]$

??? answer "&nbsp;"
    $\left\{\begin{array}{l}x_1=-2 x_3+4 x_4 \\ x_2=-2 x_3-3 x_4 \\ x_3 \text { is free } \\ x_4 \text { is free }\end{array} \quad \quad \mathbf{x}=\left[\begin{array}{c}-2 x_3 \\ -2 x_3 \\ x_3 \\ 0\end{array}\right]+\left[\begin{array}{c}4 x_4 \\ -3 x_4 \\ 0 \\ x_4\end{array}\right]=x_3\left[\begin{array}{r}-2 \\ -2 \\ 1 \\ 0\end{array}\right]+x_4\left[\begin{array}{r}4 \\ -3 \\ 0 \\ 1\end{array}\right]\right.$

**Exercise 6** (1.9.15)

Fill in the missing entries of the matrix, assuming that the equation holds for all values of the variables.

$\left[\begin{array}{lll}? & ? & ? \\ ? & ? & ? \\ ? & ? & ?\end{array}\right]\left[\begin{array}{l}x_1 \\ x_2 \\ x_3\end{array}\right]=\left[\begin{array}{c}2 x_1-4 x_2 \\ x_1-x_3 \\ -x_2+3 x_3\end{array}\right]$

??? answer "&nbsp;"
    By inspection, $\left[\begin{array}{rrr}2 & -4 & 0 \\ 1 & 0 & -1 \\ 0 & -1 & 3\end{array}\right]\left[\begin{array}{l}x_1 \\ x_2 \\ x_3\end{array}\right]=\left[\begin{array}{c}2 x_1-4 x_2 \\ x_1-x_3 \\ -x_2+3 x_3\end{array}\right]$

**Exercise 7** (2.1.1-2.1.2)

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

**Exercise 8** (2.1.10)

Assume that each matrix expression is defined. That is, the sizes of the matrices (and vectors) involved "match" appropriately.

Let $\quad A=\left[\begin{array}{rr}3 & -6 \\ -1 & 2\end{array}\right], \quad B=\left[\begin{array}{rr}-1 & 1 \\ 3 & 4\end{array}\right], \quad$ and $\quad C=$ $\left[\begin{array}{rr}-3 & -5 \\ 2 & 1\end{array}\right]$. Verify that $A B=A C$ and yet $B \neq C$.

??? answer "&nbsp;"
    $A B=\left[\begin{array}{rr}3 & -6 \\ -1 & 2\end{array}\right]\left[\begin{array}{rr}-1 & 1 \\ 3 & 4\end{array}\right]=\left[\begin{array}{rr}-21 & -21 \\ 7 & 7\end{array}\right], A C=\left[\begin{array}{rr}3 & -6 \\ -1 & 2\end{array}\right]\left[\begin{array}{rr}-3 & -5 \\ 2 & 1\end{array}\right]=\left[\begin{array}{rr}-21 & -21 \\ 7 & 7\end{array}\right]$

**Exercise 9** (2.1.13)

Assume that each matrix expression is defined. That is, the sizes of the matrices (and vectors) involved "match" appropriately.

Let $\mathbf{r}_1, \ldots, \mathbf{r}_p$ be vectors in $\mathbb{R}^n$, and let $Q$ be an $m \times n$ matrix. Write the matrix $\left[\begin{array}{lll}Q \mathbf{r}_1 & \cdots & Q \mathbf{r}_p\end{array}\right]$ as a product of two matrices (neither of which is an identity matrix).

??? answer "&nbsp;"
    Use the definition of $A B$ written in reverse order: $\left[A \mathbf{b}_1 \cdots A \mathbf{b}_p\right]=A\left[\mathbf{b}_1 \cdots \mathbf{b}_p\right]$. Thus $\left[Q \mathbf{r}_1 \cdots Q \mathbf{r}_p\right]=Q R$, when $R=\left[\begin{array}{lll}\mathbf{r}_1 & \cdots & \mathbf{r}_p\end{array}\right]$.

**Exercise 10** (2.1.40)

$[\mathbf{M}]$ Let

$$
S=\left[\begin{array}{lllll}
0 & 1 & 0 & 0 & 0 \\
0 & 0 & 1 & 0 & 0 \\
0 & 0 & 0 & 1 & 0 \\
0 & 0 & 0 & 0 & 1 \\
0 & 0 & 0 & 0 & 0
\end{array}\right]
$$

Compute $S^k$ for $k=2, \ldots, 6$.

??? answer "&nbsp;"
    $S^2=\left[\begin{array}{lllll}0 & 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 0 & 1 \\ 0 & 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 & 0\end{array}\right]$

    $S^3=\left[\begin{array}{lllll}0 & 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 0 & 1 \\ 0 & 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 & 0\end{array}\right]$

    $S^4=\left[\begin{array}{lllll}0 & 0 & 0 & 0 & 1 \\ 0 & 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 & 0\end{array}\right]$

    $S^5$ is the $5 \times 5$ zero matrix.   

    $S^6$ is also the $5 \times 5$ zero matrix.

**Exercise 11** (2.1.41)

Assume that each matrix expression is defined. That is, the sizes of the matrices (and vectors) involved "match" appropriately.

$[\mathbf{M}]$ Describe in words what happens when $A^5, A^{10}, A^{20}$, and $A^{30}$ are computed for

$$
A=\left[\begin{array}{rrr}
1 / 4 & 1 / 2 & 1 / 4 \\
1 / 2 & 1 / 3 & 1 / 6 \\
1 / 4 & 1 / 6 & 7 / 12
\end{array}\right]
$$


??? answer "&nbsp;"
    The entries in $A^{20}$ all agree with .3333333333 to 8 or 9 decimal places. The entries in $A^{30}$ all agree with .33333333333333 to at least 14 decimal places. The matrices appear to approach the matrix $\left[\begin{array}{lll}1 / 3 & 1 / 3 & 1 / 3 \\ 1 / 3 & 1 / 3 & 1 / 3 \\ 1 / 3 & 1 / 3 & 1 / 3\end{array}\right]$. Further exploration of this behavior appears in Sections 4.9 and 5.2.

**Exercise 12** (2.2.9)

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

**Exercise 13** (2.2.30-2.2.32)

Find the inverses of the matrices, if they exist. Use the algorithm introduced in this section.

1. $\left[\begin{array}{ll}3 & 6 \\ 4 & 7\end{array}\right]$
2. $\left[\begin{array}{rrr}1 & 0 & -2 \\ -3 & 1 & 4 \\ 2 & -3 & 4\end{array}\right]$
3. $\left[\begin{array}{rrr}1 & 2 & -1 \\ -4 & -7 & 3 \\ -2 & -6 & 4\end{array}\right]$

??? answer "&nbsp;"
    1. $A^{-1}=\left[\begin{array}{rr}-7 / 3 & 2 \\ 4 / 3 & -1\end{array}\right]$
    2. $A^{-1}=\left[\begin{array}{ccc}8 & 3 & 1 \\ 10 & 4 & 1 \\ 7 / 2 & 3 / 2 & 1 / 2\end{array}\right]$
    3. The matrix $A$ is not invertible.

**Exercise 14** (2.3.11)

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

**Exercise 15** (2.3.12)

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

**Exercise 16** (2.3.15)

Is it possible for a $4 \times 4$ matrix to be invertible when its columns do not span $\mathbb{R}^4$ ? Why or why not?

??? answer "&nbsp;"
    Part (h) of the IMT shows that a $4 \times 4$ matrix cannot be invertible when its columns do not span $\mathbf{R}^4$.

**Exercise 17** (2.3.17)

Can a square matrix with two identical columns be invertible? Why or why not?

??? answer "&nbsp;"
    If $A$ has two identical columns then its columns are linearly dependent. Part (e) of the IMT shows that $A$ cannot be invertible.