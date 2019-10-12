# DEPLOYER UN PROJET VUE CLI SUR GITHUB


## Créer un nouveau projet avec vue

C'est du déjà vue.

## Créer un repo sur GitHub

C'est du déjà vue.

Attention!! ne pas créer la Git Hub pages manuellement. La source doit rester en "NONE".

![GitHub Pages](https://github.com/melou-dev/cheatsheet/blob/master/vue/images/github-pages.png)

Depuis le terminal dans le projet vue.
```
git remote add origin git@github.com:githubname/reponame.git
git push -u origin master
```

## Ouvrir le projet

avec `code .` ou `vim .` dans le terminal


## Ouvrir .gitignore

* ouvrir le fichier **.gitignore**
* desactiver la ligne / dist en mettant un **#** devant.

![screenshot .gitignore](https://github.com/melou-dev/cheatsheet/commit/41c521243cf054438339a9a81ea0b07738e41e1b)


## Créer vue.config.js

Créer un fichier **vue.config.js** depuis vscode ou vim.
copier/coller le code ci-dessous et remplacer `myproject` par le nom de votre repo GitHub.

```
module.exports = {
  publicPath: process.env.NODE_ENV === 'production'
    ? '/my-project/'
    : '/'
}
```

![screenshot vue.config.js](https://github.com/melou-dev/cheatsheet/commit/23839ee62e3d6c666d53ce66bb033d070c183dfe)


## Create deploy.sh

Créer un fichier **deploy.sh** depuis vscode ou vim.
copier/coller le code ci-dessous et remplacer 

sur la ligne `git push -f git@github.com:<USERNAME>/<REPO>.git master:gh-pages`

`<USERNAME>/<REPO>` parle nom de votre GitHub / nom de votre repo GitHub.

```
#!/usr/bin/env sh

# abort on errors
set -e

# build
npm run build

# navigate into the build output directory
cd dist

# if you are deploying to a custom domain
# echo 'www.example.com' > CNAME

git init
git add -A
git commit -m 'deploy'

# if you are deploying to https://<USERNAME>.github.io
# git push -f git@github.com:<USERNAME>/<USERNAME>.github.io.git master

# if you are deploying to https://<USERNAME>.github.io/<REPO>
git push -f git@github.com:<USERNAME>/<REPO>.git master:gh-pages

cd -
```

## Deploy to 

Dans le terminal, depuis le projet : 

* Add and commit project change and push into GitHub.

* lancer les commandes `chmod +x deploy.sh` puis `./deploy.sh`.

ps: après des changements dans le projet, faire à nouveau add, commit et push puis relancer
`./deploy.sh`.



