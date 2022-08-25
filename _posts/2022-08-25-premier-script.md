---
layout: post
tags: [script, débutant]
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
path (chemin): lorssque l'on tape le nom d'une commande, le system ne cherche pas dans l'ensemble de l'ordinateur pour savoir ou le programme se trouve (ce serait trop long) mais seulement dans une liste de fichiers ou les fichiers exécutable (programmes) sont stockés. La liste de ces fichiers est appalé "path".
Pour voir la liste:
```
echo $PATH
```
Si il ne trouve pas le progranne, il affiche "not found".
