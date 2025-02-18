# Gestionnaire de Tâches avec Symfony 7

## Description
Ce projet est une application de gestion de tâches simple, construite avec Symfony 7. Il implémente les opérations CRUD (Créer, Lire, Mettre à jour, Supprimer) pour les tâches, en utilisant Doctrine ORM, Twig, et le composant Form de Symfony.

## Prérequis
Avant de commencer, assurez-vous d'avoir les outils suivants installés sur votre machine :
- PHP 8.2 ou plus
- Composer
- Symfony CLI
- SQLite (ou une autre base de données supportée par Doctrine)

## Installation

1. Clonez le dépôt :
   ```bash
   git clone https://github.com/votre-repo/task-manager.git
   cd task-manager
   ```

2. Installez les dépendances :
   ```bash
   composer install
   ```

3. Configurez la base de données :
   - Assurez-vous que SQLite est installé en vérifiant avec la commande :
     ```bash
     php -m | grep pdo_sqlite
     ```
   - Si besoin, installez SQLite :
     ```bash
     sudo apt install php-sqlite3
     ```
   - Modifiez le fichier `.env` et définissez la connexion à SQLite :
     ```ini
     DATABASE_URL="sqlite:///%kernel.project_dir%/var/data.db"
     ```
   - Créez la base de données :
     ```bash
     php bin/console doctrine:database:create
     ```
   - Effectuez les migrations :
     ```bash
     php bin/console doctrine:migrations:migrate
     ```

4. Lancez le serveur de développement :
   ```bash
   symfony server:start
   ```
   L'application sera accessible sur [http://127.0.0.1:8000](http://127.0.0.1:8000)

## Fonctionnalités
- Création de tâches avec un titre, une description et une date d'échéance.
- Affichage de la liste des tâches enregistrées.
- Mise à jour et modification des tâches.
- Suppression des tâches.

## Commandes utiles
- Génération d'un contrôleur :
  ```bash
  php bin/console make:controller NomDuControleur
  ```
- Génération d'une entité :
  ```bash
  php bin/console make:entity NomDeLEntite
  ```
- Génération d'une migration :
  ```bash
  php bin/console make:migration
  ```
- Exécution des migrations :
  ```bash
  php bin/console doctrine:migrations:migrate
  ```
- Génération automatique des opérations CRUD :
  ```bash
  php bin/console make:crud Task
  ```

## Technologies utilisées
- Symfony 7
- Doctrine ORM
- Twig
- SQLite


