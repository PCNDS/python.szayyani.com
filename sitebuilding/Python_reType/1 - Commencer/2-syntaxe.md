---
Title : Règles de Syntaxe
order : -1
---

PYTHON comme toute langue a des règles de syntaxe et de grammaire à respecter, d'autant plus qu'une langue parlé que la moindre irrespect de ces règles de logique empêcherait l'execution de votre code ! 

Sans entrer trop en détail, il est important de noter que le langage PYTHON est très sensible à certaines règles de syntaxe notamment : 

## Ordre des choses : 
PYTHON lit le code dans l'ordre du haut vers le bas. C'est à dire si vous mentionnez une variable avant de l'avoir défini/affectée PYTHON aura du mal à executer le code. 

De la même manière, chaque nouvelle instruction peut remplacer une ancienne instruction en cas de conflit. Exemple : Vous définissez `a = 10` au début du programme, et plus tard vous donnez l'instruction `a = 15`, pour le programme, désormais la variable `a` a une valeur de `15` et non `10`.

## **Majuscule** et **minuscule** 
... ne sont pas pareilles. Une *variable* nommée `variable` n'est pas la même que `Variable` et encore différent que `VariAblE`. Pour PYTHON il s'agit de trois objets différents. 

## "**Ponctuation**" 
... est très important : on ne peut pas remplacer des `: ; , . " " ' '` de manière interchangeable. Au fur et à mesur vous allez apprendre le bon usage de cela, mais il faut vraiment le respecter scrupuleusement 

## Indentation 
de même pour "**l'indentation**" qui est essentielle pour la bonne organisation et structuration de votre programme. Par exemple, considérons les deux exemples suivants : 

```python
if 1>0 :
  print("1 est positif") 

if 1>0 :
print("1 est positif")
```
Dans le 2eme cas il y aura une erreur, car, en raison de manque d'indentation, PYTHON ne reconnait pas que le message à "printer" appartient à la condition précédente. 
La questions d'indentation est particulièrement important dans les "boucles" (`if`, `for`, `while`, etc). De manière générale, tout texte "indenté" qui suit une ligne apartient au même "bloc". 

## 'Types' de données

Un mot bref sur les différents "types" de données dans PYTHON. Voici une liste très brève des "types" les plus pertinentes pour nous : 

- Types numériques : 
    - `int` : les entiers, positifs ou négatifs
    - `float` : les "flottants", c'est à dire des nombres à virgules, c'est-à-dire décimal. Pour rappel, le décimal est, comme pour les anglophones, un `.` et non un `,`
    - `complex` : les nombres complexes, avec `j` pour la partie imaginaire du nombre. 
- types 'séquence' : 
    - `str` : une chaîne de caractères, c'est à dire du texte. 
    - `list` : une liste, une collection ordonées d'objet. 
- type 'Booléen' `bool` : représentant des vrais ou faux. Exemple : `true`, `false`. 

## Commentaires `#` : 
pour faire un commentaire : Tout text qui suit le symbole `#` est considéré comme un commentaire et NON comme du code à compiler par PYTHON.  Voici deux exemple : 
```python
# définissons un ARRAY avec nos mesures

X = np.array([0, 5, 10, 15, 20])
```
ici le commentaire joue le rôles - presque - de séparateur de sections dans notre programme
```python
Xrad = np.radians(X) #ici on convertit les angles dans la liste X, de degrées en radians
```
ici on s'informe du but de cette ligne de code. 

Vous devez utiliser les commentaires dans votre code, car cela peut vraiment aider à comprendre pourquoi vous avez inclut une ligne, après le fait. 

!!!tip Points Clefs 
* 
!!!