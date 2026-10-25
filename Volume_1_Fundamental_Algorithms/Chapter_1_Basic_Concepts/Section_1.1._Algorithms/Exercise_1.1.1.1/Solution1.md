# TAOCP Vol. [1], Section [1.1], Exercise [1]

> **Difficulty Rating:** [10]  
---

## Problem Statement

> The text showed how to interchange the values of variables $m$ and $n$ using the replacement notation, by setting $t \leftarrow m,\ m \leftarrow n,\ n \leftarrow t$. Show how the values of _four_ variables $(a,b,c,d)$ can be rearranged to $(b,c,d,a)$ by a sequence of replacements. In other words, the new value of $a$ is to be the original value of $b$, etc. Try to use the minimum number of replacements.
---

The simple set of translations
$t \leftarrow a,\ a \leftarrow b, b \leftarrow c,\ c \leftarrow d,\ d \leftarrow t$ works.

The minimum number of replacements required in this instance if $5$.

In general, to rearrange $n$ variables, only $n+1$ steps are required. 