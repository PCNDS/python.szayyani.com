---
Title : Les fonctions `array` & `arange`
order : 800
---


L'objet principal que l'on utilise dans `numpy` est un ***array*** : un tableau multidimensionnel de valeurs. Un *array* **unidimensionnell** est l'équivalent d'une colonne dans un tableur comme *EXCEL* (mathémaiquement l'équivalent d'un vecteur). 

Ayant déjà importé la bibliothéque `numpy` et l'a renommée `np`, nous allons créer deux *arrays* `A` et `B` avec la commande : `A = np.array([0,1,2,3])` et `B = np.array([0,4,9,64])`. 

Une fois ce code a été compilé on peut l'appeler dans la console : 
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