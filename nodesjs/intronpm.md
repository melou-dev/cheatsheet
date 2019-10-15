# NPM :

Node Package Manager

gestionnaire de paquets officiel de Node.js

paquet : dossier contenant un fichier package.json.

package.json = registre de tout les paquets, en format objets (définit le nom, version etc..)

maj :

npm update <nom_paquet> (npm up <nom_paquet>)

sémantique versionning (semver) : MAJOR.MINOR.PATCH

Gestion des versions de façon ordonnée =>

~ mettre à jour les patchs.
^ mettre à jour les mineurs et les patchs.

- 0.1.0 (version départ) // taper à la main //
- 1.0.0 (première version stable).
- 1.0.1 (correction de bug)
- 1.1.0 (ajouts de features compatibles)
- 2.0.0 (changements non compatibles).

Installation :

global :

- npm install -g <nom_paquet>

local :

- npm install <nom_paquet>

commande utiles :

- npm outdated (affiché les packages a mettre à jour).

- npm ls (liste de tout les packages).

- npm prune (supprime tout les package inutilisés).

- npm view <nom_paquet> (avoir des informations sur un paquet).
