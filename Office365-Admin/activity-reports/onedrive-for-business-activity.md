---
title: "Office 365 Reports in the admin center - OneDrive for Business activity"
ms.author: kaarins
author: kaarins
manager: pamgreen
ms.audience: Admin
ms.topic: article
f1_keywords:
- 'O365E_ReportsODActivity'
ms.service: o365-administration
localization_priority: Normal
ms.collection: 
- M365-subscription-management
- IT_OneDriveAdmin
- IT_OneDriveAdmin_Top
- Strat_OD_admin
ms.custom:
- Core_O365Admin_Migration
- MiniMaven
- Strat_OD_admin
search.appverid:
- BCS160
- MET150
- MOE150
- GEA150
- ODB150
- ODB160
ms.assetid: 8bbe4bf8-221b-46d6-99a5-2fb3c8ef9353
description: "Get the OneDrive usage report for your organization and know the activity of every OneDrive user, the number of files shared, and the storage utilization."
---

# Office 365 Reports in the admin center - OneDrive for Business activity

The Office 365 **Reports** dashboard shows you the activity overview across the products in your organization. It lets you drill in to individual product level reports to give you more granular insight about the activities within each product. Check out [the Reports overview topic](activity-reports.md).
  
For example, you can understand the activity of every user licensed to use OneDrive by looking at their interaction with files on OneDrive. It also helps you to understand the level of collaboration going on by looking at the number of files shared.
  
> [!NOTE]
> Some functionality is introduced gradually. This means that you may not yet see this feature or it may look different than what is described in the help articles. But don't worry - it's coming soon! 
  
If you want to understand the amount of activity happening against each OneDrive account and the storage utilization, you can view the [OneDrive usage report](onedrive-for-business-usage.md).
  
> [!NOTE]
> You must be a global administrator in Office 365 or an Exchange, SharePoint, Skype for Business administrator, or reports reader to see reports. 
  
## How do I get to the OneDrive Activity report?

1. In the Microsoft 365 admin center, select **Reports** and then **Usage** from the left menu or click on the **Reports** widget.<br/>![Check out new activity reports](../media/2554deff-b840-4aa5-b2b2-83683996fedc.png)
  
2. Use the **Select a report** drop-drop at the top left and select **OneDrive activity**.<br/>![Select a report](../media/fb7bb8ea-eeb7-48c9-b739-601f41ddee16.png)
  
## Interpret the OneDrive for Business activity report

You can get a view into OneDrive for Business activity by looking at the **Files** and **Users** views. 
  
![OneDrive Activity Report](../media/316b2a03-8e42-447c-aae8-080813eebe84.png)
  
|||
|:-----|:-----|
|1.  <br/> |The **OneDrive for Business activity** report can be viewed for trends over the last 7 days, 30 days, 90 days, or 180 days. However, if you click into a particular day in the report, the table (7) will show data for up to 28 days from the current date (not the date the report was generated).  <br/> |
|2.  <br/> |Each report has a date for when this report was generated. The reports usually reflect a 24 to 48 hour latency from time of activity.  <br/> > [!NOTE]> At times there may be unpredictable delays in data collection and processing which may delay report generation. The displayed report date is always reflective of the current date for which the system has processed report data. We strive to keep these within 24-48 hours from the time of activity.           |
|3.  <br/> |The **Files** view helps you to understand the unique number of licensed users that performed file interactions against any OneDrive account.  <br/> |
|4.  <br/> |The **Users** view helps you to understand the trend in the number of active OneDrive users. A user is considered active if he or she has executed a file activity (save, sync, modify, or share) within the specified time period.  <br/> NOTE: A file activity can occur multiple times for a single file, but will only count as one active file. For example, you can save and sync the same file multiple times over a specified time period, but it will only count as one single active file and one single synced file in the data.           |
|5.  <br/> | On the **Files** chart, the Y axis is the number of unique files that any user either saved, synced, modified, or shared.  <br/>  On the **Users** chart, the Y axis is the number of unique users that performed file interactions (save, sync, modify, or share) on any OneDrive account.  <br/>  The X axis on all charts is the selected date range for this specific report.  <br/> |
|6.  <br/> |You can filter the series you see on the chart by clicking on an item in the legend. For example, on the **Files** chart, click or tap **Active** or **Synced**![OneDrive for Business Activity Report chart legend](../media/25765cf9-6e07-4ce3-951b-b46cda92c1c2.png) to see only the information related to each one. Changing this selection doesn't change the information in the grid table.  <br/> |
|7.  <br/> | The table shows you a breakdown of data at the per-user level. You can add or remove columns from the table.  <br/> ![OneDrive for Business Activity report columns](../media/849eac88-1816-40f7-85fc-e655698ed5dc.png)  <br/>  **User name** is the user name of the owner of the OneDrive account.  <br/> **Last activity date (UTC)** is the latest date a file activity was performed on the OneDrive account for the selected date range. To see activity that occurred on a specific date, select the date directly in the chart.  <br/> ![Select a specific date in the chart](../media/29e54c4b-8dc2-4ed8-9367-1f66f2988fac.png)  <br/>  This will filter the table to display file activity data only for users who performed the activity on that specific day.  <br/> **Files viewed or edited** is the number of files that the user uploaded, downloaded, modified, or viewed.  <br/> **Files synced** is the number of files that have been synced from a user's local device to the OneDrive account.  <br/> **Files shared internally** is the number of files that have been shared with users within the organization, or with users within groups (that might include external users).  <br/> **Files shared externally** is the number of files that have been shared with users outside of the organization.  <br/> **Deleted** indicates that the user's license was removed.  <br/> NOTE: Activity for a deleted user will still display in a report as long as he or she was licensed at some time during the selected time period. The **Deleted** column helps you to note that the user may no longer be active, but contributed to the data in the report.<br/>**Deleted date** is the date on which the user's license was removed.  <br/> **Product assigned** are the Office 365 products that are licensed to the user.  <br/>  If your organization's policies prevent you from viewing reports where user information is identifiable, you can change the privacy setting for all these reports. Check out the **How do I hide user level details?** section in the [Activity Reports in the Microsoft 365 admin center](activity-reports.md).  <br/> |
|8.  <br/> |Click or tap the **Manage columns** icon ![Manage Columns](../media/13d2e536-de88-4db3-80c7-7a3a57298eb4.png) to add or remove columns from the report.  <br/> |
|9.  <br/> |You can also export the report data into an Excel .csv file, by clicking or tapping the **Export** ![Export](../media/b5d12006-a2b4-4db5-af41-40f9e7aec07f.png) link. This exports data of all users and enables you to do simple sorting and filtering for further analysis. If you have less than 2000 users, you can sort and filter within the table in the report itself. If you have more than 2000 users, in order to filter and sort, you will need to export the data.  <br/> |
|||
   

