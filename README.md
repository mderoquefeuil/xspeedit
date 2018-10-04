XspeedIt
========

XspeedIt est une société d'import / export ayant robotisé toute sa chaîne d'emballage de colis.  
Elle souhaite trouver un algorithme permettant à ses robots d'optimiser le nombre de cartons d'emballage utilisés.

Les articles à emballer sont de taille variable, représentée par un entier compris entre 1 et 9.  
Chaque carton a une capacité de contenance de 10.  
Ainsi, un carton peut par exemple contenir un article de taille 3, un article de taille 1, et un article de taille 6.

La chaîne d'articles à emballer est représentée par une suite de chiffres, chacun représentant un article par sa taille.  
Après traitement par le robot d'emballage, la chaîne est séparée par des "/" pour représenter les articles contenus dans un carton.

*Exemple*  
```python
Chaîne d'articles en entrée : 163841689525773  
Chaîne d'articles emballés  : 163/8/41/6/8/9/52/5/7/73
```

L'algorithme actuel du robot d'emballage est très basique.  
Il prend les articles les uns après les autres, et les mets dans un carton.  
Si la taille totale dépasse la contenance du carton, le robot met l'article dans le carton suivant.

Objectif
--------

Implémenter une application qui permettrait de maximiser le nombre d'articles par carton.
L'ordre des cartons et des articles n'a pas d'importance.

*Exemple*  
```python
Articles      : 163841689525773  
Robot actuel  : 163/8/41/6/8/9/52/5/7/73 => 10 cartons utilisés  
Robot optimisé: 163/82/46/19/8/55/73/7   => 8  cartons utilisés
```

Spécifications
-----------

Afin d'évaluer plus précisément vos compétences, vous utiliserez la stack suivante : 
- Backend : Java 8+ et Spring Boot 1.5+ (les deux ensemble)
- Frontend : Angular 4+, React 16+ ou VueJS 2+ (un seul des trois)

Nous évaluerons la qualité de l'algorithme (complexité, lisibilité, efficacité) mais aussi l'implémentation de sa résolution (attention aux tests !)
Afin d'exploiter ce service, nous souhaitons pouvoir exploiter la solution sous forme d'une API Rest. Si nous tenons à pouvoir trier les cartons, tout autre service qui vous semble pertinent peut être ajouté à la solution.
Enfin, afin de faciliter l'usage de l'application d'un point de vue interne, une IHM doit être mise en place. Pour rester moderne, l'IHM devra être réalisée avec Angular (version 4 ou plus), React (version 16 ou plus) ou VueJS (version 2 ou plus).

Attention à ne pas brûler les étapes, une solution montée avec SpringBoot et Angular n'a aucune valeur si les cartons ne sont pas triés convenablement ou que la solution n'est pas utilisable car trop complexe à exploiter.
