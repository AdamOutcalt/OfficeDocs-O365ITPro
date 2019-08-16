---
title: "Create an Office 365 group in the admin center"
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: Admin
ms.topic: get-started-article
f1_keywords:
- 'O365P_O365GroupsAdmin'
ms.service: o365-administration
localization_priority: Normal
ms.collection: 
- M365-subscription-management 
- Adm_O365
- Adm_TOC
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 74a1ef8b-3844-4d08-9980-9f8f7a36000f
description: "Learn to create and delete Office 365 groups, add and remove group members, and customize how the group works."
---

# Create an Office 365 group in the Microsoft 365 admin center
  
While users can create an Office 365 group from Outlook or other apps, as an admin, you may need to create or delete groups, add or remove members, and customize how they work. The Microsoft 365 admin center is the place to do this. 

> [!TIP]
> Office 365 connected Yammer groups must be created in Yammer, but can be managed in the Microsoft 365 admin center like other Office 365 groups. To learn more, see [Yammer and Office 365 Groups](https://support.office.com/article/d8c239dc-a48b-47ab-b85e-6b4b8191a869.aspx). 

## Create an Office 365 group

::: moniker range="o365-worldwide"

1. In the admin center, go to the **Groups** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">Groups</a> page.

::: moniker-end

::: moniker range="o365-germany"

1. In the [admin center](https://go.microsoft.com/fwlink/p/?linkid=848041), go to the **Groups** > **Groups** page. 

::: moniker-end

::: moniker range="o365-21vianet"

1. In the [admin center](https://go.microsoft.com/fwlink/p/?linkid=850627), go to the **Groups** > **Groups** page. 

::: moniker-end

2. Select **Add a group**.
  
3. Under **Type**, choose **Office 365**.
    
    ![Create a new Office 365 Group, a new distribution list, or a new security group](../media/a50b372c-feab-4ac5-90c3-e7fcb1ff649a.png)

4. Type a name for the group.
    
5. Type a unique email address for the group.
    
6. Select **Select Owner**, and then choose the name of the person who will be designated to manage the group. Anyone who is a group owner will be able to delete email from the Group inbox. Other members won't be able to delete email from the Group inbox. 
    
7. Select **Add**.

8. Select **Close**.
    
## Configure the group

Once the group has been created, you can add members and configure additional settings.

::: moniker range="o365-worldwide"
  
### Use the new admin center to add members to a group

The new admin center is available to all Microsoft 365 admins. You can opt in by selecting the **Try the new admin center** toggle located at the top of the Home page. For more information, see [About the new Microsoft 365 admin center](../microsoft-365-admin-center-preview.md).

Users can [add themselves or request approval](https://support.office.com/article/Join-a-group-in-Outlook-2e59e19c-b872-44c8-ae84-0acc4b79c45d), or you can add them now.

1. In the admin center, refresh the page so your new group appears, select **Groups** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">Groups</a>, and then select the name of the group that you want to add members to.
    
2. On the **Members** tab, select **View all and manage members**.

3. Select **Add members**.
    
4. Select the users you want to add, and then select **Save**.
    
5. Select **Close** three times. 
    
The group will appear in Outlook with members assigned to it.

### Use the old admin center to add members to a group

::: moniker-end

Users can [add themselves or request approval](https://support.office.com/article/Join-a-group-in-Outlook-2e59e19c-b872-44c8-ae84-0acc4b79c45d), or you can add them now.

1. In the admin center, refresh the page so your new group appears, select **Groups** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">Groups</a>, and then select the group that you want to add members to.
    
2. Next to **Members**, select **Edit**.

3. Select **Add members**.
    
4. Select the users you want to add, and then select **Save**.
    
5. Select **Close** three times. 
    
The group will appear in Outlook with members assigned to it.
  
### Send copies of conversations to group members' inboxes
  
When you use the admin center to create a group, by default users  do not get copies of group emails and meeting invitations sent to their inboxes. They'll need to go to the group to see conversations and meetings. You can change this setting in the admin center.

When you turn this setting on, group members will get a copy of group emails and meeting invitations sent to their Outlook Inbox. They can read and delete this copy of the email and not affect anyone else. In the Group inbox, a copy of the email still exists.

Group members can opt out of receiving these emails by choosing to stop following the group in Outlook.

::: moniker range="o365-worldwide"

#### Use the new admin center to send copies of conversations to group members' inboxes

The new admin center is available to all Microsoft 365 admins. You can opt in by selecting the **Try the new admin center** toggle located at the top of the Home page. For more information, see [About the new Microsoft 365 admin center](../microsoft-365-admin-center-preview.md).

1. In the admin center, go to the **Groups** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">Groups</a> page, and then select the name of the group you want to change. 

2. On the **Settings** tab, select **Send copies of group conversations and events to group members** if you want members to receive copies of group messages and calendar items in their own inbox.

3. Select **Save**.

#### Use the old admin center to send copies of conversations to group members' inboxes

::: moniker-end

1. In the admin center, go to the **Groups** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">Groups</a> page, and then select the group you want to change.

2. Next to **Name**, select **Edit**.

3. Turn **Send copies of group conversations and events to group members' inboxes** to **On** if you want members to receive copies of group messages and calendar items in their own inbox.

4. Select **Save**.

### Let people outside the organization email the group

This option is great if you want to have a company email address such as info@contoso.com.
 
::: moniker range="o365-worldwide"
 
#### Use the new admin center to let people outside the organization email the group

The new admin center is available to all Microsoft 365 admins. You can opt in by selecting the **Try the new admin center** toggle located at the top of the Home page. For more information, see [About the new Microsoft 365 admin center](../microsoft-365-admin-center-preview.md).

1. Refresh your admin center page so your new group appears.

2. In the admin center groups list, select the name of the group you want to change, and then on the **Settings** tab, select **Allow external senders to email this group**.
    
4. Select **Save**.


#### Use the old admin center to let people outside the organization email the group

::: moniker-end

1. Refresh your admin center page so your new group appears.
    
2. In the admin center groups list, select the group you want to change, and then next to **Name**, select **Edit**. 
    
3. Set the **Let people outside the organization email the group** toggle to **On**.
    
4. Select **Save**.

## Who can delete email from the Group Inbox?

The Group owner can delete any emails from the Group Inbox, regardless of whether they were the initial author.
  
A member can delete an email conversation from the Group Inbox if they initiated it, and only using Outlook on the web (right-click the email, then choose **Delete**). They can't do it from the Outlook app (Outlook 2016).
  
When an email is deleted from the group mailbox, it is not deleted from any of the group members' personal mailboxes.

## Related topics

[Manage guest access to Office 365 groups](https://support.office.com/article/7c713d74-a144-4eab-92e7-d50df526ff96.aspx)

[Choose the domain to use when creating Office 365 Groups](choose-domain-to-create-groups.md)

[Allow members to send as or send on behalf of an Office 365 Group](allow-members-to-send-as-or-send-on-behalf-of-group.md)

[Upgrade distribution lists to Office 365 Groups](../manage/upgrade-distribution-lists.md)

[Manage Office 365 Groups with PowerShell](https://support.office.com/article/aeb669aa-1770-4537-9de2-a82ac11b0540)
