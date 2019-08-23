---
title: "Set up multi-factor authentication for Office 365 users"
ms.author: sirkkuw
author: sirkkuw
manager: mnirkhe
audience: Admin
ms.topic: article
f1_keywords:
- 'O365E_AdmSetSecPrivMFA'
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
- BEA160
- GEA150
ms.assetid: 8f0454b2-f51a-4d9c-bcde-2c48e41621c6
description: "Learn how to set up multi-factor authentication for Office 365 users and manage the user settings. "
monikerRange: 'o365-worldwide'
---

# Set up multi-factor authentication
  
This article describes how to set up multi-factor authentication (MFA) for Office 365 users. For more information about MFA, see [How Azure multi-factor authentication works](https://go.microsoft.com/fwlink/p/?LinkId=627437).
  
You get a free version of Azure multi-factor authentication as part of your Office 365 for business subscription. For a list of features included in your version of Office 365, see [How to get Azure Multi-Factor Authentication](https://docs.microsoft.com/en-us/azure/multi-factor-authentication/multi-factor-authentication-versions-plans).

> [!NOTE]
> You must be an Office 365 global admin to set up or modify multi-factor authentication.
  
## Enable multi-factor authentication for your organization

All Office 2016 client applications support MFA through the use of the Active Directory Authentication Library (ADAL). This means that app passwords aren't required for Office 2016 clients. However, you need to make sure your Office 365 subscription is enabled for ADAL, or modern authentication.

1. To enable modern authentication, from the [admin center](https://go.microsoft.com/fwlink/p/?linkid=834822), turn on the new admin center by selecting **Try the new admin center** toggle located at the top of the Home page.

2. Select **Settings** \> **Services & add-ins** and then choose **Modern authentication** from the list.

3. Check the **Enable modern authentication** box in the **Modern authentication** panel. 

    ![Modern authentication panel with enable checkbox checked.](../media/enablemodernauth.PNG)

## Set up multi-factor authentication in the new Microsoft 365 admin center

1. In the [admin center](https://go.microsoft.com/fwlink/p/?linkid=834822), turn on the new admin center by selecting the **Try the new admin center** toggle located at the top of the Home page.

2. In the right navigation pane, select **Setup**.

3. On the **Turn on multi-factor authentication (MFA)** card, select **View**.

4. Select **Get started**.

5. Select the **Require multi-factor authentication** and **Require users to register for multi-factor authentication and block access if risk is detected** check boxes.

6. Under **Do you want to exclude anyone from these policies**, select any users that you want to exclude from the drop-down list box.

7. Select **Choose policy**. You will return to the **Multi-factor authentication (MFA)** page, which will now say **Completed**. 

After you set up multi-factor authentication for your organization, your users will be required to set up two-step verification on their devices. For more information, see [Set up 2-step verification for Office 365](https://support.office.com/article/ace1d096-61e5-449b-a875-58eb3d74de14).

## Set up multi-factor authentication in the old Microsoft 365 admin center

1. In the admin center, go to **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a>.

2. **IMPORTANT**: BEFORE you select a user, select **Multi-factor authentication** from the drop-down list above the list of users.
  
    > [!NOTE]
    > If you don't see the **Multi-factor authentication** option, then you aren't a global admin for your subscription. Only global admins can enable or disable MFA.

3. On the **multi-factor authentication** page, find the people for whom you want to enable MFA. In order to see everyone, you might need to change the **Multi-Factor Auth status** view at the top. 

    The views have the following values, based on the MFA state of the users:

  - **Any** Displays all users. This is the default state. 

  - **Enabled** The person has been enrolled in MFA, but has not completed the registration process. They will be prompted to complete the process the next time they sign in.

  - **Enforced** The person may or may not have completed registration. If they have completed the registration process, then they are using MFA. Otherwise, they will be prompted to complete the process the next time they sign in.

4. Select the check box next to the people for whom you want to enable MFA.

5. On the right, under **quick steps**, you'll see **Enable** and **Manage user settings**. Select **Enable**.

6. In the dialog box that opens, select **enable multi-factor auth**.
   
## Allow MFA users to create app passwords for Office client apps

Older email applications like Office 2013 need app passwords. Here's how to allow your users to create them:

1. In the admin center, go to **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a>.

2. **IMPORTANT**: BEFORE you select a user, select **Multi-factor authentication** above the list of users.
  
> [!Tip]
> If you don't see the **Multi-factor authentication** option, then you aren't a global admin for your subscription. Only global admins can enable or disable MFA.

3. On the **multi-factor authentication** page, select **service settings**.

    ![The multi-factor authentication page with a hand pointing to the service settings link.](../media/98fb3542-8f43-4e3b-9a06-c6a091973188.png)
  
4. Under **app passwords**, select **Allow users to create app passwords to sign into non-browser apps**. People can then use client Office apps after they create a new password.

5. Select **Save**, then **Close**.

> [!NOTE]
> Modern authentication can be enabled for Office 2013 by setting a few registry keys. For more information, see [Enable Modern Authentication for Office 2013 on Windows devices](enable-modern-authentication.md).

## Manage MFA user settings

1. On the **multi-factor authentication** page, select the check box next to the people you want to manage.

2. On the right, under **quick steps**, select **Manage user settings**.

3. In the **Manage user settings** dialog box, select one or more of the following options: 

  - **Require selected users to provide contact methods again**

  - **Delete all existing app passwords generated by the selected users**

  - **Restore multi-factor authentication on all remembered devices**

4. Select **Save**, then **Close**.

## Bulk update users in MFA

You can bulk update the status for existing people by using a CSV file. The CSV file is used only for enabling or disabling MFA, based on the user names present in the file. It is not used to create new users.
  
1. On the **multi-factor authentication** page, select **bulk update**.

2. In the **Select a CSV file** dialog box, select **Browse for file**.

3. Browse for the file that contains the updates, then select **Open**. The column headings in your file must match the column headings in the following example:

    ![bulk update CSV sample file](../media/2adcd052-b044-4d0c-a5e4-b859645f5ea4.png)
  
4. Select the **Next** arrow. 

5. After the file is verified, select the **Next** arrow to update the accounts. 

6. When the process is finished, select the **Done** checkmark.

## Manage MFA settings in the Azure portal

1. From the [admin center](https://go.microsoft.com/fwlink/p/?linkid=834822), turn on the new admin center by selecting **Try the new admin center** toggle located at the top of the Home page.

2. In the right navigation pane, select **Setup**.

3. On the **Turn on multi-factor authentication (MFA)** card, select **View**.

4. On the **Turn on multi-factor authentication (MFA)** page, select **Manage**.

5. The **Azure portal Conditional Access - Policies** page will appear. To turn multi-factor authentication on or off:

    1. Select **Baseline policy: End user protection (Preview)**, and turn the **Enable** toggle on or off. 

    2. Select **Baseline policy: Require MFA for admins (Preview)**, and turn the **Enable** toggle on or off.

    > [!NOTE]
    > To exclude users from a policy, select **specific users excluded** > **Select excluded users**, select the users from the list, and then choose **Select**.

## Instructions for your users after MFA is set up

After you enable MFA on your tenant, give the following instructions to people to set up their second sign-in method for Office 365:
  
- [Set up 2-step verification for Office 365](https://support.office.com/article/ace1d096-61e5-449b-a875-58eb3d74de14.aspx)

- [Create an app password for Office 365](https://support.office.com/article/3e7c860f-bda4-4441-a618-b53953ee1183.aspx)
