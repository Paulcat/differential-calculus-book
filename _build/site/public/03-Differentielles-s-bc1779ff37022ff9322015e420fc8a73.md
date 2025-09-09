# Différentielles secondes

L'étude locale d'une fonction peut s'affiner au-delà de l'approximation tangentielle (linéaire), en explicitant les termes d'ordre supérieur dans les termes correctifs "petit o". Géométriquement, les termes d'ordre 2 contrôlent la position de la variété (courbe, surface, etc...) par rapport à sa tangente (convexité, concavité, points d'inflexion, etc...).

On se contentera d'étudier l'ordre 2 uniquement pour des fonctions à valeurs numériques.

## Différentielle seconde

Si $f:\mathbb{R}^n \to \mathbb{R}$ est [différentiable](#def:diff) en un point $a$, sa différentielle $L$ définit une application d'un voisinage de $a$ dans $\mathbb{R}^n$:

:::{margin}
Ici on identifie *l'application* linéaire $L(h) = f'(a) \cdot h$ avec le *vecteur* $f'(a) \in \mathbb{R}^n$.
:::

\begin{equation*}
:::{margin}
test
:::
    x = (x_1,\ldots,x_n) \mapsto \left( \partial_1 f(x), \ldots, \partial_n f(x) \right))
\end{equation*}

:::{margin}
Ici on identifie *l'application* linéaire $L(h) = f'(a) \cdot h$ avec le *coefficient* $f'(a)$


