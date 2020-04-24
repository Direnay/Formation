# Le langage CSS

CSS veux dire *Cascading Style Sheet*. C'est un langage qui permet de styliser des contenus définie en _markdown_ ou en _HTML_. 

##  Sélecteur

En CSS, on utilise des sélecteurs qui permettent de pointer un élément HTML.

Par exemple on peut pointer les balises : body pour récupérer le `<body>` ou h1 pour récupérer les `<h1>` ou 
a pour les liens `<a>`
Ou des _class_ ou des _id_ :
.truc pour la _class truc_ `<h2 class="truc">`
\#celuici pour l'id  ex. `<a id="celuici">le lien</a>`

Et après, on demande d'appliquer des instructions css

```
a {
  # les instructions pour tous les liens de la page
}

body {
  # les instructions pour toutes les balises dans le <body> 
}

```




Les sélecteurs déterminé dans le document html servirons pour attribuer un style au contenu. Exemple: h1 {color:yelow}

Il y a le sélecteur (contenue hiérarchisé du document html) à l'interieur des {} il y a la propriété dans mon exemple c'est la couleur et la valeur. Dans mon exemple c'est la couleur jaune. 
Il existe une multitude de propriété comme les encadrés, les couleurs, le centrage. 
Nous ouvrirons de {} par propriété que nous souhaitons mordier. Il est possible d'isoler des contenus afin d'appliquer un visuel commun. Cette isolation se fait sur le document HTML c'est a dire sa propriété, de quoi il découle. 

CSS execute une tâche quand l'ordre donnée est au plus précis autrement c'est le paramètre par défaut qui est executé. 
Exemple: les textes "paragraphe" s'écrivent d'un à l'autre de l'écran. Si nous souhaitons des sauts de ligne il faut le préciser.
Les listes s'écrivent les uns sous les autres, en block et non inline. L'ordre doit être données au li et non à l'ul. 
