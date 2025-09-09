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
Si l'application $f'$ est différentiable en $a$, on dit que $f$ est *deux fois différentiable en $a$* et on note $D^2f(a)$ la *différentielle seconde*. Les composantes $\partial_i f(x)$ admettent alors des [dérivées partielles](#lem:partial) en $a$, notées
\begin{equation*}
    \partial_{ij} f(a) = \partial_i (\partial_j f) (a), \quad 1 \leq i,j \leq n.
\end{equation*}
:::

### Matrice hessienne
L'application linéaire $D^2f(a)$ de $\mathbb{R}^n$ dans $\mathbb{R}^n$ est représentée la matrice $n \times n$
:::{prf:definition}Matrice hessienne
\begin{equation*}
f''(a) = \begin{bmatrix} 
    \partial_{11} f(a) & \ldots & \partial_{n1} f(a) \\
    \vdots & & \vdots
    \partial_{1n} f(a) & \ldots & \partial{nn} f(a)
    \end{bmatrix} \in \mathbb{R}^n
\end{equation*}
:::
