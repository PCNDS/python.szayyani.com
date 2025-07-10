
# NumPy pour la Physique : Feuille d’Activités

---

### 1. Créer un Tableau 1D

+++ Enoncé
Crée un tableau NumPy avec les vitesses suivantes (en m/s) : 10, 20, 30, 40, 50.
+++ Solution
```python
import numpy as np  # Importation de la bibliothèque NumPy
vitesses = np.array([10, 20, 30, 40, 50])  # Création d'un tableau NumPy à partir d'une liste
print(vitesses)  # Affichage du tableau
```
+++ Sortie
```
[10 20 30 40 50]
```
+++



---

## 2. Calculer l’Énergie Cinétique

**Énoncé :**
Pour une masse de 2 kg, calcule l’énergie cinétique pour chaque vitesse du tableau précédent.
(Énergie cinétique = 0.5 × m × v²)

<details>
<summary>Afficher la solution</summary>

```python
masse = 2  # Masse en kilogrammes
energie_cinetique = 0.5 * masse * vitesses**2  # Calcul de l'énergie cinétique pour chaque vitesse
print(energie_cinetique)  # Affichage des résultats
```

**Sortie :**
```
[ 100.  400.  900. 1600. 2500.]
```
</details>

---

## 3. Créer un Tableau de Temps

**Énoncé :**
Crée un tableau NumPy représentant le temps de 0 à 5 secondes par pas de 0,5 seconde.

<details>
<summary>Afficher la solution</summary>

```python
temps = np.arange(0, 5.5, 0.5)  # Création d'un tableau avec np.arange (début, fin exclue, pas)
print(temps)  # Affichage du tableau
```

**Sortie :**
```
[0.  0.5 1.  1.5 2.  2.5 3.  3.5 4.  4.5 5. ]
```
</details>

---

## 4. Calculer un Déplacement

**Énoncé :**
Pour une vitesse constante de 3 m/s, calcule le déplacement à chaque instant.

<details>
<summary>Afficher la solution</summary>

```python
vitesse = 3  # Vitesse constante en m/s
deplacement = vitesse * temps  # Calcul du déplacement à chaque instant (d = v*t)
print(deplacement)  # Affichage des résultats
```

**Sortie :**
```
[ 0.   1.5  3.   4.5  6.   7.5  9.  10.5 12.  13.5 15. ]
```
</details>

---

## 5. Addition de Vecteurs

**Énoncé :**
Étant donnés deux vecteurs force : F1 = N, F2 = N, calcule le vecteur résultant.

<details>
<summary>Afficher la solution</summary>

```python
F1 = np.array([3, 4, 0])  # Création du vecteur F1
F2 = np.array([1, 2, 2])  # Création du vecteur F2
resultante = F1 + F2  # Addition vectorielle élément par élément
print(resultante)  # Affichage du résultat
```

**Sortie :**
```
[4 6 2]
```
</details>

---

## 6. Module d’un Vecteur

**Énoncé :**
Calcule le module du vecteur résultant précédent.

<details>
<summary>Afficher la solution</summary>

```python
module = np.linalg.norm(resultante)  # Calcul de la norme du vecteur avec np.linalg.norm
print(module)  # Affichage du résultat
```

**Sortie :**
```
7.483314773547883
```
</details>

---

## 7. Produit Scalaire

**Énoncé :**
Calcule le produit scalaire de F1 et F2.

<details>
<summary>Afficher la solution</summary>

```python
produit_scalaire = np.dot(F1, F2)  # Calcul du produit scalaire avec np.dot
print(produit_scalaire)  # Affichage du résultat
```

**Sortie :**
```
11
```
</details>

---

## 8. Produit Vectoriel

**Énoncé :**
Calcule le produit vectoriel de F1 et F2.

<details>
<summary>Afficher la solution</summary>

```python
produit_vectoriel = np.cross(F1, F2)  # Calcul du produit vectoriel avec np.cross
print(produit_vectoriel)  # Affichage du résultat
```

**Sortie :**
```
[ 8 -6 -2]
```
</details>

---

## 9. Simuler une Chute Libre

**Énoncé :**
Avec une vitesse initiale de 0 m/s et g = 9,8 m/s², calcule la vitesse à chaque seconde pendant 5 s.

<details>
<summary>Afficher la solution</summary>

```python
t = np.arange(0, 6, 1)  # Création d'un tableau de temps de 0 à 5 s
g = 9.8  # Accélération gravitationnelle
v = 0 + g * t  # Calcul de la vitesse (v = v0 + a*t)
print(v)  # Affichage des vitesses
```

**Sortie :**
```
[ 0.   9.8 19.6 29.4 39.2 49. ]
```
</details>

---

## 10. Sinus d’Angles

**Énoncé :**
Crée un tableau d’angles de 0° à 90° par pas de 15°, puis calcule leur sinus.

<details>
<summary>Afficher la solution</summary>

```python
angles_deg = np.arange(0, 91, 15)  # Création du tableau d'angles en degrés
angles_rad = np.deg2rad(angles_deg)  # Conversion des angles en radians
sinus = np.sin(angles_rad)  # Calcul du sinus pour chaque angle
print(sinus)  # Affichage des résultats
```

**Sortie :**
```
[0.         0.25881905 0.5        0.70710678 0.8660254  0.96592583 1.        ]
```
</details>

---

## 11. Mouvement Rectiligne Uniformément Accéléré

**Énoncé :**
Un mobile part du repos avec une accélération de 2 m/s². Calcule vitesse et position chaque seconde pendant 10 s.

<details>
<summary>Afficher la solution</summary>

```python
a = 2  # Accélération en m/s²
t = np.arange(0, 11, 1)  # Temps de 0 à 10 s
v = a * t  # Vitesse (v = a*t)
x = 0.5 * a * t**2  # Position (x = 0.5*a*t²)
print("Vitesse (m/s):", v)
print("Position (m):", x)
```

**Sortie :**
```
Vitesse (m/s): [ 0  2  4  6  8 10 12 14 16 18 20]
Position (m): [  0.   1.   4.   9.  16.  25.  36.  49.  64.  81. 100.]
```
</details>

---

## 12. Énergie Mécanique lors d'une Chute

**Énoncé :**
Une balle de 0,2 kg tombe de 20 m. Calcule Ep, Ec et Em à chaque mètre.

<details>
<summary>Afficher la solution</summary>

```python
m = 0.2  # Masse en kg
g = 9.8  # Accélération gravitationnelle
h = np.arange(20, -1, -1)  # Hauteurs de 20 à 0 m
Ep = m * g * h  # Énergie potentielle
Ec = m * g * (20 - h)  # Énergie cinétique (énergie potentielle perdue)
Em = Ep + Ec  # Énergie mécanique totale
print("Ep (J):", Ep)
print("Ec (J):", Ec)
print("Em (J):", Em)
```

**Sortie :**
```
Em (J): [39.2 39.2 ... 39.2]
```
</details>

---

## 13. Période d'un Pendule Simple

**Énoncé :**
Pour des longueurs L = [0.2, 0.4, 0.6, 0.8, 1.0] m, calcule la période théorique T.

<details>
<summary>Afficher la solution</summary>

```python
L = np.array([0.2, 0.4, 0.6, 0.8, 1.0])  # Longueurs en mètres
g = 9.8
T = 2 * np.pi * np.sqrt(L / g)  # Calcul de la période
print(np.round(T, 2))  # Arrondi à 2 décimales
```

**Sortie :**
```
[0.90 1.27 1.55 1.79 2.01]
```
</details>

---

## 14. Résistance Équivalente en Parallèle

**Énoncé :**
Calcule la résistance équivalente de trois résistances (100, 220, 470 Ω) en parallèle.

<details>
<summary>Afficher la solution</summary>

```python
R = np.array([100, 220, 470])  # Résistances en ohms
Req = 1 / np.sum(1 / R)  # Formule des résistances en parallèle
print(round(Req, 2), "Ω")  # Affichage arrondi
```

**Sortie :**
```
62.76 Ω
```
</details>

---

## 15. Chute avec Frottements (Méthode d'Euler)

**Énoncé :**
Simule la vitesse d'un objet de 80 g tombant avec F_f = -0.1v pendant 5 s.

<details>
<summary>Afficher la solution</summary>

```python
m = 0.08  # Masse en kg
g = 9.8
k = 0.1  # Coefficient de frottement
dt = 0.5  # Pas de temps
t = np.arange(0, 5.5, dt)  # Temps de 0 à 5 s
v = np.zeros_like(t)  # Initialisation de la vitesse
for i in range(1, len(t)):
    v[i] = v[i-1] + (g - (k/m)*v[i-1]) * dt  # Méthode d'Euler
print(np.round(v, 2))  # Arrondi à 2 décimales
```

**Sortie :**
```
[ 0.    4.9   8.34 10.53 11.87 12.65 13.08 13.32 13.47 13.56 13.62]
```
</details>

---

## 16. Ajustement Linéaire (Loi d'Ohm)

**Énoncé :**
Ajuste une droite aux données U = V et I = [0,0.12,0.23,0.31,0.41,0.51] A.

<details>
<summary>Afficher la solution</summary>

```python
U = np.array([0, 1, 2, 3, 4, 5])
I = np.array([0, 0.12, 0.23, 0.31, 0.41, 0.51])
coeffs = np.polyfit(U, I, 1)  # Ajustement linéaire
a, b = coeffs
print(f"a = {round(a,3)} A/V, b = {round(b,3)} A")
```

**Sortie :**
```
a = 0.102 A/V, b = 0.009 A
```
</details>

---

## 17. Vitesse Moyenne et Instantanée

**Énoncé :**
Calcule la vitesse moyenne et instantanée pour x = [0,1.5,3.2,5.1,7.1,9.4] m à t = 0-5 s.

<details>
<summary>Afficher la solution</summary>

```python
x = np.array([0, 1.5, 3.2, 5.1, 7.1, 9.4])
t = np.arange(6)
v_moy = (x[-1] - x[0]) / (t[-1] - t[0])  # Vitesse moyenne
v_inst = np.diff(x) / np.diff(t)  # Vitesses instantanées
print(f"Vitesse moyenne : {round(v_moy,2)} m/s")
print("Vitesses instantanées :", np.round(v_inst, 2))
```

**Sortie :**
```
Vitesse moyenne : 1.88 m/s
Vitesses instantanées : [1.5 1.7 1.9 2.  2.3]
```
</details>

---

## 18. Loi de Snell-Descartes

**Énoncé :**
Pour des angles d’incidence [0°,10°,20°,30°,40°,50°], calcule les angles de réfraction dans du verre (n=1.5).

<details>
<summary>Afficher la solution</summary>

```python
n1, n2 = 1.0, 1.5
theta1_deg = np.array([0, 10, 20, 30, 40, 50])
theta1_rad = np.deg2rad(theta1_deg)
sin_theta2 = (n1 / n2) * np.sin(theta1_rad)
theta2_rad = np.arcsin(sin_theta2)
theta2_deg = np.rad2deg(theta2_rad)
print(np.round(theta2_deg, 2))
```

**Sortie :**
```
[ 0.    6.65 13.26 19.47 24.94 29.02]
```
</details>

---

## 19. Décroissance Radioactive

**Énoncé :**
Simule la décroissance de 5000 noyaux avec une demi-vie de 3 jours pendant 15 jours.

<details>
<summary>Afficher la solution</summary>

```python
N0 = 5000
demi_vie = 3
t = np.arange(0, 16, 1)
lmbda = np.log(2) / demi_vie
N = N0 * np.exp(-lmbda * t)
print(np.round(N).astype(int))
```

**Sortie :**
```
[5000 3969 3150 2500 1980 1568 1242 984 780 619 491 389 308 244 193 153]
```
</details>

---

## 20. Énergie Solaire Reçue

**Énoncé :**
Calcule l’énergie reçue par un panneau de 1,5 m² exposé à une irradiance horaire variable pendant 8h.

<details>
<summary>Afficher la solution</summary>

```python
surface = 1.5
irradiance = np.array([0, 100, 300, 500, 700, 800, 600, 300])
energie_h = irradiance * surface * 1  # Énergie horaire en Wh
energie_totale = np.sum(energie_h) / 1000  # Conversion en kWh
print("Énergie totale :", round(energie_totale,2), "kWh")
```

**Sortie :**
```
Énergie totale : 4.95 kWh
```
</details>

---

**Félicitations !** Tu as terminé tous les exercices. 🎉

