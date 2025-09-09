# Différentielles

L'idée fondamental du calcul différentiel est d'approcher une fonction $f$, localement au voisinage d'un point, par une application linéaire (la *tangente*).

Vous connaissez déjà la notion de *dérivée* d'une fonction $f:\mathbb{R} \to \mathbb{R}$ (en un point où celle-ci est dérivable). L'objectif de cette page est d'introduire ou rappeler les concepts qui permettent de la généraliser au cas de fonctions de variables vectorielles, et à valeurs vectorielles.

## Fonctions numériques de variable vectorielle

Commençons par considérer une fonction $f:\mathbb{R}^n \to \mathbb{R}$. Pour $\mathbf{x} = (x_1,\ldots,x_n)^\top$, on notera souvent indifféremment $f(\mathbf{x})$ ou $f(x_1,\ldots,x_n)$.

:::{prf:definition}
La $i$-ème dérivée partielle de $f$, pour $i \in \{1,\ldots,n\}$, que l'on note $\delta_i f$, lorsqu'elle existe
:::
