---
Title : Fonction: `arange`
order : 780
---

## La fonction `arange`

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
