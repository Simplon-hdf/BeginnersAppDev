<img src="./../Assets/Images/Role-Based-Access-Control.png" alt="RBAC" width="500">

Ce tableau aligne les permissions et les actions possibles pour chaque rôle selon les exigences et les scénarios d'utilisation détaillés dans nos User Stories. Il est conçu pour faciliter la compréhension des responsabilités et des capacités de chaque rôle au sein de la plateforme, assurant ainsi que les objectifs de gestion des utilisateurs, de modération des contenus et d'engagement des utilisateurs sont atteints efficacement.

### Vue d'ensemble :

| Autorisations / Rôle                                          | Visiteur | Membre | Modérateur | Administrateur | Super Administrateur |
| ------------------------------------------------------------- | -------- | ----------- | ---------- | -------------- | -------------------- |
| Gestion de l'authentification et accès à contenu personnalisé | ✅       | ✅          | ✅         | ✅             | ❌                   |
| Créer un compte membre                             | ✅       | ✅          | ✅         | ✅             | ❌                   |
| Modifier son compte                           | ❌       | ✅          | ✅         | ✅             | ❌                   |
| Désactiver son compte                           | ❌       | ✅          | ✅          | ✅             | ❌                   |
| Recevoir des notifications en cas de suppression de contenu   | ❌       | ✅          | ✅         | ✅             | ❌                   |
| Soumission de ressources                     | ❌       | ✅          | ✅         | ✅             | ❌     
| Accès à un rapport d'activité de ses ressources                 | ❌       | ✅          | ✅         | ✅             | ❌                   |
| Proposer une session d'échange                 | ❌       | ✅          | ✅         | ✅             | ❌                   |
| Publication de ressources                    | ❌       |  ❌         | ✅         | ✅             | ❌               |
| Accès à une interface de modération                           | ❌       | ❌          | ✅         | ✅             | ❌                   |
| Anonymisation de contenus non conformes                         | ❌       | ❌          | ✅         | ✅             | ❌                   |
| Accès à un rapport d'activité de modération                   | ❌       | ❌          | ✅         | ✅             | ❌                   |
| Créer un compte modérateur                                 | ❌       | ❌          | ❌         | ✅             | ❌                   |
| Désactiver des comptes modérateurs                             | ❌       | ❌          | ❌         | ✅             | ❌                   |
| Attribuer/modifier des rôles                                  | ❌       | ❌          | ❌         | ✅             | ❌                   |
| Créer des administrateurs                                     | ❌       | ❌          | ❌         | ❌             | ✅                   |
| Modifier des administrateurs                                  | ❌       | ❌          | ❌         | ❌             | ✅                   |
| Désactiver des administrateurs                                 | ❌       | ❌          | ❌         | ❌             | ✅                   |

