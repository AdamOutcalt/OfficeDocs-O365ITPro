---
title: "Resolve issues with shared mailboxes"
ms.author: cmcatee
author: cmcatee-MSFT
manager: mnirkhe
audience: Admin
ms.topic: get-started-article
f1_keywords:
- 'O365P_SharedMB'
ms.service: o365-administration
localization_priority: Priority
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
description: "----"
---

# Resolve issues with shared mailboxes

If you see error messages when creating or using a shared mailbox, try these possible solutions. 

## Issues with creating shared mailboxes
<a name="bkmk_Fix"> </a>

If you see the error message, **The proxy address "smtp:<shared mailbox name\>" is already being used by the proxy addresses or LegacyExchangeDN of "\<name>". Please choose another proxy address**, it means you're trying to give the shared mailbox a name that's already in use. For example, let's say you want shared mailboxes named info@domain1 and info@domain2. There are two ways to do this:

  - Use Windows PowerShell. See this blog post for instructions: [Create Shared Mailboxes with Same Alias at Different Domains in Office 365](https://www.cogmotive.com/blog/office-365-tips/create-shared-mailboxes-with-same-alias-at-different-domains-in-office-365)
    
  - Name the second shared mailbox something different from the start to get around the error. Then in the [admin center](#how-to-create-a-shared-mailbox-in-the-exchange-admin-center), rename the shared mailbox to what you want it to be.

## Errors about not having send permissions when using a shared mailbox

If you created a shared mailbox and then try to send a message from it, you might get this:

**This message could not be sent. You do not have the permission to send the message on behalf of the specified user.**

This message appears when Office 365 is experiencing a replication latency issue. It should go away in an hour or so, when the information about your new shared mailbox (or added user) is replicated across all of our data centers. Wait an hour and then try again to send a message.

## Related articles

[About shared mailboxes](about-shared-mailboxes.md)

[Create a shared mailbox](create-a-shared-mailbox.md)

[Configure a shared mailbox](configure-a-shared-mailbox.md)

[Convert a user mailbox to a shared mailbox](convert-user-mailbox-to-shared-mailbox.md)

[Remove a license from a shared mailbox](remove-license-from-shared-mailbox.md)


    

