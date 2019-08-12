---
title: "Manage licenses for devices"
ms.author: cmcatee
author: cmcatee-MSFT
manager: mnirkhe
ms.audience: Admin
ms.topic: article
f1_keywords:
- 'MACBillingLicensesOPPDevicesLDP'
ms.service: o365-administration
localization_priority: Normal
ms.collection: 
- M365-subscription-management
- Adm_O365
- Adm_TOC
- commerce
description: "Learn how to assign licenses to groups for use with devices."
---
# Manage licenses for devices

If you have Office 365 ProPlus for Education (device), you can assign licenses to devices by using Azure AD groups. When a device has a license, anyone who uses that device can use Office 365. For example, let’s say you have 20 laptops and tablets that are used by people in your organization. When you assign a license to each device, each person who logs in to one of the devices uses Office 365 without the need for their own license. After they log out of the device, the license stays associated with the device. The next time someone logs in to the same device, they can also use the device without the need for their own license.

> [!IMPORTANT]
> Office 365 ProPlus for Education (device) is only available to Education A3 and A5 volume licensing customers.

To begin, you create a group in the Azure Active Directory admin center, and then assign devices to the group. To learn more about device licensing, including device requirements, what types of groups you can use, and how to configure Office 365 ProPlus to use device licensing, see [Device licensing for Office 365 ProPlus for Education customers](https://go.microsoft.com/fwlink/p/?linkid=2094216).

> [!IMPORTANT]
> You must be a Global admin to complete the tasks in this article.

## Assign licenses to devices

When you assign licenses to a group, you assign licenses to all devices within the group. You can only assign one subscription to any single group.

1. In the Microsoft 365 admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licenses</a> page.
2. On the **Licenses** page, choose **Office 365 ProPlus for Education (device)**.
3. On the **Office 365 ProPlus for Education (device)** page, choose a subscription, then choose **Assign licenses**.
4. In the **Assign licenses to a group** pane, begin typing a group name, and then choose it from the results to add it to the list.
6. Choose **Assign**, then choose **Close**.

## Unassign licenses from devices

When you unassign licenses from a group, you remove the licenses from all devices within the group. All apps and their associated data are then read-only.

1. In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licenses</a> page.
2. On the **Licenses** page, choose **Office 365 ProPlus for Education (device)**.
3. On the **Office 365 ProPlus for Education (device)** page, choose a subscription, choose **More actions**, then choose **Unassign licenses**.
5. In the **Unassign licenses** dialog box, choose **Unassign**.