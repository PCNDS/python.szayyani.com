---
Title : Création des `Arrays` : `arage` & `linspace`
order : 800
---

### Qu'est-ce qu'un `array`

L'objet principal que l'on utilise dans `numpy` est un ***array*** : un tableau multidimensionnel de valeurs. Un *array* **unidimensionnell** est l'équivalent d'une colonne dans un tableur comme *EXCEL* (mathémaiquement l'équivalent d'un vecteur). 

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

### Différents types de `arrays`

Mais ... les arrays sont bien plus que juste une "liste de valeur". Ce sont des objets mathématiques, que l'on appelle des ***matrices***. On ne se sert pas beaucoup (ou du tout) des _matrices_ au lycée, mais ils sont partout dans le supérieure (surtout pour nous en physique). On peut visualiser une _matrice_ comme une grille de valeurs : une matrice $m\times n$ est composée de $n$ colonnes et de $m$ lignes de valeurs : 

$$A = \begin{bmatrix} 4 & 3\\\ 3 & 2\end{bmatrix} \quad B = \begin{bmatrix} 4 & 3 & 0 & -5\end{bmatrix}\quad C = \begin{bmatrix} 4 \\\ 3 \\\ -5\end{bmatrix} \quad D = \begin{bmatrix} 4 & 3 \\ 0 & -5\\7 & 23\end{bmatrix}$$ 

$A$, $B$, $C$ et $D$ sont quatre matrices différentes. Leurs dimensions sont $A\to 2\times 2 \quad ; \quad  B\to 1\times 4 \quad ; \quad C\to 
3\times 1 \quad ; \quad D\to 3\times 2$. 

!!! Remarque
Nous allons pas entrer en détail sur le sense mathématiques et physique de ces matrices encore, car le niveau est bien au-delà de ce que nous faisons au lycée, par en tant qu'exemple vous pouvez voir que matrice $C$ peut représent un *vecteur* : les trois chiffres représentent les coordonnées du vecteur $\vec{v} = (4, 3, -5)$. Par conséquent toute opérations effectuée sur cette matrice, représentent des opérations/manipulations faites au vecteur $\vec{v}$. 
!!!

Comment peut on donc créer des *arrays*? On va apprendre trois méthodes simples. 

### La Fonction `array`

La méthode la plus simple et la plus directe (mais pas forcément la plus utile) est de simple *définir* l'array et ses constituants, comme dans l'exemple suivant : 

+++ Code
```python
A = np.array([[4,3],[3,2]])
B = np.array([[4,3,0,-5]])

print("A est ", A) #pour afficher l'array A
print("B est ", B)
```
+++ Sortie
```pyton
>>> A est  [[4 3]
 [3 2]]
 >>> B est  [[ 4  3  0 -5]]
``` 
+++

Il y a d'autres méthodes de créer une matrice avec la fonction `array`, mais pour le moment ce que l'on a vu suffira. 

Dans les cas précédents on a pu utiliser la fonction `array` car nous avions déjà les valeurs que l'on voulait mettre dans notre matrice. Cela peut être très utile par exemple dans le cas des mesures expérimentales que nous avons relevées lors d'une expérience (des distances parcourues par un objet, des valeur de pH mesurées avec un pH-mètre, etc). 

En revanche, parfois nous voulons juste une séries de valeurs à un intervalle régulier. Pour cela nous avons deux fonctions très pratiques et simples : `arange` et `linspace`

### La fonction `arange`

La fonction `arange` permet la création d'un *array* en précisant **la valeur minimale, la valeur minimal** et **le pas** entre les valeurs, c'est à dire *l'intervalle entre valeurs successives*. 

Allons directement à un exemple pour mieux comprendre : 

+++ code
```python
D = np.arange(0, 10, 1) #une série de valeurs allant de 0 à 10 avec un pas de 1

print(D)
```
+++ sortie
```python
>>> [0 1 2 3 4 5 6 7 8 9]
```
+++

C'est aussi simple que ça. Voilà un autre exemple : 

+++ code
```python
D = np.arange(-2,2, 0.5) #une série de valeurs allant de -2 à 2 avec un pas de 0.5

print(D)
```
+++ sortie
```python
>>>[-2.  -1.5 -1.  -0.5  0.   0.5  1.   1.5]
```
+++

!!!important
Notez qu'avec la fonction `arange` la limite maximale n'est pas incluse dans l'array formé. 
!!!

### La fonction `linspace`

Le fonctionnement de `linspace` est quasi-identique à celui de `arange` avec une différence principale : avec `linspace` on précise le nombre de valeurs dans la série entre les valeurs max/min, tandis qu'avec `arange` on précise le pas. 

Voici un exemple : 

+++ code
```python
D = np.linspace(0,10, 11) #une série de 11 valeurs allant de 0 à 10

print(D)
```
+++ sortie
```python
>>> [ 0.  1.  2.  3.  4.  5.  6.  7.  8.  9. 10.]
```
+++

et voici un autre exemple : 

+++ code
```python
D = np.linspace(-5, 5, 5) #une série de 5 valeurs allant de -5 à 5

print(D)
```
+++ sortie
```python
>>> [-5.  -2.5  0.   2.5  5. ]
```
+++

