---
title : Les Fonctions
order : 900
icon : zap
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

!!!warning Respecte la Syntaxe !
* la ligne où on nomme la fonction avec `def` il est impératif de finir par `:`
* l'indentation des lignes qui suivent est impérative aussi, et à respecter. 
!!!

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

+++ code
```python
def salut(a) : 
    return print("Salut ", a,  "!")
```
+++ résultats 
```bash 
>>> salut(David)
Salut David !
>>> salut(pénélope)
Salut pénélope !
```
+++

Voyons quelques exemples de fonction prenant deux arguments. 

+++ code
```python
def puissance(a,b) : #on veut calculer a pris à la puissance b 
    return print(a**b)
```
+++ résultats
```bash
>>> puissance(2,3)
8
>>> puissance(10,5)
100000
```
+++

On a une autre manière de faire la même chose que dans l'exemple précédent : 

+++ code
```python
def puissance(a,b) : #on veut calculer a pris à la puissance b 
    res = a**b
    return res
```
+++ sortie
```bash
>>> puissance(2,3)
>>> print(res)
8
>>> puissance(10,5)
>>> print(res)
100000
```
+++

Un autre exemple plus applicable pour nous en physique : on peut définir une fonction qui calcule la vitesse à partir d'une distance et d'une durée : 

+++ code
```python
def vitesse(d,t) : 
    v = d/t
    return v)
```
+++ sortie
```bash
>>> vitesse(100,5) #on parcourt 100 m en 5 secondes
>>> print("la vitesse est donc ", v, "metres par secondes")
la vitesse est donc 20 metres par secondes
```
+++

Faisons quelques exercices d'application, facile et qui pourraient nous aider dans le future : 

[!Badge :icon-pencil: Exercice d'application]
+++ Enoncé 
1.  Définir une fonction `mpsKPH` qui permet de convertir une vitesse en $\frac{m}{s}$ en $\frac{km}{h}$. 

2.  Définir une fonction `Ec` qui calcule l'énergie cinétique pour une masse et une vitesse donnée. 

+++ Code 1
```python
def mpsKPH(a) : #la fonction prend qu'un seul argument, la vitesse en mps
    return a*3.6 
```
exemple : 
```bash
>>> mpsKPH(1)
3.6
>>> mpsKPH(36)
129.6
```
+++ Code 2
```python
def Ec(m,v) : 
    return 0.5*m*v**2
```
exemple : 

```bash
>>> Ec(10,5) #pour une masse de 10kg et vitesse de 5 m/s
125
>>> Ec(0.5, 20) #pour une masse de 500g et vitesse de 20 m/s
100 
```
+++
