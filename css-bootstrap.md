<!-- omit in toc -->
# Bootstrap

- [Introduction](#introduction)
- [Installation](#installation)
  - [Méthode rapide (CDN)](#méthode-rapide-cdn)
  - [Méthode complète (fichiers compilés)](#méthode-complète-fichiers-compilés)
    - [Fichier sources](#fichier-sources)
  - [Package manager](#package-manager)
  - [Starter Template](#starter-template)
- [Utilisation](#utilisation)
  - [Container](#container)
    - [Fluid container](#fluid-container)
    - [Responsive container](#responsive-container)
  - [Grid](#grid)
  - [Components](#components)

## Introduction

Bootstrap est un framework permettant d'aider à la création de site web responsive et mobile first.

## Installation

### Méthode rapide (CDN)

Copiez-collez le lien vers le CSS dans votre balise \<head>.

```html
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css" integrity="sha384-JcKb8q3iqJ61gNV9KGb8thSsNjpSL0n8PARn9HuZOnIxN0hoP+VmmDGMN5t9UJ0Z" crossorigin="anonymous">
```

Voilà, vous avez accès aux classes de Bootstrap!

Il faut encore ajouter les scripts Jquerry (bientôt obsolète dans la future version 5), Popper.js et ceux de Bootstrap pour que tous leurs composants fonctionnent correctement. Ceux-ci sont optionnels, vous pouvez retrouver la liste des composants qui nécessitent du JS pour fonctionner dans [la documentation](https://getbootstrap.com/docs/4.5/getting-started/introduction/#js).

Ajoutez les lignes suivantes à la fin de votre page, juste avant la fermeture de la balise \<body> pour incorporer le JS.

```html
<script src="https://code.jquery.com/jquery-3.5.1.slim.min.js" integrity="sha384-DfXdz2htPH0lsSSs5nCTpuj/zy4C+OGpamoFVy38MVBnE+IbbVYUew+OrCXaRkfj" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/popper.js@1.16.1/dist/umd/popper.min.js" integrity="sha384-9/reFTGAW83EW2RDu2S0VKaIzap3H66lZH81PoYlFhbGU+6BZp6G7niu735Sk7lN" crossorigin="anonymous"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js" integrity="sha384-B4gt1jrGC7Jh4AgTPSdUtOBvfO8shuf57BaghqFfPlYxofvL8/KUEfYiJOMMV+rV" crossorigin="anonymous"></script>
```

### Méthode complète (fichiers compilés)

Il est également possible de télécharger Bootstrap et d'accéder aux fichiers dont vous avez besoin.

Pour ce faire rendez-vous sur la [page de Download :floppy_disk:](https://getbootstrap.com/docs/4.5/getting-started/download/#compiled-css-and-js)

Il vous suffit ensuite de placer ces fichiers directement dans votre projet et de créer les liens vous même. Cette méthode peut alourdir inutilement votre site.

#### Fichier sources

Il est également possible de retrouver les fichiers pré-compilation si vous voulez jeter un oeil et éffectuer des modifications importantes.

### Package manager

Si vous travaillez avec un package manager (npm), il est tout à fait possible d'installer Bootstrap. [Référez-vous à la documentation :book:](https://getbootstrap.com/docs/4.5/getting-started/download/#package-managers) pour la commande exacte en fonction de votre projet.

### Starter Template

```html
<!doctype html>
<html lang="en">
  <head>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

    <!-- Bootstrap CSS -->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css" integrity="sha384-JcKb8q3iqJ61gNV9KGb8thSsNjpSL0n8PARn9HuZOnIxN0hoP+VmmDGMN5t9UJ0Z" crossorigin="anonymous">

    <title>Hello, world!</title>
  </head>
  <body>
    <h1>Hello, world!</h1>

    <!-- Optional JavaScript -->
    <!-- jQuery first, then Popper.js, then Bootstrap JS -->
    <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js" integrity="sha384-DfXdz2htPH0lsSSs5nCTpuj/zy4C+OGpamoFVy38MVBnE+IbbVYUew+OrCXaRkfj" crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/popper.js@1.16.1/dist/umd/popper.min.js" integrity="sha384-9/reFTGAW83EW2RDu2S0VKaIzap3H66lZH81PoYlFhbGU+6BZp6G7niu735Sk7lN" crossorigin="anonymous"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js" integrity="sha384-B4gt1jrGC7Jh4AgTPSdUtOBvfO8shuf57BaghqFfPlYxofvL8/KUEfYiJOMMV+rV" crossorigin="anonymous"></script>
  </body>
</html>
```

## Utilisation

Vous êtes normalement capable d'utiliser des classes CSS, et bien Bootstrap ce n'est que ça au final. Une grosse bibliothèque de classes pensées pour le responsive et la conception facile de template HTML.

### Container

Bootstrap propose une classe `container`qui permet d'avoir un contenu flexible facilement. Le container est nécessaires pour pouvoir utiliser leurs système de grid personnalisé (voir point suivant).

```html
<div class="container">...</div>
```

#### Fluid container

Il existe aussi une classe pour avoir un container fluide, qui prends toute la largeur disponible.

```html
<div class="container-fluid">...</div>
```

#### Responsive container

Il existe aussi des classes pour gérer les différents breakpoint de vos containers.

```html
<div class="container-sm">100% wide until small breakpoint</div>
<div class="container-md">100% wide until medium breakpoint</div>
<div class="container-lg">100% wide until large breakpoint</div>
<div class="container-xl">100% wide until extra large breakpoint</div>
```

[:book: Voir la documentation](https://getbootstrap.com/docs/4.5/layout/overview/#containers)

### Grid

Bootstrap utilise **Flexbox** pour créer un système de grille personnalisé qui facilite la mise en page de vos éléments.

Le principe est simple, votre page est divisée en 12 colonnes, vous n'avez qu'a utilisé la classe `col-x` pour afficher une ligne de `x` colone.

```html
<div class="container">
  <div class="row">
    <div class="col-4">
    <div class="col-4">
    <div class="col-4">
  </div>
  <div class="row">
    <div class="col-2">
    <div class="col-6">
    <div class="col-4">
  </div>
</div>
```


### Components

