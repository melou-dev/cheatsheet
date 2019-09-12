# String.

https://javascript.info/string

3 quotes :
* "",
* '',
* ``- backticks - plus moderne, permet:
** intégrer des expressions de type fonction et premettre leur application,

```
func"string" return (`1 + 2 = ${sum(1, 2)}.`);
```

** écrire sur plusieurs lignes, sans \n,
** écrire l'apostrophe à l'intérieur du String.


## caractères spéciaux

tous commencent avec **\**.
voir la page MDN (lien ci-dessus)


## Propriété - longueur de string.


`return (My\n.length); // 3`


## Méthode - Remplacer Majuscule/Minuscule.

**toLowerCase()** - majuscule.
**toUpperCase()** - minuscule.

```
return( "Interface".toUpperCase() ); // INTERFACE 
return( "Interface"[0]).toLowerCase() ); // i, car sélection du "i" avec [0]
```


## Méthode - accéder aux caractères (retoune un caractère)

commence à 0.

**str[index number]** - retourne le caractère choisi.

```
let str = "Hi"
return( str[0] ); // H
```


## Méthode - accéder à la position (retourne une position un nombre)

**str.indexOf(substr,pos)** - retourne le numéro du 1er caractère de la sélection.
**str.lastIndexOf(substr,pos)** - même chose mais part du dernier caractère.

```
let str = `Hi Pablo et Paul`
return( str.indexOf(`Pa`, 2)) // 13
```
dans un if pour éviter index 0 = 0 qui retournera `false`:

```
if (str.indexOf(`str`) != -1) //comparateur logique !=
if (~str.indexOf(~str.indexOf(`str`)) // Biwise, convertion en 32-bit -(n+1), n done 0(false) seulement si n == -1
```


## Méthodes - match - rechercher l'existance du/des caractères (retourne en boolean).

**str.includes(substr, pos)** - moderne, recherche si `substr` est dans `str`, position optionnelle.
**str.startsWith(substr)** - match le début.
**str.endsWith** - match la fin.


## Méthodes - isoler un partie d'un string.


|méthode                       |selections                         |nombres négatifs                               |
|:-----------------------------|:---------------------------------:|----------------------------------------------:|
|**str.slice(start [, end])**  |début, fin(non inclu et optionnel) |négatifs acceptés                              |
|**str.substring(start, end)** |entre début,  fin                  |valeur négative non accepté et processé comme 0|
|**str.substr(start, length)** | début, amplitude                  |négatifs acceptés pour le début                |

Slice est le plus flexible et le plus court.


## Méthodes - remplacer des caractères.

**Attention** on ne peut pas changer un string mais le remplacer en créant un nouveau string.
une manière simple est de sélectionner la partie à garder et créer un nouveau string avec le + pour concaténer.


## Comparaison.

L'alphabet est différent pour chaque langue. Heureusement, il y a un standard : ECMA 402 pour les navigateurs modernes.

UTF-16 - table numérique pour les comparaisons.
** Minuscule plus grand que majuscule
** Lettres avec avec des marques diatriques sont aussi plus grandes (ç et ö etc...)

### Méthode pour connaître la position.

**`letter`.codePointAt(0)** // "z" => 122

### Méthode pour créer un caractère à partir du numétique.

**str.fromCodePoint(position)**
**alert ( `\u---`)** // système hexadecimal

```
let str = '';

for (let i = 65; i <= 220; i++) {
  str += String.fromCodePoint(i);
}
alert( str );
// ABCDEFGHIJKLMNOPQRSTUVWXYZ[\]^_`abcdefghijklmnopqrstuvwxyz{|}~
// ¡¢£¤¥¦§¨©ª«¬­®¯°±²³´µ¶·¸¹º»¼½¾¿ÀÁÂÃÄÅÆÇÈÉÊËÌÍÎÏÐÑÒÓÔÕÖ×ØÙÚÛÜ
```

### Méthode pour comparer des strings dans différentes langues.

**str.localeCompare(str2)** :

* Retourne un négatif si str < str2,
* Retourne un positif si str > str2,
* Retourne 0 si équivalence.


## Méthode - Unicodes, hiéroglyphs et emojis.

emplitude = 2
**str.fromCodePoint()**
**str.codePointAt()**

## autres méthodes utiles.

**str.trim()** // enlève les espaces début et fin de string.
**str.repeat(n)** // répète le string n fois.







