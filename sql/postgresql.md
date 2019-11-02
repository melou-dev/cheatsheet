# postgresql

## commandes de base.

`sudo su postgre`

`psql`- entrer dans postgresql - installation de `pgcli` pour aide au commande

`\l` - lister les bases de données

`\du` - lister les utilisateurs ou groupe d'utilisateurs et leurs rôles : mane / Superuser, Create role, Create DB, Replication, Bypass RLS

`\q` - quitter postgresql

`\?` - `help` - aide

`\d` + dbname - afficher la base sans les données.


## commandes pour créer/supprimer une base de données.

`CREATE DATABASE databasename;` - créer une base de données ex : test

`DROP DATABASE databasename;` - supprimer une base de données


## rôle de la base de données.

 Quand on parle de rôles, on parle aussi de droits des « utilisateurs » et des « groupes ».

 le rôle détermine l'ensemble des droits disponibles pour le client connecté, il est important de configurer soigneusement les droits quand un environnement multi-utilisateurs est mis en place. 
 
un client n'est pas obligé de se connecter avec le rôle du même nom que son nom d'utilisateur dans le système d'exploitation.

### des commandes.

`CREATE ROLE username;` - créer un rôle

`DROP ROLE username;` - supprimer un rôle

`createuser username;`
`dropuser username;`

`CREATE USER username WITH PASSWORD password;` - créer un utilisateur ou groupe d'utilisateurs.

`ALTER DATABASE databasename OWNER TO username;` - attribuer une base de données à un utilisateur ou groupe d'utilisateurs ex: test / toto

`ALTER USER username WITH role;` - ex : toto / superuser

`SELECT * FROM dbname;` - sélectionner une base de données.