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
+++

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

+++
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

+++
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

+++
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

+++
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

+++
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

+++
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

+++
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

+++
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

+++
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

***

# Feuille d’exercices : Premiers graphiques avec Matplotlib

***

### Exercice 1

+++ Enoncé
Trace la courbe de la fonction \$ y = 2x \$ pour \$ x \$ allant de -10 à 10.

+++ code
```python
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(-10, 10, 100)
y = 2*x

plt.plot(x, y)
plt.show()
```
+++ sortie
![exercice_1](https://hackmd.io/_uploads/S1Wz3wiqeg.png)
+++ Remarquess
Premier contact avec `plot()`, qui trace une courbe à partir de deux séries de valeurs.
+++


***

### Exercice 2

+++ Enoncé
Reprends le graphique précédent et ajoute un titre, ainsi que des noms aux axes.

+++ code
```python
plt.plot(x, y)
plt.title("Graphique de y = 2x")
plt.xlabel("x")
plt.ylabel("y")
plt.show()
```
+++ sortie
![exercice_2](https://hackmd.io/_uploads/BJPmhvi9xl.png)
+++ remarques
On introduit ici les fonctions `title()`, `xlabel()` et `ylabel()`.
+++


***

### Exercice 3

+++ Enoncé
Trace la courbe \$ y = x^2 \$ pour \$ x \$ entre -10 et 10, en rouge pointillé et épaisseur 2.

+++ Code
```python
x = np.linspace(-10, 10, 200)
y = x**2

plt.plot(x, y, "r--", linewidth=2)
plt.show()
```

+++sortie
![exercice_3](https://hackmd.io/_uploads/BJED3wsqeg.png)

+++ Remarques
On introduit le choix du style avec `"r--"` (rouge, ligne pointillée).

+++


***

### Exercice 4

+++ Enoncé
Sur un même graphique, trace \$ y = x \$, \$ y = x^2 \$, et \$ y = x^3 \$, avec légende.

+++ Code
```python
x = np.linspace(-10, 10, 200)
plt.plot(x, x, label="y=x")
plt.plot(x, x**2, label="y=x²")
plt.plot(x, x**3, label="y=x³")
plt.legend()
plt.show()
```

+++sortie
![exercice_4](https://hackmd.io/_uploads/r1hR3wo9el.png)

+++ Remarquess
Une même figure peut afficher plusieurs fonctions, et `legend()` automatise l’affichage des noms.

+++


***

### Exercice 5

+++ Enoncé
Trace \$ y = \sin(x) \$ avec des marqueurs au lieu d’une ligne continue.

+++ Code
```python
x = np.linspace(0, 2*np.pi, 20)
y = np.sin(x)

plt.plot(x, y, "o")
plt.show()
```

+++sortie
![exercice_5](https://hackmd.io/_uploads/SyNZpDs9le.png)

+++ Remarquess
L’option `"o"` permet de remplacer la ligne par des cercles aux positions données.

+++


***

### Exercice 6

+++ Enoncé
Trace \$ y = \cos(x) \$ entre -10 et 10, avec des limites d’axes fixées.

+++ Code
```python
x = np.linspace(-10, 10, 400)
y = np.cos(x)

plt.plot(x, y)
plt.xlim(-2*np.pi, 2*np.pi)
plt.ylim(-1.5, 1.5)
plt.show()
```

+++sortie
![exercice_6](https://hackmd.io/_uploads/r1jMTwocee.png)

+++ Remarquess
Avec `xlim()` et `ylim()`, on définit précisément la zone affichée.

+++


***

### Exercice 7

+++ Enoncé
Trace \$ y = e^x \$ pour \$ x \$ entre -2 et 2. Ajoute une grille.

+++ Code
```python
x = np.linspace(-2, 2, 200)
y = np.exp(x)

plt.plot(x, y)
plt.grid(True)
plt.show()
```

+++sortie
![exercice_7](https://hackmd.io/_uploads/Hks76Diqee.png)

+++ Remarquess
L’option `grid(True)` rend la lecture plus précise.

+++


***

### Exercice 8

+++ Enoncé
Crée une figure avec **deux sous-graphes** côte à côte : $\sin(x)$ et $\cos(x)$.

+++ Code
```python
x = np.linspace(0, 2*np.pi, 200)

plt.subplot(1,2,1)
plt.plot(x, np.sin(x))
plt.title("sin(x)")

plt.subplot(1,2,2)
plt.plot(x, np.cos(x))
plt.title("cos(x)")

plt.show()
```

+++sortie
![exercice_8](https://hackmd.io/_uploads/rkuNTDo5xe.png)

+++ Remarquess
Avec `subplot(lignes, colonnes, position)`, on affiche plusieurs figures dans une seule fenêtre.

+++


***

### Exercice 9

+++ Enoncé
Génère 100 valeurs aléatoires suivant une loi normale et trace l’histogramme.

+++ Code
```python
data = np.random.normal(0, 1, 100)

plt.hist(data, bins=20)
plt.show()
```

+++sortie
![exercice_9](https://hackmd.io/_uploads/SyVPpDoqlg.png)

+++ Remarquess
`hist()` permet de visualiser la répartition de données expérimentales ou aléatoires.

+++


***

### Exercice 10

+++ Enoncé
Crée une figure avec deux sous-graphes :

  - en haut la courbe \$ y = \sin(x) \$,
  - en bas un histogramme de 200 valeurs aléatoires uniformes entre 0 et 10.

+++ Code
```python
x = np.linspace(0, 2*np.pi, 200)
y = np.sin(x)
data = np.random.uniform(0, 10, 200)

plt.subplot(2,1,1)
plt.plot(x, y)
plt.title("sin(x)")

plt.subplot(2,1,2)
plt.hist(data, bins=20)
plt.title("Histogramme [0,10]")

plt.tight_layout()
plt.show()
```

+++sortie
![exercice_10](https://ppl-ai-code-interpreter-files.s3.amazonaws.com/web/direct-files/f8fe95b8b4478bd4066d2efa8cb04187/05ddc7ef-dae1-4d8f-ad7d-066a7178e983/5e329622.png)

+++ Remarquess
On combine deux types de graphes (courbes et histogrammes) et `tight_layout()` ajuste les espaces.

+++


***

Tu peux maintenant télécharger les fichiers image et copier ce texte dans un fichier Markdown.
Pour obtenir le fichier Markdown complet avec les liens d’images prêts à l’emploi, télécharge toutes les images (exercice_1.png à exercice_10.png) et place-les dans le même dossier que ton fichier .md.
Veux-tu que je regroupe directement ces fichiers pour téléchargement ?
<span style="display:none">[^1][^2][^3][^4][^5][^6][^7]</span>

<div style="text-align: center">⁂</div>

[^1]: https://ppl-ai-code-interpreter-files.s3.amazonaws.com/web/direct-files/f8fe95b8b4478bd4066d2efa8cb04187/d5ef153c-e59b-4872-9d1f-97d2e16c7012/894572af.png

[^2]: https://ppl-ai-code-interpreter-files.s3.amazonaws.com/web/direct-files/f8fe95b8b4478bd4066d2efa8cb04187/d5ef153c-e59b-4872-9d1f-97d2e16c7012/222af4bc.png

[^3]: https://ppl-ai-code-interpreter-files.s3.amazonaws.com/web/direct-files/f8fe95b8b4478bd4066d2efa8cb04187/d5ef153c-e59b-4872-9d1f-97d2e16c7012/ea4f3ded.png

[^4]: https://ppl-ai-code-interpreter-files.s3.amazonaws.com/web/direct-files/f8fe95b8b4478bd4066d2efa8cb04187/30598b08-136e-4dbc-bfee-4633652fd73a/45634041.png

[^5]: https://ppl-ai-code-interpreter-files.s3.amazonaws.com/web/direct-files/f8fe95b8b4478bd4066d2efa8cb04187/30598b08-136e-4dbc-bfee-4633652fd73a/f71606a4.png

[^6]: https://ppl-ai-code-interpreter-files.s3.amazonaws.com/web/direct-files/f8fe95b8b4478bd4066d2efa8cb04187/30598b08-136e-4dbc-bfee-4633652fd73a/120c01c1.png

[^7]: 

