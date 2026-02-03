<h1 align="center">Orthogonality II</h1>

## Session Material:
Lay: ​​​6.4-6.6

[Recap and Exercises](https://drive.google.com/file/d/1BJFDHxnCy20o-mvCEuUkAotAKEnSBrVY/view?usp=sharing)

[Session Notes](https://drive.google.com/file/d/18le_DiM9wy9t3RGteK82Mfgn-E79v6yZ/view?usp=sharing)

[Session Material](https://viaucdk-my.sharepoint.com/:f:/g/personal/rib_viauc_dk/EtRCyXB5jWNAvJv9H0Uo-_8BEsXd36hxB3TOHflc7XSGjw?e=M8MUba)

---

## Session Description

Building on our understanding of orthogonal vectors and bases, this session focuses on powerful techniques and applications related to orthogonality. First, we'll learn the "Gram-Schmidt process" – a step-by-step method to turn *any* basis for a subspace into an orthogonal (or orthonormal) one. This is a fundamental algorithm! Related to Gram-Schmidt is the "QR factorization," a way to break down certain matrices into a product of a matrix with orthonormal columns and an upper triangular matrix.

Then, we'll tackle a super common problem in real-world data: what do you do when a linear system $A\mathbf{x}=\mathbf{b}$ has *no* exact solution? We'll introduce "least-squares" solutions – the 'best possible' approximate solutions that minimize the error. Geometrically, finding the least-squares solution involves projecting the vector $\mathbf{b}$ onto the column space of matrix $A$. We'll see how these least-squares ideas are applied, especially in fitting models to data (like finding the 'best' line through a set of points).

### Key Concepts

* Gram-Schmidt Process
* Orthogonalization
* Least Squares
* Inconsistent Systems
* Projections
* Data Fitting

!!! tip "Learning Objectives"

    - Apply the Gram-Schmidt process to construct orthogonal and orthonormal bases.
    - Solve least-squares problems and interpret best-fit solutions.
    - Analyze projections and their role in data fitting and inconsistent systems.
    - Connect orthogonality concepts to practical applications in modeling and data analysis.

## Exercises

<!--
6.4: 1, 6 12, 24
6.5: 1, 3, 5, 7, 12, 25
6.6: 3, 4, 7, 13 
-->
<style type="text/css">
    ol { list-style-type: lower-alpha; }
</style>

**Exercise 1** (6.4.1, 6.4.6)

In the following exercises, the given set is a basis for a subspace $W$. Use the Gram-Schmidt process to produce an orthogonal basis for $W$.

1. $\left[\begin{array}{r}3 \\ 0 \\ -1\end{array}\right],\left[\begin{array}{r}8 \\ 5 \\ -6\end{array}\right]$
6. $\left[\begin{array}{r}3 \\ -1 \\ 2 \\ -1\end{array}\right],\left[\begin{array}{r}-5 \\ 9 \\ -9 \\ 3\end{array}\right]$

??? answer "&nbsp;"
    1. $\left\{\left[\begin{array}{r}3 \\ 0 \\ -1\end{array}\right],\left[\begin{array}{r}-1 \\ 5 \\ -3\end{array}\right]\right\}$
    6. $\left\{\left[\begin{array}{r}3 \\ -1 \\ 2 \\ -1\end{array}\right],\left[\begin{array}{r}4 \\ 6 \\ -3 \\ 0\end{array}\right]\right\}$

**Exercise 2** (6.4.12)

Find an orthogonal basis for the column space of the following matrix:

$\left[\begin{array}{rrr}1 & 3 & 5 \\ -1 & -3 & 1 \\ 0 & 2 & 3 \\ 1 & 5 & 2 \\ 1 & 5 & 8\end{array}\right]$

??? answer "&nbsp;"
    $\left\{\left[\begin{array}{r}1 \\ -1 \\ 0 \\ 1 \\ 1\end{array}\right],\left[\begin{array}{r}-1 \\ 1 \\ 2 \\ 1 \\ 1\end{array}\right],\left[\begin{array}{r}3 \\ 3 \\ 0 \\ -3 \\ 3\end{array}\right]\right\}$

**Exercise 3** (6.4.24)

[M] Use the Gram-Schmidt process as in Example 2 to produce an orthogonal basis for the column space of

$$
A=\left[\begin{array}{rrrr}
-10 & 13 & 7 & -11 \\
2 & 1 & -5 & 3 \\
-6 & 3 & 13 & -3 \\
16 & -16 & -2 & 5 \\
2 & 1 & -5 & -7
\end{array}\right]
$$

??? answer "&nbsp;"
    $\left\{\left[\begin{array}{r}-10 \\ 2 \\ -6 \\ 16 \\ 2\end{array}\right],\left[\begin{array}{r}3 \\ 3 \\ -3 \\ 0 \\ 3\end{array}\right],\left[\begin{array}{l}6 \\ 0 \\ 6 \\ 6 \\ 0\end{array}\right],\left[\begin{array}{r}0 \\ 5 \\ 0 \\ 0 \\ -5\end{array}\right]\right\}$

**Exercise 4** (6.5.1, 6.5.3) <!-- NOTE: Formulation may be a bit confusing because we are using a and b also for labeling the exercises -->

Find a least-squares solution of $A \mathbf{x}=\mathbf{b}$ by (a) constructing the normal equations for $\hat{\mathbf{x}}$ and (b) solving for $\hat{\mathbf{x}}$.

1. $A=\left[\begin{array}{rr}-1 & 2 \\ 2 & -3 \\ -1 & 3\end{array}\right], \mathbf{b}=\left[\begin{array}{l}4 \\ 1 \\ 2\end{array}\right]$
3. $A=\left[\begin{array}{rr}1 & -2 \\ -1 & 2 \\ 0 & 3 \\ 2 & 5\end{array}\right], \mathbf{b}=\left[\begin{array}{r}3 \\ 1 \\ -4 \\ 2\end{array}\right]$

??? answer "&nbsp;"
    1. 

        (a) The normal equations are $\left(A^T A\right) \mathbf{x}=A^T \mathbf{b}:\left[\begin{array}{rr}6 & -11 \\ -11 & 22\end{array}\right]\left[\begin{array}{c}x_1 \\ x_2\end{array}\right]=\left[\begin{array}{c}-4 \\ 11\end{array}\right]$.

        (b) $\frac{1}{11}\left[\begin{array}{l}33 \\ 22\end{array}\right]=\left[\begin{array}{l}3 \\ 2\end{array}\right]$

    3. 

        (a) The normal equations are $\left(A^T A\right) \mathbf{x}=A^T \mathbf{b}:\left[\begin{array}{rr}6 & 6 \\ 6 & 42\end{array}\right]\left[\begin{array}{l}x_1 \\ x_2\end{array}\right]=\left[\begin{array}{r}6 \\ -6\end{array}\right]$
        
        (b) $\frac{1}{216}\left[\begin{array}{l}288 \\ -72\end{array}\right]=\left[\begin{array}{r}4 / 3 \\ -1 / 3\end{array}\right]$



**Exercise 5** (6.5.5)

Describe all least-squares solutions of the equation $A \mathbf{x}=\mathbf{b}$.

$A=\left[\begin{array}{lll}1 & 1 & 0 \\ 1 & 1 & 0 \\ 1 & 0 & 1 \\ 1 & 0 & 1\end{array}\right], \mathbf{b}=\left[\begin{array}{l}1 \\ 3 \\ 8 \\ 2\end{array}\right]$

??? answer "&nbsp;"
    all vectors of the form $\hat{\mathbf{x}}=\left[\begin{array}{r}5 \\ -3 \\ 0\end{array}\right]+x_3\left[\begin{array}{r}-1 \\ 1 \\ 1\end{array}\right]$ are the least-squares solutions of $A \mathbf{x}=\mathbf{b}$.

**Exercise 6** (6.5.7)

Compute the least-squares error associated with the leastsquares solution found in Exercise 4b.

??? answer "&nbsp;"
    The least squares error is $\|A \hat{\mathbf{x}}-\mathbf{b}\|=\sqrt{20}=2 \sqrt{5}$.

**Exercise 7** (6.5.12)

Find 

1. The orthogonal projection of $\mathbf{b}$ onto $\mathrm{Col} A$ and 
2. A least-squares solution of $A \mathbf{x}=\mathbf{b}$.

$A=\left[\begin{array}{rrr}1 & 1 & 0 \\ 1 & 0 & -1 \\ 0 & 1 & 1 \\ -1 & 1 & -1\end{array}\right], \mathbf{b}=\left[\begin{array}{l}2 \\ 5 \\ 6 \\ 6\end{array}\right]$

??? answer "&nbsp;"
    1. $\frac{1}{3}\left[\begin{array}{c}1 \\ 1 \\ 0 \\ -1\end{array}\right]+\frac{14}{3}\left[\begin{array}{l}1 \\ 0 \\ 1 \\ 1\end{array}\right]-\frac{5}{3}\left[\begin{array}{c}0 \\ -1 \\ 1 \\ -1\end{array}\right]=\left[\begin{array}{l}5 \\ 2 \\ 3 \\ 6\end{array}\right]$

    2. $\hat{\mathbf{x}}=\left[\begin{array}{r}1 / 3 \\ 14 / 3 \\ -5 / 3\end{array}\right]$

**Exercise 8** (6.5.25)

Describe all least-squares solutions of the system

$$
\begin{aligned}
& x+y=2 \\
& x+y=4
\end{aligned}
$$

??? answer "&nbsp;"
    The normal equations are $\left[\begin{array}{ll}2 & 2 \\ 2 & 2\end{array}\right]\left[\begin{array}{l}x \\ y\end{array}\right]=\left[\begin{array}{l}6 \\ 6\end{array}\right]$, whose solution is the set of all $(x, y)$ such that $x+y=$ 3. The solutions correspond to the points on the line midway between the lines $x+y=2$ and $x+y=$ 4.

**Exercise 9** (6.6.3-6.6.4)

Find the equation $y=\beta_0+\beta_1 x$ of the leastsquares line that best fits the given data points.

3. $(-1,0),(0,1),(1,2),(2,4)$
4. $(2,3),(3,2),(5,1),(6,0)$

??? answer "&nbsp;"
    3. The least-squares line $y=\beta_0+\beta_1 x$ is thus $y=1.1+1.3 x$.
    4. The least-squares line $y=\beta_0+\beta_1 x$ is thus $y=4.3-.7 x$.

**Exercise 10** (6.6.7)

A certain experiment produces the data $(1,1.8),(2,2.7)$, $(3,3.4),(4,3.8),(5,3.9)$. Describe the model that produces a least-squares fit of these points by a function of the form $y=\beta_1 x+\beta_2 x^2$
Such a function might arise, for example, as the revenue from the sale of $x$ units of a product, when the amount offered for sale affects the price to be set for the product.

1. Give the design matrix, the observation vector, and the unknown parameter vector.
2. [M] Find the associated least-squares curve for the data.

??? answer "&nbsp;"
    1. $\mathbf{y}=X \beta+\epsilon$, where $X=\left[\begin{array}{rr}1 & 1 \\ 2 & 4 \\ 3 & 9 \\ 4 & 16 \\ 5 & 25\end{array}\right], \mathbf{y}=\left[\begin{array}{l}1.8 \\ 2.7 \\ 3.4 \\ 3.8 \\ 3.9\end{array}\right], {\beta}=\left[\begin{array}{l}\beta_1 \\ \beta_2\end{array}\right]$, and $\epsilon=\left[\begin{array}{l}\epsilon_1 \\ \epsilon_2 \\ \epsilon_3 \\ \epsilon_4 \\ \epsilon_5\end{array}\right]$

    2. [M] One computes that (to two decimal places) $\hat{{\beta}}=\left[\begin{array}{c}1.76 \\ -.20\end{array}\right]$, so the desired least-squares equation is $y=1.76 x-.20 x^2$.

**Exercise 11** (6.6.13)

[M] To measure the takeoff performance of an airplane, the horizontal position of the plane was measured every second, from $t=0$ to $t=12$. The positions (in feet) were: $0,8.8$, $29.9,62.0,104.7,159.1,222.0,294.5,380.4,471.1,571.7$, 686.8 , and 809.2.

1. Find the least-squares cubic curve $y=\beta_0+\beta_1 t+$ $\beta_2 t^2+\beta_3 t^3$ for these data.
2. Use the result of part (a) to estimate the velocity of the plane when $t=4.5$ seconds.

??? answer "&nbsp;"
    1. The desired least-squares polynomial is $y(t)=-.8558+4.7025 t+5.5554 t^2-.0274 t^3$.
    2. The velocity $v(t)$ is the derivative of the position function $y(t)$, so $v(t)=4.7025+11.1108 t-.0822 t^2$, and $v(4.5)=53.0 \mathrm{ft} / \mathrm{sec}$.
