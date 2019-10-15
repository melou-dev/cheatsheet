# Scheduling with setTimeout et setInterval.

Ceux sont des méthodes pour programmer une fonction dans le temps.

* `setTimeout(func, delay, args)` : une fois
* `setInterval(func, delay, args)` : plusieurs fois régulièrement.
* `setTimeout(func, delay, args)` : plusieurs fois précisement.

```
/* instead of:
let timerId = setInterval(() => alert('tick'), 2000);
*/

let timerId = setTimeout(function tick() {
  alert('tick');
  timerId = setTimeout(tick, 2000);
}, 2000);
```
## Delay

delay en milliseconds ms 1000 = 1s

pas exact, processus peut être ralenti ou accéléré pour des questions de performance :
* activité du CPU,
* batterie de l'ordi,
* configuration de l'ordinateur,
* navigateur etc...


## Annuler

clearTimeout / clearInternal

```
let timerId = setTimeout(...);
clearTimeout(timerId);
```

## Programmation immédiate = Zero delay

Permet de lancer la fonction immédiatement après que le script en cours soit terminé.

`setTimeout(func, 0)`

dans le cas de plusieurs appels, alors au bout de 5 fois, il y a un interval de 4 ms.

