# Babel

https://babeljs.io/docs/en/
https://medium.com/@onlykiosk/complete-babel-7-guide-for-beginners-in-2019-7dd78214c464

## Définition.


Babel gère la traduction de la syntaxe. Polyfill assiste Babel dans la gestion des fonctionnalités manquantes.

Un préréglage ou "Preset" contrôle la traduction de Babel.

deux concepts importants de Babel: le préréglage et le polyfill.


## Installation.

dans le terminal au niveau du projet.
```
npm install --save-dev @babel/core @babel/cli @babel/preset-env
npm install --save @babel/polyfill
```

Créer un fichier appelé babel.config.js
```
const presets = [
  [
      //preset
    "@babel/env",
    {
      targets: {
        edge: "17",
        firefox: "60",
        chrome: "67",
        safari: "11.1",
      },
      // inclue que les polyffill dont vous avez besoin
      useBuiltIns: "usage",
    },
  ],
];

module.exports = { presets };
```


Puis dans le terminal.
`./node_modules/.bin/babel src --out-dir lib`

ou
`npx babel src --out-dir lib`


## Require.

* de Javascript @babel/core :
```
const babel = require("@babel/core");

babel.transform("code", optionsObject);
```

* du terminal @babel/cli :
Afficher le reste des options acceptées par l'outil cli en l'exécutant --help. Mais le plus important pour nous en ce moment sont `--plugins` et `--presents`.


## Résumé

Tout peut être configuré sur mesure.

utiliser @babel/cli pour exécuter Babel depuis le terminal, @babel/polyfill pour "Polyfill" ou traduire toutes les nouvelles fonctionnalités JavaScript et le préréglage "Preset" `env` pour inclure uniquement les transformations et les polyfills des fonctionnalités que nous utilisons et qui manquent dans nos navigateurs cibles. 



