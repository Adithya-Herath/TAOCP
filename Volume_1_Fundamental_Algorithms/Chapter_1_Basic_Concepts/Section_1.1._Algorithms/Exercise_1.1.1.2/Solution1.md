# TAOCP Vol. [1], Section [1.1], Exercise [2]

> **Difficulty Rating:** [10]  
---

## Problem Statement

> Prove that $m$ is always greater than $n$ at the beginning of step $E1$, except possibly the first time this step occurs
---


Before step 3, since r is the remainder of after being divided by n, we have $0\le r < n$. After the replacement in step 3 (or, in other words, before step 1) $m \leftarrow n$, $n \leftarrow r$ the inequality becomes $0 \le n <m$. Therefore, excluding the first time $E1$ occurs, $n<m$ at the beginning.