---
eleventyComputed:
  title: Running the {{ en.RDM }} synchronizer from a centralized server
---
To prevent your computer from being overloaded by background tasks, such as Synchronizer, perform these tasks on centralized servers.

{% snippet icon.badgeInfo %}
These instructions are for team data sources
{% endsnippet %}

## Step-by-step guide

1. Install a [portable version](/rdm/windows/installation/client/portable-usb/) of {{ en.RDM }}.
1. Add your configured advanced data source. We recommend ***Windows authentication*** for authentication type.
1. Delete the ***Local Data Source*** from the data source list.
1. Create a synchronizer entry. To test the entry, click ***Open Session***.
1. Go to ***Advanced*** in ***Synchronizer Properties*** and copy the ***Command Line*** We will paste it in step 12.
![!!KB4196](https://cdnweb.devolutions.net/docs/docs_en_kb_KB4196.png)
1. Open ***Windows Task Scheduler***.
1. Select ***Create Task***.
![!!KB4197](https://cdnweb.devolutions.net/docs/docs_en_kb_KB4197.png)
1. Enter a task name and select ***Run whether user is logged on or not***.
![!!KB4198](https://cdnweb.devolutions.net/docs/docs_en_kb_KB4198.png)
1. On ***Triggers*** tab, select ***New***.
![!!KB4199](https://cdnweb.devolutions.net/docs/docs_en_kb_KB4199.png)
1. Configure ***Settings*** as desired.
    1. Set the schedule for the trigger. In our example, we used Weekly, every Sunday, at 1:00:00 am.
    1. Check ***Stop task if it runs longer than*** and set value to 30 minutes.
    1. Check ***Enabled***, then click ***OK***.
      ![!!KB4200](https://cdnweb.devolutions.net/docs/docs_en_kb_KB4200.png)
1. On the ***Actions tab***, click ***New***.
![!!KB4201](https://cdnweb.devolutions.net/docs/docs_en_kb_KB4201.png)
1. Paste the Command line copied in step 5 into ***Program/script*** and click ***OK***.
![!!KB4202](https://cdnweb.devolutions.net/docs/docs_en_kb_KB4202.png)
1. On the pop-up, click ***Yes***.
![!!KB4203](https://cdnweb.devolutions.net/docs/docs_en_kb_KB4203.png)
1. Click ***OK***.
![!!KB4204](https://cdnweb.devolutions.net/docs/docs_en_kb_KB4204.png)

The task configuration is finished and will run automatically. You can monitor the status of the tasks in Windows Event Viewer.
