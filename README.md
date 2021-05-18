# Nom du projet

Marche à suivre pour travailler avec Git.

## Dépendences

Pour fonctionner ce projet a besoin de:

- Rien
- (optionnel) VS code
- (optionnel) Typora

## Installation

Télécharger un éditeur markdown de votre choix

## Inititialisation d'un repository

    Repository: Dépot git, il garde en mémoire les changements appliqués à un projet.

Pour initialiser `git init` dans un invité de commande (Git Bash, cmd, Powershell, etc).

## Ajouter des fichiers au commit

    Commit: Checkpoint dans l'avancée du projet (un point de sauvegarde), il retient qui a fait le commit, quand, et quels fichiers sont concerné par le commit. On lui donne un message qui sert a informer les autres utilisateurs.

Pour ajouter des fichiers au prochain commit, on passe par la commande `git add monFichier.truc`. Si on veux ajouter tous les fichiers qui ont été modifiés: `git add .`

## Vérifier le status de git (avant de faire des bêtises par exemple)

On peut vérifier l'état de git avec la commande `git status`.
Elle nous donnera les infos:

- La branche sur laquelle on est
- Les fichiers qui ont été modifés:
    - tracké (prêt à être envoyer en commit)
    - non tracké

## Effectuer un commit

Pour envoyer le commit à git (faire un checkpoint): `git commit -m "Message de commit"`

    Il existe plusieurs conventions pour les messages de commit. Celle d'Angular est la plus propre: `git commit -m "feature/Connexion(fichiers modifiés): Ce qui a été fait sur ce commit"`

## Ajouter un repository distant (remote)

Il faut créer un repo sur l'hebergeur Git de votre choix (GitHub, GitLab, BitBucket, etc).

Il faut ensuite renseigner le repo distant au repo local:
`git remote add origin url-du-remote`.

> origin fait référence à une variable locale, vous avez le choix de son nom.

### Envoyer les commits

Pour que le repository distant récupére les modifications (commits), il faut lui envoyer.

`git push branche-distante branche-locale`

Par exemple `git push origin main` pousse les modifications de ma branche main sur la branche origin/main.

### Récupérer les modifications sur le repo distant

Les changements sont poussés (trés) souvent sur le repo distant. Pour les récupérer il faut utiliser la commande pull:

`git push branche-distante branche-locale` par exemple `git pull origin main`

## Récupérer un répository distant (pour travailler en local)

Dans le cadre d'un projet en général, le répository est déja créé et nos devs n'ont plus qu'a récupérer en local le projet pour pouvoir travailler.

C'est possible gràce à la commande clone:
`git clone url-du-repo-distant`. Par exemple pour ce repository il faudrait faire `git clone https://github.com/benoitsemifir/Markdown`.

## Les branches

Les branches sont un moyen utile de travailler sur un projet (une fonctionnalité du projet) sans impacter le développement des autres utilisateurs. C'est un bon moyen de cloisonner le développement.

### Voir les branches

Pour voir les branches qui ont été créées: `git branch`. Vous verrez la liste des branches et la branche sur laquelle vous êtes est indiqué par une étoile.

### Créer une branche

Pour créer une branche: `git branch nom-de-la-branche`

Astuce: Pour créer une branche et se déplacer en une commande: `git checkout -b nom-branche`.

### Se déplacer vers une branche

Pour aller sur une branche: `git checkout nom-branche`.

note: `git checkout` peut aussi se déplacer sur un commit (attention a ne pas se perdre).


## Worflow Git

Il existe différents worflow pour utiliser git en équipe. L'un des plus connus est [git flow](https://www.atlassian.com/fr/git/tutorials/comparing-workflows/gitflow-workflow).

Il utilise les branches pour organiser le développement autour des releases (mises en production):

- main
- develop
- feature
- release
- hotfix

### main

C'est la branche stable ! Elle est protentiellement mise en production et doit donc être parfaitement stable.

### develop

C'est la branche la plus avancée dans le développement, mais pas forcément stable. Elle sert de point de sauvegarde dans l'avancée du projet (elle récupére les features).

### feature

Les branches features sont la partie cloisonnées du développement. Les développeurs mettent leur travail sur ces branches en fonction de la fonctionnalitée développée.

Par exemple les développeurs qui travaillent sur la fonctionnalitée de connexion d'une appli travaillerons sur une branche `feature/connexion`.

### release

Contient la partie préparée pour la mise en production de l'application.

### hotfix

C'est la branche qui sert à corriger les bugs introduits en prod.