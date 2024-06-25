<img src="../../Assets/Images/podium.png" alt="Podium" width="200">

# Comparatif frameworks Back-end

Dans le processus de conception et de développement de notre application, le choix des technologies et des outils est une étape cruciale qui impactera directement la qualité, la performance et la maintenabilité de notre produit final.  

Pour prendre des décisions éclairées et rationaliser nos choix technologiques, nous avons établi le tableau suivant qui évalue différents aspects clés des différents frameworks potentielles. 



Cette notation permettra notamment de comparer les stacks et donner une meilleure approche sur laquelle il faut choisir. 

| |Catégorie | 🥈 NestJS |  Express | 🥇 SpringBoot |🥉 Next.js |
|  --- | --- | --- | --- | --- | --- |
| 1 | Scalabilité | ⭐️⭐️⭐️ | ⭐️ | ⭐️⭐️⭐️⭐️⭐️  | ⭐️⭐️⭐️ |
| 2 | Payant | Gratuit | Gratuit | Payant | Gratuit |
| 3 | Rapidité | ⭐️⭐️ | ⭐️⭐️⭐️⭐️ | ⭐️ | ⭐️⭐️ |
| 4 |Popularité | ⭐️⭐️ | ⭐️⭐️⭐️ | ⭐️⭐️⭐️ | ⭐️⭐️ |
| 5 |Maturité | ⭐️⭐️ | ⭐️⭐️⭐️ | ⭐️⭐️⭐️ | ⭐️⭐️⭐️  |
| 6 |Licence Open Source | MIT | MIT | Apache 2.0 | MIT |
| 7 |Communauté GitHub | ⭐️⭐️ | ⭐️ | ⭐️⭐️  | ⭐️⭐️⭐️ |
| 8 | Contributeurs | Peu | Très peu | Nombreux | Très nombreux |
| 9 | Documentation | ⭐️⭐️⭐️ | ⭐️⭐️ | ⭐️⭐️⭐️ | ⭐️⭐️ |
| 10 | Dépendances/librairies | ⭐️⭐️⭐️ | ⭐️⭐️ | ⭐️⭐️⭐️ | ⭐️⭐️ |
| <strong>TOTAL</strong> | |<strong>17</strong> | <strong>16</strong> | <strong>20</strong> | <strong>17</strong> |

<details>
<summary>Comparatif détaillé Backend <strong>Nest</strong> Vs <strong>Express</strong> Vs <strong>SpringBoot</strong> Vs <strong>Next</strong></summary>

### **Scalabilité**

- **Nest.js** : Conçu pour s'adapter tant aux petites applications qu'aux grandes entreprises, Nest.js utilise une architecture modulaire le rendant versatile pour divers types de projets.
- **Express** : Sa flexibilité le rend approprié pour tout, des petits projets aux grandes applications d'entreprise, bien que sa structure moins prescriptive nécessite une gestion rigoureuse pour les grands projets.
- **Spring Boot** : Très adapté aux grandes applications d'entreprise, il offre des outils intégrés pour gérer efficacement les architectures complexes. L'utilisation de JVM permet de gérer des ressources très importante. 
- **Next.js**: Bien que principalement orienté vers le développement frontend avec des capacités de Server-Side Rendering (SSR), Next.js peut aussi être utilisé pour certains aspects du développement backend. Il est capable de gérer des applications de petite à moyenne taille, mais peut ne pas être l'option la plus idéale pour les très grandes applications backend, en raison de son focus sur les rendus côté serveur et l'optimisation des performances frontend. Toutefois, pour des applications intégrant fortement front et back-end, Next.js offre une bonne scalabilité au sein de son cadre spécifique, surtout lorsqu'il est utilisé en combinaison avec des services backend dédiés.

### **Coût**


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
- **Spring Boot** : Très mature et stable, soutenu par une grande entreprise (VMware).
- **Next.js** : Bien établi et soutenu par Vercel, offrant une stabilité et des mises à jour régulières, malgré son orientation plus récente comparée à des technologies comme Spring Boot ou Express.

### **Documentation et Support**

- **Nest.js** : Documentation moderne et complète, bonne communauté en ligne.
- **Express** : Riche en documentation et ressources, avec beaucoup de guides disponibles.
- **Spring Boot** : Documentation excellente et support professionnel disponible.
- **Next.js** : Excellente documentation, ressources abondantes, et une communauté très active, notamment sur les plateformes comme GitHub et Stack Overflow.

### **Licence Open Source**

- **Tous les quatre** sont sous des licences open source permissives, facilitant leur adoption et utilisation.


### **GitHub Stars** (chiffres au 25 Juin 2024)

- **NestJS** : Environ 65k étoiles.
- **Express** : Environ 64k étoiles.
- **Spring Boot** : Environ 74k étoiles.
- **Next.js** : Environ 122k étoiles, reflétant une adoption très large et un intérêt croissant.


### **Dernier commit**

- Tous maintenus activement avec des mises à jour régulières.

### **Stack Overflow**

- Tous ont une forte présence avec des milliers de questions, témoignant de leur utilisation active.


### **Librairies/Dépendances**


- **NestJS** : Excellente intégration avec d'autres bibliothèques JavaScript/TypeScript.
- **Express** : Très flexible, permet une intégration facile avec une multitude de bibliothèques.
- **Spring Boot** : Intègre bien avec l'écosystème Spring et Java, mais peut être moins flexible avec des bibliothèques non-Spring.
- **Next.js** : Très bonne intégration avec l'écosystème React et les bibliothèques JavaScript modernes, offrant des solutions clés en main pour divers besoins de développement.
</details>
<br>

**❓ Pourquoi choisir la médaille d'argent :**


✅ Nest.js est un framework moderne, open-source, gratuit et intégré avec TypeScript. Il est optimisé pour les performances entrées/sorties dans un environnement JavaScript, NestJS est une option plus adaptée que Spring Boot pour notre projet.


> **En conclusion** Nest.js est choisi pour notre projet non seulement pour ses avantages en termes de coût et de performance mais aussi pour sa flexibilité et son adéquation avec les technologies actuelles et les pratiques de développement modernes. Ces facteurs, combinés à sa capacité à évoluer efficacement selon les besoins du projet, en font une solution plus appropriée pour notre application par rapport à Spring Boot, notamment dans un contexte où la rapidité de développement et l'adaptabilité sont prioritaires.
