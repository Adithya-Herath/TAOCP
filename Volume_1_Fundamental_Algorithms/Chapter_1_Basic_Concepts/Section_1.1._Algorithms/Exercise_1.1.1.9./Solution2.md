# TAOCP Vol. [1], Section [1.1], Exercise [9]

> **Difficulty Rating:** [M30]
---

## Problem Statement

> Suppose that $C_1=(Q_1,I_1,\Omega_1,f_1)$ and $C_2=(Q_2,I_2,\Omega_2,f_2)$ are computational methods. For example, $C_1$ might stand for Algorithm $E$ as in Eqs. $(2)$ except that $m$ and $n$ are restricted in magnitude, and $C_1$ might stand for a computer program implementation of Algorithm $E$. (Thus $Q_2$ might be the set of all states of the machine, i.e., all possible configurations of its memory and registers; $f_2$ might be the definition of single machine actions; and $I_2$ might be the initial state, including the program for the greatest common divisor as well as the values of $m$ and $n$.)\
> Formulate a set-theoretic definition for the concept $``C_2 \text{ is a representation of }C_1"$ or $``C_2 \text{ simulates }C_1"$. This is to mean intuitively that any computation sequence of $C_1$ is mimicked by $C_2$, except that $C_2$ might take more steps in which to do the computation and it might retain more information in its states. (We thereby obtain a rigorous interpretation of the statement, $``$ Program $X$ is an implementation of Algorithm $Y."$)
---


We shall define $C_1$ to be *simulated* by $C_2$ if there exists a surjective function $\psi$ from $Q_2 \setminus N$ to $Q_1$ where $N \subseteq Q_2$ with $N$ disjoint to $I_2$ and $\Omega_2$ such that $\psi(\Omega_2) = \Omega_1$ and $\psi(I_2) = I_1$ such that for any computational sequence $y, y_1, \dots,y_k,y_k,\dots$ in $C_2$, there exists a unique increasing function $\alpha: \mathbb{N} \to \mathbb{N}$ s.t. $x=\psi(y)$ and $\psi(y_{\alpha(i)})=x_i$ for some computational sequence $x, x_1,\dots,x_j,x_j,\dots$ in $C_1$.

---

## Personal Notes/Remarks

Once again, I am not satisfied by my answer. 
The only good thing here, if there is anything to begin with in the first place is, by changing the perspective of trying to embed $C_1$ into $C_2$ instead to the perspective of trying to map each computational sequence in $C_2$ a computation. This is good because I completely neglected the fact that the same algorithm in $C_1$ could have multiple algorithms corresponding in $C_2$ due to redundant information\
Why do I think this is a good thing? It hasn't exactly destroyed the earlier approach I had, because I can consider a single fiber from $\psi^{-1}$ and still track my argument from $\phi$ from earlier. Another happy thought I had is the factthat this leaves me is the fact that I can do a sort of... quotient space like trick where I can group up multiple algorithms based on whether they are mapped to the same element or not... and that pretty much encapsulates the $C_2$ is a representation of $C_1$ via the explicit grouping too.\
However, this does lead to ridiculous notions like, if we have some trivial algorithm, every algorithm simulates the trivial algorithm! How do I prevent absurd notions like this? I have absolutely no idea. The purpose I had with $N$ was to have a sort of "null set" where not every state of $C_2$ should be mapped to a state in $C_1$. This allows me to emulate my earlier $\phi$ argument.\
This also still doesn't allow me to solve the problem of "is this the same implementation or a way less efficient implementation" either.
But at this point... I'll keep this at that. And try to improve on this later when I have a better understanding.