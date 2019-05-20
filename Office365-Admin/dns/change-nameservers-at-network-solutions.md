---
title: "Change nameservers to set up Office 365 with Network Solutions"
ms.author: pebaum
author: pebaum
manager: mnirkhe
audience: Admin
ms.topic: get-started-article
f1_keywords:
- 'O365P_DOM_NetS1'
- 'O365M_DOM_NetS1'
- 'O365E_DOM_NetS1'
ms.service: o365-administration
localization_priority: Normal
ms.collection: 
- M365-subscription-management
- Adm_O365
- Adm_O365_Domain_Registrars
- Adm_O365_Setup
- Adm_UI_Elements
ms.custom:
- Adm_O365
- Adm_O365_FullSet
- Adm_O365_Setup
- Core_O365Admin_Migration
- MiniMaven
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: d4ba60f3-4e1c-4180-99bd-250b8955be2a
description: "Learn to set up your Office 365 custom domain with Network Solutions if you want Office 365 to manage your DNS records. "
---

# Change nameservers to set up Office 365 with Network Solutions

 **[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.
  
Follow these instructions if you want Office 365 to manage your Office 365 DNS records for you. (If you prefer, you can [manage all your Office 365 DNS records at Network Solutions](create-dns-records-at-network-solutions.md).)
  
    
## Add a TXT record at Network Solutions to verify that you own the domain

Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.
  
> [!NOTE]
> This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like. 
  
Follow the steps below or [watch the video (start at 0:47)](https://support.office.com/en-us/article/Video-Change-nameservers-to-set-up-Office-365-with-Network-Solutions-69b092e3-c026-4d19-a7d0-16cdb2d8b261?ui=en-US&amp;rs=en-US&amp;ad=US).
  
1. To get started, go to your domains page at Network Solutions by using [this link](https://www.networksolutions.com/manage-it). You'll be prompted to log in.
    
    > [!IMPORTANT]
    > Before you choose the **Login** button, first choose **Manage My Domain Names** in the **Log In to:** drop-down list.
  
    ![Choose Manage My Domain Names and log in to Network Solutions](../media/fda7d4a1-9445-4086-be9c-87c6983ef2aa.png)
  
2. Select the check box next to the name of the domain that you are modifying.
    
    ![Select the check box for your domain](../media/2c13d2ba-4a31-44da-812c-2cc90900a183.png)
  
3. Choose **Edit DNS**.
    
    ![Click Edit DNS](../media/9d7c269f-48d1-442c-9d7b-63bd384a36a9.png)
  
4. Choose **Manage Advanced DNS Records**.
    
    (You may have to scroll down.)
    
    ![Click Manage Advanced DNS Records](../media/fd2956d6-eec3-47ea-b60a-266bab14f51f.png)
  
5. Scroll down to the **Text (TXT Records)** section, and then choose **Edit TXT Records**.
    
    ![Click Edit TXT Records](../media/240a01d6-750a-4da6-8554-641b571e4b71.png)
  
6. In the boxes for the new record, type or copy and paste the values in the following table.
    
|**Host**|**TTL**|**Text**|
|:-----|:-----|:-----|
|@  <br/> (The system will change this value to **@ (None)** when you save the record.)  <br/> |3600  <br/> |MS=ms *XXXXXXXX*  <br/> **Note**: This is an example. Use your specific **Destination or Points to Address** value here, from the table in Office 365.           [How do I find this?](../get-help-with-domains/information-for-dns-records.md)
   
    
   ![Type or paste values in the boxes for the new record](../media/8a76daab-b6ff-4c82-ba68-192b24fbb934.png)
  
7. Choose **Continue**.
    
    ![Click Continue](../media/89e7fb38-b4d9-4949-a1bb-d0dd10b361e0.png)
  
8. Choose **Save Changes**.
    
    ![Click Save Changes](../media/bd4d7cd0-c8a3-497a-b080-cfd5a5c60dc5.png)
  
9. Wait a few minutes before you continue, so that the record you just created can update across the Internet.
    
Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.
  
When Office 365 finds the correct TXT record, your domain is verified.
  
1. Choose **Setup** \> **Domains**.
    
2. On the **Domains** page, choose the domain that you are verifying. 
    
    
  
3. On the **Setup** page, choose **Start setup**.
    
    
  
4. On the **Verify domain** page, choose **Verify**.
    
    
  
> [!NOTE]
>  Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md). 
  
## Change your domain's nameserver (NS) records

To complete setting up your domain with Office 365, you change your domain's NS records at your domain registrar to point to the Office 365 primary and secondary name servers. This sets up Office 365 to update the domain's DNS records for you. We'll add all records so that email, Skype for Business Online, and your public website work with your domain, and you'll be all set.
  
> [!CAUTION]
> When you change your domain's NS records to point to the Office 365 name servers, all the services that are currently associated with your domain are affected. For example, all email sent to your domain (like rob@ *your_domain*  .com) will start coming to Office 365 after you make this change.
  
Ready to change your NS records so Office 365 can set up your domain? Follow the steps below or [watch the video (start at 2:23)](https://support.office.com/en-us/article/Video-Change-nameservers-to-set-up-Office-365-with-Network-Solutions-69b092e3-c026-4d19-a7d0-16cdb2d8b261?ui=en-US&amp;rs=en-US&amp;ad=US).
  
> [!IMPORTANT]
>  When you have completed the steps in this section, the  *only*  nameservers that should be listed are these four: **ns1.bdm.microsoftonline.com**, **ns2.bdm.microsoftonline.com**, **ns3.bdm.microsoftonline.com**, and **ns4.bdm.microsoftonline.com**. The following procedure will show you how to delete any other, unwanted nameservers from the list, and also how to add the  *correct*  nameservers if they are not already in the list. 
  
1. To get started, go to your domains page at Network Solutions by using [this link](https://www.networksolutions.com/manage-it). You'll be prompted to log in.
    
    > [!IMPORTANT]
    > Before you choose the **Login** button, first choose **Manage My Domain Names** in the **Log In to:** drop-down list. 
  
    ![Choose Manage My Domain Names and log in to Network Solutions](../media/fda7d4a1-9445-4086-be9c-87c6983ef2aa.png)
  
2. Select the check box next to the name of the domain that you are modifying.
    
    ![Select the check box for your domain](../media/2c13d2ba-4a31-44da-812c-2cc90900a183.png)
  
3. Choose **Edit DNS**.
    
    ![Click Edit DNS](../media/9d7c269f-48d1-442c-9d7b-63bd384a36a9.png)
  
4. Choose **Move DNS**.
    
    ![NetworkSolutionsBP-Redelegate-1-1](../media/e57a30f3-63d5-4bcb-84c6-c8be21c261a2.png)
  
5. Depending on whether or not there are already nameservers listed on the page that is displayed now, continue to one of the two following procedures:
    
  - If there are **NO** nameservers already listed, [If there are NO nameservers already listed](#if-there-are-no-nameservers-already-listed).
    
  - If there **ARE** nameservers already listed, [If there ARE nameservers already listed](#if-there-are-nameservers-already-listed).
    
### If there are NO nameservers already listed

1. On the **Domains** page, in the **Specify Domain Name Servers** section, choose **Add More Name Servers**.
    
    ![NetworkSolutionsBP-Redelegate-1-2-1](../media/57e22ef1-ac88-4d4a-bc8e-058023255dfd.png)
  
2. On the **Domain Names** page, type or copy and paste the nameserver values from the following table. 
    
|||
|:-----|:-----|
|**Name Server 1** <br/> |ns1.bdm.microsoftonline.com  <br/> |
|**Name Server 2** <br/> |ns2.bdm.microsoftonline.com  <br/> |
|**Name Server 2** <br/> |ns3.bdm.microsoftonline.com  <br/> |
|**Name Server 2** <br/> |ns4.bdm.microsoftonline.com  <br/> |
   
    
![NetworkSolutionsBP-Redelegate-1-2-2](../media/795e8c6b-4828-4de2-b624-82f067bb2eb1.png)
  
3. Choose **Move DNS**.
    
    ![NetworkSolutionsBP-Redelegate-1-2-3](../media/d4a0a7c2-6868-471f-bbf4-16ce2e2348de.png)
  
4. Choose **Save Changes**.
    
    ![NetworkSolutionsBP-Redelegate-1-2-4](../media/897bc864-b340-4385-abeb-f94bc7f73e5e.png)
  
> [!NOTE]
> Your nameserver record updates may take up to several hours to update across the Internet's DNS system. Then your Office 365 email and other services will be all set to work with your domain. 
  
### If there ARE nameservers already listed

> [!CAUTION]
> Follow these steps  *only*  if you have existing nameservers other than the four  *correct*  nameservers. (That is, delete  *only*  any current nameservers that are  *not*  named **ns1.bdm.microsoftonline.com**, **ns2.bdm.microsoftonline.com**, **ns3.bdm.microsoftonline.com**, or **ns4.bdm.microsoftonline.com**.)
  
1. If there are any other nameservers listed, delete each one by selecting it and then pressing the **Delete** key on your keyboard.
    
    ![NetworkSolutions-BP-Redelegate-1-5](../media/eeb8ad22-bf4a-43a8-b97a-f09c3654d89b.png)
  
2. Choose **Add More Name Servers**.
    
    ![NetworkSolutionsBP-Redelegate-1-2-1](../media/57e22ef1-ac88-4d4a-bc8e-058023255dfd.png)
  
3. On the **Domain Names** page, type or copy and paste the nameserver values from the following table.  
    
|||
|:-----|:-----|
|**Name Server 1** <br/> |ns1.bdm.microsoftonline.com  <br/> |
|**Name Server 2** <br/> |ns2.bdm.microsoftonline.com  <br/> |
|**Name Server 3** <br/> |ns3.bdm.microsoftonline.com  <br/> |
|**Name Server 4** <br/> |ns4.bdm.microsoftonline.com  <br/> |
   
    
![NetworkSolutionsBP-Redelegate-1-2-2](../media/795e8c6b-4828-4de2-b624-82f067bb2eb1.png)
  
4. Choose **Move DNS**.
    
    ![NetworkSolutionsBP-Redelegate-1-2-3](../media/d4a0a7c2-6868-471f-bbf4-16ce2e2348de.png)
  
5. Choose **Save Changes.**
    
    ![NetworkSolutionsBP-Redelegate-1-2-4](../media/897bc864-b340-4385-abeb-f94bc7f73e5e.png)
  
> [!NOTE]
> Your nameserver record updates may take up to several hours to update across the Internet's DNS system. Then your Office 365 email and other services will be all set to work with your domain.