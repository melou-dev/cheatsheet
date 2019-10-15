# Scheduling with setTimeout et setInterval.

Ceux sont des méthodes pour programmer une fonction dans le temps.

* `setTimeout(func, delay, args)` : une fois
* `setInterval(func, delay, args)` : plusieurs fois régulièrement. Plus de 5 fois, interval de 4ms
* `setTimeout(func, delay, args)` : plusieurs fois précisement. Plus de 5 fois, interval de 4ms

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
* battery de l'ordi,
* paramètres de l'ordinateur,
* navigateur etc...


## Annuler

clearTimeout / clearInternal

```
let timerId = setTimeout(...);
clearTimeout(timerId);
```

## Programmation immédiate = Zero delay

Programmer de lancer la fonction immédiatement après le script en cours soit complété.

`setTimeout(func, 0)`

