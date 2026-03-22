Blog API Engine — Service Backend Professionnel
 Présentation du Projet

Ce projet constitue le cœur d'un système de gestion de contenu (CMS) performant. Développé pour l'unité INF222 , il implémente les standards modernes du développement web pour offrir une expérience fluide entre la plateforme d'apprentissage CleeRoute et une application réelle.
🛠 Stack Technique & Écosystème
Composant	Technologie	Rôle
Runtime	Node.js	Environnement d'exécution asynchrone
Framework	Express.js	Gestion du routage et des middlewares
Database	SQLite / MongoDB	

Persistance relationnelle ou document
Documentation	Swagger UI	

Interface interactive pour tester l'API
Test Tool	Postman	

Validation des endpoints et debugging
 Architecture Modulaire (Pattern MVC)

Le projet adopte une séparation stricte des préoccupations (SoC) pour garantir une évolutivité maximale:
Bash

blog-api/
├──  controllers/   #  Intelligence : Logique métier et pilotage des données
├──  routes/        #  Aiguillage : Définition des chemins d'accès API
├──  models/        #  Structure : Schémas et interactions base de données
├──  database.js    #  Connectivité : Configuration de la persistance
├──  server.js      #  Ignition : Point d'entrée et configuration Express
└──  package.json   #  Manifeste : Gestion des scripts et dépendances

 Interface de Programmation (API)
 Gestion des Articles

L'API utilise les conventions de succès et d'échec HTTP pour une communication transparente.
Méthode	Endpoint	Action	Payload
POST	/api/articles	

Créer un article
	{titre, contenu, auteur...}
GET	/api/articles	

Lister (Filtres disponibles)
	?categorie=Tech
GET	/api/articles/:id	

Consulter par ID unique
	--
PUT	/api/articles/:id	

Mettre à jour (Partiel)
	{titre, tags...}
DELETE	/api/articles/:id	

Supprimer définitivement
	--
GET	/api/articles/search	

Recherche plein texte
	?query=mot-clé
 Qualité & Sécurité du Code

    Validation d'Entrée : Utilisation de règles strictes pour rejeter les requêtes malformées (ex: titre obligatoire, contenu > 10 caractères).

    Codes de Statut Standardisés : 

        201 : Création confirmée.

        400 : Requête invalide (Bad Request).

        404 : Ressource introuvable.

        500 : Incident serveur.

    Performance : Recherche optimisée via des paramètres de requête.

 Déploiement Rapide

    Récupération : git clone https://github.com/blaise-wafo/API-backend.git

    Initialisation : npm install

    Lancement : npm start (Accessibilité sur http://localhost:3000)

 Informations Académiques

    Auteur : Blaise Wafo

    Filière : Informatique (Génie Logiciel)

    Enseignant : Charles Njiosseu, PhD Student 

    Contexte : TAF 1 – Utilisation de Cleeroute (Date limite : 23/03/2026)