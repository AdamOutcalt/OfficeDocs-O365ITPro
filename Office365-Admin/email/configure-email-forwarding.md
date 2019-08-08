---
title: "Configure email forwarding in Office 365"
ms.author: cmcatee
author: cmcatee-MSFT
manager: mnirkhe
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: 
- M365-subscription-management 
- Adm_O365
- Adm_TOC
ms.custom:
- MSStore_Link
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: ab5eb117-0f22-4fa7-a662-3a6bdb0add74
description: "Set up email forwarding to one or more email accounts using Office365."
---

# Configure email forwarding in Office 365
  
As the admin of an Office 365 organization, you might have company requirements to set up email forwarding for a user's mailbox. Email forwarding lets you forward email messages sent to a user's mailbox to another user's mailbox inside or outside of your organization.


::: moniker range="o365-worldwide"

> [!TIP]
> Need help with the steps in this topic? We’ve got you covered. Make an appointment at your local Microsoft Store with an Answer Desk expert to help resolve your issue. Go to the [Microsoft Stores page](https://go.microsoft.com/fwlink/?LinkID=2041482) and choose your location to schedule an appointment.

::: moniker-end
  
## Configure email forwarding

 Before you set up email forwarding, note the following: 

- Once you set up email forwarding, only **new** emails sent to the  *from*  mailbox will be fowarded. 
    
- Email forwarding requires that the  *from*  account has a license. If you're setting up email forwarding because the user has left your organization, another option is to [convert their mailbox to a shared mailbox](convert-user-mailbox-to-shared-mailbox.md). This way several people can access it. However, a shared mailbox cannot exceed 50GB. 
    
You must have [admin permissions](../add-users/about-admin-roles.md) in Office 365 to do these steps. 

::: moniker range="o365-worldwide"

### Use the new admin center to configure email forwarding

The new admin center is available to all Microsoft 365 admins. You can opt in by selecting the **Try the new admin center** toggle located at the top of the Home page. For more information, see [About the new Microsoft 365 admin center](../microsoft-365-admin-center-preview.md).

1. In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.
    
2. Select the name of the user whose email you want to forward to open the properties page. 
 
3. On the **Mail** tab, select **Manage email forwarding**. 
  
4. On the email forwarding page, set the toggle to **On**, enter the forwarding address, and choose whether you want to keep a copy of forwarded emails. If you don't see this option, make sure a license is assigned to the user account. Select **Save**.
    
    **To forward to multiple email addresses**, you can ask the user to set up a rule in Outlook to forward to the addresses. To learn more, see [Use rules to automatically forward messages](https://support.office.com/article/use-rules-to-automatically-forward-messages-45aa9664-4911-4f96-9663-ece42816d746). 
    
     Or, in the admin center, [create a distribution group](../setup/create-distribution-lists.md), [add the addresses to it](add-user-or-contact-to-distribution-list.md), and then set up forwarding to point to the DL using the instructions in this article.
    
5. Don't delete the account of the user who's email you're forwarding or remove their license!  If you do, email forwarding will stop. 
    
### Use the old admin center to configure email forwarding

1. In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.

::: moniker-end

::: moniker range="o365-germany"
    
 1.   In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page. 
    
::: moniker-end

::: moniker range="o365-21vianet"

 1. In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page. 

::: moniker-end 
    
2. Select the name of the user whose email you want to forward to open the properties page. 

3. Expand **Mail settings**, and then in the **Email forwarding** section, select **Edit**.

4. On the email forwarding page, set the toggle to **On**, enter the forwarding address, and choose whether you want to keep a copy of forwarded emails. If you don't see this option, make sure a license is assigned to the user account. Select **Save**.
    
    **To forward to multiple email addresses**, you can ask the user to set up a rule in Outlook to forward to the addresses. To learn more, see [Use rules to automatically forward messages](https://support.office.com/article/use-rules-to-automatically-forward-messages-45aa9664-4911-4f96-9663-ece42816d746). 
    
     Or, in the admin center, [create a distribution group](../setup/create-distribution-lists.md), [add the addresses to it](add-user-or-contact-to-distribution-list.md), and then set up forwarding to point to the DL using the instructions in this article.
    
5. Don't delete the account of the user who's email you're forwarding or remove their license!  If you do, email forwarding will stop. 