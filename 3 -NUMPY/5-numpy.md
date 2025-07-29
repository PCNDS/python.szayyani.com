---
order : 999
icon : number
---
# :icon-book: Bibliothéque `numpy`

`numpy` est une des bibliothéques les plus utiles pour nous en physique (mais aussi dans tout autre domaines y compris la *Data Science* l'apprentissage machine )

Il s'agit d'une bibliothéque de fonctions spécialisées pour des opérations mathématiques de toutes sorte *sur des séries de données*, c'est à dire sur des matrices ou des tables de chiffres. (`numpy` est conçu particulièrement pour des opérations d'*algèbre linéaire*.). `numpy` nous permet de manipuler des vecteurs et des matrices, qui sont d'une utilité particulièrement centrale pour nous, et omniprésents dans tout domaine de la physique (et de la chimie).

C'est une bibliothéque particulièrement adaptée à ce que l'on fait en physique : l'étude des résultats expérimentaux et la modélisation. En déhors du monde de la physique, la plupart de ce que l'on appelle *Data Science* (comme par exemple l'entrainement des IA) est fait avec `numpy`.


## Quelques fonctions importantes

Sans entrer trop en détail voici une (très) petites liste des fonctions que l'on utilisera de temps, et certaines plutôt souvent 

- `np.array()` : la commande pour créer un tableau/série de valeurs. 
- `np.arange()` : Pour créer un tableau avec des valeurs régulièrement espacées. exemple :
- `np.linspace()` : pour créer un tableau avec des valeurs uniformément repartie dans intervalle donné. exemple : 
- `np.sqrt()` : pour calculer la racine carré des différentes valeurs dans un tableau
- `np.sin()`, `np.cos()`, `np.tan()`,`np.asin()`, `np.acos()`, `np.atan()`, `np.log()` : des fonctions trigonométriques et logarithmique de bases. 
- `np.dot()` : pour calcul le *produit scalaire* de deux vecteurs (vous verrez ça en classe de première). Exemple : 
- `np.polyfit()` : une fonction puissant pour modélisation polynomiale des séries de valeurs. Nous sommes particulièrement intéressés par cette fonction, en physique où notre tache principale est la construction des modèles à partir des résultats et des observations expérimentaux.

Dans les parties suivantes nous allons plonger un plus grand détail dans l'utilisation des plus importantes de ses fonctions, avec des exemples divers. 

## Calculs mathématiques sur des séries de nombres

---
Il y a bien sur **beaucoup** d'autre fonction dans `numpy` mais pour nous (en physique au lycée) celles-là suffiront. 

> {% hint style="info" %}
> Point de comparaison entre bibliothéques `math` et `numpy` :
> 
> ```python
> import math
> import numpy as np
> 
> # Utilisation de math (sur un scalaire)
> print(math.sqrt(4))  # Résultat : 2.0
> 
> # Utilisation de NumPy (sur un array)
> 
> array = np.array([1, 4, 9])
> print(np.sqrt(array))  # Résultat : [1. 2. 3.]
> ```
> {% endhint %}
