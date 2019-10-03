# RECURSION & STACK

La fonction s'appelle elle-même.

```
function pow(x, n) {
  if (n == 1) {
    return x;
  } else {
    return x * pow(x, n - 1);
  }
}
```
```
function pow(x, n) {
  return (n == 1) ? x : (x * pow(x, n - 1));
}
```

même résultat que la loop

```
function pow(x, n) {
  let result = 1;

  for (let i = 0; i < n; i++) {
    result *= x;
  }

  return result;
}
```

![recursion sheme](images/recursion-pow.svg)

Quand un fonction fait un appel imbriqué, il ce passe ceci.

* la fonction courante est stoppée.
* Le contexte d'exécution qui lui est associé est mémorisé dans une structure de données spéciale appelée pile de contexte d'exécution (STACK)
* l'appel imbriqué (fonction dans la fonction) est exécuté.
* A la fin, l'ancien contexte d'exécution est extrait de la pile et la fonction externe reprend à l'endroit où elle s'est arrêtée.

## Recursive Transversal.

comme un arbre - stucture d'une entreprise

exemples :

![recursive transversal example](images/recursive-tranversal.png)


## Factorial.

![Factorial exemple](images/javascript-recursion-function-image-exercise-1.png)
