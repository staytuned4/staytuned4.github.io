---
layout: post
tags: [script, débutant, wright script, permission, path]
---
# Écrire mon premier script et le lancer

Script: Contient texte ASCII, créer à partir d'un éditeur de texte (qui lit et écrit texte ASCII).
Exemple éditeur de texte: Vi, Vim, Emacs, nano, Gedit, Kwrite.

Ex de script:
```
#!/bin/bash
# My first script
echo "Hello world"
```

Enregistrer le script sous: hello_world

1. shebang: indique quel programme doit être utilisé pour interpréter le script. les languges comme Perl,awk, tcl, Tk, Python, utilisent le même mécanisme.
2. Commentaire (ce qui suit # est ignorer par bash) utilisé par les programmeurs pour expliquer le code.
3. echo (commande) imprime son argument sur l'écran.

# Donner au shell les permissions pour exécuter le script

chmod (commande)
chmod 755 hello_world
755: Nous donne la lecture, ecriture, exécution. Lecture, exécution aux autres.

{% include tips.html content="700: Pour rendre le script priver." %}

Lancer le sript:
```
./hello_world
```
path (chemin): lorsque l'on tape le nom d'une commande, le system ne cherche pas dans l'ensemble de l'ordinateur pour savoir ou le programme se trouve (ce serait trop long) mais seulement dans une liste de fichiers ou les fichiers exécutable (programmes) sont stockés. La liste de ces fichiers est appelé "path".
Pour voir la liste:
```
echo $PATH
```
La recherche se fera dans cette liste de fichier lorqu'une commande est entrée (si aucun chemin specifique n'est donné).
Si il ne trouve pas le progranne, il affiche "not found".

Pour ajouter un fichier au "path" (à la liste de fichier):
```
export PATH=$PATH:nomdunouveaufichier
```
Le mieux est d'inclure la commande dans le fichier .bash_profile afin qu'il soit généré automatiquement à chaque log in.

La plupart des distribution Linux encourage chaques utilisateurs à avoir un fichier "bin"pour les programmes qu'ils utilisent.
S'il n'existe pas, il peut être créer avec:
```
mkdir ~/bin
```
Si on mets notre script dans le fichier "bin", alors la commande
```
hello_world
```
suffit à lancer le sript.

Il faut ouvrir une nouvelle session terminal, avec Ubuntu et les distribution basé sur Debian, avant que le nouveau fichier "bin" ne soit reconnu.
