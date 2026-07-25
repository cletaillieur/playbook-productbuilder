---
title: "Annexe - L'exemple du Wrap UP agent RAIM 2025"
authors:
  - "Etienne Fenetrier"
last_updated: "2026-03-12"
source_row_uri: "coda://docs/1aAVKYnF9N/tables/grid-sync-1054-Table-dynamic-9dd960ee3688f9f5a4d38a2afa1f41988605de8e5cddc8199d6fe000a5293120/rows/i-kJr2DsP-Cq"
source_canvas_uri: "canvases/grid-sync-1054-Table-dynamic-9dd960ee3688f9f5a4d38a2afa1f41988605de8e5cddc8199d6fe000a5293120::i-kJr2DsP-Cq::c-YJDQrE0G_P"
migration_source: "Coda MCP"
access_level: "à vérifier"
status: "migrated-pilot"
---

# Annexe - L'exemple du Wrap UP agent RAIM 2025

Le cadrage était clair : suite à l’événement “Roadmap AI Marketing 2025”, produire un bilan personnalisé, à chaque participant, modelé sur son profil professionnel, ses intérêts et les sujets abordés le jour J dans l’événement. En somme, produire un email marketing avec un maximum de valeur.

L’approche a été la suivante :

- Synthétiser le contenu des conférences et interventions enregistré dans un format facilement exploitable (.mp4 —> .txt)

- Stocker les données pertinentes des participants (fonction, entreprise / secteur d’activité) et dégager une logique de mots clés / enjeux liés avec le contenu abordés pendant l’événement

- Rédaction d’un bilan personnalisé en deux parties via un prompt Gemini (extract du prompt ci-dessous) :

  - Partie 1 (synthèse générale) : présente les grandes idées fortes de la journée, identifiées à l'étape 1. Rends cette partie inspirante et donne une vision globale des futurs possibles du marketing.

  - Partie 2 (focus personnalisé) : utilise le fruit de ta réflexion de l'étape 2. Adresse-toi directement au participant (en utilisant "vous" et son prénom). Fais le lien entre un ou deux thèmes forts et son quotidien professionnel. Propose des pistes de réflexion ou des questions ouvertes qui l'inciteront à appliquer ces idées.

- Appliquer ce bilan dans un template PDF prédéfini

- Envoyer un mail personnalisé à chaque participant

Ce POC déguisé sous forme de projet démontre la puissance d’un Product Builder, mais souligne aussi les guidelines à suivre.

- Agilité acquise avec l’IA : 1 semaine de production pour créer un POC fonctionnel vs. potentiellement des mois de développement classique (cadrage, itération, specification, test, déploiement, etc.). Cette agilité a été permise par la puissance des outils IA :

  - Conversion .mp3 —> .txt : Grâce à Deepgram, un outil optimisé par l’IA, les transcriptions des conférences ont été générées en une journée, sans perte de qualité.

  - Génération d’un document .pdf en suivant un template en HTML, configurée sur Vertex AI.

  - Avec cette architecture, l’équipe a pu avancer rapidement. En 2 semaines, elle a réussi à trouver l’architecture adaptée, créer des données fictives, développer et tester l’agent IA, automatiser le processus, récupérer les données (post-event), cleaner, itérer et ajuster. Une quantité de travail envisageable  quelques années auparavant.

- La confirmation d’une nouvelle valeur métier : croiser rapidement et pertinemment la connaissance clients avec du contenus business. En l’occurrence il s’agit de sujets abordés lors des conférences, via des transcriptions elles mêmes générées via IA

- L’agilité a *enablé* la rapidité d’itérer, et donc permis d’affiner les choix, donnant lieu à un meilleure valeur métier :

  - Prompt engineering : en pouvant tester le résultat des versions successives des prompts rapidement, cela nous a permis d’affiner les consignes données à Gemini pour bâtir un bilan aussi bien personnalisé que pertinent.

  - Apprentissage avec la gestion de token : la maîtrise du switch button (Vertex AI) pour lancer l’agent a permis de contrôler les envois par batchs de 10 dans un premier temps pour contrôler la qualité du rendu, puis ensuite augmenter petit à petit tout en optimisant l’utilisation des tokens de l’IA (équilibre à trouver entre qualité du rendu et taille des batchs)

En revanche, le Product Builder garde toujours en tête les bonnes pratiques et évite de tomber dans le piège de l’effet tunnel à cause de l’efficacité des outils :

- Utiliser des données réelles pour garder la pertinence/valeur métier

  - Dans la phase de test, un jeu de données factices a été générées par Gemini en suivant un prompt spécifique pour avoir les catégories nécessaires au traitement

  - Le POC final a été alimenté directement sur la base de données des participants à l’événement

- Prototyper avec des outils structurés : Converteo étant partenaire Google, le choix a été fait de rester sur cette suite avec Vertex AI & Gemini, déjà bien intégré à l’écosystème de l’entreprise. Deepgram a été ajouté dans l’architecture dans la mesure où il s’agit d’un outil performant pour le besoin en question (transcription .mp3 —> .txt).

- Le choix de Deepgram a été fait dans l’optique d’anticiper les systèmes de gouvernance et le suivi de qualité. En effet, le chiffrement des données est un pilier fondamental de leur approche. Deepgram chiffre toutes les informations sensibles ou confidentielles, que ce soit en transit (les données sont chiffrées lorsqu'elles sont envoyées vers et depuis leurs serveurs (via SSL/TLS ou des protocoles similaires) ou **au repos (l**es données stockées sur leurs serveurs sont également chiffrées.)
