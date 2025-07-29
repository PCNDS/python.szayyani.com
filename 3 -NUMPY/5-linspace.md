---
Title : Fonction `linspace`
order : 760
---


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

