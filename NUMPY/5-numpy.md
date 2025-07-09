---
Titre : 
---
# :icon-book: Bibliothéque `numpy`

`numpy` est une des bibliothéques les plus utiles pour nous en physique (mais aussi dans tout autre domaines y compris la *Data Science* l'apprentissage machine )

Il s'agit d'une bibliothéque de fonctions spécialisées pour des opérations mathématiques de toutes sorte *sur des séries de données*, c'est à dire sur des matrices ou des tables de chiffres. (`numpy` est conçu particulièrement pour des opérations d'*algèbre linéaire*.). `numpy` nous permet de manipuler des vecteurs et des matrices, qui sont d'une utilité particulière pour nous, et omniprésents dans tout domaine de la physique (et de la chimie).

C'est une bibliothéque particulièrement adaptée à ce que l'on fait en physique : l'étude des résultats expérimentaux et la modélisation. En déhors du monde de la physique, la plupart de ce que l'on appelle *Data Science* (comme par exemple l'entrainement des IA) est fait avec `numpy`.


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
## La fonction `arange`


## La fonction `linspace`


## La fonction `dot`

## la fonction `linalg.solve` : 


Celle-là est un de nos grands amis, car `linalg.solve` nous permet de résoudres des équations algébrique, mais surtout des systèmes d'équations. 

C'est donc un outil puissant pour nous en physique car nos problèmes se réduisent très souvent en un système d'équation à résoudre (et ce même dans des domains de physique bien plus avance tel que la mécanique quantique). 

De manière général `linalg.solve` nous permet de résoudre des équation du type : $A\cdot X = b$ où on connait $A$ et $b$. Voici un exemple très basique : $$ 4\cdot x = 8$$ 
Ici $A \to 4$, $X \to x$ et $b \to 8$. C'est l'exemple le plus simple et basique que l'on peut donner. Utile, mais pas *très* intéressant. Voici comment trouver la solution avec `linalg.solve` : 

+++ code
```python!
import numpy as np 

# définissons nos données 
A = np.array([[4]])
b = np.array([8])

#passons à la résolution 
X = np.linalg.solve(A,b)

print(X) #pour afficher le résultat    
```
+++
+++ sortie
```python!
>>> 2
```
+++

!!!danger Attention : 
* `linalg.solve` prend comme argument des `array` et donc il faut toujours définir ses variable et données par la fonction `array`
* `linalg.solve` est *conçu* pour résoudre des *systèmes d'équations* et donc va toujours supposer que le $A$ est une matrice au moins en 2 dimensions, d'où `A = np.array([[4]])` et non `A = np.array([4])`, tandis que `b = np.array([8])`. 
!!!

La vraie puissance de cette fonction est dans ça capacité à résoudre des systèmes d'équation, telle que vous l'avez appris en fin du collège. 

Prenons un exemple simple: deux équations linéaires avec deux variables inconcue $x$ et $y$: 
$$4x + 3y = 10 $$ $$3x + 2y = 6$$

On peut réécrire ce système sous forme $A\cdot X = b$ : 
$$
\begin{bmatrix}4 & 3\\\ 3 & 2\end{bmatrix} \cdot \begin{bmatrix} x \\\ y \end{bmatrix} = \begin{bmatrix} 10 \\\ 6 \end{bmatrix}
$$

où $A = \begin{bmatrix}4 & 3\\\ 3 & 2\end{bmatrix}$ et $b= \begin{bmatrix} 10 \\\ 6 \end{bmatrix}$. Le matrice $\begin{bmatrix} x \\\ y \end{bmatrix}$ correspond donc à la *solution* que `linalg.solve` doit nous trouver. 

+++ code
```python!
import numpy as np 

# définissons nos données 
A = np.array([[4, 3], [3, 2]])
b = np.array([10, 6])

#passons à la résolution 
X = np.linalg.solve(A,b)

print(X) #pour afficher le résultat    
```
+++
+++ sortie
```python!
>>> 2 #X est donc la matrice avec les deux solutions pour x et y
```
+++






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
> ```python
> array = np.array([1, 4, 9])
> print(np.sqrt(array))  # Résultat : [1. 2. 3.]
> ```
> {% endhint %}
