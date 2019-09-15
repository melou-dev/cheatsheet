# Array.

le tableau fait parti du type "objet", à la différence des autres objets il permet de garder des données de manière ordonnée.


## Déclaration.

```
let arr = new Array(); // peu utilisé, crée un nouvel array mais sans élément.
let arr = []; // le plus courant
```
on appelle un élément du tableau par son numéro à partir de 0.

```
let fruits = ["apple", "orange"];

return ( fruit[0] ); //apple
```


## Remplace un élément.

```
fruits[1] = "pear"; // now ["apple", "pear",]
```


## Ajoute un élément.

```
fruits[2] = "lemon"; // now ["apple", "pear", "lemon",]
```


## Compte le nombre d'éléments avec la propriété "lenght".

```
return( fruits.lenght ); // 3
```
pour une liste de boolean :
```
return array.filter(Boolean).length; // retourne le nombre de "true"
```
**ATTENTION** : si on marque manuellement un numéro inférieur au nombre d'éléments, le tableau sera réduit sans pouvoir revenir en arrière.


## montre tout les éléments du tableau.

```
return( fruits ); // apple,pear,lemon
```
**A SAVOIR** :
* un tableau peut garder des éléments de types différents.

* il est important de terminer chaque élément par un virgule **,**.


## Méthode "pop/push (rapide) & shift/unshift" (lente)

* <= shift (prendre l'élément index 0) // <= push (Ajouter un élément à la fin index -1)

* | pop (prendre l'élément à la fin index -1)
push |

FIFO
![explanation FIFO](https://upload.wikimedia.org/wikipedia/commons/thumb/5/52/Data_Queue.svg/300px-Data_Queue.svg.png)

LIFO
![explanation LIFO](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e1/Stack_%28data_structure%29_LIFO.svg/440px-Stack_%28data_structure%29_LIFO.svg.png)

**POP**
```
return( fruits.pop() ); // retire le dernier "limon" et alerte
```
**PUSH**
```
fruits.push("limon");
return( fruits ); // apple, pear, limon en rajoutant "limon"
```
 **A SAVOIR** : `fruits.push(...)` égale `fruits[fruits.lenght]`

**SHIFT**
 ```
 return( fruits.shift() ); // enlève "apple" et alerte
 ```

**UNSHIFT**
```
fruits.unshift("apple"); // remet l'élément
return( fruits ); // apple, pear, limon
```
**A SAVOIR** : Push & unshift peuvent ajouter plusieurs élément à la fois séparés par une virgule.


## Loops.

```
let arr = ["apple", "pear", "limon"];
```

**FOR** - boucle par index.
```
for (let i = 0; i < arr.lenght; i++) {
    return( arr[i] );
}
```

**FOR..OF** - boucle par élément - moderne et approprié.
```
 for (let fruit of fruits) {
     return( fruits );
 }
```

## un array dans un array.

```
let matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9],
];

return( matrix[1][1] ); // 5
```

## toString.

```
let arr = [1, 2, 3,];
return( arr ); 1,2,3
return( String(arr) === `1,2,3` ); // true
```

**A SAVOIR** : l'addition d'array concatène [1,2] + 3 // "1,23".



