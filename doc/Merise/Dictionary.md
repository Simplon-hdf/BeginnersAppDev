# Dictionnaire de données

### Introduction

Un dictionnaire de donnée se définit comme un référentiel de métadonnées qui renseigne sur le contexte d’une base de données et qui fournit les informations nécessaires pour pouvoir l’interpréter.  
Cette documentation facilite la gestion des bases de données et permet aux administrateurs et utilisateurs de comprendre facilement la structure de leurs bases de données.

| Entité |     Métadonnées      | Type de données | Longueur | Description                                                                      | Exemple                              |
| :----: | :------------------: | :-------------: | :------: | :------------------------------------------------------------------------------- | ------------------------------------ |
|        |       user_id        |   INTEGER(11)   |          | Identifiant unique de l'utilisateur.                                             | 1                                    |
|        |     user_pseudo      |   VARCHAR(75)   |          | Pseudo unique de l'utilisateur. Contrainte d'unicité appliquée.                  | johnDoe                              |
|        |    user_password     |  VARCHAR(255)   |          | Mot de passe de l'utilisateur, haché et salé. Utilisation de bcrypt recommandée. | $2cakofefedzdzopk4opkza4k3ml2ml9jui8 |
|        |      user_email      |   VARCHAR(75)   |          | Adresse email unique de l'utilisateur. Format valide vérifié.                    | mailto:john@doe.fr                   |
|        | user_account_type_id |   INTEGER(11)   |          | Identifiant du type de compte de l'utilisateur.                                  | 2                                    |

<details>
<summary><span style="color: #26B260">Récapitulatif des entités du dictionnaire de données</span></summary>

### Utilisateur (User)

| Métadonnées          | Type         |
| :------------------- | :----------- |
| user_id              | INTEGER(11)  |
| user_pseudo          | VARCHAR(75)  |
| user_password        | VARCHAR(255) |
| user_email           | VARCHAR(75)  |
| user_account_type_id | INTEGER(11)  |

</details>
