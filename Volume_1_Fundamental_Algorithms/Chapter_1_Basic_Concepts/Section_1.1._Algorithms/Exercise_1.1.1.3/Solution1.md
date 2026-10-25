# TAOCP Vol. [1], Section [1.1], Exercise [3]

> **Difficulty Rating:** [20]
---

## Problem Statement

> Change Algorithm $E$ (for the sake of efficiency) so that all trivial replacement operations such as $``m \leftarrow n"$ are avoided. Write this new algorithm in the style of algorithm $E$, and call it Algorithm $F$.
---


$[E1]$ Divide $m$ by $n$ and let $r$ be the remainder.\
$[E2]$ If $r=0$, the algorithm terminates and $n$ is the answer.\
$[E3]$ $m \leftarrow r$.\
$[E4]$ Divide $n$ by $m$ and let $r$ be the remainder.\
$[E5]$ If $r=0$, the algorithm terminates and $m$ is the answer.\
$[E6]$ $n \leftarrow r$, and go back to step E1.
