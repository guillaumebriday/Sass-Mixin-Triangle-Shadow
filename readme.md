# Sass Mixin Triangle Shadow

La génération de triangles en CSS peut être périlleuse, qui plus est lorsqu'il faut y rajouter une ombre sur le contours.
Cette mixin pour [SASS](http://sass-lang.com/) permet de les générer automatiquement avec différents réglages.

[DEMO](http://guillaumebriday.fr/lab/Sass-Mixin-Triangle-Shadow/)

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

## Improvements

N'hésitez pas à proposer des modifications ou des améliorations que j'ajouterais avec plaisir mais également à me contacter pour avec des informations complémentaires ou me remonter un bug.
