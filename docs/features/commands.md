# Commandes spéciales essentielles du chat GitHub Copilot

Le chat de GitHub Copilot propose plusieurs commandes spéciales essentielles que vous devez connaître. Ces commandes permettent à GitHub Copilot d'accéder à des informations auxquelles il n'aurait pas accès autrement.

> [!IMPORTANT]
> Ces commandes sont principalement utiles dans le [mode Ask](../modes/mode-ask.md) de GitHub Copilot. Dans les modes [Agent](../modes/mode-agent.md) et [Edit](../modes/mode-edit.md), GitHub Copilot importe automatiquement le contexte nécessaire. Parmi ces commandes, la référence vers les fichiers (`#file:`) reste la plus utilisée dans tous les contextes.

## Commandes avec préfixe

Ces commandes permettent à GitHub Copilot d'accéder à des contextes spécifiques et d'enrichir ses connaissances pour mieux répondre à vos questions.

### `#web`

Permet à GitHub Copilot d'accéder à Internet pour rechercher des informations récentes ou spécifiques.

```
#web Quelle est la dernière version de React et quelles sont ses nouvelles fonctionnalités ?
```

### `#fetch`

Alternative pour récupérer des informations depuis Internet, similaire à `#web` mais optimisée pour certains types de contenu.

```
#fetch https://github.com/username/repository Analyse ce dépôt GitHub.
```

### `#terminalLastCommand`

Donne accès à l'historique de votre terminal et à la dernière commande exécutée.

```
#terminalLastCommand Pourquoi cette commande échoue-t-elle ?
```

### `#file:<chemin_du_fichier>`

Permet d'accéder à un fichier spécifique hors du contexte actuel.

```
#file:src/utils/auth.js Peux-tu m'expliquer ce que fait ce code ?
```

> [!TIP]
> Il n'est pas nécessaire d'écrire la commande entière. Tapez simplement `#` suivi du début du nom du fichier et l'autocomplétion de Visual Studio Code vous proposera automatiquement les fichiers correspondants.

### `#codebase`

Permet d'explorer votre projet pour trouver les fichiers pertinents à votre question.

```
#codebase Comment puis-je optimiser ce composant ?
```

## Commandes avec préfixe @

Ces commandes permettent d'obtenir une aide spécifique sur différentes technologies et outils.

### `@workspace`

Fournit un contexte global sur votre projet en cours.

```
@Workspace Comment puis-je structurer ce projet ?
```

### `@vscode`

Fournit de l'aide sur Visual Studio Code, ses commandes et ses fonctionnalités.

```
@vscode Comment configurer le débogage pour une application Node.js ?
```

### `@terminal`

Fournit des informations sur les commandes et opérations du terminal.

```
@terminal Comment puis-je créer un script bash pour automatiser mes déploiements ?
```

### `@azure`

Fournit de l'aide spécifique sur les services et fonctionnalités Azure.

```
@azure Comment configurer un Azure Function avec authentification ?
```

### `@github`

Fournit de l'aide sur GitHub, ses fonctionnalités et bonnes pratiques.

```
@github Comment configurer des GitHub Actions pour mon projet ?
```
