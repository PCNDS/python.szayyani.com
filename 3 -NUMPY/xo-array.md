---
title : Exercices - Array
order : 500
icon : pencil
---

## Exercices sur la fonction `array`

### Exercice 1 : Création d'un tableau simple
+++ Enoncé
Crée un tableau contenant les nombres 1, 2, 3, 4, 5 en utilisant la fonction `array` du module `numpy`.
+++ Code
```python
import numpy as np
tableau = np.array([1, 2, 3, 4, 5])
print(tableau)
```
+++

---

### Exercice 2 : Tableau de nombres flottants
+++ Enoncé
Crée un tableau contenant les nombres flottants 1.5, 2.5, 3.5, 4.5 en utilisant `array`.
+++ Code
```python
import numpy as np
tableau = np.array([1.5, 2.5, 3.5, 4.5])
print(tableau)
```
+++

---

### Exercice 3 : Tableau à deux dimensions
+++ Enoncé
Crée un tableau à deux dimensions (matrice) contenant les lignes [1, 2, 3] et [4, 5, 6] en utilisant `array`.
+++ Code
```python
import numpy as np
tableau = np.array([[1, 2, 3], [4, 5, 6]])
print(tableau)
```
+++

---

### Exercice 4 : Tableau de chaînes de caractères
+++ Enoncé
Crée un tableau contenant les chaînes de caractères "bonjour", "le", "monde" en utilisant `array`.
+++ Code
```python
import numpy as np
tableau = np.array(["bonjour", "le", "monde"])
print(tableau)
```
+++

---

### Exercice 5 : Tableau avec des zéros
+++ Enoncé
Crée un tableau de 5 zéros en utilisant `array` et `zeros` de `numpy`.
+++ Code
```python
import numpy as np
tableau = np.zeros(5)
print(tableau)
```
+++
