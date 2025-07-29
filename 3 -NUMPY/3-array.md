---
Title : Fonction: `array`
order : 790
---

## La Fonction `array`

La méthode la plus simple et la plus directe (mais pas forcément la plus utile) est de simple *définir* l'array et ses constituants, comme dans l'exemple suivant : 

+++ Code
```python
A = np.array([[4,3],[3,2]])
B = np.array([[4,3,0,-5]])

print("A est ", A) #pour afficher l'array A
print("B est ", B)
```
+++ Sortie
```pyton
>>> A est  [[4 3]
 [3 2]]
 >>> B est  [[ 4  3  0 -5]]
``` 
+++

Il y a d'autres méthodes de créer une matrice avec la fonction `array`, mais pour le moment ce que l'on a vu suffira. 

Dans les cas précédents on a pu utiliser la fonction `array` car nous avions déjà les valeurs que l'on voulait mettre dans notre matrice. Cela peut être très utile par exemple dans le cas des mesures expérimentales que nous avons relevées lors d'une expérience (des distances parcourues par un objet, des valeur de pH mesurées avec un pH-mètre, etc). 

En revanche, parfois nous voulons juste une séries de valeurs à un intervalle régulier. Pour cela nous avons deux fonctions très pratiques et simples : `arange` et `linspace`

