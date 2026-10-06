# Compte rendu TP01-git

## Partie 1
1. Voici l'url de mon compte GitHub : https://github.com/SompayracLoic
   
## Partie 2
1. **Voici la sortie de `gitconfig --list --global` :**<br>
   `user.name=Loic Sompayrac ` <br>
   `user.email=loic.sompayrac@e.rascol.net` <br>
   `init.defaultbranch=main` <br>
   `core.editor=nano`

2. L'option `--global` sert à écrire ces paramètres pour tous les repos de ma session plutôt que pour chaque repo spécifiquement.
   
## Partie 3
1. **Git status réponds :** <br>
   `fatal: ni ceci ni aucun de ses répertoires parents (jusqu'au point de montage /) n'est un dépôt git` <br>
   `Arrêt à la limite du système de fichiers (GIT_DISCOVERY_ACROSS_FILESYSTEM n'est pas défini).` <br>
   Puisque le système de fichier que l'on a créé n'est pas encore un repo GitHub.

2. a) Le dossier que `git init` a créé est le dossier *".git"*.<br> 
    On ne le voyait pas avec un simple `ls` car le point *"."* devant le nom du dossier, indique àLinux que c'est un dossier caché.

   b) Git status réponds maitenant : <br>
   `Sur la branche main`

   `Aucun commit`

   `rien à valider (créez/copiez des fichiers et utilisez "git add" pour les suivre)`

3. a) `git status` range `README.md` dans la catégorie des fichiers non suivis.<br>
   b) Le fichier se trouve dans le répertoire de travail de git.

4. a) Ce qui a changé dans la réponse de `git status` est le répertoire dans lequel se trouve `README.md`. <br>
   b) Le fichier `README.md` se trouve maitenant dans la zone de préparation de git.

5. a) Voici la sortie de `git log` : <br>
   `commit 4686606452eeba39d6b319ddabcad2807f34d1f4 (HEAD -> main)` <br>
   `Author: Loic Sompayrac <loic.sompayrac@e.rascol.net>`<br>
   `Date:   Tue Sep 29 16:22:42 2026 +0200`<br>

   ` Création du README`
   
   b) **Hash :** "4686606452eeba39d6b319ddabcad2807f34d1f4" <br> 
   **Auteur :** "Loic Sompayrac \<loic.sompayrac@e.rascol.net>" <br>
   **Date :** "Tue Sep 29 16:22:42 2026 +0200" *(Mardi 29 Septembre 16h22 UTC - 02:00)*<br>
   **Message :** "Création du README"

   c) Le HASH comporte 40 caractères , est écrit en base 16, et représente un total de 160 bits.


7. a) `git status` nous informe que le fichier `README.md` est modifié.<br>
   b) `git dif` nous montre la différence entre la version locale du fichier et la version du fichier qui est sur le dépôt. Les `+` au début des lignes annoncent que c'est un nouveau changement que le fichier du dépôt n'a pas.

8. a) Voici la sortie de `git log --oneline` : <br> 
   `cc464c2 (HEAD -> main) Commit puisque le tp m'y force`<br> 
   `813894d Création de l'aide mémoire Git`<br> 
   `c7c8de5 Ajout des questions 3.7 (fin du cours)`<br> 
   `12b741d Ajout de l'année scolaire dans le README`<br> 
   `751d084 Ajout du compte rendu (questions 0 à 3.5)`<br> 
   `4686606 Création du README` <br> 
   b) Il est préférable de ne faire qu'un seul commit puisque de cette façon nous pouvons avoir un historique des versions plus précis et détaillé en cas de problèmes.

## Partie 4

1. `git show` montre le changement qui a été poussé dans ce commit sur le fichier `README.md` ainsi que l'heure et la date du commit.

2. `git restore` a fait en sorte que le fichier `README.md` retourne à l'état de son dernier commit. Ainsi, non, si on le l'avais jamais commit, alors git restore n'aurait pas marché.

3. `test.txt` se retrouve dans la zone des fichiers non suivis. Le fichier n'a pas été supprimé du disque mais ne sera simplement pas suivi par git.

4. a)Tous les fichiers "parasites" que nous avions créés ont disparus de la de la réponse de git status.<br>
   b)Le fichier.`gitignore` en revanche, lui, apparaît. Oui il faut commit le fichier `.gitignore`.

5. Lors du premier commit, `README.md` ne contenait que le corps du texte, depuis, l'année scolaire depuis laquelle il a été créé a été ajoutée.

## Partie 5

1. a) Deux fichiers ont été créés :<br>
   - `id_ed25519` : C'est ma clef privée.<br>
   - `id_ed25519.pub` : C'est ma clef publique.<br>
   b) Les permissions des deux fichiers se présentent comme telles : <br>
   `-rwx------ 1 lsompayrac 1cielir-26-27  464 oct.   6 14:42 id_ed25519`<br>
   `-rwx------ 1 lsompayrac 1cielir-26-27  109 oct.   6 14:42 id_ed25519.pub`<br>
   Par défaut, j'ai des droits 600 car seulement moi (l'utilisateur) doit y avoir accès.

2. a) `ssh -T git@github.com` renvoie : <br>
   `Hi SompayracLoic! You've successfully authenticated, but GitHub does not provide shell access.`<br>
   b) On peut sans danger donner la clef publique à Github car elle ne fonctionne pas sans la clef privée. La clef privée tant qu'à elle est faite pour identifier le poste sur lequel elle se trouve, et permettre à la clef publique, d'établir une connexion entre le pc et Github. Si quelqu'un choppe ma clef privée, il peut se faire passer pour mon poste, et supprimer tout mon repo.

## Partie 6

1. 
