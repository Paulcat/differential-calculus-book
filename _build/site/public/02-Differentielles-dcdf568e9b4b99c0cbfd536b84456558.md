# Différentielles

L'idée fondamental du calcul différentiel est d'approcher une fonction $f$, localement au voisinage d'un point, par une application linéaire (la *tangente*).

Vous connaissez déjà la notion de *dérivée* d'une fonction $f:\mathbb{R} \to \mathbb{R}$ (en un point où celle-ci est dérivable). L'objectif de cette page est d'introduire ou rappeler les concepts qui permettent de la généraliser au cas de fonctions de variables vectorielles, et à valeurs vectorielles.

## Définition

Soient $E$ et $F$ deux espaces vectoriels, munis de leurs normes respectives $|\!| \cdot |\!|_E$ et $|\!| \cdot |\!|_F$. On donne ci-dessous la définition formelle de la différentiabilité locale.
:::{prf:definition}
:label: def:diff
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

Lorsqu'elle existe, l'application $L$ est unique: on écrira $L(h) = f'(a) \cdot h$, pour mettre en évidence la linéarité.

Dans la suite, on se concentre à nouveau sur les cas où $E = \mathbb{R}^n$ et $F = \mathbb{R}^m$, munis de leurs bases canoniques respectives.

## Fonctions numériques de variable réelle

Pour une fonctions $f : \mathbb{R} \to \mathbb{R}$, la notion de [différentiabilité](#def:diff) ci-dessus équivaut à celle de dérivabilité: en effet, l'existence de la limite
\begin{equation*}
    \lim_{h \to 0} \frac{f(a+h) - f(a)}{h} = f'(a) \in \mathbb{R}
\end{equation*}
montre bien que $f(a+h) = f(a) + f'(a)h + o(h)$. Dans ce cas, $f'(a)$ est un *réel*: c'est le coefficient directeur de la droite tangente à $f$ en $a$: localement, i.e. en zoomant suffisamment sur le point $a$, la fonction $f$ se comporte comme la droite affine $h \mapsto f(a) + f'(a)h$.

## Fonctions numériques de variable vectorielle

### Dérivées partielles
On considère maintenant une fonction $f:\mathbb{R}^n \to \mathbb{R}$. La différentiabilité de $f$ entraîne l'existence des dérivées le long de chaque vecteur de la base canonique $e_i$.
:::{margin}
Pour $x = (x_1,\ldots,x_n)^\top$ dans la base canonique, on notera indifféremment $f(x)$ ou $f(x_1,\ldots,x_n)$. 
:::

:::{prf:lemma}Dérivée partielle
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
Soit $f:\mathbb{R}^n \to \mathbb{R}$ une fonction différentiable. Le *gradient* de $f$ en un point $a$, usuellement noté $\nabla f(a)$ ou $f'(a)$, est le vecteur défini par
\begin{equation*}
    \nabla f(a) = \begin{bmatrix} \partial_1f(a) \\ \partial_2 f(a) \\ \vdots \\ \partial_n f(a) \end{bmatrix} \in \mathbb{R}^n.
\end{equation*}
:::
Sur $\mathbb{R}^n$, on peut définir le produit scalaire usuel
\begin{equation*}
    x \cdot y = \sum_{i=1}^n x_i y_i \quad \forall x,y \in \mathbb{R}^n
\end{equation*}
Lorsque $f$ est [différentiable](#def:diff) de différentielle $L$, le gradient de $f$ est l'unique vecteur tel que, pour tout $h \in \mathbb{R}^n$
\begin{equation*}
    L(h) = \nabla f(a) \cdot h
\end{equation*}

:::{prf:example}
Le gradient de la fonction $f$ de l'[exemple précédent](#ex:partial) est donné par
\begin{equation*}
    \nabla f(x_1,x_2) = \begin{bmatrix} 4x_1 + x_2 -1 \\ x_1 - 6x_2 \end{bmatrix}.
\end{equation*}
:::


## Fonctions vectorielles de variable vectorielles

Lorsque $f$ est une application de $\mathbb{R}^n$ dans $\mathbb{R}^m$, on notera
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
En surchargeant l'opération $\cdot$, i.e. en écrivant de manière générique $f'(a) \cdot h$, que
- $f'(a)$ soit un réel et $h$ un réel ($n=m=1$)
- $f'(a)$ soit un vecteur et $h$ un vecteur ($m=1$)
- $f'(a)$ soit une matrice et $h$ un vecteur,

on insiste surtout sur la linéarité de l'application $L:h\mapsto f'(a) \cdot h$.
:::
\begin{equation*}
    L(h) = J_f(a) \cdot h,
\end{equation*}
où cette fois l'opération $\cdot$ est à comprendre comme le produit matrice $\cdot$ vecteur.
