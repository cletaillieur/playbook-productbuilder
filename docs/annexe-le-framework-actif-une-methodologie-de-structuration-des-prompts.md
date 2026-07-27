---
authors:
  - "Etienne Fenetrier"
last_updated: "2026-03-12"
---

# Annexe - Le framework ACTIF, une méthodologie de structuration des prompts

Pour appliquer ces principes de manière standardisée, le Product Builder s'appuie sur une méthode de structuration de prompt. Il en existe plusieurs (STAR, RODE, etc.).

Le framework ACTIF est l’une des méthodes que le Product Builder doit utiliser pour rédiger les spécifications de son Contrat du Prompt.

⇒ Exemple de Contrat du Prompt basé sur ACTIF 

Voici comment un Product Builder spécifierait une tâche d'analyse de sentiment pour l'équipe d'ingénierie.

**A (Action) :** “Tu dois analyser une liste d'avis clients et pour chacun, identifier le sentiment (Positif, Négatif, Neutre), le sujet principal (Livraison, Qualité Produit, Service Client) et extraire une citation clé.”

**C (Contexte) :** “Ces avis proviennent de notre site e-commerce pour le produit 'Chaise Ergonomique Pro'. Voici trois exemples pour te guider :

- Livraison rapide mais la chaise grince → Sentiment : Négatif, Sujet : Qualité Produit.

- Super confortable, je recommande → Sentiment : Positif, Sujet : Qualité Produit.

- Le suivi de colis était clair → Sentiment : Positif, Sujet : Livraison.”

**T (Tonalité) :** “La sortie doit être neutre et informative. Pas de phrases, juste les données.”

**I (Identité) :** “Tu es un outil d'analyse de données NLP. Tu es précis, factuel et ne donne jamais ton opinion.”

**F (Format) :** “La sortie doit être un tableau au format Markdown avec les colonnes suivantes : *ID Avis, Sentiment, Sujet Principal, Citation Clé*.”

Cette approche structurée garantit que toutes les facettes du comportement de l'IA sont définies, créant un contrat clair et testable pour l'équipe d'ingénierie.
