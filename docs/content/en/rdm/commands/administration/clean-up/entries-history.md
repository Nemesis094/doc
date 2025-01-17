---
eleventyComputed:
  title: Clean up entry history
  status: Topic available in German language
---
The ***Entry History*** deletes the history attached to your entry, you can find the history by right clicking on your entry and selecting ***View – Entry History***.

{% snippet icon.badgeInfo %}
This feature requires an [advanced data source](/rdm/windows/data-sources/data-sources-types/advanced-data-sources/).
{% endsnippet %}

{% snippet icon.badgeInfo %}
You must be an administrator of the data source to perform this action.
{% endsnippet %}

## Settings
1. Go to the ***Administration*** tab in the ribbon.
1. Click on ***Clean Up*** and then ***Clean Up Entry History***.
1. Select prior to which date the ***Entry History*** will be deleted.
1. Select from which {{ en.VLT }} the ***Entry History*** will be deleted.
1. Click ***OK***.
![Clean up deleted history](https://cdnweb.devolutions.net/docs/docs_en_rdm_windows_RDMWin0005.png)
   {% snippet icon.badgeWarning %}
   There will be no backup of the ***Entry History***. We strongly recommend to do a [backup](/rdm/windows/commands/file/backup/) before proceeding.
   {% endsnippet %}

1. Click on ***Proceed anyway***.
![Confirmation](https://cdnweb.devolutions.net/docs/docs_en_rdm_windows_RDMWin0004.png)

1. Click ***OK*** to close the dialog window.
