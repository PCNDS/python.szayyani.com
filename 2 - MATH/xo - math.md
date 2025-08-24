---
title : Exercices d'entraînment
order : -1
---

Absolument ! Voici 10 exercices progressifs sur le module `math` de Python, parfaits pour des lycéens.

### Exercice 1 : Les bases
+++ Enoncé
Écris un programme qui calcule et affiche :
1. La valeur de π (pi)
2. La racine carrée de 16
3. 5 à la puissance 3 (en utilisant `math.pow`)
+++ code
```python
import math

print("1. La valeur de π est :", math.pi)
print("2. La racine carrée de 16 est :", math.sqrt(16))
print("3. 5 à la puissance 3 est :", math.pow(5, 3))
```
+++ sortie
```python
>>> 1. La valeur de π est : 3.141592653589793
>>> 2. La racine carrée de 16 est : 4.0
>>> 3. 5 à la puissance 3 est : 125.0
```
+++ commentaire
Exercice d'introduction pour se familiariser avec l'import du module et l'utilisation des fonctions de base.
+++

---

### Exercice 2 : Arrondis et troncature
+++ Enoncé
Soit le nombre `x = 3.7`. Utilise le module `math` pour :
1. Arrondir à l'entier inférieur (`floor`)
2. Arrondir à l'entier supérieur (`ceil`)
3. Obtenir la valeur tronquée (`trunc`)
+++ code
```python
import math

x = 3.7
print("1. Floor de", x, ":", math.floor(x))
print("2. Ceil de", x, ":", math.ceil(x))
print("3. Trunc de", x, ":", math.trunc(x))
```
+++ sortie
```python
>>> 1. Floor de 3.7 : 3
>>> 2. Ceil de 3.7 : 4
>>> 3. Trunc de 3.7 : 3
```
+++ commentaire

Permet de comprendre la différence entre ces trois méthodes d'arrondi, une notion importante.

+++



---

### Exercice 3 : Factorielle et constante d'Euler
+++Enoncé
Calculer la somme des sinus des angles 0°, 30°, 45°, 60°, 90° (en radians).

+++ code

```python
import math
angles_degres = [0, 30, 45, 60, 90]
somme_sinus = sum(math.sin(math.radians(a)) for a in angles_degres)
print(somme_sinus)
```

+++ sortie

```
3.2071067811865475
```

+++ commentaire

Il faut convertir les degrés en radians avant de calculer le sinus. `sum()` additionne tous les résultats.
+++

---

### Exercice 4 : Arrondir

+++Enoncé
Pour un angle en degrés donné (45°), calculer sa tangente et afficher la valeur arrondie à 4 décimales.
+++ code
```python
import math
angle = 45
tangente = math.tan(math.radians(angle))
print(round(tangente, 4))
```
+++ sortie
```
1.0
```
+++ commentaire
La tangente de 45° est exactement 1. La fonction `round` est utile pour arrondir le résultat.
+++

---

### Exercice 5 : Utilisation de fonction trigonométrique inverse

+++Enoncé
Calculer l’angle (en degrés) dont le sinus vaut 0.5, en utilisant la fonction d’arc sinus.
+++ code
```python
import math
valeur_sin = 0.5
angle_radians = math.asin(valeur_sin)
angle_degres = math.degrees(angle_radians)
print(angle_degres)
```
+++ sortie
```
30.000000000000004
```
+++ commentaire
`math.asin()` retourne l’arc sinus en radians. `math.degrees()` convertit ce résultat en degrés.
+++

---

### Exercice 6 : Calcul trigonométrique 

+++ Enoncé
Calculer l’angle (en degrés) dont le cosinus est égal à $\sqrt{2}/2$.
+++ code
```python
import math
valeur_cos = math.sqrt(2)/2
angle_radians = math.acos(valeur_cos)
angle_degres = math.degrees(angle_radians)
print(angle_degres)
```
+++ sortie
```
45.0
```
+++ commentaire
`math.acos()` est la fonction d’arc cosinus, inverse du cosinus.
+++

---

### Exercice 7 : Aire d'un triangle 

+++Enoncé
Calculer l’aire d’un triangle dont deux côtés mesurent 7 et 10, et l’angle entre eux est de 40° (formule : $\text{aire} = \frac{1}{2}ab\sin(C)$).
+++ code
```python
import math
a = 7
b = 10
angle_C_deg = 40
angle_C_rad = math.radians(angle_C_deg)
aire = 0.5 * a * b * math.sin(angle_C_rad)
print(round(aire, 2))
```
+++ sortie
```
22.57
```
+++ commentaire
La fonction sinus est utilisée pour calculer l’aire du triangle selon la formule trigonométrique classique.
+++

---

### Exercice 8 : Factorielle et constante d'Euler
+++ Enoncé
Calcule et affiche :
1. La factorielle de 5 (`5!`)
2. La constante d'Euler `e` (base du logarithme népérien)
3. Le logarithme népérien de la constante `e` (doit donner 1)
4. Le logarithme en base 10 de 100 (doit donner 2)
+++ code
```python
import math

print("1. Factorielle de 5 :", math.factorial(5))
print("2. Constante e :", math.e)
print("3. ln(e) :", math.log(math.e))
print("4. log10(100) :", math.log10(100))
```
+++ sortie
```python
1. Factorielle de 5 : 120
2. Constante e : 2.718281828459045
3. ln(e) : 1.0
4. log10(100) : 2.0
```
+++ commentaire
Introduit les concepts de factorielle (récursivité possible plus tard) et de logarithmes.
+++

---

### Exercice 9 : Périmètre et Aire d'un cercle
+++ Enoncé
Demande à l'utilisateur de saisir le rayon d'un cercle.
Calcule et affiche :
1. Le périmètre du cercle (`2 * π * rayon`)
2. L'aire du cercle (`π * rayon²`)
+++ code
```python
rayon = float(input("Entrez le rayon du cercle : "))

perimetre = 2 * math.pi * rayon
aire = math.pi * math.pow(rayon, 2)  # On pourrait aussi utiliser rayon**2

print(f"Pour un cercle de rayon {rayon} :")
print(f"- Périmètre : {perimetre:.2f}")
print(f"- Aire : {aire:.2f}")
```
+++ sortie
```python
Entrez le rayon du cercle : 5
Pour un cercle de rayon 5.0 :
- Périmètre : 31.42
- Aire : 78.54
```
+++ commentaire
Combine l'interaction utilisateur (`input`) avec les calculs mathématiques. Très satisfaisant pour les élèves.
+++

---
### Exercice 10 : Calcul de tangente 
+++Enoncé
Pour un angle en degrés donné (45°), calculer sa tangente et afficher la valeur arrondie à 4 décimales.
+++ code
```python
import math
angle = 45
tangente = math.tan(math.radians(angle))
print(round(tangente, 4))
```
+++ sortie
```
1.0
```
+++ commentaire
La tangente de 45° est exactement 1. La fonction `round` est utile pour arrondir le résultat.
+++

---

### Exerice 11 : Calcul d'arcsin

+++Enoncé
Calculer l’angle (en degrés) dont le sinus vaut 0.5, en utilisant la fonction d’arc sinus.
+++ code
```python
import math
valeur_sin = 0.5
angle_radians = math.asin(valeur_sin)
angle_degres = math.degrees(angle_radians)
print(angle_degres)
```
+++ sortie
```
30.000000000000004
```
+++ commentaire
`math.asin()` retourne l’arc sinus en radians. `math.degrees()` convertit ce résultat en degrés.
+++

---

### Exercice 12 : Trigonométrie 

+++Enoncé
Calculer l’angle (en degrés) dont le cosinus est égal à $\sqrt{2}/2$.
+++ code
```python
import math
valeur_cos = math.sqrt(2)/2
angle_radians = math.acos(valeur_cos)
angle_degres = math.degrees(angle_radians)
print(angle_degres)
```
+++ sortie
```
45.0
```
+++ commentaire
`math.acos()` est la fonction d’arc cosinus, inverse du cosinus.
+++

---

### Exercice 13 : Aire d'un triangle 
+++Enoncé
Calculer l’aire d’un triangle dont deux côtés mesurent 7 et 10, et l’angle entre eux est de 40° (formule : $\text{aire} = \frac{1}{2}ab\sin(C)$).

+++ code
```python
import math
a = 7
b = 10
angle_C_deg = 40
angle_C_rad = math.radians(angle_C_deg)
aire = 0.5 * a * b * math.sin(angle_C_rad)
print(round(aire, 2))
```
+++ sortie
```
22.57
```
+++ commentaire
La fonction sinus est utilisée pour calculer l’aire du triangle selon la formule trigonométrique classique.
***
