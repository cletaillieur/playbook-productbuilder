---
title: "1.2.1 Compétences techniques d'un Product Builder"
authors:
  - "Avenert Cazako"
last_updated: "2026-03-24"
source_row_uri: "coda://docs/1aAVKYnF9N/tables/grid-sync-1054-Table-dynamic-9dd960ee3688f9f5a4d38a2afa1f41988605de8e5cddc8199d6fe000a5293120/rows/i-yPFirKpRmP"
source_canvas_uri: "canvases/grid-sync-1054-Table-dynamic-9dd960ee3688f9f5a4d38a2afa1f41988605de8e5cddc8199d6fe000a5293120::i-yPFirKpRmP::c-YJDQrE0G_P"
migration_source: "Coda MCP"
access_level: "à vérifier"
status: "migrated-pilot"
---

# 1.2.1 Compétences techniques d'un Product Builder

La force d’un Product Builder réside dans sa maîtrise des environnements no/low-code, qu’il met au service de deux objectifs clés : la maîtrise des outils d’automatisation (n8n, Make, Zapier) et de prototypage (Lovable, Bolt, Firebase Studio).

  
**Le prototypage rapide, pour donner vie à l’expérience IA**

Pour un produit IA, un cahier des charges ne suffit pas. L’expérience doit se vivre. Le Product Builder utilise donc des outils comme Lovable pour construire des prototypes interactifs.

Les objectifs de ce prototypage rapide sont triples :

- **Matérialiser la vision** : montrer concrètement comment l’agent interagira, bien au-delà d’un wireframe statique.

- **Dérisquer l’UX** : tester très tôt les réactions des utilisateurs pour identifier les points clés à aller approfondir en phase de recherche.

- **Faciliter l’alignement** : créer un objet de discussion concret pour les équipes métier, techniques et design.

Dans l’approche classique, un designer doit accepter de perdre beaucoup de temps à prototyper sur Figma en créant des liens interactifs linéaires. Il doit en perdre ensuite encore plus pour créer un prototype à choix multiple, afin de permettre à des utilisateurs de tester librement un parcours de plusieurs pages.

À l’inverse, aujourd’hui les possibilités de vibe design brisent ces contraintes pour tester mieux et plus rapidement dans un contexte concurrentiel où le time-to-market est plus important que jamais.

  
**L’automatisation, pour démontrer la valeur par l’action**

Les outils comme n8n, Make, Zapier ou Supabase constituent le couteau suisse du Product Builder. De fait, l’automatisation lui permet de construire des pipes de données fonctionnelles pour optimiser des processus existants ou pour simuler le back-end d’un futur produit.

**→ Un exemple concret : l’automatisation de la synthèse des retours clients**

Pour automatiser la synthèse des retours clients, le Product Builder peut créer un workflow sur Make qui :

1. Détecte chaque nouveau message posté dans un canal Slack dédié.

1. L’envoi à l’API d’OpenAI pour une classification de sentiment et une extraction d’entités.

1. Insère le résultat dans un tableau de bord Notion pour une analyse en temps réel.

En quelques heures et sans une ligne de code, il a non seulement optimisé un processus mais aussi démontré la valeur d’une approche agentique.



**La maîtrise des techniques IA fondamentales**

Pour le Product Builder, maîtriser les concepts comme le RAG (Retrieval-Augmented Generation) ou le Prompt Engineering n’est pas un exercice académique : c’est la clé pour augmenter sa propre efficacité et transformer des heures de travail manuel en quelques minutes d’analyse assistée.  
Avant même de construire un produit pour ses clients, il applique ces techniques pour son propre métier : la gestion de produit.

**→ Un exemple concret : l’augmentation de la phase de Discovery**

L’IA peut venir augmenter la phase de Discovery. Notamment dans une tâche classique et chronophage du PM : la synthèse d’entretiens utilisateurs destinés à préparer la prochaine roadmap. Cela peut commencer par la création de sa propre base de connaissance avec le RAG : le Product Builder centralise les 10 transcriptions dans un dossier. Ce dossier devient une mini base de connaissance privée.

Grâce au RAG, il ne relit plus, mais il interroge. Par exemple, il peut poser des questions directement à ses entretiens, comme : “*Quels sont les 3 ‘pain points’ les plus cités concernant notre processus d’onboarding ?*” ou “*Extrais-moi toutes les citations exactes qui mentionnent un concurrent*.”

Le Product Builder peut ensuite aller plus loin, jusqu’à la génération de livrables avec le Prompt Engineering. En utilisant des techniques de prompting avancées (Few-shot, Chain of Thought), il peut générer des synthèses ou même des user stories. Cela nécessite la création d’un Agent de Discovery personnel avec un prompt de ce type :

> *“Persona : Tu es un Product Manager senior spécialisé dans notre produit.  
Contexte : Tu as accès aux 10 entretiens utilisateurs que je viens de mener.  
Tâche : En te basant uniquement sur ces entretiens, rédige une user story complète au format “En tant que…, je veux…, afin de…”  pour le besoin le plus fréquemment exprimé par nos utilisateurs.  
Pense étape par étape pour construire ta réponse.”*

En quelques minutes, il est ainsi possible d’obtenir une user story fondée sur des données réelles, alors que ce travail lui aurait pris plusieurs heures manuellement.  


**La maîtrise des frameworks d’IA complexes**

Un prompt comme celui de l’exemple ci-dessus peut vite devenir complexe. Sans structure, se crée rapidement de la dette de prompt : c’est-à-dire des prompts mal conçus, non documentés, qui deviennent impossibles à maintenir ou à faire évoluer. Le Product Builder évite ce travers en utilisant des frameworks de prompting structurés.

C’est-à-dire qu’il **considère la structuration d’un prompt comme un jeu de Lego, avec des composants clairs et réutilisables** : au lieu d’un long texte, il utilise un format modulaire. Cette approche permet de limiter les cycles d’itération, de faciliter la collaboration (on peut partager des briques de prompt), et de construire des agents plus fiables et plus faciles à déboguer.

  
**→ Un exemple concret : un prompt structuré pour un agent expert marketing**

```
RÔLE
Tu es un analyste marketing expert.
CONTEXTE
Tu analyses des verbatims clients pour un produit e-commerce.
TÂCHE
Catégorise le verbatim suivant en : ‘Livraison’, ‘Qualité Produit’, ‘Paiement’.
FORMAT DE SORTIE
Réponds uniquement avec la catégorie.
VERBATIM
{insérer le verbatim ici}
```



**L’évaluation de la data**

Au quotidien, le Product Builder doit aussi savoir se comporter comme un véritable détective de la donnée. Avant de construire un produit IA, sa première mission est d’auditer la matière première qui formera l’intelligence de l’agent. Le Product Builder évalue chaque source de données avant de l’exploiter. Il en mesure le potentiel et les risques, car pour un LLM, le principe est implacable : *garbage in, garbage out*. Un produit IA premium ne peut être construit que sur des fondations de données irréprochables.

**→ Un exemple concret : un chatbot basé sur une FAQ**

Dans le cadre du développement d’un chatbot FAQ pour une marque du secteur de l’habillement, le Product Builder de Converteo ne s’est pas contenté de lire la page FAQ existante. Son analyse a été plus profonde et s’est structurée autour de nombreuses questions, dont :

- **La donnée est-elle à jour ?** (“cette politique de retour de 2021 est-elle encore valable ?”).

- **Est-elle complète ?** (les 5000 derniers tickets de support révèlent que le suivi de commande est le vrai sujet n°1, pourtant absent de la FAQ).

- **Est-elle fiable ?** (pourquoi la FAQ mentionne “3-5 jours” de livraison quand la doc interne dit “7 jours” ?).

- **Enfin, est-elle propre ?** (les balises HTML et le jargon interne vont polluer les réponses de l’agent).

À l’issue d’un tel audit, le rôle de le Product Builder n’est pas de bloquer le projet, mais de proposer une solution stratégique en réponse à ses constats.
