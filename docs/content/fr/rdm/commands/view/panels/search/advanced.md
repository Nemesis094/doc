---
eleventyComputed:
  title: Recherche avancée
---
La fonction de ***Recherche avancée*** vous permet de rechercher des entrées et des dossiers en fonction de plusieurs critères dans un {{ fr.VLT }} à la fois. Pour effectuer des recherches dans plusieurs {{ fr.VLT }}s simultanément, veuillez vous référer à [***Recherche multi-{{ fr.VLT }}s***](/fr/rdm/windows/commands/view/panels/search/multi-vault/).  
![Fenêtre de recherche avancée](https://webdevolutions.azureedge.net/docs/fr/rdm/windows/clip10250.png) 

Il est possible de sélectionner plusieurs entrées à la fois avec <kbd>Maj</kbd>+clic ou toutes les entrées avec le raccourci <kbd>Ctrl</kbd>+<kbd>A</kbd>. Un clic droit sur une ou plusieurs entrées affiche le même menu et les mêmes options que le ***{{ fr.NPANE }}***. 

### Onglet Recherche 

<table>
	<tr>
		<th>

OPTION 
		</th>
		<th>
DESCRIPTION 
		</th>
	</tr>
	<tr>
		<td>
Critère 
		</td>
		<td>
Vous pouvez choisir entre plusieurs différents critères pour affiner votre recherche :  

* Référence au contact 
* Date de création 
* Champs personnalisé 
* Description 
* Domaine 
* Dossier 
* Hôte 
* Favoris 
* Étiquettes 
* Date de la dernière mise à jour 
* Nom 
* OS 
* Force du mot de passe 
* Groupe de sécurité (ancien système)* 
* Numéro de série 
* Rôle du serveur 
* Statut 
* Nom d'utilisateur 
* URL 
* Version 
* IP 
* MAC 
* Logiciel 

*La sécurité ancienne et les groupes de sécurité ont été dépréciés et seront complètement supprimés à partir de la version 2023.3 de {{ fr.RDM }}. Voir [Migration des groupes de sécurité (ancien) vers les groupes d'utilisateurs](/fr/kb/remote-desktop-manager/how-to-articles/migration-security-groups-user-groups/).
		</td>
	</tr>
	<tr>
		<td>
Charger 
		</td>
		<td>
Charger les recherches précédemment enregistrées. 
		</td>
	</tr>
	<tr>
		<td>
Enregistrer 
		</td>
		<td>
Enregistrer votre recherche localement pour la réutiliser. 
		</td>
	</tr>
	<tr>
		<td>
Enregistrer en tant que 
		</td>
		<td>
Enregistrer une recherche précédemment enregistrée, mais sous un autre nom. 
		</td>
	</tr>
	<tr>
		<td>
Exporter 
		</td>
		<td>
Exporter les entrées de votre résultat de recherche sous forme de fichier CSV, HTML, XLS ou XML. Les informations sensibles seront cryptées à l'aide d'AES. 
		</td>
	</tr>
	<tr>
		<td>
Recherche 
		</td>
		<td>
Une fois que vous avez sélectionné vos critères de recherche, cliquer sur ***Recherche*** pour afficher les résultats de la recherche. 
		</td>
	</tr>
	<tr>
		<td>
Réinitialiser 
		</td>
		<td>
Réinitialiser tous vos champs pour procéder à une nouvelle recherche. 
		</td>
	</tr>
	<tr>
		<td>
Sélectionner dans le ***{{ fr.NPANE }}*** 
		</td>
		<td>
Sélectionner votre résultat de recherche dans votre ***{{ fr.NPANE }}***. Cette option peut être utilisée en combinaison avec une modification par lot. 
		</td>
	</tr>
</table>

Il y aura une liste déroulante à côté de certains champs des critères (ex : Nom) pour vous donner des options de recherche supplémentaires :  

* ***Contient*** - tout nom qui comprend les caractères que vous avez saisis, n'importe où dans le nom du champ. 
* ***Commençant par*** - tout nom commençant par les caractères que vous avez saisis. 
* ***Finissant par*** - tout nom se terminant par les caractères que vous avez saisis. 
* ***Expression exacte*** - trouvera des noms qui correspondent à chaque caractère que vous avez entré, exactement comme il a été entré. 
* ***Ne contient pas*** - tout nom qui ne contient pas les caractères que vous avez saisis. 
* ***Expression régulière*** (regex) - toute chaîne de caractères spécifiant, selon une syntaxe précise, un ensemble de chaînes de caractères possibles. 