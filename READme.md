# Git commandes

## Différents status de GIT

- **Non indexer** de base lorsque vous ajoutez un nouveau fichier
- **indexer mais pas encore ajouter** pour indexer seulement il va falloire utiliser la command **git add -N nomDuFichier**
- **indexer mais ajouter** pour ajouter les changements de votre fichier il va falloire utiliser la command **git add nomDuFichier**
- **indexer et valider** pour valider vos changements et avoir une branch sans changement il faut commit et donc utiliser la commande \*\*git commit -m(message) "Votre message"

> vous avez nottamment une commande pour visualiser les commit qui ont été soit par vous même soit par votre équipe la commande git est log.

> ex: **git log**

On peut nottamment lier un remote distant à notre projet git avec la command **git remote add NomAlias URLclientGit ex: https://github.com/Pseudo/monProjet.git**

sur notre remote on peut bien évidemment avoir tous ce que que nous avons en local en faisant aprés un **commit** un **push**

> ex: si vous venez seulement d'ajouter votre remote il va falloire faire la commande ci-dessous

- **git push -u NomDeVotreAlias(par convention le nom de l'alias est origin) master(le nom de la branche cibler)**

sinon si vous avez déjà fais la commande ci-dessus il va falloir utiliser cette commande

- **git push**

## Les sous branches

Vous avez deux commandes pour pouvoir faire des sous branch sois vous devriez utiliser la commande

- **git branch NomDeVotreBranche**
  Ou bien
- **git checkout -B NomDeVotreBranche**

la différence entre c'est deux commande est que la deuxième commande permet à la fois de créer votre branche et vous switchez directement demande

> à noté que l'argument -B permet aussi de remplacer la branche si elle existe déjà à utiliser que si la branch en question n'éxiste déjà pas /!\

Si vous préférez jouer sur la sécurité et que utiliser la première commande il va falloir utiliser la commande **git checkout NomDeVotreBranch** pour switcher de branch.

## Feature branch

lorsque vous voulez collaborer sur git et créer une nouvelle feature dans votre app il va falloire alors crée un sous-branch qui découle de master

> Comment savoir sur quelle branch on est ?

```bash
    $ git branch
    * master
```

**\*sinon vous pouvez aussi aider votre team sur une feature il faudra alors dans sa sous-branch pour lui apporter de l'aide sur une feature complexe.
pour ne pas avoir de conflit dans une sous-branch vous devrez alors crée une branch qui découlera de la branch de votre collègue. /!\***

## Mettre à jour une sous branch

Pour pouvoir mettre à jour une sous-branch par rapport à votre master local ou distante ou par rapport à une simple branch distante il va falloire taper la commande

> **git rebase NomDeVotreBranch sur laquelle vous voulez rebaser votre sous-branch**

sinon si vous voulez rebaser une branch local par rapport à une branch distante il va falloire utiliser cette commande.

> **git rabse AliasIndiquantVotreRepoDistant(ex: origin)/NomDeVotreBranchDistante**
