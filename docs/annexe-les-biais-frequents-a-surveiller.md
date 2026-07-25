---
title: "Annexe - Les biais fréquents à surveiller"
authors:
  - "Etienne Fenetrier"
last_updated: "2026-03-12"
source_row_uri: "coda://docs/1aAVKYnF9N/tables/grid-sync-1054-Table-dynamic-9dd960ee3688f9f5a4d38a2afa1f41988605de8e5cddc8199d6fe000a5293120/rows/i-9QOcFATK3V"
source_canvas_uri: "canvases/grid-sync-1054-Table-dynamic-9dd960ee3688f9f5a4d38a2afa1f41988605de8e5cddc8199d6fe000a5293120::i-9QOcFATK3V::c-YJDQrE0G_P"
migration_source: "Coda MCP"
access_level: "à vérifier"
status: "migrated-pilot"
---

# Annexe - Les biais fréquents à surveiller

En plus de poser un problème d’expérience utilisateur et d’éthique, les biais de l’IA peuvent aussi être illégaux. Les biais peuvent venir d’un modèle pré-entraîné, ou des données qui ont été utilisées par la suite pour le spécialiser. 

Exemples de biais provenant des données : 

- Biais historique. Le LLM reproduit des préjugés et des discriminations jugés intolérables aujourd’hui parce qu’il se base sur tout l’historique des données, y compris sur des époques où les normes étaient différentes.

- Biais de sélection quand les données d’entraînement sous représentent certains groupes (par exemple problème de détection d’une couleur de peau parce qu’un LLM a été entraîné sur des photos de personnes d’une autre couleur de peau).

- Biais linguistique ou culturel. Une majorité de LLMs sont entraînés sur une plus grande quantité de données occidentales et en anglais, ce qui les peut faire baisser la pertinence des recommandations dans d’autres langues ou contextes culturels. 

Exemples de biais algorithmiques : 

- Amplification. Les modèles ont tendance à amplifier les biais présents (60% dans le dataset devient 90% dans l’output).

- Agrégation. À l’opposé, les modèles déterminent parfois une moyenne ne tenant pas en compte du contexte et risquent de faire la même recommandation même quand elle n’est pas pertinente (par exemple recommander le même nombre de calorie quel que soit l’âge, le poids et le sexe de la personne).
