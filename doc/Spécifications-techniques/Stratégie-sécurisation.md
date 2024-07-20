<img src="../../doc/Assets/Images/secutiy_strategy.jpg" alt="security strategy">

# Stratégie de Sécurisation Complète pour notre application

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

## 1. Couche front

### Chiffrement des communications (HTTPS/TLS/HSTS)

Nous renforcerons la sécurité des données en transit entre le client et le serveur en mettant en place des tunnels sécurisés. Le protocole **HTTPS**, associé aux standards de sécurité **TLS** (Transport Layer Security) et **HSTS** (HTTP Strict Transport Security), garantira que toutes les communications dont la première entre l'application et nos serveurs seront chiffrées forçant l’utilisation de HTTPS.  
Cela protégera les données des utilisateurs contre les interceptions malveillantes et assurera la confidentialité des informations échangées, même sur des réseaux moins sécurisés.

### Protection des Entêtes avec Helmet

Nous protégerons nos applications Express.js en utilisant **Helmet**, un ensemble de middleware pour sécuriser les applications Express en définissant divers en-têtes HTTP. Cela inclura la protection contre les attaques **XSS** (Cross-Site Scripting), le contrôle de la politique de contenu, la prévention de l'ouverture de fenêtres contextuelles indésirables (**CSP** (Content Security Policy) ), entre autres.  
Grâce à **NestJS**, la mise en œuvre de ces mesures de sécurité sera simplifiée, nous permettant de garantir une base solide pour la protection de l’environnement numérique de nos utilisateurs.
Nous protégerons nos applications Express.js en utilisant **Helmet**, un ensemble de middleware pour sécuriser les applications Express en définissant divers en-têtes HTTP. Cela inclura la protection contre les attaques **XSS** (Cross-Site Scripting), le contrôle de la politique de contenu, la prévention de l'ouverture de fenêtres contextuelles indésirables (**CSP** (Content Security Policy) ), entre autres.  
Grâce à NestJS, la mise en œuvre de ces mesures de sécurité sera simplifiée, nous permettant de garantir une base solide pour la protection de l’environnement numérique de nos utilisateurs.

### Nettoyage des Formulaires et Sanétization

Nous appliquerons des méthodes de nettoyage et de sanitization sur les données saisies par les utilisateurs pour prévenir les injections **SQL** et **XSS**. Toutes les entrées utilisateur seront validées et échappées pour garantir l'intégrité des données et la sécurité de l'application.

([cf. Politique des mots de passes](#politique-des-mots-de-passe))

### Politique de Sécurité Same-Origin et CSP

Ces mesures contrôleront les ressources chargées et exécutées sur le site.

- **Same-Origin Policy** (SOP)  
  Nous empêcherons les scripts de différentes origines d’interagir entre eux, contribuant ainsi à la prévention des attaques XSS. Par exemple, cela protégera les contributions des développeurs contre l’injection de scripts malveillants.
- **Cross-Origin Resource Sharing** (CORS)  
  Nous utiliserons **CORS** pour sécuriser le partage de ressources entre différentes origines. Cela permettra, par exemple, aux développeurs d’accéder de manière sécurisée aux API externes nécessaires sans compromettre la sécurité des données utilisateurs et des projets partagés sur la plateforme.
- **Content Security Policy** (CSP)
- En établissant une **CSP** stricte, nous limiterons les sources de contenu autorisées. Cela aidera à prévenir les attaques XSS en contrôlant les scripts exécutés sur notre application. Par exemple, seules les sources de confiance pourront être chargées, garantissant ainsi que les bibliothèques de code utilisées restent sécurisées.
- **Intégrité des Sous-Ressources** (SRI)  
  Nous utiliserons **SRI** (Subresource Integrity) pour garantir l’intégrité des ressources chargées depuis des origines tierces. En vérifiant les empreintes cryptographiques des fichiers externes, nous assurerons que les bibliothèques et les outils tiers n’ont pas été altérés, protégeant ainsi le code des projets collaboratifs contre toute modification malveillante.

### Mécanismes de Limitation d’Essais d’Authentification

Limitez les tentatives de connexion infructueuses pour prévenir les attaques par force brute. Après plusieurs échecs, bloquez temporairement l’accès et alertez l’utilisateur.

([cf. Politique des mots de passes](#politique-des-mots-de-passe))

## 2. Couche API Back-end

### Authentification et Gestion des Sessions avec OAuth 2.0 et JWT

Sécurisez les APIs en utilisant **OAuth 2.0** pour l’authentification et les JSON Web Tokens (**JWT**) pour la gestion des sessions.
Sécurisez les APIs en utilisant **OAuth 2.0** pour l’authentification et les JSON Web Tokens (**JWT**) pour la gestion des sessions.

**OAuth 2.0 et JWT** : Bien que mentionnés dans la gestion des sessions, leur application aux APIs assure une couche supplémentaire de sécurité pour l'authentification et la gestion des autorisations, adaptée aux interactions entre services.

- **Tokens et JWT** : Nous utilisons ces méthodes pour assurer des sessions sécurisées avec des identifiants uniques et des données codées, permettant une gestion stateless qui augmente la scalabilité et la performance.

**Validation et Sanitization des Requêtes API**:

Assurez-vous que chaque requête API soit scrutée pour valider et assainir son contenu, ciblant efficacement les tentatives d’injections **SQL** et **XSS**.
Assurez-vous que chaque requête API soit scrutée pour valider et assainir son contenu, ciblant efficacement les tentatives d’injections **SQL** et **XSS**.

**Chiffrement des communications**:

Nous renforcerons la sécurité des données en transit entre le serveur et le client en mettant en place des tunnels sécurisés. Le protocole HTTPS, associé aux standards de sécurité **TLS** (Transport Layer Security) et **HSTS** (HTTP Strict Transport Security), garantira que toutes les communications dont la première entre l'application et nos serveurs seront chiffrées forçant l’utilisation de HTTPS.  
Cela protégera les données des utilisateurs contre les interceptions malveillantes et assurera la confidentialité des informations échangées, même sur des réseaux moins sécurisés.

**Limitation du Taux de Requêtes (Rate Limiting)**:

Mettez en place des contrôles stricts sur le nombre de requêtes acceptées pour prévenir les attaques par déni de service (DoS).

### Gestion des Identités Utilisateurs avec les UUID

Nous utiliserons des **UUID** (Universally Unique IDentifiers) pour renforcer la sécurité et la confidentialité des données des utilisateurs. Les UUID, générés de manière aléatoire, rendront difficile la prédiction des identifiants et contribueront à la protection contre les tentatives d'accès non autorisé.

### Transmission Sécurisée des Mots de Passe

Assurez-vous que les mots de passe sont toujours transmis de manière sécurisée, en utilisant des connexions HTTPS pour éviter les interceptions

### Journalisation des Requêtes API

Enregistrez chaque appel API, y compris les détails de la requête tels que l’adresse IP source, les paramètres de requête, les en-têtes, et les réponses. Cela permet de tracer les actions à travers l’API et de détecter des anomalies comme des tentatives d’injection ou des abus de l’API.

### Visualisation des end-points API via Swagger

Ensemble de règles et d’outils pour décrire, produire, consommer et visualiser des services web RESTful.

### Monitoring et Journalisation

Nous allons mettre en place un système de surveillance continue pour détecter les activités suspectes et réagir rapidement en cas d'incident. Des journaux d'audit détaillés seront maintenus pour enregistrer toutes les actions effectuées sur la plateforme, facilitant ainsi la détection des comportements anormaux et la réponse aux menaces potentielles.

### Sécuriser les routes via des ACL (Access Control List)

Contrôle des permissions et des rôles utilisateurs à chaque demande d’accès aux ressources protégées (fichiers, fonctionnalités admin/modérateur)

### Gestion des Rôles avec RBAC (Role-Based Access Control)

Système qui assigne des permissions aux utilisateurs en fonction des rôles qu'ils occupent. Définir les rôles est fondamental pour respecter le principe du moindre privilège, qui vise à limiter les privilèges des utilisateurs uniquement à ce dont ils ont besoin pour accomplir leurs tâches. Ici nous avons défini rôles:

- Super-administrateur

- Administrateur

- Modérateur

- Membre

**Sécurité** : Des mesures robustes seront implémentées pour protéger les données contre les accès non autorisés et les pertes.  
**Politique de Confidentialité** : Une politique claire et accessible décrira la gestion des données personnelles et les droits des utilisateurs.

## 3. Couche bdd

### Politique des Mots de Passe

- **Catégories de Mots de Passe** :  
  Les super administrateurs et les administrateurs bénéficient d’un accès complet, nécessitant le plus haut niveau de sécurité.
  Les modérateurs et les utilisateurs standard ont accès aux fonctionnalités standards de l’application, y compris la gestion des commentaires et auront un niveau de sécurité moindre.

- **Longueur des Mots de Passe** :  
  La longueur des mots de passe est déterminée non seulement pour la sécurité, mais aussi pour maintenir la performance optimale du système :

  - Pour les Super administrateurs et Administrateurs, nous exigeons des mots de passe d’au moins **15 caractères**.

  - Les Modérateurs et utilisateurs doivent utiliser des mots de passe d’au moins **12 caractères**.

  - La longueur maximale autorisée de 100 caractères est un compromis entre flexibilité et efficacité systémique.

- **Règles de Complexité** :  
  Tous les mots de passe doivent intégrer une combinaison de lettres majuscules, minuscules, chiffres, et symboles spéciaux. Nous proscrivons également l’utilisation de suites logiques ou répétitives.  
   Nous metterons également en place des Regex pour renforcer la sécurité

- **Délai d’Expiration des Mots de Passe** :  
  La fréquence de renouvellement des mots de passe est adaptée au rôle :

- Un renouvellement **annuel** équilibrant sécurité et facilité d’utilisation. Ce délai a été choisie en fonction du besoin de sécurité de l’application mais aussi afin de ne pas contraindre l’utilisateur à rentrer son mot de passe trop régulièrement

• **Mécanismes de Limitation d’Essais d’Authentification**

Nous limiterons les tentatives de connexion infructueuses à 5 essais, puis déclenchera l’envoi d’un mail pour réinitialiser le mot de passe.

• **Méthode de Conservation des Mots de Passe**

Les mots de passe sont stockés de manière sécurisée, utilisant un hachage **Bcrypt** avec salage, assurant que chaque mot de passe est unique et protégé contre les attaques.

• **Méthode de Recouvrement d’Accès**

En cas de perte ou de vol des mots de passe, nous fournissons un lien de réinitialisation à usage unique (validité de 24h), assurant une récupération sécurisée.

### ORM contre les Injections SQL

Employez un ORM pour accéder à la base de données, ce qui aide à prévenir les injections SQL en fournissant une couche d’abstraction qui sépare le code SQL de la logique métier.

### **Stratégie de Sauvegarde**

Nous mettrons en place une stratégie de sauvegarde robuste pour protéger les données de l'application contre les incidents tels que les pannes, les erreurs ou les attaques. Des sauvegardes régulières des données seront effectuées pour garantir la disponibilité et l'intégrité des informations des utilisateurs en cas de problème. Automatisation régulière des sauvegardes de la bdd grâce à pg_cron afin de lutter contre les ransomwares

### RGPD (Règlement général sur la protection des données)

Nous mettrons en place les mesures suivantes pour assurer la conformité au RGPD, mais aussi la confiance des utilisateurs, leur garantissant un traitement respectueux et sécurisé de leurs données personnelles. :

- **Consentement Explicite** :  
  L'application exigera un consentement clair de l'utilisateur pour le traitement des données personnelles lors de la création de profil.
- **Minimisation des Données** :  
  Seules les informations indispensables seront collectées pour la réservation.
- **Droits des Utilisateurs** :  
  Les utilisateurs seront informés de leurs droits RGPD, incluant le droit à la consultation (accès à leurs données), droit de rectification (correction de leurs données), droit à l’oublie (suppression de leurs données) et la possibilité de retirer leur consentement à tout moment. Les utilisateurs peuvent contacter le référent RGPD par email pour faire valoir leur droits.
- **En cas de violation de données** :  
  Nous informerons sans délai les autorités compétentes (CNIL) et les utilisateurs impactés, respectant un délai de 72 heures.
- Mise en place d’un formulaire de demande d’accès

### Stockage Sécurisé des Mots de Passe

Utilisez des méthodes de hachage robustes, comme Bcrypt, pour le stockage des mots de passe. Bcrypt intègre un salage automatique qui rend chaque hash unique et résistant aux attaques par tables de correspondance.  
([cf. Politique des mots de passes](#politique-des-mots-de-passe))

En adoptant une approche proactive en matière de sécurité et en mettant en œuvre des mesures appropriées, notre apllication s'efforcera de fournir à ses utilisateurs un environnement sûr et fiable pour leur veille technologique.

[🔙 Retour à la Table des matières principale](../../README.md)
