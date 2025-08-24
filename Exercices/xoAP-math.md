---
title : Exercices - Math
order : 10
---


### Exercice 3 : Hypothénuse d'un triangle
+++ Enoncé
Écris une fonction `hypotenuse(a, b)` qui calcule la longueur de l'hypoténuse d'un triangle rectangle dont les côtés adjacents à l'angle droit ont pour longueurs `a` et `b`.
Utilise la fonction `math.hypot` et vérifie avec le théorème de Pythagore `math.sqrt(a**2 + b**2)`.
+++ code
```python
import math

def hypotenuse(a, b):
    # Méthode 1 : Fonction dédiée
    resultat_hypot = math.hypot(a, b)
    # Méthode 2 : Théorème de Pythagore
    resultat_pythagore = math.sqrt(a**2 + b**2)

    print(f"Avec math.hypot({a}, {b}) : {resultat_hypot}")
    print(f"Avec Pythagore sqrt({a}² + {b}²) : {resultat_pythagore}")
    return resultat_hypot

# Test avec un triangle 3-4-5
hypotenuse(3, 4)
```
+++ sortie
```python
>>> Avec math.hypot(3, 4) : 5.0
>>> Avec Pythagore sqrt(3² + 4²) : 5.0
```
+++ commentaire

Excellent exercice pour faire le lien entre les mathématiques et la programmation. Montre qu'il existe souvent plusieurs solutions.

+++

---

### Exercice 4 : Conversion degrés/radians
+++ Enoncé
Le module `math` travaille principalement en radians.
1. Crée une fonction `degres_vers_radians(angle_deg)` qui convertit un angle de degrés en radians.
2. Crée une fonction `radians_vers_degres(angle_rad)` qui fait la conversion inverse.
3. Teste avec 180°, 90° et 45°.
+++ code
```python
import math

def degres_vers_radians(angle_deg):
    return angle_deg * (math.pi / 180)

def radians_vers_degres(angle_rad):
    return angle_rad * (180 / math.pi)

# Tests
angles_test = [180, 90, 45]
for angle in angles_test:
    rad = degres_vers_radians(angle)
    deg = radians_vers_degres(rad)
    print(f"{angle}° -> {rad:.4f} rad -> {deg:.1f}°")
```
+++ sortie
```python
180° -> 3.1416 rad -> 180.0°
90° -> 1.5708 rad -> 90.0°
45° -> 0.7854 rad -> 45.0°
```
+++ commentaire

Fondamental pour la suite, car les fonctions trigonométriques de `math` nécessitent des angles en radians.

+++

---

### Exercice 7 : Distance entre deux points
+++ Enoncé
Écris une fonction `distance(x1, y1, x2, y2)` qui calcule la distance entre deux points A(x1, y1) et B(x2, y2) dans un plan 2D en utilisant le théorème de Pythagore.
+++ code
```python
import math

def distance(x1, y1, x2, y2):
    dx = x2 - x1  # Différence des abscisses
    dy = y2 - y1  # Différence des ordonnées
    return math.sqrt(dx**2 + dy**2)

# Test avec les points A(1, 1) et B(4, 5)
d = distance(1, 1, 4, 5)
print(f"La distance entre A(1,1) et B(4,5) est : {d:.2f}")
```
+++ sortie
```python
La distance entre A(1,1) et B(4,5) est : 5.00
```
+++ commentaire
Application géométrique classique et très visuelle. On peut facilement dessiner le triangle rectangle pour illustrer.
+++

---

### Exercice 5 : Trigonométrie et triangle rectangle
+++ Enoncé
Dans un triangle rectangle, l'hypoténuse mesure 10 cm et un angle mesure 35°.
Calcule la longueur du côté adjacent et du côté opposé à cet angle en utilisant `math.cos` et `math.sin`.
+++ code
```python
import math

hypotenuse = 10
angle_deg = 35

# Conversion de l'angle en radians
angle_rad = math.radians(angle_deg)

# Calcul des côtés
cote_adjacent = hypotenuse * math.cos(angle_rad)
cote_oppose = hypotenuse * math.sin(angle_rad)

print(f"Pour un angle de {angle_deg}° et une hypoténuse de {hypotenuse} cm :")
print(f"- Côté adjacent : {cote_adjacent:.2f} cm")
print(f"- Côté opposé : {cote_oppose:.2f} cm")
```
+++ sortie
```python
Pour un angle de 35° et une hypoténuse de 10 cm :
- Côté adjacent : 8.19 cm
- Côté opposé : 5.74 cm
```
+++ commentaire

Application concrète de la trigonométrie. Montre l'utilité de la conversion degrés/radians.

---

### Exercice 9 : Résolution d'une équation du second degré
+++ Enoncé
Écris un programme qui résoud une équation du second degré de la forme `ax² + bx + c = 0`.
Le programme doit demander les coefficients a, b et c à l'utilisateur, calculer le discriminant (`delta = b² - 4ac`) et afficher les solutions en utilisant `math.sqrt`.
Gère le cas où le discriminant est négatif.
+++ code
```python

print("Résolution de l'équation ax² + bx + c = 0")
a = float(input("Entrez le coefficient a : "))
b = float(input("Entrez le coefficient b : "))
c = float(input("Entrez le coefficient c : "))

# Calcul du discriminant
delta = b**2 - 4*a*c

print(f"\nPour l'équation {a}x² + {b}x + {c} = 0")
print(f"Delta = {delta}")

if delta > 0:
    # Deux solutions réelles
    x1 = (-b - math.sqrt(delta)) / (2*a)
    x2 = (-b + math.sqrt(delta)) / (2*a)
    print("Deux solutions réelles :")
    print(f"x1 = {x1:.2f}")
    print(f"x2 = {x2:.2f}")
elif delta == 0:
    # Une solution réelle
    x0 = -b / (2*a)
    print("Une solution réelle double :")
    print(f"x0 = {x0:.2f}")
else:
    # Discriminant négatif
    print("Le discriminant est négatif. Aucune solution réelle.")
```
+++ sortie
```python
Résolution de l'équation ax² + bx + c = 0
Entrez le coefficient a : 1
Entrez le coefficient b : -3
Entrez le coefficient c : 2

Pour l'équation 1.0x² + -3.0x + 2.0 = 0
Delta = 1.0
Deux solutions réelles :
x1 = 1.00
x2 = 2.00
```
+++ commentaire

Exercice de synthèse plus complexe. Fait appel aux conditions, aux formules mathématiques et à la fonction `sqrt`.

+++

---

### Exercice 10 : Approximation de π par la formule de Leibniz

+++ Enoncé
Utilise la formule de Leibniz pour approximer la valeur de π :
π/4 = 1 - 1/3 + 1/5 - 1/7 + 1/9 - 1/11 + ...
Demande à l'utilisateur le nombre d'itérations `n` et calcule une approximation de π. Compare le résultat avec `math.pi`.
+++ code
```python
import math

n = int(input("Entrez le nombre d'itérations pour l'approximation de π : "))

approximation_pi = 0
signe = 1  # Gère l'alternance des signes +/-

for i in range(n):
    terme = 1 / (2*i + 1)  # Dénominateur: 1, 3, 5, 7, ...
    approximation_pi += signe * terme
    signe *= -1  # Change le signe pour le terme suivant

approximation_pi *= 4  # On a calculé π/4, donc on multiplie par 4

print(f"\nAprès {n} itérations :")
print(f"- Approximation de π : {approximation_pi}")
print(f"- Vraie valeur de π  : {math.pi}")
print(f"- Erreur            : {abs(math.pi - approximation_pi)}")
```
+++ sortie
```python
Entrez le nombre d'itérations pour l'approximation de π : 1000

Après 1000 itérations :
- Approximation de π : 3.140592653839794
- Vraie valeur de π  : 3.141592653589793
- Erreur            : 0.000999999749998981
```
+++ commentaire

Exercice avancé qui introduit les notions de série, d'approximation et de boucles. Montre comment les mathématiques et l'informatique peuvent collaborer pour résoudre des problèmes.

---


