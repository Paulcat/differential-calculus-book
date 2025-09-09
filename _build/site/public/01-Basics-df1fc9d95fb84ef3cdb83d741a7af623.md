# Notions d'algèbre linéaire

Un problème d'optimisation général s'écrit

\begin{equation*}
    \text{minimiser}\quad f(x) \quad \text{avec} \quad  x \in \mathcal{D}
\end{equation*}

Une grande majorité de problèmes supposent que $\mathcal{D} \subset E$ où $E$ est un *espace vectoriel* de **dimension finie**, par exemple:

- $E = \mathbb{R}^n$ (les variables sont des vecteurs) 
- $E = \mathbb{R}^{n_1 \times n_2}$ (les variables sont des matrices)
- $E = \mathbb{R}^{n_1 \times \ldots \times n_d}$ (les variables sont des tenseurs)

:::{note}
On peut étudier des problèmes d'optimisation sur des espaces plus généraux (espaces de dimension infinie, espaces métriques, etc...).  Avantage: norme, produit scalaire, etc...
:::

On commence par revenir sur des notions de bases sur le calcul dans $\mathbb^n$
