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

git add les fichiers: ajout de fichier
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

