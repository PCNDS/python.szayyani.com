---
Title : La fonction `linalg.solve`
order : 700
---

Celle-là est un de nos grands amis, car `linalg.solve` nous permet de résoudres des équations algébrique, mais surtout des systèmes d'équations. 

C'est donc un outil puissant pour nous en physique car nos problèmes se réduisent très souvent en un système d'équation à résoudre (et ce même dans des domains de physique bien plus avance tel que la mécanique quantique). 

De manière général `linalg.solve` nous permet de résoudre des équation du type : $A\cdot X = b$ où on connait $A$ et $b$. 

Voici un exemple très basique : $ 4\cdot x = 8 $

Ici $A \to 4$, $X \to x$ et $b \to 8$. C'est l'exemple le plus simple et basique que l'on peut donner. Utile, mais pas *très* intéressant. Voici comment trouver la solution avec `linalg.solve` : 

+++ code
```python
import numpy as np 

# définissons nos données 
A = np.array([[4]])
b = np.array([8])

#passons à la résolution 
X = np.linalg.solve(A,b)

print(X) #pour afficher le résultat    
```
+++ sortie
```python
>>> 2
```
+++

!!!danger Attention : 
* `linalg.solve` prend comme argument des `array` et donc il faut toujours définir ses variable et données par la fonction `array`
* `linalg.solve` est *conçu* pour résoudre des *systèmes d'équations* et donc va toujours supposer que le $A$ est une matrice au moins en 2 dimensions, d'où `A = np.array([[4]])` et non `A = np.array([4])`, tandis que `b = np.array([8])`. 
!!!

La vraie puissance de cette fonction est dans ça capacité à résoudre des systèmes d'équation, telle que vous l'avez appris en fin du collège. 

Prenons un exemple simple: deux équations linéaires avec deux variables inconcue $x$ et $y$: 

$$ 4x + 3y = 10 \\ $$ 
$$ 3x + 2y = 6 $$

On peut réécrire ce système sous forme $A\cdot X = b$ : 
$$
\begin{bmatrix}4 & 3\\\ 3 & 2\end{bmatrix} \cdot \begin{bmatrix} x \\\ y \end{bmatrix} = \begin{bmatrix} 10 \\\ 6 \end{bmatrix}
$$

où $A = \begin{bmatrix}4 & 3\\\ 3 & 2\end{bmatrix}$ et $b= \begin{bmatrix} 10 \\\ 6 \end{bmatrix}$. Le matrice $\begin{bmatrix} x \\\ y \end{bmatrix}$ correspond donc à la *solution* que `linalg.solve` doit nous trouver. 

+++ Code
```python
import numpy as np 

# définissons nos données 
A = np.array([[4, 3], [3, 2]])
b = np.array([10, 6])

#passons à la résolution 
X = np.linalg.solve(A,b)

print(X) # pour afficher de manière la plus simple l'array avec x et y 
print("x = ", X[0], "et y = ", X[1]) #pour afficher le résultat de manière plus claire 
```
+++ Sortie
```python
>>> [-2.0 , 6.0] #l'array avec les deux valeur calculée pour x et y 
>>> x =  -2.0 et y =  6.0 
```
+++

Quel intérêt pour nous en physique de pouvoir faire ça? Eh bah figurez vous que ça nous arrive très souvent à avoir beson de résoudre un système d'équatin pour trouver la solution à un problème. Un exemple très simple est trouver l'intersection entre deux droites, ou encore le point d'intersection de trois plans. 

Imaginons donc un système de trois équations avec trois variables $x, y, z$ qui représentent trois plans : 

$$ x + y + z = 2 \\ $$
$$ x + 2y - 3z = 0 \\ $$ 
$$ 5x - 3y + z = -1 $$

Pour rappel, la solution serait un point dans l'espace tridimensionnel ayant des coordonnées $(x, y, z)$. Comme avant nous allons suivre les étapes suivantes : 
1. transformer le système en une équation du type $A\cdot X = b$ ou $A$ serait une matrice $3\times 3$, et $b$ est une matrice $3\times 1$. 
2. Définir les `arrays`avec les valeurs des matrices 
3. Utiliser `np.linalg.solve` pour trouver la solution. 

+++ Code
```python
import numpy as np 

# définissons nos données 
A = np.array([[1,1,1], [1,2,-3], [5,-3,1]])
b = np.array([2,0,-1])

#passons à la résolution 
X = np.linalg.solve(A,b)

print(X) # pour afficher de manière la plus simple l'array avec x et y 
print("x = ", X[0], "et y = ", X[1], "et z =", X[2]) #pour afficher le résultat de manière plus claire 
```
+++ Sortie
```python
>>> [0.25 1.   0.75] #l'array avec les deux valeur calculée pour x et y 
>>> x = 0.25 et y =  1.0 et z = 0.75 
```
+++

Vous allez pouvoir vraiment voir la puissance de cette fonction dans la partie exercices avec des applications à toute sorte de problèmes physique et chimiques. 