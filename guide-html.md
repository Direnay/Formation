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
## Les métadonnées

Sont les données qui constituent les éléments de bases dans la création d'un document html.
Sont dans les enfants de _\<head>_ et s'érivent de cette manière là \:

```\<head>
    \<meta title="titre de la page"
permet de nommer l'oglet de la fenêtre. 
           charset="utf-8"
           Correspond à l'encodage de la page. Permet à se que les caractère soit bien lisible
           name="texte apparant sur moteur recherche"
           keywords="mot clés permettant aux utilisateurs de trouver le site sur moteur recherche"
           link href ou rel dépend du document ou lien vers l'icone qui s'affiche en haut de la fenêtre
``` 
Ils existent plein d'autre métadonnée. Se reporter aux guide mdn. 

# Les balises de texte
## Les titres
## Les paragraphes

Les paragraphes se distinguent par la formule 
```<p>texte</p>```

## Entité pour les caractère

Par défaut htlm mets à la suite les contenus écris.Permet un saut de ligne visible. 
```<br>```

Pour mettre un mot en gras il faut l'entourner par _strong_ avec une balise fermante \:
```<strong> le mot </strong>```

Pour les formule mathématique utilisé la balise _pre_. Les espaces et les caractères serons affiché comme sur l'éditeur html. 
```<pre> le mot </pre>```

## Liens
avec ancrage

Permet aux utilisateur d'afficher le liens dans une nouvelle fenêtre. 
```\<a target= blank"lien externe"```

Pour créer des liens interne nous pouvons relier des mots entre eux aisni (les mots ne peuvent contenir des caractères spéciaux, ni maj, juste lettre simple et - ou _ ) \:

```<a id="cuisine"``` élement de base
```<a href="#cuisine"``` en reponse c'est à dire lien vers _cuisine_

Le id permet d'isoler un élément afin d'en faire un usage spécifique comme un lien mais un autre caractère pourrait lui être apporté comme l'ancrage _classe_ puis pour y faire référence au lieu d'un # comme pour id il faut mettre un _._

## Image
### format des images
Il existe différents format d'image \:,  est 
- JPG ; le plus classique mais lourd et supporte mal la transparence.
- PNG ; supporte la transparence, légé, qualité dans le détail
- GIF ; animation, lourd, supporte mal la transparence. 
- SVG ; cool pour icone, concerve les formes, facile pour modifier. 

## Police d'écriture/ font-family
Se reporter à https://developer.mozilla.org/fr/docs/Web/CSS/font-family pour les différents types de famille d'écriture. 
Pour changer la police d'écriture la formule est la suivante: 
```font-family: "le style voulue"```
Il faut lié cette formule à un corps de texte comme le titre, le paragraphe ect. 

## Dimensions
Tout comme la police d'écriture il faut l'inclure à un corps de texte ou image, liens ect. 
width= chiffre en px (pixel) ou en chiffre em?
représente la largueur

height= pareil pour les unités de mesure
