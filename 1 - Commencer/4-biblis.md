---
Title : Les Bibliothéques ! 
order : -3
---


Malgré la présences d'un nombre considérable d'opérations dans une installation basique de PYTHON, on a souvent besoin de pouvoir faire des choses qui ne sont pas possible sans définir nous-me$eme une fonction capable de le faire. 

Par exemple, si l'on voulait calcular la racine carré d'une nombre, il n'existe pas une fonction prédéfinie dans PYTHON. Néanmoins nous pouvons définir une fonction pour calculer la racine carré d'un nombre. Mais si l'on fait ça pour toute opération plus complexe (trigonométrique, logarithmique, etc) le travail peut devenir très laborieux.

Heureusement les gens généreux ont déjà fait ce travail pour nous, et l'ont mis dans une ***bibliothéque***. Une bibliothéque (ou module) est uen collection de fonction définie pour nous, pret à utiliser sans aucun effort de notre part. 

Ces bibliothéques sont groupés souvent par le type de fonction qu'ils proposent. Par exemple, pour visualisation graphique des données, ou pour faire de l'algèbre linéaire, ou la logique symbolique, etc. 

Nous sommes intéressé, en particulier, par trois bibliothéques : 

| Bibliothéque | L'usage |
| ------------ | ------- |
| **Math** |Des opérations mathématiques plus avancées et complexes (e.g. trigonométrique, logarithmiques, etc) |
|**Numpy** |Algèbre linéaire, traitement des séries de données, Data analysis (analyse des données|
|**Matplotlib**|Faire des graphqiues, visualisation des données|

## "Importation" d'une bibliothéque

Si nous voulons utiliser une ou des fonctions dans une bibliothéque il faut le dire au tout début de notre programme en utilisant l'instruction `import`. 

Il y a deux façons d'utiliser cette fonction : 
1. on "importe" TOUTE la bibliothéques. Dans ce cas-là le code est : 
```python
import math as m
```
Ici on donne l'instruction d'important toute la bibliothéque "math" ET on la renomme "m" (pour des raisons que vous allez voir)
2. on "importe" une fonction seulement, avec le code suivant : 
```python
from math import sin
```
Ici on donne l'instruction de chercher dans la bibliothéque "math" et d'importer *seulement* la fonction "sin" (sinus). 

> [!NOTE]
> **A noter :**
> - importation d'une bibliothéque dans votre IDE nécessite une connexion internet, si cela n'a jamais été fait avant
> - importation d'une seule fonction est *beaucoup* plus rapide qu'uen bibliothéque entière, et donc si vous ne comptais utiliser pas plusieurs fonction, il vaut mieux d'importer seulement la fonction nécessaire. 

Afin d'utiliser la fonction dans une bibliothéque dans votre programme il faut utiliser la notation suivante : `bibliotheque.fonction()`. Par exemple si l'on veut utiliser la fonction `sin` dans la bibliothéque `math` il faut : 
```python
import math as m 

A = m.sin(30)
```
Ici on a renommé `math` comme `m` et on dit au logiciel de chercher la fonction `sin` dans `m` et de l'appliquer à un angle de $30$. 

!!!tip Points Clefs 
* 
!!!