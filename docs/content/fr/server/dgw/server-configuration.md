---
eleventyComputed:
  title: Configuration du {{ fr.DGW }} avec {{ fr.DVLS }}
  order: 30
  description: Ce sujet décrit comment configurer {{ fr.DVLS }}, gratuit ou non, pour se connecter avec {{ fr.DGW }}.
  keywords:
  - VPN
  - Listener
---
Ce sujet décrit comment configurer {{ fr.DVLS }} pour se connecter avec {{ fr.DGW }}. Il y a deux façons d'installer un {{ fr.DGW }} : <a href="#installation-cote-a-cote">l'***installation côte à côte***</a> et <a href="#installation-autonome">l'***installation autonome***</a>.
{% snippet icon.badgeInfo %}
Plusieurs passerelles peuvent être utilisées par {{ fr.DVLS }}, mais seulement un {{ fr.DGW }} peut être installé sur une machine.
{% endsnippet %}

## Différences entre l'installation côte à côte et autonome
L'installation ***côté à côte*** sera utilisée si vous devez installer {{ fr.DGW }} sur la même machine que celle où {{ fr.DVLS }} est hébergé. Il s'agit d'un processus d'installation simplifié qui configurera automatiquement le nouveau {{ fr.DGW }} avec les informations de l'instance {{ fr.DVLS }} (URI d'accès et clé publique).

Pour installer {{ fr.DGW }} sur une autre machine que celle où {{ fr.DVLS }} est hébergé, vous devez suivre le processus d'installation ***autonome***. La procédure est similaire, mais vous devrez fournir plus d'informations sur votre instance {{ fr.DVLS }} pour la compléter.

## Installation côte à côte
{% snippet icon.badgeInfo %}
Pour mettre en place un {{ fr.DGW }} gratuit, il faut le configurer en utilisant ***l'installation côte à côte***. Cela crée une passerelle capable de gérer jusqu'à 5 sessions simultanées.
{% endsnippet %}

Cette méthode permet également de gérer davantage de sessions si une ou plusieurs licences {{ fr.DGW }} sont disponibles. Cette procédure d'installation est la plus simple des deux. Cependant, cette méthode est recommandée pour les mises en page de réseau plus simples.
1. Depuis la {{ fr.DVLSCONSOLE }}, cliquer sur l'onglet ***Compagnons***.
![Onglet Compagnons](https://cdnweb.devolutions.net/docs/fr/server/ServerOp2053.png)
1. Dans la section {{ fr.DGW }}, cliquer sur ***Installer***.
1. Choisir ***Installation côte à côte***.
![Installation côte à côte](https://cdnweb.devolutions.net/docs/fr/server/ServerOp0004.png)
   {% snippet icon.badgeHelp %}
   Il est possible de télécharger un fichier [.msi](https://devolutions.net/fr/gateway/download) pour installer {{ fr.DGW }} sur un {{ fr.DVLS }} hors ligne.
   {% endsnippet %}

1. Si les valeurs par défaut ne fonctionnent pas pour votre environnement, saisir les paramètres souhaités.
    1. ***Port d'écoute HTTP*** : Port HTTP(s) pour accéder à la passerelle. (7171 par défaut)
    1. ***Port d'écoute TCP*** : Port utilisé pour les sessions RDP. (8181 par défaut)
1. Cliquer sur ***OK***.
![Bouton OK](https://cdnweb.devolutions.net/docs/fr/server/ServerOp0005.png)
1. Accéder à l'interface Web {{ fr.DVLS }}, se connecter avec un compte administrateur.
1. Aller dans ***Administration*** – ***{{ fr.DGW }}***.
![{{ fr.DGW }}](https://cdnweb.devolutions.net/docs/fr/server/ServerOp0006.png)
1. Cliquer sur le bouton ***Ping*** pour tester la passerelle souhaitée dans la liste et voir si une connexion peut être établie avec succès. Si la page était déjà ouverte, il faut d'abord la rafraîchir.
![Ping](https://cdnweb.devolutions.net/docs/fr/server/ServerOp0007.png)

## Installation autonome
L'installation en utilisant la méthode ***autonome*** permettra d'installer {{ fr.DGW }} sur un serveur distinct de {{ fr.DVLS }}. Cela peut être pour des raisons de performance ou pour accéder à des réseaux auxquels {{ fr.DVLS }} ne peut pas accéder.
{% snippet icon.badgeInfo %}
La {{ fr.DVLSCONSOLE }} doit être installée sur le serveur sur lequel {{ fr.DGW }} sera installé.
{% endsnippet %}

1. Dans la {{ fr.DVLSCONSOLE }}, cliquer sur l'onglet ***Compagnons***.
![Onglet Compagnons](https://cdnweb.devolutions.net/docs/fr/server/ServerOp0017.png)
1. Dans la section {{ fr.DGW }}, cliquer sur ***Installer***.
1. Choisir ***Installation autonome***.
![Installation autonome](https://cdnweb.devolutions.net/docs/fr/server/ServerOp0008.png)
1. Choisir entre ***Télécharger la version*** et ***Installation à partir d'un fichier msi***.
   {% snippet icon.badgeHelp %}
   Il est possible de télécharger un fichier [.msi](https://devolutions.net/fr/gateway/download) pour installer {{ fr.DGW }} sur un {{ fr.DVLS }} hors ligne.
   {% endsnippet %}

1. Cliquer sur ***Suivant***.
![Bouton Suivant](https://cdnweb.devolutions.net/docs/fr/server/ServerOp0009.png)
1. Saisir le champ d'information ***URI d'accès***, par exemple https://gateway.exemple.com.
![Écouteurs](https://cdnweb.devolutions.net/docs/fr/server/ServerOp0018.png)
1. Choisir les ports ***Écouteurs*** pour {{ fr.DGW }} (par défaut ils sont 7171 et 8181).
    1. Si HTTPS est choisi au lieu de HTTP dans l'étape ci-dessus, la ***Configuration du certificat*** sera nécessaire.
    1. ***Fichier du certificat***: Il doit s'agir d'un certificat de chaîne complète (.pfx, .p12, .pem, .crt).
    1. ***Mot de passe du certificat***: Nécessaire uniquement si un certificat .pfx ou .p12 a été utilisé.
    1. ***Fichier de la clé privée***: Nécessaire uniquement si un certificat .pem ou .crt a été utilisé.
   {% snippet icon.shieldWarning %}
   Ne partager pas la clé privée avec d'autres utilisateurs, car elle peut être utilisée pour décrypter la communication entre un utilisateur et un {{ fr.DGW }}. Seule la clé publique doit être partagée.
   {% endsnippet %}

1. Cliquer sur ***Suivant***.
1. Choisir entre :
    * ***Utiliser la clé publique de l'instance {{ fr.DVLS }} '{{ fr.DVLS }}'*** : cette option est utilisée si {{ fr.DGW }} installé est sur le même serveur que le {{ fr.DVLS }};
    * ***À partir du fichier*** : Si l'installation de {{ fr.DGW }} se fait sur un autre ordinateur, télécharger la clé publique du {{ fr.DVLS }} que qui doit être couplé avec ce {{ fr.DGW }}.
![Télécharger la clé publique](https://cdnweb.devolutions.net/docs/fr/server/ServerOp0011.png)
1. Cliquer sur ***Suivant***.
![Suivant](https://cdnweb.devolutions.net/docs/fr/server/ServerOp0012.png)
1. Cliquer sur ***Installer***.
![Installer](https://cdnweb.devolutions.net/docs/fr/server/ServerOp0013.png)
1. Cliquer sur ***Close***.
![Bouton Close](https://cdnweb.devolutions.net/docs/fr/server/ServerOp0014.png)
1. Sur l'interface Web {{ fr.DVLS }}, connectez-vous avec un compte administrateur.
1. Accéder à ***Administration - {{ fr.DGW }}***.
![{{ fr.DGW }}](https://cdnweb.devolutions.net/docs/fr/server/ServerOp0006.png)
1. Cliquer sur le bouton ***Ajouter*** dans le coin supérieur droit.
![Bouton Ajouter](https://cdnweb.devolutions.net/docs/fr/server/ServerOp0015.png)
1. Saisir les informations suivantes.
    1. ***Nom***: Nom du {{ fr.DGW }} qui sera affiché dans {{ fr.RDM }}.
    1. ***Description***: Description de la passerelle.
    1. ***Définir par défaut***: Si l'option est cochée, cette passerelle sera sélectionnée par défaut lors de la configuration de {{ fr.RDM }}.
    1. ***URL de {{ fr.DGW }}***: L'URL {{ fr.DVLS }} à laquelle la passerelle se connectera.
    1. ***Port d'écoute TCP***: Définir le port avec la même valeur de port TCP que celui configuré dans la {{ fr.DVLSCONSOLE }}.
1. Cliquer sur ***Enregistrer***.
![Bouton Enregistrer](https://cdnweb.devolutions.net/docs/fr/server/ServerOp0016.png)

La passerelle devrait maintenant être visible dans la liste. Il est possible de vérifier l'état de la passerelle à l'aide du bouton ***Ping***.
![Ping](https://cdnweb.devolutions.net/docs/fr/server/ServerOp0007.png)
