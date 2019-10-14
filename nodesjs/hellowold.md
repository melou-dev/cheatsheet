# Créer un serveur Node.js

https://nodejs.org/en/docs/guides/getting-started-guide/

## installer node js

`npm outdated` voir si bonne version.

`npm install -g npm`



Vérifier si à jour
```
(async (a = 1, ...b) => ({...b, a, [a]: `${a}`}))();
​// New Promise APIs
require('util').promisify;
require('fs').promises;
```

## créer un fichier app.js

une fois node installer, créer votre serveur web.

créer un fichier nommé **`app.js`**.

copier/coller le code suivant


```
const http = require('http'); // demande d'importer le HTTP module.

const hostname = '127.0.0.1'; // l'adresse du serveur dans des variables
const port = 3000;

const server = http.createServer((req, res) => { // la méthode http.createServer() crée un objet serveur HTTP.
  res.statusCode = 200; // HTTP 200 signifie que la transmission est OK au niveau du http.
  res.setHeader('Content-Type', 'text/plain'); // set = écrit un header type texte
  res.end('Hello World\n'); // renvoit la réponse à l'utilisateur.
});

// appel la fonction ci-dessus.
server.listen(port, hostname, () => {
  console.log(`Server running at http://${hostname}:${port}/`);
});
```

En détail et en Anglais.
```
//Node.js has a built-in module called HTTP, which allows Node.js 
//to transfer data over the Hyper Text Transfer Protocol (HTTP).
//To include the HTTP module, use the require() method:
const http = require('http');

// variables
const hostname = '127.0.0.1';
const port = 3000;

//create a server object:
// The http.createServer() method turns your computer into an HTTP server.
// The http.createServer() method creates an HTTP Server object.
const server = http.createServer((req, res) => { // request, response
  res.statusCode = 200; // HTTP 200 means transmission is OK on the http level.
  //res.setHeader() is a native method of Node.js and res.header()
  // is an alias of res.set() method from Express framework.
  // ... The only difference is res.setHeader() allows you only to set a singular header and 
  // res.header() will allow you to set multiple headers.
  res.setHeader('Content-Type', 'text/plain');
  res.end('Hello World\n'); //write a response to the client "Hello World" and go to next line and end the response //
});

//the server object listens on port to show "Hello World"
// The HTTP Server object can listen to ports on your computer and execute
// a function, a requestListener, each time a request is made.
server.listen(port, hostname, () => {
  console.log(`Server running at http://${hostname}:${port}/`);
});
```

## Lancer le serveur

dans le terminal lancer `node app.js`

le console.log s'affiche.

Visiter http://localhost:3000

Pour voir le 

**Hello World** s'afficher.