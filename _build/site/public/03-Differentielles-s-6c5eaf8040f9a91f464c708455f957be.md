# Différentielles secondes

L'étude locale d'une fonction peut s'affiner au-delà de l'approximation tangentielle (linéaire), en explicitant les termes d'ordre supérieur dans les termes correctifs "petit o". Géométriquement, les termes d'ordre 2 contrôlent la position de la variété (courbe, surface, etc...) par rapport à sa tangente (convexité, concavité, points d'inflexion, etc...).

On se contentera d'étudier l'ordre 2 uniquement pour des fonctions à valeurs numériques.

## Différentielle seconde

### Définition
Si $f:\mathbb{R}^n \to \mathbb{R}$ est [différentiable](#def:diff) sur un voisinage $U$ de $a$, sa différentielle $L$ définit une application $f'$ de $U$ dans $\mathbb{R}^n$:

\begin{equation*}
    x = (x_1,\ldots,x_n) \mapsto f'(x) = \begin{bmatrix} \partial_1 f(x) \\ \vdots \\ \partial_n f(x) \end{bmatrix}.
\end{equation*}

:::{prf:definition}Différentielle seconde
Si l'application $f'$ est différentiable en $a$, on dit que $f$ est *deux fois différentiable en $a$* et on note $D^2_af$ la *différentielle seconde*. Les composantes $\partial_i f(x)$ admettent alors des [dérivées partielles](#lem:partial) en $a$, notées
\begin{equation*}
    \partial_{ij}^2 f(a) = \partial_i (\partial_j f) (a), \quad 1 \leq i,j \leq n.
\end{equation*}
:::

### Matrice hessienne
De même que la *différentielle* définit une application *linéaire* 
\begin{equation*}
    h \mapsto f'(a) \cdot h = \sum_{i=1}^n \partial_i f(a) h_i,
\end{equation*}
représentée par le [gradient](#def:gradient) de $f$, la différentielle seconde définit une application *bilinéaire*
\begin{equation*}
    (h,k) \mapsto f''(a) \cdot (h,k) = \sum_{i,j=1}^n \partial_{ij}^2 f(a) h_i k_j
\end{equation*}
représentée par la matrice *hessienne* de $f$.

:::{prf:definition}Matrice hessienne
:label: def:hessienne
La *matrice hessienne* de $f$ en $a \in \mathbb{R}^n$, usuellement notée $H_f(a)$ ou $f''(a)$, est la matrice $n\times n$ définie par
\begin{equation*}
H_f(a) = 
\begin{bmatrix} 
    \partial_{11}^2 f(a) & \ldots & \partial_{n1}^2 f(a) \\
    \vdots & & \vdots\\
    \partial_{1n}^2 f(a) & \ldots & \partial_{nn}^2 f(a)
    \end{bmatrix} \in \mathbb{R}^{n \times n}.
\end{equation*}
:::

Lorsqu'elle est définie, la matrice hessienne est *symétrique*: en effet, le théorème de Schwarz assure que pour une fonction $f$ deux fois différentiable en $a \in \mathbb{R}^n$, on a
\begin{equation*}
    \partial_{ij}^2 f(a) = \partial_{ji}^2 f(a).
\end{equation*}

:::{prf:example}
La matrice hessienne dans l'[exemple précédent](#ex:partial) est, pour tout $(x_1,x_2) \in \mathbb{R}^2$,
\begin{equation*}
    H_f(x_1,x_2) = \begin{bmatrix} 4 & 1 \\ 1 & -6 \end{bmatrix}
\end{equation*}
:::
