# Convexité

Une propriété fondamentale en optimisation est la *convexité*. Cette notion est plus cruciale que la différentiabilité quand il s'agit de minimiser une fonction.

:::{prf:definition}Fonction convexe
Une fonction $f:E \to \mathbb{R}$ est dite *convexe* lorsque pour tout $x,y \in E$, pour tout $\la \in [0,1]$,
\begin{equation*}
    f(\la x +  (1-\la)y) \leq \la f(x) + (1-\la) f(y).
\end{equation*}
:::
