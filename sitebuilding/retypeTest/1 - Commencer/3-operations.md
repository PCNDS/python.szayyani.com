---
Title : Opérations de base
order : -2
---

Une fois installé PYTHON est capable d'un certain nombre d'opération mathématiques et logiques de bases. 

## Opérations arithmétiques

Voici une liste courte des opérations arithmétiques les plus pertinentes pour nous : 


| Symbole |   Operation    | Exemple          |
|:-------:|:--------------:|:---------------- |
|    `*`    | multiplication | `>>2*3` <br> `6` |
|    `/`     | division      |`>>6/3` <br> `2`|
|    `+`     |addition|`>>2+3` <br> `5`|
|   `-`      |soustraction|`>>2-3` <br> `-1`|
|    `**`     |puissance/exposant|`>>2**3` <br> `8`|
|`%`|reste (d'une division euclidéenne|`>>5%2` <br> `1`|
|   `//`    |quotient (d'une div. euclidéenne|`>>5//2` <br> `2`|

## Opérations d'affectation

Même si PYTHON s'écrit preque comme une rédaction mathématique (une des raisons pour laquelle on aime bien PYTHON), il y a des différences entre des symboles identiques. 

L'exemple parfait est le symbole `=`. Dans PYTHON `=` est une **affectation** (un assignement). Cela veut dire que quand vous écrivez ` a = 10`, vous êtes en train d'assigner une valeur (10) a une variable (a). 

Voici donc quelques opérations d'affectation (j'aurais déclaré d'amont que `a = 10`) : 



| Symbole | Opération | Exemple |
| :-------: | :---------: | :------- |
| `+=`        |addition|`a += 3` equivaut `a = a + 3` donc $13$|
|  `*=`       |multiplication|`a *= 3` équivaut `a = a * 3`donc $30$|
|   `**=`     |exponentiation|`a **= 3` équivaut `a = a**3` donc $1000$|

## Fonctions

Au coeur de PYTHON, et ce qui fait sa puissance calculatoire, sont les ***fonctions***. Une fonction est un ***ensemble d'instructions, qui prendre des arguments en entrée et qui retourne un/des résultats***. 

Les opérations mathématiques pré-éxistantes dans le programme de base sont des fonctions (très simples), mais l'on peut définir d'autre fonctions nous-mêmes. 

Les valeurs sur lesquelles une fonction fait son opération s'appelle ses *argument*. Voici un exemple : 
`sin(theta)` : ici la fonction **sin** a qu'un seul argument: la variable **theta**. 

**Une fonction peut avoir un seul ou plusieurs arguments**. Les fonctions trigononmétriques par exemples prennent qu'un seul argument. Mais la majorité des fonctions dans PYTHON prennet plusieurs arguments. Par exemple, la fonction `plot` qui permet de créer des graphiques/tracés, prend *au moins* deux argument : la variable en abcisse et la variable en ordonnnées `plot(x,y)` et retourne un graphique avec le tracé de $y=f(x)$.

Comme vous allez voir plus tard, vous pouvez définir vos propres fonctions, pour faire n'importe quelle opération, mais il y a déjà des catalogues de fonctions prédéfinie par d'autres personnes pour l'utilisation de toute le monde: ce sont des ***bibliothéques***. 

## Quelques fonctions de bases

Vous allez voirs des fonctions et des opérations spécifiques à la physique et maths dans les parties suivantes, mais il y a des fonctions de base que tout le monde doit connaître. Voici en une petite liste : 
- `print()` : cette fonction donne l'instruction d'écrire et retourner un texte ou un résultats calculé. Exemple : 
```python
>>> print("Hello world ! ")
Hello world !
>>> print("2 + 2")
2 + 2
>>> print (2+2)
4
```
- `len()` : permet de déterminer la longueur d'une séquence (de caractères, d'une liste, etc). Exemple : 
```python
>>> len("PYTHON")
6
>>> len([0,4,44,444, 4444])
5
```
- `type` : rèvle le "type" d'une donnée. Exemple : 

```python
>>> type(10)
'int' # c'est à dire un entier
>>> type(10.0)
'float' # c'est à dire un décimal
```
- `input()` : demande à l'utilisateur de saisir une donnée, de n'importe quel type (nombre, caractère, etc). Exemple : 

```python
nom = input("quel est votre nom de famille?")
# une fois executé la console demande à l'utilisateur de saisir un numbre, que PYTHON par la suite affecte dans la variable `nom`
```
