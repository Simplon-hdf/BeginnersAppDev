# Dictionnaire de données

### Introduction

Un dictionnaire de donnée se définit comme un référentiel de métadonnées qui renseigne sur le contexte d’une base de données et qui fournit les informations nécessaires pour pouvoir l’interpréter.  
Cette documentation facilite la gestion des bases de données et permet aux administrateurs et utilisateurs de comprendre facilement la structure de leurs bases de données.

| Entité | Attribut | Type de Données | Longueur | Contraintes                          | Description                | Exemple          |
| ------ | -------- | --------------- | -------- | ------------------------------------ | -------------------------- | ---------------- |
| Roles  | roleId   | SERIAL          |          | AUTO-INCREMENT, NOT NULL, UNIQUE, PK | Identifiant unique du rôle | 1                |
|        | nameRole | VARCHAR         | 50       | NOT NULL, UNIQUE                     | Nom du rôle                | "Administrateur" |

<details>
<summary><span style="color: #26B260">Récapitulatif des entités du dictionnaire de données</span></summary>

### Utilisateur (User)

| Entités              | Type         |
| :------------------- | :----------- |
| user_id              | INTEGER(11)  |
| user_pseudo          | VARCHAR(75)  |
| user_password        | VARCHAR(255) |
| user_email           | VARCHAR(75)  |
| user_account_type_id | INTEGER(11)  |

</details>
