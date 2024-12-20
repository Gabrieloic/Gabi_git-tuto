# Gabi_git-tuto


## initialisation des etapes de configuration de git 


```bash

# documentation officielle pour recherche sur le sujet
	https://git-scm.com/docs
	https://docs.github.com/en/get-started


# on initialise le fichier .git dans notre repertoire local )
	git init ( dans le repertoire local de notre dossier )

# on cree le fichier Readme.md en y rajoutant les informations qu'on veut et idealement avec le nom du repo au debut 
	echo "# Gabi_git-tuto" >> README.md 

# on specifie l'origin de notre repo distant via la connexion ssh pour que tout les commit arrivent dans ce repo
	git remote add origin git@github.com:Gabrieloic/Gabi_git-tuto.git

# on fait un etat des modifications qui ont ete faite dans notre repo local et on aura la liste tous les fichier modifies 
	git status

# on doit maintenant mettre ces fichier dans la liste des fichiers suivis ( qui seront envoyes lors du  commit )
	git add <Nom_du_fichier>

# on peut faire un rajout de tous les fichiers vu qu'on est dans le meme dossier en faisant 
	git add .

# on doit maintenant figer l'etat de nos fichiers dans Git
	git commit -m " <commentaire que nous souhaitons voir s'afficher une fois le push effectue> "

# a partir d'ici on peut pusher tous les fichiers modifies sur notre repo distant
	git push origin main

# on a la possibilite d'avoir les logs des differents commit qui ont ete fait ainsi que leurs utilisateurs
	git log

# on peut recuperer les logs en details avec les dernieres infos qui ont ete modif, le nombre de lignes rajoutees...
	git show

# si on s'est trompe et on veut annuler un git add on fait 
	git restore --staged <Nom_du_fichier_a_annuler> ou alors <.> pour tous les fichiers

```

## Cette partie a ete cree sur la nouvelle branche dev puis commite : et done elle est absente sur la main parce qu'on n'a pas encore merge

```bash

# on peut creer une nouvelle branche avec cette commande
	git checkout -b <Nom_de_la_branche>

# une fois cree on peut naviguer a travers les branches 
	git chekout <Nom_de_la_branche_ou_on _veut_etre>
	git branch #affiche toutes les branches sur notre repo et en vert celle ou on se trouve

## Cette partie apparaitra desormais dans le branche main parce qu'on va la merger : c'est a dire, toutes les modifs qui ont ete faite sur la branche dev seront desormais dans la main. Pour merger on fait comme suit

## on revient d'abords sur la branche dans laquelle on veut merger ( dans notre cas c'est main)
	git checkout main

## on fait ensuite le merge depuis la branche dev
	git merge dev

## on vera que toutes les modifs de la dev sont desormais en local sur la branche main. on peut maintenant faire un push de main sur le repo distant
	git push origin main

```

## On va integrer le concept de "PULL OU MERGE REQUEST" qui est la revue de code

```bash


# Dans cette partie, pour une bonne pratique, on va integrer la notion de "Revue de code".
# Pour cela, on va creer un branche, faire des modifications, les envoyer sur le depot distant,
# puis creer une "PULL REQUEST" pour demander une revue de code.

# Cela dit, on est sur notre branche dev, on fait les modifs puis on les push sur le repo distant.
# Une fois fait, on va sur la GUI de notre repo et on remarquera qu'il nous est propose de faire 
# un "PULL REQUEST" sur github et ce sera "MERGE REQUEST" sur gitlab: mais c'est la meme action.

# Ca veut dire qu'on informe une equipe de dev que nous avons apporte des modifs et qu'on aimerait
# les pusher sur la main mais il faudrait qu'il verifie si tout est bon avant de valider

```

