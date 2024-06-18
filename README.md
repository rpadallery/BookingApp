# Projet d'Application de Voyage - README

## Introduction

Bienvenue sur le dépôt de notre application de voyage, une solution web complète permettant aux utilisateurs de rechercher et réserver des trajets de voyage. Ce projet utilise des technologies modernes pour développer, tester, et déployer une application web robuste et scalable. L'application est composée d'un frontend et d'un backend, tous deux développés en JavaScript, et elle est intégrée avec divers services et outils pour assurer une qualité et une performance optimales.

## 1. Initialisation du Projet

### Dépôts GitHub

Le projet est hébergé sur GitHub avec deux dépôts séparés pour le frontend et le backend, tous deux initialisés depuis des exemples d'application web et hébergés sur des dépôts GitHub privés pour assurer la confidentialité et le contrôle.

### GitHub Flow

Nous avons mis en place un GitHub flow avec plusieurs branches structurées pour faciliter le développement, les tests, et les déploiements :
- `production` : Branche principale pour les versions stables en production.
- `main` : Branche utilisée pour la pré-production.
- Branches de fonctionnalités : Créées pour chaque nouvelle fonctionnalité ou correction de bug.

## 2. Configuration du Projet

### Variables d'Environnement

Un fichier `.env` a été ajouté au backend pour gérer les variables d'environnement sensibles. La connexion à MongoDB Atlas est gérée par la variable `CONNECTION_STRING`, configurée selon les instructions détaillées dans des vidéos explicatives.

### Base de Données

La base de données MongoDB héberge une collection de voyages appelée `trips`, initialisée à partir du fichier `trips.json` fourni. Cette configuration permet de démarrer rapidement avec des données prédéfinies.

## 3. Tests Cypress

### Tests Automatisés

Nous avons intégré Cypress pour les tests end-to-end, garantissant la fiabilité des fonctionnalités critiques de l'application. Voici quelques tests implémentés :
- Recherche de trajets Paris-Bruxelles pour la date du jour.
- Fonction de réservation.
- Suppression d'éléments du panier.
- Fonction d'achat.

### Intégration Continue

Ces tests sont exécutés automatiquement dans une pipeline CI/CD, intégrée avec GitHub Actions pour assurer une vérification continue de la qualité du code.

## 4. Tests de Montée en Charge

### Utilisation de Ddosify

Ddosify a été intégré dans notre pipeline CI/CD pour effectuer des tests de montée en charge. Cela permet de s'assurer que notre application peut gérer des pics de trafic et rester performante sous une forte demande.

## 5. Tests de Securité et de Qualité du code

### Analyse de Code avec SonarQube

SonarQube a été intégré pour analyser la qualité du code du frontend, permettant de détecter et de corriger les erreurs potentielles et d'améliorer la maintainabilité du code.

## 5. Déploiement Continu

### Déploiement sur AWS EC2

Le frontend et le backend sont déployés automatiquement sur des instances AWS EC2 :
- **Frontend** : Déployé sur une instance EC2 dédiée après avoir passé les tests sur l'environnement de test.
- **Backend** : Déployé sur une instance EC2 avec configuration de redondance et de scalabilité pour assurer une haute disponibilité.


## Remarques Importantes

- **Optimisation des Runners GitHub** :
  - Nous avons optimisé l'utilisation des runners GitHub pour gérer efficacement les crédits disponibles pendant le développement et les tests.

- **Vérification en Production** :
  - Une étape de vérification a été ajoutée dans notre pipeline pour garantir que l'application est correctement déployée et fonctionnelle en environnement de production.

