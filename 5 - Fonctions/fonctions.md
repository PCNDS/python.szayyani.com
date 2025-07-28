---
title : Fonctions
order : 900
---
# Fonctions : un superpouvoir

Tout ce que l'on a pu faire jsuqu'alors a été grâce aux différentes fonctions que vous avez vues, dans des différentes bibliothéques. Ce qu'il faut savoir c'est que toutes ces fonctions ont été *définies* par quelqu'un et puis rendues disponibles et réutilisables. Par exemple pour calculer une *racine carrée* comme on a vu avec `sqrt()`, il y a un algorithm qui a été défini et puis mis dans une bibliothéque, afin de ne pas forcer chaque individu à rédéfinir cet algorthme calculatoire pour pour chaque calcul de racine carrée. 

En effet, une bibliothéque est un ensemble de ces fonctions, créees et définies par des individus partout (presque toujours gratuitements) afin de simplifier la tâche de codage ! ... Et vous pouvez faire la même chose ! 

!!!success ***Définition***
- Une fonction est un bloc de code qui peut être réutilisé plusieurs fois dans un programme, afin de rendre le programme plus organise, claire et économique. 
- une fois définie on peut penser d'une fonction comme une machine qui prend des *arguments* ou des *paramètres* et renvoie un résultats en modifiant ces arguments. 
!!!

## Déclaration d'une fonction 

*Déclarer* une fonction est comment on la définit, c'est-à-dire définir l'opération que l'on voudrait effectuer sur les paramètres d'entrée. 

On utilise `def` pour commence, suivi du nom de la fonction et les paramètres à inclure; puis nous définissons l'ensemble des opération à effectuer sur ces paramètres et pour finir, on donne ce que la fonction doit *retourner*, c'est à dire le résultat final. Voilà la forme générale schématique d'une déclaration de fonction

```python
def nom_dela_fonction(param1, param2, ...) :
    code qui donne les instructions
    return résultat
```

Regardons un exemple simple : on va définir une fonction `carre` qui calcule le carré d'un nombre `a`. 


```python
def carre(a) :
    return a*a
```

une fois définie nous pouvons utiliser cette fonction avec différentes valeurs de `a` : 

```bash
>>> carre(2)
4
>>> carre(10)
100
>>> carre(2.5)
6.25
```

Une fonction n'est pas que pour les calculs mathématiques, mais aussi d'autres opérations. Voici un exemple :

+++ Code
```python
def salut(a) : 
    return print("Salut ", a,  "!")
```
+++ Résultats 
```bash 
>>> salut(David)
Salut David !
>>> salut(pénélope)
Salut pénélope !
```

Voyons quelques exemples de fonction prenant deux arguments. 

+++ Code
```python
def puissance(a,b) : #on veut calculer a pris à la puissance b 
    return print(a**b)
```
+++ Résultats
```bash
>>> puissance(2,3)
8
>>> puissance(10,5)
100000
```
+++