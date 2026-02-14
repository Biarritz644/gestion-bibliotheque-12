# gestion-bibliotheque-12
Projet Java L2 - Gestion de Bibliothèque / Médiathèque


 Présentation du Projet

Dans le cadre de notre travail académique en Java, nous avons entrepris la conception et le développement d’un '' logiciel de gestion de bibliothèque ''.

Ce projet vise à mettre en pratique :

- La programmation orientée objet (POO)
- L’architecture en couches
- Le travail collaboratif avec Git et GitHub
- L’organisation professionnelle d’un projet logiciel

 Architecture du Projet
 
L’application est structurée selon une architecture en couches séparant les responsabilités :
/backend
/model
/dao
/service
/frontend
/ui


Backend
Le backend contient la logique métier et la gestion des données.

Package '' model ''
Contient les entités principales du système :

- Livre  
- Client  
- Emprunt  

Package '' dao ''
Implémente le pattern '' Data Access Object (DAO) '' pour la gestion des données.

package '' service ''
Contient la logique métier et les règles de gestion.

 Frontend
Le frontend est contenu dans : /frontend/ui 

Il gère l’interface utilisateur et communique avec la couche service.

 Répartition des Responsabilités

 Backend

| Membre   | Entité    | Responsabilité |
|-----------|------------|---------------|
| Joseph   | Livre      | model, dao, service |
| Hermann  | Client     | model, dao, service |
| Yves     | Emprunt    | model, dao, service |

Chaque membre est responsable de son entité dans les trois couches du backend.

Frontend

| Membre | Responsabilité |
|---------|----------------|
| Kevin  | Interface utilisateur |
| Andy   | Interface utilisateur |

La répartition interne des classes UI est librement organisée entre Kevin et Andy.

 Chronologie d’Exécution

Le respect de l’ordre de développement est obligatoire :

1. Implémentation de **Livre** (Joseph)
2. Implémentation de **Client** (Hermann)
3. Implémentation de **Emprunt** (Yves)  
   ⚠ Dépend de Livre et Client
4. Intégration backend
5. Développement et connexion du frontend
6. Tests globaux



 Organisation Git

Stratégie de Branches

Chaque membre travaille sur une branche dédiée :

- `feature/livre`
- `feature/client`
- `feature/emprunt`
- `feature/ui`

La branche `main` est protégée.  
Aucun développement direct n’est autorisé dessus.

---

Workflow

```bash
# Création d’une branche
git checkout -b feature/nom-entite

# Ajouter les modifications
git add .

# Commit
git commit -m "Description claire des modifications"

ensuite
-Ouvrir une Pull resquert
