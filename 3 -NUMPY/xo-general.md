---
Title : Exercices - encore plus ! 
order : 450
icon : pencil 
---
## Exercices Généraux pour aller plus loin 

### Ex. 1 
+++ Enoncé
Créez un vecteur de 5 valeurs également espacées entre $0$ et $10$.
+++ code
```python
import numpy as np
x = np.linspace(0, 10, 5)
print(x)
```
+++ sortie
```
[ 0.   2.5  5.   7.5 10. ]
```
+++
---
### Ex. 2
+++ Enoncé
Créez un vecteur allant de $0$ à $5$ (exclu) avec un pas de $0,5$.
+++ code
```python
import numpy as np
x = np.arange(0, 5, 0.5)
print(x)
```
+++ sortie
```
[0.  0.5 1.  1.5 2.  2.5 3.  3.5 4.  4.5]
```
+++
---
### Ex. 3
+++ Enoncé
Créez un tableau NumPy à partir de la liste `[1, 2, 3, 4, 5]`.
+++ code
```python
import numpy as np
x = np.array([1, 2, 3, 4, 5])
print(x)
```
+++ sortie
```
[1 2 3 4 5]
```
+++
---
### Ex. 4
+++ Enoncé
Créez un vecteur de 5 valeurs de 1 à 5, puis calculez leur carré.
+++ code
```python
import numpy as np
x = np.linspace(1, 5, 5)
y = x**2
print(y)
```
+++ sortie
```
[ 1.  4.  9. 16. 25.]
```
+++
---
### Ex. 5
+++ Enoncé
Créez un tableau $3\times 3$ contenant les entiers de $1$ à $9$.
+++ code
```python
import numpy as np
x = np.arange(1, 10).reshape(3, 3)
print(x)
```
+++ sortie
```
[[1 2 3]
 [4 5 6]
 [7 8 9]]
```
+++
---
### Ex. 6
+++ Enoncé
Créez un tableau de $1$ à $5$ puis calculez la somme de ses éléments.
+++ code
```python
import numpy as np
x = np.arange(1, 6)
s = np.sum(x)
print(s)
```
+++ sortie
```
15
```
+++
---
### Ex. 7
+++ Enoncé
Calculez le produit matriciel de `A=[[1,2],[3,4]]` et `B=[[5,6],[7,8]]`.
+++ code
```python
import numpy as np
A = np.array([[1, 2], [3, 4]])
B = np.array([[5, 6], [7, 8]])
C = A @ B
print(C)
```
+++ sortie
```
[[19 22]
 [43 50]]
```
+++
---
### Ex. 8
+++ Enoncé
Résolvez le système linéaire $2x + y = 8$ et $x + 3y = 13$.
+++ code
```python
import numpy as np
A = np.array([[2, 1], [1, 3]])
b = np.array([8, 13])
sol = np.linalg.solve(A, b)
print(sol)
```
+++ sortie
```
[2.2 3.6]
```
+++
---
### Ex. 9
+++ Enoncé
Créez une matrice $3\times 3$ de $1$ à $9$, soustrayez la matrice identité $3\times 3$.
+++ code
```python
import numpy as np
I = np.eye(3)
M = np.arange(1, 10).reshape(3, 3)
R = M - I
print(R)
```
+++ sortie
```
[[0. 2. 3.]
 [4. 4. 6.]
 [7. 8. 8.]]
```
+++
---
### Ex. 10
+++ Enoncé
Résolvez le système :
$$ 
3x + 2y - z = 1 \\
2x - 2y + 4z = -2 \\
-x + 0.5y - z = 0 
$$
+++ code
```python
import numpy as np
A = np.array([[3, 2, -1], [2, -2, 4], [-1, 0.5, -1]])
b = np.array([1, -2, 0])
sol = np.linalg.solve(A, b)
print(sol)
```
+++ sortie
```
[ 1. -2. -2.]
```
+++

