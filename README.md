# sass-notion
1. inclure dans le fichier package.json => script => "sass": "node-sass -w scss -o css"

2. npm run sass

## Heritage :

%"class parent" { contenu class }

class enfant {
@extend %class parent;
contenu class enfant
}

## Imbrication:

utiliser "&-nom class enfant" {contenu class)

## variable:

utiliser "$nom variable :"

## Mixin:

nouveau fichier "\_mixins.scss"
Déclarer une mixins: @mixin "nom" {contenu en dur ou @content}

=> fichier scss parent
@import "mixins";
dans la class de notre choix @include "nom mixin" {contenu mixin si @content utilisé}

## Mixin media query:

nouveau fichier "\_media.scss"
Déclarer une mixins: @mixin "nom" {contenu en dur ou @content}

## Mixin et paramettre:

@mixin nom($prop, $couleur, $taille) {
  #{$prop}: $couleur;
font-size: $taille;
}

=> dans la class du fichier scss parent :
.conteneurX {
@include nom(background, red, 25px);
}

## Fonctions:

@function sum($arg1, $arg2){
  @return $arg1 + $arg2;
}

