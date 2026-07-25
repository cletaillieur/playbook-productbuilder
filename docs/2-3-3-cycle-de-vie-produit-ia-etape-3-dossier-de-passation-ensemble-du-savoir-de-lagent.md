---
title: "2.3.3 Cycle de vie Produit IA - Étape 3 : Dossier de passation - Ensemble du savoir de l'agent"
authors:
  - "Duy Tan PHAM VU"
last_updated: "2026-03-17"
source_row_uri: "coda://docs/1aAVKYnF9N/tables/grid-sync-1054-Table-dynamic-9dd960ee3688f9f5a4d38a2afa1f41988605de8e5cddc8199d6fe000a5293120/rows/i-NQi7Mpufp7"
source_canvas_uri: "canvases/grid-sync-1054-Table-dynamic-9dd960ee3688f9f5a4d38a2afa1f41988605de8e5cddc8199d6fe000a5293120::i-NQi7Mpufp7::c-YJDQrE0G_P"
migration_source: "Coda MCP"
access_level: "à vérifier"
status: "migrated-pilot"
---

# 2.3.3 Cycle de vie Produit IA - Étape 3 : Dossier de passation - Ensemble du savoir de l'agent

Le Contrat du Prompt définit la personnalité de l'agent : son ton, ses limites, ses réflexes comportementaux. Le modèle de données, lui, constitue son intelligence et sa mémoire.

Cette distinction est fondamentale. Un agent peut être parfaitement programmé pour répondre avec courtoisie et précision, mais si on lui donne accès à un catalogue produit obsolète de 2022, il recommandera des articles qui n'existent plus. La qualité de ses réponses dépend directement de la qualité de ses connaissances.

En phase d'industrialisation, le rôle du Product Builder n'est pas de construire les pipelines de données, mais de devenir l’architecte de la connaissance. Il doit spécifier avec une rigueur absolue quelles données sont nécessaires, pourquoi elles sont fiables, et comment elles doivent être utilisées.

Négliger cette étape conduit inévitablement au syndrome du ***garbage in, garbage out*** : l'agent, s'appuyant sur des données obsolètes ou non pertinentes, répondra avec une confiance absolue, mais de manière totalement erronée. Le Modèle de Données est donc le document qui garantit la pertinence et la fiabilité des réponses de l'IA.

Il se structure autour de trois piliers fondamentaux : **la cartographie des connaissances** (Knowledge Mapping), **la garantie de la qualité des données** (Data Readiness) et **la spécification des métadonnées métier**.



**La cartographie des connaissances (Knowledge Mapping)** 

Durant la phase de prototypage, le Product Builder a souvent bricolé avec quelques fichiers pour prouver la faisabilité. Pour l'industrialisation, il doit formaliser cette exploration en une cartographie exhaustive des sources de vérité. Il ne s'agit pas de fournir les données elles-mêmes, mais de livrer une carte au trésor aux ingénieurs pour qu'ils sachent où creuser.

Cela implique donc de lister et prioriser toutes les sources d'information indispensables au bon fonctionnement de l'agent. Cette liste doit être actionnable pour l'équipe technique.

Pour un agent assistant commercial, la cartographie pourrait ressembler à ceci :

[ÉLÉMENT CODA À VÉRIFIER — référence à une table Coda intégrée (« Table 4 »), non développée par l'API : seul le lien a été retourné, pas les données de la table]
## [Table 4](https://coda.io/d/_dGKuDyag4nM#Table-4_tugrid-l0Gt9TQrf3)

**La garantie de la qualité des données (Data Readiness)**

Une fois les sources identifiées, le Product Builder doit en spécifier les critères de qualité. Son rôle est de s'assurer que les données sont prêtes pour l'IA avant que l'équipe d'ingénierie n'investisse du temps à construire des connecteurs. En tant que garant de la propreté de la matière première, il doit donc définir **les règles qui assurent que la donnée est fiable, à jour et propre.** Il agit comme un auditeur de la qualité. 

Quelques exemples de règles :

**Règle de fraîcheur :** "Toute information provenant des *Argumentaires Commerciaux* doit être considérée comme obsolète après 6 mois. Les documents doivent avoir un champ *last_updated*."

**Règle de complétude :** "Une *Fiche Produit* n'est exploitable que si elle contient au minimum les sections *Caractéristiques Techniques, Prix et Disponibilité*."

**Règle de nettoyage :** "Les transcriptions d'appels clients doivent être pré-traitées pour anonymiser tous les noms de personnes et les numéros de téléphone avant d'être envoyées au modèle."



**La spécification des métadonnées métier**

C'est l'étape la plus stratégique. Toutes les données n'ont pas la même valeur. Le Product Builder doit enrichir la simple donnée brute avec une couche d'intelligence métier : les métadonnées. Ces informations supplémentaires guident l'IA dans son raisonnement, lui permettant de hiérarchiser et de contextualiser l'information.

Ici, le rôle du Product Builder est de traduire la logique métier en attributs que les ingénieurs pourront attacher aux données lors de leur traitement (indexing). 

Par exemple :

**Métadonnée de priorité :** "Lorsqu'une information existe à la fois dans les *Fiches Produits* et les *Argumentaires Commerciaux*, la *Fiche Produit* fait toujours foi. Le Product Builder doit spécifier une note de priorité (ex: priorité: 1 pour les fiches produits, priorité 2 pour les argumentaires)."

**Métadonnée de péremption :** "Toute *Offre Promotionnelle* doit être taguée avec une date de fin (expiration_date). L'agent ne doit jamais proposer une offre dont la date est dépassée."

**Métadonnée d'audience :** "Les documents de la section *Juridique* doivent être tagués audience: *interne*. Si l'utilisateur final n'est pas identifié comme un employé Converteo, l'agent ne doit pas utiliser ces sources pour sa réponse."

En formalisant ces trois piliers, le Product Builder ne se contente pas de donner des fichiers à l'équipe technique. Il fournit un plan directeur pour la construction d'une base de connaissance fiable, intelligente et gouvernée, socle indispensable à un agent IA de production.

**Il est aussi important de définir comment l'information brute sera transformée en donnée structurée et intelligente.** Le Product Builder doit spécifier le schéma des métadonnées, cette couche d'intelligence métier qui permet à l'IA de raisonner sur les données. 



Par exemple : 

```
JSON
**{**
  **"document_id": "string",**
  **"source_name": "string",**
  **"document_type": ["Fiche Produit", "CR Réunion", "Note Juridique"],**
  **"creation_date": "YYYY-MM-DD",**
  **"expiration_date": "YYYY-MM-DD",**
  **"author": "string",**
  **"audience_tag": ["Public", "Interne", "Confidentiel"],**
  **"priority_level": "integer"**
**}**
```

Ce schéma garantit que chaque information est non seulement stockée, mais aussi contextualisée (sa fraîcheur, sa confidentialité, son importance).
