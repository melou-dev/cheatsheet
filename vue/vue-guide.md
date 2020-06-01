# VUE

## Start with vue.

Créer 3 fichiers depuis le terminal.
`touch index.html index.css index.js`

ds HTLM

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
  </head>
  <body>
    <div id="app">{{ message }}</div>

    <script src="index.js"></script>

  </body>
</html>
```

ds js

```
"use strict";

var app = new vue({
  el: "app",
  data: {
    message: "hello vue!"
  }
});
```
