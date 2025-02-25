# Projet-TP-analyse 
                                ****Résolution des systémes linéaires***

 
  
![Demo_projet](https://user-images.githubusercontent.com/57879341/103366327-a2c71900-4ac2-11eb-906a-6401b3320965.gif)

# Introduction 

L’algèbre linéaire est un outil essentiel pour toutes les branches des mathématiques appliquées,
en particulier lorsqu’il s’agit de modéliser puis résoudre numériquement des problèmes issus de
divers domaines : des sciences physiques ou mécaniques, des sciences du vivant, de la chimie, de
l’économie, des sciences de l’ingénieur,...
Les systèmes linéaires interviennent dans de nombreux contextes d’applications car ils forment
la base calculatoire de l’algèbre linéaire.




# Partie Théorique: 


## Définition d'un système linéaire 

Un système de m équations à n inconnues x1, x2, ...xn s’écrit sous forme matricielle : AX = B où A est une matrice comportant m lignes et n colonnes,
X est le vecteur colonne dont les composantes sont les xi et B , le second
membre, est aussi un vecteur colonne avec n composantes.
Le vecteur X est appelé solution du système.




## Résolution par la méthode de Gauss
Le principe en est le suivant : 

par des combinaisons linéaires successives, on
transforme le système initial, que l’on prend tel quel sans changer l’ordre
des équations, en un système triangulaire supérieur, système ensuite résolu
en commençant par la dernière des équations transformées.
On rappelle qu’un système est dit triangulaire supérieur si la matrice associée est triangulaire supérieure.

Élimination de Gauss
2 étapes :
1. Transformation du système original
en un système triangulaire supérieur.
2. Résolution du système triangulaire
par substitution arrière.

### Remarques sur la méthode de Gauss
1. Un pivot est une valeur par laquelle on doit diviser
 pour résoudre le système linéaire.
2. On n’a pas utilisé la seconde opération élémentaire.
3. On peut aussi travailler avec la matrice augmentée.

## Résolution par la  méthode de Gauss-Jordan

En algèbre linéaire, l'élimination de Gauss-Jordan, aussi appelée méthode du pivot de Gauss, nommée en hommage à Carl Friedrich Gauss et Wilhelm Jordan, est un algorithme pour déterminer les solutions d'un système d'équations linéaires, pour déterminer le rang d'une matrice ou pour calculer l'inverse d'une matrice (carrée) inversible. Lorsqu'on applique l'élimination de Gauss à une matrice, on obtient sa forme échelonnée réduite.


L'algorithme de Gauss-Jordan produit la matrice échelonnée réduite d'une matrice à l'aide d'opérations élémentaires sur les lignes. 
Trois types d'opérations élémentaires sont utilisées :

* Échange de deux lignes 
* Multiplication d'une ligne par un scalaire non nul 
* Ajout du multiple d'une ligne à une autre ligne.

L'élimination de Gauss-Jordan peut résoudre un système d'équations AX = B, où A est une matrice n × m de rang r, B est un vecteur fixé, et X le vecteur inconnu. On crée un tableau à n lignes et m + 1 colonnes en bordant la matrice A par le vecteur B. On réduit la matrice sous forme échelonnée réduite.

Si les pivots de la matrice échelonnée réduite associée à (A|B) sont situés uniquement dans les m premières colonnes (ce qui est toujours le cas si r = n ) et ont pour indice de colonnes k1, …, kr , alors la dernière colonne fournit une solution particulière, obtenue en prenant tous ses termes nuls sauf ceux situés à la ligne d'indice ki et à qui on donne la valeur du terme situé à la ligne i de la dernière colonne, i variant de 1 à r.

On obtient la solution générale du système en ajoutant à cette solution particulière un élément quelconque du noyau de A. Celle-ci s'obtient en donnant des valeurs quelconques aux coefficients de X situés à un indice de ligne autre que les ki, et en déterminant les coefficients situés aux lignes d'indice ki de façon à satisfaire le système (ce qui est facile compte tenu de la forme échelonnée de la matrice).

* Si le dernier pivot de la matrice échelonnée réduite associée à (A|B) se situe dans la dernière colonne, alors il n'y a pas de solution.

* Si la matrice A est carrée inversible (autrement dit, le système est de Cramer), alors on obtient dans la dernière colonne l'unique solution X du système.

Variante : dans l'algorithme précédent, si on se borne à obtenir une matrice échelonnée (non réduite), on obtient une matrice triangulaire supérieure. Il ne reste plus qu'à « remonter » pour retrouver les valeurs des coefficients de X.

# Partie Pratique: 

Nous allons réaliser une interface Graphique permettant la résolution des systémes linéaires en se basant sur les éléments suivants:
- [PyQt 5](https://www.riverbankcomputing.com/software/pyqt/download5)
- [Python 3](https://www.python.org)
- [Qt Designer](doc.qt.io/qt-5/qtdesigner-manual.html)
- [SymPy](http://www.sympy.org/)
- ...
### QtPy5

C'est un module libre qui permet de lier le langage Python avec la bibliothèque Qt distribué sous deux licences : une commerciale et la GNU GPL. Il permet ainsi de créer des interfaces graphiques en Python. Une extension de Qt Creator (utilitaire graphique de création d'interfaces Qt) permet de générer le code Python d'interfaces graphiques.

### QTdesigner 


Qt Designer permet de créer graphiquement l’interface utilisateur ainsi que la gestion des évènements (signaux et
slots).il aide à créer une GUI (interface utilisateur graphique). nous pouvons donc  charger une interface graphique depuis Python.

# Conclustion et perspectives :

#### Méthode de Gauss Jordan
* fait disparaître les
coefficients en haut et en
bas de la diagonale.
* Pas de substitution arrière.

Pour terminer, il nous reste à parler d’une chose importante par rapport à la précision de la méthode Gauss-Jordan. Comme vous l’avez constaté, à chaque étape on divise l’équation par un nombre qu’on a appelé pivot. Et comme vous le savez une division est toujours dangereuse si on l’a fait avec un nombre très petit. Ça peut fausser complétement le résultat. Par conséquent, il faut toujours choisir le plus grand coefficient de la ligne comme pivot. Pour cela on peut librement changer l’ordre des équations de façon à placer dans la case pivot le plus grand nombre en valeur absolue. Autre chose, la méthode Gauss-Jordan peut aussi être utilisée pour trouver l’inverse d’une matrice. Pour cela, il suffit de poser la matrice en question côte à côte avec la matrice identité (A|I) et faire les transformations nécessaires pour arriver à (I|A-1). 
* La méthode est stable mais assez sensible aux erreurs de troncatures. Elle est aussi sensiblement plus lente que d’autres méthodes comme la LU décomposition.
## A FAIRE
- Ajouter des nouvelle méthode ( gauss seidel et jacobi ).
- Afficher par détail tous les étapes.

