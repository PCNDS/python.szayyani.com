
# NumPy pour la Physique : Feuille d’Activités

---

## Fonction numpy : array

### Exercice 1 : Créez un tableau NumPy à partir de la liste `` et affichez-le.

<details><summary>Solution</summary>

```python
# Crée un tableau NumPy à partir d'une liste Python
arr = np.array([1, 2, 3, 4])
# Affiche le tableau créé
print(arr)
```

**Sortie :**

```
[1 2 3 4]
```

</details>

---

### Exercice 2 : Créez un tableau NumPy 2D de forme (2, 3) contenant les nombres de 1 à 6, puis affichez-le.

<details><summary>Solution</summary>

```python
# Crée un tableau 2D NumPy avec 2 lignes et 3 colonnes
arr = np.array([[1, 2, 3],
                [4, 5, 6]])
# Affiche le tableau 2D
print(arr)
```

**Sortie :**

```
[[1 2 3]
 [4 5 6]]
```

</details>

---

### Exercice 3 : Créez un tableau NumPy à partir de la liste de nombres flottants `[1.1, 2.2, 3.3]` et affichez-le.

<details><summary>Solution</summary>

```python
# Crée un tableau NumPy avec des nombres à virgule flottante
arr = np.array([1.1, 2.2, 3.3])
# Affiche le tableau créé
print(arr)
```

**Sortie :**

```
[1.1 2.2 3.3]
```

</details>

---

## Fonction numpy : arange

### Exercice 1 : Utilisez `np.arange` pour créer un tableau contenant les entiers de 0 à 9 inclus, puis affichez-le.

<details><summary>Solution</summary>

```python
# Crée un tableau avec les entiers de 0 à 9
arr = np.arange(10)
# Affiche le tableau
print(arr)
```

**Sortie :**

```
[0 1 2 3 4 5 6 7 8 9]
```

</details>

---

### Exercice 2 : Utilisez `np.arange` pour créer un tableau contenant les entiers de 5 à 15 inclus, puis affichez-le.

<details><summary>Solution</summary>

```python
# Crée un tableau avec les entiers de 5 à 15
arr = np.arange(5, 16)
# Affiche le tableau
print(arr)
```

**Sortie :**

```
[ 5  6  7  8  9 10 11 12 13 14 15]
```

</details>

---

### Exercice 3 : Utilisez `np.arange` pour créer un tableau contenant les nombres de 0 à 20 inclus, avec un pas de 2, puis affichez-le.

<details><summary>Solution</summary>

```python
# Crée un tableau de 0 à 20 avec un pas de 2
arr = np.arange(0, 21, 2)
# Affiche le tableau
print(arr)
```

**Sortie :**

```
[ 0  2  4  6  8 10 12 14 16 18 20]
```

</details>

---

## Fonction numpy : linspace

### Exercice 1 : Utilisez `np.linspace` pour créer un tableau contenant 5 valeurs également espacées entre 0 et 1, puis affichez-le.

<details><summary>Solution</summary>

```python
# Crée un tableau de 5 valeurs entre 0 et 1, espacées uniformément
arr = np.linspace(0, 1, 5)
# Affiche le tableau
print(arr)
```

**Sortie :**

```
[0.   0.25 0.5  0.75 1.  ]
```

</details>

---

### Exercice 2 : Utilisez `np.linspace` pour créer un tableau contenant 10 valeurs également espacées entre 1 et 10, puis affichez-le.

<details><summary>Solution</summary>

```python
# Crée un tableau de 10 valeurs entre 1 et 10, espacées uniformément
arr = np.linspace(1, 10, 10)
# Affiche le tableau
print(arr)
```

**Sortie :**

```
[ 1.  2.  3.  4.  5.  6.  7.  8.  9. 10.]
```

</details>

---

### Exercice 3 : Utilisez `np.linspace` pour créer un tableau contenant 3 valeurs également espacées entre -1 et 1, puis affichez-le.

<details><summary>Solution</summary>

```python
# Crée un tableau de 3 valeurs entre -1 et 1, espacées uniformément
arr = np.linspace(-1, 1, 3)
# Affiche le tableau
print(arr)
```

**Sortie :**

```
[-1.  0.  1.]
```

</details>

---

## Fonction numpy : dot

### Exercice 1 : Calculez le produit scalaire des vecteurs ``et`` à l’aide de `np.dot` et affichez le résultat.

<details><summary>Solution</summary>

```python
# Définition du premier vecteur
v1 = np.array([1, 2, 3])
# Définition du second vecteur
v2 = np.array([4, 5, 6])
# Calcul du produit scalaire
result = np.dot(v1, v2)
# Affiche le résultat
print(result)
```

**Sortie :**

```
32
```

</details>

---

### Exercice 2 : Calculez le produit matriciel de deux matrices 2x2 `[,]` et `[,]` avec `np.dot` et affichez le résultat.

<details><summary>Solution</summary>

```python
# Définition de la première matrice 2x2
m1 = np.array([[1, 2], [3, 4]])
# Définition de la deuxième matrice 2x2
m2 = np.array([[5, 6], [7, 8]])
# Calcul du produit matriciel
result = np.dot(m1, m2)
# Affiche le résultat
print(result)
```

**Sortie :**

```
[[19 22]
 [43 50]]
```

</details>

---

### Exercice 3 : Calculez le produit scalaire de deux vecteurs orthogonaux ``et`` avec `np.dot` et affichez le résultat.

<details><summary>Solution</summary>

```python
# Premier vecteur orthogonal
v1 = np.array([1, 0])
# Deuxième vecteur orthogonal
v2 = np.array([0, 1])
# Calcul du produit scalaire (doit être 0)
result = np.dot(v1, v2)
# Affiche le résultat
print(result)
```

**Sortie :**

```
0
```

</details>

---

## Fonction numpy : sqrt

### Exercice 1 : Calculez la racine carrée du nombre 16 avec `np.sqrt` et affichez le résultat.

<details><summary>Solution</summary>

```python
# Calcul de la racine carrée de 16
result = np.sqrt(16)
# Affiche le résultat
print(result)
```

**Sortie :**

```
4.0
```

</details>

---

### Exercice 2 : Calculez la racine carrée de chaque élément du tableau `` avec `np.sqrt` et affichez le résultat.

<details><summary>Solution</summary>

```python
# Création du tableau
arr = np.array([1, 4, 9, 16])
# Calcul de la racine carrée de chaque élément
result = np.sqrt(arr)
# Affiche le tableau résultat
print(result)
```

**Sortie :**

```
[1. 2. 3. 4.]
```

</details>

---

### Exercice 3 : Calculez la racine carrée du nombre flottant 2.25 avec `np.sqrt` et affichez le résultat.

<details><summary>Solution</summary>

```python
# Calcul de la racine carrée de 2.25
result = np.sqrt(2.25)
# Affiche le résultat
print(result)
```

**Sortie :**

```
1.5
```

</details>

---

## Fonction numpy : sin

### Exercice 1 : Calculez le sinus de 0 avec `np.sin` et affichez le résultat.

<details><summary>Solution</summary>

```python
# Calcul du sinus de 0
result = np.sin(0)
# Affiche le résultat
print(result)
```

**Sortie :**

```
0.0
```

</details>

---

### Exercice 2 : Calculez le sinus des angles `[0, π/2, π]` (en radians) avec `np.sin` et affichez les résultats.

<details><summary>Solution</summary>

```python
# Création d'un tableau d'angles en radians
arr = np.array([0, np.pi/2, np.pi])
# Calcul du sinus pour chaque angle
result = np.sin(arr)
# Affiche le tableau résultat
print(result)
```

**Sortie :**

```
[0.0000000e+00 1.0000000e+00 1.2246468e-16]
```

</details>

---

### Exercice 3 : Calculez le sinus de π/4 avec `np.sin` et affichez le résultat.

<details><summary>Solution</summary>

```python
# Calcul du sinus de π/4
result = np.sin(np.pi/4)
# Affiche le résultat
print(result)
```

**Sortie :**

```
0.7071067811865475
```

</details>

---

## Fonction numpy : cos

### Exercice 1 : Calculez le cosinus de 0 avec `np.cos` et affichez le résultat.

<details><summary>Solution</summary>

```python
# Calcul du cosinus de 0
result = np.cos(0)
# Affiche le résultat
print(result)
```

**Sortie :**

```
1.0
```

</details>

---

### Exercice 2 : Calculez le cosinus des angles `[0, π/2, π]` (en radians) avec `np.cos` et affichez les résultats.

<details><summary>Solution</summary>

```python
# Création d'un tableau d'angles en radians
arr = np.array([0, np.pi/2, np.pi])
# Calcul du cosinus pour chaque angle
result = np.cos(arr)
# Affiche le tableau résultat
print(result)
```

**Sortie :**

```
[ 1.000000e+00  6.123234e-17 -1.000000e+00]
```

</details>

---

### Exercice 3 : Calculez le cosinus de π/4 avec `np.cos` et affichez le résultat.

<details><summary>Solution</summary>

```python
# Calcul du cosinus de π/4
result = np.cos(np.pi/4)
# Affiche le résultat
print(result)
```

**Sortie :**

```
0.7071067811865476
```

</details>

---

## Fonction numpy : sum

### Exercice 1 : Calculez la somme des éléments du tableau `` avec `np.sum` et affichez le résultat.

<details><summary>Solution</summary>

```python
# Création d'un tableau
arr = np.array([1, 2, 3, 4])
# Calcul de la somme des éléments
result = np.sum(arr)
# Affiche le résultat
print(result)
```

**Sortie :**

```
10
```

</details>

---

### Exercice 2 : Calculez la somme de tous les éléments du tableau 2D `[,]` avec `np.sum` et affichez le résultat.

<details><summary>Solution</summary>

```python
# Création d'un tableau 2D
arr = np.array([[1, 2], [3, 4]])
# Calcul de la somme de tous les éléments
result = np.sum(arr)
# Affiche le résultat
print(result)
```

**Sortie :**

```
10
```

</details>

---

### Exercice 3 : Calculez la somme des éléments du tableau 2D `[,]` selon les colonnes (axe 0) avec `np.sum` et affichez le résultat.

<details><summary>Solution</summary>

```python
# Création d'un tableau 2D
arr = np.array([[1, 2], [3, 4]])
# Calcul de la somme selon l'axe 0 (colonnes)
result = np.sum(arr, axis=0)
# Affiche le résultat
print(result)
```

**Sortie :**

```
[4 6]
```

</details>

---

## Fonction numpy : mean

### Exercice 1 : Calculez la moyenne des éléments du tableau `` avec `np.mean` et affichez le résultat.

<details><summary>Solution</summary>

```python
# Création d'un tableau
arr = np.array([1, 2, 3, 4])
# Calcul de la moyenne
result = np.mean(arr)
# Affiche le résultat
print(result)
```

**Sortie :**

```
2.5
```

</details>

---

### Exercice 2 : Calculez la moyenne de tous les éléments du tableau 2D `[,]` avec `np.mean` et affichez le résultat.

<details><summary>Solution</summary>

```python
# Création d'un tableau 2D
arr = np.array([[1, 2], [3, 4]])
# Calcul de la moyenne de tous les éléments
result = np.mean(arr)
# Affiche le résultat
print(result)
```

**Sortie :**

```
2.5
```

</details>

---

### Exercice 3 : Calculez la moyenne des éléments du tableau 2D `[,]` selon les lignes (axe 1) avec `np.mean` et affichez le résultat.

<details><summary>Solution</summary>

```python
# Création d'un tableau 2D
arr = np.array([[1, 2], [3, 4]])
# Calcul de la moyenne selon l'axe 1 (lignes)
result = np.mean(arr, axis=1)
# Affiche le résultat
print(result)
```

**Sortie :**

```
[1.5 3.5]
```

</details>

---

## Fonction numpy : average

### Exercice 1 : Calculez la moyenne pondérée du tableau `` avec les poids `[0.1, 0.2, 0.3, 0.4]` en utilisant `np.average` et affichez le résultat.

<details><summary>Solution</summary>

```python
# Création d'un tableau de valeurs
arr = np.array([1, 2, 3, 4])
# Définition des poids associés
weights = np.array([0.1, 0.2, 0.3, 0.4])
# Calcul de la moyenne pondérée
result = np.average(arr, weights=weights)
# Affiche le résultat
print(result)
```

