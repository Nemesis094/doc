---
eleventyComputed:
  title: Multi-factor authentication
---
{% snippet icon.badgeInfo %}
This feature is only available for [{{ en.DVLS }}](/rdm/mac/data-sources/data-sources-types/advanced-data-sources/server/), [Microsoft SQL Server](/rdm/mac/data-sources/data-sources-types/advanced-data-sources/microsoft-sql-server/configure-sql-server/), and [SQLite](/rdm/mac/data-sources/data-sources-types/sqlite/) data sources.
{% endsnippet %}

Multi-factor authentication (MFA) identifies users by at least two different components: something that the user knows (often a password) and something that the user possesses (e.g., a validation code sent to a mobile device). If one of the components is missing or supplied incorrectly, the user's identity is not established with sufficient certainty and access to the data source will remain blocked.

MFA is set at the data source level, except in {{ en.DVLS }}, where it is [set on the user](/server/web-interface/administration/configuration/server-settings/security/two-factor/). {{ en.RDMMAC }} supports [Authenticator (TOTP)](/rdm/mac/data-sources/multi-factor-authentication/authenticator-totp/), [Yubikey](/rdm/mac/data-sources/multi-factor-authentication/yubikey/), and [Duo](/rdm/mac/data-sources/multi-factor-authentication/duo/).

Go to the section that corresponds to your data source type:

* [SQL Server](#configure-multi-factor-authentication-on-a-microsoft-sql-server-data-source)
* [SQLite](#configure-multi-factor-authentication-on-a-sqlite-data-source)

### Configure Multi-Factor Authentication on a Microsoft SQL Server Data Source

1. In {{ en.RDMMAC }}, go to the data source for which you want to configure the MFA.
1. Go to ***File – My Account Settings – Data Source MFA***.
![File – My Account Settings – Data Source MFA](https://cdnweb.devolutions.net/docs/docs_en_rdm_mac_RDMMac2056.png)
1. In the ***Multi-Factor Configuration*** window, click ***Change***.
![Change Multi-Factor Configuration](https://cdnweb.devolutions.net/docs/docs_en_rdm_mac_clip10064.png)
1. Select your MFA ***Type*** in the drop-down list.
![Multi-Factor Authentication Type](https://cdnweb.devolutions.net/docs/docs_en_rdm_mac_clip10066.png)
1. Follow one of the links below depending on the choice made in the previous step:
    * [Authenticator (TOTP)](/rdm/mac/data-sources/multi-factor-authentication/authenticator-totp/)
    * [Yubikey](/rdm/mac/data-sources/multi-factor-authentication/yubikey/)
    * [Duo](/rdm/mac/data-sources/multi-factor-authentication/duo/)

### Configure Multi-Factor Authentication on a SQLite Data Source

1. In {{ en.RDMMAC }}, go to ***File – Data Sources***.
1. Select the SQLite data source in the left menu, then click on ***Edit data source*** button.
![Edit data source](https://cdnweb.devolutions.net/docs/docs_en_rdm_mac_RDMMac2057.png)
1. Next to the ***Multi-factor*** setting, click on ***None***.
![Multi-factor Option](https://cdnweb.devolutions.net/docs/docs_en_rdm_mac_clip10065.png)
1. In the ***Multi-Factor Configuration*** window, click ***Change***.
![Two Factor Configuration](https://cdnweb.devolutions.net/docs/docs_en_rdm_mac_clip10064.png)
1. Select your MFA ***Type*** in the drop-down list.
![Two Factor Configuration](https://cdnweb.devolutions.net/docs/docs_en_rdm_mac_clip10066.png)
1. Follow one of the links below depending on the choice made in the previous step:
    * [Authenticator (TOTP)](/rdm/mac/data-sources/multi-factor-authentication/authenticator-totp/)
    * [Yubikey](/rdm/mac/data-sources/multi-factor-authentication/yubikey/)
    * [Duo](/rdm/mac/data-sources/multi-factor-authentication/duo/)
