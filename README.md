## Zen-fs ? Quesaco ?

Zen-fs est un générateur de font-sizes responsives sous **sass**, basé sur cet [excellent article](https://www.smashingmagazine.com/2017/05/fluid-responsive-typography-css-poly-fluid-sizing/) de [Jake Wilson](https://github.com/Jakobud) et son mixin **poly-fluid-sizing**.

## Fonctionnement

**Zen-fs** contient de base 5 font-sizes responsive : 

|name | value |
|----|----|
|**main**| 14px|
|small|12px|
|big|26px|
|large|36px|
|huge|64px|

Chaque taille étant calculée par rapport à la taille **main**.

A chacune de ses tailles est associée une **map** de la forme :

```sass
(
  $breakpoint: $font-size,
  $breakpoint: $font-size,
  $breakpoint: $font-size
  ...
);
```

C'est cette map qui permet de déterminer le comportement responsive de la font-size ciblée.

/!\ Les breakpoints sont ensuite utilisés dans une media-query de type *min-width*.

## Générateur

Comme énoncé plus haut, Zen-fs est un générateur. Il expose :

* les classes utilitaires correspondant aux font-sizes
* les classes silencieuse permettant d'appliquer un comportement responsive à un selecteur en particulier (en utilisant un **@extend**)

## Variables

| name | desc | default |
|---|---|----|
|$zfs-prefixe| détermine le préfixe ajouté en début de classe et de classe silencieuse | zfs |
| $zfs-main | taille de font de reference | 14px



