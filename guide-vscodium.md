# Guide VSCodium
VSCodium est un éditeur de texte HTML et CSS. Il permet également de communiquer avec github. Ainsi les documents peuvent être modifé dans les deux lieu. Pour connecter le github à vscodium il faut réliser la tâche du chapitre suivant.

## Cloner un projet

Cloner un projet permet d'avoir les documents sur github à l'identique dans le disque dur de l'ordinateur. 
Pour cloner un projet existant sur l'éditeur VSCodium il faut aller dans la barre d'action sur: 
- affichage
    - palette de commande
        - cloner
            - entrer l'adresse SSH du dépôt en question. Elle se trouve dans le dossier github crée. 
            - choisir l'emplacement de l'enregistrement du document
            - l'ouvir sur VSCodium
### Pull (tirer)

> C'est un peu comme retirer son courrier

Faire un "pull" permet de récupérer les éventuelles modifications d'un dépot distant (github) vers mon dépot local (sur mon ordi).
Lorsque je réalise des modifications sur github (ajout/suppression de documents, modifier le contenu d'un document...) le nombre correspondant au modification apparaît en bas en bleue à coté d'une flèche descendante. Pour me siganler que j'ai des receptions en attente. Il faut cliquer sur le cercle fléché afin de réccupérer ces modification pour que les documents soit à jour dans mon ordinateur et ceux sur le site github. 

### enregistrer un commit

> C'est un peu comme préparer un colis pour la Poste

Ensuite je peux ouvrir un document pour le modifier. Une fois les modification réalisé j'enregistre (ctrl+s). Une fois enregistré le symbole medecin (graphique) va afficher un chiffre. Je clique dessus et commente le _commit_ (commettre) désigne le fait de commettre un acte sur le document. On peut expliquer ce qu'on a fait en ajoutant un message de _commit_ Puis cliquer sur _ctrl+entré_ ainsi la modification est nommée.

### Push (pousser) 
> c'est un peu comme poster ton colis pour l'envoyer à github

Pour "pusher" cliquer sur la flèche montante indiquant le nombre de commit réalisé sur github. Afin de renvoyer vers github les modifications réalisé sur vscodium. 
