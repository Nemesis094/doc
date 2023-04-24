---
eleventyComputed:
  title: Installation avec un script
  description: Les instructions suivantes expliquent comment installer un {{ fr.DGW }} à l'aide d'un script via {{ fr.HUBB }}.
---
Les instructions suivantes expliquent comment installer un {{ fr.DGW }} à l'aide d'un script via {{ fr.HUBB }}.

## Étapes de l'installation avec un script

{% snippet icon.badgeInfo %} 
L'installation du script nécessite l'utilisation de PowerShell 7.
{% endsnippet %} 

1. Se connecter avec un compte administrateur {{ fr.HUBB }}. 
1. Accéder à l'onglet ***Administration*** sur la gauche.  
![Onglet Administration](/img/fr/hub/DGW0020.png)
{% snippet icon.badgeCaution %} 
Un ***Utilisateur d'application*** est nécessaire pour continuer. S'il n'a pas encore été créé, la page d'aide [Gestion des utilisateurs d'application](/fr/hub/web-interface/hub-overview/administration/management/application-users/manage-application-users/) est disponible. 
{% endsnippet %} 

3. L'***Utilisateur d'application*** devra avoir la permission de gérer le {{ fr.DGW }} pour que le script fonctionne. Cliquer sur ***Permissions du système***, qui se trouve sous la section ***Configuration et sécurité***.  
![Administration – Permissions du système](/img/fr/hub/DGW0022.png)
1. Sélectionner le bouton ***Modifier*** dans le coin supérieur droit.  
![Modifier](/img/fr/hub/DGW0023.png)
1. Dans l'onglet ***Système***, faites défiler vers le bas jusqu'à ***Gérer les passerelles***. Sélectionner l'***Utilisateur d'application*** ou le groupe d'utilisateurs souhaité.  
![Gérer les passerelles](/img/fr/hub/DGW0024.png)
1. Retourner à l'onglet ***Administration***. 
1. Cliquer sur {{ fr.DGW }}, qui se trouve sous la section ***Gestion***.  
![{{ fr.DGW }}](/img/fr/hub/DGW0021.png)
1. Cliquer sur le bouton ***Ajouter*** ( ***+*** ) en haut à droite.  
![Ajouter](/img/fr/hub/DGW0025.png)
1. Sélectionner ***Installer avec un script*** dans la liste déroulante.  
![Installer avec un script](/img/fr/hub/DGW0026.png)
1. Saisir les informations correctes. Si le champ ***Licence*** est laissé sur ***Aucun***, l'option ***Free*** sera utilisée par défaut.  
![Champs d'information](/img/fr/hub/DGW0027.png)
![Champs d'information](/img/fr/hub/DGW0028.png)
1. Cliquer sur ***Télécharger***.  
![Télécharger](/img/fr/hub/DGW0029.png)
1. Exécuter le script téléchargé avec PowerShell 7 en mode administrateur. (Il doit être installé sur le serveur hébergeant le site {{ fr.DGW }}.) 
1. Le script vous demandera ***Do you want to set a certification*** ? Saisir ***Y*** et appuyer sur ***Entrée***. 
1. Saisir le chemin d'accès au fichier du certificat. 
1. Saisir le mot de passe du certificat. (Si le mot de passe a été copié dans le presse-papiers, ne faites pas CTRL+V, un clique droit suffira.) 
1. Appuyer sur ***Entrée*** lorsque le ***Statut de la demande Web*** est terminé. 
1. Si l'installation est réussie, le message suivant s'affiche : ***Installation du {{ fr.DGW }} terminée!***. Appuyer sur ***Entrée***. 
1. Retourner à la page web {{ fr.DGW }} et cliquer sur ***Actualiser***.  
![Actualiser](/img/fr/hub/DGW0030.png)
1. La page {{ fr.DGW }} s'affiche avec un cercle rouge pour indiquer que la passerelle est hors ligne. Cliquer sur ***Modifier***.  
![Modifier](/img/fr/hub/DGW0031.png)
1. Descendre au bas de la page et cliquer sur ***Tester connexion***. Une boîte de message avec ***Connexion réussie*** devrait apparaître en haut à droite.  
![Tester connexion](/img/fr/hub/DGW0032.png)
1. Un rectangle affichera les informations pour chaque {{ fr.DGW }} Hub.  
![Connexion réussie](/img/fr/hub/DGW0033.png)

{% snippet icon.badgeInfo %} 
Visiter [Configuration dans {{ fr.RDM }}](/fr/hub/dgw/rdm-configuration/) pour en savoir plus sur la liaison entre {{ fr.RDM }} et {{ fr.DGW }}.
{% endsnippet %} 