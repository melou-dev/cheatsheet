# Bubbling & Capturing.

https://javascript.info/bubbling-and-capturing


## bubbling.

lorsqu'un évènement arrive sur un élément, l'évènement se propage au parent et ascendants.

![Bubbling scheme](https://raw.githubusercontent.com/melou-dev/cheatsheet/master/javascript/dom/images/bubbling.png)

il y a des exceptions comme l'évènement "focus".


### différence entre élément **event.target** & **this** .

lorqu'un évènement, tel qu'un "élément.onclick", arrive :

  * **event.target** - cible l'élément choisi(l'élément de l'évèvement ou des descendants) sans bubbling.

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


## Capturing.


