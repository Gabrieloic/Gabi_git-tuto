# Gabi_git-tuto


## initialisation des etapes de configuration de git 



````` bash

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

