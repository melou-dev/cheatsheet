# Fonction objet, NFE.

Les fonctions sont des objets.

Fonction déclaration (collecté (hoisted) en global et peut être appelé à tout moment) : `function functionname() {}`
Fonction expression (dans un variable, executé au moment de son expression) : `let a = function () {}` 
NFE, Named Function Expression (comme ci-dessous mais elle est nommée) : `let b = function functionname() {}`


## Propriétés

* **name** : normalement indiquée après function mais étant optionnel, s'il aucun nom n'a été donné, Javascript tente de le deviner.


* **lenght** : compte le nombre d'argument mais pas lorqu'ils sont écris en reste "...".


## Avantages

Les fonctions peuvent porter des propriétés supplémentaires. Cette caractéristique est bien connue des librairies JavaScript.

Elles proposent un fonction principale et attachent de nombreuses fonctions utile à l'intérieur et ainsi évitent des conflits.
nom de la fonction jQuery => $
nom des fonctions lodash => _, _.clone, _.keyBy

