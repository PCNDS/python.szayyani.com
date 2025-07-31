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

## Opérations avec les listes

Créeons deux liste `num1` et `num2`, et puis voyaons ce qu'on peut faire comme combinaisons entre les deux listes. On les définit ici directement dans la console : 


```python 
>>> num1 = [0, 1, 2, 3, 4]
>>> num2 = [10, 5, -1, 0, 1]
>>> num1 + num2 = [0, 1, 2, 3, 4, 10, 5, -1, 0, 1]
>>> num1 - num2
ERROR
```

Ce qu'on apprend avec un exemple aussi simple c'est qu'une operation `+` entre deux listes n'est pas simplement une additions des éléments. Ceci est logique car une liste peut être un ensemble d'autres choses que nombres. Par conséquent l'opération `-` n'a pas de sens entre deux listes. Voici un autre exemple : 

```python
>>> prenoms = ["Bobo", "Bibi", "Babou"]
>>> objets = ["mangue", "table", "pc", "chaise"]
>>> prenoms + objets 
["Bobo", "Bibi", "Babou", "mangue", "table", "pc", "chaise"]
```

Voici un autre exemple : 

+++ code
```python
>>> prenoms = ["Bobo", "Bibi", "Babou"]
>>> objets = ["mangue", "table", "pc", "chaise"]
>>> prenom*2 
```
+++ sortie
```python
["Bobo", "Bibi", "Babou", "Bobo", "Bibi", "Babou"]
```
+++ explication
l'operation `prenoms*2` équivaut littéralement `prenoms+prenoms`. 
+++

Même rien nous empêche d'utiliser des listes de nombre pour notre travail scientifique, on voit bien que les listes ne sont pas vraiment bien adaptées à la tâche (surtout quand on aura besoin de manipuler des tableaux de valeurs avec des opérations mathématiques plus complexes) : pour cela nous nous tournons vers les `array`s dans la bibliothéque `numpy`, à venir. 

## Opérations pour modifier une liste 

Voici une petite liste de quelques opérations très utiles pour manipuler et modificer les *listes* dont on se sert très souvent (pour deux listes qu'on définit comme `A = ["Bobo", "Bibi", "Babou", "mangue", "banane", "Bobo", "maison"]`et `B = [1, 2, 10, 10, 18, 10, 7, 0]`): 

* `len` retourne la longueur d'une liste, c'est à dire le nombre d'élément qu'elle contient : 
```python
>>> len(A)
7
>>> len(B)
8
```
* `append` est très utilisé pour ajouter un élément à une liste
```python
>>> A.append("Bouba")
>>> A
["Bobo", "Bibi", "Babou", "mangue", "banane", "Bobo", "maison", "Bouba"]
>>> B.append("Bouba")
>>> B
[1, 2, 10, 10, 18, 10, 7, 0, "Bouba"]
```
* `count` retourne le nombre d'occurence d'un élément dans la liste 
```python
>>> A.count("Bobo")
2
>>> B.count(10)
3
```
* `remove` permet d'éliminer un élément : `B.remove(1)`
* `sort` permet d'ordonner une liste : dans l'ordre alphabétique pour une les avcec des caractères, dans l'ordre numérique croissant pour une liste avec des nombres
* `max` et `min` permettent de trouver la valeur max/min dans une liste (caractères ou nombres)
* `sum` fait la somme arithmétique des éléments dans la liste (ne marche qu'avec une liste de nombres)
* 




