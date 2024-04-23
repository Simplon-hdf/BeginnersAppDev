<img src="../doc/Assets/Images/secutiy_strategy.jpg" alt="security strategy">

# Stratégie de Sécurisation Complète pour notre application

## Introduction

We are committed to providing a secure community platform where technology enthusiasts can follow the latest trends, exchange information and collaborate with other members. To ensure data security and user privacy, we implement a comprehensive security strategy that integrates key security concepts, secure development practices, and advanced monitoring mechanisms.

## Enjeux de Sécurité et Menaces Principales

Notre application traitera des données sensibles telles que les profils d'utilisateurs, les préférences de suivi technologique, les commentaires et les contributions partagées sur la plateforme. Afin de maintenir la confiance des utilisateurs et de respecter les réglementations en vigueur, telles que le RGPD, nous devons nous assurer de protéger ces informations contre tout accès non autorisé.

Les principales menaces identifiées pour notre application incluent :

- **Injection de Script Côté Client (XSS)** : Cette vulnérabilité peut permettre à des attaquants d'injecter du code malveillant dans les pages web, compromettant ainsi la sécurité des utilisateurs et la confidentialité de leurs données.
- **Attaque par Forgery de Requêtes Inter-Sites (CSRF)** : Les attaquants pourraient manipuler les actions des utilisateurs authentifiés sur la plateforme, compromettant ainsi l'intégrité des données et les transactions.
- **Injection SQL (SQLi)** : Les failles dans la gestion des bases de données pourraient permettre aux attaquants d'accéder, de modifier ou de supprimer des données sensibles, constituant ainsi une menace sérieuse pour la sécurité et l'intégrité des données des utilisateurs.

## Recommandations de l'ANSII (Agence Nationale de la Sécurité des Systèmes d'Information)

Nous nous engageons à suivre les recommandations de l'ANSII pour garantir la sécurité de notre application. L'ANSII, en tant qu'autorité nationale en matière de cybersécurité, fournit des lignes directrices et des bonnes pratiques essentielles pour protéger les systèmes d'information contre les menaces et les attaques. En adhérant aux normes et aux principes recommandés par l'ANSII, nous renforçons la résilience de notre application et nous nous assurons de maintenir un niveau de sécurité élevé pour nos utilisateurs.

Voici les recommandations que nous comptons suivre:

<details>
<summary>Recommandations Web (✅)</summary>

- R1 Mettre en œuvre TLS à l’état de l’art
- R2 Mettre en œuvre HSTS (HTTP Strict Transport Security)
- R4 Utiliser l’API DOM à bon escient
- R5 Dissocier clairement la composition des pages web
- R6 Expliciter la nature d’une ressource avec l’en-tête Content-Type
- R7 Vérifier l’échappement des contenus inclus
- R8 Vérifier la conformité des données issues de sources externes
- R9 Proscrire l’usage de la fonction eval()
- R12 Contrôler l’intégrité des contenus tiers
- R13 Restreindre les contenus aux ressources fiables
- R14 Mettre en œuvre CSP par en-tête HTTP
- R15 Interdire des contenus inline
- R16 Définir la directive default-src dans CSP
- R17 Utiliser CSP contre le clickjacking
- R18 Utiliser X-Frame-Options contre le clickjacking
- R40 Vérifier la valeur de l’Origin lors de la réception d’une requête CORS
- R43 Anonymiser le chargement des ressources en cross-origin
- R44 Préférer l’utilisation de l’API Fetch à XMLHttpRequest
- R45 Sécuriser l’ouverture de nouvelles fenêtres
- R46 Définir une stratégie d’ouverture en cross-origin
- R47 Utiliser le mode strict
- R59-R60 Adaptation des profils de sécurité et des configurations au contexte spécifique d'utilisation
- R61-R63 Limiter l'usage des composants tiers, les maintenir à jour et ne pas altérer leur code source
</details>

<details>
<summary>Recommandations Authentification (✅)</summary>

- R2 Privilégier l’utilisation de moyens d’authentification forts
- R3 Conduire une analyse de risque
- R6 Remettre les facteurs d’authentification au travers de canaux sécurisés
- R9 Conserver les historiques d’utilisation des facteurs d’authentification
- R10 Limiter dans le temps le nombre de tentatives d’authentification
- R11 Réaliser l’authentification au travers d’un canal sécurisé
- R12 Limiter la durée de validité d’une session authentifiée
- R13 Protéger les données d’authentification stockées par le vérifieur
- R14 Ne pas donner d’information sur l’échec de l’authentification
- R16 Définir une politique d’utilisation des facteurs d’authentification
- R17 Sensibiliser les utilisateurs à la sécurité de l’authentification
- R18 Mettre en place un processus de révocation des facteurs d’authentification
- R19 Définir des délais adaptés de prise en compte des révocations
- R20 Mettre en place une politique de sécurité des mots de passe
- R21 Imposer une longueur minimale pour les mots de passe
- R22 Ne pas imposer de longueur maximale pour les mots de passe
- R23 Mettre en œuvre des règles sur la complexité des mots de passe
- R24 Ne pas imposer par défaut de délai d’expiration sur les mots de passe des comptes non sensibles
- R25 Imposer un délai d’expiration sur les mots de passe des comptes à privilèges
- R26 Révoquer immédiatement les mots de passe en cas de compromission suspectée ou avérée
- R27 Mettre en place un contrôle de la robustesse des mots de passe lors de leur création ou de leur renouvellement
- R28 Utiliser un sel aléatoire long
- R29 Utiliser une fonction de dérivation de mots de passe memory-hard/itérative
- R38 Modifier les mots de passe par défaut
- R39 Utiliser un facteur de possession avec sécurité qualifiée/certifiée
- R40 Ne pas utiliser un facteur inhérent comme unique facteur d’authentification
- R41 Utiliser un facteur inhérent uniquement associé à un facteur d’authentification fort
- R42 Favoriser une rencontre en présence lors de l’enregistrement d’un facteur inhérent
</details>

## Proposition de Stratégie de Sécurisation

### Principaux Concepts de Sécurité

Nous allons appliquer une approche de défense en profondeur en intégrant plusieurs couches de sécurité à travers l'ensemble de notre application. Cela inclura la sécurisation de l'infrastructure, du réseau, du système d'exploitation, de l'application et des données.

Nous allons limiter les points d'entrée potentiels pour les attaquants en réduisant la surface d'attaque de notre application. Cela implique de désactiver les services inutilisés, de limiter les ports ouverts et d'appliquer des mises à jour de sécurité régulières pour tous les composants du système.

Nous accorderons uniquement les permissions nécessaires à chaque utilisateur ou composant du système selon le principe du privilège minimum. Cela limitera les risques en réduisant la portée des actions qu'un utilisateur ou un processus peut effectuer.

### Tunnels de Sécurisation (HTTPS/TLS/HSTS)

Nous renforcerons la sécurité des données en transit en mettant en place des tunnels sécurisés. Le protocole HTTPS, associé aux standards de sécurité TLS (Transport Layer Security) et HSTS (HTTP Strict Transport Security), garantira que toutes les communications entre l'application et nos serveurs seront chiffrées. Cela protégera les données des utilisateurs contre les interceptions malveillantes et assurera la confidentialité des informations échangées, même sur des réseaux moins sécurisés.

### Monitoring et Journalisation

Nous allons mettre en place un système de surveillance continue pour détecter les activités suspectes et réagir rapidement en cas d'incident. Des journaux d'audit détaillés seront maintenus pour enregistrer toutes les actions effectuées sur la plateforme, facilitant ainsi la détection des comportements anormaux et la réponse aux menaces potentielles.

### Nettoyage des Formulaires et Sanétisation

Nous appliquerons des méthodes de nettoyage et de sanitization sur les données saisies par les utilisateurs pour prévenir les injections SQL et XSS. Toutes les entrées utilisateur seront validées et échappées pour garantir l'intégrité des données et la sécurité de l'application.

### ORM contre les Injections SQL

Nous utiliserons un ORM (Object-Relational Mapping) pour accéder à la base de données, ce qui réduira considérablement le risque d'injections SQL en séparant le code SQL de la logique métier et en fournissant une abstraction sécurisée pour interagir avec la base de données.

### Protection des Entêtes avec Helmet

Nous protégerons nos applications Express.js en utilisant Helmet, un ensemble de middleware pour sécuriser les applications Express en définissant divers en-têtes HTTP. Cela inclura la protection contre les attaques XSS, le contrôle de la politique de contenu, la prévention de l'ouverture de fenêtres contextuelles indésirables (CSP), entre autres.

### Politique de Sécurité

Nous mettrons en œuvre la politique de sécurité Same-Origin pour prévenir les attaques XSS en restreignant l'accès et l'interaction des scripts entre différentes origines.

Nous utiliserons CORS pour sécuriser le partage de ressources entre différentes origines, en contrôlant l'accès aux ressources entre différents domaines et en prévenant les attaques CSRF.

Nous définirons une CSP pour limiter les sources de contenu autorisées et prévenir les attaques XSS en contrôlant les scripts exécutés sur notre application.

Nous utiliserons SRI pour garantir l'intégrité des ressources chargées depuis des origines tierces, en vérifiant les empreintes cryptographiques des fichiers externes.

### Politique des Mots de Passe

Nous adopterons une politique de mots de passe stricte qui inclura des exigences de complexité, de longueur minimale et de vérification approfondie des critères. Les mots de passe seront stockés de manière sécurisée en utilisant le hashage SHA256 avec salage pour prévenir les attaques par force brute et assurer la confidentialité des informations des utilisateurs.

### Gestion des Identités Utilisateurs avec les UUID

Nous utiliserons des UUID (Universally Unique IDentifiers) pour renforcer la sécurité et la confidentialité des données des utilisateurs. Les UUID, générés de manière aléatoire, rendront difficile la prédiction des identifiants et contribueront à la protection contre les tentatives d'accès non autorisé.

### Stratégie de Sauvegarde

Nous mettrons en place une stratégie de sauvegarde robuste pour protéger les données de l'application contre les incidents tels que les pannes, les erreurs ou les attaques. Des sauvegardes régulières des données seront effectuées pour garantir la disponibilité et l'intégrité des informations des utilisateurs en cas de problème.

### RGPD (Règlement général sur la protection des données)

Nous mettrons en place les mesures suivantes pour assurer la conformité au RGPD :

- **Consentement Explicite** : L'application exigera un consentement clair de l'utilisateur pour le traitement des données personnelles lors de la création de profil.

- **Minimisation des Données** : Seules les informations indispensables seront collectées pour la réservation.

- **Droits des Utilisateurs** : Les utilisateurs seront informés de leurs droits RGPD, incluant le droit à la consultation (accès à leurs données), droit de rectification (correction de leurs données), droit à l’oublie (suppression de leurs données) et la possibilité de retirer leur consentement à tout moment.

- **Sécurité** : Des mesures robustes seront implémentées pour protéger les données contre les accès non autorisés et les pertes.

- **Gestion des Sous-Traitants** : Le traitement des paiements par des tiers respectera également le RGPD.

- **Notification en Cas de Violation** : En cas de fuite de données, nous informerons les autorités compétentes et les utilisateurs concernés dans un délai de 72 heures.

- **Politique de Confidentialité** : Une politique claire et accessible décrira la gestion des données personnelles et les droits des utilisateurs.

En adoptant une approche proactive en matière de sécurité et en mettant en œuvre des mesures appropriées, notre application s'efforcera de fournir à ses utilisateurs un environnement sûr et fiable pour leur apprentissage et veille technologique.
