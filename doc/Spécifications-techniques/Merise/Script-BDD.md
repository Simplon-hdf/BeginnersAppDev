# Dépendance

Ce script nécessite l'activation de l'extension "uuid-ossp" pour la génération des UUID (identifiants uniques non séquentiels).

```sql
CREATE DATABASE IF NOT EXISTS db_beginers_app;

CREATE EXTENSION IF NOT EXISTS "uuid-ossp";

CREATE TABLE IF NOT EXISTS tags (
   tag_id VARCHAR (36) NOT NULL UNIQUE DEFAULT uuid_generate_v4(),
   tag_title VARCHAR(100) NOT NULL,
   created_at DATETIME NOT NULL,
   updated_at DATETIME NOT NULL,
   PRIMARY KEY(tag_id),
   UNIQUE(tag_title)
);

CREATE TABLE IF NOT EXISTS roles (
   role_id VARCHAR (36) NOT NULL UNIQUE DEFAULT uuid_generate_v4(),
   role_name VARCHAR(100) NOT NULL,
   created_at DATETIME NOT NULL,
   updated_at DATETIME NOT NULL,
   PRIMARY KEY(role_id),
   UNIQUE(role_name)
);

CREATE TABLE IF NOT EXISTS ressources_types (
   ressource_type_id VARCHAR (36) NOT NULL UNIQUE DEFAULT uuid_generate_v4(),
   type_name VARCHAR(50) NOT NULL,
   created_at DATETIME NOT NULL,
   updated_at DATETIME NOT NULL,
   PRIMARY KEY(ressource_type_id),
   UNIQUE(type_name)
);

CREATE TABLE IF NOT EXISTS ressources_status (
   ressource_status_id VARCHAR (36) NOT NULL UNIQUE DEFAULT uuid_generate_v4(),
   name VARCHAR(100) NOT NULL,
   created_at DATETIME NOT NULL,
   updated_at DATETIME NOT NULL,
   PRIMARY KEY(ressource_status_id),
   UNIQUE(name)
);

CREATE TABLE IF NOT EXISTS users (
   user_id VARCHAR (36) NOT NULL UNIQUE DEFAULT uuid_generate_v4(),
   username VARCHAR(100) NOT NULL,
   email VARCHAR(100) NOT NULL,
   password VARCHAR(255) NOT NULL,
   is_active BOOLEAN NOT NULL,
   created_at DATETIME NOT NULL,
   updated_at DATETIME NOT NULL,
   role_id VARCHAR (36) NOT NULL,
   PRIMARY KEY(user_id),
   UNIQUE(username),
   UNIQUE(email),
   FOREIGN KEY(role_id) REFERENCES roles(role_id)
);

CREATE TABLE IF NOT EXISTS ressources (
   ressource_id VARCHAR (36) NOT NULL UNIQUE DEFAULT uuid_generate_v4(),
   title VARCHAR(50) NOT NULL,
   content TEXT,
   summary VARCHAR(255),
   is_reported BOOLEAN NOT NULL,
   created_at DATETIME NOT NULL,
   updated_at DATETIME NOT NULL,
   user_id VARCHAR (36) NOT NULL,
   ressource_type_id VARCHAR (36) NOT NULL,
   ressource_status_id VARCHAR (36) NOT NULL,
   user_id_1 VARCHAR (36) NOT NULL,
   PRIMARY KEY(ressource_id),
   UNIQUE(title),
   FOREIGN KEY(user_id) REFERENCES users(user_id),
   FOREIGN KEY(ressource_type_id) REFERENCES ressources_types(ressource_type_id),
   FOREIGN KEY(ressource_status_id) REFERENCES ressources_status(ressource_status_id),
   FOREIGN KEY(user_id_1) REFERENCES users(user_id)
);

CREATE TABLE IF NOT EXISTS sharing_sessions (
   sharing_session_id VARCHAR (36) NOT NULL UNIQUE DEFAULT uuid_generate_v4(),
   title VARCHAR(255) NOT NULL,
   description TEXT,
   event_start_datetime DATETIME NOT NULL,
   event_end_datetime DATETIME NOT NULL,
   created_at DATETIME NOT NULL,
   updated_at DATETIME NOT NULL,
   user_id VARCHAR (36) NOT NULL,
   PRIMARY KEY(sharing_session_id),
   UNIQUE(title),
   FOREIGN KEY(user_id) REFERENCES users(user_id)
);

CREATE TABLE IF NOT EXISTS comments (
   comment_id VARCHAR (36) NOT NULL UNIQUE DEFAULT uuid_generate_v4(),
   content VARCHAR(255),
   is_reported BOOLEAN,
   created_at DATETIME NOT NULL,
   updated_at DATETIME NOT NULL,
   comment_id_1 VARCHAR (36) NOT NULL,
   user_id VARCHAR (36) NOT NULL,
   ressource_id VARCHAR (36) NOT NULL,
   PRIMARY KEY(comment_id),
   UNIQUE(comment_id_1),
   FOREIGN KEY(comment_id_1) REFERENCES comments(comment_id),
   FOREIGN KEY(user_id) REFERENCES users(user_id),
   FOREIGN KEY(ressource_id) REFERENCES ressources(ressource_id)
);

CREATE TABLE IF NOT EXISTS ressources_status_history (
   ressource_status_history_id VARCHAR (36) NOT NULL UNIQUE DEFAULT uuid_generate_v4(),
   status_changed_at DATETIME NOT NULL,
   preview_state VARCHAR(50),
   new_state VARCHAR(50),
   created_at DATETIME NOT NULL,
   updated_at DATETIME NOT NULL,
   ressource_id VARCHAR (36) NOT NULL,
   PRIMARY KEY(ressource_status_history_id),
   FOREIGN KEY(ressource_id) REFERENCES ressources(ressource_id)
);

CREATE TABLE IF NOT EXISTS have (
   tag_id VARCHAR (36) NOT NULL UNIQUE DEFAULT uuid_generate_v4(),
   ressource_id VARCHAR (36) NOT NULL,
   PRIMARY KEY(tag_id, ressource_id),
   FOREIGN KEY(tag_id) REFERENCES tags(tag_id),
   FOREIGN KEY(ressource_id) REFERENCES ressources(ressource_id)
);

CREATE TABLE IF NOT EXISTS reference (
   ressource_id VARCHAR (36) NOT NULL,
   sharing_session_id VARCHAR (36) NOT NULL,
   PRIMARY KEY(ressource_id, sharing_session_id),
   FOREIGN KEY(ressource_id) REFERENCES ressources(ressource_id),
   FOREIGN KEY(sharing_session_id) REFERENCES sharing_sessions(sharing_session_id)
);

CREATE TABLE IF NOT EXISTS refer (
   tag_id VARCHAR (36) NOT NULL,
   sharing_session_id VARCHAR (36) NOT NULL,
   PRIMARY KEY(tag_id, sharing_session_id),
   FOREIGN KEY(tag_id) REFERENCES tags(tag_id),
   FOREIGN KEY(sharing_session_id) REFERENCES sharing_sessions(sharing_session_id)
);

CREATE TABLE IF NOT EXISTS follow (
   user_id VARCHAR (36) NOT NULL,
   user_id_1 VARCHAR (36) NOT NULL,
   PRIMARY KEY(user_id, user_id_1),
   FOREIGN KEY(user_id) REFERENCES users(user_id),
   FOREIGN KEY(user_id_1) REFERENCES users(user_id)
);

```

> 📌 Dans le contexte de notre application, nous n'avons pas fait le choix de préfixer le nom de nos tables.
Mais dans un cas concret nous aurions choisi cette option afin d'améliorer encore la sécurité et l'intégrité des données. 

