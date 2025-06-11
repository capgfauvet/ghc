# Configuration de GitHub Copilot comme reviewer automatique

GitHub Copilot peut réviser automatiquement les pull requests lorsqu'elles sont créées avec le statut **Open** ou lorsqu'elles passent du statut **Draft** à **Open**. Une configuration simple permet d'activer cette fonctionnalité.

## Configuration sur un dépôt

- Accéder à la page principale du dépôt sur GitHub
- Cliquer sur **Settings** (droits d'administration sur le dépôt requis)
- Dans la barre latérale gauche : **Code and automation > Rules > Rulesets**
- Cliquer sur **New ruleset**
- Cliquer sur **New branch ruleset**
- Nommer l'ensemble de règles et définir le **Enforcement Status** sur **Active**
- Renseigner la/les **Target branches**
- Sous "Banch rules" : Cocher **Require a pull request before merging**, puis **Request pull request review from Copilot**
- Cliquer sur **Create**

Copilot ne révise qu'une fois automatiquement. Pour redemander une révision après modifications, cliquer sur **Request review** à côté du nom de Copilot dans les **Reviewers** de la pull request.

> Extrait de la [documentation officielle](https://docs.github.com/fr/copilot/using-github-copilot/code-review/configuring-automatic-code-review-by-copilot).
