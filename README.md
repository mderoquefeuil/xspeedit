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

La solution proposée sera évaluée selon trois critères successifs :

1. La résolution de l'algorithme - en tenant compte de la qualité du code (complexité, lisibilité, efficacité) mais aussi de sa robustesse (attention aux tests, à la documentation, ...)

2. Afin d'exploiter efficacement ce service, une API Rest doit être mise en place (s'appuyer sur spring boot). Si le service principal est le rangement des articles dans des boites, n'hésitez pas à ajouter d'autres services qui vous sembleraient pertinents.

3. Enfin, la mise en place d'une IHM est souhaité pour traiter efficacement ce rangement par des individus non techniques. Réalisez une interface avec un framework JS (Angular, React ou Vue) répondant à ce besoin.

Attention à bien respecter l'ordre, développer une IHM si l'API Rest ne fonctionne pas est inutile. De même, réaliser l'API Rest si l'algorithme ne résoud pas bien le problème ne sert à rien. Si vous ne vous sentez pas en mesure de réaliser l'étape 2 ou 3 dans un laps de temps suffisant, concentrez vos efforts sur la ou les étapes que vous pouvez atteindre. Un code plus réduit mais de bonne qualité sera toujours mieux considéré qu'un code plus ample mais incorrect, invalide ou dur à relire.

Pensez également bien à tester votre code (et à nous montrer que vous l'avez testé) ! Un code dont on ne peut garantir la qualité est un code inutile car peu ou pas fiable.
