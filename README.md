# Nom du projet

Super projet machin bidule

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

