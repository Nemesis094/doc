---
eleventyComputed:
  title: Retrieve credentials with the {{ en.WBEX }}
---
{% snippet icon.badgeInfo %}
You need website entries in {{ en.DVLS }} to be able to retrieve their credentials. If that is not the case, start by [adding a website entry with the {{ en.WBEX }}](/server/workspace-browser-extension/using-workspace-browser-extension/add-website-entry-workspace-browser-extension/).
{% endsnippet %}

The {{ en.WBEX }} facilitates access to your credentials by automatically matching websites to saved credentials in {{ en.DVLS }} website entries. It is also possible to filter through your entries via the {{ en.WBEX }} to manually find your credentials.

After the [installation](/server/workspace-browser-extension/installation/) of the {{ en.WBEX }} and its [pairing](/server/workspace-browser-extension/first-login-workspace-browser-extension/) with {{ en.DVLS }}, you can immediately use the extension to retrieve your credentials. However, you may want to modify some of the settings to customize your experience. We recommend that you follow the steps in the [Settings](#settings) section first: they will guide you through setting up the {{ en.WBEX }} by suggesting best practices for retrieving credentials. You can also skip the configuration and go straight to [Retrieving credentials](#retrieving-credentials).

## Settings
1. Click on the {{ en.WBEX }} icon in your toolbar of your browser, then click on the ***Settings*** icon.
![Settings Icon](https://cdnweb.devolutions.net/docs/docs_en_server_ServerOp2015.png)
1. Click on ***General*** in the ***Configuration*** section.
![Settings – Configuration – General](https://cdnweb.devolutions.net/docs/docs_en_server_ServerOp2016.png)
1. In the ***General*** tab, the ***Show icon in fields*** setting should be enabled by default. If not, check the box next to the option to enable it.
   {% snippet icon.badgeNotice %}
   With this option enabled, a {{ en.WBEX }} icon is displayed in every credential fields on the websites you visit. This makes it easier to select the correct entry from which to retrieve your credentials, especially when more than one is available.
   {% endsnippet %}

   ![General – Show icon in fields](https://cdnweb.devolutions.net/docs/docs_en_server_ServerOp2017.png)

4. Click ***Save***.
5. Click on ***{{ en.DVLS }}*** in the ***Data sources*** section.
![Settings – Data sources – {{ en.DVLS }}](https://cdnweb.devolutions.net/docs/docs_en_server_ServerOp2018.png)
1. In the ***Actions*** tab, enable the ***Automatically retrieve credentials on page load*** and ***Automatically fill in credentials on load*** options by checking the boxes next to them. Below is a description of each setting:
    * ***Automatically retrieve credentials on page load*** (enabled by default): Allows the {{ en.WBEX }} to automatically search for available credentials when loading a web page.
    * ***Automatically fill in credentials on load*** (disabled by default): Credentials fields are automatically filled in when loading a web page. This only works if you only have one set of credentials for a given website.
![Actions – Automatically retrieve and fill in credentials on load](https://cdnweb.devolutions.net/docs/docs_en_server_ServerOp2019.png)
   {% snippet icon.badgeInfo %}
   If the ***Automatically submit the form after filling*** setting is enabled, the credentials are automatically submitted when the fields are filled. Enabling it is optional as it is not a best practice.
   {% endsnippet %}
7. Click ***Save***.

You can now continue to the next section to learn how to retrieve your website entry credentials.

## Retrieving Credentials
{% snippet icon.badgeInfo %}
This section is based on the {{ en.WBEX }} configuration steps from the [previous section](#settings). We highly recommend that you follow them before going forward, as some features may differ between your experience and what is shown below.
{% endsnippet %}

Credentials can be retrieved from {{ en.DVLS }} automatically or manually via the {{ en.WBEX }}. Follow the steps from the section that best suits your needs:

* [Automatically retrieving credentials](#automatically-retrieving-credentials)
* [Manually retrieving credentials](#manually-retrieving-credentials)

### Automatically Retrieving Credentials
1. Go to the login page of the website. This page will be different for each website; this section will use the Atlassian website as an example. One of two scenarios can happen:
    * If you only have one set of credentials for this website, the login fields should already be filled in with your credentials. If that is the case, follow the login process of the website until you successfully log in to your account. You do not have to follow the next step.
  ![Automatically Filled Credentials Fields](https://cdnweb.devolutions.net/docs/docs_en_server_ServerOp2024.png)
    * If you have more than one set of credentials or if your credentials are not filled in, click on the {{ en.WBEX }} icon in the credential field and select the entry that contains your credentials for that website. If multiple entries are available, you can search for the one you want using the ***Filter*** bar. Follow the rest of the website's login process until you successfully log in to your account.
  ![Entry Filter and Selection](https://cdnweb.devolutions.net/docs/docs_en_server_ServerOp2021.png)

### Manually Retrieving Credentials
Depending on the options you have enabled/disabled, you may need to retrieve your credentials manually:

1. Go to the login page of the website you want to access. This page will be different for each website; this section will use the Atlassian website as an example.
1. Click on the {{ en.WBEX }} in your browser. Website entries that are linked to this website will appear.
1. Click on the website entry that contains the credentials for this website. If multiple entries are available, you can use the ***Filter*** bar to find the one you need.
   {% snippet icon.badgeInfo %}
   If needed, you can also use the icons that appear when hovering over the entry to copy your username, copy your password, or get an overview of the entry.
   {% endsnippet %}

   ![Entry Selection](https://cdnweb.devolutions.net/docs/docs_en_server_ServerOp2022.png)
4. Your credentials will be transferred to the credentials fields of the website. Follow the rest of the website's login process until you successfully log in to your account.
![Credentials Transfer in Corresponding Fields](https://cdnweb.devolutions.net/docs/docs_en_server_ServerOp2023.png)
