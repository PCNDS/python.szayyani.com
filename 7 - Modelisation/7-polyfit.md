---
title : Modélisation avec `polyfit`
order : 900
icon : gear
---
# Modélisation graphique avec Python

On voudrait faire la même modélisation avec PYTHON (dans Edupython à l'école) en vous servant de la bibliothèque `matplotlib.pyplot` pour l’affichage du nuage des points.

Modéliser nos résultats, c'est à dire trouver la "courbe de tendance" adaptée à nos données est différente avec Python. 

Nous avons plusieurs possibilités mais nous nous focalisons sur deux options : la fonction `polyfit(abscisse,ordonnee,ordre)` dans la bibliothèque `numpy`, ou de la fonction `linregress` dans la bibliothèque `scipy.stats`.

## Modélisation avec `polyfit`
La fonction `polyfit(abscisse,ordonnee,ordre)` nous propose la courbe décrite par une *fonction polynomial* (dont le *degrée* nous choisissons) la mieux adaptée à nos données. (Pour rappel une fonction polynomiale s'écrit comme une somme des puissance d'une variable $x$ : 
$$f(x) = a\cdot x^n + b\cdot x^{n-1} + \cdots + p\cdot x + q$$

Le **degrée $n$** de la fonction correspond à la puissance de $x$ la plus élevée. 

Vous en conniassez déjà quelques exemple : 

- $f(x) = a$ la fonction constante est un polynôme de degrée $0$
- $f(x) = a\cdot x + b$ : la fonction linéaire est une polynôme de premier degrée ($n=1$)
- $f(x) = a\cdot x^2 + b\cdot x + c$ : la fonction quadratique (qui décrit une parabole) est un polynôme de degree $2$.  
    
Commençons comme toujours avec l'importation des bibliothéques `numpy` pour le traitement des séries de nombres, et `matplotlib` pour la visualisation graphique. 

```python
import numpy as np
import matplotlib.pyplot as plt
```

Voici donc comment utiliser la fonction `polyfit` : 
- Il est important de définir les données avec la fonction `np.array`, pour que **Python** les reconnaisse comme une séries de valeur numériques (`float`) et non juste une liste d'object. 
- Une fois `numpy` importé comme np, on peut utiliser avece `np.polyfit(x,y,n)`.
    `polyfit` prend 3 arguments : $x$ = la grandeur en abscisse, la variable indépendante de la fonction;  $y$ = la grandeur en ordonnée; $n$ = le degrée de la fonction polynomiale qui modéliser les résultats.
- En fonction du type de fonction polynomiale utilisée pour la modélisation, la `polyfit` génère un certain nombre de paramètres. Par exemple, pour une modélisation par une fonction linéaire du type $y = a\cdot x + b$, `polyfit` calcule et génère les paramètres $a$ et $b$ pour la droite la mieux adaptée aux valeurs mesurées. 
    
    Ces paramètres sont stockés dans la mémoire de l'environnement de codage et afin d’y accéder il faut les 'écrire' dans des variables : `a, b = polyfit(x,y,1)` (où $x$ et $y$ sont changent en fonction des noms que nous avons donnés à nos grandeurs). 
    
    Grâce à cela, les paramètres caractérisant la droite de notre modèle sont désormais stockés dans les variables $a$ et $b$. 
    
- Afin d’afficher la droite de modélisation, il faut utiliser la fonction `plot` dans `matplotlib` : `plt.plot(x,f(x), ...)` où $x$ = est la variable indépendante, $f(x)$ = ce qu’on veut faire apparaître en ordonnée, c’est à dire la fonction $f(x)$ ; et les paramètres de visualisation comme la couleur ou le style de ligne pour la courbe. 

## Exemple d'un corrigé

```python
import numpy as np 
import matplotlib.pyplot as plt 
import scipy.stats as ss

##### Series de donnees 

m = np.array([0, 10, 40, 100, 150, 200, 250]) #les masses utilisees
P = np.array([0, 0.15 , 0.35, 1.1, 1.5, 1.9, 2.7 ]) #les poids mesures

##### Trace de la courbe de tendance avec POLYFIT

a, b = np.polyfit(m, P, 1) #etant donne que les resultats ont l'allure lineaire
print("le coefficient directeur est :", a, " N/g")

##### Trace de la courbe de tendance avec LINREGRESS

c, d, rvalue, pvalue, stderr = ss.linregress(m, P)
print("le coefficient directeur est :", c, " N/g ; et Le coefficient de correlation est :", rvalue)


##### graphique de P = f(m)
plt.plot(m,P, 'x', label = "modèle lingress")
plt.plot(m, a*m+b, 'r--', label = "modele polyfit")
plt.title( "P = f(m)")
plt.xlabel("masse m (kg)")
plt.ylabel("poids P (N)")
plt.legend(loc = "best")
plt.grid(True)
plt.savefig("massePoids.png")
plt.show() 
```
