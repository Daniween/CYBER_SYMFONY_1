# 🛡️ Projet Symfony – Atelier Sécurité Web

Ce projet Symfony contient volontairement des **vulnérabilités OWASP** à découvrir et corriger.  
L’objectif pédagogique : apprendre à détecter et corriger des failles de sécurité courantes.

---

## ⚙️ Prérequis

-   PHP **>= 8.1**
-   [Composer](https://getcomposer.org/download/)
-   [Symfony CLI](https://symfony.com/download)

---

## 🚀 Installation

Cloner le dépôt :

```bash
git clone https://github.com/Daniween/BTS_CYBER_SYMFONY_1.git
cd BTS_CYBER_SYMFONY_1
composer install
```

## 🗄️ Doctrine & Base de données

Créer la base :

```bash
php bin/console doctrine:database:create
```

Exécuter les migrations (structure de la BDD) :

```bash
php bin/console doctrine:migrations:migrate
```

## 🏃 Lancer l’application

Avec le serveur Symfony CLI :

```bash
symfony serve -d
```

ou avec le serveur PHP natif :

```bash
php -S 127.0.0.1:8000 -t public
```

Accéder à l’application : 👉 [http://127.0.0.1:8000](http://127.0.0.1:8000)

## 📂 Commandes utiles Doctrine

Vérifier le mapping :

```bash
php bin/console doctrine:schema:validate
```

Créer une migration après modification des entités :

```bash
php bin/console make:migration
```

Exécuter les migrations :

```bash
php bin/console doctrine:migrations:migrate
```

## 🧪 Tests de sécurité (atelier)

Une fois le projet lancé, explorez les routes suivantes pour identifier des failles.
Objectif : pour chaque vulnérabilité → identifier l’OWASP Top 10 concerné et proposer un correctif.
