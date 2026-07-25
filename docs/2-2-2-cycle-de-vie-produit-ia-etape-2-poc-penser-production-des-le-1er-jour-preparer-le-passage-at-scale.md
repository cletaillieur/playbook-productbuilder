---
title: "2.2.2 Cycle de vie Produit IA - Étape 2 : POC, penser production dès le 1er jour - Préparer le passage at scale"
authors:
  - "Avenert Cazako"
last_updated: "2026-03-17"
source_row_uri: "coda://docs/1aAVKYnF9N/tables/grid-sync-1054-Table-dynamic-9dd960ee3688f9f5a4d38a2afa1f41988605de8e5cddc8199d6fe000a5293120/rows/i-DgPKzxLi6Q"
source_canvas_uri: "canvases/grid-sync-1054-Table-dynamic-9dd960ee3688f9f5a4d38a2afa1f41988605de8e5cddc8199d6fe000a5293120::i-DgPKzxLi6Q::c-YJDQrE0G_P"
migration_source: "Coda MCP"
access_level: "à vérifier"
status: "migrated-pilot"
---

# 2.2.2 Cycle de vie Produit IA - Étape 2 : POC, penser production dès le 1er jour - Préparer le passage at scale

Le rôle du Product Builder est certes de construire vite pour tester une idée, mais aussi de savoir anticiper la phase d’industrialisation pour éviter que son projet ne reste à l’état de POC. Cela ne veut pas dire que tout doit être optimisé dès le prototypage, mais que les contraintes doivent être envisagées dès le départ pour assurer la pertinence du test. 

​

**Quelques questions pour cadrer le besoin et les contraintes :**

- Quel résultat attend-on du modèle ? 

- Comment le modèle va-t-il être utilisé? 

- Quels sont les enjeux de gouvernance et le cadre légal à prendre en compte ?

- Quel budget et quelles ressources est-on prêt à allouer au modèle ?

  


Le POC du Product Builder ne doit pas forcément répondre à tous ces besoins parfaitement, car il pourra être amélioré en phase d’industrialisation, mais **le but est de partir dès le début sur une idée qui puisse être déployée à l’échelle et d’anticiper des problèmes de fond** qui rendraient un déploiement plus large impossible. 

Le Product Builder peut se servir du *vibe coding* pour développer son produit rapidement et sans validation extérieure. Mais moins le code est relu, plus la QA devient cruciale.

Pour les builders qui ne viennent pas du développement, il est important de s’acculturer aux bonnes pratiques du code et de l’IA. Ces quelques principes de base éviteront déjà beaucoup de problèmes :

- Toujours utiliser un environnement de test, ne jamais déployer directement sur l’environnement live.

- Avoir un code organisé et avec des commentaires qui permettront de faciliter la relecture humaine

- Comprendre le versioning, Git.

- Sécuriser la clé API (ne pas avoir une clé visible dans un repo publique par exemple)

- Inclure des *unit tests* dans le code pour la robustesse (les LLMs peuvent le faire très rapidement).

- Connaître les bases de l’évaluation d’IA (précision, vitesse de réponse, coût par inférence, biais) pour pouvoir déterminer si le POC est probant ou non. 

- Etc.

La liste pourrait être très longue et il ne faut pas chercher la perfection pour garder en agilité, mais si le POC est déployé auprès d’un grand nombre d’utilisateurs ou s’il est déployé à l’externe, un niveau minimum de qualité est nécessaire.

Pour contrôler la qualité du produit, le Product Builder peut s’associer avec un SME (Subject Matter Expert) qui pourra valider le contenu ou le ton des réponses. Pour la partie plus technique, il existe aussi des outils d’aide à la QA (PromptFoo, LangSmith, DeepEval…) qui peuvent couvrir une partie des cas.

À noter qu’un POC développé par le Product Builder est là pour valider une idée : il est possible de le construire sans se demander quel langage choisir, mais cela rendra l’industrialisation plus difficile. En pratique, beaucoup d’outils de *vibe coding* permettent aujourd’hui de choisir le langage, donc autant coder directement dans le langage utilisé dans les autres produits de l’entreprise pour faciliter l’industrialisation ensuite. 

Mais cette préparation technique ne suffit cependant pas. Le passage à l'échelle impose également au Product Builder une transformation profonde de son rôle.
