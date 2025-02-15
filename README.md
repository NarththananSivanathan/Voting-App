# 🗳️ Votting App

## 📄 Description du projet

Ce projet est une application distribuée permettant à une audience de voter entre deux propositions et d'afficher les résultats en temps réel.

### 📌 Composition du projet :

- 🐍 Vote : Application web en Python permettant aux utilisateurs de voter. Un utilisateur ne peut voter qu'une seule fois par navigateur, mais il peut changer son vote à tout moment.
- ⚙️ Worker : Service en .NET qui récupère les votes depuis Redis et les stocke dans PostgreSQL.
- 📊 Result : Application web en Node.js affichant les résultats en direct.

## 🎯 Objectif

Moderniser le déploiement du projet avec Docker en conteneurisant chaque module et en orchestrant les services avec Docker Compose. L'application doit assurer la persistance des données 
et garantir un fonctionnement fluide et stable.

## 🛠️ Technologies utilisées :

Ce projet utilise les technologies suivantes :

### 📌 Back-end :

- 🐍 Python (Vote app) → Pour gérer le système de vote.
- ⚙️ .NET Core (Worker service) → Pour traiter et stocker les votes.
- 🌐 Node.js (Result app) → Pour afficher les résultats en temps réel.

### 📌 Bases de données & Messagerie :

- 🐘 PostgreSQL → Pour stocker les votes de manière persistante.
- 📝 Redis → Pour transmettre les votes en temps réel.

### 📌 Conteneurisation & Orchestration :

- 🐳 Docker → Pour conteneuriser chaque service de l’application.
- 📦 Docker Compose → Pour orchestrer les différents conteneurs et services.

## 📦 Installation

### 📋 Prérequis

- Avoir `🐳 Docker` sur sa machine

### 🪜 Étapes

1. **Construire et démarrer tous les services définis dans `docker-compose.yml` :**
   ```sh
   docker-compose up -d --build
