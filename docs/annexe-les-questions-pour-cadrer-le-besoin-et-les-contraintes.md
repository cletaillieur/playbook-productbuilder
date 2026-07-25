---
title: "Annexe - Les questions pour cadrer le besoin et les contraintes"
authors:
  - "Etienne Fenetrier"
last_updated: "2026-03-12"
source_row_uri: "coda://docs/1aAVKYnF9N/tables/grid-sync-1054-Table-dynamic-9dd960ee3688f9f5a4d38a2afa1f41988605de8e5cddc8199d6fe000a5293120/rows/i-m9pw0S9Wlr"
source_canvas_uri: "canvases/grid-sync-1054-Table-dynamic-9dd960ee3688f9f5a4d38a2afa1f41988605de8e5cddc8199d6fe000a5293120::i-m9pw0S9Wlr::c-YJDQrE0G_P"
migration_source: "Coda MCP"
access_level: "à vérifier"
status: "migrated-pilot"
---

# Annexe - Les questions pour cadrer le besoin et les contraintes

**Quel résultat attend-on du modèle ?** 

- Est-ce que la tâche pourrait être accomplie sans IA ou avec un modèle de machine learning classique ? 

- Quel est le degré de personnalisation du modèle nécessaire ? Est-ce qu’un modèle clé en main pourrait être utilisé tel quel ? Est-ce qu’il faudrait ajouter un RAG, du fine-tuning ou créer un modèle 100% sur-mesure ?

- Si le modèle doit être entraîné, quelles sont les données accessibles? 

**Comment le modèle va-t-il être utilisé?** 

- Comment l’utilisateur final accèdera-t-il au modèle ? 

- A quels outils existants le modèle devra-t-il être connecté ?

- Faut-il que le modèle soit accessible hors ligne ?

- Quel est le temps de réponse maximal que peut avoir le modèle ?

- Quel est le degré d’erreur maximal acceptable ? 

**Quels sont les enjeux de gouvernance et le cadre légal à prendre en compte ?**

- A quel point les données utilisées pour le modèle sont-elles sensibles ? Le modèle pourra-t-il garantir la sécurité des données ? 

- Quel serait l’impact d’une erreur du modèle et le risque pour l’entreprise ?

- Y a-t-il des obligations légales à respecter (RGPD par exemple) ?

- Y aura-t-il des contraintes sur l’hébergement du modèle ?

- Y a-t-il des enjeux de souveraineté et des préférences quant à la nationalité de l’entreprise fournissant le modèle ?

**Quel budget et quelles ressources est-on prêt à allouer au modèle ?**

- Quel budget l’entreprise souhaite-t-elle investir? Et quelles ressources humaines ?

- Quel mode de facturation et conditions d’utilisation serait préférable ? Abonnement et usage illimité, facturation par token…

- Comment s’effectuerait le monitoring et la maintenance du modèle ? Le modèle est-il accompagné d’un service client, d’une communauté active, ou de documentation ?

- Quels seraient les coûts additionnels associés ? Stockage des données, API calls, infrastructure
