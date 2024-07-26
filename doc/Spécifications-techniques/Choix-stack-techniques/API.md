<img src="../../../doc/Assets/Images/API.png" alt="API" width="600">

# Comparaison des types d'API

## Introduction

Dans le cadre de notre projet utilisant NextJS avec TypeScript et TypeORM pour interagir avec une base de données PostgreSQL, nous devons choisir le type d’API qui convient le mieux à nos besoins. Dans ce document, nous allons comparer les trois principaux types d’API : API Rest, GraphQL et SOAP, et justifier notre choix final.

## Types d'API

### 1. REST API (API Rest)

#### Description :

Une API Rest est basée sur le modèle architectural REST (Representational State Transfer). Elle utilise les méthodes HTTP standard (GET, POST, PUT, DELETE) pour effectuer des opérations CRUD (Create, Read, Update, Delete) sur des ressources.

#### Distinction stateless :

Les API Rest stateless, ne stockent pas l'état de la session côté serveur entre les requêtes. Chaque requête client contient toutes les informations nécessaires pour être traitée de manière autonome par le serveur, sans dépendre de requêtes précédentes.

#### Avantages des API Rest Stateless (par défault) :

- Facilité de mise en cache, évolutivité simplifiée, robustesse et tolérance aux pannes.
- Moins de complexité pour gérer l'état côté serveur.
- (optionnel) On peut exploiter des composants statefull ou mécanismes côté clients pour gérer les informations d'état.

### 2. GraphQL API

#### Description :

Une API GraphQL permet aux clients de spécifier exactement les données dont ils ont besoin. Elle utilise un seul endpoint pour toutes les requêtes, et les clients demandent uniquement les champs spécifiques dont ils ont besoin pour chaque requête.

#### Avantages :

- Flexibilité : Les clients peuvent demander exactement les données dont ils ont besoin, ce qui peut réduire la quantité de données transférées.
- Évolutivité : Un seul endpoint pour toutes les requêtes, simplifiant la gestion et l’évolution de l’API.

#### Inconvénients :

- Complexité : La mise en œuvre de GraphQL peut être plus complexe que REST.
- Performances : Peut introduire des surcharges supplémentaires sur le serveur pour traiter les requêtes complexes.

### 3. SOAP API

#### Description :

SOAP (Simple Object Access Protocol) est un protocole de communication basé sur XML permettant l’échange d’informations structurées dans des environnements distribués.

#### Avantages :

- Standardisation : SOAP est un protocole très standardisé avec des spécifications détaillées.
- Sécurité : Supporte nativement des standards de sécurité comme WS-Security.

#### Inconvénients :

- Complexité : SOAP est souvent plus complexe à implémenter et à consommer que REST ou GraphQL.
- Performances : L’utilisation de XML et la surcharge de protocole peuvent entraîner des performances moindres.

## Comparaison

| Critère                   | REST API        | GraphQL API     | SOAP API |
| ------------------------- | --------------- | --------------- | -------- |
| Facilité d'utilisation    | ✅              | ⭐️⭐️⭐️⭐️⭐️ | ⭐️⭐️   |
| Performance               | ⭐️⭐️⭐️⭐️⭐️ | ⭐️⭐️⭐️       | ⭐️⭐️   |
| Flexibilité               | ⭐️⭐️⭐️       | ✅              | ⭐️⭐️   |
| Courbe d'apprentissage    | ✅              | ⭐️⭐️⭐️       | ⭐️⭐️   |
| Évolutivité               | ✅              | ✅              | ⭐️⭐️   |
| Outils et support         | ✅              | ⭐️⭐️⭐️       | ⭐️⭐️   |
| Adoption dans l'industrie | ⭐️⭐️⭐️       | ⭐️⭐️⭐️       | ⭐️⭐️   |

<details>
<summary>Légende</summary>

- ✅ : Avantage significatif
- ⭐️⭐️⭐️⭐️⭐️ : Très bon
- ⭐️⭐️⭐️ : Bon
- ⭐️⭐️ : Moyen

</details>

## Choix de l'API

Pour notre projet, nous recommandons l'utilisation d'une API Rest stateless. Cette recommandation est basée sur les facteurs suivants :

- Facilité d'utilisation : Les API Rest sont largement connues et utilisées, ce qui rend leur adoption et leur compréhension faciles pour les développeurs.
- Performance : Les API Rest offrent des performances élevées et sont bien adaptées aux opérations CRUD sur des ressources.
- Évolutivité : Les API Rest stateless sont particulièrement évolutives grâce à leur nature sans état, ce qui les rend faciles à mettre en cache et à scaler horizontalement.
- Moins de complexité : Les API Rest stateless sont généralement moins complexes.

En conclusion, une API Rest stateless répondra le mieux à nos besoins en matière de simplicité, de performance et de facilité de mise en œuvre pour notre projet.

[🔙 Retour à la Table des matières principale](../Choix-stack-techniques/README.md)
