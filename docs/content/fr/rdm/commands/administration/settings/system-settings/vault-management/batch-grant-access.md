---
eleventyComputed:
  title: Accorder l'accès en lot
  description: La fonctionnalité Accorder l'accès en lot permet de définir des permissions et ensembles de permissions à plusieurs utilisateurs, groupes d'utilisateurs et/ou utilisateurs d'application en même temps sur des entrées, dossiers ou {{ fr.VLT }}s.
---
La fonctionnalité ***Accorder l'accès en lot*** permet de définir des permissions et ensembles de permissions à plusieurs utilisateurs, groupes d'utilisateurs et/ou utilisateurs d'application en même temps sur des entrées, dossiers ou {{ fr.VLT }}s.

## Emplacement

***Accorder l'accès en lot*** se trouve dans les propriétés des entrées, dossiers et {{ fr.VLT }}s sous ***Sécurité – Permissions*** (ou sous ***Sécurité – Permissions héritées*** pour la racine du {{ fr.VLT }}). Définissez les permissions à ***Personnalisé***, puis cliquez sur ***Accorder l'accès***.

![Propriétés – Sécurité – Permissions](https://cdnweb.devolutions.net/docs/fr/rdm/windows/RDMWin2138.png)

On peut également y accéder par le menu ***Administration*** :
1. Dans {{ fr.RDM }}, aller dans ***Administration – Paramètres système – Gestion des {{ fr.VLT }}s***.
1. Sous ***Permissions par défaut***, sélectionner ***Personnalisé*** dans le menu déroulant ***Autorisation***.

   ![Permissions par défaut personnalisées](https://cdnweb.devolutions.net/docs/fr/rdm/windows/RDMWin2139.png)

1. Cliquer sur ***Accorder l'accès***.

   ![Accorder l'accès](https://cdnweb.devolutions.net/docs/fr/rdm/windows/RDMWin2140.png)

La fenêtre ***Accorder l'accès en lot*** est maintenant ouverte.

![Accorder l'accès en lot](https://cdnweb.devolutions.net/docs/fr/rdm/windows/RDMWin2141.png)

La fenêtre est divisée en deux sections : les <a href="#permissions">paramètres des permissions</a> et la <a href="#utilisateurs">sélection des utilisateurs</a>.

## Paramètres

### Permissions

Dans les paramètres des permissions, vous pouvez sélectionner les permissions à accorder. Vous pouvez afficher soit les ***Permissions*** ou les ***Ensembles de permissions*** créés précédemment (ou ceux créés par défaut).

{% snippet icon.badgeHelp %}
Les ensembles de permissions sont créés et configurés dans ***Administration – Paramètres du système – Gestion des {{ fr.VLT }}s – Ensembles de permissions***. Pour davantage d'information, voir [Ensembles de permissions](/fr/rdm/windows/commands/administration/settings/system-settings/vault-management/permission-sets).
{% endsnippet %}

![Paramètres de permissions](https://cdnweb.devolutions.net/docs/fr/rdm/windows/RDMWin2142.png)

### Utilisateurs

Les utilisateurs peuvent être sélectionnés un par un en cochant la case à côté de chacun d'eux, mais cette méthode peut s'avérer fastidieuse si vous avez beaucoup d'utilisateurs. Des outils sont disponibles pour vous aider dans votre processus de sélection :
* ***Filtre*** : Filtrer vos utilisateurs, groupes d'utilisateurs et utilisateurs d'applications par ***Nom*** ou ***Description***.
* ***Type*** : Afficher seulement les utilisateurs, les groupes d'utilisateurs ou les utilisateurs d'application.
* ***Sélectionné*** : Afficher seulement les utilisateurs, groupes d'utilisateurs et utilisateurs d'application sélectionnés ou non sélectionnés.

![Sélection des utilsiateurs](https://cdnweb.devolutions.net/docs/fr/rdm/windows/RDMWin2143.png)
