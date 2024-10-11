# Laravel Skeleton

Ce projet est un skeleton Laravel avec plusieurs packages préinstallés pour faciliter le développement. Voici les packages inclus ainsi que les commandes nécessaires pour configurer le projet après l'installation.

## Packages Inclus

- **PHPStan** : Un analyseur de code statique pour trouver des bugs dans votre code PHP.
- **PHPCS** : PHP_CodeSniffer détecte les violations des standards de codage.
- **PHPUnit** : Un framework pour les tests unitaires.
- **Clean DB** : Outil pour nettoyer la base de données entre les tests.
- **Media Library** : Gestion des médias dans Laravel.
- **Filament** : Panneau d'administration pour Laravel.
- **Breeze** : Kit de démarrage pour l'authentification.
- **Eloquent Sortable** : Ajouter une fonctionnalité de tri à vos modèles Eloquent.
- **Laravel Debug Bar** : Barre de débogage pour Laravel.
- **Laravel Sluggable** : Génère automatiquement des slugs pour vos modèles Eloquent.
- **Userback** : Outil de feedback utilisateur.
- **Sentry** : Outil de monitoring des erreurs et des performances.
- **Tailwind CSS** : Framework CSS utilitaire.

## Étapes d'installation

### 1. Fork le dépôt

### 2. Installer les dépendances
composer install
npm install

### 3. Migrer la base de données
php artisan migrate

### 4. Configurer le fichier .env
APP_URL=http://localhost

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=database_name
DB_USERNAME=root
DB_PASSWORD=
DB_DATABASE_TEST=test
DB_USERNAME_TEST=root
DB_PASSWORD_TEST=

SENTRY_DSN=https://examplePublicKey@o0.ingest.sentry.io/0

APP_USERBACK=true
APP_USERBACK_TOKEN="tokenuserback"

### 5. Générer la clé de l'application
php artisan key:generate

### 6. Exécuter les tests
Pour vérifier que tout est bien configuré, exécutez les tests unitaires :

PHPStan : vendor/bin/phpstan analyse
PHPCS : vendor/bin/phpcs

### 7. Autres commandes utiles
Clean DB : php artisan db:clean

Tailwind CSS : Pour compiler Tailwind CSS, utilise npm run dev pour le mode développement et npm run prod pour le mode production. ctrl + c pour sortir.

Stokage des fichier : php artisan storage:link

### 8. Commandes Composer
composer test =>  phpunit 
composer cs-fix =>  phpcbf 
composer cs-check =>  phpcs 
composer cs => phpcs + cbf  
composer stan =>  phpstan 
composer check-all => phpcbf + phpcs + phpstan + phpunit

## Configuration des packages
PHPStan
Pour configurer PHPStan, vous pouvez éditer le fichier phpstan.neon à la racine du projet et y ajouter vos configurations spécifiques.

PHPCS
Pour configurer PHPCS, vous pouvez éditer le fichier phpcs.xml à la racine du projet et y définir vos règles de codage.

Userback
Pour intégrer Userback, utilisez la clé API fournie dans le fichier .env pour configurer le SDK Userback dans votre projet. Le code de Userback est dans le fichier resources\views\layouts\app.blade.php

Sentry
Pour Sentry, assurez-vous que votre fichier .env contient le DSN de Sentry et que les erreurs non gérées sont capturées comme décrit dans la documentation. Vous pouvez éditer le fichier config/sentry.php.

Tailwind CSS
Pour Tailwind CSS, assurez-vous que le fichier tailwind.config.js est correctement configuré.
