Blog API – Système de Gestion de Contenu (Backend)
 Présentation du Projet

Ce projet consiste en la conception et le développement d'une API RESTful pour la gestion d'un blog. Il a été réalisé dans le cadre de l'unité d'enseignement INF222 - Développement Backend. L'objectif est de structurer un apprentissage efficace en programmation web en s'appuyant sur la plateforme CleeRoute.
 Stack Technique

    Environnement d'exécution : Node.js.

    Framework Web : Express.js.

    Base de Données : SQLite (Persistance des données).

    Tests & Debugging : Postman.

 Architecture du Projet

Le projet suit une séparation claire entre les routes, les contrôleurs et les modèles pour garantir la maintenabilité du code.
Plaintext

blog-api/
├── controllers/    # Logique métier (traitement des requêtes)
├── routes/         # Définition des points de terminaison (endpoints)
├── database.js     # Configuration et connexion SQLite
├── server.js       # Point d'entrée de l'application
├── package.json    # Dépendances et scripts
└── README.md       # Documentation du projet

 Installation et Utilisation
1. Cloner le dépôt
Bash

git clone https://github.com/blaise-wafo/API-backend.git
cd API-backend

2. Installer les dépendances
Bash

npm install

3. Lancer le serveur
Bash

node server.js

    Le serveur sera accessible sur : http://localhost:3000

 Documentation des Endpoints

L'API respecte les conventions REST et utilise les codes de statut HTTP appropriés (200, 201, 400, 404, 500).
Méthode	Endpoint	Description
POST	/api/articles	

Créer un nouvel article
GET	/api/articles	

Récupérer tous les articles
GET	/api/articles/:id	

Lire un article spécifique via son ID
PUT	/api/articles/:id	

Modifier un article existant
DELETE	/api/articles/:id	

Supprimer un article définitivement
GET	/api/articles/search	

Recherche par titre ou contenu (?query=...)
Exemple de corps de requête (POST)
JSON

{
  "titre": "Apprendre Node.js",
  "contenu": "Guide complet sur le développement backend...",
  "auteur": "Blaise Wafo",
  "date": "2026-03-21",
  "categorie": "Développement",
  "tags": "backend, nodejs, sql"
}

 Fonctionnalités & Bonnes Pratiques

    Validation des données : Vérification des champs obligatoires (titre, auteur) avant insertion.

    Gestion d'erreurs : Réponses claires en cas de ressources non trouvées ou de requêtes mal formées.

    Modularité : Structure organisée pour faciliter l'évolution du backend.

 Auteur

    Nom : Blaise Wafo 

    Filière : Informatique (Génie Logiciel) 

    UE : INF222 – Programmation Web 

Projet réalisé pour le TAF 1 - Utilisation de CleeRoute (Mars 2026).