---
title : Bibliothéques `math`
order : 0
---

Cette bibliothéque standard de PYTHON permet d'élargir le nombre d'opérations mathématiques possibles au-delà des opérations de base déjà présentes en PYTHON. 

Voici ce que contient (globalement) `math` : 
- opérations mathématiques plus avancées : des fonction *trigonométriques* (`sin()`, `cos()`, `tan()`, `asin()`, `acos()`, `atan()`, `radians()`, etc), des fonctions *logarithmiques* et *exponentielles* (`exp(x)`, `log(x)`, `log10(x)`, `pow(x, y)`, `sqrt(x)`, etc),
- Des constantes importantes : `pi`, `e`, `inf`, etc
- d'autres fonctions *numériques* : `ceil(x)`, `floor(x)`, etc

## Quelques exemples 
Supposons que nous avons importé `maths as m`. 

### Fonctions trigonométriques : 
Si l'on veux utiliser les fonctions trigonométrique $\sin/\cos/\tan$ (et leurs inverses $\arcsin/\arccos/\arctan$) en `Python` il faut obligatoirement passer par `math` (ou `numpy` mais on verra cela dans le prochain chapitre). 

!!!warning Remarque
Dans le langage `Python` l'argument des fonctions trigo est par défaut en *radian* et non en degrées; et donc par exemple, `m.sin(90)` sera interprété comme sinus de $90\; rad$. 
!!!

Voici quelques exemples 
```python 
>>> m.sin(0)
0
>>> m.sin(m.pi)
0
>>> m.tan(m.pi/8)
1
>>> m.sin(m.pi/4)
1
>>> m.cos(m.pi/3)
0.5
>>> m.asin(1)
pi/4
```
### Conversion $radians \leftrightarrow °$ 

On peut aussi convertir les angles de radians en degrées et l'inverse : 
```python
>>> m.radians(180) # pour convertir degrees en radians
3.141592653589793
>>> m.degrees(m.pi) # pour convertir radians en degrees
180.0
```
### Puissances et logarithmes

* Pour calculer une puissance du genre $x^y$, il y a `math.pow(x,y)` : 
```python
>>> m.pow(2,4)
16
>>> m.pow(4,0.5)
2
```
* Pour calculs une exponentielle du genre $e^{n}$ il y a `math.exp(n)` : 
```python
>>> m.exp(1)
2.718281828459045
>>> m.exp(-1)
0.36787944117144233
```
* pour les calcul lograithmique du genre $\log_{base}{x}$ il y a `log(x,base)`. Important de note que la valeur *par défaut* de la base est $e$, c'est à dire `m.log(x)`$=\ln(x)$, et donc `m.log(x,10)`$= \log_{10}(x)$: 
```python
>>> m.log(1,10) #log de 0 en base 10
0.0
>>> m.log10(10) # log de 10 en base 10
1.0
>>> m.log(m.e) #ln(e)
1.0
>>> m.log(5**2,5) # log de 5^2 en base 5
2.0
```
* calcul de la racine carré $\sqrt{x}$ grâce à `m.sqrt(x)` : 
```python
>>> m.sqrt(9)
3.0
>>> m.sqrt(5**10)
3125 #c'est a dire 5^5
```

### Autres fonction mathématiques 
* `m.floor` arrondi un décimale vers le bas
```python
>>> m.floor(10.6)
10
```
* `m.ceil` arrondi un décimal vers le haut 
```python 
>>> m.ceil(10.4)
11
```
* `m.factorial` pour calculer le factoriel d'un nombre : $x!$
```python
>>> m.factorial(3)
6
```
* `m.gcd` pour calculer le *plus grand dénominateur commun* entre deux nombres
```python
>>> m.gcd(15,160)
5
```

## Des constantes mathématiques 
Une autre utilisation importante de cette bibliothéque est la présence des constantes importantes en maths, notamment : $\pi \; e \; \text{et } \infty $. 

|constante| fonction `math`|
|:----:|:----:|
|$e$ constante d'Euler| `math.e`|
|$\pi$ pi|`math.pi`|
|$\infty$| `math.inf`|


!!!tip 
La particularité de la bibliothéques `math` est le fait qu'elle est conçu pour opérer sur des ***scalaires***, c'est à dire un seul nombre à chaque fois, et *non* une série de nombre. 
!!!