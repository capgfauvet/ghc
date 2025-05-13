# Dossier des prompts

Le dossier des prompts permet de stocker et réutiliser des instructions prédéfinies pour GitHub Copilot. Un prompt est un fichier Markdown portant l’extension `.prompt.md`, structuré pour guider Copilot dans l’exécution de tâches spécifiques.

## Emplacement et structure

Les prompts sont stockés dans le dossier `.github/prompts/` et portent l'extension `.prompt.md`.

Exemple d'organisation :

```
.github/prompts/
  ├── documentation.prompt.md
  ├── code-review.prompt.md
  ├── testing.prompt.md
  ├── refactoring.prompt.md
  └── ...
```

## Structure d’un fichier prompt

Un fichier prompt se compose de deux parties :

### 1. En-tête optionnel (Front Matter)

L’en-tête, délimité par `---`, permet de définir des métadonnées :

| Propriété     | Description                                                                                    |
| ------------- | ---------------------------------------------------------------------------------------------- |
| `mode`        | Mode de chat à utiliser lors de l’exécution du prompt : `ask`, `edit` ou `agent` (par défaut). |
| `tools`       | Liste des outils utilisables en mode agent (ex. : `terminalLastCommand`, `githubRepo`).        |
| `description` | Courte description du prompt.                                                                  |

Exemple :

```
---
mode: "agent"
tools: [terminalLastCommand, githubRepo]
description: "Génère un résumé de la sélection courante et propose une commande adaptée."
---
```

### 2. Corps du prompt

Le corps contient le contenu du prompt, rédigé en Markdown. Il peut inclure :

- Instructions en langage naturel
- Contexte supplémentaire
- Liens vers d’autres prompts ou fichiers d’instructions (liens relatifs recommandés)
- Titres, listes, blocs de code, etc.

## Utilisation des variables dans un prompt

Il est possible d’insérer des variables dynamiques dans le contenu du prompt, selon la syntaxe `${variableName}`. Les variables disponibles sont :

- **Variables d’espace de travail**

  - `${workspaceFolder}` : chemin du dossier racine
  - `${workspaceFolderBasename}` : nom du dossier racine

- **Variables de sélection**

  - `${selection}` : contenu sélectionné
  - `${selectedText}` : texte sélectionné

- **Variables de contexte fichier**

  - `${file}` : chemin du fichier courant
  - `${fileBasename}` : nom du fichier courant
  - `${fileDirname}` : dossier du fichier courant
  - `${fileBasenameNoExtension}` : nom du fichier sans extension

- **Variables d’entrée utilisateur**
  - `${input:variableName}` : valeur passée depuis le chat
  - `${input:variableName:placeholder}` : valeur avec texte d’aide

## Utilisation dans le chat Copilot

- Référencer un prompt avec : `#file:.github/prompts/nom-du-fichier`
- Ou taper `/nom-du-fichier` dans le chat
- Les prompts peuvent être combinés avec d’autres instructions

## Bonnes pratiques

- Garder les prompts concis et spécifiques
- Organiser par catégories ou fonctionnalités
- Mettre à jour selon l’évolution du projet

---
