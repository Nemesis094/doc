---
eleventyComputed:
  title: Roles and permissions
  description: Each role in {{ en.DHUB }} has its own set of permissions.
---
Each ***Role*** in {{ en.DHUB }} has its own set of ***Permissions***.

## Permissions

| PERMISSION                  | RESTRICTED | READERS | PRIVILEGED READERS | OPERATORS | PRIVILEGED OPERATORS | CONTRIBUTORS | {{ en.VLT }} OWNERS |
|-----------------------------|:------------:|:---------:|:---------------------:|:-----------:|:----------------------:|:--------------:|:--------------:|
| View {{ en.VLT }}           |   {{ icon.badgeNotice | safe }}   | {{ icon.badgeNotice | safe }} | {{ icon.badgeNotice | safe }} | {{ icon.badgeNotice | safe }} | {{ icon.badgeNotice | safe }} | {{ icon.badgeNotice | safe }} | {{ icon.badgeNotice | safe }} |
| View entries                |            | {{ icon.badgeNotice | safe }} | {{ icon.badgeNotice | safe }} | {{ icon.badgeNotice | safe }} | {{ icon.badgeNotice | safe }} | {{ icon.badgeNotice | safe }} | {{ icon.badgeNotice | safe }} |
| Manage {{ en.VLT }}         |            |         |                     |           |                      |              | {{ icon.badgeNotice | safe }} |
| Add entries                 |            |         |                     |           |                      | {{ icon.badgeNotice | safe }} | {{ icon.badgeNotice | safe }} |
| Edit entries                |            |         |                     |           |                      | {{ icon.badgeNotice | safe }} | {{ icon.badgeNotice | safe }} |
| Delete entries              |            |         |                     |           |                      | {{ icon.badgeNotice | safe }} | {{ icon.badgeNotice | safe }} |
| Connect (execute)           |            |         |                     | {{ icon.badgeNotice | safe }} | {{ icon.badgeNotice | safe }} | {{ icon.badgeNotice | safe }} | {{ icon.badgeNotice | safe }} |
| View password               |            |         |                     |           | {{ icon.badgeNotice | safe }} | {{ icon.badgeNotice | safe }} | {{ icon.badgeNotice | safe }} |
| View sensitive              |            |         | {{ icon.badgeNotice | safe }} | {{ icon.badgeNotice | safe }} | {{ icon.badgeNotice | safe }} | {{ icon.badgeNotice | safe }} | {{ icon.badgeNotice | safe }} |
| View password history       |            |         |                     |           |                      | {{ icon.badgeNotice | safe }} | {{ icon.badgeNotice | safe }} |
| View sensitive history      |            |         |                     |           |                      | {{ icon.badgeNotice | safe }} | {{ icon.badgeNotice | safe }} |
| Manage attachments          |            |         |                     |           |                      | {{ icon.badgeNotice | safe }} | {{ icon.badgeNotice | safe }} |
| Manage documentation        |            |         |                     |           |

## Sensitive information permissions

In {{ en.DHUB }}, all sensitive information is hidden by default. Some can be viewed by anyone that has access to the entry by clicking on the eye icon, and others require ***View sensitive*** or ***View password*** permissions to be viewed. The value of a hidden custom field is also encrypted and protected with the ***View sensitive*** permission.

The ***View sensitive*** permission is granted to ***Reader***, ***Operator***, ***Contributor***, and ***Manager*** roles, while the ***Contributor*** or ***Manager*** roles are required for the ***View password*** permission. Therefore, even if passwords are indeed sensitive information, you will not be able to view them with the ***View sensitive*** permission alone.

You can see the difference between the ***View sensitive*** permission and ***View password*** permission icons in the image below.

![Sensible information icons](https://cdnweb.devolutions.net/docs/docs_en_hub_Hub2267.png)