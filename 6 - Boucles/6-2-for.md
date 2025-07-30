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
+++ explication
la fonction `range(n)` fait un décompte de $0\to n-1$. 


