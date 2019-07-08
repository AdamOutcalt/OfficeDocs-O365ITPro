---
title: "Troubleshooting Microsoft 365 usage analytics"
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: troubleshooting
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
ms.assetid: a73632a1-62c8-4a13-8115-913773b30f93
description: "Learn how to troubleshoot issues with the Office 365 Adoption content pack."
---

# Troubleshooting Microsoft 365 usage analytics

Explore the following list of error messages to get help with the most common issues with Microsoft 365 usage analytics.
  
    
## We are unable to process your request. You have to first subscribe to this data from the Microsoft 365 admin center

 **Error Code :** 422 
  
 **Where you will see this message:** In Power BI when you are connecting to the Office 365 Adoption public preview content pack or when directly calling the Office 365 Reporting APIs. 
  
 **Cause:** Before you can connect to the content pack you have to subscribe to the data from the Microsoft 365 admin center. If this step isn't done first, you won't be able to connect to the content pack, even if you provide your Office 365 tenant id. 
  
 **To fix this error:** To subscribe to the data, go to the admin center \> **Reports** \> **Usage** and locate the Office 365 Adoption tile on the main dashboard page. Select the **Get started** button and then in the **Reports** pane that opens, turn the **Make data available to the Office 365 Adoption content pack for Power BI** setting on and **Save**.
  
## We are processing your data

 **Where you will see this message:** In the **Office 365 Adoption** tile on the **Usage** dashboard in the Microsoft 365 admin center. 
  
 **Cause:** When you [opt in to seeing data in the content pack](enable-usage-analytics.md) from the Microsoft 365 admin center, the Office 365 system starts generating historical usage data for your organization. Depending on the size of your tenant, this step could take anywhere between 2 hours to 48 hours. 
  
 **To fix this:** Just be patient, but if the message does not change to **Your data is ready** after 3 days, [contact Office 365 for business support](../contact-support-for-business-products.md).
  
## We are unable to process your request at this time. We are still preparing the data for your organization

 **Error Code:** 423 
  
 **Where you will see this message:** In Power BI when you are connecting to the Office 365 Adoption public preview content pack or when directly calling the Office 365 Reporting APIs. 
  
 **Cause:** When you [opt in to seeing data in the content pack](enable-usage-analytics.md) from the admin center, the Office 365 system starts generating historical usage data for your organization. Depending on the size of your tenant, this step could take anywhere between 2 hours to 48 hours. 
  
 **To fix this:** Just be patient, but if the message does not change to **Your data is ready** even 3 days since initiation, [contact Office 365 for business support](../contact-support-for-business-products.md).
  
## The tenant ID you provided is not in the correct format

 **Error Code:** 400 
  
 **Where you will see this message:** In Power BI when you are connecting to the Office 365 Adoption public preview content pack or when directly calling the Office 365 Reporting APIs. 
  
 **Cause:** The tenant id is a guid and has to be in the format of xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. If you enter any other string in the tenant input box you will get this error. 
  
 **To fix this error:** Go to the admin center \> **Reports** \> **Usage** and locate the Office 365 Adoption tile on the main dashboard page. The tenant id is listed on the tile. You can copy it from here and paste it in the dialog box for connecting to the content pack. 
  
## The tenant ID you provided is not recognized by our system

 **Error Code:** 404 
  
 **Where you will see this message:** In Power BI when you are connecting to the Office 365 Adoption public preview content pack or when directly calling the Office 365 Reporting APIs. 
  
 **Cause:** The tenant id you provided is not valid or does not exist. 
  
 **To fix this error:** Go to the admin center \> **Reports** \> **Usage** and locate the Office 365 Adoption tile on the main dashboard page. The tenant id is listed on the tile. You can copy it from here and paste it in the dialog box for connecting to the content pack. 
  
## Please re-enter your credentials to sign in to Power BI again

Error Code: 302
  
 **Where you will see this message:** In Power BI when you are connecting to the Office 365 Adoption public preview content pack or when directly calling the Office 365 Reporting APIs. 
  
 **Cause:** The authorization code failed and may require you to enter your credentials again. 
  
 **To fix this error:** Sign out of Power BI, and then sign in again. 
  
## You do not have the right authorization to access to this data. To be able to gain access to the data from this service you need to be either a global admin or any one of the product admins

 **Error Code:** 403 
  
 **Where you will see this message:** In Power BI when you are connecting to the Office 365 Adoption public preview content pack or when directly calling the Office 365 Reporting APIs. 
  
 **Cause:** The authorization code failed because the user who tried connecting to the content pack does not have the right level of authorization to access this data. 
  
 **To fix this error:** Provide the credentials of a user who is either a **global administrator**, **Exchange administrator**, **Skype for Business administrator,** or a **SharePoint administrator** to connect to the content pack. See [Office 365 admin roles](../add-users/about-admin-roles.md) for more information. 
  
## Refresh failed

 **Where you will see this message:** Email from Power BI or failed status in the refresh history. 
  
 **Cause:** Sometimes the credentials of the user who connected to the content pack are reset, and not updated in the connection settings of the content pack causing the user to see refresh failure errors. 
  
 **To fix this error:** In Power BI, find the dataset corresponding to the Office 365 Adoption dashboard (Office 365 Adoption_preview.pbix) , choose **schedule refresh** and provide your Office 365 admin credentials. 
  
If that doesn't work, clear the cache, and re-create the content pack.
  
## Failed to update data source credentials

 **Error Code:** 400 
  
 **Where you will see this message:** In Power BI when you are connecting to the Office 365 Adoption public preview content pack. 
  
 **Cause:** Some users who have multi-factor authentication (MFA) enforced may see a 400 error when connecting to the content pack. This is currently a known issue and only impacts the connection flow. 
  
 **To fix this:** Connect with credentials that are not MFA enforced. 
  
A global admin can turn MFA on or off, for instructions, see [Set up multi-factor authentication for Office 365 users](../security-and-compliance/set-up-multi-factor-authentication.md).
  