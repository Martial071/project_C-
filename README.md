# Documentation du tuto git

## Initialisation du depot

'''
git init
'''

## Lien entre notre projet en local et le projet a distance sur github

'''
git remote add origin git@github.com:Martial071/project_C-.git (url du ssh)

dans le même dossier que .git créé après git init
'''

'''
Toutes les infos reliées à ton projet git sont dans le fichier .git/config. On peut y faire directement des modifs


'''
## Informations sur l'état de notre local


'''
git status

unstracked files : Tu as fait des modifs sur ta machine mais git ne les prend pas en compte

git add les fichiers ou . pour tous les fichiers: ajout de fichier
git commit "message": figer l'état (informations) de notre fichier dans git 
entrée : on a un truc dans le terminal, i pour inserer un message et echap pour arreter

:WQ (pour valider ton message)
:q! (quitter et forcer le faite de quitter sans confirmation)

git commit -m message :  eviter l'editeur dans le terminal

git (-u : facultatif) push origin main


'''



## 🔑 Configuration des accès SSH

Ce dépôt utilise le protocole SSH pour la gestion des accès et du code.

### 1. Générer et ajouter sa clé SSH à GitHub

Si vous n'avez pas encore configuré de clé SSH sur votre machine :

1. Générez une clé SSH dans votre terminal :
   ```bash
   ssh-keygen -t ed25519 -C "votre_email@example.com"


### 2.Affichez et copiez l'intégralité de votre clé publique

cat ~/.ssh/id_ed25519.pub

Ajoutez-la sur GitHub dans Settings > SSH and GPG keys > New SSH key.

### 3.Tester la connexion

ssh -T git@github.com

Note : Il est possible d'ajouter plusieurs clés SSH sur un même compte GitHub (par exemple pour différents environnements ou terminaux sur une même machine).


## Faire des configurations

Permet d'éviter une demande d'username et adresse mail. A utiliser avec un repos pour une autre personne et donc utiliser ses ident.

Faire une recherche git username pour toute la documentation.

## Evolution d'un projet ( historique )

git log
git show : plus d'infos que git log

## Rediger un bon commit

'''
Titre du commit

Description de notre commit avec des infos sur l'évolution du projet
'''
git restore --staged fichiers (avant commiter et après add) : pour retirer les fichiers que tu voulais push


## Créer des branches

Créer plusieurs branshes en fonction des problèmes et des collab


git branch : la liste de  branches sur le projet
git checkout -b newbranch (develop sur laquelle on developpe le projet) : pour créer un new branch  

rmque :  ligne vert ajout de code et ligne bleu modif en vs code
commit après création d'une branche

## Merger les branches : transferer les infos de la branche develop dans main

git checkout branch : déplacer d'une branch à une autre
git merge branch* : merger le travaille de la branch develop dans la branch courante (pourquoi il faut un git checkout first)

!!!! git stash : garder tes modifs dans une seule branche avant de changer. Supprime moment et donc ne pourra pas être present dans l'autre branch si tu merge !!!!

ou tu git push avant de changer sinon tu conserveras les mêmes modifs de part et d'autre de ta branche
git stash pop : quand tu reviens sur ta branch ou il y a les modifs

!!!!Non, pas obligatoirement ! Tu peux fusionner (merge) des branches en local sur ton ordinateur sans avoir besoin de les push au préalable et push après.!!!!

## Pull request

Pour les bonnes pratiques, on integres la notion de revue de code



