<h1 align="center">Eigenvalues</h1>

## Session Material:

Lay: ​5.1-5.3

[Recap and Exercises](https://drive.google.com/file/d/1wNL5E-jT3YuMJqcTAerjT93qPsChGpOc/view?usp=sharing)

[Session Notes](https://drive.google.com/file/d/1B9R3FF0Xz6bitUmtA7I_0IjbwJuhYa0_/view?usp=sharing)

[Session Material](https://viaucdk-my.sharepoint.com/:f:/g/personal/rib_viauc_dk/ErEbWej73CxBiXGFKP-mtx4BzkmBdQWAJOwzWIuvuzoBZw?e=oCjf1Z)

---

## Session Description

This session introduces some of the most powerful and fascinating concepts in linear algebra: eigenvalues and eigenvectors! We'll explore what these special vectors (eigenvectors) and scalars (eigenvalues) are – basically, vectors that only get scaled (not changed in direction) when a matrix transformation is applied. We'll learn how to find eigenvalues by solving the "characteristic equation" and then find the corresponding eigenvectors by solving a system of equations.

Understanding the set of all eigenvectors for a specific eigenvalue (the "eigenspace") is also key. Finally, we'll tackle the concept of "diagonalization" – a super useful technique where we can transform certain matrices into simpler diagonal forms using their eigenvectors and eigenvalues. This process, often called similarity transformation, simplifies many calculations and reveals deeper properties of the matrix and the transformation it represents.

### Key Concepts

- Eigenvalues
- Eigenvectors
- Characteristic Equation
- Eigenspaces
- Diagonalization
- Matrix Similarity

!!! tip "Learning Objectives"

    - Define and compute eigenvalues and eigenvectors for matrices.
    - Solve the characteristic equation and construct eigenspaces.
    - Diagonalize matrices and explain the process of similarity transformation.
    - Analyze the significance of eigenvalues and eigenvectors in matrix transformations.
    - Apply diagonalization to simplify matrix computations and interpret results.

## Exercises

<!--
​​5.1: 1, 3, 5, 7, 13, 16, 40
5.2: 1, 3, 6, 10, 11
5.3: 1, 6, 10-14, 35, 36
-->
<style type="text/css">
    ol { list-style-type: lower-alpha; }
</style>

**Exercise 1** (5.1.1)

Is $\lambda=2$ an eigenvalue of $\left[\begin{array}{ll}3 & 2 \\ 3 & 8\end{array}\right]$ ? Why or why not?

??? answer "&nbsp;"
    2 is an eigenvalue of $A$.

**Exercise 2** (5.1.3)

Is $\left[\begin{array}{l}1 \\ 3\end{array}\right]$ an eigenvector of $\left[\begin{array}{ll}1 & -1 \\ 6 & -4\end{array}\right]$ ? If so, find the eigenvalue.

??? answer "&nbsp;"
    $\left[\begin{array}{l}1 \\ 3\end{array}\right]$ is an eigenvector of $A$ with eigenvalue -2 .

**Exercise 3** (5.1.5)

Is $\left[\begin{array}{r}3 \\ -2 \\ 1\end{array}\right]$ an eigenvector of $\left[\begin{array}{rrr}-4 & 3 & 3 \\ 2 & -3 & -2 \\ -1 & 0 & -2\end{array}\right]$ ? If so, find the eigenvalue.

??? answer "&nbsp;"
    $\left[\begin{array}{r}3 \\ -2 \\ 1\end{array}\right]$ is an eigenvector of $A$ for the eigenvalue -5.

**Exercise 4** (5.1.7)

Is $\lambda=4$ an eigenvalue of $\left[\begin{array}{rrr}3 & 0 & -1 \\ 2 & 3 & 1 \\ -3 & 4 & 5\end{array}\right]$ ? If so, find one corresponding eigenvector.

??? answer "&nbsp;"
    Yes, $\lambda=4$ is an eigenvalue of $A$. The general solution is not requested, so to save time, simply take any nonzero value for $x_3$ to produce an eigenvector. If $x_3=1$, then $\mathbf{x}=(-1,-1,1)$.

**Exercise 5** (5.1.13, 5.1.16)

Find a basis for the eigenspace corresponding to both listed eigenvalues.

13. $A=\left[\begin{array}{rrr}4 & 0 & 1 \\ -2 & 1 & 0 \\ -2 & 0 & 1\end{array}\right], \lambda=1,2,3$
16. $A=\left[\begin{array}{rrrr}5 & 0 & -1 & 0 \\ 1 & 3 & 0 & 0 \\ 2 & -1 & 3 & 0 \\ 4 & -2 & -2 & 4\end{array}\right], \lambda=4$

??? answer "&nbsp;"
    13. 
    
        For $\lambda=1$ : The general solution of $(A-I) \mathbf{x}=\mathbf{0}$ is $x_2 \mathbf{e}_2$, where $\mathbf{e}_2=\left[\begin{array}{l}0 \\ 1 \\ 0\end{array}\right]$, and so $\mathbf{e}_2$ provides a basis for the eigenspace.

        For $\lambda=2$ : The general solution of $(A-2 I) \mathbf{x}=\mathbf{0}$ is $x_3\left[\begin{array}{c}-1 / 2 \\ 1 \\ 1\end{array}\right]$. A nice basis vector for the eigenspace is $\left[\begin{array}{r}-1 \\ 2 \\ 2\end{array}\right]$.

        For $\lambda=3$ : A basis vector for the eigenspace is $\left[\begin{array}{r}-1 \\ 1 \\ 1\end{array}\right]$.

    16. 

        Basis for the eigenspace : $\left\{\left[\begin{array}{l}1 \\ 1 \\ 1 \\ 0\end{array}\right],\left[\begin{array}{l}0 \\ 0 \\ 0 \\ 1\end{array}\right]\right\}$

**Exercise 6** (5.1.40)

[M] Use a matrix program to find the eigenvalues of the matrix. Then use the method of Example 4 with a row reduction routine to produce a basis for the eigenspace.

$\left[\begin{array}{rrrrr}-23 & 57 & -9 & -15 & -59 \\ -10 & 12 & -10 & 2 & -22 \\ 11 & 5 & -3 & -19 & -15 \\ -27 & 31 & -27 & 25 & -37 \\ -5 & -15 & -5 & 1 & 31\end{array}\right]$

??? answer "&nbsp;"
    [M] For $\lambda=-14$, basis: $\left\{\left[\begin{array}{r}-1 \\ 0 \\ 1 \\ 0 \\ 0\end{array}\right],\left[\begin{array}{r}10 \\ 6 \\ 0 \\ 5 \\ 1\end{array}\right]\right\}$. 
    
    For $\lambda=42$, basis: $\left\{\left[\begin{array}{r}0 \\ 1 \\ -2 \\ 5 \\ 0\end{array}\right],\left[\begin{array}{r}-5 \\ -1 \\ -3 \\ 0 \\ 5\end{array}\right]\right\}$.

**Exercise 7** (5.2.1, 5.2.3, 5.2.6)

Find the characteristic polynomial and the real eigenvalues of the following matricies.

1. $\left[\begin{array}{ll}2 & 7 \\ 7 & 2\end{array}\right]$
3. $\left[\begin{array}{rr}-4 & 2 \\ 6 & 7\end{array}\right]$
6. $\left[\begin{array}{rr}9 & -2 \\ 2 & 5\end{array}\right]$

??? answer "&nbsp;"
    1. The characteristic polynomial is $\operatorname{det}(A-\lambda I)=(2-\lambda)^2-7^2=4-4 \lambda+\lambda^2-49=\lambda^2-4 \lambda-45$, the eigenvalues of $A$ are -2 and -1.
    3. The characteristic polynomial is $\operatorname{det}(A-\lambda I)=(-4-\lambda)(7-\lambda)-(2)(6)=\lambda^2-3 \lambda-40$, the eigenvalues of $A$ are 8 and -5.
    6. The characteristic polynomial is $\operatorname{det}(A-\lambda I)=(9-\lambda)(5-\lambda)-(-2)(2)=\lambda^2-14 \lambda+49=(\lambda-7)(\lambda-7)$, thus $A$ has only one eigenvalue, 7, with multiplicity 2.

**Exercise 8** (5.2.10, 5.2.11)

Following exercises require techniques from Section 3.1. Find the characteristic polynomial of each matrix, using either a cofactor expansion or the special formula for $3 \times 3$ determinants described prior to Exercises 15-18 in Section 3.1. [Note: Finding the characteristic polynomial of a $3 \times 3$ matrix is not easy to do with just row operations, because the variable $\lambda$ is involved.]

10. $\left[\begin{array}{rrr}3 & 1 & 1 \\ 0 & 5 & 0 \\ -2 & 0 & 7\end{array}\right]$
11. $\left[\begin{array}{lll}3 & 0 & 0 \\ 2 & 1 & 4 \\ 1 & 0 & 4\end{array}\right]$

??? answer "&nbsp;"
    10. $-\lambda^3+15 \lambda^2-73 \lambda+115$
    11. $-\lambda^3+8 \lambda^2-19 \lambda+12$

**Exercise 9** (5.3.1)

Let $A=P D P^{-1}$ and compute $A^4$.

$P=\left[\begin{array}{ll}5 & 7 \\ 2 & 3\end{array}\right], D=\left[\begin{array}{ll}2 & 0 \\ 0 & 1\end{array}\right]$

??? answer "&nbsp;"
    $A^4=\left[\begin{array}{ll}5 & 7 \\ 2 & 3\end{array}\right]\left[\begin{array}{cc}16 & 0 \\ 0 & 1\end{array}\right]\left[\begin{array}{rr}3 & -7 \\ -2 & 5\end{array}\right]=\left[\begin{array}{cc}226 & -525 \\ 90 & -209\end{array}\right]$

**Exercise 10** (5.3.6)

The matrix $A$ is factored in the form $P D P^{-1}$. Use the Diagonalization Theorem to find the eigenvalue of $A$ and a basis for the eigenspace.

$\begin{aligned} A & =\left[\begin{array}{rrr}3 & 0 & 0 \\ -3 & 4 & 9 \\ 0 & 0 & 3\end{array}\right] \\ & =\left[\begin{array}{rrr}3 & 0 & -1 \\ 0 & 1 & -3 \\ 1 & 0 & 0\end{array}\right]\left[\begin{array}{lll}3 & 0 & 0 \\ 0 & 4 & 0 \\ 0 & 0 & 3\end{array}\right]\left[\begin{array}{rrr}0 & 0 & 1 \\ -3 & 1 & 9 \\ -1 & 0 & 3\end{array}\right]\end{aligned}$

??? answer "&nbsp;"
    $\lambda=4:\left[\begin{array}{l}0 \\ 1 \\ 0\end{array}\right] ; \lambda=3:\left[\begin{array}{l}3 \\ 0 \\ 1\end{array}\right],\left[\begin{array}{c}-1 \\ -3 \\ 0\end{array}\right]$

**Exercise 11** (5.3.10-14)

Diagonalize the matrices, if possible. The real eigenvalues for Exercises (b)-(e) are included next to the matrix.

10. $\left[\begin{array}{ll}1 & 3 \\ 4 & 2\end{array}\right]$
11. $\left[\begin{array}{lll}0 & 1 & 1 \\ 2 & 1 & 2 \\ 3 & 3 & 2\end{array}\right]$
    $\lambda=-1,5$
12. $\left[\begin{array}{lll}3 & 1 & 1 \\ 1 & 3 & 1 \\ 1 & 1 & 3\end{array}\right]$
    $\lambda=2,5$
13. $\left[\begin{array}{rrr}2 & 2 & -1 \\ 1 & 3 & -1 \\ -1 & -2 & 2\end{array}\right]$
    $\lambda=1,5$
14. $\left[\begin{array}{rrr}2 & 0 & -2 \\ 1 & 3 & 2 \\ 0 & 0 & 3\end{array}\right]$
    $\lambda=2,3$

??? answer "&nbsp;"
    10. 

        For $\lambda=-2$: The general solution is $x_2\left[\begin{array}{r}-1 \\ 1\end{array}\right]$, and a nice basis vector for the eigenspace is $\mathbf{v}_1=\left[\begin{array}{r}-1 \\ 1\end{array}\right]$.

        For $\lambda=5$: The general solution is $x_2\left[\begin{array}{c}3 / 4 \\ 1\end{array}\right]$, and a basis vector for the eigenspace is $\mathbf{v}_2=\left[\begin{array}{l}3 \\ 4\end{array}\right]$.

        $D=\left[\begin{array}{rr}-2 & 0 \\ 0 & 5\end{array}\right]$

    11. 

        For $\lambda=-1$: The general solution is $x_2\left[\begin{array}{c}-1 \\ 1 \\ 0\end{array}\right]+x_3\left[\begin{array}{r}-1 \\ 0 \\ 1\end{array}\right]$, and a nice basis for the eigenspace is $\left\{\mathbf{v}_1, \mathbf{v}_2\right\}=\left\{\left[\begin{array}{c}-1 \\ 1 \\ 0\end{array}\right],\left[\begin{array}{c}-1 \\ 0 \\ 1\end{array}\right]\right\}$.

        For $\lambda=5$: general solution is $x_3\left[\begin{array}{r}1 / 3 \\ 2 / 3 \\ 1\end{array}\right]$, and a nice basis vector for the eigenspace is $\mathbf{v}_3=\left[\begin{array}{l}1 \\ 2 \\ 3\end{array}\right]$.

        $D=\left[\begin{array}{ccc}-1 & 0 & 0 \\ 0 & -1 & 0 \\ 0 & 0 & 5\end{array}\right]$

    12. 

        For $\lambda=2$: The general solution is $x_2\left[\begin{array}{c}-1 \\ 1 \\ 0\end{array}\right]+x_3\left[\begin{array}{r}-1 \\ 0 \\ 1\end{array}\right]$, and a nice basis for the eigenspace is $\left\{\mathbf{v}_1, \mathbf{v}_2\right\}=\left\{\left[\begin{array}{c}-1 \\ 1 \\ 0\end{array}\right],\left[\begin{array}{c}-1 \\ 0 \\ 1\end{array}\right]\right\}$.

        For $\lambda=5$: The general solution is $x_3\left[\begin{array}{l}1 \\ 1 \\ 1\end{array}\right]$, and a basis for the eigenspace is $\mathbf{v}_3=\left[\begin{array}{l}1 \\ 1 \\ 1\end{array}\right]$.

        $D=\left[\begin{array}{lll}2 & 0 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 5\end{array}\right]$

    13. 

        For $\lambda=5$: The general solution is $x_3\left[\begin{array}{r}-1 \\ -1 \\ 1\end{array}\right]$, and a basis for the eigenspace is $\mathbf{v}_1=\left[\begin{array}{r}-1 \\ -1 \\ 1\end{array}\right]$.

        For $\lambda=1$: The general solution is $x_2\left[\begin{array}{r}-2 \\ 1 \\ 0\end{array}\right]+x_3\left[\begin{array}{l}1 \\ 0 \\ 1\end{array}\right]$, and a basis for the eigenspace is $\left\{\mathbf{v}_2, \mathbf{v}_3\right\}=\left\{\left[\begin{array}{r}-2 \\ 1 \\ 0\end{array}\right],\left[\begin{array}{l}1 \\ 0 \\ 1\end{array}\right]\right\}$.

        $D=\left[\begin{array}{lll}5 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1\end{array}\right]$

    14. 

        For $\lambda=2$: The general solution is $x_2\left[\begin{array}{c}-1 \\ 1 \\ 0\end{array}\right]$, and a basis for the eigenspace is $\mathbf{v}_1=\left[\begin{array}{c}-1 \\ 1 \\ 0\end{array}\right]$.

        For $\lambda=3$: The general solution is $x_2\left[\begin{array}{l}0 \\ 1 \\ 0\end{array}\right]+x_3\left[\begin{array}{r}-2 \\ 0 \\ 1\end{array}\right]$, and a nice basis for the eigenspace is $\left\{\mathbf{v}_2, \mathbf{v}_3\right\}=\left\{\left[\begin{array}{l}0 \\ 1 \\ 0\end{array}\right],\left[\begin{array}{c}-2 \\ 0 \\ 1\end{array}\right]\right\}$.

        $D=\left[\begin{array}{lll}2 & 0 & 0 \\ 0 & 3 & 0 \\ 0 & 0 & 3\end{array}\right]$

**Exercise 12** (5.3.35, 5.3.36)

[M] Diagonalize the matrices. Use your matrix program's eigenvalue command to find the eigenvalues, and then compute bases for the eigenspaces as in Section 5.1.

35. $\left[\begin{array}{rrrrr}13 & -12 & 9 & -15 & 9 \\ 6 & -5 & 9 & -15 & 9 \\ 6 & -12 & -5 & 6 & 9 \\ 6 & -12 & 9 & -8 & 9 \\ -6 & 12 & 12 & -6 & -2\end{array}\right]$
36. $\left[\begin{array}{rrrrr}24 & -6 & 2 & 6 & 2 \\ 72 & 51 & 9 & -99 & 9 \\ 0 & -63 & 15 & 63 & 63 \\ 72 & 15 & 9 & -63 & 9 \\ 0 & 63 & 21 & -63 & -27\end{array}\right]$

??? answer "&nbsp;"
    35. $D=\left[\begin{array}{ccccc}7 & 0 & 0 & 0 & 0 \\ 0 & 7 & 0 & 0 & 0 \\ 0 & 0 & 7 & 0 & 0 \\ 0 & 0 & 0 & -14 & 0 \\ 0 & 0 & 0 & 0 & -14\end{array}\right]$
    36. $D=\left[\begin{array}{ccccc}24 & 0 & 0 & 0 & 0 \\ 0 & -48 & 0 & 0 & 0 \\ 0 & 0 & -48 & 0 & 0 \\ 0 & 0 & 0 & 36 & 0 \\ 0 & 0 & 0 & 0 & 36\end{array}\right]$