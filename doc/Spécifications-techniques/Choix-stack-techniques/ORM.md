<img src="../../Assets/Images/podium.png" alt="Podium" width="200">

# Comparatif frameworks ORM

Dans le processus de conception et de développement de notre application, le choix des technologies et des outils est une étape cruciale qui impactera directement la qualité, la performance et la maintenabilité de notre produit final.  
Pour prendre des décisions éclairées et rationaliser nos choix technologiques, nous avons établi le tableau suivant qui évalue différents aspects clés des différents frameworks potentielles.  
Chaque aspect est évalué sur une échelle de 1 à 3, où 1 représente une faible adéquation et 3 une adéquation maximale. Une fois que chaque technologie aura été évaluée selon ces critères, nous serons en mesure de comparer les résultats et de sélectionner le framework le mieux adapté à nos besoins spécifiques.
| Catégorie | 🥉 Sequelize | 🥇 Prisma | 🥈 TypeORM |
|--------------------------|-----------|--------|---------|
| Big ou small | 1 | 3 | 3 |
| _ Custo | 2 | 3 | 3 |
| _ Rapidité | 1 | 3 | 3 |
| Popularité | 2 | 3 | 3 |
| Maturité | 3 | 3 | 3 |
| Releases | 2 | 3 | 3 |
| Best Practices | 3 | 3 | 3 |
| Equipe Core | 2 | 3 | 3 |
| GitHub Stars | 2 | 3 | 3 |
| Licence Open Source | MIT | Apache 2.0 | MIT |
| _ Distribution | Simple | Simple | Simple |
| _ Commercial | Faible | Faible | Faible |
| _ Modification | Facile | Facile | Facile |
| _ Restriction | Aucune | Aucune | Aucune |
| Commu GitHub | 2 | 3 | 3 |
| _ Contributeurs | Nombreux | Nombreux | Nombreux |
| _ Used | Fréquemment | Très fréquemment | Fréquemment |
| _ Issu | Modérés | Peu | Modérés |
| _ Pull Request | Actives | Très actives | Actives |
| _ Process contribution | Clair | Clair | Clair |
| Dernier commit | 3 | 3 | 3 |
| Sponso | Peu | Peu | Peu |
| Stackoverflow | 3 | 3 | 3 |
| _ Tag | Populaire | Populaire | Populaire |
| _ Nombre de question | Nombreux | Nombreux | Nombreux |
| _ Dernière question | Récemment | Récemment | Récemment |
| \_ Réponse valider | Haute | Haute | Haute |
| Documentation | 3 | 3 | 3 |
| Bibliothèque | 3 | 3 | 3 |
| Magique | 1 | 3 | 2 |
| Mariage librairies | 3 | 2 | 3 |
| Payant | Gratuit | Gratuit | Gratuit |
| TOTAL | 61 | 79 | 78 |

<details>
<summary>Comparatif détaillé ORM Sequilize Vs Prisma Vs TypeORM</summary>
### **Scalabilité (Big ou Small)**

- **Sequelize** : Bien adapté pour des applications de taille moyenne, mais peut présenter des défis en termes de performance avec des bases de données très larges ou complexes.
- **Prisma** : Conçu pour être performant à grande échelle, avec un focus sur la modernité et l'efficacité, adapté aussi bien pour les petites que les grandes applications.
- **TypeORM** : Très flexible et capable de gérer de grands schémas de base de données avec de nombreuses relations, idéal pour des applications d'entreprise complexes.

### **Coût (Custo)**

- **Sequelize**, **Prisma**, **TypeORM** : Tous trois sont open-source et gratuits. Le coût de développement peut varier en fonction de la familiarité des développeurs avec l'ORM et le langage de programmation associé (JavaScript/TypeScript).

### **Rapidité (Performance)**

- **Sequelize** : Bonnes performances pour des opérations standards, mais peut devenir lent lors de la manipulation de requêtes complexes ou de grands volumes de données.
- **Prisma** : Offre d'excellentes performances, surtout avec sa récente architecture qui optimise les requêtes et réduit la surcharge sur la base de données.
- **TypeORM** : Performances robustes, bien adapté pour des transactions complexes et peut être optimisé avec des techniques avancées de gestion des données.

### **Popularité**

- **Sequelize** : Très populaire parmi les développeurs Node.js, surtout pour ceux qui utilisent encore JavaScript.
- **Prisma** : Gagne rapidement en popularité en raison de son approche moderne et de ses fonctionnalités avancées.
- **TypeORM** : Populaire dans la communauté TypeScript, souvent choisi pour son intégration native avec ce langage.

### **Maturité**

- **Sequelize** : L'un des ORM les plus anciens pour Node.js, avec une large base d'utilisateurs et de nombreuses années de développement.
- **Prisma** : Plus récent mais a rapidement évolué et s'est établi comme un choix solide grâce à ses mises à jour fréquentes et son approche innovante.
- **TypeORM** : Bien établi, surtout apprécié dans les projets TypeScript, avec une communauté active et des mises à jour régulières.

### **Best Practices**

- **Sequelize** : Suit les pratiques courantes des ORM avec une API riche et des fonctionnalités complètes de gestion des relations et des transactions.
- **Prisma** : Encourage les meilleures pratiques modernes avec un schéma de configuration centralisé et une génération automatique de requêtes optimisées.
- **TypeORM** : Utilise le décorateur et les entités pour définir les modèles, favorisant un code clair et maintenable.

### **Équipe Core**

- **Sequelize** : Développé et maintenu par une communauté de contributeurs open-source.
- **Prisma** : Soutenu par une entreprise (Prisma Labs) avec une équipe de développement dédiée et professionnelle.
- **TypeORM** : Également maintenu par une communauté open-source, avec des contributions majeures de quelques développeurs clés.

### **GitHub Stars**

- **Sequelize** : Environ 26k étoiles.
- **Prisma** : Environ 26k étoiles.
- **TypeORM** : Environ 28k étoiles.

### **Dernier commit**

- Les trois ORM sont activement maintenus avec des mises à jour fréquentes pour corriger les bugs et ajouter des fonctionnalités.

### **Stack Overflow**

- Les trois ont des communautés actives sur Stack Overflow, offrant de l'aide et des ressources pour résoudre les problèmes de développement.

### **Documentation et Support**

- **Sequelize** : Documentation complète avec des guides détaillés pour différents cas d'utilisation.
- **Prisma** : Excellente documentation, moderne et bien organisée, facilitant l'apprentissage et la mise en œuvre.
- **TypeORM** : Bonne documentation, en particulier pour les utilisateurs de TypeScript, avec des exemples détaillés et des instructions de configuration.

### **Magique**

- **Sequelize** : Relativement conventionnel sans trop de "magie" dans la manipulation des données.
- **Prisma** : Plus "magique" en raison de son abstraction élevée et de la génération automatique de requêtes, ce qui simplifie considérablement le développement.
- **TypeORM** : Moins "magique" mais utilise des décorateurs pour enrichir les classes d'entité, ce qui peut sembler magique pour les nouveaux utilisateurs, tout en offrant une transparence accrue sur la façon dont les données sont gérées.

### **Mariage librairies**

- **Sequelize**, **Prisma**, et **TypeORM** : Tous permettent une bonne intégration avec d'autres bibliothèques JavaScript/TypeScript, bien que Prisma soit souvent perçu comme ayant l'approche la plus moderne et la plus intégrée en raison de sa capacité à générer des requêtes optimisées et de sa gestion efficace des relations.
</details>
<br>

**❓ Pourquoi choisir la médaille d'argent :**

✅ TypeORM est un choix judicieux par rapport à Prisma, surtout si on valorise une intégration poussée avec TypeScript, une flexibilité accrue dans la gestion des requêtes SQL, et une compatibilité étendue avec divers systèmes de bases de données. Sa gestion avancée des relations et sa communauté bien établie en font une solution fiable pour les applications complexes. De plus, sa maturité et sa stabilité éprouvées assurent une base solide pour le développement d'applications d'entreprise critiques. Ces atouts rendent TypeORM particulièrement adapté pour notre projet nécessitant un contrôle précis et une adaptabilité élevée.

> **En conclusion** TypeORM est le choix idéal d'ORM pour ses capacités supérieures à gérer des bases de données complexes et pour sa compatibilité native avec TypeScript, qui améliore significativement la qualité et la maintenabilité du code. Il allie haute performance, intégration technique approfondie, et un support robuste, rendant TypeORM particulièrement bien adapté pour le développement d'applications robustes et évolutives.
>
> >
>
> - Sa flexibilité permet une personnalisation approfondie adaptée aux besoins spécifiques de notre projet, soutenue par une communauté active et une documentation riche.
> - TypeORM offre également un contrôle accru et une transparence dans la gestion des opérations de base de données.
