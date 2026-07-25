---
title: "Annexe - Glossaire simplifié"
authors:
  - "Etienne Fenetrier"
last_updated: "2026-03-12"
source_row_uri: "coda://docs/1aAVKYnF9N/tables/grid-sync-1054-Table-dynamic-9dd960ee3688f9f5a4d38a2afa1f41988605de8e5cddc8199d6fe000a5293120/rows/i-CbpX2Ljkpu"
source_canvas_uri: "canvases/grid-sync-1054-Table-dynamic-9dd960ee3688f9f5a4d38a2afa1f41988605de8e5cddc8199d6fe000a5293120::i-CbpX2Ljkpu::c-YJDQrE0G_P"
source_embedded_table_uri: "coda://docs/GKuDyag4nM/pages/section-vm5HjfTJxw/tables/grid-gbdJmLw2b8"
migration_source: "Coda MCP"
access_level: "à vérifier"
status: "migrated-pilot"
---

# Annexe - Glossaire simplifié

[ÉLÉMENT CODA À VÉRIFIER — colonnes sans nom de schéma officiel : `table_columns_read` échoue techniquement sur cette table (imbriquée dans une cellule canvas, erreur serveur « canvas not found »). Les noms de colonnes ci-dessous ont été déduits de la ligne d'en-tête visuelle de la table (texte en gras et surligné en orange), récupérée via `table_rows_read` en contournement. La couleur de surlignage n'est pas représentable en Markdown standard et n'a pas été reportée — seul le contenu textuel est conservé intégralement.]

| Terme | Définition | Vulgarisation |
|---|---|---|
| Prompt | La consigne ou la commande que vous donnez à l'IA pour obtenir une réponse. | **Brief client 1 :** "Améliorez mon ROI" est un brief flou.<br>**Brief client 2 :** "Analyse mes campagnes SEA du Q3 et identifie le top 3 des axes d'optimisation" |
| Agent | Une IA qui ne se contente pas de répondre, mais qui agit. Elle utilise des outils pour accomplir une mission. | Un consultant vs. un dashboard Looker : le dashboard montre les KPIs. Le consultant utilise l'agent pour analyser, créer une présentation et envoyer un email de synthèse. L'agent exécute ces actions. |
| Contexte | L'ensemble des informations (instructions, documents, etc.) que vous fournissez à l'agent pour l'orienter. | Le dossier de mission sur le Drive : "Aide-moi à réaliser cette synthèse en t'inspirant des documents COPROJ sur le drive Client "XXX_XXX"" |
| Tools | Les capacités d'action de l'agent. Chaque outil lui donne un "pouvoir" spécifique. | La stack technique du consultant : un accès à BigQuery pour requêter la donnée, un script Python pour la nettoyer, une API Google Ads pour extraire les performances, etc. |
| RAG<br>(Retrieval Augmented Generation) | La méthode du ***livre ouvert*** : l'IA cherche l'info dans vos documents avant de répondre, au lieu d'inventer. | Un nouveau consultant vient de rejoindre le cabinet et demande des ressources pour faciliter son intégration. L'IA va avoir accès aux éléments intranet Converteo pour donner les ressources correspondantes au besoin. |
| Itération | Le processus d'amélioration continue : tester un prompt / agent, analyser le résultat, et l'ajuster en plusieurs cycles pour l'affiner. | Les différents cycles de développement : "Je construis une première version de mon agent mais il hallucine beaucoup."<br>Je passe en phase d'itération -> Je regarde en détail les raisons et j'ajuste le contexte qui était trop flou. |
| Fallback | Le plan B de l'agent. C'est l'action de secours prévue lorsqu'il est bloqué ou ne sait pas répondre. | Agent Expert en reporting financier : "Mon agent m'invente des réponses car il veut à tout prix m'apporter de la valeur."<br>Je lui indique qu'en cas de problème il peut me notifier qu'il n'a pas trouvé réponse à ma requête. |
| MCP | Un standard de communication qui permet à un agent de dialoguer de manière unifiée avec de multiples outils et sources de données. | C'est un adaptateur universel qui permet à un agent de se brancher sur n'importe quel outil sans créer une connexion sur mesure. |
