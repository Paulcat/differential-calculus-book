# Différentielles

L'idée fondamental du calcul différentiel est d'approcher une fonction $f$, localement au voisinage d'un point, par une application linéaire (la *tangente*).

Vous connaissez déjà la notion de *dérivée* d'une fonction $f:\mathbb{R} \to \mathbb{R}$ (en un point où celle-ci est dérivable). L'objectif de cette page est d'introduire ou rappeler les concepts qui permettent de la généraliser au cas de fonctions de variables vectorielles, et à valeurs vectorielles.

## Définition

Soient $E$ et $F$ deux espaces vectoriels, munis de leurs normes respectives $|\!| \cdot |\!|_E$ et $|\!| \cdot |\!|_F$. On donne ci-dessous la définition formelle de la différentiabilité locale.
:::{prf:definition}
:label: def-diff
Soit $U$ un ouvert de $E$. Une application $f:U \to F$ est dite différentiable en un point $a \in U$ s'il existe une application *linéaire* $L \in \mathcal{L}(E,F)$ telle que
\begin{equation*}
    f(a+h) = f(a) + L(h) + o(|\!| h|\!|).
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

Dans la suite, on se concentre à nouveau sur les cas où $E = \mathbb{R}^n$ et $F = \mathbb{R}^m$, munis de leurs bases canoniques respectives.

## Fonctions numériques de variable réelle

Pour une fonctions $f : \mathbb{R} \to \mathbb{R}$, la notion de [différentiabilité](#def-diff) ci-dessus équivaut à celle de dérivabilité: en effet, l'existence de la limite
\begin{equation*}
    \lim_{h \to \infty} \frac{f(a+h) - f(a)}{h} = f'(a) \in \mathbb{R}
\end{equation*}
montre bien que $f(a+h) = f(a) + f'(a)h + o(h)$. Dans ce cas, $f'(a)$ est un *réel*: c'est le coefficient directeur de la droite tangente à $f$ en $a$.

## Fonctions numériques de variable vectorielle

On considère maintenant une fonction $f:\mathbb{R}^n \to \mathbb{R}$. Pour $x = (x_1,\ldots,x_n)^\top$ dans la base canonique, on notera indifféremment $f(x)$ ou $f(x_1,\ldots,x_n)$. La différentiabilité de $f$ entraîne l'existence des dérivées le long de chaque vecteur de base $e_i$, appelée *dérivées partielles*.

:::{prf:definition}
Soit $f:\mathbb{R}^n\to\mathbb{R}$ [différentiable](#def-diff) en $a$. Alors, pour tout $i=1,\ldots,n$,
\begin{equation*}
    \lim_{t\to 0} \frac{f(a_1,\ldots,a_i+t,\ldots,a_n)-f(a)}{t} = f'(a) \cdot e_i
\end{equation*}
On note cette limite $\partial_i f(a)$, appelée *dérivée partielle* de $f$ en $a$.
:::

Pour $\mathbf{x} = (x_1,\ldots,x_n)^\top$ dans la base canonique, on notera souvent indifféremment $f(\mathbf{x})$ ou $f(x_1,\ldots,x_n)$.

:::{prf:definition}
La $i$-ème dérivée partielle de $f$, pour $i \in \{1,\ldots,n\}$, que l'on note $\delta_i f$, lorsqu'elle existe
:::
