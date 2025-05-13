# Instructions pour GitHub Copilot

L’application des instructions par GitHub Copilot est entièrement automatique dès lors que les fichiers sont correctement renseignés et placés à l’emplacement attendu (soit `.github/copilot-instructions.md` pour le fichier principal, soit `.github/instructions/*.instructions.md` pour les instructions avancées).

## Le fichier principal : `copilot-instructions.md`

Le fichier `copilot-instructions.md` permet de fournir des instructions personnalisées à GitHub Copilot. Il doit être placé dans le dossier `.github/` à la racine du repository, soit à l'emplacement : `.github/copilot-instructions.md`. Ce fichier adapte les suggestions et réponses de Copilot au contexte du projet.

### Objectif et utilisation

Ce fichier permet de :

- Définir le contexte du projet
- Spécifier des standards de code et bonnes pratiques
- Fournir des instructions spécifiques au domaine
- Orienter le comportement de Copilot selon les besoins

### Format et contenu recommandé

#### Structure de base

```markdown
# Instructions pour GitHub Copilot

## Contexte du projet

[Description générale du projet, de son objectif et de son domaine]

## Standards de code

[Description des standards de code et conventions à suivre]

## Architecture

[Information sur l'architecture du projet]

## Instructions spécifiques

[Instructions précises pour Copilot]
```

## Les fichiers avancés : .instructions.md

En complément du fichier principal, il est possible d'utiliser des fichiers d'instructions spécifiques avec l'extension `.instructions.md` dans le dossier `.github/instructions/`. Ces fichiers permettent de cibler des contextes, langages ou tâches précises grâce à la propriété `applyTo` (utilisation des [glob patterns](https://code.visualstudio.com/docs/editor/glob-patterns)).

### Exemple de structure

```markdown
---
applyTo: "**/*.js"
---

# Standards JavaScript

- Toujours utiliser `const` ou `let` (jamais `var`)
- Préférer les fonctions fléchées pour les callbacks
- ...
```

## Meilleures pratiques

- Rédiger des instructions courtes et autonomes. Chaque instruction doit être une affirmation simple et unique.
- Pour transmettre plusieurs informations, utiliser plusieurs instructions distinctes.
- Ne pas faire référence à des ressources externes (ex : standards de codage précis) dans les instructions, afin d'éviter des références non comprises ou non accessibles par Copilot.
- Organiser les instructions en plusieurs fichiers selon les thématiques ou types de tâches. Cette approche facilite la maintenance, permet de référencer des instructions personnalisées dans les fichiers de prompts, et évite la duplication pour différentes tâches.

## Instructions de domaine spécifique

```markdown
## Instructions métier pour e-commerce

- Les prix doivent toujours être calculés avec 2 décimales
- La TVA doit être appliquée avant les remises
- Les commandes suivent le cycle : Créée -> Payée -> Préparée -> Expédiée -> Livrée
```
