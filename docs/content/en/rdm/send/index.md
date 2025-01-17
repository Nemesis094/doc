---
eleventyComputed:
  title: "{{ en.DSEND }}"
  description: "{{ en.DSEND }} features a secure method to generate a link to share secrets instead of using insecure email to send sensitive data."
  order: 45
---
{{ en.DSEND }} features a secure method to generate a link to share secrets instead of using insecure email to send sensitive data. Send a password through in-app secure messaging or create a shareable link to send secrets outside your organization securely.

## Features
{% snippet icon.badgeInfo %}
[{{ en.DSEND_STANDALONE }}](https://devolutions.net/devolutions-send/) is also available if you do not have a license for one of our compatible products.
{% endsnippet %}

Despite sharing the same underlying architecture, slight differences exist between the feature set of the standalone and in-app versions of {{ en.DSEND }}.

* Unique short-lived (24-hour) link encrypted on the client side.
* Optional protection via a client-provided passphrase.
* Users may be non-Devolutions users (not linked to a {{ en.DA }}).
* Character limit of 10 kb.
* A sender email is required and stored with the GUID as part of the “payload” stored in the database.

## Using {{ en.DSEND }} with {{ en.RDM }}
1. In the ribbon, navigate to the ***Window*** tab.
1. Click ***Message***.  
![Message button](https://cdnweb.devolutions.net/docs/RDMW0016_2024_1.png)
1. Click ***Send Message***.  
![Send Message](https://cdnweb.devolutions.net/docs/RDMW0017_2024_1.png)
1. Select one of the two available options:
    * [Send In-app](#send-in-app)
    * [Create Shareable Link](#create-shareable-link)

### Send in-app
![Send in-app](https://cdnweb.devolutions.net/docs/RDMW0018_2024_1.png)
This feature is covered in [***Secure messages***](/rdm/commands/window/panels/secure-messages/).

### Create Shareable Link
![Create Shareable Link](https://cdnweb.devolutions.net/docs/RDMW0025_2024_1.png)
1. Enter the information in the ***Message*** field.
   {% snippet icon.badgeInfo %}
   A ***Passphrase*** may be added for additional security.
   {% endsnippet %}
1. Click on ***Create Link***.
![Create Link](https://cdnweb.devolutions.net/docs/RDMW0026_2024_1.png)
1. Copy the link and send it to the intended individual(s).
![Copy to Clipboard](https://cdnweb.devolutions.net/docs/RDMW0027_2024_1.png)
