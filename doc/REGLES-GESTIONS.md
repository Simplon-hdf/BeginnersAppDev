
## Règles de gestion



# Un utilisateur 

- Un compte utilisateur contient un pseudo 
- Un compte utilisateur contient une adresse mail
- Un compte utilisateur contient un mot de passe
- Un compte utilisateur contient un niveau de privilège 2 lors de la création du compte

# Les niveaux de privilèges 

- Les niveaux de privilèges ne sont modifiable que par un compte ayant un niveau de privilège au minimum Administrateur 

Les niveaux de privilèges:

1- Visiteur
2- Utilisateur connecté 
3- Modérateur
4- Administrateur
5- Super-Administrateur

# Tags 

- Un tag contient un intitule (ex : c#, PHP, IA)

# Articles 

- Un article est composé d'un titre
- Un article est composé d'une courte description
- Un article est composé une zone de texte
- Un article peut contenir des liens vers des sources externes
- Un article est écrit par un utilisateur connecté 
- Un article contient le pseudo de l'auteur de l'article
- Un article contient le nombre de fois qu'il a été placer en favoris 
- Un article ne peut pas avoir le même titre qu'un autre article
- Un article peut être relié à un ou plusieurs tags 

# Gestion des articles

- Un article ne peut être ajouté que par un compte ayant au minimum le niveau de privilège d'un utilisateur de l'application.
- Un article ne peut être modéré que par un compte ayant au minimum le niveau de privilège d'un modérateur
- Un article ne peut être visible qu'après avoir été modéré par un compte ayant le niveau de privilège nécessaire 
- Un article peut être signalé
- Un article peut être noté par d'autres utilisateurs 
- Un article peut être placer dans les favoris d'un utilisateur connecté

# Les ressources éducatives 

- Une ressource peut être un Cheat Sheet, une bibliothèque de tutotiel sur des langages de programmations/outils
- Une ressource peut contenir des liens vers des sites externes (documentation officielle d'un lanagage de programmation)
- Une ressource contient un titre 
- Une ressource contient une description 
- Une ressource peut contenir du code 
- Une ressource ne peut pas avoir le même titre qu'une autre ressource 
- Une ressource peut être relié à un ou plusieurs tags 

# Gestion des ressources éducatives 

- Une ressource peut être placer en favoris par un utilisateur connecté
- Une ressource doit être ajoutée par un compte ayant au minimum le niveau de privilège d'un modérateur
- Une ressource peut être commenter par des utilisateurs connectés 

# Les Commentaires 

- Un utilisateur doit être connecté pour pouvoir commenter une ressource ou un article
- Les ressources et les articles de l'application dispose d'une section commentaire en bas de page 

# Un commentaire

- Un commentaire est relié à un contenu (ressource ou article) OU à un commentaire
- Un commentaire est ajouté par un utilisateur connecté 
- Un commentaire a une date d'ajout 
- Un commentaire ne peut pas contenir d'adresse mail  
- Un commentaire ne peut pas permettre l'exécution de code sur l'application

# Gestion des commentaires

- Chaque commentaire doit être relié à un utilisateur. Son pseudo doit être visible ainsi que la date à laquelle il a ajouté le commentaire 
- Un utilisateur ne peut pas supprimer ou modifier le commentaire d'un autre utilisateur 
- Un commentaire peut être signaler y compris par un visiteur 
- Un commentaire peut être relier à un autre commentaire en tant que réponse 

# Favoris 

- Un utilisateur doit être connecté pour ajouter des contenus en favoris (articles et ressources)"

# Modération de contenus

- Cette section ne peut être accessible que par un compte ayant un niveau de privilège au minimum de modérateur

# Tableau de bord Utilisateur

- Le tableau de bord n'est accessible que par un utilisateur connecté 
- Le tableau de bord contient les titres des contenus placés en favoris par l'utilisateur 
- Le tableau de bord contient les tags préférées de l'utilisateur 

# Gestion du tableau de bord utilisateur

- Un utilisateur peut enlever des contenus de son tableau de bord 
- Un utilisateur peut ajouter des contenus à son tableau de bord

# Tableau de bord Modérateur 

- Le tableau de bord modérateur n'est accessible qu'avec un compte connecté ayant un niveau de privilège à minima de modérateur 
- Le tableau de bord modérateur contient une partie modération des commentaires 
- Le tableau de bord modérateur contient une partie modération des articles
- Le tableau de bord modérateur contient une partie ajout de ressources
- le tableau de bord modérateur contient une partie tendances et besoins utilisateurs 

# Planifier une discussion sur un thème 

- La Planification de la discussion est gérer par Calendly 
- Un utilisateur doit être connecté pour proposer une session d'échange 
- Une discussion est reliée à un ou plusieurs tags 

# Recherche de contenus

- Une recherche de contenus peut être effectuer par tous y compris les visiteurs 
- Les ressources peuvent être rechercher selon le titre du contenu OU le(s) tags auquelles elles sont reliées
- La recherche trie les résultats obtenus selon la correspondance de la recherche puis la date d'ajout (du plus récent au plus ancient) sur l'application

# Tendances et besoins utilisateurs 

- Le tableau de bord modérateur n'est accessible qu'avec un compte connecté ayant un niveau de privilège à minima de modérateur 
- Cette partie contient les statistiques en fonction du type de contenu 
- Les tendances contiennent un tableau des tags en fonction du nombre de contenus dans l'application et du nombre de visiteur total, du nombre d'utilisateur ayant placé en favoris 
- Les tendances contiennent un tableau des contenus, du nombre de commentaires, du nombre de visiteur et de nombre de fois placés en favoris

# Modération des utilisateurs 

- Un utilisateur peut signaler le commentaire d'un autre utilisateur alors celui-ci sera modérer. 
- Un compte utilisateur peut être desactiver par un compte ayant au moins le niveau de privilège d'un modérateur 
- Un compte utilisateur peut être supprimer par un compte ayant au moins le niveau de privilège d'un modérateur 