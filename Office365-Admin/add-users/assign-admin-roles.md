---
title: "Assign admin roles in Office 365 for business"
ms.author: cmcatee
author: cmcatee-MSFT
manager: mnirkhe
audience: Admin
ms.topic: get-started-article
f1_keywords:
- 'O365P_AssignAdminPermissions'
ms.service: o365-administration
localization_priority: Normal
ms.collection: 
- M365-subscription-management
- Adm_O365
- Adm_O365_Top
- Adm_UI_Elements
- EU_O365_UI_Elements
- strat_admin_top
ms.custom:
- Adm_O365
- Adm_O365_FullSet
- Adm_O365_Top
- MiniMaven
- strat_admin_top
- MSStore_Link
search.appverid:
- BCS160
- MET150
- MOE150
- BEA160
- GEA150
ms.assetid: eac4d046-1afd-4f1a-85fc-8219c79e1504
description: "Learn how to assign administrator roles to a user or multiple users in your business so that they can perform specific tasks in the Microsoft 365 admin center."
---

# Assign admin roles
 
If you're the person who purchased your Microsoft business subscription, you are the global admin. This means you have unlimited control over the products in your subscriptions and you can access most data.

For more informataion, see [About admin roles](about-admin-roles.md).

When you add new users, if you don't assign them an admin role then they are in the "user role" and don't have admin privileges to any of the Microsoft admin centers. But if you need help getting things done, you can assign an admin role to a user. For example, if you need someone to help reset passwords, you shouldn't assign them the global admin role, you should assign them the password admin role. Having too many global admins, with unlimited access to your data and online business, is a security risk.
  
## Assign admin roles to a user from the new admin center
This new roles experience is rolling out to organizations starting at the end of June. If you aren't seeing the new **Roles** page, see [Assign admin roles from the classic admin center](assign-admin-roles.md#assign-admin-roles-to-a-user-from-the-classic-admin-center) later in this article.

In the new admin center, you can assign users to a role in 2 different ways: 
- You can go to the user's details and **Manage roles** to assign a role to the user.
- And you can now go to **Roles** and select the role, and then add multiple users to it.

### Assign admin roles to users (New Roles experience)

1. In the admin center, go to **Roles** > **Roles** to view all of the admin roles available for your organization.
1. Select the admin role that you want to assign the user to. 
1. Select **Assigned admins** > **Add**.
1. Type the user's **display name** or **username**, and then select the user from the list of suggestions. 
1. Add multiple users until you're done. 
1. Select **Save**, and then the user will be added to the list of assigned admins.

### Assign a user to an admin role from Active users
::: moniker range="o365-worldwide"
1.  In the admin center, go to **Users** > [Active users](https://go.microsoft.com/fwlink/p/?linkid=834822) page.

::: moniker-end

::: moniker range="o365-germany"

1. In the admin center, go to **Users** > [Active users]https://go.microsoft.com/fwlink/p/?linkid=847686) page.

::: moniker-end

::: moniker range="o365-21vianet"

1. In the admin center, go to **Users** > [Active users](https://go.microsoft.com/fwlink/p/?linkid=850628) page.

::: moniker-end

2. On the **Active users** page, select the user whose admin role you want to change. In the flyout pane, next to **Roles**, choose **Manage roles**. 

3. Select the admin role that you want to assign to the user. If you don't see the role you're looking for, select **Show all** at the bottom of the list.

## Assign admin roles to a user from the classic admin center

::: moniker range="o365-worldwide"
1.  In the admin center, go to **Users** > [Active users](https://go.microsoft.com/fwlink/p/?linkid=834822) page.

::: moniker-end

::: moniker range="o365-germany"

1. In the admin center, go to the [Active users]https://go.microsoft.com/fwlink/p/?linkid=847686) page.

::: moniker-end

::: moniker range="o365-21vianet"

1.In the admin center, go to **Users** > (https://go.microsoft.com/fwlink/p/?linkid=850628) page.

::: moniker-end

2. On the **Active users** page, select the user whose administrator role you want to change. In the detail pane, next to **Roles**, choose **Edit**. 
    
    If you don't see the **Edit** option, then you don't have a permission to edit and can't assign admin roles to other people. Ask a global admin in your business to assign roles for you. In a small business, the business owner (the person who purchased your subscription) is a global admin. In a large business, key people in the IT department are global admins.

3. Choose **Customized administrator** to see a list of roles we've customized for you. For a description of each role, see [About Office 365 admin roles.](about-admin-roles.md)
    
## More info about admin role settings

1. In the **Alternative email address** box, type an email address that is not connected to Office 365. This email address is used for important notifications, including resetting the password for your Office 365 admin account, so the person must be able to access this email account whether they can access Office 365 or not. 
    
    > [!NOTE]
    > If you don't want to receive product-related communications at this alternate email address, change your contact preferences on the **About me** page. For more information, see [Change your contact preferences](../manage/change-contact-preferences.md). 
  
2. Choose **Save** \> **Close**.
    
3. Choose **More** > **Edit contact information**.
    
4. In the **Mobile phone** box, type the number of a mobile phone—including the country code if the user has one—that can receive a text (SMS) message. This phone number is also used when you reset your password for your Office 365 admin account. 
    
    You need a mobile phone that's capable of receiving text messages for password reset only if one or both of the following applies to you:
    
  - Your organization has a custom domain that you've set up to use with Office 365.
    
  - Your Office 365 subscription is synchronized through directory synchronization.
    
5. When you have finished, choose **Save**.
    
### Assign admin roles to multiple users

If you know PowerShell, see [Assign roles to user accounts with Office 365 PowerShell](https://go.microsoft.com/fwlink/?linkid=854257). It's ideal for assigning roles to hundreds of users.
  
Use the following instructions to assign roles to tens of users.

::: moniker range="o365-worldwide"
1.  In the admin center, go to the [Active users](https://admin.microsoft.com/AdminPortal/Home#/homepage) page

::: moniker-end

::: moniker range="o365-germany"

1. In the admin center, go to the [Active users](https://portal.office.de/adminportal/home) page.

::: moniker-end

::: moniker range="o365-21vianet"

1.In the admin center, go to the [Active users](https://login.partner.microsoftonline.cn) page.

::: moniker-end

2. On the **Active users** page, check the box next to the names of the users whose admin roles you want to change, and then click **Edit user roles**.
    
3. Choose the roles you want to assign, and the click **Save**.
    
## Didn't work for you?

Here are the top issues customers encounter when assigning admin roles:
  
admin role and so you don't have permissions to assign admin roles to other users. Ask another admin to assign roles for you.

::: moniker range="o365-worldwide"

> [!TIP]
> Need help with the steps in this topic? We’ve got you covered. Make an appointment at your local Microsoft Store with an Answer Desk expert to help resolve your issue. Go to the [Microsoft Stores page](https://go.microsoft.com/fwlink/?LinkID=2041482) and choose your location to schedule an appointment.

::: moniker-end
    
## Related Topics

[Assign roles to user accounts with Office 365 PowerShell](https://docs.microsoft.com/en-us/office365/enterprise/powershell/assign-roles-to-user-accounts-with-office-365-powershell)

[Authorize or remove partner relationships](https://support.office.com/article/201ccb3b-6011-4bf1-a6b2-84e7cc1ee2d0.aspx)