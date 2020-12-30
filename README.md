# Projet-TP-analyse 
                                ****Résolution des systémes linéaires***

 
  
![Demo_projet](https://user-images.githubusercontent.com/57879341/103366327-a2c71900-4ac2-11eb-906a-6401b3320965.gif)

# Introduction 

Un système de m équations à n inconnues x1, x2, ...xn s’écrit sous forme matricielle : AX = B où A est une matrice comportant m lignes et n colonnes,
X est le vecteur colonne dont les composantes sont les xi et B , le second
membre, est aussi un vecteur colonne avec n composantes.
Le vecteur X est appelé solution du système.



# Partie Théorique: 


## Résolution par la méthode de Gauss
Le principe en est le suivant : par des combinaisons linéaires successives, on
transforme le système initial, que l’on prend tel quel sans changer l’ordre
des équations, en un système triangulaire supérieur, système ensuite résolu
en commençant par la dernière des équations transformées.
On rappelle qu’un système est dit triangulaire supérieur si la matrice associée est triangulaire supérieure.
Mise en œuvre de la méthode sur le système suivant :

2x1 + x2 + 4x3 = 9 (eq1)

x1 + x3 = 3 (eq2)

6x1 + 4x2 + 2x3 = 6 (eq3)

Dans la première étape de la méthode, on élimine l’inconnue x1 dans
les équations (eq2) et (eq3) en les combinant chacune à (eq1), celle-ci,
servant de ligne pivot, reste inchangée. Cela n’est possible que parce
que x1 apparaît dans (eq1). Si ce n’est pas le cas, il faut permuter
(eq1) avec la première des équations suivantes qui contient x1.
La méthode de Gauss remplace l’équation (eq2) par (eq2) − 1
2 (eq1) ,
mais pas (eq2) par 2(eq2) − (eq1), qui éliminerait aussi x1 mais ce qui
n’est plus Gauss.
De même, (eq3) est remplacée par (eq3)− 6
2 (eq1). Après cette première
étape, on obtient le système équivalent :

2x1 + x2 + 4x3 = 9

−1/2x2 − x3 = −3/2

x2 − 10x3 = −21
(eq1)
(eq2
0
)
(eq3
0
)
• Dans la deuxième étape, c’est la deuxième ligne qui joue le rôle de
ligne pivot si x2 est présent (sinon on permute (eq2
0
) avec (eq3
0
))
et, pour éliminer x2 dans la troisième ligne, on remplace celle-ci par
(eq3
0
) − 1
−1
2
(eq2
0
) soit (eq3
0
) + 2(eq2
0
). On obtient alors le système
équivalent, triangulaire supérieur, suivant :



2x1 + x2 + 4x3 = 9
− 1
2x2 − x3 = −3
2
− 12x3 = −24
(eq1)
(eq2
0
)
(eq3”)
• On résout le système par "remontée" en commençant par la dernière
équation.
(eq3”) donne x3 = 2 ,
(eq2
0
) donne −1
2x2 = −3
2 + x3 = 1
2 soit x2 = −1
(eq1) donne 2x1 = 9 − x2 − 4x3 =9+1 − 4 ∗ 2=2 d’où x1 = 1 et la
solution unique X =


1
−1
2

.
Par la suite, les systèmes seront résolus par cette méthode. Pour n
équations, il y aura n − 1 étapes.




## Résolution par la  méthode de Gauss-Jordan

En algèbre linéaire, l'élimination de Gauss-Jordan, aussi appelée méthode du pivot de Gauss, nommée en hommage à Carl Friedrich Gauss et Wilhelm Jordan, est un algorithme pour déterminer les solutions d'un système d'équations linéaires, pour déterminer le rang d'une matrice ou pour calculer l'inverse d'une matrice (carrée) inversible. Lorsqu'on applique l'élimination de Gauss à une matrice, on obtient sa forme échelonnée réduite.


L'algorithme de Gauss-Jordan produit la matrice échelonnée réduite d'une matrice à l'aide d'opérations élémentaires sur les lignes. 
Trois types d'opérations élémentaires sont utilisées :

*Échange de deux lignes ;
*Multiplication d'une ligne par un scalaire non nul ;
*Ajout du multiple d'une ligne à une autre ligne.

L'élimination de Gauss-Jordan peut résoudre un système d'équations AX = B, où A est une matrice n × m de rang r, B est un vecteur fixé, et X le vecteur inconnu. On crée un tableau à n lignes et m + 1 colonnes en bordant la matrice A par le vecteur B. On réduit la matrice sous forme échelonnée réduite.

Si les pivots de la matrice échelonnée réduite associée à (A|B) sont situés uniquement dans les m premières colonnes (ce qui est toujours le cas si r = n ) et ont pour indice de colonnes k1, …, kr , alors la dernière colonne fournit une solution particulière, obtenue en prenant tous ses termes nuls sauf ceux situés à la ligne d'indice ki et à qui on donne la valeur du terme situé à la ligne i de la dernière colonne, i variant de 1 à r.

On obtient la solution générale du système en ajoutant à cette solution particulière un élément quelconque du noyau de A. Celle-ci s'obtient en donnant des valeurs quelconques aux coefficients de X situés à un indice de ligne autre que les ki, et en déterminant les coefficients situés aux lignes d'indice ki de façon à satisfaire le système (ce qui est facile compte tenu de la forme échelonnée de la matrice).

* Si le dernier pivot de la matrice échelonnée réduite associée à (A|B) se situe dans la dernière colonne, alors il n'y a pas de solution.

* Si la matrice A est carrée inversible (autrement dit, le système est de Cramer), alors on obtient dans la dernière colonne l'unique solution X du système.

Variante : dans l'algorithme précédent, si on se borne à obtenir une matrice échelonnée (non réduite), on obtient une matrice triangulaire supérieure. Il ne reste plus qu'à « remonter » pour retrouver les valeurs des coefficients de X.
