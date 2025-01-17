---
eleventyComputed:
  title: "{{ en.RDMJ }}"
  keywords:
  - Bastion server
  - Jump box
  - Jump server
  - Service host
---
{{ en.RDMJ }} connects to a remote host, often called a Jump Box, Service Host, or a Bastion Server, which in turn connects to other hosts. {{ en.RDMJ }} is actually an RDP in an RDP.

This can be compared to RD Gateway from Microsoft and to some extent SSH port forwarding.

The Jump is performed through {{ en.RDMA }}. The Agent needs to be **currently executing** in a Windows Session on the remote host, or set to automatically start upon login. We have decided NOT to have this available through a service at this time.

The {{ en.RDMJ }} feature does not allow you to circumvent the need to properly license your remote host to allow more than two RDP connection at a time. There is no other way except for installing remote desktop session host role on the server and purchasing RDS CAL (per user) for the remote connection. For more information please consult this Microsoft link: [Activate the Remote Desktop Services license server](https://learn.microsoft.com/en-us/windows-server/remote/remote-desktop-services/rds-activate-license-server).

{{ en.RDM }} must be installed on the Jump Host for the agent to be able to run commands. The application does not have to connect to any data source, as {{ en.RDM }} only serves as a shell for the agent to run commands.

{% youtube 'AfpCDZGphA8' %}

Both instances of {{ en.RDMJ }} or {{ en.RDM }} and {{ en.RDMA }} running on the ***Jump Host*** communicate through an RDP channel. Commands are sent securely over the RDP channel and are then executed on the Service Host. Commands include running a script or opening a remote session of any type. It can even launch a VPN client on the Service Host prior to running the remote session.
* [Usage Scenarios](#usage-scenarios)
* [Configure a Jump Host](#configure-a-jump-host)
* [Configure a session to use the Jump Host](#configure-a-session-to-use-the-jump-host)
* [Validate that the Jump Host works](#validate-that-the-jump-host-works)
* [Pro Tips](#pro-tips)

## Usage scenarios

### Accessing a secure network through a single host

This allows you to have a strict firewall policy that allows connections only from a specific IP address. This configuration only grants you access to hosts that are accessible from the Jump Box. Imagine you have the following infrastructure:
![!!clip10825](https://cdnweb.devolutions.net/docs/docs_en_rdm_windows_clip10825.png)

You need to access the remote hosts, but you want to limit risks and expose only the Jump Host to the internet traffic. This allows you to create strict firewall rules and to open only a single port. Therefore, it forces you to connect to the Jump Host before hopping to a remote host.
![!!clip10826](https://cdnweb.devolutions.net/docs/docs_en_rdm_windows_clip10826.png)

{{ en.RDMJ }} helps achieve that goal simply and efficiently.

### Workaround limitations of some VPN clients

These limitations make it impossible to use multiple VPN clients concurrently on the same workstation. In this case, you can have multiple virtual machines, each running a single VPN client. Using these virtual machines as jump boxes allows you to connect to the virtual machine, launch the VPN client, then launch the remote session.
![!!clip10820](https://cdnweb.devolutions.net/docs/docs_en_rdm_windows_clip10820.png)

## Configure a Jump Host

1. Create an ***RDP*** entry for the ***Jump Host***.
1. Fill the entry with a ***Name***, ***Host*** and the ***Credentials***.
   {% snippet icon.badgeCaution %}
   For ***Jumps*** to work, you need to supply the credentials via the ***Jump Host*** session. If the RDP sessions prompt you for the credentials after the start, the ***Jump*** will fail.
   {% endsnippet %}

   ![Create an RDP entry for the Jump Host](https://cdnweb.devolutions.net/docs/docs_en_rdm_windows_RDMWin6193.png)

1. In the ***Jump Host*** section, check ***Is Jump host***.
![Check Is Jump host](https://cdnweb.devolutions.net/docs/docs_en_rdm_windows_RDMWin6195.png)
1. Click ***OK***.
1. Launch the ***Jump Host*** session.
1. Install {{ en.RDM }} on the ***Jump Host***.
   {% snippet icon.badgeNotice %}
   The ***Jump Host*** acts as a relay between the local and the remote systems, allowing to use the {{ en.RDM }} license that has been used on the local workstation to register the application on the ***Jump Host***.

   Install {{ en.RDM }} on the ***Jump Host***, perform your first jump and {{ en.RDM }} will be unlocked/licensed automatically via the jump communication/handshake.

   There is no need to create a data source on the ***Jump Host***. {{ en.RDM }} will open for the first time with a default ***SQLite Local Data Source***. This is sufficient because the application on the ***Jump Host*** only acts as an intermediate between the local and the remote hosts.
   {% endsnippet %}

1. Confirm {{ en.RDMA }} is started and set to ***Auto Start***.

   {% snippet icon.badgeCaution %}
   ***Auto Start*** must only be activated for the {{ en.RDMA }} or {{ en.RDM }} but not for both. In the case where {{ en.RDM }} is set to ***Auto Start*** please make sure to delete the shortcuts form either/both the following locations:

   * Run: shell:startup
   * Run: shell:common startup
   {% endsnippet %}

    1. Go to ***Tools - More Tools***.
{type="a"}
    1. Select {{ en.RDMA }}.
    1. Click ***OK***.
    1. Click ***Yes***.
![!!RdmWin4058](https://cdnweb.devolutions.net/docs/docs_en_rdm_windows_RDMWin6196.png)

1. Right-click the {{ en.RDMA }} icon in the taskbar.
    1. Check ***Auto Start***.
{type="a"}
1. Adjust the user interface of the ***Jump Host*** to maximize the area to display remote sessions.
    * Make the application full screen.
    * Hide the ***{{ en.NPANE }}*** in the ***View*** tab.
    * Hide the ***Ribbon*** in the ***View*** tab.
        * To show the ***Ribbon*** again, click the {{ en.RDM }} icon at the top left corner.
   {% snippet icon.badgeNotice %}
   To reset the layout, in the ***Window*** tab, click ***Reset Layout***.
   {% endsnippet %}

The ***Jump Host*** is ready to use.

## Configure a session to use the Jump Host

1. Create an ***RDP*** entry, on the local {{ en.RDM }} instance.
1. Set the ***Jump Host*** by clicking on the ***RDM Jump settings*** button.
    * The ***Jump Host*** can be ***Inherited*** if it is defined in the parent folder.
or
    * Choose a specific ***Session*** to point directly to the ***Jump Host*** entry.
![!!RDMWin2235](https://cdnweb.devolutions.net/docs/docs_en_rdm_windows_RDMWin2235.png)
1. Click ***OK*** twice.
1. Launch the RDP session. The {{ en.RDMJ }} opens automatically and it looks like a session in a session.

## Validate that the Jump Host works

1. Start the ***RDP*** session of the ***Jump Host Server***.
1. Wait for {{ en.RDMA }} to connect.
1. On the ***RDP*** tab, right click ***Agent Status***. {{ en.RDMA }} should be connected.
1. Keep the ***RDP*** tab open.
1. Start the ***Jump*** session. ***Jump*** session should start on the ***Jump Host Server***.
1. Close all sessions.
1. Start the ***Jump*** session directly. ***Jump Host Server*** and ***Jump*** session should both start.

All should be working correctly. If any of the steps fails, it is where you need to investigate.

## Pro tips

* To gain more space for the dashboard, in the ***View*** tab, hide the ***Ribbon*** and ***{{ en.NPANE }}*** since the menus are not needed.
* Use the same {{ en.RDM }} license on the local and the remote instances. The Jump Host acts as a relay between the local and the remote systems, allowing to use the {{ en.RDM }} license that has been used on the local workstation to register the application on the Jump Host.
* There is no need to create a data source on the Jump Host. {{ en.RDM }} will open for the first time with a default ***SQLite Local Data Source***. This is sufficient because the application on the Jump Host only acts as an intermediate between the local and the remote hosts.
