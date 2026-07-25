---
title: "Annexe - Quels KPIs à prendre en compte dans un projet IA ?"
authors:
  - "Etienne Fenetrier"
last_updated: "2026-03-12"
source_row_uri: "coda://docs/1aAVKYnF9N/tables/grid-sync-1054-Table-dynamic-9dd960ee3688f9f5a4d38a2afa1f41988605de8e5cddc8199d6fe000a5293120/rows/i-m5ZnlsT2s6"
source_canvas_uri: "canvases/grid-sync-1054-Table-dynamic-9dd960ee3688f9f5a4d38a2afa1f41988605de8e5cddc8199d6fe000a5293120::i-m5ZnlsT2s6::c-YJDQrE0G_P"
source_embedded_table_uri: "coda://docs/GKuDyag4nM/pages/section-vm5HjfTJxw/tables/grid-8ZadEHo3x2"
migration_source: "Coda MCP"
access_level: "à vérifier"
status: "migrated-pilot"
---

# Annexe - Quels KPIs à prendre en compte dans un projet IA ?

[ÉLÉMENT CODA À VÉRIFIER — colonnes sans nom de schéma officiel : `table_columns_read` échoue techniquement sur cette table (imbriquée dans une cellule canvas, erreur serveur « canvas not found »). Les noms de colonnes ci-dessous ont été déduits de la ligne d'en-tête visuelle de la table (texte en gras et surligné), récupérée via `table_rows_read` en contournement. Les couleurs de surlignage des cellules d'origine (bleu, vert, jaune, orange) ne sont pas représentables en Markdown standard et n'ont pas été reportées — seul le contenu textuel est conservé intégralement.]

| Catégorie de KPI | Indicateur Clé de Performance (Métrique) | Objectif & Utilité Stratégique |
|---|---|---|
| Qualité Intrinsèque du Modèle | **Précision et Fiabilité (Accuracy and Reliability)**<br>- Ancrage (Groundedness)<br>- Exactitude Factuelle<br>- Taux d'Hallucination | Mesurer la capacité du modèle d'IA à fournir des réponses correctes, basées sur les sources de données fournies, et à ne pas inventer d'informations. C'est la base de la confiance. |
| Qualité Intrinsèque du Modèle | **Cohérence et Fluidité (Coherence & Fluency)**<br>- Cohérence<br>- Fluidité du langage<br>- Verbosité (concision) | Évaluer si les réponses sont logiques, bien écrites, et directes. Une réponse juste mais mal formulée dégrade l'expérience utilisateur. |
| Qualité Intrinsèque du Modèle | **Performance Technique (Technical Performance)**<br>- Score F1<br>- Précision (retrieval)<br>- Taux d'appel de fonction valide | Pour les équipes techniques : Valider la performance brute du modèle sur des benchmarks standards (pertinence de la recherche, capacité à utiliser des outils externes). |
| Performance & Qualité Système | **Latence (Latency)**<br>- Latence du modèle<br>- Latence de la réponse complète | Garantir une expérience utilisateur fluide. Une IA trop lente, même si elle est juste, sera perçue comme un outil de mauvaise qualité et ne sera pas adoptée. |
| Performance & Qualité Système | **Fiabilité du Service (Reliability)**<br>- Disponibilité (Uptime en %)<br>- Taux d'erreur | S'assurer que le service est fonctionnel et accessible en quasi-permanence. Un outil indisponible est un outil inutile. |
| Adoption & Satisfaction Utilisateur | **Engagement & Rétention**<br>- Taux d'adoption (utilisateurs actifs)<br>- Taux de rétention- Sessions par utilisateur | Mesurer si les utilisateurs intègrent l'outil dans leurs habitudes de travail. Une forte rétention est le meilleur indicateur de la valeur perçue. |
| Adoption & Satisfaction Utilisateur | **Satisfaction & Sentiment**<br>- NPS (Net Promoter Score)<br>- CSAT (Customer Satisfaction Score)<br>- Analyse de sentiment | Suivre l'impact direct du chatbot sur la satisfaction et la perception des utilisateurs. Permet de détecter les points de friction et les "Wow moments". |
| Valeur Métier & ROI | **Efficacité Opérationnelle**<br>- Temps de traitement moyen (AHT)<br>- Taux de résolution au premier contact<br>- Taux de confinement (Containment) | Quantifier les gains de productivité directs. Mesure la capacité de l'IA à traiter des tâches plus rapidement et de manière autonome, sans intervention humaine. |
| Valeur Métier & ROI | **Impact Financier (ROI)**<br>- Réduction des coûts opérationnels<br>- Temps économisé par employé<br>- Augmentation du chiffre d'affaires (si applicable) | Traduire les gains de productivité et l'amélioration de l'expérience client en valeur monétaire. C'est l'indicateur ultime pour justifier l'investissement. |
| Valeur Métier & ROI | **Expérience Client & Croissance**<br>- Réduction du taux d'attrition (Churn)<br>- Temps passé sur le site/la plateforme | Estimer l'impact positif à long terme sur la fidélité des clients et leur engagement avec la marque, générant une croissance durable. |
