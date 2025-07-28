---
icon : graph
order : 999
---

# Bibliothéque `matplotlib.pyplot`

Il s'agit d'une bibliothéque *essentielle* pour nous en physique car c'est notre outil principal de visualization de nos résultats expérimentaux. 

`matplotlib` est une bibliothéques vaste avec beaucoup de possibilité de visualisation des données, allant des nuages de points (notre utilisation principale au lycée), jusqu'aux camembers, histogrammes, bar-graphes ... 


## Création d'un graphique

La commande la plus basique de création d'un graphique/tracé est `plot` (verbe anglais pour "tracer un graphique"). 

La fonction `plot` prend *au moins* deux arguments : abscisse, et ordonnée. Mais, elle peut prendre plus aussi : ce sont des paramètres *optionnels* qui permettent d'affiner l'apparence du graphique. On les verra dans une sous-partie qui suit. Il est important de noter que l'argument d'ordonnée peut etre une série de valeur (comme un `array`), ***ou*** une fonction. 

Si après important nous avons nommée la bibliothéque `plt` la commande devient `plt.plot(abscisse,ordonnée)`

Il nous faut au moins une deuxième fonction dans `matplotlib` afin d'afficher notre graphique : `show()`, qui indique à PYTHON *d'afficher le graphique que l'on vient de créer*. 

Exemple : 

```python   
import numpy as np
import matplotlib.pyplot as plt

X = np.array([0, 1, 3, 5, 10])
Y = np.array([0, 2, 6, 7, 15])

plt.plot(X,Y)
plt.show()
```
ce qui donne : 
![fig](https://hackmd.io/_uploads/HkP5kN_0R.png)

Bon, c'est en effet un graphique, minimaliste ... *trop* minimaliste pour nous en physique (on veut un nuage de points, car relier les mesures comme ça n'a aucun sens physique pour nous!). Mais on a le minimum pour créer un graphique maintenant. 

## 'Enjolification/formatage' de votre graphique 

Il y a quelques fonctions supplémenatires à apprendre afin de pouvoir créer un graphique plus digne de ce nom ! dans un premier temps nous allons apprendre à ajouter quelques paramètres optionnels à la fonction `plot` et puis ajouter d'autres fonctions pour complèter le graphique. 

Paramètres optionnels de formatage de la fonction `plot` : 
- **couleur** : `'b'` -> bleu, `'r'` -> rouge, `'g'` -> vert, `'k'` -> noir 
- **marquer** (style des points des données) : `'x'` -> croix, `'+'` des + , `'o'` -> des ronds , `'s'` -> des carrés , `'D'` -> des losanges, `'^'` -> des triangles
- **style des lignes/coursbes** : `'-'` -> ligne continue, `'--'` -> ligne pointillée, `'-.'` -> ligne mixte, `':'` -> ligne *en* pointillées
- `label` : afin de donner une étiquette à une courbe qui apparaîtra dans la légende. Ex : `label="angles en radians"`


Quelques fonctions supplémentaires pour le formattage du graphique : 
- `title()` : permet la création du titre du graphique 
- `xlabel()` et `ylabel()` : permettent de donne le titre de chaque axe 
- `legend()` : ajoute une légendre au graphique, ce qui serait nécessaire dans les cas où nous visualisons plusieurs courbes à la fois. 
- `grid()` : permet d'afficher un quadrillage sur le graphique. 
- `xlim()` et `ylim()` : permet de vous définir les valeurs max/min de vos axes 


## Plusieurs courbes sur un même graphique
Nous avons besoin, souvent, de mettres deux ou plusieurs courbes/séries de valeur sur un même graphique. C'est très facile de faire cela en PYTHON. Il suffit de créer chaque courbe avec une fonctioni `plot` séparée avant de donner l'instruction d'affiche avec `show()`. Voici un exemple : 

```python
import numpy as np
import matplotlib.pyplot as plt

W = np.array([0, 1, 2, 3, 4, 5])
X = np.array([0, 2, 4, 6, 8, 10])
Y = np.array([0, 4, 8, 12, 16, 20])

plt.plot(W,X)
plt.plot(W,Y)
plt.show()
```
Ce qui donne le graphique suivant : 
![fig2](https://hackmd.io/_uploads/S1NN8Nu0A.png)

Vous voyez maintenant l'intérêt du formattage et l'étiquettage de vos graphiques ! 

Un exemple plus complet donc : 

```python
import numpy as np
import matplotlib.pyplot as plt

W = np.array([0, 1, 2, 3, 4, 5])
X = np.array([0, 2, 4, 6, 8, 10])
Y = np.array([0, 4, 8, 12, 16, 20])

plt.plot(W,X, 'xg', label="X = f(W)")
plt.plot(W,Y, 'Db', label="Y = f(W)")
plt.xlabel("Grandeur en abscisse")
plt.ylabel("Grandeur en ordonnée")
plt.title("Titre de mon graphique")
plt.grid()
plt.legend()
plt.show()
```
Ce qui donne : 
![fig3](https://hackmd.io/_uploads/ByaVwNOA0.png)

Jolie n'est-ce pas?