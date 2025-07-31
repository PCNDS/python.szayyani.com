---
title : Les Listes 
order : -3
---

# Les `liste`s

Un des *objets* le plus utiles et plus utilisés dans PYTHON est une liste. 

Une liste est simplement *un ensemble d'éléments* auquel un donne on nom, que l'on peut manipuler par la suite. 

!!!success ***Point Syntaxe***
On créer une liste très simplent en mettant des éléments entre crochets : `[ ]`. 
Voici un exemple d'une liste de prénoms : 
```python 
prenoms = ["Bobo", "Bibi", "Babou"]
```
et voici une liste de nombres
```python
nombres = [1, 10, -6, 0, 389]
```
!!!

## Accéder aux élements dans une liste

Chaque élement dans une liste est situé à une position que l'on peut préciser. Prenons la liste `prenoms` que l'on a déjà créee. Pour préciser un élément dans la liste il faut donner le nom de la liste suivi des crochets et le numéro de l'élément (le premier étant toujouts 0) : 

```python
>>> prenoms[0] #donne le premier élément dans la liste
Bobo
>>> prénoms[2] #donne le 3e élément dans la liste
Babou
```
Ou encore avec la liste `nombres` : 

```python 
>>> nombres[3] #donne la 4e élément
0
```

## Opérations pour modifier une liste 




