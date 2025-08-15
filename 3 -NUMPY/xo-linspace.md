---
title : Exercices - linspace
order : 480
icon : pencil
---
Je vais régler ça en te fournissant directement le contenu du fichier ici. Tu pourras alors le copier et l'enregistrer dans un fichier `.md` sur ton ordinateur.

---

## Exercices sur la fonction `linspace`

### Exercice 1 : Série linéaire de 0 à 1
+++ Enoncé
Utilise `linspace` pour créer un tableau de 5 nombres régulièrement espacés entre 0 et 1 (inclus).
+++ Code
```python
import numpy as np
tableau = np.linspace(0, 1, 5)
print(tableau)
```
+++ sortie
```
[0.   0.25 0.5  0.75 1.  ]
```
+++

---

### Exercice 2 : Série linéaire de 1 à 10
+++ Enoncé
Utilise `linspace` pour créer un tableau de 10 nombres régulièrement espacés entre 1 et 10 (inclus).
+++ Code
```python
import numpy as np
tableau = np.linspace(1, 10, 10)
print(tableau)
```
+++ sortie
```
[ 1.  2.  3.  4.  5.  6.  7.  8.  9. 10.]
```
+++

---

### Exercice 3 : Série linéaire de 0 à 100
+++ Enoncé
Utilise `linspace` pour créer un tableau de 6 nombres régulièrement espacés entre 0 et 100 (inclus).
+++ Code
```python
import numpy as np
tableau = np.linspace(0, 100, 6)
print(tableau)
```
+++ sortie
```
[  0.  20.  40.  60.  80. 100.]
```
+++

---

### Exercice 4 : Série linéaire de -5 à 5
+++ Enoncé
Utilise `linspace` pour créer un tableau de 11 nombres régulièrement espacés entre -5 et 5 (inclus).
+++ Code
```python
import numpy as np
tableau = np.linspace(-5, 5, 11)
print(tableau)
```
+++ sortie
```
[-5. -4. -3. -2. -1.  0.  1.  2.  3.  4.  5.]
```
+++

---

### Exercice 5 : Série linéaire de 0 à π
+++ Enoncé
Utilise `linspace` pour créer un tableau de 5 nombres régulièrement espacés entre 0 et π (inclus). Utilise `np.pi` pour π.
+++ Code
```python
import numpy as np
tableau = np.linspace(0, np.pi, 5)
print(tableau)
```
+++ sortie
```
[0.         0.78539816 1.57079633 2.35619449 3.14159265]
```
+++

---

### Exercice 6 : Série linéaire de 10 à 0
+++ Enoncé
Utilise `linspace` pour créer un tableau de 6 nombres régulièrement espacés entre 10 et 0 (inclus).
+++ Code
```python
import numpy as np
tableau = np.linspace(10, 0, 6)
print(tableau)
```
+++ sortie
```
[10.  8.  6.  4.  2.  0.]
```
+++

---

### Exercice 7 : Série linéaire de 0 à 2π
+++ Enoncé
Utilise `linspace` pour créer un tableau de 9 nombres régulièrement espacés entre 0 et 2π (inclus).
+++ Code
```python
import numpy as np
tableau = np.linspace(0, 2*np.pi, 9)
print(tableau)
```
+++ sortie
```
[0.         0.78539816 1.57079633 2.35619449 3.14159265 3.92699082
 4.71238898 5.49778714 6.28318531]
```
+++

---

### Exercice 8 : Série linéaire de 0.1 à 1
+++ Enoncé
Utilise `linspace` pour créer un tableau de 20 nombres régulièrement espacés entre 0.1 et 1 (inclus).
+++ Code
```python
import numpy as np
tableau = np.linspace(0.1, 1, 20)
print(tableau)
```
+++ sortie
```
[0.1         0.14736842 0.19473684 0.24210526 0.28947368 0.33684211
 0.38421053 0.43157895 0.47894737 0.52631579 0.57368421 0.62105263
 0.66842105 0.71578947 0.76315789 0.81052632 0.85789474 0.90526316
 0.95263158 1.        ]
```
+++

---

### Exercice 9 : Série linéaire de -π à π
+++ Enoncé
Utilise `linspace` pour créer un tableau de 13 nombres régulièrement espacés entre -π et π (inclus).
+++ Code
```python
import numpy as np
tableau = np.linspace(-np.pi, np.pi, 13)
print(tableau)
```
+++ sortie
```
[-3.14159265 -2.44346095 -1.74532925 -1.04719755 -0.34906585  0.34906585
  1.04719755  1.74532925  2.44346095  3.14159265]
```
+++

---

### Exercice 10 : Série linéaire de 0 à 1000
+++ Enoncé
Utilise `linspace` pour créer un tableau de 21 nombres régulièrement espacés entre 0 et 1000 (inclus).
+++ Code
```python
import numpy as np
tableau = np.linspace(0, 1000, 21)
print(tableau)
```
+++ sortie
```
[  0.  50. 100. 150. 200. 250. 300. 350. 400. 450. 500. 550. 600. 650.
 700. 750. 800. 850. 900. 950.1000.]
```
+++

---

### Exercice 11 : Série linéaire de 0 à 1 (sans inclure 1)
+++ Enoncé
Utilise `linspace` pour créer un tableau de 5 nombres régulièrement espacés entre 0 et 1, **sans inclure 1**. Utilise l'argument `endpoint=False`.
+++ Code
```python
import numpy as np
tableau = np.linspace(0, 1, 5, endpoint=False)
print(tableau)
```
+++ sortie
```
[0.  0.2 0.4 0.6 0.8]
```
+++

---

### Exercice 12 : Série linéaire de 1 à 100 (sans inclure 100)
+++ Enoncé
Utilise `linspace` pour créer un tableau de 10 nombres régulièrement espacés entre 1 et 100, **sans inclure 100**.
+++ Code
```python
import numpy as np
tableau = np.linspace(1, 100, 10, endpoint=False)
print(tableau)
```
+++ sortie
```
[ 1. 12. 23. 34. 45. 56. 67. 78. 89.]
```
+++

---
