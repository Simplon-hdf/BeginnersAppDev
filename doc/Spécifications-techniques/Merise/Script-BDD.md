# Dépendance

Ce script nécessite l'activation de l'extension "uuid-ossp" pour la génération des UUID (identifiants uniques non séquentiels).

```sql
CREATE DATABASE IF NOT EXISTS db_beginers_app;

CREATE EXTENSION IF NOT EXISTS "uuid-ossp";

CREATE TABLE IF NOT EXISTS tags (
   tag_uuid VARCHAR (36) NOT NULL UNIQUE DEFAULT uuid_generate_v4(),
   tag_title VARCHAR(100) NOT NULL,
   created_at DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP(0)::TIMESTAMP WITHOUT TIME ZONE,
   updated_at DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP(0)::TIMESTAMP WITHOUT TIME ZONE,
   PRIMARY KEY(tag_uuid UUID),
   UNIQUE(tag_title)
);

CREATE TABLE IF NOT EXISTS roles (
   role_uuid VARCHAR (36) NOT NULL UNIQUE DEFAULT uuid_generate_v4(),
   role_name VARCHAR(100) NOT NULL,
   created_at DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP(0)::TIMESTAMP WITHOUT TIME ZONE,
   updated_at DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP(0)::TIMESTAMP WITHOUT TIME ZONE,
   PRIMARY KEY(role_uuid),
   UNIQUE(role_name)
);

CREATE TABLE IF NOT EXISTS ressources_types (
   ressource_type_uuid VARCHAR (36) NOT NULL UNIQUE DEFAULT uuid_generate_v4(),
   type_name VARCHAR(50) NOT NULL,
   created_at DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP(0)::TIMESTAMP WITHOUT TIME ZONE,
   updated_at DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP(0)::TIMESTAMP WITHOUT TIME ZONE,
   PRIMARY KEY(ressource_type_uuid),
   UNIQUE(type_name)
);

CREATE TABLE IF NOT EXISTS ressources_status (
   ressource_status_uuid VARCHAR (36) NOT NULL UNIQUE DEFAULT uuid_generate_v4(),
   name VARCHAR(100) NOT NULL,
   created_at DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP(0)::TIMESTAMP WITHOUT TIME ZONE,
   updated_at DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP(0)::TIMESTAMP WITHOUT TIME ZONE,
   PRIMARY KEY(ressource_status_uuid),
   UNIQUE(name)
);

CREATE TABLE IF NOT EXISTS users (
   user_uuid VARCHAR (36) NOT NULL UNIQUE DEFAULT uuid_generate_v4(),
   username VARCHAR(100) NOT NULL,
   email VARCHAR(100) NOT NULL,
   password VARCHAR(255) NOT NULL,
   is_active BOOLEAN NOT NULL DEFAULT TRUE,
   created_at DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP(0)::TIMESTAMP WITHOUT TIME ZONE,
   updated_at DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP(0)::TIMESTAMP WITHOUT TIME ZONE,
   role_uuid VARCHAR (36) NOT NULL,
   PRIMARY KEY(user_uuid),
   UNIQUE(username),
   UNIQUE(email),
   FOREIGN KEY(role_uuid) REFERENCES roles(role_uuid)
);

CREATE TABLE IF NOT EXISTS ressources (
   ressource_uuid VARCHAR (36) NOT NULL UNIQUE DEFAULT uuid_generate_v4(),
   title VARCHAR(50) NOT NULL,
   content TEXT,
   summary VARCHAR(255),
   is_reported BOOLEAN NOT NULL,
   created_at DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP(0)::TIMESTAMP WITHOUT TIME ZONE,
   updated_at DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP(0)::TIMESTAMP WITHOUT TIME ZONE,
   user_uuid VARCHAR (36) NOT NULL,
   ressource_type_uuid VARCHAR (36) NOT NULL,
   ressource_status_uuid VARCHAR (36) NOT NULL,
   user_uuid_1 VARCHAR (36) NOT NULL,
   PRIMARY KEY(ressource_uuid),
   UNIQUE(title),
   FOREIGN KEY(user_uuid) REFERENCES users(user_uuid),
   FOREIGN KEY(ressource_type_uuid) REFERENCES ressources_types(ressource_type_uuid),
   FOREIGN KEY(ressource_status_uuid) REFERENCES ressources_status(ressource_status_uuid),
   FOREIGN KEY(user_uuid_1) REFERENCES users(user_uuid)
);

CREATE TABLE IF NOT EXISTS sharing_sessions (
   sharing_session_uuid VARCHAR (36) NOT NULL UNIQUE DEFAULT uuid_generate_v4(),
   title VARCHAR(255) NOT NULL,
   description TEXT,
   event_start_datetime DATETIME NOT NULL,
   event_end_datetime DATETIME NOT NULL,
   created_at DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP(0)::TIMESTAMP WITHOUT TIME ZONE,
   updated_at DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP(0)::TIMESTAMP WITHOUT TIME ZONE,
   user_uuid VARCHAR (36) NOT NULL,
   PRIMARY KEY(sharing_session_uuid),
   UNIQUE(title),
   FOREIGN KEY(user_uuid) REFERENCES users(user_uuid)
);

CREATE TABLE IF NOT EXISTS comments (
   comment_uuid VARCHAR (36) NOT NULL UNIQUE DEFAULT uuid_generate_v4(),
   content VARCHAR(255),
   is_reported BOOLEAN,
   created_at DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP(0)::TIMESTAMP WITHOUT TIME ZONE,
   updated_at DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP(0)::TIMESTAMP WITHOUT TIME ZONE,
   comment_uuid_1 VARCHAR (36) NOT NULL,
   user_uuid VARCHAR (36) NOT NULL,
   ressource_uuid VARCHAR (36) NOT NULL,
   PRIMARY KEY(comment_uuid),
   UNIQUE(comment_uuid_1),
   FOREIGN KEY(comment_uuid_1) REFERENCES comments(comment_uuid),
   FOREIGN KEY(user_uuid) REFERENCES users(user_uuid),
   FOREIGN KEY(ressource_uuid) REFERENCES ressources(ressource_uuid)
);

CREATE TABLE IF NOT EXISTS ressources_status_history (
   ressource_status_history_uuid VARCHAR (36) NOT NULL UNIQUE DEFAULT uuid_generate_v4(),
   status_changed_at DATETIME NOT NULL,
   preview_state VARCHAR(50),
   new_state VARCHAR(50),
   created_at DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP(0)::TIMESTAMP WITHOUT TIME ZONE,
   updated_at DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP(0)::TIMESTAMP WITHOUT TIME ZONE,
   ressource_uuid VARCHAR (36) NOT NULL,
   PRIMARY KEY(ressource_status_history_uuid),
   FOREIGN KEY(ressource_uuid) REFERENCES ressources(ressource_uuid)
);

CREATE TABLE IF NOT EXISTS have (
   tag_uuid VARCHAR (36) NOT NULL UNIQUE DEFAULT uuid_generate_v4(),
   ressource_uuid VARCHAR (36) NOT NULL,
   PRIMARY KEY(tag_uuid, ressource_uuid),
   FOREIGN KEY(tag_uuid) REFERENCES tags(tag_uuid),
   FOREIGN KEY(ressource_uuid) REFERENCES ressources(ressource_uuid)
);

CREATE TABLE IF NOT EXISTS reference (
   ressource_uuid VARCHAR (36) NOT NULL,
   sharing_session_uuid VARCHAR (36) NOT NULL,
   PRIMARY KEY(ressource_uuid, sharing_session_uuid),
   FOREIGN KEY(ressource_uuid) REFERENCES ressources(ressource_uuid),
   FOREIGN KEY(sharing_session_uuid) REFERENCES sharing_sessions(sharing_session_uuid)
);

CREATE TABLE IF NOT EXISTS refer (
   tag_uuid VARCHAR (36) NOT NULL,
   sharing_session_uuid VARCHAR (36) NOT NULL,
   PRIMARY KEY(tag_uuid, sharing_session_uuid),
   FOREIGN KEY(tag_uuid) REFERENCES tags(tag_uuid),
   FOREIGN KEY(sharing_session_uuid) REFERENCES sharing_sessions(sharing_session_uuid)
);

CREATE TABLE IF NOT EXISTS follow (
   user_uuid VARCHAR (36) NOT NULL,
   user_uuid_1 VARCHAR (36) NOT NULL,
   PRIMARY KEY(user_uuid, user_uuid_1),
   FOREIGN KEY(user_uuid) REFERENCES users(user_uuid),
   FOREIGN KEY(user_uuid_1) REFERENCES users(user_uuid)
);

```

> 📌 Dans le contexte de notre application, nous n'avons pas fait le choix de préfixer le nom de nos tables.
> Mais dans un cas concret nous aurions choisi cette option afin d'améliorer encore la sécurité et l'intégrité des données.

[🔙 Retour à la Table des matières](../../Spécifications-techniques/Merise/README.md)
