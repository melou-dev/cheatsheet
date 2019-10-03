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
