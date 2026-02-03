<h1 align="center">Orthogonality I</h1>

## Session Material:

Lay: 6.1-6.3

[Recap and Exercises](https://drive.google.com/file/d/1-dTU3V-AQwzTVMj91JG1BigrllA5Cze9/view?usp=sharing)

[Session Notes](https://drive.google.com/file/d/1zXPM_pQHZRK51D9d-J4pQj6p3l8ExaRX/view?usp=sharing)

[Session Material](https://viaucdk-my.sharepoint.com/:f:/g/personal/rib_viauc_dk/EsTiRlgRBLpMku31mwnbViIBHTOgpvFeUWhBaN0WGJJMkA?e=KYrKvB)

---

## Session Description

Let's add some geometry back into our vector spaces! This session introduces the idea of the "inner product" (or dot product in $\mathbb{R}^n$) as a way to measure things like the "length" of a vector and the "distance" between vectors. Most importantly, it gives us a precise way to define "orthogonal" (or perpendicular) vectors. We'll explore orthogonal complements – the set of all vectors truly perpendicular to a given subspace, and see how they connect fundamental spaces we've already studied.

Building on this, we'll look at "orthogonal sets" of vectors, where every pair is perpendicular. These sets are really special because they're automatically linearly independent, and if they also span the space, they form an "orthogonal basis" – which makes finding coordinates ridiculously easy! Finally, we'll learn how to "orthogonally project" a vector onto a subspace. Think of this as finding the closest point in that subspace to the original vector, a super useful tool with lots of applications (related to the Best Approximation Theorem).

### Key Concepts

* Inner Product / Dot Product
* Vector Length and Distance
* Orthogonal Vectors, Complements, Sets, Bases, and Projection
* Best Approximation

!!! tip "Learning Objectives"

    - Compute inner products, vector lengths, and distances in vector spaces.
    - Identify and construct orthogonal and orthonormal sets and bases.
    - Determine orthogonal complements and analyze their properties.
    - Apply orthogonal projection to find best approximations in subspaces.
    - Interpret the geometric meaning of orthogonality in linear algebra.

---

## Exercises

<style type="text/css">
    ol { list-style-type: lower-alpha; }
</style>

**Exercise 0**

[Do this exercise first.pdf](https://viaucdk-my.sharepoint.com/:b:/g/personal/rib_viauc_dk/EfVeTGnf_6dGu4Pozd45Z1gBf86W3BOdPiSdvMvwO4XHUw?e=cs0QrB)


**Exercise 1** (6.1.1)

Compute the quantities using the vectors

$$
\mathbf{u}=\left[\begin{array}{r}
-1 \\
2
\end{array}\right], \quad \mathbf{v}=\left[\begin{array}{l}
4 \\
6
\end{array}\right], \quad \mathbf{w}=\left[\begin{array}{r}
3 \\
-1 \\
-5
\end{array}\right], \quad \mathbf{x}=\left[\begin{array}{r}
6 \\
-2 \\
3
\end{array}\right]
$$

$\mathbf{u} \cdot \mathbf{u}, \mathbf{v} \cdot \mathbf{u}$, and $\frac{\mathbf{v} \cdot \mathbf{u}}{\mathbf{u} \cdot \mathbf{u}}$

??? answer "&nbsp;"
    $\mathbf{u} \cdot \mathbf{u}=(-1)^2+2^2=5, \mathbf{v} \cdot \mathbf{u}=4(-1)+6(2)=8$, and $\frac{\mathbf{v} \cdot \mathbf{u}}{\mathbf{u} \cdot \mathbf{u}}=\frac{8}{5}$.


**Exercise 2** (6.1.11)

Find a unit vector in the direction of the given vector.

$\left[\begin{array}{c}7 / 4 \\ 1 / 2 \\ 1\end{array}\right]$

??? answer "&nbsp;"
    $\frac{1}{\sqrt{(7 / 4)^2+(1 / 2)^2+1^2}}\left[\begin{array}{r}7 / 4 \\ 1 / 2 \\ 1\end{array}\right]=\frac{1}{\sqrt{69 / 16}}\left[\begin{array}{r}7 / 4 \\ 1 / 2 \\ 1\end{array}\right]=\left[\begin{array}{l}7 / \sqrt{69} \\ 2 / \sqrt{69} \\ 4 / \sqrt{69}\end{array}\right]$

**Exercise 3** (6.1.13)

Find the distance between $\mathbf{x}=\left[\begin{array}{r}10 \\ -3\end{array}\right]$ and $\mathbf{y}=\left[\begin{array}{l}-1 \\ -5\end{array}\right]$.

??? answer "&nbsp;"
    Since $\mathbf{x}=\left[\begin{array}{c}10 \\ -3\end{array}\right]$ and $\mathbf{y}=\left[\begin{array}{l}-1 \\ -5\end{array}\right],\|\mathbf{x}-\mathbf{y}\|^2=[10-(-1)]^2+[-3-(-5)]^2=125$ and $\operatorname{dist}(\mathbf{x}, \mathbf{y})=\sqrt{125}=5 \sqrt{5}$.

**Exercise 4** (6.1.15-6.1.18)

Determine which pairs of vectors in the following exercises are orthogonal.

1.  $\mathbf{a}=\left[\begin{array}{r}8 \\ -5\end{array}\right], \mathbf{b}=\left[\begin{array}{l}-2 \\ -3\end{array}\right]$
2.  $\mathbf{u}=\left[\begin{array}{r}12 \\ 3 \\ -5\end{array}\right], \mathbf{v}=\left[\begin{array}{r}2 \\ -3 \\ 3\end{array}\right]$
3.  $\mathbf{u}=\left[\begin{array}{r}3 \\ 2 \\ -5 \\ 0\end{array}\right], \mathbf{v}=\left[\begin{array}{r}-4 \\ 1 \\ -2 \\ 6\end{array}\right]$
4.  $\mathbf{y}=\left[\begin{array}{r}-3 \\ 7 \\ 4 \\ 0\end{array}\right], \mathbf{z}=\left[\begin{array}{r}1 \\ -8 \\ 15 \\ -7\end{array}\right]$

??? answer "&nbsp;"
    15. Since $\mathbf{a} \cdot \mathbf{b}=8(-2)+(-5)(-3)=-1 \neq 0, \mathbf{a}$ and $\mathbf{b}$ are not orthogonal.
    16. Since $\mathbf{u} \cdot \mathbf{v}=12(2)+(3)(-3)+(-5)(3)=0, \mathbf{u}$ and $\mathbf{v}$ are orthogonal.
    17. Since $\mathbf{u} \cdot \mathbf{v}=3(-4)+2(1)+(-5)(-2)+0(6)=0, \mathbf{u}$ and $\mathbf{v}$ are orthogonal.
    18. Since $\mathbf{y} \cdot \mathbf{z}=(-3)(1)+7(-8)+4(15)+0(-7)=1 \neq 0, \mathbf{y}$ and $\mathbf{z}$ are not orthogonal.

**Exercise 5** (6.2.1)

Determine whether the set of vectors is orthogonal.

$\left[\begin{array}{r}-1 \\ 4 \\ -3\end{array}\right],\left[\begin{array}{l}5 \\ 2 \\ 1\end{array}\right],\left[\begin{array}{r}3 \\ -4 \\ -7\end{array}\right]$

??? answer "&nbsp;"
    Since $\left[\begin{array}{r}-1 \\ 4 \\ -3\end{array}\right] \cdot\left[\begin{array}{r}3 \\ -4 \\ -7\end{array}\right]=2 \neq 0$, the set is not orthogonal.

**Exercise 6** (6.2.9)

Show that $\left\{\mathbf{u}_1, \mathbf{u}_2\right\}$ or $\left\{\mathbf{u}_1, \mathbf{u}_2, \mathbf{u}_3\right\}$ is an orthogonal basis for $\mathbf{R}^2$ or $\mathbf{R}^3$, respectively. Then express $\mathbf{x}$ as a linear combination of the u's.

$\mathbf{u}_1=\left[\begin{array}{l}1 \\ 0 \\ 1\end{array}\right], \mathbf{u}_2=\left[\begin{array}{r}-1 \\ 4 \\ 1\end{array}\right], \mathbf{u}_3=\left[\begin{array}{r}2 \\ 1 \\ -2\end{array}\right]$, and $\mathbf{x}=\left[\begin{array}{r}8 \\ -4 \\ -3\end{array}\right]$

??? answer "&nbsp;"
    Since $\mathbf{u}_1 \cdot \mathbf{u}_2=\mathbf{u}_1 \cdot \mathbf{u}_3=\mathbf{u}_2 \cdot \mathbf{u}_3=0,\left\{\mathbf{u}_1, \mathbf{u}_2, \mathbf{u}_3\right\}$ is an orthogonal set. Since the vectors are non-zero, $\mathbf{u}_1, \mathbf{u}_2$, and $\mathbf{u}_3$ are linearly independent by Theorem 4. Three such vectors in $\mathbb{R}^3$ automatically form a basis for $\mathbb{R}^3$. So $\left\{\mathbf{u}_1, \mathbf{u}_2, \mathbf{u}_3\right\}$ is an orthogonal basis for $\mathbb{R}^3$. By Theorem 5,

    $$
    \mathbf{x}=\frac{\mathbf{x} \cdot \mathbf{u}_1}{\mathbf{u}_1 \cdot \mathbf{u}_1} \mathbf{u}_1+\frac{\mathbf{x} \cdot \mathbf{u}_2}{\mathbf{u}_2 \cdot \mathbf{u}_2} \mathbf{u}_2+\frac{\mathbf{x} \cdot \mathbf{u}_3}{\mathbf{u}_3 \cdot \mathbf{u}_3} \mathbf{u}_3=\frac{5}{2} \mathbf{u}_1-\frac{3}{2} \mathbf{u}_2+2 \mathbf{u}_3
    $$

**Exercise 7** (6.2.12)

Compute the orthogonal projection of $\left[\begin{array}{r}1 \\ -1\end{array}\right]$ onto the line through $\left[\begin{array}{r}-1 \\ 3\end{array}\right]$ and the origin.

??? answer "&nbsp;"
    $\hat{\mathbf{y}}=\frac{\mathbf{y} \cdot \mathbf{u}}{\mathbf{u} \cdot \mathbf{u}} \mathbf{u}=-\frac{2}{5} \mathbf{u}=\left[\begin{array}{r}2 / 5 \\ -6 / 5\end{array}\right]$

**Exercise 8** (6.2.21)

Determine whether the set of vectors is orthonormal. If the set is only orthogonal, normalize the vectors to produce an orthonormal set.

$\left[\begin{array}{l}1 / \sqrt{10} \\ 3 / \sqrt{20} \\ 3 / \sqrt{20}\end{array}\right],\left[\begin{array}{c}3 / \sqrt{10} \\ -1 / \sqrt{20} \\ -1 / \sqrt{20}\end{array}\right],\left[\begin{array}{c}0 \\ -1 / \sqrt{2} \\ 1 / \sqrt{2}\end{array}\right]$

??? answer "&nbsp;"
    Let $\mathbf{u}=\left[\begin{array}{l}1 / \sqrt{10} \\ 3 / \sqrt{20} \\ 3 / \sqrt{20}\end{array}\right], \mathbf{v}=\left[\begin{array}{r}3 / \sqrt{10} \\ -1 / \sqrt{20} \\ -1 / \sqrt{20}\end{array}\right]$, and $\mathbf{w}=\left[\begin{array}{r}0 \\ -1 / \sqrt{2} \\ 1 / \sqrt{2}\end{array}\right]$. Since $\mathbf{u} \cdot \mathbf{v}=\mathbf{u} \cdot \mathbf{w}=\mathbf{v} \cdot \mathbf{w}=0,\{\mathbf{u}, \mathbf{v}, \mathbf{w}\}$ is an orthogonal set. Also, $\|\mathbf{u}\|^2=\mathbf{u} \cdot \mathbf{u}=1,\|\mathbf{v}\|^2=\mathbf{v} \cdot \mathbf{v}=1$, and $\|\mathbf{w}\|^2=\mathbf{w} \cdot \mathbf{w}=1$, so $\{\mathbf{u}, \mathbf{v}, \mathbf{w}\}$ is an orthonormal set.

**Exercise 9** (6.2.35)

[M] Show that the columns of the matrix $A$ are orthogonal by making an appropriate matrix calculation. State the calculation you use.

$A=\left[\begin{array}{rrrr}-6 & -3 & 6 & 1 \\ -1 & 2 & 1 & -6 \\ 3 & 6 & 3 & -2 \\ 6 & -3 & 6 & -1 \\ 2 & -1 & 2 & 3 \\ -3 & 6 & 3 & 2 \\ -2 & -1 & 2 & -3 \\ 1 & 2 & 1 & 6\end{array}\right]$

??? answer "&nbsp;"
    [M] One can compute that $A^T A=100 I_4$. Since the off-diagonal entries in $A^T A$ are zero, the columns of $A$ are orthogonal.

**Exercise 10** (6.3.1)

You may assume that $\left\{\mathbf{u}_1, \ldots, \mathbf{u}_4\right\}$ is an orthogonal basis for $\mathbb{R}^4$.

$\mathbf{u}_1=\left[\begin{array}{r}0 \\ 1 \\ -4 \\ -1\end{array}\right], \mathbf{u}_2=\left[\begin{array}{l}3 \\ 5 \\ 1 \\ 1\end{array}\right], \mathbf{u}_3=\left[\begin{array}{r}1 \\ 0 \\ 1 \\ -4\end{array}\right], \mathbf{u}_4=\left[\begin{array}{r}5 \\ -3 \\ -1 \\ 1\end{array}\right]$, $\mathbf{x}=\left[\begin{array}{r}10 \\ -8 \\ 2 \\ 0\end{array}\right]$. 

Write $\mathbf{x}$ as the sum of two vectors, one in
$\operatorname{Span}\left\{\mathbf{u}_1, \mathbf{u}_2, \mathbf{u}_3\right\}$ and the other in Span $\left\{\mathbf{u}_4\right\}$.

??? answer "&nbsp;"
    $\mathbf{x}-\frac{\mathbf{x} \cdot \mathbf{u}_4}{\mathbf{u}_4 \cdot \mathbf{u}_4} \mathbf{u}_4=\left[\begin{array}{r}10 \\ -8 \\ 2 \\ 0\end{array}\right]-\left[\begin{array}{r}10 \\ -6 \\ -2 \\ 2\end{array}\right]=\left[\begin{array}{r}0 \\ -2 \\ 4 \\ -2\end{array}\right]$

**Exercise 11** (6.3.3)

Verify that $\left\{\mathbf{u}_1, \mathbf{u}_2\right\}$ is an orthogonal set, and then find the orthogonal projection of $\mathbf{y}$ onto $\operatorname{Span}\left\{\mathbf{u}_1, \mathbf{u}_2\right\}$.

$\mathbf{y}=\left[\begin{array}{r}-1 \\ 4 \\ 3\end{array}\right], \mathbf{u}_1=\left[\begin{array}{l}1 \\ 1 \\ 0\end{array}\right], \mathbf{u}_2=\left[\begin{array}{r}-1 \\ 1 \\ 0\end{array}\right]$

??? answer "&nbsp;"
    Since $\mathbf{u}_1 \cdot \mathbf{u}_2=-1+1+0=0,\left\{\mathbf{u}_1, \mathbf{u}_2\right\}$ is an orthogonal set. The orthogonal projection of $\mathbf{y}$ onto $\operatorname{Span}\left\{\mathbf{u}_1, \mathbf{u}_2\right\}$ is

    $$
    \hat{\mathbf{y}}=\frac{\mathbf{y} \cdot \mathbf{u}_1}{\mathbf{u}_1 \cdot \mathbf{u}_1} \mathbf{u}_1+\frac{\mathbf{y} \cdot \mathbf{u}_2}{\mathbf{u}_2 \cdot \mathbf{u}_2} \mathbf{u}_2=\frac{3}{2} \mathbf{u}_1+\frac{5}{2} \mathbf{u}_2=\frac{3}{2}\left[\begin{array}{l}
    1 \\
    1 \\
    0
    \end{array}\right]+\frac{5}{2}\left[\begin{array}{r}
    -1 \\
    1 \\
    0
    \end{array}\right]=\left[\begin{array}{r}
    -1 \\
    4 \\
    0
    \end{array}\right]
    $$


**Exercise 12** (6.3.7)

Let $W$ be the subspace spanned by the $\mathbf{u}$ 's, and write $y$ as the sum of a vector in $W$ and a vector orthogonal to $W$.

$\mathbf{y}=\left[\begin{array}{l}1 \\ 3 \\ 5\end{array}\right], \mathbf{u}_1=\left[\begin{array}{r}1 \\ 3 \\ -2\end{array}\right], \mathbf{u}_2=\left[\begin{array}{l}5 \\ 1 \\ 4\end{array}\right]$

??? answer "&nbsp;"
    $\hat{\mathbf{y}}=\frac{\mathbf{y} \cdot \mathbf{u}_1}{\mathbf{u}_1 \cdot \mathbf{u}_1} \mathbf{u}_1+\frac{\mathbf{y} \cdot \mathbf{u}_2}{\mathbf{u}_2 \cdot \mathbf{u}_2} \mathbf{u}_2=0 \mathbf{u}_1+\frac{2}{3} \mathbf{u}_2=\left[\begin{array}{r}10 / 3 \\ 2 / 3 \\ 8 / 3\end{array}\right], \mathbf{z}=\mathbf{y}-\hat{\mathbf{y}}=\left[\begin{array}{r}-7 / 3 \\ 7 / 3 \\ 7 / 3\end{array}\right]$

**Exercise 13** (6.3.13)

Find the best approximation to $\mathbf{z}$ by vectors of the form $c_1 \mathbf{v}_1+c_2 \mathbf{v}_2$.

$\mathbf{z}=\left[\begin{array}{r}3 \\ -7 \\ 2 \\ 3\end{array}\right], \mathbf{v}_1=\left[\begin{array}{r}2 \\ -1 \\ -3 \\ 1\end{array}\right], \mathbf{v}_2=\left[\begin{array}{r}1 \\ 1 \\ 0 \\ -1\end{array}\right]$

??? answer "&nbsp;"
    $\hat{\mathbf{z}}=\frac{\mathbf{z} \cdot \mathbf{v}_1}{\mathbf{v}_1 \cdot \mathbf{v}_1} \mathbf{v}_1+\frac{\mathbf{z} \cdot \mathbf{v}_2}{\mathbf{v}_2 \cdot \mathbf{v}_2} \mathbf{v}_2=\frac{2}{3} \mathbf{v}_1-\frac{7}{3} \mathbf{v}_2=\left[\begin{array}{c}-1 \\ -3 \\ -2 \\ 3\end{array}\right]$

**Exercise 14** (6.3.17)

Let $\mathbf{y}=\left[\begin{array}{l}4 \\ 8 \\ 1\end{array}\right], \quad \mathbf{u}_1=\left[\begin{array}{l}2 / 3 \\ 1 / 3 \\ 2 / 3\end{array}\right], \quad \mathbf{u}_2=\left[\begin{array}{r}-2 / 3 \\ 2 / 3 \\ 1 / 3\end{array}\right], \quad$ and
$W=\operatorname{Span}\left\{\mathbf{u}_1, \mathbf{u}_2\right\}$.

1. Let $U=\left[\begin{array}{ll}\mathbf{u}_1 & \mathbf{u}_2\end{array}\right]$. Compute $U^T U$ and $U U^T$.
2. Compute $\operatorname{proj}_W \mathbf{y}$ and $\left(U U^T\right) \mathbf{y}$.

??? answer "&nbsp;"
    1. $U^T U=\left[\begin{array}{ll}1 & 0 \\ 0 & 1\end{array}\right], U U^T=\left[\begin{array}{rrr}8 / 9 & -2 / 9 & 2 / 9 \\ -2 / 9 & 5 / 9 & 4 / 9 \\ 2 / 9 & 4 / 9 & 5 / 9\end{array}\right]$
    2. Since $U^T U=I_2$, the columns of $U$ form an orthonormal basis for $W$, and by Theorem 10 $\operatorname{proj}_W \mathbf{y}=U U^T \mathbf{y}=\left[\begin{array}{rrr}8 / 9 & -2 / 9 & 2 / 9 \\ -2 / 9 & 5 / 9 & 4 / 9 \\ 2 / 9 & 4 / 9 & 5 / 9\end{array}\right]\left[\begin{array}{l}4 \\ 8 \\ 1\end{array}\right]=\left[\begin{array}{l}2 \\ 4 \\ 5\end{array}\right]$.