---
Title : Les `Arrays`
order : 800
---

## Qu'est-ce qu'un `array`

L'objet principal que l'on utilise dans `numpy` est un ***array*** : un *tableau multidimensionnel de valeurs*. Un *array* **unidimensionnell** est l'équivalent d'une colonne dans un tableur comme *EXCEL* (mathémaiquement l'équivalent d'un vecteur). 

Ayant déjà importé la bibliothéque `numpy` et l'a renommée `np`, nous allons créer deux *arrays* `A` et `B` de manière suivante  : 
```python
# supposons que nous avon déjà importé la bibliothéque numpy comme np

A = np.array([0,1,2,3])  
B = np.array([0,4,9,64])
```

Une fois ce code a été compilé on peut les appeler dans la console : 

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

Notez bien comment nous avons pu manipuler les valeurs dans les arrays : 
* une opération de base comme la multiplication applique l'opération à _tous_ les éléments de l'array 
* de même pour les opérations mathématique entre deux arrays (au contraire des `lists`)

## Différents types de `arrays`

Mais ... les arrays sont bien plus que juste une "liste de valeur". Ce sont des objets mathématiques, que l'on appelle des **tableaux** ou plus mathématiquement ***matrices***. On ne se sert pas beaucoup (ou du tout) des _matrices_ au lycée, mais ils sont partout dans le supérieure (surtout pour nous en physique). On peut visualiser une _matrice_ comme une grille de valeurs : une matrice $m\times n$ est composée de $n$ colonnes et de $m$ lignes de valeurs : 

$$A = \begin{bmatrix} 4 & 3\\\ 3 & 2\end{bmatrix} \quad B = \begin{bmatrix} 4 & 3 & 0 & -5\end{bmatrix}\quad C = \begin{bmatrix} 4 \\\ 3 \\\ -5\end{bmatrix} \quad D = \begin{bmatrix} 4 & 3 \\ 0 & -5\\7 & 23\end{bmatrix}$$ 

$A$, $B$, $C$ et $D$ sont quatre matrices différentes. Leurs dimensions sont $A\to 2\times 2 \quad ; \quad  B\to 1\times 4 \quad ; \quad C\to 
3\times 1 \quad ; \quad D\to 3\times 2$. 

!!!info Remarque
Nous n'allons pas entrer en détail sur le sense mathématiques et physique de ces matrices encore, car le niveau est bien au-delà de ce que nous faisons au lycée, par en tant qu'exemple vous pouvez voir que matrice $C$ peut représent un *vecteur* : les trois chiffres représentent les coordonnées du vecteur $\vec{v} = (4, 3, -5)$. Par conséquent toute opérations effectuée sur cette matrice, représentent des opérations/manipulations faites au vecteur $\vec{v}$. 
!!!

Comment peut on donc créer des *arrays*? On va apprendre trois méthodes simples. 

