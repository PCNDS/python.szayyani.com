# :icon-book: Bibliothéque `numpy`

Une bibliothéque spécialisée pour des opérations mathématiques de toutes sorte *sur des séries de données*, c'est à dire sur des matrices ou des tables de chiffres. (`numpy` est conçu particulièrement pour des opérations d'*algèbre linéaire*.)

Il s'agit d'une bibliothéque particulièrement adaptée à ce que l'on fait en physique : l'étude des résultats expérimentaux et la modélisation. En déhors du monde de la physique, la plupart de ce que l'on appelle *Data Science* (comme par exemple l'entrainement des IA) est fait avec `numpy`.


## Quelques fonctions importantes

Sans entrer trop en détail voici une (très) petites liste des fonctions que l'on utilisera de temps, et certaines plutôt souvent : 

- `np.array()` : la commande pour créer un tableau/série de valeurs. 
- `np.polyfit()` : une fonction puissant pour modélisation polynomiale des séries de valeurs. Nous sommes particulièrement intéressés par cette fonction, en physique où notre tache principale est la construction des modèles à partir des résultats et des observations expérimentaux. 
- `np.arange()` : Pour créer un tableau avec des valeurs régulièrement espacées. exemple : 
```python
np.arange(0, 10, 2)  # donne [0, 2, 4, 6, 8]
```
- `np.linspace()` : pour créer un tableau avec des valeurs uniformément repartie dans intervalle donné. exemple : 
```python
np.linspace(0, 1, 5)  #  donne [0., 0.25, 0.5, 0.75, 1.]
```
- `np.sqrt()` : pour calculer la racine carré des différentes valeurs dans un tableau
- `np.sin()`, `np.cos()`, `np.tan()`,`np.asin()`, `np.acos()`, `np.atan()`, `np.log()` : des fonctions trigonométriques et logarithmique de bases. 
- `np.dot()` : pour calcul le *produit scalaire* de deux vecteurs (vous verrez ça en classe de première). Exemple : 
```python
np.dot(A,B)  # donne 214
```

## La fonction `array`

L'objet principal que l'on utilise dans `numpy` est un ***array*** : un tableau multidimensionnel de valeurs. Un *array* **unidimensionnell** est l'équivalent d'une colonne dans un tableur comme *EXCEL* (mathémaiquement l'équivalent d'un vecteur). 

Ayant déjà importé la bibliothéque `numpy` et l'a renommée `np`, nous allons créer deux *arrays* `A` et `B` avec la commande : `A = np.array([0,1,2,3])` et `B = np.array([0,4,9,64])`. Une fois ce code a été compilé on peut l'appeler dans la console : 
```python
>>> A
[0,1,2,3]
>>> B
[0,4,9,64]
```
maintenant je peux faire des opérations mathématiques de toute sorte *sur toutes les valeurs* dans ces tableaux. 

Voici quelques exemples : 
```python
>>> 3*A
[0,3,6,9]
>>> A**3
[0,1,8,27]
>>> np.sqrt(B) # sqrt (square root) est la fonction de racine carré
[0,2,3,8]
>>> A + B 
[0, 5, 11, 67]
>>> np.sin(A)
[0. 0.84147098 0.90929743 0.14112001]
```


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
> ```python
> array = np.array([1, 4, 9])
> print(np.sqrt(array))  # Résultat : [1. 2. 3.]
> ```
> {% endhint %}
