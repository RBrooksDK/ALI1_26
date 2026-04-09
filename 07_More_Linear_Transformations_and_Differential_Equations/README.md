---
tags:
    - Linear Transformations
    - Differential Equations
    - Diagonalization
    - Phase Portraits
    - Dynamical Systems
    - Change of Basis
    - Stability Analysis
    - Eigenvalues
    - Decoupling
---

<h1 align="center">More Linear Transformations and Differential Equations</h1>

## Session Material:

Lay: 5.4 and 5.7

[Recap and Exercises]()

[Session Notes](https://viaucdk-my.sharepoint.com/:b:/g/personal/rib_viauc_dk/IQBE1pM3e8ioSad4PbYjdABAAZjiaZpb1MR0bRneDMnSlrw?e=7KgHVN)

[Session Material]()

---

## Session Description
This session explores the deep connection between eigenvalues and the geometry of linear transformations, ultimately applying these tools to solve systems of **Differential Equations**. We begin by revisiting linear transformations through the lens of a basis. You will learn how to find the matrix of a transformation relative to a specific basis and how choosing the "right" basis—specifically one consisting of eigenvectors—can simplify a complex transformation into a simple diagonal matrix.

We then transition into the continuous world with **Section 5.7**, where we use these algebraic tools to solve systems of first-order linear differential equations ($\mathbf{x}' = A\mathbf{x}$). You will discover how the eigenvalues of matrix $A$ determine the long-term behavior of a dynamic system. By "decoupling" the equations using eigenvectors, we can transform a tangled system of changing variables into a set of independent, solvable equations. Finally, we will visualize these solutions using **phase portraits**, learning to identify whether a system’s origin is an attractor, a repeller, or a saddle point.

### Key Concepts

*   The Matrix of a Linear Transformation
*   Diagonal Matrix Representations ($[T]_{\mathcal{B}}$)
*   Similarity and Diagonalization
*   Systems of First-Order Differential Equations
*   Decoupling a Dynamical System
*   Fundamental Sets of Solutions
*   Phase Portraits (Attractors, Repellers, and Saddle Points)
*   Stability Analysis

!!! tip "Learning Objectives"

    - Find the matrix of a linear transformation relative to a non-standard basis.
    - Understand how similarity transformations relate different matrix representations of the same mapping.
    - Solve systems of linear differential equations using eigenvalues and eigenvectors.
    - Decouple systems of equations to find general solutions for $\mathbf{x}' = A\mathbf{x}$.
    - Construct and interpret phase portraits to describe the stability and trajectory of a system over time.
    - Relate the sign and magnitude of eigenvalues to the physical behavior of a dynamical system.

---

## Exercises

<!--
5.7: 1-8, 15, 16, 19, 20 
-->
<style type="text/css">
    ol { list-style-type: lower-alpha; }
</style>

**Exercise 1** (5.4.1)

Let $T: \mathbb{R}^2 \to \mathbb{R}^2$ be the linear transformation that rotates vectors counterclockwise by $\pi / 4$ radians. Find the matrix of $T$ relative to the standard basis $\mathcal{E}_2$.

??? answer "&nbsp;"
    $T=\left[\begin{array}{rr}\cos \frac{\pi}{4} & -\sin \frac{\pi}{4} \\ \sin \frac{\pi}{4} & \cos \frac{\pi}{4}\end{array}\right]=\left[\begin{array}{rr}\frac{\sqrt{2}}{2} & -\frac{\sqrt{2}}{2} \\ \frac{\sqrt{2}}{2} & \frac{\sqrt{2}}{2}\end{array}\right]$

**Exercise 2** (5.4.7)

Assume the mapping \(T: \mathbb{P}_2 \rightarrow \mathbb{P}_2\) defined by

$$
T\left(a_0+a_1 t+a_2 t^2\right)=3 a_0+\left(5 a_0-2 a_1\right) t+\left(4 a_1+a_2\right) t^2
$$

is linear. Find the matrix representation of \(T\) relative to the basis \(\mathcal{B}=\left\{1, t, t^2\right\}\).

??? answer "&nbsp;"
    \(\left[\begin{array}{rrr}3 & 0 & 0 \\ 5 & -2 & 0 \\ 0 & 4 & 1\end{array}\right]\)

**Exercise 3** (5.7.1)

A particle moving in a planar force field has a position vector $\mathbf{x}$ that satisfies $\mathbf{x}^{\prime}=A \mathbf{x}$. The $2 \times 2$ matrix $A$ has eigenvalues 4 and 2 , with corresponding eigenvectors $\mathbf{v}_1=\left[\begin{array}{r}-3 \\ 1\end{array}\right]$ and $\mathbf{v}_2=\left[\begin{array}{r}-1 \\ 1\end{array}\right]$. Find the position of the particle at time $t$, assuming that $\mathbf{x}(0)=\left[\begin{array}{r}-6 \\ 1\end{array}\right]$.

??? answer "&nbsp;"
    $c_1=5 / 2, c_2=-3 / 2$, and $\mathbf{x}(t)=\frac{5}{2}\left[\begin{array}{r}-3 \\ 1\end{array}\right] e^{4 t}-\frac{3}{2}\left[\begin{array}{r}-1 \\ 1\end{array}\right] e^{2 t}$

**Exercise 4** (5.7.2)

Let $A$ be a $2 \times 2$ matrix with eigenvalues -3 and -1 and corresponding eigenvectors $\mathbf{v}_1=\left[\begin{array}{r}-1 \\ 1\end{array}\right]$ and $\mathbf{v}_2=\left[\begin{array}{l}1 \\ 1\end{array}\right]$. Let $\mathbf{x}(t)$ be the position of a particle at time $t$. Solve the initial value problem $\mathbf{x}^{\prime}=A \mathbf{x}, \mathbf{x}(0)=\left[\begin{array}{l}2 \\ 3\end{array}\right]$.

??? answer "&nbsp;"
    $c_1=1 / 2, c_2=5 / 2$, and $\mathbf{x}(t)=\frac{1}{2}\left[\begin{array}{r}-1 \\ 1\end{array}\right] e^{-3 t}+\frac{5}{2}\left[\begin{array}{l}1 \\ 1\end{array}\right] e^{-t}$

**Exercise 5** (5.7.3-5.7.6)

Solve the initial value problem $\mathbf{x}^{\prime}(t)=A \mathbf{x}(t)$ for $t \geq 0$, with $\mathbf{x}(0)=(3,2)$. Classify the nature of the origin as an attractor, repeller, or saddle point of the dynamical system described by $\mathbf{x}^{\prime}=A \mathbf{x}$. Find the directions of greatest attraction and/or repulsion. When the origin is a saddle point, sketch typical trajectories.

3. $A=\left[\begin{array}{rr}2 & 3 \\ -1 & -2\end{array}\right]$
4. $A=\left[\begin{array}{rr}-2 & -5 \\ 1 & 4\end{array}\right]$
5. $A=\left[\begin{array}{rr}7 & -1 \\ 3 & 3\end{array}\right]$
6. $A=\left[\begin{array}{ll}1 & -2 \\ 3 & -4\end{array}\right]$

??? answer "&nbsp;"
    3. $c_1=-5 / 2, c_2=9 / 2$, and $\mathbf{x}(t)=-\frac{5}{2}\left[\begin{array}{r}-3 \\ 1\end{array}\right] e^t+\frac{9}{2}\left[\begin{array}{r}-1 \\ 1\end{array}\right] e^{-t}$.
    Since one eigenvalue is positive and the other is negative, the origin is a saddle point of the dynamical system described by $\mathbf{x}^{\prime}=A \mathbf{x}$. The direction of greatest attraction is the line through $\mathbf{v}_2$ and the origin. The direction of greatest repulsion is the line through $\mathbf{v}_1$ and the origin.
    4. $c_1=13 / 4, c_2=-5 / 4$, and $\mathbf{x}(t)=\frac{13}{4}\left[\begin{array}{r}-1 \\ 1\end{array}\right] e^{3 t}-\frac{5}{4}\left[\begin{array}{r}-5 \\ 1\end{array}\right] e^{-t}$.
    Since one eigenvalue is positive and the other is negative, the origin is a saddle point of the dynamical system described by $\mathbf{x}^{\prime}=A \mathbf{x}$. The direction of greatest attraction is the line through $\mathbf{v}_2$ and the origin. The direction of greatest repulsion is the line through $\mathbf{v}_1$ and the origin.
    5. $c_1=-1 / 2, c_2=7 / 2$, and $\mathbf{x}(t)=-\frac{1}{2}\left[\begin{array}{l}1 \\ 3\end{array}\right] e^{4 t}+\frac{7}{2}\left[\begin{array}{l}1 \\ 1\end{array}\right] e^{6 t}$.
    Since both eigenvalues are positive, the origin is a repellor of the dynamical system described by $\mathbf{x}^{\prime}=A \mathbf{x}$. The direction of greatest repulsion is the line through $\mathbf{v}_2$ and the origin.
    6. $c_1=-1, c_2=5$, and $\mathbf{x}(t)=-\left[\begin{array}{l}2 \\ 3\end{array}\right] e^{-2 t}+5\left[\begin{array}{l}1 \\ 1\end{array}\right] e^{-t}$.
    Since both eigenvalues are negative, the origin is an attractor of the dynamical system described by $\mathbf{x}^{\prime}=A \mathbf{x}$. The direction of greatest attraction is the line through $\mathbf{v}_1$ and the origin.

**Exercise 6** (5.7.7-5.7.8)

Make a change of variable that decouples the equation $\mathbf{x}^{\prime}=A \mathbf{x}$. Write the equation $\mathbf{x}(t)=P \mathbf{y}(t)$ and show the calculation that leads to the uncoupled system $\mathbf{y}^{\prime}=D \mathbf{y}$, specifying $P$ and $D$.

7. $A=\left[\begin{array}{rr}7 & -1 \\ 3 & 3\end{array}\right]$
8. $A=\left[\begin{array}{ll}1 & -2 \\ 3 & -4\end{array}\right]$

??? answer "&nbsp;"
    7. 

        $\left[\begin{array}{l}y_1^{\prime}(t) \\ y_2^{\prime}(t)\end{array}\right]=\left[\begin{array}{ll}4 & 0 \\ 0 & 6\end{array}\right]\left[\begin{array}{l}y_1(t) \\ y_2(t)\end{array}\right]$

    8. 

        $\left[\begin{array}{l}y_1^{\prime}(t) \\ y_2^{\prime}(t)\end{array}\right]=\left[\begin{array}{rr}-2 & 0 \\ 0 & -1\end{array}\right]\left[\begin{array}{l}y_1(t) \\ y_2(t)\end{array}\right]$

**Exercise 7** (5.7.19)

[M] Find formulas for the voltages $v_1$ and $v_2$ (as functions of time $t$ ) for the circuit in Example 1, assuming that $R_1=1 / 5$ ohm, $R_2=1 / 3$ ohm, $C_1=4$ farads, $C_2=3$ farads, and the initial charge on each capacitor is 4 volts.

??? answer "&nbsp;"
    The general solution is $\mathbf{x}(t)=c_1\left[\begin{array}{l}1 \\ 2\end{array}\right] e^{-.5 t}+c_2\left[\begin{array}{r}-3 \\ 2\end{array}\right] e^{-2.5 t}$.

    $\left[\begin{array}{l}v_1(t) \\ v_2(t)\end{array}\right]=\mathbf{x}(t)=\frac{5}{2}\left[\begin{array}{l}1 \\ 2\end{array}\right] e^{-.5 t}-\frac{1}{2}\left[\begin{array}{r}-3 \\ 2\end{array}\right] e^{-2.5 t}$

**Exercise 8** (5.7.20)

[M] Find formulas for the voltages $v_1$ and $v_2$ for the circuit in Example 1, assuming that $R_1=1 / 15 \mathrm{ohm}, R_2=1 / 3 \mathrm{ohm}$, $C_1=9$ farads, $C_2=2$ farads, and the initial charge on each capacitor is 3 volts.

??? answer "&nbsp;"
    The general solution is thus $\mathbf{x}(t)=c_1\left[\begin{array}{l}1 \\ 3\end{array}\right] e^{-t}+c_2\left[\begin{array}{r}-2 \\ 3\end{array}\right] e^{-2.5 t}$.

    $\left[\begin{array}{l}v_1(t) \\ v_2(t)\end{array}\right]=\mathbf{x}(t)=\frac{5}{3}\left[\begin{array}{l}1 \\ 3\end{array}\right] e^{-t}-\frac{2}{3}\left[\begin{array}{r}-2 \\ 3\end{array}\right] e^{-2.5 t}$