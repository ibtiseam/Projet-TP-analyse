# Projet-TP-analyse 
                                ****Résolution des systémes linéaires***

  * Ce projet represente une tentative pour  faciliter la résolution des systémes linéaires. 
  
![Demo_projet](https://user-images.githubusercontent.com/57879341/103366327-a2c71900-4ac2-11eb-906a-6401b3320965.gif)

## Méthodes couvertes

1. Méthode Elimenation de Gauss
2. Méthode de Gauss-Jordan

* En algèbre linéaire, l'élimination de Gauss-Jordan, aussi appelée méthode du pivot de Gauss, nommée en hommage à Carl Friedrich Gauss et Wilhelm Jordan, est un algorithme pour déterminer les solutions d'un système d'équations linéaires, pour déterminer le rang d'une matrice ou pour calculer l'inverse d'une matrice (carrée) inversible. Lorsqu'on applique l'élimination de Gauss à une matrice, on obtient sa forme échelonnée réduite.


L'algorithme de Gauss-Jordan produit la matrice échelonnée réduite d'une matrice à l'aide d'opérations élémentaires sur les lignes. Trois types d'opérations élémentaires sont utilisées :

Échange de deux lignes ;
Multiplication d'une ligne par un scalaire non nul ;
Ajout du multiple d'une ligne à une autre ligne.
Exemple.

On part de la matrice

{\displaystyle \mathrm {A} ={\begin{pmatrix}2&-1&0\\-1&2&-1\\0&-1&2\end{pmatrix}}}{\mathrm  {A}}={\begin{pmatrix}2&-1&0\\-1&2&-1\\0&-1&2\end{pmatrix}}
Il s'agit d'une matrice réelle, donc le module d'un coefficient est sa valeur absolue.

Première itération, j = 1 (et r = 0) :
étape 1.1 : on cherche dans la première colonne de la matrice la valeur maximale des valeurs absolues des coefficients. Elle vaut 2, située en (1, 1), de sorte que k = 1,
étape 1.2.1 : r = 1,
étape 1.2.2 : r = k, il n'y a pas d'échange,
étape 1.2.3 : on divise la ligne 1 par A(1, 1) = 2, soit {\displaystyle {\begin{pmatrix}1&-1/2&0\end{pmatrix}}}{\begin{pmatrix}1&-1/2&0\end{pmatrix}},
étape 1.2.4 :
ligne i = 2, on a A(2, 1) = -1 ; on calcule
{\displaystyle {\begin{pmatrix}-1&2&-1\end{pmatrix}}-(-1)\times {\begin{pmatrix}1&-1/2&0\end{pmatrix}}={\begin{pmatrix}0&3/2&-1\end{pmatrix}}}{\begin{pmatrix}-1&2&-1\end{pmatrix}}-(-1)\times {\begin{pmatrix}1&-1/2&0\end{pmatrix}}={\begin{pmatrix}0&3/2&-1\end{pmatrix}},
ligne i = 3, on a A(3, 1) = 0, la ligne n'est donc pas modifiée,
la matrice est alors
{\displaystyle \mathrm {A} '={\begin{pmatrix}1&-1/2&0\\0&3/2&-1\\0&-1&2\end{pmatrix}}}{\mathrm  {A}}'={\begin{pmatrix}1&-1/2&0\\0&3/2&-1\\0&-1&2\end{pmatrix}} ;
deuxième itération, j = 2 (et r = 1) :
étape 2.1 : on cherche dans les lignes 2 à 3 de la deuxième colonne la valeur maximale en valeur absolue. Il s'agit de 3/2, situé en (2, 2),
étape 2.2.1 : r = 2,
étape 2.2.2 : r = k, il n'y a pas d'échange.
étape 2.2.3 : on divise la ligne 2 par A'(2, 2) = 3/2, soit {\displaystyle {\begin{pmatrix}0&1&-2/3\end{pmatrix}}}{\begin{pmatrix}0&1&-2/3\end{pmatrix}},
étape 2.2.4 :
ligne i = 1, on a A'(1, 2) = -1/2 ; on calcule
{\displaystyle {\begin{pmatrix}1&-1/2&0\end{pmatrix}}-(-1/2)\times {\begin{pmatrix}0&1&-2/3\end{pmatrix}}={\begin{pmatrix}1&0&-1/3\end{pmatrix}}}{\begin{pmatrix}1&-1/2&0\end{pmatrix}}-(-1/2)\times {\begin{pmatrix}0&1&-2/3\end{pmatrix}}={\begin{pmatrix}1&0&-1/3\end{pmatrix}},
ligne i = 3, on a A'(3, 2) = -1 ; on calcule
{\displaystyle {\begin{pmatrix}0&-1&2\end{pmatrix}}-(-1)\times {\begin{pmatrix}0&1&-2/3\end{pmatrix}}={\begin{pmatrix}0&0&4/3\end{pmatrix}}}{\begin{pmatrix}0&-1&2\end{pmatrix}}-(-1)\times {\begin{pmatrix}0&1&-2/3\end{pmatrix}}={\begin{pmatrix}0&0&4/3\end{pmatrix}},
la matrice est alors
{\displaystyle \mathrm {A} ''={\begin{pmatrix}1&0&-1/3\\0&1&-2/3\\0&0&4/3\end{pmatrix}}}{\mathrm  {A}}''={\begin{pmatrix}1&0&-1/3\\0&1&-2/3\\0&0&4/3\end{pmatrix}} ;
troisième itération, j = 3 (et r = 2) :
étape 3.1 : le pivot de la troisième colonne, troisième ligne est 4/3. Donc k = 3
étape 3.2.1 : r = k,
étape 3.2.2 : il n'y a aucune ligne à permuter,
étape 3.2.3 : on divise la ligne 3 par A''(3, 3) = 4/3, elle devient {\displaystyle {\begin{pmatrix}0&0&1\end{pmatrix}}}{\begin{pmatrix}0&0&1\end{pmatrix}}
étape 3.2.4 :
ligne i = 1, on a A''(1, 3) = -1/3. La dernière étape annule ce coefficient.
ligne i = 2, on a A''(2, 3) = -2/3. La dernière étape annule ce coefficient.
la matrice est alors
{\displaystyle \mathrm {A} '''={\begin{pmatrix}1&0&0\\0&1&0\\0&0&1\end{pmatrix}}}{\mathrm  {A}}'''={\begin{pmatrix}1&0&0\\0&1&0\\0&0&1\end{pmatrix}} qui est réduite échelonnée
