# Projet-TP-analyse 
  * Ce projet represente une tentative peremttant de comprendre et faciliter la résolution des systémes linéaires. 
  
![Demo_projet](https://user-images.githubusercontent.com/57879341/103366327-a2c71900-4ac2-11eb-906a-6401b3320965.gif)

## Méthodes couvertes

1. Méthode Elimenation de Gauss
2. Méthode de Gauss-Jordan

* En algèbre linéaire, l'élimination de Gauss-Jordan, aussi appelée méthode du pivot de Gauss, nommée en hommage à Carl Friedrich Gauss et Wilhelm Jordan, est un algorithme pour déterminer les solutions d'un système d'équations linéaires, pour déterminer le rang d'une matrice ou pour calculer l'inverse d'une matrice (carrée) inversible. Lorsqu'on applique l'élimination de Gauss à une matrice, on obtient sa forme échelonnée réduite.
@@ -35,11 +35,4 @@ Si la matrice A est carrée inversible (autrement dit, le système est de Cramer
Variante : dans l'algorithme précédent, si on se borne à obtenir une matrice échelonnée (non réduite), on obtient une matrice triangulaire supérieure. Il ne reste plus qu'à « remonter » pour retrouver les valeurs des coefficients de X.


## Méthode de Gauss-Seidel : 
*La méthode de Gauss-Seidel est une méthode itérative de résolution d'un système linéaire (de dimension finie) de la forme {\displaystyle Ax=b}Ax=b, ce qui signifie qu'elle génère une suite qui converge vers une solution de cette équation, lorsque celle-ci en a une et lorsque des conditions de convergence sont satisfaites (par exemple lorsque {\displaystyle A}A est symétrique définie positive). L'algorithme suppose que la diagonale de {\displaystyle A}A est formée d'éléments non nuls.

** La méthode se décline en une version « par blocs ».

*** Le principe de la méthode peut s'étendre à la résolution de systèmes d'équations non linéaires et à l'optimisation, mais avec des conditions d'efficacité moins claires. En optimisation, l'utilité de cette approche dépendra beaucoup de la structure du problème. Le principe gauss-seidelien permet aussi d'interpréter d'autres algorithmes.
