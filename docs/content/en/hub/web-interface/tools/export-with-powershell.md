---
eleventyComputed:
  title: Export with PowerShell
---
{% snippet icon.badgeInfo %} 
Exporting and importing data from and to {{ en.DHUBP }} is done differently than in {{ en.DHUBB }}. Refer to [Import/Export data with {{ en.DHUBP }}](/kb/hub-business/how-to-articles/import-export-data-hub-personal/) if you are using {{ en.DHUBP }}. 
{% endsnippet %}
 
In the {{ en.DHUBB }} ***Tools*** tab, you can find under the ***Export*** section the ***Export with PowerShell*** feature. It allows you to export your {{ en.DHUBB }} data in the Json or Csv format using a PowerShell script.  
![Export with PowerShell](https://webdevolutions.azureedge.net/docs/en/hub/Hub2077.png) 

You will first need to create an application user with the ***Manager*** role.  

Once done, you have the choice to automatically or manually fill in your information in the PowerShell script. Whichever option you choose, you will need access to your ***Application Secret*** and your ***Application key*** and to know the ***Destination folder path***.  
![Steps to Export with PowerShell](https://webdevolutions.azureedge.net/docs/en/hub/Hub2078.png) 

{% snippet icon.badgeInfo %} 
Visit our step-by-step guide on how to [Export data from {{ en.DHUBB }} with PowerShell](/kb/hub-business/how-to-articles/export-data-hub-business-powershell/). 
{% endsnippet %}