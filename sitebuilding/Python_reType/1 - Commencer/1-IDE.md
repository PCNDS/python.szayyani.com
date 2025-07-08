---
Title : IDE - Environnement de Codage
icon : iterations
order : 1
---

## IDE - Environnement de codage 

### Installation d'un IDE

Un IDE (Independent Development Environement) - EDI en français - est *l'espace* dans lequel on écrit et on compile notre code. 

Il y a littéralement des centaines d'IDE pour coder en PYTHON, utilisable gratuitement. La majorité sont à télécharger et installer sur votre PC/Mac, et un certain nombre sont utilisable directement sur internet (dans le *nuage*) et donc nécessite aucune installation 

> [!INFO] IDE téléchargeable sur votre ordi : 
> Voici quelques suggestions d'IDE pour vous, **téléchargeable pour votre ordinateur personnel**: 
> - **[Edupython](https://edupython.tuxfamily.org/#t%C3%A9l%C3%A9chargement)** : développé par l'éducation nationale pour l'utilisation par des lycéens. Ne marche que sur *Windows*
> - **[SPYDER](https://www.spyder-ide.org/download/)** : Un IDE robuste et utilisable par tout niveau d'expertise. Installable sous toutes plateformes *windows/mac/linux*. [Bonne guide > d'installation ici.](https://docs.spyder-ide.org/current/installation.html) 

> [!INFO] IDE dans le nuage, sans téléchargement nécessaire :  
> Voici queqlues suggestion d'IDE **utilisable sur le web** :
> - [**Google Colab**](https://colab.research.google.com/) : Un *notebook* basée sur *Jupyter*. Gratuit à utiliser si vous avez un compte Google/Gmail/Gdrive. l'avantage de cette plateform est > le fait de pouvoir écrire comme dans un traitement de text ET inclure de bloc de code executable comme dans un IDE ET la possibilité de partage son document avec quelques d'autre. 
> - [**Replit**](https://repl.it) : Un IDE dans le *cloud/nuage*. Il suffit de créer son compte gratuit et vous pouvez coder dans beaucoup de langue différentes, dont PYTHON. Pas besoin > > 
  d'installer quoique ce soit. 


Une fois votre IDE installé vous pouvez commencer avec quelques opérations de base. 

### Interface d'un IDE 

De manière générale votre environnement de codage est divisé en deux partie : 
- **Editeur** : comme un traitement de texte, là où vous allez écrire votre programme/code (script).
- **Console** : l'endroit où s'affichent les résultats de l'execution de votre programme (textes, chiffres ou graphiques), mais là où vous pouvez interagir avec le programme une fois executé. 

Un IDE est essentiellement un traducteur. Vous ecrivez votre programme dans la langue choisie (PYTHON, Java, javascript, C++, Ruby, etc ...), et puis l'IDE traduit ce programme en langage machine (en code binaire composé des $1$ et $0$). 

L'IDE fait cela grâce à un *compilateur*. Execution d'un programme s'appelle donc "compiler le code". 

### Executer un programme 


Afin de compiler votre programme il y a un bouton dans l'interface de votre IDE (souvent en form d'un bouton "play" :arrow_forward:).  Since il existe des raccourcis clavier : `ctrl-F9`. (dans le cas de google colab ou jupyter c'est `ctrl-entrer`)

#### Dans la console

IL y a la possibilité d'executer certains opérations ou fonctions directement dans la console. **voilà à quoi ressemble la console** : 

```python
>>> 
```
Vous pouvez y écrire une commande comme `print` (pour écrire un texte), et tapper `entrer` et l'executer toute de suite : 

```python
>>> print("Hello World !")
Hello World ! 
```

La console est aussi un calculatrice, c'est à dire vous pouvez écrire le calcule que vous voulez effectuer directement dans la console, appuyer sur `entrer` et obtenir le résultat toute de suite: 
```python
>>> 2*2
4
>>> 2*(3+5)
16
```

Un des _superpouvoir_ de PYTHON est la possibilité de créer ses propres fonctions. On verra ça bien plus tard, mais en effet vous pouvez *définir* vous même une **fonction**. 

Une fois votre programme compilé, la fonction est utilisable dans la console. Imaginer que vous avec défini une fonction qui calcule la racien carré d'un nombre, que vous nommez `racineCarre`. Après avoir compilé le programme, vous pouvez utiliser directement dans la console, la fonction que vous avez créee, comme le suivant : 

```python
>>> racineCarre(16)
4
```

!!!tip Points Clefs 
* Afin de coder en `PYTHON`, il faut un environnemetn de codage : un IDE. 
* IDe est composé d'un **éditeur** pour écrire le code, et une  **console** pour executer le code et voir ses résultats.
!!!

