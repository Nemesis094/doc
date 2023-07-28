---
eleventyComputed:
  title: Documentation
  description: The Documentation feature allows for storing information about resources in the data source.
---
The ***Documentation*** feature allows for storing information about resources in the data source. To access an entry's documentation, select an entry in the [{{ en.NPANE }}](/rdm/windows/user-interface/navigation-pane/) , then select the ***Documentation*** tab in the ***Dashboard***. Alternatively, right-click an entry in the ***{{ en.NPANE }}***, then select ***View – Documentation***.  

The documentation is written using ***Markdown***, a plain text formatting syntax. ***Plain text*** and ***HTML*** are also available.

{% snippet icon.badgeInfo %} 
This feature is also available with {{ en.DVLS }}, Hub Business, Hub Personal and SQL Server data sources.  
{% endsnippet %}
 
{% snippet icon.badgeInfo %} 
The ***Documentation*** feature is encrypted only for {{ en.DVLS }}, Hub Business and Hub Personal data sources. If you are using data sources like SQL Server or Azure SQL, the ***Documentation*** feature is not encrypted. 
{% endsnippet %}
 
{% snippet icon.badgeCaution %} 
The feature for using ***Documentation*** in offline mode is available for documents that are stored in the database.  This property is set to be inherited by default.
{% endsnippet %}

## Create a new page  
 1. Choose the entry in the ***Navigation Pane***.  
 1. Go to the ***Documentation*** tab and click ***New page***.  
  ![Documentation tab – New page](https://webdevolutions.blob.core.windows.net/docs/en/rdm/mac/RDMMac6018.png)  
 1. Enter a name and select ***Documentation type***.  
  ![Documentation type](https://webdevolutions.blob.core.windows.net/docs/en/rdm/mac/RDMMac6023.png)  
 1. Choose a ***Default template***.
  ![Default template](https://webdevolutions.blob.core.windows.net/docs/en/rdm/mac/RDMMac6024.png)  

***Tutorial*** creates a document containing generated text and ***Empty*** a blank document. The last option, ***Custom***, lets you select a custom template of your choice. 

You can select ***Set as new default*** to save your preferences when you create a new document and ***Add as last page*** to insert the new page at the bottom of the file list.

 5. Click ***OK*** to close the window.

##  Synchronize offline documentation  
 1. Choose the entry in the ***Navigation Pane***.  
 1. Go to ***Administration – Vault Settings*** in the ribbon. 
 ![Vault Settings](https://webdevolutions.blob.core.windows.net/docs/en/rdm/mac/RDMMac6025.png)  
 1. In ***Security Settings – Offline – Synchronize documentation to offline***, select ***Yes***.  
 ![Synchronize documentation to offline](https://webdevolutions.blob.core.windows.net/docs/en/rdm/mac/RDMMac6019.png)  
 1. Click ***Save*** and close the window.  
 ![Documentation tab](https://webdevolutions.blob.core.windows.net/docs/en/rdm/mac/RDMMac6026.png)  
 The offline ***Documentation*** tab is now available in the ***Dashboard***.   

