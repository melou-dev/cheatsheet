# héritage prototypal

http://javascript.info/prototype-inheritance

En JavaScript, tous les objects ont une propriété caché appelé **[[Prototype]]**

on l'appelle par `obj.__proto__`

Si on veut lire la propriété d'un objet ou appeler une méthode et qu'elle n'existe pas, JavaScript essaie de le trouver dans le prototype.

Ecrire ou supprimer des opérations agit directement sur l'objet et n'utilise pas le prototype.
(assuming it’s a data property, not a setter).?????

If we call obj.method(), and the method is taken from the prototype, this still references obj. So methods always work with the current object even if they are inherited ???? 

`for..in` boucle ses propres propriétés et celles en héritage. Toutes les autres méthodes pour obtenir la clef ou la valeur opère dans l'objet lui-même.

```
let head = {
  glasses: 1
};

let table = {
  pen: 3,
  __proto__: head
};

let bed = {
  sheet: 1,
  pillow: 2,
  __proto__: table
};

let pockets = {
  money: 2000,
  __proto__: bed
};

alert( pockets.pen ); // 3
alert( bed.glasses ); // 1
alert( table.money ); // undefined
```

