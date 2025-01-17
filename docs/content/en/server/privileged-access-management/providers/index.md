---
eleventyComputed:
  title: Providers
  description: Providers are required to scan the Active Directory structure, your local network for SSH discovering, SQL accounts, Windows local accounts, or Azure AD users and groups.
  order: 20
---
Providers are required to scan the Active Directory structure, your local network for SSH discovering, SQL accounts, Windows local accounts, or Azure AD users and groups.

{% youtube 'drRLA7U8YsQ?si=ihVhTcJOKxAh5kKS&amp;start=57' %}

![Providers dashboard](https://cdnweb.devolutions.net/docs/docs_en_server_ServerOp8140.png)

Here are the available provider types:

* ***Managed*** providers:
    * [Domain user](/server/privileged-access-management/providers/domain-provider/)
    * [Local user](/server/privileged-access-management/providers/local-ssh-provider/)
    * [SQL user](/server/privileged-access-management/providers/sql-server-provider/)
    * [Windows user](/server/privileged-access-management/providers/windows-users-provider/)
    * [Azure AD user](/server/privileged-access-management/providers/azure-ad-user-provider/)

![Managed providers](https://cdnweb.devolutions.net/docs/docs_en_server_ServerOp2107.png)

* ***Unmanaged*** providers:
    * MySQL user
    * Cisco user
    * Oracle user

![Unmanaged providers](https://cdnweb.devolutions.net/docs/docs_en_server_ServerOp2108.png)

* ***AnyIdentity*** providers:
    * Windows accounts
    * Windows local accounts

![AnyIdentity providers](https://cdnweb.devolutions.net/docs/docs_en_server_ServerOp2109.png)

Multiple providers can be created and can reach different domains as long as the {{ en.DVLS }} instance can communicate with the domain controller.
