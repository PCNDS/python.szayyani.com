---
title : Boucle FOR
order : -1
---

# Boucle `FOR`

On utiliser la boucle `for` quand nous savons combien de fois nous voulons faire un calcul, ou executer une séries d'instruction. 

Voilà la structure générale d'une boucle `for` : 

!!!success Point Syntaxe
```python
for élement in séquence : 
    les instructions

la suite du programme
```

* important de noter le `:` à la fin de la première ligne qui est obligatoire 
* **l'indentation** est à respecter, car il n'y a rien pour signaler la fin de la boucle sauf le retour à la ligne à la fin de la boucle
* le `for` et le `in` sont obligatoire dans la déclaration des conditions de la boucle
!!!

Regardons quelques exemples simples pour mieux comprendre. 

!!!light [!Badge :icon-pencil: Exemple]
+++ description
On veut un programme qui dit bonjour dans l'ordre à une liste de nom que l'on définit au début. 
+++ code 

```python 
prénoms = ["Bobo", "Babou", "Bibi"]

for noms in prénoms : 
    print("salut ", nom)
```
+++ sortie
```bash
>>> Bobo
Babou
Bibi
```
+++ Remarque 
Les prénoms sont des caractères d'où la nécessité de mettre les guillements quand on définit la liste. 
+++
!!!

Voic un autre exemple qui utiliser une nouvelle fonction `range`qui est très pratique et utile pour nous. 

+++ Description
On veut créer un compteur, et lui dire de compter de zero à 5. 
+++ code
```python
for i in range(6) : 
    print(i)
```
+++ sortie 
 ```bash
 >>> 0
 1
 2
 3
 4
 5
 ```
 +++

!!!success *** Point Syntaxe***
* la fonction `range(n)` fait un décompte de $0\to n-1$. Dans un premier temps la boucle commence avec une valeur par défaut $0$ (car on n'a pas précisé quel valeur pour le départ). et puis a la fin de chaque boucle $i$ passe au numéro suivant, et puis s'arrête à la valeur de $n-1$. 
* on peut préciser dans quelle *gamme* de valeur on veut utiliser `range`, comme `range(2,6)`. 
!!!

+++ description 
On veut un compteure qui commence à $3$ et arrête à $10$. 
+++ code 
```python
for in range(3,11) : 
    print(i)
```
+++ sortie
```bash
>>> 
```
+++ remarque
Attention au fait que pour `range(a,b)` la gamme des valeur va de $a\to b-1$. 
+++


