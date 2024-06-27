## Application

### Accessibilité
- L'application doit être conforme aux normes d'accessibilité WCAG pour garantir l'accessibilité à tous les utilisateurs.

## Utilisateurs

### Visiteur
- Un visiteur peut s’enregistrer pour devenir membre avec un pseudonyme, un email et un mot de passe et un état actif par défaut
- Un visiteur peut télécharger une ressource
- Un visiteur peut lire les ressources présentes sur la plateforme
- Un  visiteur peut parcourir les différentes catégories de contenu
- Un visiteur peut utiliser la fonction de recherche pour trouver des ressources

### Membres
- Un membre peut soumettre à publication une ressource
- Un membre peut soumettre à publication un lien d’une ressource
- Un membre peut déposer un ou des commentaires à une publication
- Un membre peut modifier son commentaire si aucun autre commentaire n’a été ajouté en réponse à celui-ci
- Un membre peut répondre à un ou des commentaires
- Un membre peut ajouter une note à une ressource (notation en étoile sur /5 )
- Un membre peut modifier sa note à une ressource (notation en étoile sur /5 )
- Un membre peut supprimer sa note à une ressource (notation en étoile sur /5 )
- Un membre peut télécharger une ressource
- Un membre peut visualiser une vidéo (tutoriel, conférence…)
- Un membre a un dashboard où il visualise ses commentaires
- Un membre a un dashboard où il visualise ses favoris (ressources)
- Un membre a un dashboard où il visualise les statistiques de ses publications (nombre de vues, commentaires, partages, etc.)
- Un membre peut ajouter des contenus (ressources) en favori à son dashboard
- Un membre peut supprimer des contenus (ressources) en favori à son dashboard
- Un membre peut lister les tags des contenus les plus visités
- Un membre peut filtrer les tags des contenus les plus visités
- Un membre peut recevoir des notifications pour les nouveaux contenus correspondant à ses intérêts
- Un membre peut signaler du contenu inapproprié aux modérateurs
- Un membre peut suivre d’autres utilisateurs
- Un membre peut proposer et participer à des discussions de groupe ou forums
- Un membre peut configurer des alertes sur ses tags préférés
- Un membre peut voir les sessions d’échange proposées par les autres membres

### Modérateur
- Un modérateur a tous les droits d’un membre
- Un modérateur peut anonymisé un commentaire en cas de contenu haineux, discriminant ou inapproprié, déclenchant une notification automatique à l'encontre de l'auteur du commentaire
- Un modérateur peut envoyer une notification à un membre
- Un modérateur peut désactiver un membre (avec notification automatique)
- Un modérateur vérifie les ressources avant publication
- Un modérateur peut ajouter une ressource
- Un modérateur peut désactiver une ressource
- Un modérateur peut voir une ressource désactivée
- Un modérateur a un dashboard où il visualise les dernières resources avant mise en ligne
- Un modérateur a un dashboard où il visualise ses dernières ressources archivées
- Un modérateur a un dashboard où il visualise les derniers commentaires signalés
- Un modérateur peut restaurer une ressource
- Un modérateur peut accéder à l’historique des modifications des commentaires et des ressources
- Un modérateur peut attribuer des avertissements aux membres pour comportements inappropriés
- Un modérateur peut consulter des rapports d’activité des membres
- Un modérateur a un outil pour détecter automatiquement du contenu inapproprié sur les commentaires
- Un modérateur peut bloquer temporairement un membre

### Administrateur
- Un administrateur a les droits d’un modérateur
- Un administrateur peut créer, modifier et désactiver des comptes utilisateurs, y compris ceux des modérateurs
- Un administrateur peut configurer les permissions et rôles des membres
- Un administrateur peut voir et gérer toutes les notifications envoyées par la plateforme
- Un administrateur peut générer et consulter des rapports d’activité et des statistiques détaillées sur l’utilisation de la plateforme
- Un administrateur peut gérer les catégories de contenu et les tags associés
- Un administrateur peut superviser et auditer les actions des modérateurs
- Un administrateur a un dashboard où il visualise les statistiques d’engagement
- Un administrateur peut voir les statistiques en fonction du type de contenu
- Un administrateur peut voir les tags les plus populaires mis en favoris
- Un administrateur peut voir les ressources les plus populaires mis en favoris
- Un administrateur peut voir le nombre de commentaires
- Un administrateur peut voir le nombre de visiteurs
- Un administrateur peut voir le nombre de membres

### Super-administrateur
- Un super administrateur peut créer, modifier et désactiver des comptes administrateurs
- Un super administrateur peut s’authentifier et interagir qu’en ligne de commande

### Droit commun à tous les utilisateurs sauf visiteur
- Un utilisateur est informé de ses droits RGPD, incluant le droit à la consultation (accès à ses données), droit de rectification (correction de ses données), droit à l’oublie (suppression de ses données) et la possibilité de retirer son consentement à tout moment.
- Un utilisateur a obligatoirement un et un seul statut de membre, modérateur, administrateur
- Un utilisateur peut se connecter avec son email et son mot de passe
- Un utilisateur peut faire une demande de désactivation de son compte
- Un utilisateur peut réinitialiser son mot de passe si il l’a oublié via un email ou une question de sécurité.

## Tags

- Un tag contient un intitule unique (exemple : C#, PHP, IA)

## Commun à toutes les Ressources 
- Un ressource est composé d'un titre unique
- Un ressource est composé d'une description
- Un ressource a une date de publication
- Un ressource a le pseudo de l'auteur de la ressource
- Un ressource a le nombre de fois qu'il a été placé en favoris
- Un ressource a une moyenne des notations données par les membres (étoile/5)
- Un ressource peut être relié à un ou plusieurs tags
- Un ressource peut être issu d’une source externe et être repartager sur ce site
- Un ressource peut contenir des commentaires
- Un ressource peut être désactivé

### Ressources : Un Article

- Un article peut contenir une image

### Ressources : Un CheatSheet
- Un CheatSheet est un document PDF

### Ressources : Un Tutoriel
- Un tutoriel peut contenir une vidéo

## Les sessions d'échanges 
- Une session d'échange possède un titre
- Une session d'échange possède une description
- Une session d'échange possède une date de début et une heure de début
- Une session d'échange possède une date de fin et une heure de fin

## Un commentaire
- Un commentaire doit être relié à un seul contenu (ressource)
- Un commentaire peut être la réponse à un commentaire
- Un commentaire ayant une réponse ne peut plus être modifié
- Un commentaire est ajouté par un membre
- Un commentaire a une date de création
- Un commentaire a une date de modification
- Un commentaire ne doit pas contenir d’adresse mail
- Un commentaire a le pseudo de son auteur