# TAOCP Vol. [1], Section [1.1], Exercise [9]

> **Difficulty Rating:** [M30]
---

## Problem Statement

> Suppose that $C_1=(Q_1,I_1,\Omega_1,f_1)$ and $C_2=(Q_2,I_2,\Omega_2,f_2)$ are computational methods. For example, $C_1$ might stand for Algorithm $E$ as in Eqs. $(2)$ except that $m$ and $n$ are restricted in magnitude, and $C_1$ might stand for a computer program implementation of Algorithm $E$. (Thus $Q_2$ might be the set of all states of the machine, i.e., all possible configurations of its memory and registers; $f_2$ might be the definition of single machine actions; and $I_2$ might be the initial state, including the program for the greatest common divisor as well as the values of $m$ and $n$.)\
> Formulate a set-theoretic definition for the concept $``C_2 \text{ is a representation of }C_1"$ or $``C_2 \text{ simulates }C_1"$. This is to mean intuitively that any computation sequence of $C_1$ is mimicked by $C_2$, except that $C_2$ might take more steps in which to do the computation and it might retain more information in its states. (We thereby obtain a rigorous interpretation of the statement, $``$ Program $X$ is an implementation of Algorithm $Y."$)
---


We shall define $C_1$ to be *simulated* by $C_2$ if there exists a one-to-one function $\phi$ from $Q_1$ to $Q_2$ such that $\phi(\Omega_1) \subseteq \Omega_2$ and $\phi(I_1) \subseteq I_2$ such that for any computational sequence $x, x_1, \dots,x_k,x_k,\dots$ where $x \in I_1$ and $x_k \in \Omega_1$, for $y=\phi(x)$ its corresponding computational sequence $y, y_1, \dots, y_l,y_l,\dots$ with $y_l \in \Omega_2$ is such that $\phi(x_i)=y_{\alpha(i)}$ where $\alpha: \mathbb{N} \to \mathbb{N}$ is an increasing function.

---

## Personal Notes/Remarks

I am not exactly sure about this definition.
Clearly, if an algorithm is being simulated by another, then its states initial, or terminal should be larger in size. The one-to-one correspondance makes sense, or else even something which maps all the intial states to one initial state, and all the terminal states to one terminal state for example would break things.
What I'm not exactly delighted about this definition is the fact that if any algorithm $C_2$, regardless of the way the implementation has happened, just takes more steps than the $C_1$, maybe due to inefficiency rather than taking more steps to do mimic the computation, too would be categorized in the same way. But I suppose in such low level abstraction you may lose some things?