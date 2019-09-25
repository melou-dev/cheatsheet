# MAP - WEAKMAP - SET - WEAKSET

- **Object** : ranger des données avec les clefs de type string.
- **Array** : ranger des données de manière ordonnée indexer à partir de l'index 0.
- **Map** : ranger des données de manière ordonnée par ordre d'arrivée avec des clefs de tous les types (string, number, boolean, object etc...)
- **WeakMap** - ranger des données [clefs, valeurs] temporairement, les clefs sont uniquement des objets.
- **set** : ranger des données sans clefs,de manière ordonnée par ordre d'arrivée, mode de rangement à donnée unique non duplicable. si deux données identiques la 2ème écrase la 1ère.
- **Weakset** - ranger des données [valeurs] temporairement, les valeurs sont uniquements des objets

## MAP - méthodes et propriété.

### Méthodes.

**new Map([iterable])** – créer une **map** avec option iterable (e.g. array) d'une paire [key,value].

**map.set(key, value)** – stocker une valeur avec sa clef.

**map.get(key)** – retourner la donnée en appelant sa clef, "undefined" si la clef n'existe pas.

**map.has(key)** – boolean, retourne "true" si la clef existe, sinon "false".

**map.delete(key)** – supprimer la valeur en appelant sa clef.

**map.clear()** – supprimer toutes les données et clefs de la "map".


### propriété.

**map.size** – retourne le nombre d'éléments [key,value].


## Set - méthodes et propriété.

### Méthodes.

**new Set([iterable])**  – créer un **set** de données avec option iterable (e.g. array).

**set.add(value)** – ajouter une donnée (ne fait rien si la donnée existe) et retourne le "set".

**set.delete(value)** – supprimer la donnée et  retouner en boolean "true si la donnée et existe, sinon "false".

**set.has(value)** – retourner en boolean "true si la donnée et existe, sinon "false".

**set.clear()** – supprimer toutes les données du set.

### Propriété.

**set.size** – compter les données du "set".


## Méthodes d'Iteration.

**map.keys()** & **set.key()** – retourner les clefs.

**map.values()** & **set.values** – retourner les valeurs.

**map.entries()** & **set.entries** – retourner un iterable par [key, value] et [value, value].

```
let recipeMap = new Map([
  ['cucumber', 500],
  ['tomatoes', 350],
  ['onion',    50]
]);

// iterater par la clef.
for (let vegetable of recipeMap.keys()) {
  alert(vegetable); // cucumber, tomatoes, onion
}

// iterater par les valeurs.
for (let amount of recipeMap.values()) {
  alert(amount); // 500, 350, 50
}

// iterate par [key, value].
for (let entry of recipeMap) { // the same as of recipeMap.entries()
  alert(entry); // cucumber,500 (and so on)
}
```

```
let set = new Set(["oranges", "apples", "bananas"]);

for (let value of set) alert(value);

// the same with forEach:
set.forEach((value, valueAgain, set) => {
  alert(value);
});
```

## **Object.entries: "Map" à partir d'"Object"** vs **Object.fromEntries: "Object" à partir de "Map"**.

**Object.entries(obj)**
```
let obj = {
  name: "John",
  age: 30
};

let map = new Map(Object.entries(obj));

alert( map.get('name') ); // John
```

**Object.fromEntries(map)**
```
let prices = Object.fromEntries([
  ['banana', 1],
  ['orange', 2],
  ['meat', 4]
]);

// now prices = { banana: 1, orange: 2, meat: 4 }

alert(prices.orange); // 2
```


## WeakMap - WeakSet

Non interable

**weakMap/Set.get(key)**
**weakMap/Set.set(key, value)**
**weakMap/Set.delete(key)**
**weakMap/Set.has(key)**

