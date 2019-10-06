# Paramètres de reste et operateurs étendus.

## Paramètre restes "..."

Permet d'obtenir une array à partir d'une liste de paramètres.

args est le nom de l'array. **...nomdel'array**
```
function sumAll(...args) {
  let sum = 0;

  for (let arg of args) sum += arg;

  return sum;
}

return ( sumAll(1, 2, 3) ); // 6
```

titles est le nom de l'array. **Il est toujours à la fin**.
```
function showName(firstName, lastName, ...titles) {
  alert( firstName + ' ' + lastName ); // Julius Caesar

  // le reste des arguments sont mis dans l'array "titles"
  // i.e. titles = ["Consul", "Imperator"]
  alert( titles[0] ); // Consul
  alert( titles[1] ); // Imperator
  alert( titles.length ); // 2
}

showName("Julius", "Caesar", "Consul", "Imperator");
```

L'ancienne méthode est un array-like appelé **arguments**.


## Opérateurs étendues ou SPREAD OPERATOR.

D'un array, les arguments sont transformés en liste ce qui permet d'appliqué des méthodes d'objet.

```
let arr = [3, 5, 1];

alert( Math.max(arr) ); // NaN
```

```
let arr = [3, 5, 1];

alert( Math.max(...arr) ); // 5
```

Multiples itérables combinés avec de simples arguments.

```
let arr1 = [1, -2, 3, 4];
let arr2 = [8, 3, -8, 1];

alert( Math.max(1, ...arr1, 2, ...arr2, 25) ); // 25
```

REST et SPREAD se combinent.

```
let arr = [3, 5, 1];
let arr2 = [8, 9, 15];

let merged = [0, ...arr, 2, ...arr2];

alert(merged); // 0,3,5,1,2,8,9,15
```

Un string étant itérable, on peut lui applique le **"SPREAD"**

