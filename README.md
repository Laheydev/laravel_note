# laravel_note
Note de cours

Initialisation du projet pour laravel 7

- composer create-project --prefer-dist laravel/laravel Nom_appli
- création de la base de données
- creer le fichier.env avec les configurations locales
- initialisation du git
- npm instal
- composer instal
- composer require laravel/ui
- php artisan ui bootstrap --auth
- création du task.json pour lancer les tâches automatiques dans visual studio code, npm run watch et php artisan serve
- génère clé laravel php artisan key:generate
- créer le lien symbolique php artisan storage:link

Commande principale artisan 

- php artisan make:model Models/NomModel
- php artisan route:liste
- php artisan make:migration
- php artisan migrate
- php artisan db:seed
- php artisan make:controller NomController
- php artisan cache:clear
- php artisan make:middleware NomMIddleware

Route et réponses

- création de préfixes pour regrouper un ensemble de route concernant une partie du site:
=> Route::group(['prefix'=>'admin'], function() {
    "Déclaration des routes"
}) ;
- création de middleware globaux pour protéger les acces. 

=> 
