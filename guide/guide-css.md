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

## Référencer une feuille 

###Feuille de style CSS _**externe**_ 

il faut ajouter un <link> élément dans le document HTML 
```<link rel="stylesheet" href="styles.css">```
chemin possible ;
<!-- Inside a subdirectory called styles inside the current directory -->
<link rel="stylesheet" href="styles/style.css">

<!-- Inside a subdirectory called general, which is in a subdirectory called styles, inside the current directory -->
<link rel="stylesheet" href="styles/general/style.css">

<!-- Go up one directory level, then inside a subdirectory called styles -->
<link rel="stylesheet" href="../styles/style.css">

### Feuille de style CSS _**interne**_

Le code HTML d'une feuille de style interne peut ressembler à ceci:
<!DOCTYPE html>
``<style>
h1 {
color: blue; 
background-color: yellow;
border: 1px solid black;
}``
          
## Les instructions CSS

Après avoir ciblé un sélecteur HTML (h1, p, ect) nous pouvons indiquer dans la balise toute les modifications concernant cette élément. 

* La couleur peux être modifier avec "color: yellow "
* La couleur de font par "background-color: red "
* Encadré ombragé "box-shadow; 8px 8px 12px rgb(7, 7, 7);
* Bordure "border: 3px solid;"
* La couleur de la bordure "border-color: #74383f;"

## Les couleurs

Les couleurs sont écrits après un # sur 6 chiffres ou lettres qui définissent une couleurs précise. 
Pour harmoniser les couleurs du site il exite un site qui propose (en fonction d'une photo est possible) des palettes de couleurs _**https://coolors.co/**_
 
## taille
Il existe plusieurs façon de définir la taille d'un élément. 
* les pixels _**px**_ sont généralemnt utiliser pour définir la taille du texte mais on peux aussi définir d'autre éléments. Il représente en pixel la taille de l'élément.
* les poucentage _**%**_ sont généralment utiliser pour définir la taille d'une image ou logo et autre sybolle exterieur en fonction de sa taille initiale. 
* _**em**_ peuvent avoir un chiffre décimale 1.3 (il faut séparer les chiffre par un .)
* valeur relative peuvent aussi être utilisé comme (c'est limité car il n'y en a que 7); 
    *xx-small: minuscule ;
    * x-small: très petit ;
    * small: petit ;
    * medium: moyen ;
    * large: grand ;
    * x-large: très grand ;
    * xx-large: euh… gigantesque.

## Marge

margin left...
float
padding

## style image



## style texte
https://fonts.google.com/
font...

## grid (grille)

## class/div
