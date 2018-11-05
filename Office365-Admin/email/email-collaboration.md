---
title: "Email collaboration in Office 365"
ms.author: kwekua
author: kwekua
manager: scotv
ms.audience: Admin
ms.topic: overview
f1_keywords:
- 'O365P_SCDistListAdmin'
- 'O365P_SCCollabO365'
- 'O365M_SCDistListAdmin'
- 'O365M_SCCollabO365'
- 'O365E_SCDistListAdmin'
- 'O365E_SCCollabO365'
ms.service: o365-administration
localization_priority: Normal
ms.collection: Adm_O365
ms.custom:
- Adm_O365
- Adm_O365_FullSet
- Core_O365Admin_Migration
- MiniMaven
- ScenarioChain
search.appverid:
- BCS160
- MET150
- MOE150
- MOW150
- OWE150
- OWP150
- SPO160
- BSA160
- SPB160
ms.assetid: eb3e840f-ed60-4461-81f5-12381c132b89
description: "Learn about the various types of groups and how to use them with the various collaboration features of Office 365."
---

# Email collaboration in Office 365

Office 365 encourages collaboration through Groups in Outlook, distribution lists (also called distribution groups), shared mailboxes, and public folders. Each of these options has a different purpose, user experience, and feature set. What to use depends on what the user needs to do and which tools your organization provides.
  
## Summary of collaboration options
<a name="BKMK_SUMMARYOFCOLLABORATIONOPTIONS"> </a>

This table explains the various collaboration options available to you.
  


|**Collaboration tool**|**Description**|
|:-----|:-----|
|Groups in Outlook  <br/> |A shared workspace that works across all applications in Office 365. Includes a shared inbox, calendar, and OneDrive for Business site for storing files. Users can create, find, and join Groups in Outlook right from their email or calendar. New and existing users with an Exchange Online or Office 365 subscription can use Groups in Outlook.  <br/> |
|Shared mailbox  <br/> |A mailbox for select users to read and send email messages and share a common calendar. Shared mailboxes also can serve as a generic email address (such as info@contoso.com or sales@contoso.com) that customers can use to inquire about your company. When the Send As permission is enabled on the shared mailbox, email sent from the mailbox will use the generic address (e.g., sales@contoso.com).  <br/> |
|Distribution list (also called distribution group)  <br/> |Used to distribute email messages to two or more people at the same time. Distribution groups are also known as mail-enabled distribution groups. A variant of the distribution group, called the dynamic distribution group, is a mail-enabled Active Directory group object used to send email to a large and evolving group of recipients. The exact recipients are determined by filters and conditions that you specify, such as all members of a particular locale or all full-time employees.   <br/><br/> Office 365 Groups in Outlook offer a more powerful solution for collaboration than distribution groups. To learn more, see [Why you should upgrade your distribution lists to groups in Outlook](https://support.office.com/article/7fb3d880-593b-4909-aafa-950dd50ce188.aspx) and [Migrate distribution lists to Office 365 Groups](../manage/upgrade-distribution-lists.md).  <br/> |
|Public folder  <br/> |Designed for shared access, public folders provide an easy and effective way to collect, organize, and share information with other people in your organization. Public folders organize content in a deep hierarchy that's easy to browse and always visible in the Outlook folder view. A public folder can be mail-enabled and added as a member of the distribution group. Email sent to the distribution group is automatically added to the public folder for archiving or later reference. Public folders also provide simple document sharing when you don't have a SharePoint Online subscription.  <br/> |
   
## Which collaboration tool to use?
<a name="BKMK_SUMMARYOFCOLLABORATIONOPTIONS"> </a>

The following table gives you a quick glance at the various types of groups and explains when and how to use them with the various collaboration features.
  

||**Groups in Outlook**|**Distribution lists**|**Shared mailboxes**|**Public folders**|
|:-----|:-----|:-----|:-----|:-----|
|**Who uses?** <br/> |Users who want a collaboration workspace for their group messages, files, and calendar that is integrated with the services they already use (Outlook Web App, OneDrive for Business)  <br/> |Users who need to send email to a group of recipients with a common interest or characteristic.  <br/> |Shared mailboxes are a great way to handle customer email questions because several people in your organization can share the responsibility of monitoring the mailbox and responding to queries. Your customer questions get quicker answers, and related emails are all stored in one mailbox.  <br/><br/> Delegates working on behalf of a virtual identity, such as support@contoso.com. Delgates can respond to email as that shared mailbox identity.  <br/> |With the proper permissions, everyone in your organization can access and search public folders. They are ideal for email archiving or for sharing documents.  <br/> |
|**Ideal group size** <br/> |Any  <br/> |Large  <br/> |Small  <br/> |Large  <br/> |
|**Access** <br/> |Exchange Online and Office 365 users  <br/> |For distribution groups, members must be manually added. For dynamic distribution groups, members are added based on filtering criteria.  <br/> |Users can be granted Full Access and/or Send As permissions. If granted Full Access permissions, users must also add the shared mailbox to their Outlook profile to access the shared mailbox.  <br/> |Accessible by anyone in your organization  <br/> |
|**Shared calendar?** <br/> |Yes  <br/> |No  <br/> |Yes  <br/> |Yes  <br/> |
|**Email arrives in user's personal Inbox?** <br/> |No. Users can subscribe to a group and then forward all Group messages to their inbox  <br/> |Yes. Email arrives in the inbox of all distribution group members.  <br/> |No. Email arrives in the Inbox of the shared mailbox.  <br/> |No. Email arrives in the public folder.  <br/> |
|**Supported clients** <br/> | Outlook 2016  <br/>  Outlook 2013 (forward after subscribing)  <br/>  Outlook Web App  <br/>  Outlook 2010 (forward after subscribing)  <br/>  Outlook 2007 (forward after subscribing)  <br/> | Outlook 2016  <br/>  Outlook 2013  <br/>  Outlook Web App  <br/>  Outlook 2010  <br/>  Outlook 2007  <br/> | Outlook 2016  <br/>  Outlook 2013  <br/>  Outlook Web App  <br/>  Outlook 2010  <br/>  Outlook 2007  <br/> | Outlook 2016  <br/>  Outlook 2013  <br/>  Outlook Web App  <br/>  Outlook 2010  <br/>  Outlook 2007  <br/> |

  
## Related topics

- [Manage distribution groups](https://technet.microsoft.com/en-us/library/bb124513%28v=exchg.150%29.aspx)
    
- [Use Office 365 Groups instead of Site Mailboxes](https://support.office.com/article/737d6b1f-67cc-41fe-8db8-f2d09dd1673b.aspx)
    
- [Create shared mailboxes in Office 365](create-a-shared-mailbox.md)
    
- [Public folders in Office 365 and Exchange Online](https://technet.microsoft.com/en-us/library/jj200758%28v=exchg.150%29.aspx)
    

