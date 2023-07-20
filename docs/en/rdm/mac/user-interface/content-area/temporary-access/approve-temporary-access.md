---
eleventyComputed:
  title: Approve temporary access to an entry in {{ en.RDM }} for Mac
  order: 20
  description: The Temporary Access feature allows users to request a temporary elevation of their permissions for a specific entry. The approver must then approve or deny the request. 
---

{% snippet icon.badgeInfo %} 
If a temporary access request was made in {{ en.RDM }} from a {{ en.HUB }} database, the authorization process must be performed in {{ en.HUB }}. See [Approve temporary access to an entry in {{ en.HUBB }}](/hub/web-interface/hub-overview/temporary-access/approve-temporary-access/). 
{% endsnippet %}
 
The ***Temporary Access*** feature allows users to request a temporary elevation of their permissions for a specific entry. The approver must then approve or deny the request. 

{% snippet icon.badgeInfo %} 
When using {{ en.DVLS }} , Microsoft SQL Server or Microsoft Azure SQL data sources, you must first [Enable temporary access](/kb/remote-desktop-manager/how-to-articles/enable-temporary-access/) in {{ en.RDM }}. 
{% endsnippet %}
 
To learn how to view your past and current requests, go to [View temporary access requests](#view-temporary-access-requests).   

To learn how to respond to a request, go to [Approve/Deny temporary access requests](#approvedeny-temporary-access-requests).  

## View temporary access requests 

To view all your past and current requests, you must use the following ***pending access requests*** box to open the ***Pending Access Requests*** window.  
![Dashboard – pending access requests](https://webdevolutions.blob.core.windows.net/docs/en/rdm/mac/RDMMac6005.png) 

In the ***Pending Access Requests*** window, you can see all your temporary access requests and sort them by ***Status***, ***Username***, ***Data source user***, ***Entry***, ***Action***, ***Requested on***, ***Requested duration***, ***Requested start time***, ***Requested end time***, ***Authorized duration***, ***Authorized start time***, ***Authorized end time***, ***Authorizer username*** and ***Authorizer data source user***.
![Show temporary access requests](https://webdevolutions.blob.core.windows.net/docs/en/rdm/mac/RDMMac6006.png) 

It is also possible to display only certain requests with the ***Status*** drop-down menu or with the filter bar at the top.  

Using ***View messages***, you can view the ***Request message*** and the ***Authorization message*** of a specific request.  

![View messages](https://webdevolutions.blob.core.windows.net/docs/en/rdm/mac/RDMMac6016.png) 

The ***Request message*** window opens.

![Request messages](https://webdevolutions.blob.core.windows.net/docs/en/rdm/mac/RDMMac6007.png) 

Finally, clicking on ***Approve*** or ***Deny*** opens the ***Temporary Access Response*** window, which is described in the [next section](#approvedeny-temporary-access-requests). 

## Approve/Deny temporary access requests 

{% snippet icon.badgeInfo %} 
The duration of ***Temporary Access*** begins when the request is approved.
{% endsnippet %}

To respond to a request, you need to open the ***Temporary Access Response*** window. There are two ways to access it.  

The first option is to use the ***Pending Access Requests*** box (see image below) in the ***Overview*** tab of your ***Dashboard***. Clicking on either the green check mark (approve the request) or the red "X" (deny the request) next to a request will open the ***Temporary Access Response*** window.  
![Pending Access Requests](https://webdevolutions.blob.core.windows.net/docs/en/rdm/mac/RDMMac6008.png) 

The second option requires you to go through the other ***Pending Access Requests*** box described in the [previous section](#view-temporary-access-requests). Whatever way you choose to access the response window, the result will be the same.  
![Temporary Access Response](https://webdevolutions.blob.core.windows.net/docs/en/rdm/mac/RDMMac6014.png) 

This view is divided into two sections: 

* The ***Request Info*** section contains information about the user's request. Because this was done on the user's side, fields in this section cannot be edited. You can view the ***Entry's dependencies*** such as linked credentials and VPNs.

* The ***Response Parameters*** section allows you to change the temporary access duration specified by the user. It is also possible to write a message to the user explaining your decision, but it remains optional. 

Clicking on ***Approve*** or ***Deny*** will approve or deny the request, depending on what you selected earlier. A confirmation window will pop up which you can make disappear by clicking on ***OK***. 

{% snippet icon.badgeInfo %} 
To learn more about the end user experience in {{ en.RDM }}, visit [Request temporary access to an entry in {{ en.RDM }} for Mac](/rdm/mac/user-interface/content-area/temporary-access/request-temporary-access/). 
{% endsnippet %}