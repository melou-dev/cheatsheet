# dotenv-extended

Dotenv est un module indépendant qui charge les variables d'environnement dans des fichiers .env. Le stockage de la configuration dans l'environnement distinct du code est basé sur la méthodologie de l'application "Twelve-Factor".

Les applications 12 facteurs stockent la configuration dans des variables d’environnement (souvent raccourcies en variables d’env, ou env). 

# installation.

Dans le terminal :
`npm i --save dotenv-extended`


Dans le fichier js principal :

`require('dotenv-extended').load();`

puis création d'un fichier .env contenant les variables "NAME=VALUE"

par exemple : 

```
MONGO_HOST=localhost
MONGO_DATABASE=TestDB
MONGO_USER=dbusername
MONGO_PASS=dbpassword!
```

