# Différentielles secondes

L'étude locale d'une fonction peut s'affiner au-delà de l'approximation tangentielle (linéaire), en explicitant les termes d'ordre supérieur dans les termes correctifs "petit o". Géométriquement, les termes d'ordre 2 contrôlent la position de la variété (courbe, surface, etc...) par rapport à sa tangente (convexité, concavité, points d'inflexion, etc...).

On se contentera d'étudier l'ordre 2 uniquement pour des fonctions à valeurs numériques.

## Différentielle seconde

Si $f:\mathbb{R}^n \to \mathbb{R}$ est [différentiable](#def:diff) sur un voisinage $U$ de $a$, sa différentielle $L$ définit une application $f'$ de $U$ dans $\mathbb{R}^n$:

\begin{equation*}
    x = (x_1,\ldots,x_n) \mapsto f'(x) = \begin{bmatrix} \partial_1 f(x) \\ \vdots \\ \partial_n f(x) \end{bmatrix}.
\end{equation*}

:::{prf:definition}Différentielle seconde
Si l'application $f'$ est différentiable en $a$, on dit que $f$ est *deux fois différentiable en $a$* et on note $D^2f(a)$ la *différentielle seconde*. Les composantes $\partial_i f(x)$ admettent alors des [dérivées partielles](#lem:partial) en $a$, notées
\begin{equation*}
    \partial_{ij} f(a)
\end{equation*}
:::

