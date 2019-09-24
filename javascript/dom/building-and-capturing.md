# Bubbling & Capturing.

est un modèle de «délégation d'événements», un modèle de gestion d'événements extrêmement puissant.

https://javascript.info/bubbling-and-capturing

![eventflow sheme](https://raw.githubusercontent.com/melou-dev/cheatsheet/master/javascript/dom/images/eventflow.png)

Les évènements standard du DOM décrivent 3 phases de propagation :

1. Capturing – l'évènement se propage de haut en bas jusqu'à l'élément. rarement utilisé car invisible pour nous.

2. Target  – l'évènement atteind l'élément ciblé.

3. Bubbling phase – l'évènement remonte "bubble" de bas en haut depuis l'élément ciblé.

C'est-à-dire que pour un clic sur <td>, l'événement passe d'abord par les ascendants jusqu'à l'élément (phase de capture ou "capturing"), puis il atteint la cible et s'y déclenche (phase cible ou "target"), puis il remonte (phase de bullage ou "bubbling").

La propriété d'objet évènement suivant sert à déterminer dans quelle phase on se trouve.
**event.eventPhase** – la phase courant (capturing=1, target=2, bubbling=3).


## bubbling.

lorsqu'un évènement arrive sur un élément, l'évènement se propage au parent et ascendants.

![Bubbling scheme](https://raw.githubusercontent.com/melou-dev/cheatsheet/master/javascript/dom/images/bubbling.png)

il y a des exceptions comme l'évènement "focus".


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




