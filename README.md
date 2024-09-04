# FirstCrudG2

## Installation 

Installationj de la derniere version stable avec les dependaences courantes pour un site web

    symfony new FirstCrudG2 --webapp

    cd FirstCrudG2

### Mise à jour composer 

    composer self-update

### Mise en route server

    symfony serve -d

### Creation d'un crontroleur

    php bin/console make:controller HomeController

2 fichiers sont créés, le controleur et sa vue

     created: src/Controller/HomeController.php
     created: templates/home/index.html.twig

### Pour voir le chemin  genere pour le controleur

    php bin/console debug:route

### Pour le fichier 

```php
<?php
#src/Controller/Homecontroller.php

# ...
  #[Route('/home', name: 'app_home')]
    public function index(): Response
    {
        return $this->render('home/index.html.twig', [
            'controller_name' => 'HomeController',
        ]);
# ...
```
on souhaite avoir cette page comme accueil reel de notre site

```php
<?php
#src/Controller/Homecontroller.php

# ...
  #[Route('/', name: 'homepage')]
    public function index(): Response
    {
        return $this->render('home/index.html.twig', [
            'controller_name' => 'HomeController',
        ]);
# ...
```


