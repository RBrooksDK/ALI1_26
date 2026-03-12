<h1 align="center">Change of Basis</h1>

## Session Material:

Lay: 4.4, 4.7

[Recap and Exercises](https://drive.google.com/file/d/1u7TprwMubz5ntzuN5FoVVzdoYz50S0uU/view?usp=sharing)

[Session Notes](https://drive.google.com/file/d/1h-S7ivJiycrIPS66p_neczeViHX23X3V/view?usp=sharing)

[Session Material](https://viaucdk-my.sharepoint.com/:f:/g/personal/rib_viauc_dk/IgCFhq7FZrJJQorMNZVGauVfAYSd9oYjWJr1r3VBA5lJdEQ?e=ikCFi9)

### Session Recording

<div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%; overflow: hidden;">
    <iframe 
        src="https://drive.google.com/file/d/1KVLd4MxZ0IeJqc9mZOpzbBTGEp8-uNo8/preview" 
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
        allow="autoplay; encrypted-media" 
        allowfullscreen>
    </iframe>
</div>

---

## Session Description

This session explores the concept of coordinate mappings and change of basis. We'll learn how to represent vectors in different coordinate systems and understand how changing from one basis to another affects the representation of vectors and linear transformations.

We'll start by understanding coordinate vectors relative to a basis, then learn how to construct the change-of-coordinates matrix that allows us to convert between different coordinate systems. This is fundamental for understanding how the same vector or transformation can be represented differently depending on the chosen basis.

### Key Concepts

* Coordinate Vectors
* Coordinate Mappings
* Change-of-Coordinates Matrix
* Change of Basis
* Matrix Representations in Different Bases

!!! tip "Learning Objectives"

    - Represent vectors as coordinate vectors relative to a given basis.
    - Construct and use the change-of-coordinates matrix.
    - Convert between coordinate systems using change of basis.
    - Understand how linear transformations are represented in different bases.
    - Apply change of basis to solve problems involving coordinate systems.

---

<style type="text/css">
    ol { list-style-type: lower-alpha; }
</style>

## Exercises


**Exercise 1** (4.4.3)

Find the vector \(\mathbf{x}\) determined by the coordinate vector \([\mathbf{x}]_{\mathcal{B}}\) and the basis \(\mathcal{B}\).

\(\mathcal{B}=\left\{\left[\begin{array}{r}1 \\ -2 \\ 3\end{array}\right],\left[\begin{array}{r}5 \\ 0 \\ -2\end{array}\right],\left[\begin{array}{r}4 \\ -3 \\ 0\end{array}\right]\right\},[\mathbf{x}]_{\mathcal{B}}=\left[\begin{array}{r}1 \\ 0 \\ -2\end{array}\right]\)


??? answer "&nbsp;"
    \(=\left[\begin{array}{r}-7 \\ 4 \\ 3\end{array}\right]\)

**Exercises 2** (4.4.7)

Find the coordinate vector \([\mathbf{x}]_{\mathcal{B}}\) of \(\mathbf{x}\) relative to the basis \(\mathcal{B}=\left\{\mathbf{b}_1, \ldots, \mathbf{b}_n\right\}\).

\(\mathbf{b}_1=\left[\begin{array}{r}1 \\ -1 \\ -3\end{array}\right], \mathbf{b}_2=\left[\begin{array}{r}-3 \\ 4 \\ 9\end{array}\right], \mathbf{b}_3=\left[\begin{array}{r}2 \\ -2 \\ 4\end{array}\right], \mathbf{x}=\left[\begin{array}{r}8 \\ -9 \\ 6\end{array}\right]\)

??? answer "&nbsp;"
    \([\mathbf{x}]_{\mathcal{B}}=\left[\begin{array}{r}-1 \\ -1 \\ 3\end{array}\right]\)

**Exercises 3** (4.4.10)

Find the change-of-coordinates matrix from \(\mathcal{B}\) to the standard basis in \(\mathbb{R}^n\).

\(\mathcal{B}=\left\{\left[\begin{array}{l}3 \\ 0 \\ 6\end{array}\right],\left[\begin{array}{r}2 \\ 2 \\ -4\end{array}\right],\left[\begin{array}{r}1 \\ -2 \\ 3\end{array}\right]\right\}\)


??? answer "&nbsp;"
    \(P_B = \left[\begin{array}{rrr}3 & 2 & 1 \\ 0 & 2 & -2 \\ 6 & -4 & 3\end{array}\right]\)

**Exercises 4** (4.4.17)

The vectors \(\mathbf{v}_1=\left[\begin{array}{r}1 \\ -3\end{array}\right], \mathbf{v}_2=\left[\begin{array}{r}2 \\ -8\end{array}\right], \mathbf{v}_3=\left[\begin{array}{r}-3 \\ 7\end{array}\right] \operatorname{span} \mathbb{R}^2\) but do not form a basis. Find two different ways to express \(\left[\begin{array}{l}1 \\ 1\end{array}\right]\) as a linear combination of \(\mathbf{v}_1, \mathbf{v}_2, \mathbf{v}_3\).

??? answer "&nbsp;"
    There are infinitely many correct answers to this problem. One possible answer is:

    \(5 \mathbf{v}_1-2 \mathbf{v}_2\) and \(10 \mathbf{v}_1-3 \mathbf{v}_2+\mathbf{v}_3\).

    There are also infinitely many incorrect answers to this problem!

**Exercises 5** (4.4.32)

Let \(\mathbf{p}_1(t)=1+t^2, \mathbf{p}_2(t)=t-3 t^2, \mathbf{p}_3(t)=1+t-3 t^2\).

1. Use coordinate vectors to show that these polynomials form a basis for \(\mathbb{P}_2\).

2. Consider the basis \(\mathcal{B}=\left\{\mathbf{p}_1, \mathbf{p}_2, \mathbf{p}_3\right\}\) for \(\mathbb{P}_2\). Find \(\mathbf{q}\) in \(\mathbb{P}_2\), given that \([\mathbf{q}]_{\mathcal{B}}=\left[\begin{array}{r}-1 \\ 1 \\ 2\end{array}\right]\).

??? answer "&nbsp;"
    1. Row reduce to check for pivots
    
    2. \(\mathbf{q}(t)=1+3 t-10 t^2\).

**Exercises 6** (4.7.2)

Let \(\mathcal{B}=\left\{\mathbf{b}_1, \mathbf{b}_2\right\}\) and \(\mathcal{C}=\left\{\mathbf{c}_1, \mathbf{c}_2\right\}\) be bases for a vector space \(V\), and suppose \(\mathbf{b}_1=-2 \mathbf{c}_1+4 \mathbf{c}_2\) and \(\mathbf{b}_2=3 \mathbf{c}_1-6 \mathbf{c}_2\).

1. Find the change-of-coordinates matrix from \(\mathcal{B}\) to \(\mathcal{C}\).

2. Find \([\mathbf{x}]_{\mathcal{C}}\) for \(\mathbf{x}=2 \mathbf{b}_1+3 \mathbf{b}_2\).

??? answer "&nbsp;"
    1. \(\underset{C \leftarrow B}{P}=\left[\begin{array}{rr}-2 & 3 \\ 4 & -6\end{array}\right]\).

    2. \([\mathbf{x}]_C=\left[\begin{array}{r}5 \\ -10\end{array}\right]\)

**Exercises 7** (4.7.14)

In \(\mathbb{P}_2\), find the change-of-coordinates matrix from the basis \(\mathcal{B}=\left\{1-3 t^2, 2+t-5 t^2, 1+2 t\right\}\) to the standard basis. Then write \(t^2\) as a linear combination of the polynomials in \(\mathcal{B}\).

??? answer "&nbsp;"
    \(t^2=3\left(1-3 t^2\right)-2\left(2+t-5 t^2\right)+(1+2 t)\)

**Exercises 8** (4.7.19)

[M] Let

$$
\begin{aligned}
& P=\left[\begin{array}{rrr}
1 & 2 & -1 \\
-3 & -5 & 0 \\
4 & 6 & 1
\end{array}\right], \\
& \mathbf{v}_1=\left[\begin{array}{r}
-2 \\
2 \\
3
\end{array}\right], \mathbf{v}_2=\left[\begin{array}{r}
-8 \\
5 \\
2
\end{array}\right], \mathbf{v}_3=\left[\begin{array}{r}
-7 \\
2 \\
6
\end{array}\right]
\end{aligned}
$$

1. Find a basis \(\left\{\mathbf{u}_1, \mathbf{u}_2, \mathbf{u}_3\right\}\) for \(\mathbb{R}^3\) such that \(P\) is the change-of-coordinates matrix from \(\left\{\mathbf{u}_1, \mathbf{u}_2, \mathbf{u}_3\right\}\) to the basis \(\left\{\mathbf{v}_1, \mathbf{v}_2, \mathbf{v}_3\right\}\). [Hint: What do the columns of \({ }_{\mathcal{C} \leftarrow \mathcal{B}}\) represent?]

2. Find a basis \(\left\{\mathbf{w}_1, \mathbf{w}_2, \mathbf{w}_3\right\}\) for \(\mathbb{R}^3\) such that \(P\) is the change-of-coordinates matrix from \(\left\{\mathbf{v}_1, \mathbf{v}_2, \mathbf{v}_3\right\}\) to \(\left\{\mathbf{w}_1, \mathbf{w}_2, \mathbf{w}_3\right\}\).

??? answer "&nbsp;"
    1. \(\left[\begin{array}{rrr}-6 & -6 & -5 \\ -5 & -9 & 0 \\ 21 & 32 & 3\end{array}\right]\).

    2. \(\left[\begin{array}{rrr}28 & 38 & 21 \\ -9 & -13 & -7 \\ -3 & 2 & 3\end{array}\right]\)
