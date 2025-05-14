# Mode Edit de GitHub Copilot

Le mode Edit permet de modifier, transformer ou corriger du code existant de façon interactive directement dans les fichiers du projet. Il est conçu pour des modifications de code rapides et ciblées, et non pour des tâches de raisonnement complexe ou de planification avancée.

## Usages principaux

- Optimisation ou refactorisation d’algorithmes
- Conversion de code d’un langage à un autre
- Correction de bugs ou d’erreurs
- Modernisation ou amélioration de la lisibilité
- Ajout de validations ou de gestion d’erreurs
- Application de bonnes pratiques

Exemple : « Remplace les concaténations par de l’interpolation de chaînes des fichiers [...]. »

> Pour des questions générales ou des explications sans modification de code, consulter le mode [Ask](./mode-ask.md). Pour des actions avancées ou des raisonnements complexes, voir le mode [Agent](./mode-agent.md).

## Différences avec le mode Agent

- **Portée de l’édition** : le mode Edit est adapté lorsque la demande concerne uniquement des modifications de code et que la zone à modifier est bien identifiée. Pour des modifications plus larges ou nécessitant une analyse contextuelle, consulter la documentation du [mode Agent](./mode-agent.md).
- **Durée** : le [mode Agent](./mode-agent.md) implique plusieurs étapes (détermination du contexte, planification, sélection des fichiers, etc.), ce qui peut allonger le temps de réponse.
- **Déterminisme** : le [mode Agent](./mode-agent.md) évalue le résultat des modifications et peut itérer plusieurs fois, rendant son comportement plus non-déterministe que le mode Edit.
- **Quota de requêtes** : selon la complexité de la tâche, une seule demande en [mode Agent](./mode-agent.md) peut générer de nombreuses requêtes vers le service backend.
