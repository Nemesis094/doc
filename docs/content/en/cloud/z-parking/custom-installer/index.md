---
eleventyComputed:
  title: "{{ en.CI }}"
  description: The {{ en.CI }} replicates the settings from the Remote Desktop Manager instance used to create the package and stores them in the package for distribution.
---
{% snippet icon.badgeInfo %}
***{{ en.CI }}*** will be removed from {{ en.DPORTAL }}. You can still [access the URL](https://docs.devolutions.net/kb/general-knowledge-base/rdm-online-services-removed-devolutions-portal/) if needed
{% endsnippet %}

The ***{{ en.CIM }}*** will allow you to generate and download custom installation packages for {{ en.RDMWIN }}.

{% snippet icon.shieldWarning %}
The ***{{ en.CIM }}*** uploads a configuration file to our online services. You should not use the service to redistribute passwords for data sources.
{% endsnippet %}

{% snippet icon.badgeNotice %}
For stability reasons, in large installation bases, the latest official release is not available to the {{ en.CIS }} until an undetermined period while we ensure that no major issues are present. We recommend using this time with your organization to perform integration tests on a few workstations before upgrading your entire team.
{% endsnippet %}

## Settings

{% snippet icon.badgeInfo %}
The ***No Internet connection*** option in {{ en.RDM }} (***File*** – ***Option*** – ***Tools*** – ***Advanced***) must be disabled for {{ en.CI }} to work.
{% endsnippet %}

The ***{{ en.CI }}*** replicates the settings from the {{ en.RDM }} instance used to create the package and stores them in the package for distribution. You have control over which categories of settings you are redistributing, but not discrete settings. It may be desirable to have a {{ en.RDM }} installation that is used specifically to create the Installation Package.

You can go to ***File – {{ en.DA }} – Tools*** to access the ***{{ en.CIM }}***.
![File – {{ en.DA }} – {{ en.CIM }}](https://cdnweb.devolutions.net/docs/docs_en_cloud_clip0009.png)

Please consult our [{{ en.CI }} package creation guide](/rdm/windows/installation/client/custom-installer-service/).

If the package has already been generated, you can download it directly from the portal as described in [Download {{ en.CI }} Package](/cloud/rdm-online-services/custom-installer/download-custom-installer/).
