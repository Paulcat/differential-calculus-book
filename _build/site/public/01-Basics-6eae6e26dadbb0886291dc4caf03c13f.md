# Notions d'algèbre linéaire

L'objectif du cours est de vous introduire à des problèmes d'optimisation définis sur $\mathbb{R}^n$ (l'ensemble des vecteurs réels de dimension $n$). Cet espace est l'exemple le plus standard d'un *$\mathbb{R}$-espace vectoriel* de dimension finie.

:::{note}
On peut étudier des problèmes d'optimisation sur des espaces bien plus généraux (espaces de dimension infinie, espaces métriques, etc...).  Avantage: norme, produit scalaire, etc...
:::

L'objectif de cette page est de vous donner quelques concepts clés associés à un espace vectoriel.

## Applications linéaires

Soient $E$ et $F$ deux $\mathbb{R}$-espaces vectoriels.

### Définition

:::{prf:definition}
:label:def-lineaire
Une application $f:E \to F$ est appelée *application linéaire* si pour tout $(x,y) \in E$, pour tout $\lambda,\mu \in \mathbb{R}$, on a
\begin{equation*}
    f(\lambda x + \mu y) = \lambda f(x) + \mu f(y)
\end{equation*}

Lorsque $f$ est à valeurs scalaires (i.e. $F = \mathbb{R}$), on parle de *forme linéaire*.
:::

On note en général $\mathcal{L}(E,F)$ l'ensemble des applications linéaires de $E$ dans $F$.

### Matrice d'une application

Dans la suite, on suppose que $E$ et $F$ sont tous deux de dimension finie, de base $\mathcal{E} = (e_1, \ldots, e_n)$ et $\mathcal{V} = (v_1,\ldots,v_m)$ respectivement. Dans ce cas, pour connaître une application $f$, il faut et il suffit de connaître les images $f(e_i)$ pour tout $e_i \in \mathcal{E}$.

:::{prf:definition}
:label: def-matrice
La matrice des coordonnées dans la base $\mathcal{V}$ des vecteurs $f(e_i)$, pour $e_i \in \mathcal{E}$, est appelée *matrice de l'application $f$ dans les base $\mathcal{E}$ et $\mathcal{F}$*, notée $M_{\mathcal{E},\mathcal{V}}(f)$. Autrement dit,
\begin{equation*}
    \begin{aligned}
        & \begin{matrix} & f(e_1) & & f(e_i) & & f(e_n) \end{matrix}\\
        M_{\mathcal{E},\mathcal{V}}(f) = &\begin{bmatrix}
                & & & & & a_{i,1} & & & & &\\
                & & & & & a_{i,2} & & & & &\\
                & & & & & & & & & &\\
                & & & & & a_{i,m} & & & & &\\
            \end{bmatrix}
        \begin{matrix} v_1 \\ v_2 \\ \\ v_m \end{matrix} 
    \end{aligned}.
\end{equation*}

C'est une matrice de $\mathbb{R}^{m \times n}$.
:::


Dans les cas qui nous intéressent, l'espace $E$ sera $\mathbb{R}^n$ muni de sa base canonique, c'est-à-dire les vecteur $e_i$ tels que
\begin{equation*}
    e_{ik} = \left\{ \begin{aligned} &1 \quad \text{si}\quad  k=i \\ &0 \quad \text{sinon} \end{aligned} \right..
\end{equation*}
De même $F$ sera $\mathbb{R}^m$ muni de sa base canonique. On notera alors plus simplement $M(f)$, ou $M_f$, ou $M$ la matrice d'une application linéaire de $E$ dans $F$. Notons que si $M$ est la matrice de l'application, alors pour tout $x \in E$, $f(x) = Mx$.


### Noyau et Image

Soit $f \in \mathcal{L}(E,F)$.

:::{prf:definition}
:label: def-noyau-image
- On appelle *noyau* de $f$ l'ensemble
\begin{equation*}
    \left\{ x \in E \; | \; f(x) = 0 \right\}
\end{equation*}
- On appelle *image* de $f$ l'ensemble
\begin{equation*}
    \left\{y \in F \; | \; \exists\, x \in E, \quad y = f(x) \right\}
\end{equation*}
:::

Le noyau et l'image de $f$ sont des sous-espaces vectoriels de $E$ et $F$, respectivement. On définit de la même manière le noyau et l'image d'une matrice.


# Normes

Besoin d'une notion de distance, pour mesurer la proximité de deux vecteurs: on munit notre espace d'une norme

:::{prf:definition}
:label: def-norme
Une norme
:::

:::{margin}
test1
:::

:::{sidebar}
test2
:::

:::{topic}
test3
:::


ceci est un [embedding](#def-norme)

