---
title: "Office 365 Reports in the admin center - OneDrive for Business usage"
ms.author: kaarins
author: kaarins
manager: pamgreen
audience: Admin
ms.topic: article
f1_keywords:
- 'o365p_reportsod4busage'
- 'O365M_ReportsOD4BUsage'
- 'O365E_ReportsOD4BUsage'
ms.service: o365-administration
localization_priority: Normal
ms.collection: 
- M365-subscription-management
- Adm_O365
- Adm_NonTOC
search.appverid:
- BCS160
- MET150
- MOE150
- GEA150
- ODB150
- ODB160
ms.assetid: 0de3b312-c4e8-4e4b-a02d-32b2f726a680
description: "Get the OneDrive for Business Usage Report to know about the total number of files and storage used across your organization. "
---

# Office 365 Reports in the admin center - OneDrive for Business usage

The Office 365 **Reports** dashboard shows you the activity overview across the products in your organization. It enables you to drill in to individual product level reports to give you more granular insight about the activities within each product. Check out [the Reports overview topic](activity-reports.md).
  
For example, the OneDrive card on the dashboard gives you a high-level view of the value you are getting from OneDrive for Business in terms of the total number of files and storage used across your organization. You can then drill into it to understand the trends of active OneDrive accounts, how many files are users interacting with as well as the storage used. It also gives you details for each user's OneDrive.
  
> [!NOTE]
> You must be a global administrator in Office 365 or an Exchange, SharePoint, Skype for Business administrator, or reports reader to see reports. 
  
## How do I get to the OneDrive Usage Report?

1. In the admin center, go to **Reports** > [Usage](https://go.microsoft.com/fwlink/p/?linkid=2074756).
    
2. From the **Select a report** drop-down, select **OneDrive** \> **Usage**. 
  
## Interpret the OneDrive usage report

You can get a view into OneDrive for Business usage by looking at the **Accounts**, **Files**, and **Storage** views. 
  
![OneDrive Usage Report](../media/49c5b93b-d081-436e-8992-236343a6d46b.png)
  
|||
|:-----|:-----|
|1.  <br/> |The **OneDrive usage** report shows trends over the last 7 days, 30 days, 90 days, or 180 days. However, if you click into a particular day in the report, the table (7) will show data for up to 28 days from the current date (not the date the report was generated).  <br/> |
|2.  <br/> |Each report has a date for when this report was generated. The reports usually reflect a 24 to 48 hour latency from time of activity.  <br/> NOTE: At times there may be unpredictable delays in data collection and processing which may delay report generation. The displayed report date is always reflective of the current date for which the system has processed report data. We strive to keep these within 24-48 hours from the time of activity.           |
|3.  <br/> |The **Accounts** view shows the trend in the number of total and active OneDrive accounts. "Active accounts" are any in which users view, modify, upload, download, share, or sync files.  <br/> |
|4.  <br/> |The **Files** view shows the number of number of total and active files. A file is considered active if it has been saved, synced, modified or shared within the specific time period.  <br/> NOTE: A file activity can occur multiple times for a single file, but will count only as one active file. For example, you can save and sync the same file multiple times over a specified time period, but it will count only as one single active file and one single synced file in the data.           |
|5.  <br/> |The **Storage** view shows the trend in the amount of OneDrive storage you're using.  <br/> > NOTE: The size includes any versions and metadata associated with the files.           |
|6.  <br/> | On the **Accounts** chart, the Y axis is the number of OneDrive accounts.  <br/>  On the **Files** chart, the Y axis is the number of files stored in OneDrive.  <br/>  On the **Storage** chart, the Y axis is the amount of OneDrive storage used.  <br/>  The X axis on all charts is the selected date range for this specific report.  <br/> |
|7.  <br/> |You can filter the series you see on the chart by clicking on an item in the legend. For example, on the **Files** chart, tap or click **Total files** or **Active files**. On the **Accounts** chart, tap or click **Total accounts** or **Active accounts**. Or on the **Storage** chart, tap or click **Storage used**. Changing your selection doesn't change the information in the table.  <br/> |
|8.  <br/> | The table shows you a breakdown of data for each user's OneDrive. To appear in the table, a user needs to have been assigned a product license that includes OneDrive, and they need to have SharePoint Online turned on. The user also needed to either sign in to the OneDrive sync client, or browse to their OneDrive using a web browser.  <br/>  If the OneDrive has had file activity, it will have the latest date that the file activity was performed. The rows in the table are sorted by **Last activity date** so the OneDrive with the most recent file activity appears at the top of the list.  <br/>  You can add or remove columns from the table.  <br/> ![Column options](../media/onedriveusage-columns.png)  <br/> **URL** is the web address for the user's OneDrive.  <br/> **Deleted** is the deletion status of the OneDrive. It takes at least 7 days for accounts to be marked as deleted.  <br/> **Owner** is the username of the primary administrator of the OneDrive.  <br/> **Owner principal name** is the email address of the owner of the OneDrive.  <br/> **Last activity date (UTC)** is the latest date a file activity was performed in the OneDrive. If the OneDrive has had no file activity, the value will be blank.  <br/> **Files** is the number of files in the OneDrive.  <br/> **Active files** is the number of active files within the time period. A file is considered active if it has been saved, synced, modified or shared within the selected time period.  <br/> NOTE: A file activity can occur multiple times for a single file, but will count only as one active file. For example, you can save and sync the same file multiple times over a specified time period, but it will count only as one single active file and one single synced file in the data. >  If files were removed during the specified time period for the report, the number of active files shown in the report may be larger than the current number of files in the OneDrive. >  Deleted users will continue to appear in reports for 180 days.<br/>**Storage used (MB)** is the amount of storage the OneDrive uses in MB. This includes any versions and metadata associated with the files.  <br/>  If your organization's policies prevent you from viewing reports where user information is identifiable, you can change the privacy setting for all these reports. Check out the **How do I hide user level details?** section in the [Activity Reports in the Microsoft 365 admin center Preview](activity-reports.md).  <br/> |
|9.  <br/> |Click or tap the **Manage columns** icon ![Manage Columns](../media/13d2e536-de88-4db3-80c7-7a3a57298eb4.png) to add or remove columns from the report.  <br/> |
|10.  <br/> |You can also export the report data into an Excel .csv file, by clicking or tapping the **Export** ![Export](../media/4dc548cc-8061-48d5-9240-6793affca43a.png) link. This exports the date for each OneDrive and allows you to do simple sorting and filtering for further analysis. If you have less than 2000 OneDrive accounts, you can sort and filter within the table in the report itself. If you have more than 2000 OneDrive accounts, you need to export the data to filter and sort.  <br/> NOTE: When the data is exported to an Excel file, note that the date the content report was generated is reflected in the file in the **Data as of** column.  <br/> |
|||
   

