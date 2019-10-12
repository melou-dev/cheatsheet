# DEPLOYER PROJET VUE SUR GITHUB.


## Créer un nouveau projet avec vue.

c'est du déjà vue.

## Créer un repo sur GitHub.

ça c'est du déjà vue.

Attention!! ne pas créer la Git Hub pages manuellement. La source doit rester en "NONE".

![GitHub Pages](https://github.com/melou-dev/cheatsheet/blob/master/vue/images/github-pages.png)

dans le terminal dans le projet vue.
```
git remote add origin git@github.com:githubname/reponame.git
git push -u origin master
```

## ouvrir le projet.

avec `code .` ou `vim .` dans le terminal


## open .gitignore.

* ouvrir le fichier **.gitignore**
* desactiver la ligne / dist en mettant un **#** devant.

![screenshot .gitignore](https://github.com/melou-dev/cheatsheet/commit/41c521243cf054438339a9a81ea0b07738e41e1b)


## Create deploy.sh

Créer un fichier **deploy.sh** depuis vscode ou vim.
copier/coller le code ci-dessous et remplacer `myproject` par le nom de votre repo GitHub.

```
module.exports = {
  publicPath: process.env.NODE_ENV === 'production'
    ? '/my-project/'
    : '/'
}
```

![screenshot deploy.sh](https://github.com/melou-dev/cheatsheet/commit/3c4799a3211dd82aa5662dc28af19751d464aa35)




