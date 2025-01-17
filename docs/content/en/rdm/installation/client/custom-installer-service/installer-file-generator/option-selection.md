---
eleventyComputed:
  title: Option selection
  description: When generating the installer file, you must decide what to include in the configuration.
---
When generating the installer file, you must decide what to include in the configuration. This process will replicate the configuration of the {{ en.RDM }} instance currently used and will generate an installer file (.rdi). Once it has been generated, the installer file can be used as many times as needed to create {{ en.CI }}s. For security reasons, some settings that may contain credentials such as ***Saved templates*** are disabled by default. Enable them based on your risk level.

{% snippet icon.shieldWarning %}
The same dialog is used for the {{ en.CIS }} and for exporting the {{ en.RDM }} configuration file. Some options must **not** be used for the {{ en.CIS }} to prevent sharing credentials that must stay confidential. Please read the documentation carefully.
{% endsnippet %}

{% snippet icon.badgeInfo %}
{{ en.RDM }} may install required add-ons automatically when it detects that they are needed (configured in ***File – Options – Paths***). If you need to customize the application's installation path of an add-on, you must first perform the modification, then create the installation package. This setting will be replicated in the installer file (*.rdi).
{% endsnippet %}

## Options

You can open the ***Installer File Generator*** from ***File – {{ en.DA }} – Installer File Generator***. It is also accessible when creating a installation package in ***File – {{ en.DA }} – {{ en.CIM }}***.
![Installer file generator](https://cdnweb.devolutions.net/docs/docs_en_rdm_windows_clip11249.png)

### Miscellaneous

{% snippet icon.shieldWarning %}
Do not redistribute the ***{{ en.DA }} credentials***. Doing so would share these to all users having access to the online account used to create the installer package.

All ***Local templates*** will be included. If any of these contain credentials, it may pose a security risk. Ensure that you only share what is needed.
{% endsnippet %}

![Miscellaneous options](https://cdnweb.devolutions.net/docs/docs_en_rdm_windows_clip11260.png)

| OPTION                                 | DESCRIPTION                                                                                               |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Proxy settings                         | Includes your Internet proxy settings. This option is enabled by default.                                 |
| Saved installation paths               | Preserves your installation paths configured for external third-party applications. Use this only when all of the user's machines use the same paths. This option is enabled by default. |
| Saved templates                        | Includes your local templates in the {{ en.CI }}. Database templates are stored in the data source and may be a better option if you need to share them. |
| {{ en.DA }} credentials                | Includes your {{ en.DA }} credentials used to create the {{ en.CI }}. Consult the security warning above. |
| Include data source credentials        | Includes the credentials for all selected data sources below. Consult the security warning above.         |
| Clear application lock information     | Clears the information from ***File – Options – Security – Lock – Lock application*** (local).            |
| Force always retrieve new registration | Allows the administrator to force the users to use this new configuration file.                           |

{% snippet icon.badgeInfo %}
Since version 2022.3 of {{ en.RDM }}, the license registration information is stored in the data source, which means it can no longer be included in a {{ en.CI }}. Follow this [step-by-step guide](/rdm/windows/installation/client/registration/team-edition/) to add your license serial and assign it to your users from an [advanced data source](/rdm/windows/data-sources/data-sources-types/advanced-data-sources/).

If your users each have their own individual data source ({{ en.DHUBP }}, SQLite), you need to provide them the license serial so they can manually register in ***Administration – Management – Licenses***.
{% endsnippet %}

### Data sources

Select the data sources that must be included in the configuration. In the ***Description*** column, you will see details about each data source.

{% snippet icon.shieldWarning %}
You should only share data sources that are either using Integrated Security or an environment variable for the username. Passwords for accessing a data source should never be shared.
{% endsnippet %}
