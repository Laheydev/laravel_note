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

- création de préfixes pour reg'*4fzrouper un ensemble de route concernant une partie du site:
=> Route::group(['prefix'=>'admin'], function() {
    "Déclaration des routes"
}) ;
- création de middleware globaux pour protéger les acces. 

=> création du middleware avec les règles dans le bsande puis déclaration du middleware dans app/http/kennel.php
Dans le routeMiddleware
=> ensuite assignation du middleware à une route ou un ensemble
=> Route::middleware(['admin'])->group .... 

Model

- déclaration des propriétés de type date pour les manipuler avec carbon 
=> protected $dates =['propriété'];
- déclaration des propriétés definissables avec la méthode create
=> protected $fillable =['propriété']
- utilisation du softdelete
=> avec SoftDelete au model et ajout d un champ date deleted_at

Relations

-one to one
=> relation unique entre deux entités 
=> ajout de la clé étrangère dans la table appartenant
=> ajout d une methode au singulier de chaque entite dans l autre
=> hasOne dans la table possédante
=> belongsTo dans la table appartenante

- one to many
=> une entité ayant des relations avec plusieurs autres entités
=> ajout de la clé étrangère dans la table appartenante
=> ajout d une méthode au pluriel dans le model possédante avec 
=> ajout d une méthode utilisée singulier dans le model appartenant
=> hasMany dans la possédante
=> belongsTo dans l appartenante

- Many to many
=> relation multiples entre plusieurs entites
=> création d une table pivot sans model
=> ajout des clés étrangères de chaque entités dans le pivot
=> ajout de méthodes au pluriel dans chaque model
=> belongsToMany dans chaque modèle



