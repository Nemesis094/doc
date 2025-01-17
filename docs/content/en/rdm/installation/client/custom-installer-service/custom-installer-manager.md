---
eleventyComputed:
  title: "{{ en.CIM }}"
  description: In {{ en.RDM }}, click on File – {{ en.DA }} – Sign-in to connect to your {{ en.DA }} if you are not already signed in.
---
{% snippet icon.badgeNotice %}
For stability reasons, the latest version of {{ en.RDM }} is made available with a small delay for custom installers to ensure that no major issues are present. We recommend using this time with your organization to perform integration tests on a few workstations before upgrading your entire team.
{% endsnippet %}

## Create an installation package

1. In {{ en.RDM }}, click on ***File – {{ en.DA }} – Sign-in*** to connect to your {{ en.DA }} if you are not already signed in.
![{{ en.DA }} sign-in](https://cdnweb.devolutions.net/docs/docs_en_rdm_windows_RDMWin2211.png)
1. Under ***Tools***, click on ***{{ en.CIM }}*** to create a new {{ en.CI }} with specific settings.
![File – {{ en.DA }} – {{ en.CIM }}](https://cdnweb.devolutions.net/docs/docs_en_rdm_windows_clip11247.png)
1. Click on ***New Package***.
![{{ en.CIM }} – New package](https://cdnweb.devolutions.net/docs/docs_en_rdm_windows_clip11251.png)
1. Select the application ***Version*** in the drop-down list. A ***Name*** for your package will be generated automatically, which you can change if you wish. You can also write a brief ***Description*** of your package, but this is optional.
![Installation package creation](https://cdnweb.devolutions.net/docs/docs_en_rdm_windows_clip11252.png)
1. If you do not have a {{ en.RDM }} Installer file (.rdi), leave the ***Create a configuration just for this package*** option enabled. If you have already created one, enable the ***Use existing Remote Desktop Installer (rdi) file*** option instead and select your file on your computer using the ellipsis button.
1. Click on ***Create***. Skip to step 9 if you selected ***Use existing Remote Desktop Installer (rdi) file*** in the previous step.
1. If you need to create a new configuration file, the ***Installer file generator*** window will open. See our [Option Selection](/rdm/windows/installation/client/custom-installer-service/installer-file-generator/option-selection/) guide for more information about the different options to choose from.
![Installer file generator](https://cdnweb.devolutions.net/docs/docs_en_rdm_windows_clip11249.png)
1. Click on ***Generate*** to create the file when you are done with your selection.
1. When prompted, save the installation package file locally on your computer.
