# Règles de gestion

### <span style="color: #26B260;">**1.** Application</span>

- **Accessibilité**
  - L'application doit être conforme aux normes d'accessibilité WCAG pour garantir l'accessibilité à tous les utilisateurs

### <span style="color: #26B260;">**2. Gestion des Comptes Utilisateurs**</span>

- **Création de compte**
  - Un compte utilisateur contient un pseudonyme
  - Un compte utilisateur contient une adresse mail
  - Un compte utilisateur contient un mot de passe sécurisé
  - Un compte utilisateur contient un niveau de privilège "Utilisateur connecté" (niveau 2) lors de la création de celui-ci
- **Sécurité des Mots de Passe**
  - Un mot de passe doit être haché et salé avant stockage.
- **Modification de Privilèges**
  - Seul un utilisateur avec un niveau de privilège "Administrateur" (niveau 4) ou “Super-administrateur” (niveau 5) peut modifier les niveaux de privilège d'autres comptes.
  - Les niveaux de privilèges :
    - 1- Visiteur
    - 2- Utilisateur connecté
    - 3- Modérateur
    - 4- Administrateur
    - 5- Super-Administrateur

### <span style="color: #26B260;">**3. Tags et Articles**</span>

- **Gestion des Tags**
  - Un tag est contient un intitulé unique (exemple : C#, PHP, IA)
- **Création et Modération d'Articles**
  - Un article est composé d'un titre
  - Un article est composé d'un résumé
  - Un article est composé d'une description
  - Un article contient une date de publication
  - Un article peut contenir des liens vers des sources externes
  - Un article contient le pseudo de l'utilisateur ayant écrit l'article
  - Un article contient le nombre de fois qu'il a été placé en favoris
  - Un article ne peut pas avoir le même titre qu'un autre article
  - Un article peut être relié à un ou plusieurs tags
- **Gestion des articles**
  - Un article ne peut être ajouté que par un compte ayant au minimum le niveau de privilège d'un "Utilisateur connecté" (niveau 2) de l'application.
  - Un article ne peut être modéré que par un compte ayant au minimum le niveau de privilège d'un "Modérateur" (niveau 3)
  - Un article ne peut être visible qu'après avoir été modéré par un compte ayant au minimum le niveau de privilège d'un "Modérateur" (niveau 3)
  - Un article peut être signalé par tous les lecteurs y compris les visiteurs de l'application
  - Un article peut être noté par d'autres "Utilisateurs connectés" (niveau 2)
  - Un article peut être placé dans les favoris d'un "Utilisateur connecté" (niveau 2) par celui-ci

### <span style="color: #26B260;">**4. Les ressources éducatives**</span>

- **Création de Ressources**
  - Une ressource peut être un Cheat Sheet, une bibliothèque de tutoriel sur les langages de programmation, ...
  - Une ressource peut contenir des liens vers des sites externes (documentation officielle d'un langage de programmation par exemple)
  - Une ressource contient un titre
  - Une ressource contient une description
  - Une ressource peut contenir du code
  - Une ressource ne peut pas avoir le même titre qu'une autre ressource
  - Une ressource peut être reliée à un ou plusieurs tags
- **Gestion des ressources éducatives**
  - Une ressource peut être placée en favoris par un "Utilisateur connecté" (niveau 2)
  - Une ressource doit être ajoutée par un compte ayant au minimum le niveau de privilège d'un "Modérateur" (niveau 3)
  - Une ressource peut être commentée par des "Utilisateurs connectés" (niveau 2)
- **Les commentaires**
  - Un utilisateur doit être connecté pour pouvoir commenter une ressource ou un article
  - Les ressources et les articles de l'application disposent d'une section commentaire en bas de page
- **Un commentaire**
  - Un commentaire doit être relié à un contenu (ressource ou article) OU à un commentaire d'un contenu
  - Un commentaire est ajouté par un "Utilisateur connecté" (niveau 2)
  - Un commentaire doit être modéré
  - Un commentaire a une date d'ajout
  - Un commentaire ne peut pas contenir d'adresse mail
  - Un commentaire ne peut pas permettre l'exécution de code sur l'application
  - Un commentaire ne doit pas contenir d’adresse mail
- **Gestion des commentaires**
  - Un commentaire doit être relié à un "Utilisateur connecté" (niveau 2).
    - Son pseudo doit être visible
    - La date à laquelle il a ajouté le commentaire doit apparaître
  - Un "Utilisateur connecté" ne peut pas supprimer ou modifier le commentaire d'un autre "Utilisateur connecté"
  - Un commentaire peut être signalé y compris par un visiteur
  - Un commentaire peut être relié à un autre commentaire en tant que réponse

### <span style="color: #26B260;">**5. Modération et sécurité**</span>

- **Notification d'Activités :**
  - Un utilisateur recevra une notification si il y a une activité suspecte sur son compte
- **Audit et Journalisation :**
  - Une action critique, telle que la modification des privilèges et la suppression de comptes doit être audité
  - Une action critique, telle que la modification des privilèges et la suppression de comptes doit être journalisé

### <span style="color: #26B260;">**6. Tableau de bord utilisateur**</span>

- **Accès**
  - Le tableau de bord n'est accessible que par un "Utilisateur connecté" (niveau 2)
- **Contenus**
  - Le tableau de bord contient les titres des contenus (articles et ressources) placés en favoris par l'utilisateur (niveau 2)
  - Le tableau de bord contient les tags des contenus les plus visités par l'utilisateur (niveau 2)
- **Gestion du tableau de bord utilisateur**
  - Un utilisateur (niveau 2) peut supprimer des contenus de son tableau de bord
  - Un utilisateur (niveau 2) peut ajouter des contenus à son tableau de bord

### <span style="color: #26B260;">**7. Tableau de bord modérateur**</span>

- **Accès**
  - Le tableau de bord modérateur n'est accessible qu'avec un compte connecté ayant un niveau de privilège au minimum de “modérateur” (niveau3)
- **Contenus**
  - Le tableau de bord modérateur contient une partie modération des commentaires
  - Le tableau de bord modérateur contient une partie modération des articles
- **Gestion du tableau de bord utilisateur**
  - Un modérateur peut ajouter une ressource
  - Un modérateur peut supprimer une ressource
  - Un modérateur connait les tendances et besoins utilisateur
  - Un modérateur peut désactiver un utilisateur connecté (avec notification automatique)
  - Un modérateur peut envoyer une notification à un utilisateur connecté

### <span style="color: #26B260;">8. Tableau de bord **pour les statistiques d'engagement**</span>

- **Accès**
  - Le tableau des statistiques n'est accessible qu'avec un compte connecté ayant un niveau de privilège au minimum de “administrateur” (niveau4)
- **Tendances et besoins utilisateur**
  - Le tableau contient les statistiques en fonction du type de contenu
  - Les tendances contiennent un tableau des tags par nombre de contenus dans l'application, nombre de visiteurs total et nombre d'utilisateurs ayant placé en favoris un contenu de ce tag
  - Les tendances contiennent un tableau des contenus, du nombre de commentaires reliés aux contenus, du nombre de visiteurs et du nombre de fois placés en favoris
- **Fonctionnalités du tableau de bord**
  - Un tableau affiche des statistiques détaillées classées selon le type de contenu
    - un aperçu des tags les plus populaires mesuré par le nombre total de contenus associés
    - le nombre de visiteurs
    - le nombre de fois que les contenus ont été ajoutés aux favoris par les utilisateurs.
  - Un tableau récapitule pour une vision claire de l'interaction des utilisateurs avec le contenu :
    - le nombre de commentaires
    - le nombre de visiteurs
    - la fréquence à laquelle les contenus sont favorisés

### <span style="color: #26B260;">**9. Organisation de discussions thématiques**</span>

- **Outil de Planification**
  - La planification d’une discussion est gérée par Calendly
- **Conditions de Participation**
  - Un utilisateur doit avoir un niveau de privilège "Utilisateur connecté" (niveau 2) ou supérieur pour proposer une session d'échange
- **Association aux Tags**
  - Une discussion est reliée à un ou plusieurs tags

### <span style="color: #26B260;">**10. Fonctionnalités de Recherche et Navigation**</span>

- **Accessibilité**
  - Une recherche de contenus peut être effectuée par tous y compris les visiteurs
- **Critères de Recherche**
  - le titre du contenu, pour des requêtes directes
  - les tags associés, afin de filtrer les contenus par sujets ou thématiques spécifiques
- **Options de Tri des Résultats** :
  - pertinence par rapport aux termes recherché
  - date d'ajout, avec une option pour afficher les contenus les plus récents en premier
  - popularité, mesurée par la fréquence des consultations ou des interactions des utilisateurs

### <span style="color: #26B260;">**11. Gestion de la modération des utilisateurs**</span>

- **Signalement de Commentaires**
  - Un utilisateur (niveau 2) peut signaler un commentaire inapproprié ou offensant posté par un autre utilisateur
- **Suspension de Compte lors de la Modération**
  - Lorsqu'un compte utilisateur fait l'objet d'une modération suite à un signalement, il est temporairement désactivé, empêchant toute connexion à l'application pendant la durée de l'examen
- **Désactivation de Compte**
  - Un compte utilisateur (niveau 2) peut être désactivé par un utilisateur ayant au moins le niveau de privilège “modérateur” en cas de non-respect des règles de la communauté
- **Suppression de Compte**
  - Un compte utilisateur (niveau 2) peut être définitivement supprimé par un utilisateur ayant au moins le niveau de privilège “modérateur”, assurant ainsi une gestion stricte et sécurisée des membres de la plateforme
