<h1 align="center">Differential Equations</h1>

## Session Material:

Lay: 5.7

[Recap and Exercises](https://drive.google.com/file/d/1IdILvufN2_j4yMma1oCD1NfzmSo6C2tm/view?usp=sharing)

[Session Notes](https://drive.google.com/file/d/1SiSA99_BH1VNszqPkM41wJ1CxjX2oaj_/view?usp=sharing)

[Session Material](https://viaucdk-my.sharepoint.com/:f:/g/personal/rib_viauc_dk/Elax7Cbk0DNLhpjCdiMwfOwBmG7jxqF7AJW5boJBajmB7Q?e=NzLWfW)

---

## Session Description

We've learned about eigenvalues and eigenvectors and how to diagonalize matrices. In this session, we'll see a powerful application of these ideas to the real world: solving systems of linear differential equations! We'll discover how the eigenvalues and eigenvectors of a matrix connected to the system give us the fundamental building blocks for the solutions.

We'll focus on understanding how these concepts help us find the general solution to systems of equations that describe things changing over time, like population models or coupled systems. The eigenvalues will relate to the exponential growth or decay rates, and the eigenvectors will define the directions of these changes. While this is just an introduction, it highlights how abstract linear algebra tools are essential for tackling dynamic problems in science and engineering.

### Key Concepts

* Systems of Differential Equations
* Applications of Eigenvalues
* Applications of Eigenvectors
* Linear Differential Equations
* Solution Structure
* Exponential Solutions

!!! tip "Learning Objectives"

    - Model and solve systems of linear differential equations using matrix methods.
    - Apply eigenvalues and eigenvectors to construct general solutions.
    - Interpret the role of exponential solutions in dynamic systems.
    - Analyze the structure of solutions for linear differential equations.
    - Connect linear algebra concepts to real-world applications in science and engineering.

---

## Exercises

<!--
5.7: 1-8, 15, 16, 19, 20 
-->
<style type="text/css">
    ol { list-style-type: lower-alpha; }
</style>

**Exercise 1** (5.7.1)

A particle moving in a planar force field has a position vector $\mathbf{x}$ that satisfies $\mathbf{x}^{\prime}=A \mathbf{x}$. The $2 \times 2$ matrix $A$ has eigenvalues 4 and 2 , with corresponding eigenvectors $\mathbf{v}_1=\left[\begin{array}{r}-3 \\ 1\end{array}\right]$ and $\mathbf{v}_2=\left[\begin{array}{r}-1 \\ 1\end{array}\right]$. Find the position of the particle at time $t$, assuming that $\mathbf{x}(0)=\left[\begin{array}{r}-6 \\ 1\end{array}\right]$.

??? answer "&nbsp;"
    $c_1=5 / 2, c_2=-3 / 2$, and $\mathbf{x}(t)=\frac{5}{2}\left[\begin{array}{r}-3 \\ 1\end{array}\right] e^{4 t}-\frac{3}{2}\left[\begin{array}{r}-1 \\ 1\end{array}\right] e^{2 t}$

**Exercise 2** (5.7.2)

Let $A$ be a $2 \times 2$ matrix with eigenvalues -3 and -1 and corresponding eigenvectors $\mathbf{v}_1=\left[\begin{array}{r}-1 \\ 1\end{array}\right]$ and $\mathbf{v}_2=\left[\begin{array}{l}1 \\ 1\end{array}\right]$. Let $\mathbf{x}(t)$ be the position of a particle at time $t$. Solve the initial value problem $\mathbf{x}^{\prime}=A \mathbf{x}, \mathbf{x}(0)=\left[\begin{array}{l}2 \\ 3\end{array}\right]$.

??? answer "&nbsp;"
    $c_1=1 / 2, c_2=5 / 2$, and $\mathbf{x}(t)=\frac{1}{2}\left[\begin{array}{r}-1 \\ 1\end{array}\right] e^{-3 t}+\frac{5}{2}\left[\begin{array}{l}1 \\ 1\end{array}\right] e^{-t}$

**Exercise 3** (5.7.3-5.7.6)

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

**Exercise 4** (5.7.7-5.7.8)

Make a change of variable that decouples the equation $\mathbf{x}^{\prime}=A \mathbf{x}$. Write the equation $\mathbf{x}(t)=P \mathbf{y}(t)$ and show the calculation that leads to the uncoupled system $\mathbf{y}^{\prime}=D \mathbf{y}$, specifying $P$ and $D$.

7. $A=\left[\begin{array}{rr}7 & -1 \\ 3 & 3\end{array}\right]$
8. $A=\left[\begin{array}{ll}1 & -2 \\ 3 & -4\end{array}\right]$

??? answer "&nbsp;"
    7. 

        $\left[\begin{array}{l}y_1^{\prime}(t) \\ y_2^{\prime}(t)\end{array}\right]=\left[\begin{array}{ll}4 & 0 \\ 0 & 6\end{array}\right]\left[\begin{array}{l}y_1(t) \\ y_2(t)\end{array}\right]$

    8. 

        $\left[\begin{array}{l}y_1^{\prime}(t) \\ y_2^{\prime}(t)\end{array}\right]=\left[\begin{array}{rr}-2 & 0 \\ 0 & -1\end{array}\right]\left[\begin{array}{l}y_1(t) \\ y_2(t)\end{array}\right]$

**Exercise 5** (5.7.15-5.7.16)

Construct the general solution of $\mathbf{x}^{\prime}=A \mathbf{x}$ involving complex eigenfunctions and then obtain the general real solution. Describe the shapes of typical trajectories.

15. $[\mathbf{M}] A=\left[\begin{array}{rrr}-8 & -12 & -6 \\ 2 & 1 & 2 \\ 7 & 12 & 5\end{array}\right]$
16. $[\mathbf{M}] A=\left[\begin{array}{rrr}-6 & -11 & 16 \\ 2 & 5 & -4 \\ -4 & -5 & 10\end{array}\right]$

??? answer "&nbsp;"
    15. The general solution is $\mathbf{x}(t)=c_1\left[\begin{array}{r}-4 \\ 1 \\ 4\end{array}\right] e^t+c_2\left[\begin{array}{r}-6 \\ 1 \\ 5\end{array}\right] e^{-t}+c_3\left[\begin{array}{r}-1 \\ 0 \\ 1\end{array}\right] e^{-2 t}$. The origin is a saddle point.
    A solution with $c_1=0$ is attracted to the origin while a solution with $c_2=c_3=0$ is repelled.
    16. The general solution is $\mathbf{x}(t)=c_1\left[\begin{array}{r}7 \\ -2 \\ 3\end{array}\right] e^{4 t}+c_2\left[\begin{array}{r}3 \\ -1 \\ 1\end{array}\right] e^{3 t}+c_3\left[\begin{array}{l}2 \\ 0 \\ 1\end{array}\right] e^{2 t}$. The origin is a repellor, because all eigenvalues are positive. All trajectories tend away from the origin.

**Exercise 6** (5.7.19)

[M] Find formulas for the voltages $v_1$ and $v_2$ (as functions of time $t$ ) for the circuit in Example 1, assuming that $R_1=1 / 5$ ohm, $R_2=1 / 3$ ohm, $C_1=4$ farads, $C_2=3$ farads, and the initial charge on each capacitor is 4 volts.

??? answer "&nbsp;"
    The general solution is $\mathbf{x}(t)=c_1\left[\begin{array}{l}1 \\ 2\end{array}\right] e^{-.5 t}+c_2\left[\begin{array}{r}-3 \\ 2\end{array}\right] e^{-2.5 t}$.

    $\left[\begin{array}{l}v_1(t) \\ v_2(t)\end{array}\right]=\mathbf{x}(t)=\frac{5}{2}\left[\begin{array}{l}1 \\ 2\end{array}\right] e^{-.5 t}-\frac{1}{2}\left[\begin{array}{r}-3 \\ 2\end{array}\right] e^{-2.5 t}$

**Exercise 7** (5.7.20)

[M] Find formulas for the voltages $v_1$ and $v_2$ for the circuit in Example 1, assuming that $R_1=1 / 15 \mathrm{ohm}, R_2=1 / 3 \mathrm{ohm}$, $C_1=9$ farads, $C_2=2$ farads, and the initial charge on each capacitor is 3 volts.

??? answer "&nbsp;"
    The general solution is thus $\mathbf{x}(t)=c_1\left[\begin{array}{l}1 \\ 3\end{array}\right] e^{-t}+c_2\left[\begin{array}{r}-2 \\ 3\end{array}\right] e^{-2.5 t}$.

    $\left[\begin{array}{l}v_1(t) \\ v_2(t)\end{array}\right]=\mathbf{x}(t)=\frac{5}{3}\left[\begin{array}{l}1 \\ 3\end{array}\right] e^{-t}-\frac{2}{3}\left[\begin{array}{r}-2 \\ 3\end{array}\right] e^{-2.5 t}$