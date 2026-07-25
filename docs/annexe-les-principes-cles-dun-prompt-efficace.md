---
authors:
  - "Etienne Fenetrier"
last_updated: "2026-03-12"
---

# Annexe - Les principes clés d'un prompt efficace

Avant même de structurer le prompt, le Product Builder doit intégrer trois meilleures pratiques fondamentales qui garantissent la qualité de la réponse du modèle.

⇒ Clarté et Spécificité

Un prompt vague donnera une réponse générique. Plus le Product Builder est précis sur le contexte, la cible et le format attendu, meilleure sera la réponse.

**Pourquoi c'est important ?** L'IA n'a pas le contexte de vos projets. Le PM doit le lui fournir pour rendre les réponses précises et exploitables.

**Rôle du Product Builder :** fournir le contexte métier et les exemples pertinents qui permettent au modèle de comprendre la demande spécifique.

⇒ Langage Positif vs. Négatif

Il faut formuler les instructions en disant à l'IA ce qu'elle doit faire, plutôt que ce qu'elle ne doit pas faire. Les modèles réagissent mieux aux instructions positives et directes.

**Pourquoi c'est important ?** Une instruction négative (ex: "N'oublie pas de citer les sources") peut paradoxalement amener l'IA à se concentrer sur le concept à éviter. Une instruction positive (Cite systématiquement tes sources) est plus efficace.

**Rôle du Product Builder :** définir les actions attendues sous forme d'instructions affirmatives.

⇒ Structure et Ponctuation

La manière dont le prompt est structuré a un impact direct sur la structure de la réponse. Un prompt organisé facilite l'interprétation par l'IA et produit une réponse plus claire.

**Pourquoi c'est important ?** Si vous demandez un tableau ou un format de sortie particulier (JSON, Markdown), le modèle pourra le générer plus facilement, rendant la réponse directement utilisable par d'autres systèmes.

**Rôle du Product Builder :** définir le format de sortie attendu dans le Contrat du Prompt.
