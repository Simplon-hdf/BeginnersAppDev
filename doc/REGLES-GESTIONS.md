
## Règles de gestion



# Un compte utilisateur 

- Un compte utilisateur contient un pseudo 
- Un compte utilisateur contient une adresse mail
- Un compte utilisateur contient un mot de passe
- Un compte utilisateur contient un niveau de privilège 2 lors de la création de celui-ci

# Les niveaux de privilèges 

- Les niveaux de privilèges ne sont modifiables que par un compte ayant un niveau de privilège au minimum Administrateur 

Les niveaux de privilèges:

1- Visiteur
2- Utilisateur connecté 
3- Modérateur
4- Administrateur
5- Super-Administrateur

# Tags 

- Un tag contient un intitule (exemple : c#, PHP, IA)

# Articles 

- Un article est composé d'un titre
- Un article est composé d'un résumé
- Un article est composé d'une description
- Un article peut contenir des liens vers des sources externes
- Un article contient le pseudo de l'utilisateur ayant écrit l'article
- Un article contient le nombre de fois qu'il a été placé en favoris 
- Un article ne peut pas avoir le même titre qu'un autre article
- Un article peut être relié à un ou plusieurs tags 

# Gestion des articles

- Un article ne peut être ajouté que par un compte ayant au minimum le niveau de privilège d'un utilisateur de l'application.
- Un article ne peut être modéré que par un compte ayant au minimum le niveau de privilège d'un modérateur
- Un article ne peut être visible qu'après avoir été modéré par un compte ayant le niveau de privilège nécessaire 
- Un article peut être signalé par tous les lecteurs y compris les visiteurs de l'application
- Un article peut être noté par d'autres utilisateurs connectés 
- Un article peut être placé dans les favoris d'un utilisateur connecté par celui-ci

# Les ressources éducatives 

- Une ressource peut être un Cheat Sheet, une bibliothèque de tutoriel sur les langages de programmation, ...
- Une ressource peut contenir des liens vers des sites externes (documentation officielle d'un langage de programmation)
- Une ressource contient un titre 
- Une ressource contient une description 
- Une ressource peut contenir du code 
- Une ressource ne peut pas avoir le même titre qu'une autre ressource 
- Une ressource peut être reliée à un ou plusieurs tags 

# Gestion des ressources éducatives 

- Une ressource peut être placée en favoris par un utilisateur connecté
- Une ressource doit être ajoutée par un compte ayant au minimum le niveau de privilège d'un modérateur
- Une ressource peut être commentée par des utilisateurs connectés 

# Les commentaires 

- Un utilisateur doit être connecté pour pouvoir commenter une ressource ou un article
- Les ressources et les articles de l'application disposent d'une section commentaire en bas de page 

# Un commentaire

- Un commentaire doit être relié à un contenu (ressource ou article) OU à un commentaire d'un contenu
- Un commentaire est ajouté par un utilisateur connecté 
- Un commentaire a une date d'ajout 
- Un commentaire ne peut pas contenir d'adresse mail  
- Un commentaire ne peut pas permettre l'exécution de code sur l'application

# Gestion des commentaires

- Chaque commentaire doit être relié à un utilisateur. Son pseudo doit être visible ainsi que la date à laquelle il a ajouté le commentaire 
- Un utilisateur ne peut pas supprimer ou modifier le commentaire d'un autre utilisateur 
- Un commentaire peut être signalé y compris par un visiteur 
- Un commentaire peut être relié à un autre commentaire en tant que réponse 

# Favoris 

- Un utilisateur doit être connecté pour ajouter des contenus en favoris (articles et ressources)

# Modération de contenus

- Cette section ne peut être accessible que par un compte ayant un niveau de privilège au minimum de modérateur

# Tableau de bord utilisateur

- Le tableau de bord n'est accessible que par un utilisateur connecté 
- Le tableau de bord contient les titres des contenus placés en favoris par l'utilisateur 
- Le tableau de bord contient les tags des contenus les plus visités par l'utilisateur 

# Gestion du tableau de bord utilisateur

- Un utilisateur peut enlever des contenus de son tableau de bord 
- Un utilisateur peut ajouter des contenus à son tableau de bord

# Tableau de bord modérateur 

- Le tableau de bord modérateur n'est accessible qu'avec un compte connecté ayant un niveau de privilège au minimum de modérateur 
- Le tableau de bord modérateur contient une partie modération des commentaires 
- Le tableau de bord modérateur contient une partie modération des articles
- Le tableau de bord modérateur contient une partie ajout de ressources
- le tableau de bord modérateur contient une partie tendance et besoins utilisateur 

# Planifier une discussion sur un thème 

- La planification de la discussion est gérée par Calendly 
- Un utilisateur doit être connecté pour proposer une session d'échange 
- Une discussion est reliée à un ou plusieurs tags 

# Recherche de contenus

- Une recherche de contenus peut être effectuée par tous y compris les visiteurs 
- Les ressources peuvent être recherchées selon le titre du contenu OU les tags auxquelles elles sont reliées
- La recherche trie les résultats obtenus selon la correspondance de la recherche puis la date d'ajout (du plus récent au plus anciens) sur l'application

# Tendances et besoins utilisateur 

- Le tableau de bord modérateur n'est accessible qu'avec un compte connecté ayant un niveau de privilège au minimum de modérateur 
- Cette partie contient les statistiques en fonction du type de contenu 
- Les tendances contiennent un tableau des tags par nombre de contenus dans l'application, nombre de visiteurs total et nombre d'utilisateurs ayant placé en favoris un contenu de ce tag 
- Les tendances contiennent un tableau des contenus, du nombre de commentaires reliés aux contenus, du nombre de visiteurs et du nombre de fois placés en favoris

# Modération des utilisateurs 

- Un utilisateur peut signaler le commentaire d'un autre utilisateur 
- Le compte d'un utilisateur en cours de modération est désactivé. Il ne peut plus se connecter à l'application.  
- Un compte utilisateur peut être désactivé par un compte ayant au moins le niveau de privilège d'un modérateur 
- Un compte utilisateur peut être supprimé par un compte ayant au moins le niveau de privilège d'un modérateur 