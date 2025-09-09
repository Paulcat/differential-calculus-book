# Différentielles


# Différentielles premières

L'idée fondamental du calcul différentiel est d'approcher une fonction $f$, localement au voisinage d'un point, par une application linéaire (la *tangente*).

Vous connaissez déjà la notion de *dérivée* d'une fonction $f:\mathbb{R} \to \mathbb{R}$ (en un point où celle-ci est dérivable). L'objectif de cette page est d'introduire ou rappeler les concepts qui permettent de la généraliser au cas de fonctions de variables vectorielles, et à valeurs vectorielles.

## Définition

Soient $E$ et $F$ deux espaces vectoriels, munis de leurs normes respectives $|\!| \cdot |\!|_E$ et $|\!| \cdot |\!|_F$. On donne ci-dessous la définition formelle de la différentiabilité locale.
:::{prf:definition}
:label: def:diff
Soit $U$ un ouvert de $E$. Une application $f:U \to F$ est dite différentiable en un point $a \in U$ s'il existe une application *linéaire* $D_af \in \mathcal{L}(E,F)$ telle que
\begin{equation*}
    f(a+h) = f(a) + D_af(h) + o(|\!| h|\!|).
\end{equation*}
:::

:::{margin}
La notation $o(|\!|h|\!|)$ (lire "petit o de norme de $h$") signifie que le reste
\begin{equation*}
    R(h) = f(a+h) - f(a) - D_af(h)
\end{equation*}
est infiniment petit par rapport à $h$, c'est-à-dire
\begin{equation*}
    \lim_{h \to 0} \frac{|\!|R(h)|\!|}{|\!|h|\!|} = 0
\end{equation*}
:::

L'intérêt de considérer un ouvert $U$ est que cela permet de définir une boule ouverte autour de $a$ tel que, pour $h$ suffisamment petit, $a+h \in U$. Lorsqu'elle existe, l'application $D_af$ est unique: on écrira $D_af(h) = f'(a) \cdot h$, pour mettre en évidence la linéarité.

Dans la suite, on se concentre à nouveau sur les cas où $E = \mathbb{R}^n$ et $F = \mathbb{R}^m$, munis de leurs bases canoniques respectives.

## Fonctions de $\mathbb{R}$ dans $\mathbb{R}$

Pour une fonctions $f : \mathbb{R} \to \mathbb{R}$, la notion de [différentiabilité](#def:diff) ci-dessus équivaut à celle de dérivabilité: en effet, l'existence de la limite
\begin{equation*}
    \lim_{h \to 0} \frac{f(a+h) - f(a)}{h} = f'(a) \in \mathbb{R}
\end{equation*}
montre bien que $f(a+h) = f(a) + f'(a)h + o(h)$. Dans ce cas, $f'(a)$ est un *réel*: c'est le coefficient directeur de la droite tangente à $f$ en $a$: localement, i.e. en zoomant suffisamment sur le point $a$, la fonction $f$ se comporte comme la droite affine $h \mapsto f(a) + f'(a)h$.

## Fonctions de $\mathbb{R}^n$ dans $\mathbb{R}$.

### Dérivées partielles
On considère maintenant une fonction numérique de variable vectorielle. La différentiabilité de $f$ entraîne l'existence des dérivées le long de chaque vecteur de la base canonique $e_i$.
:::{margin}
Pour $x = (x_1,\ldots,x_n)^\top$ dans la base canonique, on notera indifféremment $f(x)$ ou $f(x_1,\ldots,x_n)$. 
:::

:::{prf:lemma}Dérivée partielle
:label: lem:partial
Soit $f:\mathbb{R}^n\to\mathbb{R}$ [différentiable](#def:diff) en $a$. Alors, pour tout $i=1,\ldots,n$, on a 
\begin{equation*}
    \lim_{t\to 0} \frac{f(a_1,\ldots,a_i+t,\ldots,a_n)-f(a)}{t} = f'(a) \cdot e_i .
\end{equation*}
On notera cette limite $\partial_i f(a)$, appelée *dérivée partielle* de $f$ en $a$.
:::

Dans la pratique, calculer la $i$-ème dérivée partielle de $f(x_1,\ldots,x_n)$ est simple: on fixe toutes les variables $x_j$ pour $j\neq i$, et on calcule la dérivée par rapport à la variable $x_i$.

:::{prf:example}
:label: ex:partial
On considère la fonction $f(x_1,x_2) = 2x_1^2 + x_1x_2 - 3x_2^2 - x_1 + 1$. Ses dérivées partielles sont
\begin{equation*}
\left\{
\begin{aligned}

    &\partial_1 f(x_1,x_2) = 4x_1 + x_2 - 1\\
    &\partial_2 f(x_1,x_2) = x_1 - 6x_2

\end{aligned}
\right..
\end{equation*}
:::

:::{warning}
La différentiabilité d'une fonction entraîne l'existence des dérivées partielles, mais l'inverse n'est pas vrai: une fonction peut avoir des dérivées partielles en $a$ sans même être continue en $a$.
:::


### Gradient

Le gradient de $f$ est le vecteur de ses dérivées partielles.
:::{prf:definition}Gradient
:label: def:gradient
Soit $f:\mathbb{R}^n \to \mathbb{R}$ une fonction différentiable. Le *gradient* de $f$ en un point $a$, usuellement noté $\nabla f(a)$ ou $f'(a)$, est le vecteur défini par
\begin{equation*}
    \nabla f(a) = \begin{bmatrix} \partial_1f(a) \\ \partial_2 f(a) \\ \vdots \\ \partial_n f(a) \end{bmatrix} \in \mathbb{R}^n.
\end{equation*}
:::
Sur $\mathbb{R}^n$, on peut définir le produit scalaire usuel
\begin{equation*}
    x \cdot y = \sum_{i=1}^n x_i y_i \quad \forall x,y \in \mathbb{R}^n
\end{equation*}
Lorsque $f$ est [différentiable](#def:diff) de différentielle $D_af$, le gradient de $f$ est l'unique vecteur tel que, pour tout $h \in \mathbb{R}^n$
\begin{equation*}
    D_af(h) = \nabla f(a) \cdot h
\end{equation*}

:::{prf:example}
Le gradient de la fonction $f$ de l'[exemple précédent](#ex:partial) est donné par
\begin{equation*}
    \nabla f(x_1,x_2) = \begin{bmatrix} 4x_1 + x_2 -1 \\ x_1 - 6x_2 \end{bmatrix}.
\end{equation*}
:::


## Fonctions de $\mathbb{R}^n$ dans $\mathbb{R}^m$

Lorsque $f$ est une application à valeurs vectorielles de variable vectorielle, on notera
\begin{equation*}
    f(x) = \begin{bmatrix} f_1(x) \\ \vdots \\ f_m(x) \end{bmatrix} \in \mathbb{R}^m
\end{equation*}
où pour tout $j=1,\ldots,m$, $f_j$ est une application de $\mathbb{R}^n$ dans $\mathbb{R}$.

:::{prf:definition}Matrice jacobienne
Soit $f:\mathbb{R}^n \to \mathbb{R}^m$ une application différentiable. La matrice jacobienne de $f$ en un point $a \in \mathbb{R}^n$, usuellement notée $J_f(a)$ ou $f'(a)$, est la matrice
\begin{equation*}
    J_f(a) = 
    \begin{bmatrix} 
        \partial_1 f_1(a) & \partial_2 f_1(a) & \ldots & \partial_n f_1(a) \\
        \partial_1 f_2(a) & \partial_2 f_2(a) & \ldots & \partial_n f_2(a) \\
        \vdots & \vdots & & \vdots \\
        \partial_1 f_m(a) & \partial_2 f_m(a) & \ldots & \partial_n f_m(a)
    \end{bmatrix} \in \mathbb{R}^{m \times n}.
\end{equation*}
:::

De manière analogue au gradient, la matrice jacobienne de $f$ est l'unique matrice telle que, pour tout $h \in \mathbb{R}^n$,
:::{margin}
On surcharge la notation $f'(a) \cdot h$, qui prend un sens différent selon que
- $f'(a)$ est un réel et $h$ un réel
- $f'(a)$ est un vecteur et $h$ un vecteur
- $f'(a)$ est une matrice et $h$ un vecteur.

Le point commun dans les trois cas est la linéarité de $D_af:h\mapsto f'(a) \cdot h$.
:::
\begin{equation*}
    D_af(h) = J_f(a) \cdot h,
\end{equation*}
où cette fois l'opération $\cdot$ est à comprendre comme un produit matriciel.

:::{important}
On retiendra que le principe fondamental du calcul différentiel consiste à voir que
\begin{equation*}
    \left( \begin{array}{c} \text{accroissement} \\ \text{de la fonction} \end{array} \right)
    =
    \left( \begin{array}{c} \text{terme linéaire en} \\ \text{l'accroissement de la variable} \end{array} \right)
    +
    \left( \begin{array}{c} \text{petit terme} \\ \text{correctif} \end{array} \right)
\end{equation*}
\begin{equation*}
    \qquad f(x)-f(x_0) \quad = \qquad \qquad f'(x_0) \cdot (x-x_0) \qquad \qquad \; + \;\, \quad o(|\!|x-x_0|\!|) \qquad \quad  
\end{equation*}
Géométriquement, cela exprime qu'une courbe est, au voisinage d'un point, confondue avec une droite (la tangente), une surface avec un espace tangent, etc...:
\begin{equation*}
    f(x) \simeq f(x_0) + f'(x_0)\cdot (x-x_0)
\end{equation*}
:::

## Chain rule

Une propriété importante des différentielles est la **formule de différentiation des fonctions composées**.

:::{prf:proposition}
Si $f : E \to F$ et $g : F \to G$ sont des application différentiables en $a$ (sur des espaces vectoriels $E, F$ et $G$), alors l'application $g \circ f$ est différentiable en $a$ et on a
\begin{equation*}
    (g \circ f)'(a) = g'(f(a)) \cdot f'(a)
\end{equation*}
:::

Cette formule est cruciale pour comprendre les algorithmes de propagation de gradient dans les réseaux de neurones.


# Différentielle seconde
