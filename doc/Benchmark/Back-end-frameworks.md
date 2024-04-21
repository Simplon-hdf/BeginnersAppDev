<img src="../Assets/Images/podium.png" alt="Podium" width="200">

# Comparatif frameworks Back-end

Dans le processus de conception et de développement de notre application, le choix des technologies et des outils est une étape cruciale qui impactera directement la qualité, la performance et la maintenabilité de notre produit final.  
Pour prendre des décisions éclairées et rationaliser nos choix technologiques, nous avons établi le tableau suivant qui évalue différents aspects clés des différents frameworks potentielles.  
Chaque aspect est évalué sur une échelle de 1 à 3, où 1 représente une faible adéquation et 3 une adéquation maximale. Une fois que chaque technologie aura été évaluée selon ces critères, nous serons en mesure de comparer les résultats et de sélectionner le frameworks le mieux adapté à nos besoins spécifiques.
| Catégorie | 🥈 NestJS | 🥉 Express | 🥇 SpringBoot | Next.js |
| --- | --- | --- | --- | --- |
| Big ou small | 3 | 3 | 3 | 2 |
| _ Custo | 3 | 3 | 2 | 2 |
| _ Rapidité | 3 | 3 | 2 | 2 |
| Popularité | 3 | 3 | 3 | 2 |
| Maturité | 2 | 3 | 3 | 2 |
| Releases | 3 | 3 | 3 | 2 |
| Best Practices | 3 | 2 | 3 | 2 |
| Equipe Core | 3 | 2 | 3 | 2 |
| GitHub Stars | 2 | 3 | 2 | 2 |
| Licence Open Source | MIT | MIT | Apache 2.0 | MIT |
| _ Distribution | Facile | Facile | Complexe | Facile |
| _ Commercial | Forte | Forte | Forte | Modérée |
| _ Modification | Facile | Facile | Modérée | Facile |
| _ Restriction | Aucune | Aucune | Aucune | Aucune |
| Commu GitHub | 3 | 3 | 2 | 2 |
| _ Contributeurs | Nombreux | Très nombreux | Nombreux | Modérés |
| _ Used | Fréquemment | Très fréquemment | Fréquemment | Occasionnellement |
| _ Issu | Modérés | Nombreux | Modérés | Modérés |
| _ Pull Request | Actives | Très actives | Actives | Modérées |
| _ Process contribution | Clair | Clair | Clair | Clair |
| Dernier commit | 3 | 3 | 3 | 2 |
| Sponso | Variable | Variable | Forte | Variable |
| Stackoverflow | 2 | 3 | 3 | 1 |
| _ Tag | Populaire | Très populaire | Populaire | Moins populaire |
| _ Nombre de question | Nombreux | Très nombreux | Nombreux | Moins nombreux |
| _ Dernière question | Récemment | Récemment | Récemment | Moins récemment |
| \_ Réponse valider | Haute | Très haute | Haute | Modérée |
| Documentation | 3 | 2 | 3 | 2 |
| Bibliothèque | 3 | 2 | 3 | 2 |
| Magique | 2 | 1 | 3 | 1 |
| Mariage librairies | 3 | 2 | 2 | 2 |
| Payant | Gratuit | Gratuit | Payant | Gratuit |
| TOTAL | 58 | 57 | 59 | 40 |

<details>
<summary>Comparatif détaillé Backend Nest Vs Express Vs SpringBoot Vs Next</summary>

### **Big ou Small (Scalabilité)**

- **Nest.js** : Conçu pour s'adapter tant aux petites applications qu'aux grandes entreprises, Nest.js utilise une architecture modulaire et supporte les microservices, le rendant versatile pour divers types de projets.
- **Express** : Sa flexibilité le rend approprié pour tout, des petits projets aux grandes applications d'entreprise, bien que sa structure moins prescriptive nécessite une gestion rigoureuse pour les grands projets.
- **Spring Boot** : Très adapté aux grandes applications d'entreprise, il offre des outils intégrés pour gérer efficacement les architectures complexes.
- **Next.js**: Bien que principalement orienté vers le développement frontend avec des capacités de Server-Side Rendering (SSR), Next.js peut aussi être utilisé pour certains aspects du développement backend. Il est capable de gérer des applications de petite à moyenne taille, mais peut ne pas être l'option la plus idéale pour les très grandes applications backend, en raison de son focus sur les rendus côté serveur et l'optimisation des performances frontend. Toutefois, pour des applications intégrant fortement front et back-end, Next.js offre une bonne scalabilité au sein de son cadre spécifique, surtout lorsqu'il est utilisé en combinaison avec des services backend dédiés.

### **Coût (Custo)**

- **Nest.js** et **Express** : Open-source et gratuits, ces frameworks peuvent varier en coût de développement selon la disponibilité et l'expertise des développeurs.
- **Spring Boot** : Gratuit et open-source, mais peut impliquer des coûts opérationnels plus élevés en raison des ressources serveur et potentiellement des licences pour des outils complémentaires.
- **Next.js** : Également open-source et gratuit. Les coûts associés sont principalement liés au développement et à l'infrastructure de serveur pour le SSR, mais peuvent être optimisés avec une bonne planification.

### **Rapidité (Performance)**

- **Nest.js** : Performant, surtout avec Fastify.
- **Express** : Rapide pour des opérations de base mais peut être ralenti par des middleware lourds.
- **Spring Boot** : Performant mais avec un démarrage potentiellement lent dû à la lourdeur de la JVM.
- **Next.js** : Très performant pour le rendu des pages côté serveur et l'optimisation du chargement initial des pages web. Les performances peuvent varier selon la complexité des pages et l'utilisation des ressources statiques ou dynamiques.

### **Popularité**

- **Express** : Très populaire dans l'écosystème Node.js, souvent choisi pour sa simplicité.
- **Nest.js** : Rapidement populaire pour ceux qui cherchent une structure plus définie.
- **Spring Boot** : Forte popularité dans l'écosystème Java, particulièrement en entreprise.
- **Next.js** : Extrêmement populaire dans le développement de front-end moderne, notamment pour des applications réactives et des sites avec SSR.

### **Maturité et Stabilité**

- **Express** : Établi avec une large communauté et un écosystème riche.
- **Nest.js** : Plus récent mais stable et basé sur des principes éprouvés.
- **Spring Boot** : Très mature et stable, soutenu par une grande entreprise.
- **Next.js** : Bien établi et soutenu par Vercel, offrant une stabilité et des mises à jour régulières, malgré son orientation plus récente comparée à des technologies comme Spring Boot ou Express.

### **Documentation et Support**

- **Nest.js** : Documentation moderne et complète, bonne communauté en ligne.
- **Express** : Riche en documentation et ressources, avec beaucoup de guides disponibles.
- **Spring Boot** : Documentation excellente et support professionnel disponible.
- **Next.js** : Excellente documentation, ressources abondantes, et une communauté très active, notamment sur les plateformes comme GitHub et Stack Overflow.

### **Licence Open Source**

- **Tous les quatre** sont sous des licences open source permissives, facilitant leur adoption et utilisation.

### **GitHub Stars**

- **NestJS** : Environ 56k étoiles.
- **Express** : Environ 59k étoiles.
- **Spring Boot** : Environ 65k étoiles.
- **Next.js** : Environ 90k étoiles, reflétant une adoption très large et un intérêt croissant.

### **Dernier commit**

- Tous maintenus activement avec des mises à jour régulières.

### **Stack Overflow**

- Tous ont une forte présence avec des milliers de questions, témoignant de leur utilisation active.

### **Magique**

- **NestJS** : Utilise une "magie" modérée avec des décorateurs et l'injection de dépendances pour simplifier le développement.
- **Express** : Minimise la "magie", offrant plus de contrôle au développeur.
- **Spring Boot** : Niveau élevé de "magie" avec beaucoup d'auto-configurations pour simplifier le démarrage et la maintenance des applications.
- **Next.js** : Modérément "magique" en automatisant certaines configurations pour le rendu côté serveur et la génération de pages statiques, facilitant ainsi le développement rapide.

### **Mariage librairies**

- **NestJS** : Excellente intégration avec d'autres bibliothèques JavaScript/TypeScript.
- **Express** : Très flexible, permet une intégration facile avec une multitude de bibliothèques.
- **Spring Boot** : Intègre bien avec l'écosystème Spring et Java, mais peut être moins flexible avec des bibliothèques non-Spring.
- **Next.js** : Très bonne intégration avec l'écosystème React et les bibliothèques JavaScript modernes, offrant des solutions clés en main pour divers besoins de développement.
</details>
<br>

**❓ Pourquoi choisir la médaille d'argent :**

✅ Nest.js est un framework moderne, intégré avec TypeScript et optimisé pour les performances I/O dans un environnement JavaScript, NestJS est une option plus adaptée que Spring Boot pour votre projet.

> **En conclusion** Nest.js est choisi pour notre projet non seulement pour ses avantages en termes de coût et de performance mais aussi pour sa flexibilité et son adéquation avec les technologies actuelles et les pratiques de développement modernes. Ces facteurs, combinés à sa capacité à évoluer efficacement selon les besoins du projet, en font une solution plus appropriée pour notre application par rapport à Spring Boot, notamment dans un contexte où la rapidité de développement et l'adaptabilité sont prioritaires.
