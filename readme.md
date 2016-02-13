# Sass Mixin Triangle Shadow

La génération de triangles en CSS peut être périlleuse, qui plus est lorsqu'il faut y rajouter une ombre sur le contours.
Cette mixin pour [SASS](http://sass-lang.com/) permet de les générer automatiquement avec différents réglages.

[DEMO](http://guillaumebriday.fr/lab/Sass-Mixin-Triangle-Shadow/)

[Codepen.io](http://codepen.io/ZiiCEagle/pen/obyGaX)

*Il est important de noter qu'il y aura sûrement des ajustements à faire selon vos besoins.*

## Utilisation

Commencer par importer la mixin dans votre projet.

```css
@import 'triangle-shadow';
```

Rappel des paramètres :
```css
@mixin triangle-shadow($position, $offset, $size, $color, $box-shadow-pos, $box-shadow-blur, $box-shadow-color);
```

Pour mettre un triangle sur l'élément qui a la class "selector" par exemple, il faudra s'en servir de la façon suivante :
```css
.selector {
    $color-shadow: #337ab7;
    $color-triangle: #282b2e;

    box-shadow: 0px 0px 6px 3px $color-shadow;
    @include triangle-shadow('top', 50%, 10px, $color-triangle, 3px, 4px, $color-shadow);
}
```

Vous pouvez également surchargé un triangle à une autre position, de la manière suivante par exemple :

```css
$color-shadow: #337ab7;
$color-triangle: #282b2e;

.selector {
    box-shadow: 0px 0px 6px 3px $color-shadow;
    @include triangle-shadow('top', 50%, 10px, $color-triangle, 3px, 4px, $color-shadow);
}

@media screen and (min-width: 750px){
    .selector {
        @include triangle-shadow('bottom', 50%, 10px, $color-triangle, 3px, 4px, $color-shadow);
    }
}
```

## Améliorations

N'hésitez pas à proposer des modifications ou des améliorations que j'ajouterais avec plaisir mais également à me contacter pour avec des informations complémentaires ou me remonter un bug.
