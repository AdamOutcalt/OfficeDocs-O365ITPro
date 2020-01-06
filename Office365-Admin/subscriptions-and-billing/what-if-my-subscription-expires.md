---
title: "What happens to my data and access when my subscription ends?"
ms.author: cmcatee
author: cmcatee-MSFT
manager: mnirkhe
audience: Admin
ms.topic: article
f1_keywords:
- 'O365P_DataLifecycle'
- 'O365M_DataLifecycle'
- 'O365E_DataLifecycle'
ms.service: o365-administration
localization_priority: Normal
ms.collection: 
- M365-subscription-management
- Adm_O365
- Adm_TOC
- commerce
search.appverid:
- BCS160
- MET150
- MOE150
- BEA160
- GEA150
ms.assetid: 4436582f-211a-45ec-b72e-33647f97d8a3
description: "Learn what happens to your data when your Office 365 for business subscription expires, is disabled, or if you cancel."
---

# What happens to my data and access when my Office 365 for business subscription ends?

If your subscription ends—either because it expires, or because you decide to cancel—your access to Office 365 services, applications, and customer data go through multiple states before the subscription is fully turned off, or *deprovisioned*. If you are aware of this progression, you'll be better equipped to return your subscription to an active state before it's too late, or—if you're leaving Office 365—back up your data before it is ultimately deleted.
  
## Office 365 for business: Subscription lifecycle
- If your subscription expires, it goes through the following stages: Expired / Disabled / Deprovisioned. The Expired stage starts directly after the subscription has reached its end date.
- If you cancel the renewal of your annual subscription, it goes through the same stages as an expired subscription and the first stage starts at the anniversary of the annual subscription (not at the date of cancelling the subscription renewal).
- If you cancel your monthly subscription, it will be disabled immediately (at the date of cancellation). This means your users will lose access to the Office 365 assets immediately and only admins will have access to the data for the next 90 days.

The following table explains what you can expect when a paid Office 365 for business subscription expires.

| **Active**                                                             | **Expired <br/>(30 days\*)**                                                | **Disabled <br/>(90 days\*)**                                               | **Deprovisioned**                                                                         |
|------------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| *Data accessible to all*                                               | *Data accessible to all*                                                     | *Data accessible to admins only*                                             | **Data deleted<br/>Azure Active Directory is removed, if not in use by other services** |
| Users have normal access to Office 365, data, and Office applications  | Users have normal access to Office 365, files, and applications              | Users can't access Office 365, files, or applications                        | Users can't access Office 365, files, or applications                                     |
| Admins have normal access to Office 365, data, and Office applications | Admins can access the admin center                                           | Admins can access the admin center, but can't assign licenses to users       | Admins can access the admin center to purchase and manage other subscriptions             |
|                                                                        | Global or billing admins can reactivate the subscription in the admin center | Global or billing admins can reactivate the subscription in the admin center |                                                                                           |

*For most offers, in most countries and regions.
  
> [!NOTE]
> **What is "customer data"?** Customer data, as defined in the [Microsoft Online Service Terms](https://go.microsoft.com/fwlink/p/?LinkId=613649), refers to all data, including all text, sound, or image files that are provided to Microsoft by, or on behalf of, the customer through the customer's use of Office 365 services. To learn more about the protection of customer data, see the [Get started with the Microsoft Service Trust Portal](https://support.office.com/article/f30e2353-0bd6-41ed-8347-eea1fb8d2662).
  
## What are my options if my subscription is about to expire?

While a subscription is active, you and your end users have normal access to your data, services like email and OneDrive for Business, and Office applications. As the admin, you'll receive a series of notifications via email and in the admin center as your subscription nears its expiration date.
  
Before the subscription actually reaches its expiration date, you have a few options:

::: moniker range="o365-worldwide"
  
- **Enable recurring billing for the subscription.**

  - If **Recurring billing** is already turned on, you don't have to take any action. Your subscription will be automatically billed, and you'll be charged for an additional year or month, depending on your current payment frequency. If for any reason you've turned **Recurring billing** off, you can always [turn Recurring billing back on](renew-your-subscription.md).

  - If you purchased Office 365 Business with a prepaid card, you can [turn on Recurring billing](renew-your-subscription.md) for your subscription.

  - If you're an Open Volume Licensing customer with a prepaid, one-year subscription, contact your partner to purchase a new product key. You'll receive instructions via email to activate your key in the [Volume Licensing Service Center](https://go.microsoft.com/fwlink/p/?LinkID=282016). To learn how to find a new partner, or the partner you've worked with in the past, see [Find your Office 365 partner or reseller](../manage/find-your-partner-or-reseller.md).

  - If you have Office 365 Business, see [Manage recurring billing for your subscription](renew-your-subscription.md).

- **Let the subscription expire.**

  - If you're paying by credit card or invoice and you don't want to continue your subscription, [turn Recurring billing off](renew-your-subscription.md). Your subscription will expire on its expiration date, and you can ignore all related email notifications.

  - If you're an Open Volume Licensing customer working with a partner, you can let your subscription expire by taking no action.

  - If you're a Office 365 Small Business Premium customer, and you prepaid for Office 365 and activated it with a product key, you can let your subscription expire by taking no action.

- **Cancel before the subscription expires.** For details, see [Cancel your subscription](cancel-your-subscription.md).
  
::: moniker-end

::: moniker range="o365-germany"
  
- **Manage recurring billing for the subscription.**

  - If **Recurring billing** is already turned on, you don't have to take any action. Your subscription will be automatically billed, and you'll be charged for an additional year or month, depending on your current payment frequency. If for any reason you've turned **Recurring billing** off, you can always [turn Recurring billing back on](renew-your-subscription.md).

  - If you purchased Office 365 Business with a prepaid card, you can [turn on Recurring billing](renew-your-subscription.md) for your subscription.

  - If you're an Open Volume Licensing customer with a prepaid, one-year subscription, contact your partner to purchase a new product key. You'll receive instructions via email to activate your key in the [Volume Licensing Service Center](https://go.microsoft.com/fwlink/p/?LinkID=282016). To learn how to find a new partner, or the partner you've worked with in the past, see [Find your Office 365 partner or reseller](../manage/find-your-partner-or-reseller.md).

  - If you have Office 365 Business, see [Renew Office 365 for business](renew-your-subscription.md).

- **Let the subscription expire.**

  - If you're paying by credit card or invoice and you don't want to continue your subscription, [turn Recurring billing off](renew-your-subscription.md). Your subscription will expire on its expiration date, and you can ignore all related email notifications.

  - If you're an Open Volume Licensing customer working with a partner, you can let your subscription expire by taking no action.

  - If you're a Office 365 Small Business Premium customer, and you prepaid for Office 365 and activated it with a product key, you can let your subscription expire by taking no action.

- **Cancel before the subscription expires.** For details, see [Cancel your subscription](cancel-your-subscription.md).
  
::: moniker-end

::: moniker range="o365-21vianet"
  
- **Renew the subscription.** If **Recurring billing** is already turned on, you don't have to take any action. Your subscription will be automatically billed, and you'll be charged for an additional year or month, depending on your current payment frequency. If for any reason you've turned **Recurring billing** off, you can always [turn Recurring billing back on](renew-your-subscription.md).

- **Let the subscription expire.** If you're paying by credit card or invoice and you don't want to continue your subscription, [turn Recurring billing off](renew-your-subscription.md). Your subscription will expire on its expiration date, and you can ignore all related email notifications.

- **Cancel before the subscription expires.** For details, see [Cancel your subscription](cancel-your-subscription.md).

::: moniker-end

## What happens after my subscription expires?
If you let your subscription expire, it goes through multiple states before it is ultimately deleted. This gives you, as the admin, time to reactivate if you want to continue the service, or to back up your data if you decide you no longer want the subscription.
  
Here's what you can expect when your subscription is in each state.
  
### State: Expired
  
::: moniker range="o365-worldwide"

 **What to expect:** The expired state lasts for 30 days for most subscriptions, including subscriptions purchased through [Microsoft Open](https://go.microsoft.com/fwlink/p/?LinkID=613298), in most countries and regions. For Volume Licensing products, except for Microsoft Open, the expired state lasts 90 days.

::: moniker-end

::: moniker range="o365-germany"

 **What to expect:** The expired state lasts for 30 days for most subscriptions, including subscriptions purchased through [Microsoft Open](https://go.microsoft.com/fwlink/p/?LinkID=613298), in most countries and regions. For Volume Licensing products, except for Microsoft Open, the expired state lasts 90 days.

::: moniker-end

::: moniker range="o365-21vianet"

 **What to expect:** The expired state is 30 days for most subscriptions, in most countries and regions.

::: moniker-end

In this state, users have normal access to the Office 365 portal, Office applications, and services such as email and SharePoint Online.
  
As an admin, you still have access to the admin center. Don't worry—global or billing admins can [reactivate the subscription](reactivate-your-subscription.md) and continue using Office 365. If you don't reactivate, be sure to [back up your data](back-up-data-before-switching-plans.md).
  
### State: Disabled
  
::: moniker range="o365-worldwide"

 **What to expect:** If you don't reactivate your subscription while it is in the expired state, it moves into a disabled state, which lasts for 90 days for most subscriptions, in most countries and regions. For Volume Licensing products, the disabled state lasts 30 days.

::: moniker-end

::: moniker range="o365-germany"

 **What to expect:** If you don't reactivate your subscription while it is in the expired state, it moves into a disabled state, which lasts for 90 days for most subscriptions, in most countries and regions. For Volume Licensing products, the disabled state lasts 30 days.

::: moniker-end

::: moniker range="o365-21vianet"

 **What to expect:** If you don't reactivate your subscription while it is in the expired state, it moves into a disabled state, which is 90 days for most subscriptions, in most countries and regions.

::: moniker-end

::: moniker range="o365-worldwide"

In this state, your access decreases significantly. Your users can't sign in, or access services like email or SharePoint Online. Office applications eventually move into a read-only, reduced functionality mode and display [Unlicensed Product notifications](https://support.office.com/article/0d23d3c0-c19c-4b2f-9845-5344fedc4380.aspx). You can still sign in and get to the admin center, but can't assign licenses to users. Your customer data, including all user data, email, and files on team sites, is available only to you and other admins.

::: moniker-end

As a global or billing admin, you can [reactivate the subscription](reactivate-your-subscription.md) and continue using Office 365 with all of your customer data intact. If you choose not to reactivate, be sure to [back up your data](back-up-data-before-switching-plans.md).

### State: Deprovisioned
  
 **What to expect:** If you don't reactivate your subscription while it is in grace or disabled, the subscription is deprovisioned.
  
Admins and users no longer have access to the services or Office applications that came with the subscription. All customer data—from user data to documents and email—is permanently deleted and unable to be recovered in any way.
  
At this point, you can't reactivate the subscription. However, as a global or billing admin, you can still access the admin center to manage other subscriptions, or to buy new subscriptions to meet your business needs.
  
> [!NOTE]
> Adding a new subscription of the same type that has been deprovisioned does not restore the data that was associated with the deprovisioned subscription.

### What happens when my trial ends?

When your trial ends, you won't be able to continue using Office 365 for free. You have a few options:

::: moniker range="o365-worldwide"
- **Buy Office 365.** When your trial expires, it moves into a grace period, giving you another 30 days (for most trials, in most countries and regions) to purchase Office 365. To learn how to convert your trial into a paid subscription, see [Buy your trial version of Office 365 for business](buy-a-subscription-from-your-free-trial.md).

::: moniker-end

::: moniker range="o365-germany"
- **Buy Office 365.** When your trial expires, it moves into a grace period, giving you another 30 days (for most trials, in most countries and regions) to purchase Office 365. To learn how to convert your trial into a paid subscription, see [Buy your trial version of Office 365 for business](buy-a-subscription-from-your-free-trial.md).

::: moniker-end

::: moniker range="o365-21vianet"
- **Buy Office 365.** When your trial expires, it moves into a grace period, giving you another 30 days (for most trials, in most countries and regions) to purchase Office 365. To learn how to convert your trial into a paid subscription, see [Buy or try subscriptions for Office 365 operated by 21Vianet](../services-in-china/buy-or-try-subscriptions.md).

::: moniker-end

- **Extend your trial.** Need more time to evaluate Office 365? In certain cases, you may be able to [extend your trial](extend-your-trial.md).

- **Cancel the trial or let it expire.** If you decide not to buy Office 365, you can let your trial expire or [cancel it](cancel-your-subscription.md). Be sure to back up any data you want to keep. Soon after the 30 day grace period, your trial account information and data is permanently erased.

## What happens if I cancel a subscription?

If you cancel your subscription before its term end date, the subscription skips the expired state and moves directly into the disabled state, which is 90 days for most subscriptions, in most countries and regions. We recommend that you [back up your data](back-up-data-before-switching-plans.md) before canceling, but as an admin, you can still access and back up data for your organization while it is in the disabled state. Any customer data that you leave behind may be deleted after 90 days, and will be deleted no later than 180 days after cancellation.
  
Here's what to expect for you and your users if you cancel a subscription.
  
- **Admin access** Admins can still sign in and access the admin center, and buy other subscriptions as needed. As a global or billing admin, you have 90 days to [reactivate the subscription](reactivate-your-subscription.md) with all data intact.

- **User access** Your users won't be able to use services like OneDrive for Business, or access customer data—for example, email or documents on team sites. Office applications, like Word and Excel, will eventually move into a read-only, reduced functionality mode and display [Unlicensed Product notifications](https://support.office.com/article/0d23d3c0-c19c-4b2f-9845-5344fedc4380.aspx).

To learn how to cancel, see [Cancel your subscription](cancel-your-subscription.md).
  
> [!IMPORTANT]
> If you want your subscription data to be deleted before the typical Disabled period is over, you can request expedited deprovisioning. When you request expedited deprovisioning, your subscription data is deleted within 3 days of cancellation. To use expedited deprovisioning, [call support](../contact-support-for-business-products.md).

> [!NOTE]
> The information on this page is subject to the [Microsoft Policy Disclaimer and Change Notice](https://go.microsoft.com/fwlink/p/?LinkId=613651). Return to this site periodically to review any changes.
