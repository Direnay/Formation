# Html

Est le langage que les navigateurs reconnaissent. Il va attacher du sens aux contenus.
Par exemple, demander qu'un mot soit considérer comme titre ou qu plusieurs mots soient considérés comme une liste ou qu'un fichier soit interprété comme une image, etc.

## Débuter un document 

Un document _html_ peut-être rédiger avec nimporte quel _éditeur de texte_ on doit faire attention à indiquer l'extension _.htm_ ou _.html_ par exemple : _conteuse.html_ pour qu'il puisse être interprété par un navigateur par exemple.

_Au début du document nous devons indiquer le langage parlé c'est à dire le _html_ comme ceci : ```<html> </html>```

La plupart des ordres généraux (_balises html_) s'écrivent entre _<>_ ; pour ouvrire et _/>_ pour refermer l'ordre. Elles doivent s'ouvrir et se refermer en fonction de la hiercharchie du contenu dans le document. Exemple : Il est entendu que la balise du document html sera fermé à la toute fin du document. 

```
<html>
    <head>
        <meta description="le blabla qui apparaît lors de la recherche google">
        <meta keywords="conteuse, montpellier, conte, raconter, histoire, kurde, mésopotamie" >
    </head>
    <body>
        <!-- représente le corps du texte -->
        <h1>Numéroter les titres en fonction de son importance. Le 1er étant le plus important.</h1>
    </body>
</html>
```

## Insérer un image

Pour insérer une image il faut utiliser cette balise :

```<image src="adresse de l'image">
