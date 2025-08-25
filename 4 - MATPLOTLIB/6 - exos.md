---
title : Exercice d'application 
order : 900
icon : pencil
---

Evidemment vous auriez importé la biblie avant tout : `import matplotlib.pyplot as plt`. 

## Ex.1 - les bases 

+++ Enoncé
Produire un graphique de nuages de points à partir des listes suivenantes : `A = [-2, 2, 5, 10, 3.3]` et `B = [0, 2, 5, 9, 15]`. 
+++ code 
```python 

```
+++ sortie 

+++ commentaire


## Exercice 1 : Tracer une ligne simple
+++ Enoncé  
Trace la courbe reliant les points donnés dans la liste `y = [1, 3, 2, 4]`. L’axe des abscisses sera automatiquement créé par matplotlib.  

+++ Code  
```python
import matplotlib.pyplot as plt

y = [1, 3, 2, 4]
plt.plot(y)
plt.show()
```

+++ Sortie  
Une ligne brisée passant par les points (0,1), (1,3), (2,2), (3,4).  

+++ Commentaires  
Si on ne donne qu’une liste, matplotlib utilise automatiquement l’index (0,1,2,…) comme axe des abscisses.  

---

## Exercice 2 : Tracer deux courbes sur le même graphique
+++ Enoncé  
Trace les courbes des deux listes : `y1 = [1, 2, 3, 4]` et `y2 = [4, 3, 2, 1]` sur le même graphique.  

+++ Code  
```python
import matplotlib.pyplot as plt

y1 = [1, 2, 3, 4]
y2 = [4, 3, 2, 1]

plt.plot(y1)
plt.plot(y2)
plt.show()
```

+++ Sortie  
Deux courbes apparaissent : l’une croissante et l’autre décroissante.  

+++ Commentaires  
Plusieurs appels à `plt.plot()` permettent d’afficher plusieurs courbes sur le même graphique.  

---

## Exercice 3 : Ajouter un titre et des labels
+++ Enoncé  
Trace la courbe `y = [2, 4, 6, 8]` et ajoute un titre au graphique, ainsi que des labels aux axes.  

+++ Code  
```python
import matplotlib.pyplot as plt

y = [2, 4, 6, 8]

plt.plot(y)
plt.title("Courbe simple")
plt.xlabel("Indice")
plt.ylabel("Valeur")
plt.show()
```

+++ Sortie  
Un graphique avec un titre "Courbe simple", l’axe des abscisses nommé "Indice" et l’axe des ordonnées "Valeur".  

+++ Commentaires  
Les fonctions `plt.title()`, `plt.xlabel()` et `plt.ylabel()` permettent d’ajouter des annotations au graphique.  

---

## Exercice 4 : Tracer une fonction mathématique
+++ Enoncé  
Trace la fonction `y = x²` pour `x` allant de -5 à 5.  

+++ Code  
```python
import matplotlib.pyplot as plt

x = list(range(-5, 6))
y = [i**2 for i in x]

plt.plot(x, y)
plt.title("y = x²")
plt.show()
```

+++ Sortie  
Une parabole symétrique centrée en 0.  

+++ Commentaires  
On peut calculer les valeurs d’une fonction mathématique avec une boucle ou une liste en compréhension.  

---

## Exercice 5 : Modifier l’apparence d’une courbe
+++ Enoncé  
Trace la fonction `y = x³` avec une couleur rouge et des pointillés.  

+++ Code  
```python
import matplotlib.pyplot as plt

x = list(range(-5, 6))
y = [i**3 for i in x]

plt.plot(x, y, 'r--')  # r = rouge, -- = pointillés
plt.title("y = x³")
plt.show()
```

+++ Sortie  
Une courbe cubique rouge en pointillés.  

+++ Commentaires  
Les arguments de style dans `plt.plot()` permettent de changer couleur, forme des points et type de ligne.  

---

## Exercice 6 : Ajouter une légende
+++ Enoncé  
Trace `y = x` et `y = x²` sur le même graphique et ajoute une légende.  

+++ Code  
```python
import matplotlib.pyplot as plt

x = list(range(-5, 6))
y1 = [i for i in x]
y2 = [i**2 for i in x]

plt.plot(x, y1, label="y = x")
plt.plot(x, y2, label="y = x²")
plt.legend()
plt.show()
```

+++ Sortie  
Deux courbes avec une légende en haut à droite.  

+++ Commentaires  
`plt.legend()` affiche la légende basée sur les labels fournis dans `plt.plot()`.  

---

## Exercice 7 : Tracer un nuage de points (scatter plot)
+++ Enoncé  
Trace un nuage de points avec `x = [1,2,3,4,5]` et `y = [5,4,3,2,1]`.  

+++ Code  
```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [5, 4, 3, 2, 1]

plt.scatter(x, y, color='green')
plt.title("Nuage de points")
plt.show()
```

+++ Sortie  
Un nuage de points verts en diagonale décroissante.  

+++ Commentaires  
`plt.scatter()` permet de faire des graphiques de dispersion au lieu de courbes continues.  

---

## Exercice 8 : Tracer un histogramme
+++ Enoncé  
Trace l’histogramme des valeurs contenues dans la liste `data = [1,1,2,2,2,3,3,4,5,5,5,5]`.  

+++ Code  
```python
import matplotlib.pyplot as plt

data = [1,1,2,2,2,3,3,4,5,5,5,5]

plt.hist(data, bins=5, color='orange', edgecolor='black')
plt.title("Histogramme")
plt.show()
```

+++ Sortie  
Un histogramme montrant la fréquence d’apparition de chaque valeur.  

+++ Commentaires  
Un histogramme est utile pour visualiser la répartition d’un jeu de données.  

---

## Exercice 9 : Tracer plusieurs sous-graphiques
+++ Enoncé  
Affiche `y = x` et `y = x²` dans deux graphiques séparés (un au-dessus de l’autre).  

+++ Code  
```python
import matplotlib.pyplot as plt

x = list(range(-5, 6))
y1 = [i for i in x]
y2 = [i**2 for i in x]

plt.subplot(2,1,1)
plt.plot(x, y1)
plt.title("y = x")

plt.subplot(2,1,2)
plt.plot(x, y2)
plt.title("y = x²")

plt.tight_layout()
plt.show()
```

+++ Sortie  
Deux graphiques superposés : une droite et une parabole.  

+++ Commentaires  
`plt.subplot(n,m,i)` divise la fenêtre en `n × m` graphiques et affiche le i-ème.  

---

## Exercice 10 : Tracer une courbe avec style avancé
+++ Enoncé  
Trace `y = sin(x)` pour `x` allant de 0 à 2π avec une courbe bleue, des points en cercle, une grille et une légende.  

+++ Code  
```python
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 2*np.pi, 50)
y = np.sin(x)

plt.plot(x, y, 'bo-', label="sin(x)")  # b = bleu, o = cercles, - = ligne continue
plt.title("y = sin(x)")
plt.xlabel("x (radians)")
plt.ylabel("sin(x)")
plt.legend()
plt.grid(True)
plt.show()
```

+++ Sortie  
Une sinusoïde bleue avec des cercles sur chaque point, une grille et une légende.  

+++ Commentaires  
Cet exercice combine plusieurs notions : styles, légende, grille, et utilisation de `numpy` pour générer des points.  

