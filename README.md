<<<<<<< HEAD
#  Blog API - Backend

[![Node.js](https://img.shields.io/badge/Node.js-20.x-339933?logo=node.js&logoColor=white)](https://nodejs.org/)
[![Express.js](https://img.shields.io/badge/Express.js-4.x-000000?logo=express&logoColor=white)](https://expressjs.com/)
[![SQLite](https://img.shields.io/badge/SQLite-3.x-003B57?logo=sqlite&logoColor=white)](https://www.sqlite.org/)

API RESTful complète pour la gestion d'un blog. Développée dans le cadre de l'UE **INF222 – Développement Backend**, ce projet illustre la mise en œuvre d'une architecture backend robuste et maintenable.

---

##  Fonctionnalités

-  **CRUD complet** pour les articles de blog
-  **Recherche flexible** par titre ou contenu
-  **Validation des données** côté serveur
-  **Gestion centralisée des erreurs**
-  **Architecture MVC** (Modèle-Vue-Contrôleur)
-  **Base de données SQLite** – aucune configuration supplémentaire nécessaire
-  **Code modulaire et évolutif**

---

##  Stack Technique

| Composant       | Technologie                     |
| :-------------- | :------------------------------ |
| **Runtime**     | Node.js                         |
| **Framework**   | Express.js                      |
| **Base de données** | SQLite (avec `sqlite3`)     |
| **Tests API**   | Postman / Insomnia              |

---

##  Architecture du Projet

blog-api/

├──  controllers/ # Logique métier (traitement des requêtes)

   └── articleController.js

├──  routes/ # Définition des endpoints

   └── articleRoutes.js

├──  database.js # Configuration et connexion SQLite

├──  server.js # Point d'entrée de l'application

├──  package.json # Dépendances et scripts

└──  README.md # Documentation du projet
text


---

##  Installation et Utilisation

### 1. Cloner le dépôt
```bash
git clone https://github.com/blaise-wafo/API-backend.git
cd API-backend
```
### 2. Installer les dépendances

```bash
npm install
```
### 3. Lancer le serveur

```bash
node server.js
```
Le serveur démarre sur http://localhost:3000 
![alt text](<Capture d’écran du 2026-03-23 01-47-54.png>)
### Documentation de l'API

L'API respecte les conventions REST et utilise les codes de statut HTTP standards.
 Endpoints disponibles
Méthode	Endpoint	Description

POST	/api/articles	Créer un nouvel article

GET	/api/articles	Récupérer tous les articles

GET	/api/articles/:id	Récupérer un article par son ID

PUT	/api/articles/:id	Modifier un article existant

DELETE	/api/articles/:id	Supprimer un article

GET	/api/articles/search	Rechercher (?query=mot-clé)
 Exemple de corps de requête (POST /api/articles)
 ```bash
json

{
  "titre": "Apprendre Node.js",
  "contenu": "Guide complet sur le développement backend avec Node.js et Express.",
  "auteur": "Blaise Wafo",
  "date": "2026-03-21",
  "categorie": "Développement",
  "tags": "backend, nodejs, express, sql"
}
```
 ### Codes de statut HTTP utilisés

    200 OK – Requête réussie

    201 Created – Ressource créée avec succès

    400 Bad Request – Données invalides ou manquantes

    404 Not Found – Ressource introuvable

    500 Internal Server Error – Erreur serveur

 ### Tests avec Postman

Un environnement de test est disponible. Importez la collection Postman fournie pour tester rapidement tous les endpoints.
 Bonnes Pratiques Implémentées

![alt text](<Capture d’écran du 2026-03-23 01-29-48.png>)

     Validation stricte des données entrantes (titre, auteur obligatoires)

     Modularité du code (séparation des responsabilités)

     Gestion d'erreurs centralisée avec messages appropriés

     Documentation claire et complète

### Auteur

Blaise Wafo

 Filière : Informatique 
 UE : INF222 – Programmation Web

