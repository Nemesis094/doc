---
eleventyComputed:
  title: Running {{ en.RDM }} as another user
---
There are many different types of credentials and they are used by a multitude of users. On Windows systems, having multiple user accounts enables the ability to launch {{ en.RDM }} under a different set of credentials while we are already logged on using main credentials. This allows for using Integrated security to connect to an [Advanced Data Source](/rdm/windows/data-sources/data-sources-types/advanced-data-sources/).

{% snippet icon.badgeInfo %}
These solutions require the "Secondary Log-on" service to be running.
{% endsnippet %}

{% snippet icon.badgeInfo %}
If the other account belongs to a domain different than the one from your workstation, solution A must be used.
{% endsnippet %}

## Solution A - RunAs command

This solution is ideal if you do this often, you can create a batch file with the command and simply type in your password when prompted.

The RunAs command has many parameters to change its behaviour, we will not cover them all here, but if you have an advanced scenario we suggest you consult the Windows help.

1. Open a command prompt.
1. Type runas /netonly /user:{your username here}. Usage of the NetOnly parameter signals that the credentials will be used for network access only. Ensure your username is entered as your infrastructure requires. Typically its {domain}\{user}, i.e. windjammer\david
1. Append the full path to {{ en.RDM }}, typically **%ProgramFiles(x86)%\Devolutions\Remote Desktop Manager\RemoteDesktopManager.exe**, but you must ensure this is correct for your machine.
1. When you press enter, you are prompted for the password, then the application will launch.
![!!KB4584](https://cdnweb.devolutions.net/docs/docs_en_kb_KB4584.png)

## Solution B - Shift+right-click on the shortcut or executable to ## {{ en.RDM }}

When you press <kbd>Shift</kbd>+right-click on an executable, you will notice an additional menu item for Run as different user
![!!KB4585](https://cdnweb.devolutions.net/docs/docs_en_kb_KB4585.png)

You are presented with a logon form in which you must specify the username and password.
![!!KB4586](https://cdnweb.devolutions.net/docs/docs_en_kb_KB4586.png)
