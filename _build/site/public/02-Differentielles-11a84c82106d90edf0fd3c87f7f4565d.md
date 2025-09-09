# Différentielles

L'idée fondamental du calcul différentiel est d'approcher une fonction $f$, localement au voisinage d'un point, par une application linéaire (la *tangente*).

Vous connaissez déjà la notion de *dérivée* d'une fonction $f:\mathbb{R} \to \mathbb{R}$ (en un point où celle-ci est dérivable). L'objectif de cette page est d'introduire ou rappeler les concepts qui permettent de la généraliser au cas de fonctions de variables vectorielles, et à valeurs vectorielles.

## Définition

Soient $E$ et $F$ deux espaces vectoriels, munis de leurs normes respectives $|\!| \cdot |\!|_E$ et $|\!| \cdot |\!|_F$. On donne ci-dessous la définition formelle de la différentiabilité locale.
:::{prf:definition}
Soit $U$ un ouvert de $E$. Une application $f:U \to F$ est dite différentiable en un point $a \in U$ s'il existe une application *linéaire* $L \in \mathcal{L}(E,F)$ telle que
\begin{equation*}
    f(a+h) = f(a) + L(h) + o(|\!| h|\!|)
\end{equation*}
:::

:::{margin}
La notation $o(|\!|h|\!|)$ (lire "petit o de norme de $h$") signifie que le reste
\begin{equation*}
    R(h) = f(a+h) - f(a) - L(h)
\end{equation*}
est infiniment petit par rapport à $h$, c'est-à-dire
\begin{equation*}
    \lim_{h \to 0} \frac{|\!|R(h)|\!|}{|\!|h|\!|} = 0
\end{equation*}
:::

Lorsqu'elle existe, l'application $L$ est unique: on écrira $L(h) = f'(a) \cdot h$, ce qui a l'avantage de mettre en évidence la linéarité.

Dans la suite, on se concentre à nouveau sur les cas (standards en optimisation) où $E = \mathbb{R}^n$ et $F = \mathbb{R}^m$, munis de leurs bases canoniques respectives.

## Fonctions numériques de variable réelle

Pour des fonctions $f : \mathbb{R} \to \mathbb{R}$, la différentiabilité

## Fonctions numériques de variable vectorielle

On considère maintenant une fonction $f:\mathbb{R}^n \to \mathbb{R}$. Pour $\mathbf{x} = (x_1,\ldots,x_n)^\top$, on notera souvent indifféremment $f(\mathbf{x})$ ou $f(x_1,\ldots,x_n)$.

:::{prf:definition}
La $i$-ème dérivée partielle de $f$, pour $i \in \{1,\ldots,n\}$, que l'on note $\delta_i f$, lorsqu'elle existe
:::
