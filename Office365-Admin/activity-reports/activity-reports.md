---
title: "Activity Reports in the Microsoft 365 admin center"
ms.author: kwekua
author: kwekua
manager: scotv
audience: Admin
ms.topic: overview
f1_keywords:
- 'O365P_ReportsUsageOverview'
- 'O365M_ReportsYammerActivity'
- 'O365M_ReportsUsageOverview'
- 'O365E_ReportsYammerActivity'
- 'O365E_ReportsUsageOverview'
- 'O365M_ReportsUsageOverview'
- 'O365P_ReportsUsageOverview'
ms.service: o365-administration
localization_priority: Normal
ms.collection: 
- M365-subscription-management
- Adm_O365
- Adm_TOC
search.appverid:
- MET150
- MOE150
- GEA150
ms.assetid: 0d6dfb17-8582-4172-a9a9-aed798150263
description: "Get a periodic report of how people in your organization are using Office 365 services. Usage Overview dashboard lets you drill into each chart for more insights."
---

# Activity Reports in the Microsoft 365 admin center

You can easily see how people in your business are using Office 365 services. For example, you can identify who is using a service a lot and reaching quotas, or who may not need an Office 365 license at all.
  
Reports are available for the last 7 days, 30 days, 90 days, and 180 days. Data won't exist for all reporting periods right away. The reports become available within 48 hours.
  
Watch this video for on overview: on how you can use the reports:
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/fb726f8e-aead-43b2-ba0f-53ba5b886bf7?autoplay=false]
  
## How to get to the Reports dashboard

::: moniker range="o365-worldwide"

1. In the admin center, go to the **Reports** \>  [Usage](https://go.microsoft.com/fwlink/p/?linkid=2074756) page.

::: moniker-end

::: moniker range="o365-germany"

1. Go to the [365 admin center](https://portal.office.de/adminportal/home) and choose **Reports** \> **Usage**.

::: moniker-end

::: moniker range="o365-21vianet"

1. Go to the [365 admin center](https://login.partner.microsoftonline.cn) and choose **Reports** \> **Usage**.

::: moniker-end

   
2. Choose **Select a report** at the top of the dashboard to select from a list of all available reports. Or, click an at-a-glance activity widget for a service (email, OneDrive, etc) to see more information. <br/>![The Office 365 Usage dashboard](../media/usage-report-dashboard.png)
  
## Who can see reports

People who have the following permissions:
  
- Office 365 global admins: We recommend that only a few people in your company have this role. It reduces the risk to your business.
    
- Exchange admins
    
- SharePoint admins
    
- Skype for Business admins
    
- Reports reader
    
To learn more, see [About Office 365 admin roles](../add-users/about-admin-roles.md) and [Assign admin roles in Office 365](../add-users/assign-admin-roles.md).
  
## Which activity reports are available in the admin center

Depending on your Office 365 subscription, here are the available reports.
  
- [Email activity](email-activity.md)
    
- [Mailbox usage](mailbox-usage.md)
    
- [Office activations](microsoft-office-activations.md)

- [Active Users](active-users.md)
  
- [Email apps usage](email-apps-usage.md)
  
- [Office 365 groups](office-365-groups.md)
  
- [OneDrive for Business user activity](onedrive-for-business-activity.md)
  
- [OneDrive for Business usage](onedrive-for-business-usage.md)
  
- [SharePoint site usage](sharepoint-site-usage.md)
  
- [SharePoint activity](sharepoint-activity.md)
  
- [Skype for Business Online activity](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online-reporting/activity-report)
  
- [Skype for Business Online conference organized activity](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online-reporting/conference-organizer-activity-report)
  
- [Skype for Business Online conference participant activity](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online-reporting/conference-participant-activity-report)
  
- [Skype for Business Online peer-to-peer activity](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online-reporting/peer-to-peer-activity-report)
  
::: moniker range="o365-worldwide"

- [Yammer activity](yammer-activity-report.md)

::: moniker-end

::: moniker range="o365-worldwide"

- [Yammer device usage](yammer-device-usage-report.md)

::: moniker-end

::: moniker range="o365-worldwide"

- [Yammer groups activity report](yammer-groups-activity-report.md)

::: moniker-end

::: moniker range="o365-worldwide"

- [Microsoft Teams user activity](microsoft-teams-user-activity.md)

::: moniker-end

::: moniker range="o365-worldwide"

- [Microsoft Teams device usage](microsoft-teams-device-usage.md)

::: moniker-end

## How to view licensing information

- To see how many licenses you have assigned and unassigned, in the admin center, go to **Billing** \> [Licenses](https://go.microsoft.com/fwlink/p/?linkid=842264).
    
- To see who is licensed, unlicensed, or guest, in the admin center, go to **Users** \> [Active users](https://go.microsoft.com/fwlink/p/?linkid=834822). Use the **Filter** menu to filter your list.
  
## How to view usage information for a specific user

Use the service reports to research how much a specific user is using the service. For example, to find out how much mailbox storage a specific user has consumed, open the Mailbox usage report, and sort the users by name. If you have thousands of users, export the report to Excel so you filter through the list quickly.
  
You can't generate a report where you enter a user's account and then get a list which services they are using and how much.
  
## Hide user details in the reports

If you want to hide user level information when you're generating your reports, you can quickly make that change in the admin center.
  
1. In the admin center, go to **Settings** \> **Services &amp; add-ins**. 
  
2. Select **Reports**. 
  
3. In the **Reports** pane, select the options you want, and then choose **Save changes**.
  
Your user list will look like this:
  
![Office 365 reports - anonymized user list](../media/2ed99bce-4978-4ee3-9ea2-4a8db26eef02.png)
  
It'll take a few minutes for these changes to take effect on the reports in the reports dashboard. This setting also applies to the reports API.
  
## What happens to usage data when a user account is closed?

Whenever you close a user's account, Microsoft will delete that user's usage data within 30 days. That user will still be included in the Activity chart totals (see number 1) for the periods she was active in, but will not appear in the User Details table (see number 2).
  
However, when you select a particular day (see number 3), up to 28 days from the current date, the report show the user's usage for that day in the User Details table (see number 2).
  
## Related Topics

[Reports in the Office 365 Security &amp; Compliance Center](https://support.office.com/article/7acd33ce-1ec8-49fb-b625-43bac7b58c5a)
  

