# Projet 8 — Analyse de données sociodémographiques avec SQL et dbt

## Présentation du projet

Ce projet a été réalisé dans le cadre de ma formation Data Analyst chez OpenClassrooms.

L'objectif est de préparer, nettoyer et enrichir des données sociodémographiques afin de construire un jeu de données exploitable pour l'analyse.

## Objectifs du projet

- Préparer les données brutes.
- Nettoyer et standardiser les variables.
- Enrichir les données avec les informations de population.
- Organiser les transformations en plusieurs étapes.
- Préparer les données pour de futures analyses.

## Technologies utilisées

- SQL
- Snowflake
- Approche de modélisation dbt
- GitHub

## Étapes de réalisation

### Étape 1 — Préparation des données

Fichier : students_staging.sql

Création d'une vue STUDENTS_STAGING à partir des données brutes STUDENTS_RAW.

Variables sélectionnées :
- USER_ID
- AGE_GROUP
- GENDER
- REGION
- YEAR_PATH_STARTED

### Étape 2 — Nettoyage des données

Fichier : students_clean.sql

Création d'une vue STUDENTS_CLEAN.

Utilisation de la fonction SQL TRIM() pour supprimer les espaces superflus dans les variables AGE_GROUP, GENDER et REGION.

### Étape 3 — Enrichissement des données

Fichier : students_demography_final.sql

Création de la vue STUDENTS_DEMOGRAPHY_FINAL.

Réalisation d'une jointure LEFT JOIN entre STUDENTS_CLEAN et POPULATION_CLEAN sur la variable REGION.

Cette étape permet d'ajouter les informations de population aux données des étudiants.

## Fichiers disponibles

- students_staging.sql : préparation des données.
- students_clean.sql : nettoyage et standardisation.
- students_demography_final.sql : enrichissement avec la population.

## Compétences développées

- Requêtes SQL
- Création de vues
- Nettoyage de données
- Jointures SQL
- Structuration des transformations
- Documentation technique
- Préparation des données pour l'analyse

## Résultat du projet

Le projet présente une chaîne de transformation SQL organisée en trois niveaux :

Données brutes → Staging → Nettoyage → Enrichissement

Les scripts illustrent une approche de modélisation inspirée de dbt. Ce dépôt ne contient pas un projet dbt complet et exécutable.

## Auteur

Roger AGNEROH

Data Analyst Junior — Formation OpenClassrooms

Portfolio :
https://agnerohroger-arch.github.io/
