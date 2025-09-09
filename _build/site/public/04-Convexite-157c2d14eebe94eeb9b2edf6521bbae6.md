# Convexité

Une propriété fondamentale en optimisation est la *convexité*. Cette notion est plus cruciale que la différentiabilité quand il s'agit de minimiser une fonction.

:::{prf:definition}Fonction convexe
Une fonction $f:E \to \mathbb{R}$ est dite *convexe* si pour tout $x,y \in E$, pour tout $\lambda \in [0,1]$,
:::{math}
:label: eq:convexity
    f(\lambda x +  (1-\lambda)y) \leq \lambda f(x) + (1-\lambda) f(y).
:::
Lorsque l'inégalité est stricte, $f$ est dite *strictement convexe*.
:::

Géométriquement, l'[équation précédente](#eq:convexity)
