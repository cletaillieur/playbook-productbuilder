---
authors:
  - "Etienne Fenetrier"
last_updated: "2026-03-12"
---

# 1.3 Les (nombreux) défis et enjeux du rôle hybride de Product Builder

L'une des transformations les plus profondes apportées par l'IA est le passage de simples applications à **des systèmes agentiques, c’est-à-dire des agents capables de raisonner, de planifier et d'exécuter des tâches complexes de manière autonome**. Cependant, ce gain d'autonomie pour la machine crée aussi un paradoxe pour celui qui l’a construit…

​

**Le paradoxe agentique : plus d'autonomie pour l'IA = moins d'autonomie pour le Builder**

Intuitivement, on pourrait penser que des outils plus puissants rendent le constructeur plus indépendant. En réalité, c'est l'inverse qui se produit. Plus un produit IA devient agentique et ambitieux, plus sa connexion à l'écosystème de l'entreprise devient critique. Et plus cette connexion est profonde, plus le Product Builder a besoin à la fois de compétences techniques pointues et d'une collaboration structurée avec les équipes IT et Ingénierie.

Pourquoi ? Parce que nous passons d'**un monde de Software-as-a-Service (SaaS) à un monde de Service-as-a-Software**, dans lequel il ne s’agit plus seulement de designer des interfaces (des écrans, des boutons), mais de designer aussi des comportements (avec des agents qui prennent des décisions, interagissent avec des APIs, modifient des données).

Un simple chatbot conversationnel peut être construit en quasi-autonomie. Mais un agent qui doit accéder au CRM, lire les derniers e-mails d'un client, interroger la base de données logistique pour vérifier un stock, puis déclencher un remboursement via une API financière, ne peut plus être une solution isolée. **Il devient une porte d'entrée vers le cœur du système d'information de l'entreprise.**

À ce stade, les enjeux de sécurité, de gouvernance des données, de scalabilité et de fiabilité deviennent non-négociables. Le Product Builder ne peut plus et ne doit plus agir seul. **Son rôle passe de constructeur solo à chef d'orchestre d'une équipe hybride**.



**La matrice d'autonomie : naviguer entre construction et collaboration**

Pour aider le Product Builder à se positionner, une matrice qui croise deux axes peut être utilisée :

- **La complexité du prototype** : à quel point la logique de l'agent lui-même est-elle complexe ? S'agit-il d'un simple question-réponse ou d'un système multi-agents avec une planification complexe ?

- **La complexité de la stack IT d'intégration** : l'agent doit-il se connecter à des systèmes d'information sensibles, complexes ou anciens (legacy) ?

Le croisement de ces deux axes définit ensuite quatre grands modes de travail pour le Product Builder.


**Quadrant 1 - Autonomie (Stack simple / Prototype simple)**

C'est le domaine de l'expérimentation rapide et de la validation d'hypothèses à faible risque. Le Product Builder est ici dans son rôle le plus autonome.

Mode de travail : ***le Builder shippe seul***. Il peut concevoir, construire et déployer de petites applications ou des outils internes sans dépendre de l'IT, à condition de respecter des garde-fous clairs (par exemple, ne pas manipuler de données clients sensibles).

**→ Un exemple concret : un Chatbot de FAQ Interne**

> Un chatbot simple basé sur une technique de RAG, qui répond aux questions des employés en se basant sur une base de connaissances publique et limitée (par exemple, les 10 dernières pages du site web de l'entreprise).

> Le prototype est simple (question-réponse basique) et la stack IT est minimale (pas de connexion à des données internes ou des systèmes critiques). Le Product Builder peut le créer de A à Z avec des outils du marché, le tester et le déployer en quelques jours.



**Quadrant 2 - Innovation (Stack complexe / Prototype simple)**

Ici, l'enjeu n'est pas la complexité de l'agent, mais le risque lié à son intégration dans des systèmes sensibles. Le but est de dérisquer la valeur d'une connexion avant de la construire de manière industrielle.

Mode de travail : ***le Builder travaille en sandbox*** (environnement de test isolé). Il ne se connecte pas directement aux systèmes de production, mais à des versions de test, des données anonymisées, ou des APIs de pré-production fournies et sécurisées par l'IT. Son rôle est de prouver la valeur de l'interaction.

**→ Un exemple concret : un assistant RAG sur données internes**

> Pour un assistant qui permet aux équipes commerciales de poser des questions sur les contrats clients, l'agent doit accéder à une base de données de contrats qui est une information sensible.

> La logique du prototype reste simple (RAG), mais la stack IT est complexe et risquée. Le Builder travaille avec l'IT pour obtenir un export anonymisé de 100 contrats dans un environnement sécurisé. Il construit son prototype sur ces données pour démontrer que l'agent peut extraire des informations pertinentes. S'il y arrive, il justifie l'investissement pour un projet plus large de co-engineering.



**Quadrant 3 - Co-Engineering (Stack complexe / Prototype complexe)**

C'est le quadrant des projets IA les plus stratégiques et les plus transformateurs. L'autonomie n'est plus une option ; la collaboration structurée est la seule voie possible.

Mode de travail : ***le binôme Product Builder - Ingénieur*** devient l'unité de production. Le Builder apporte la vision produit, la compréhension métier et la capacité de prototypage rapide des comportements de l'agent. L'Ingénieur (ou l'équipe IT) apporte l'expertise en architecture, sécurité, scalabilité et intégration. Ils construisent ensemble, dans un processus de co-engineering où la frontière entre prototype et production s'estompe.

**→ Un exemple concret : un système multi-agents en production**

> Pour un système qui automatise le traitement d'une réclamation client de bout en bout, un premier agent qualifie la demande, un deuxième interroge le CRM et la base logistique, un troisième évalue le préjudice et propose un geste commercial basé sur des règles métier, et un quatrième déclenche le remboursement via le système financier.

> Le prototype lui-même est très complexe (orchestration de plusieurs agents, planification) et il doit interagir avec de multiples systèmes IT critiques (CRM, ERP, Finance). C'est le cœur de la transformation agentique. Le Product Builder conçoit le comportement et la logique des agents, tandis que l'équipe d'ingénierie construit les connecteurs sécurisés, assure la fiabilité des APIs et met en place le monitoring en production.



**Quadrant 4 - Autonomie avancée (Stack simple / Prototype complexe) - La zone de danger**

Ce quadrant mérite une mention spéciale car il représente un piège courant. Le Product Builder, en confiance, tente de construire un agent très complexe (par exemple, un planificateur autonome) mais en le gardant sur une stack simple, déconnectée de l'entreprise.

Il crée ainsi un *gadget* impressionnant en démo, mais qu’il est impossible d’industrialiser car il n'a jamais été confronté à la réalité des systèmes de l'entreprise. C'est le chemin le plus court vers le *purgatoire des projets pilotes*.

**Un prototype n'est pas un produit de production** ; le confondre est un anti-pattern classique : 95% des projets GenAI échouent à passer en production, souvent à cause de cette "vallée de la mort" entre le POC et l'industrialisation.

La complexité d'un agent doit toujours être pensée en fonction de son intégration future. C’est là que le rôle de Product Builder prend toute son importance : shipper vite en anticipant la scalabilité !



---



Ce constat étant fait, il convient de mettre en place des bonnes pratiques pour permettre un apport de valeur à l’échelle de l’entreprise et sortir de l’agent home made restreint by design à un petit périmètre. 

Cela implique de prendre en compte les différents enjeux de gouvernance pour parvenir à ses fins :

- **Les conflits de périmètre avec l'ingénierie** : la nature hybride du rôle peut créer des frictions, les ingénieurs peuvent percevoir le Product Builder comme du shadow IT créant des solutions non conformes, tandis que le Product Builder peut être frustré par la lenteur du développement traditionnel. Il donc est essentiel de ne pas réduire l'ingénierie à des rustines techniques.

- **La gouvernance, sécurité et limites des outils :** l'utilisation d'outils low-code et d'IA pose des risques de sécurité, de conformité (RGPD) et de souveraineté des données, tandis que les plateformes ont des limites de scalabilité, de performance et de personnalisation, et peuvent créer une dépendance (*vendor lock-in*).
