# Optimisation du prompting avec GitHub Copilot

L'art du prompting est essentiel pour obtenir des réponses précises et adaptées de GitHub Copilot. Cette page présente les principes fondamentaux du prompting, la gestion du contexte et les techniques pour formuler des requêtes efficaces.

## Qu'est-ce que le prompting avec Copilot ?

Le prompting désigne la manière de formuler les requêtes adressées à Copilot. Un prompt bien construit guide l'IA pour générer des suggestions pertinentes, en tenant compte du contexte fourni.

### Types de contexte

#### 1. Contexte de conversation

- L'historique des messages échangés dans la session actuelle

#### 2. Contexte de code

- **Implicite** : Le fichier actuellement ouvert dans l'éditeur
- **Explicite** : Les fichiers référencés via `#file:`

#### 3. Instructions personnalisées

- Si un fichier `.github/copilot-instructions.md` existe dans le dépôt, son contenu est automatiquement intégré dans le contexte et permet de personnaliser le comportement de GitHub Copilot

> [!NOTE]
> L'enrichissement du contexte est possible grâce aux commandes spéciales décrites dans [commandes.md](./commandes.md).

## Limites et contraintes du contexte

GitHub Copilot possède une limite de contexte (nombre de tokens qu'il peut traiter) :

- Les fichiers volumineux peuvent facilement dépasser cette limite
- Les conversations longues réduisent l'espace disponible pour le nouveau contexte
- L'historique de conversation ancien peut être omis dans les sessions très longues

### Signes d'un contexte saturé

- Copilot commence à ignorer certaines informations fournies
- Les réponses deviennent moins précises ou pertinentes
- Copilot "oublie" des détails mentionnés précédemment

## Stratégies d'optimisation du contexte

### Techniques avancées

#### Structuration du contexte

Pour optimiser la prise en compte des informations par GitHub Copilot, il est recommandé de structurer le contexte de manière réfléchie :

- **Priorisation** : placer les éléments essentiels en début de message afin de garantir leur prise en compte prioritaire.
- **Contextualisation progressive** : enrichir le contexte par étapes, en commençant par les informations principales puis en ajoutant progressivement des détails ou des précisions selon la complexité du sujet.

#### Segmentation des problèmes complexes

Pour les tâches complexes, décomposer le problème en petites parties et guider Copilot à travers chaque étape.
