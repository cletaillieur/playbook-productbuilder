---
title: "2.3.4 Cycle de vie Produit IA - Étape 3 : Dossier de passation - Archi technique et modèle de données"
authors:
  - "Erik Perrier"
last_updated: "2026-03-17"
source_row_uri: "coda://docs/1aAVKYnF9N/tables/grid-sync-1054-Table-dynamic-9dd960ee3688f9f5a4d38a2afa1f41988605de8e5cddc8199d6fe000a5293120/rows/i-_0emuyJHvl"
source_canvas_uri: "canvases/grid-sync-1054-Table-dynamic-9dd960ee3688f9f5a4d38a2afa1f41988605de8e5cddc8199d6fe000a5293120::i-_0emuyJHvl::c-YJDQrE0G_P"
migration_source: "Coda MCP"
access_level: "à vérifier"
status: "migrated-pilot"
---

# 2.3.4 Cycle de vie Produit IA - Étape 3 : Dossier de passation - Archi technique et modèle de données

Durant la phase de prototypage, le Product Builder a souvent empilé des outils et des API sans réelle contrainte d'infrastructure. Pour l'industrialisation, cette approche artisanale doit se transformer en une spécification d'architecture claire, même si le Product Builder n'implémente pas lui-même les composants.

Son rôle n'est pas de devenir architecte système, mais de documenter les choix fonctionnels qui ont un impact direct sur l'expérience utilisateur et la performance métier. Il doit traduire la logique produit en contraintes techniques compréhensibles par les ingénieurs.

​

**→ Un exemple concret : une orchestration multi-agents pour traiter la Voix du Client (VOC)**

Les équipes Voix du Client de Converteo développent une architecture agentique pour automatiser le traitement des enquêtes de satisfaction d'un grand groupe énergétique. Le système repose sur plusieurs agents spécialisés qui collaborent pour transformer les verbatims en actions concrètes.

L'**agent de classification ou de pré-analyse** constitue la première brique : il classifie automatiquement les verbatims parmi 70 catégories (problèmes d'accès à l'espace client, suivi de consommation, facturation, etc.). 

Cette classification est le point de départ d'un routage intelligent vers d'autres agents spécialisés. Par exemple, lorsqu'un problème de connexion est identifié, **un agent SI** est déclenché. Il accède aux logs de connexion pour vérifier si l'utilisateur a réellement rencontré une erreur technique. Si c'est le cas, l'information remonte directement aux équipes infrastructure concernées.

Un **agent CRM** vient compléter le dispositif pour enrichir l'analyse avec les données client. 

Enfin, **un agent de restitution** génère des synthèses mensuelles avec KPI pour tenir informées les différentes équipes métier, qui conservent la main sur les actions à mener.

L'orchestration de ces différents agents permet de passer d'une analyse manuelle chronophage à un système semi-automatisé qui garde l'humain dans la boucle pour les décisions stratégiques.



**→ Un exemple concret : une architecture modulaire pour anticiper les évolutions d’un assistant** 

Pour répondre aux trois use cases d’un assistant IA d’une plateforme retail media - RAG sur documentation, requêtes analytiques simples et analyses de corrélations - le Product Builder a fait le choix d'une architecture multi-agent orchestrée.

Plutôt qu'un agent unique essayant de tout faire, le système repose sur :

1. Un agent orchestrateur qui analyse la requête utilisateur et route vers le bon agent spécialisé.

1. Un agent RAG dont le rôle exclusif est de faire des recherches dans les bases de connaissance.

1. Un agent Looker capable d'interroger la base de données via des requêtes analytiques.

1. Un agent Corrélation qui utilise l'agent Looker plusieurs fois pour identifier des relations entre différentes métriques.

Cette architecture modulaire offre plusieurs avantages :

- Contexte maîtrisé : chaque agent dispose uniquement du prompt système et des connaissances nécessaires à sa tâche, réduisant la pollution du contexte et améliorant la précision.

- Évolutivité : ajouter un nouvel agent (ex: un agent de recherche web) ne nécessite qu'une nouvelle classe et une ligne de configuration.

- Maintenance facilitée : modifier le comportement du RAG n'impacte pas les agents analytiques.

En complément, un agent juge a été ajouté pour scorer automatiquement la qualité des réponses, créant une boucle de feedback continue qui permet d'affiner progressivement les performances de chaque agent.
