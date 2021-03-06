# Git | Commandes

## Auteur
### Kevin DOOLAEGHE

## Sources
* [Git - Reference](https://git-scm.com/docs)
* [Git Cheat Sheets](https://training.github.com/)
* [Clone HTTPs repositories - `gh auth login`](https://cli.github.com/manual/gh_auth_login)
* [Github on CLI (`gh` command)](https://github.com/cli/cli/blob/trunk/docs/install_linux.md)

## Commandes

### Commandes de base

→ Afficher l'aide :
* `git help [-a]`
* `git`

→ Définir le nom d'utilisateur et son email :
* `git config --global --list`
* `git config --global user.name "Nom"`
* `git config --global user.email "E-mail"`
* `git config --global --unset-all user.name`
* `git config --global --replace-all user.name "Nouveau nom"`

→ Afficher les logs :
* `git log <option>`
* `-(n)` : Afficher les n derniers commits
* `--since`, `--after` : Afficher les commits après une date
* `--until`, `--before` : Afficher les commits avant une date
* `--author` : Afficher les commits d'un auteur
* `-S` : Afficher les commits contenant la chaîne de caractères

→ Afficher le statut du dépôt :
* `git status`

→ Afficher les modifications qui ne sont pas encore indexées :
* `git diff`

→ Initialiser un dépôt :
* `git init`

### Gestion des fichiers

→ Ajouter des fichiers au suivi de version :
* `git add <fichier>`
* `git add *`

→ Effacer des fichiers indexés :
* `git rm <fichier>`

→ Déplacer des fichiers :
* `git mv <src> <dst>`

→ Ignorer des fichiers :
* Créer un fichier `.gitignore`
* Renseigner les fichiers ou la forme des fichiers

→ Faire un commit :
* `git commit -a -m "message"`

### Gestion des branches

→ Ajouter une branche :
* `git branch <branche>`
* `git checkout -b <branche>`

→ Supprimer une branche :
* `git branch -d <branche>`

→ Changer de branche :
* `git checkout <branche>`

→ Pousser la branche :
* `git push --set-upstream origin <branche>`

→ Fusionner deux branches :
* `git checkout <dst>`
* `git merge <src> [-no-ff]`

### Fonctionnement en distant

→ Cloner un dépôt distant :
* `git clone <url>`
* `git clone <url> --branch <branche>`
* `git clone https://[utilisateur]:[mot de passe]@[projet]`

→ Afficher la liste des dépôts distants enregistrés :
* `git remote`

→ Ajouter un dépôt distant :
* `git remote add <nom> <url>`

→ Renommer un dépôt distant :
* `git remote rename <ancien> <nouveau>`

→ Récupérer les informations sans les ajouter à la branche courante :
* `git fetch <nom>`

→ Récupérer les information et les ajouter à la branche courante :
* `git pull origin <branch>`

→ Pousser son travail sur un dépôt distant :
* `git push origin <branch>`
* La branche par défaut est `master`

→ Inspecter un dépôt distant :
* `git remote show [n]`
