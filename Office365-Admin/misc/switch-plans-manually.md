---
title: "Switch Office 365 for business plans manually"
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
ms.custom:
- Adm_O365
- Core_O365Admin_Migration
- MiniMaven
search.appverid:
- BCS160
- MET150
- MOE150
- BEA160
ms.assetid: eb0d0680-5677-41a0-8c46-4b9d47f1c209
ROBOTS: NOINDEX
description: "Switch Office 365 for business subscriptions manually by buying a new subscription and ensuring that both the subscriptions are listed and active."
---

# Switch Office 365 for business plans manually

::: moniker range="o365-worldwide"
> [!NOTE]
> This article applies to the old admin center. To view the article about the admin center (preview), see [Change plans manually](change-plans-manually.md). The preview is available to all Microsoft 365 admins, you can opt in by selecting **Try the preview** toggle located at the top of the Home page. For more information, see [About Microsoft 365 admin center preview](../microsoft-365-admin-center-preview.md).
::: moniker-end

## Step 1: Decide how to switch plans

The best way to switch all your users from one plan to another is to use the [Use the Switch plans button](../subscriptions-and-billing/switch-to-a-different-plan.md#use-the-switch-plans-button). Sometimes this isn't possible. Do a manual switch instead:
  
- If the **Switch plans** button isn't there.

- If, when you select the **Switch plans** button, the plan you want isn't listed.

- If you don't want to switch all your users in the same way. Some businesses need different users subscribed to different plans. Use a manual switch for this.

To continue with a manual switch, read [Step 2: Buy a new subscription](#step-2-buy-a-new-subscription) in this topic.
  
## Step 2: Buy a new subscription

 **Already purchased?** If you already have a subscription you want to move users to, skip this step and go to [Step 3: Check your new subscription and licenses](#step-3-check-your-new-subscription-and-licenses) in this topic.
  
- OR -
  
 **Purchase a new subscription and licenses:** Follow the steps in [Buy another Office 365 for business subscription](../subscriptions-and-billing/buy-another-subscription.md) to buy a new subscription.
  
Make sure you purchase a subscription for the same organization that the users are in now. For example, check the email addresses for the users you want to move. If their email addresses include @contoso.com, you must purchase a new subscription for contoso.com. Include a license for each user that you want to move.
  
 **If you need help choosing a plan**, see the [Office 365 for business product comparison](https://go.microsoft.com/fwlink/p/?linkid=842056) page, or [call support](../contact-support-for-business-products.md).
  
## Step 3: Check your new subscription and licenses

1. In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Subscriptions</a> page.

    If you're using Office 365 Germany, go to this <a href="https://go.microsoft.com/fwlink/p/?linkid=847745" target="_blank">Subscriptions</a> page.

    If you're using Office 365 operated by 21Vianet, go to this <a href="https://go.microsoft.com/fwlink/p/?linkid=850626" target="_blank">Subscriptions</a> page.

2. **Verify that both subscriptions are listed and active**

    The subscription that you're moving users from and the subscription that you're moving users to must be listed together. If the new subscription isn't there when you first check, try again later. Check that both subscriptions are listed under **ACTIVE**. [The new subscription isn't listed, or isn't active](#the-new-subscription-isnt-listed-or-isnt-active).

   **The new Office 365 for business subscription with available licenses**

    ![The subscription page showing the number of licenses for the new subscription.](../media/65a73e96-7c95-4daa-b6ec-71a4bf74dda5.png)
  
3. **Check that you have enough licenses for each user**

    Each user needs a license that matches their subscription. So if you want to move ten users to Office 365 Enterprise E5, you'll need to make sure ten licenses are available. In the picture here, ten licenses were purchased for Office 365 Enterprise E5, and all ten licenses are available for assignment.

4. **Need more licenses for the new subscription?** Go to the **Subscriptions** page and [Buy more licenses](../subscriptions-and-billing/buy-licenses.md).
  
    [What about the old licenses?](#what-about-the-old-licenses)

### The new subscription isn't listed, or isn't active

- **If you purchased a subscription by invoice** and a credit check is required, it can take up to two working days before the subscription is available.

- **If you purchased two subscriptions and they are not both listed here**, they may have been purchased for different organizations (for different domains). Subscriptions can't cross organization boundaries.

- **If you know you have an additional subscription**, and it's not listed here, or not listed under **ACTIVE**, [call support](../contact-support-for-business-products.md).

### What about the old licenses?

The licenses for the current subscription will be removed later; you'll only pay for the new user licenses from then on.
  
## Step 4: Reassign licenses

### Reassign a license for one user

1. In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.

    If you're using Office 365 Germany, go to this <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.

    If you're using Office 365 operated by 21Vianet, go to this <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.

2. On the **Active users** page, select the box next to the name of the user who you want to assign a license to.

3. On the right, in the **Product licenses** row, choose **Edit**.

4. In the **Product licenses** pane, switch the toggle to the **On** position for the license you want to assign to this user. By default, all services associated with that license are automatically assigned to the user.

    > [!TIP]
    > To limit which services are available to the user, switch the toggles to the **Off** position for the services that you want to remove for that user. For example, if you want the user to have access to all available services except Skype for Business Online, you can switch the toggle for the Skype for Business Online service to the **Off** position.
  
    ![Setting license assignments for a user.](../media/5e53a979-6b08-4981-bb0b-fa657146334b.png)
  
5. Switch the toggle to the **Off** position for licenses that this user no longer needs.

6. At the bottom of the **Product licenses** pane, choose **Assign** \> **Close** \> **Close**.

### Reassign licenses for multiple users at once

1. In the Admin center, go to the <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page, or choose **Users** \> **Active users**.

    If you're using Office 365 Germany, go to this <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.

    If you're using Office 365 operated by 21Vianet, go to this <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.

2. Select the boxes next to the names of the users who you want to replace existing licenses for.

3. In the **Bulk actions** pane, choose **Edit product licenses**.

4. In the **Assign products** pane, select **Replace existing product license assignments** \> **Next**.

5. Switch the toggle to the **On** position for the products you want to assign to these users.

    > [!TIP]
    > - To limit which services are available to the user, switch to toggles to the **Off** position for the services that you want to remove for that user. For example, if you want the user to have access to all available services except Skype for Business Online, you can switch the toggle for the Skype for Business Online service to the **Off** position.
    > - Any previous license assignments for the selected users will be removed.
  
    ![Setting license assignments for a user.](../media/5e53a979-6b08-4981-bb0b-fa657146334b.png)
  
6. At the bottom of the **Replace existing products** pane, select **Replace** \> **Close**.

## Step 5: Cancel subscriptions or remove licenses that you no longer need (Optional)

If you moved all users from one subscription to another, and you no longer need the original subscription, you can [cancel the subscription](../subscriptions-and-billing/cancel-your-subscription.md).
  
If you moved only some users to a different subscription, [remove licenses](../subscriptions-and-billing/remove-licenses-from-subscription.md) that you no longer need.
  
## Call support to help you switch plans

[Call support](../contact-support-for-business-products.md)