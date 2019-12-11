---
title: "Remove license from shared mailbox"
ms.author: anfowler
author: adefowler
manager: scotv
audience: Admin
ms.topic: troubleshooting
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
ms.assetid: bb229ee9-e7be-4990-b3eb-354e75740496
description: "Remove license from a shared mailbox to assign it to another user. "
---

# Remove a license from a shared mailbox

Shared mailboxes don't need a license unless the mailbox has over 50GB of data. Follow these instructions to remove a license from a shared mailbox so that you can either assign it to a user or return the license so that you aren't paying for a license you don't need.
  
## Remove the license

::: moniker range="o365-worldwide"

> [!NOTE]
> If you're not using the new Microsoft 365 admin center, you can turn it on by selecting the **Try the new admin center** toggle located at the top of the Home page.

1. In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.

   > [!NOTE]
   > You need to remove the license from the Active users page. You can't remove the license from the Shared mailbox page because licenses are user settings. 
  
2. Select the shared mailbox. 
    
3. One the **Licenses and Apps** tab, expand **Licenses** and uncheck the box for the license you want to remove.
    
4. Select **Save changes**.
    
5. When you return to the **Active users** page, the status of the shared mailbox will be **Unlicensed**. 

6. You're still paying for the license. To stop paying for it, [remove the license from your subscription](../subscriptions-and-billing/remove-licenses-from-subscription.md). 

::: moniker-end


::: moniker range="o365-germany"
    
 1. In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page. 
    
   > [!NOTE]
   > You need to remove the license from the Active users page. You can't remove the license from the Shared mailbox page because licenses are user settings. 

2. Select the shared mailbox, and then select **Edit** next to **Product licenses**.
    
3. One the **Product licenses** page, set the toggle to **Off** for the license you want to remove.
    
4. Select **Save**.
    
5. When you return to the **Active users** page, the status of the shared mailbox will be **Unlicensed**. 

6. You're still paying for the license. To stop paying for it, [remove the license from your subscription](../subscriptions-and-billing/remove-licenses-from-subscription.md). 

::: moniker-end

::: moniker range="o365-21vianet"

 1. In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page. 

   > [!NOTE]
   > You need to remove the license from the Active users page. You can't remove the license from the Shared mailbox page because licenses are user settings. 

2. Select the shared mailbox, and then select **Edit** next to **Product licenses**.
    
3. One the **Product licenses** page, set the toggle to **Off** for the license you want to remove.
    
4. Select **Save**.
    
5. When you return to the **Active users** page, the status of the shared mailbox will be **Unlicensed**. 

6. You're still paying for the license. To stop paying for it, [remove the license from your subscription](../subscriptions-and-billing/remove-licenses-from-subscription.md). 

::: moniker-end 

## Related articles

[About shared mailboxes](about-shared-mailboxes.md)

[Create a shared mailbox](create-a-shared-mailbox.md)

[Configure a shared mailbox](configure-a-shared-mailbox.md)

[Convert a user mailbox to a shared mailbox](convert-user-mailbox-to-shared-mailbox.md)

[Resolve issues with shared mailboxes](resolve-issues-with-shared-mailboxes.md)