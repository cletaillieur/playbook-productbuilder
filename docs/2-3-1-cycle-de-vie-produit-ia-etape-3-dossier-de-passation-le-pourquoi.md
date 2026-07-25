---
authors:
  - "Alexia Maynart"
last_updated: "2026-03-17"
---

# 2.3.1 Cycle de vie Produit IA - Étape 3 : Dossier de passation - Le "Pourquoi"

Avant d'engager une équipe technique, le Product Builder doit apporter la preuve de la valeur de son produit via deux actions clés : 

- **La création d'un POC :** cet artefact n'est pas une première version du produit, mais un outil d'apprentissage rapide conçu pour rendre l'idée tangible et tester les hypothèses fondamentales : le problème est-il réel (désirabilité) et la solution est-elle techniquement envisageable (faisabilité) ? 

- **La collecte de retours qualitatifs :** en organisant des sessions de test avec des utilisateurs cibles, le Product Builder observe leurs comportements et écoute leurs réactions spontanées face au POC. L'objectif n'est pas de savoir s'ils aiment l'outil, mais de capturer leurs moments de frustration ("C'est trop lent"), leurs doutes ("Comment savoir si c'est vrai ?") et leurs moments de satisfaction ("Wow, quel gain de temps !").

Ces apprentissages bruts constituent la matière première du dossier de passation. Ils forment le “***Pourquoi”*** émotionnel et économique du projet, constitué des apprentissages utilisateurs, du business case et des objectifs métiers.



**Avec les apprentissages utilisateurs, il s’agit de traduire le quali en specs**, car le développeur n'est pas dans la tête de l'utilisateur.

Le rôle du Product Builder est de passer de ***l'émotion*** (le feedback) à ***la logique*** (une instruction claire). Un feedback comme “***c'est nul”***, est inutile. À l’inverse, un feedback comme ***“ça répond à côté de la plaque quand je parle du projet X”*** est une mine d'or. La mission du PM est de transformer cette mine d'or en instruction technique.

Parmi les questions clés à se poser :

- **Quelle est la cause racine de la frustration ?** *L'IA est "trop froide" ? L’agent ne comprend pas le scope? Etc.*

- **Puis-je transformer ce feedback en une règle binaire (Oui/Non) ?** *Feedback flou : “La réponse est trop longue”. Règle binaire : “La réponse dépasse-t-elle 200 mots ?” (Oui/Non).*

- **Comment pourrais-je l'illustrer avec un exemple "Avant/Après" ?** *Avant : Montrer la mauvaise réponse de l'IA pendant le test. Après : Écrire la réponse idéale que l'on attend.* 

Deux pièges sont toutefois à éviter :

- **Le piège de la sympathie** : ne pas juste lister les feedbacks. Il faut les regrouper par thèmes (ton, précision, formatage) et en extraire une règle générale.

- **Le piège de l'implicite** : ne jamais penser que *les développeurs vont comprendre*. Non, il faut tout écrire. Par exemple, “*L'IA doit être pro”* ne veut rien dire, alors que “*L'IA ne doit jamais utiliser de tutoiement ni d'émojis”* est une règle claire.



**Dans le Business Case technique,** le Product Builder présente ensuite les résultats de l'expérience, mettant en avant les chiffres les plus percutants qu’il a pu observer : temps gagné, nombre de clics évités, taux de satisfaction, etc. Une question clé à se poser peut être par exemple : *“Si je devais pitcher ce projet en 30 secondes à un directeur financier, quels KPIs j'utiliserais ?”* (probablement la ***réduction des coûts de X%*** ou un ***gain de productivité de Y heures/semaine***).

Il peut aussi se demander comment ce KPI va évoluer avec la mise en production : si le prototype a montré un gain de 10 min par tâche pour 10 personnes, en production, pour 200 personnes, quel serait l'impact financier annuel ? 

L’enjeu est simple : chaque partie prenante (Manager, Partner, Tech Lead, PM/PO et bien sûr client) doit comprendre ce qui justifie la dépense du capital. Le prototype n'était pas un jouet, c'était une expérience scientifique pour prouver une hypothèse de valeur. 

Parmi les pièges à éviter ici :

- **Les “*****vanity metrics”*** : “*l'IA a généré 1000* réponses” ne veut rien dire. À l’inverse, “*850 de ces 1000 réponses ont été jugées utiles et n'ont pas nécessité de réécriture”* est un KPI de qualité.

- **Oublier le coût** : le ROI doit aussi prendre en compte le coût futur (API, serveurs, maintenance). En cela, le Product Builder doit être réaliste. “*On gagne 1000€/mois mais l'outil en coûte 2000€/mois”* n'est pas un bon business case !

De fait, cela conduit à **une priorisation par la valeur**. Car si le prototype est un couteau suisse plein de gadgets cools, la V1 industrielle doit être un scalpel : moins de fonctions, mais une précision chirurgicale sur la fonction la plus importante. Le rôle du Product Builder ici est de décider ce qu'on garde et, surtout, ce qu'on jette (pour l'instant). **En somme, c'est le passage de ce qui est possible à ce qui est essentiel.**



Les questions clés à se poser :

- Si je ne pouvais garder qu'une seule fonctionnalité du prototype, laquelle serait-ce ? C'est le ***Must-Have***.

- Quelle est la fonctionnalité qui a généré le plus de “***Wow”*** chez les utilisateurs ? C'est probablement un ***Should-Have***.

- Quelle fonctionnalité était impressionnante en démo, mais que personne n'a réellement utilisée pendant les tests ? C'est un ***Won't Have***.

- Qu'est-ce qui est techniquement le plus complexe à industrialiser ? Si ce n'est pas un ***Must-Have***, il faut le déprioriser agressivement pour la V1.

Tous ces éléments et toutes ces décisions doivent être documentés afin d’apporter des informations claires aux équipes dev en industrialisation.

Dans ce processus, attention à ne pas s'attacher à une fonctionnalité seulement parce qu'elle est impressionnante techniquement. Si elle ne résout pas le problème ou ne s'aligne pas avec la valeur business de départ, elle doit attendre ! 

En outre, refuser de déprioriser, c’est le meilleur moyen de livrer un produit médiocre et en retard. Être un bon Product Builder, c'est savoir dire ***non*** ou ***pas maintenant***. La crédibilité du planning en dépend.

> Lire aussi : [Quels KPIs prendre en compte dans un projet IA](annexe-quels-kpis-a-prendre-en-compte-dans-un-projet-ia.md) en annexe.
