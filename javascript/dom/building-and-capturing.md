# Délégation d'évènements - Bubbling & Capturing.

https://javascript.info/bubbling-and-capturing

dans le dom, un modèle de gestion d'événements extrêmement puissant existe sur lequel on peut agir en fonction de l'objectif à atteindre suite à une intéraction avec un utilisateur.

**A SAVOIR**

L'évènement se propage toujours du haut (windows) vers le bas, élément cliqué. Puis du bas, élément cliqué vers le haut.

![eventflow sheme](https://raw.githubusercontent.com/melou-dev/cheatsheet/master/javascript/dom/images/eventflow.png)

Les évènements standard du DOM décrivent 3 phases de propagation :

1. Capturing – l'évènement se propage de haut en bas jusqu'à l'élément. rarement utilisé car invisible pour nous.

2. Target  – l'évènement atteind l'élément ciblé.

3. Bubbling phase – l'évènement remonte "bubble" de bas en haut depuis l'élément ciblé.

C'est-à-dire que pour un clic sur <td>, l'événement passe d'abord par les ascendants jusqu'à l'élément (phase de capture ou "capturing"), puis il atteint la cible et s'y déclenche (phase cible ou "target"), puis il remonte (phase de bullage ou "bubbling").

Grâce à ça on pourra placer, un gestionnaire d'évènement "Handler" sur un ascendant et l'interaction se propager sur sa descendance sans devoir assigner des "Handler" sur chaque descendant qui peuvent être nombreux, dans le cas d'une liste, d'un tableau ou de plusieurs boutons d'un menu par exemple.


## bubbling.

![Bubbling scheme](https://raw.githubusercontent.com/melou-dev/cheatsheet/master/javascript/dom/images/bubbling.png)



### différence entre élément **event.target** & **this** .

lorqu'un évènement, tel qu'un "élément.onclick", arrive :

  * **event.target** - cible l'élément choisi(l'élément de l'évènement ou des descendants) sans bubbling.

  * **this** - cible uniquement l'élément ou l'évènement est placé. si on clic sur un descendant c'est l'élément qui sera ciblé.


### Stop bubbling.

Il n’y a généralement aucun besoin réel d’empêcher la formation de bulles. Une tâche qui semble le nécessiter peut être résolue par d’autres moyens. 

si toutefois, on souhaite éviter la propagation de l'évènement jusqu'au HTML, puis document, puis windows : 

```
<body onclick="alert(`the bubbling doesn't reach here`)">
  <button onclick="event.stopPropagation()">Click me</button>
</body>
```

**event.stopImmediatePropagation()** - si plusieurs "handlers" sur un même élément.



## des modèles de comportement "behavior pattern".

Nous pouvons également utiliser la délégation d’événements pour ajouter des «comportements» aux éléments de manière déclarative, avec des attributs et des classes spéciaux.

* **data-counter** - compteur de point
* **data-toggle-id="idname"** - faire apparaître et disparaître des éléments.


## Conclusion

outil intéressant en JS :

* **les +** :
w up correctly.
- gain de temps car moins de code.

- gain de d'espace mémoire.

- Possibilité de changer les éléments sans changer le code.


* **les -** : 

- Il y a des exceptions comme l'évènement "focus" sans bubbling.

- Attention à l'utilisation du event.stopImmediatePropagation().

- La performance du CPU mais c'est négligeable.



