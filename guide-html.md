# Html

Est le langage que les navigateurs reconnaissent. Il va attacher du sens aux contenus.
Par exemple, demander qu'un mot soit considérer comme titre ou qu plusieurs mots soient considérés comme une liste ou qu'un fichier soit interprété comme une image, etc.

[Guide HTML sur MDN](https://developer.mozilla.org/fr/docs/Apprendre/HTML/Introduction_%C3%A0_HTML)

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

## Les listes

Pour faire une liste de choses et d'autre (ex : pierre, feuille, ciseau. Liste de courses) il y a deux possibilité : 

- [Unordered List UL](https://developer.mozilla.org/fr/docs/Web/HTML/Element/ul) :
```
<ul>
    <li>élément</li>
    <li>autre élément</li>
</ul>
 ```
Permet d'obtenir une liste avec des points (bullet)
<ul>
    <li>élément</li>
    <li>autre élément</li>
</ul>

---

- [Ordered List OL](https://developer.mozilla.org/fr/docs/Web/HTML/Element/ol) :
```
<ol>
    <li>élément</li>
    <li>autre élément</li>
</ol>
 ```
permet d'obtenir une liste avec des numéros par exemple pour une recette

<ol>
    <li>éplucher les pommes</li>
    <li>manger les pépins</li>
</ol>

## Les titres

Ils s'écrivent de cette façon et toujours entre des balises, contrairement à _markdown_ il faut les refermer : 
```h1, h2, h3, ...```
```<h1>Titre</h1>```

 En les hierarchisant, du plus au moins important : h1 à h5
 
## hr

Cette anotation ```<hr>``` permet de faire apparaître une ligne de démarcation entre les différents contenue écrit. Sa forme (longueur, largeur, couleur...) peux être modifier en _css_ au même titre que les autres contenus

## Liens

Les liens _html_ se précisent par l'ancrage :

```<a href="l'adresse URL">texte qui va apparaitre</a>```

<a href="https://direnay.github.io/conteuse">La conteuse Diren</a>

_anchor_ : a

## Image

Pour inclure une image la formule est la suivante : 
```<img src="emplacement URL">```

<img src="https://gite.equisud.com/img/img_square_13.jpg">
 
Il peux être interessant d'ajouter un texte alternative au cas ou la photo ne s'affiche pas. Le texte alternatif s'affiche à la place. 
Permet aussi aux mal voyants de savoir de quoi il s'agit. Ne remplace pas la légende. 
Le contenu de l'alternative est concidéré par le moteur de recherche. 
exemple :
```<img src="emplacement" alt="ce que c'est">```

Ainsi que la nommination de l'image. C'est à dire qu'il est plus intéressant de nommer comme on le souhaite l'image que de mettre par exemple: _image343_

### Le code

La balise :
```<pre>```

permet de préserver le texte sans l'interpréter par exemple une balise ne sera pas interprétée.
On l'utilise pour présenter du code ou des formules mathématiques.
