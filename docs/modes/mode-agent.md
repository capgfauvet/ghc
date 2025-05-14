# Mode Agent de GitHub Copilot

Le mode Agent permet d’automatiser des tâches complexes en interagissant directement avec l’environnement de développement et le code du projet. Il se distingue par sa capacité à orchestrer des workflows de bout en bout, à automatiser des opérations à grande échelle et à intégrer plusieurs outils pour une gestion avancée du projet. Ce mode est particulièrement adapté aux scénarios nécessitant une compréhension globale du code, des modifications multi-fichiers ou l’exécution de suites d’actions coordonnées, offrant ainsi une solution incontournable pour l’automatisation et la productivité dans des contextes complexes.

## Usages principaux

- Exploration de l’espace de travail et analyse de la structure du projet
- Recherche et modification de fichiers
- Exécution de commandes dans le terminal
- Génération de composants, modules ou fichiers
- Installation et configuration de dépendances
- Refactoring multi-fichiers
- Exécution et analyse de tests
- Résolution de bugs complexes

Exemple : « Corrige la fuite mémoire dans cette fonction. »

> Pour des explications ou questions sans modification de code, consulter le mode [Ask](./mode-ask.md).
> Pour des modifications ciblées sur une zone de code, voir le mode [Edit](./mode-edit.md).

## Considérations de sécurité

- L’agent a accès à l’ensemble de l’espace de travail et peut modifier des fichiers
- Il peut exécuter des commandes dans le terminal avec les privilèges de l’utilisateur
- Examiner attentivement les commandes et modifications proposées avant validation
- Ne jamais demander l’exécution de code dont la fonction n’est pas comprise
- Ne pas utiliser l’agent sur des données sensibles sans comprendre les implications
