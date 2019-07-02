---
title: "Change nameservers to set up Office 365 with MyDomain"
ms.author: pebaum
author: pebaum
manager: mnirkhe
audience: Admin
ms.topic: get-started-article
f1_keywords:
- 'O365P_DOM_MD1'
- 'O365M_DOM_MD1'
- 'O365E_DOM_MD1'
ms.service: o365-administration
localization_priority: Normal
ms.collection: 
- M365-subscription-management
- Adm_O365
- Adm_NonTOC
- Adm_O365_Setup
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: c5f6140a-4a12-401b-9bbd-7dfb0d6b0ba3
description: "Learn how you can set up Office 365 to manage the DNS records of your custom domain at MyDomain."
---

# Change nameservers to set up Office 365 with MyDomain

 **[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.
  
Follow these instructions if you want Office 365 to manage your Office 365 DNS records for you. (If you prefer, you can [manage all your Office 365 DNS records at MyDomain](create-dns-records-at-mydomain.md).)
  
## Add a TXT record for verification

Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.
  
> [!NOTE]
> This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like. 
  
1. To get started, go to your domains page at MyDomain by using [this link](https://www.mydomain.com/controlpanel). You'll be prompted to log in first.
    
2. In the **My Favorites** section, choose **Domain Central**.
    
3. Under **Domain**, choose the name of the domain that you want to edit.
    
4. In the **Overview** row, choose **DNS**.
    
5. From the **Modify** drop-down list, choose **TXT/SPF Record**.
    
6. Under **Content**, in the box for the new record, type or copy and paste the value from the following table.
    
||
|:-----|
|**Content** <br/> |
|MS=ms *XXXXXXXX*  <br/> **Note**: This is an example. Use your specific **Destination or Points to Address** value here, from the table in Office 365. [How do I find this?](../get-help-with-domains/information-for-dns-records.md)          |
   
7. Choose **Add**.
    
8. Wait a few minutes before you continue, so that the record you just created can update across the Internet.
    
Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.
  
When Office 365 finds the correct TXT record, your domain is verified.
  
1. In the Microsoft 365 admin center, choose **Setup** \> **Domains**.
    
2. On the **Domains** page, choose the domain that you are verifying. 
    
3. On the **Setup** page, choose **Start setup**.
    
4. On the **Verify domain** page, choose **Verify**.
    
> [!NOTE]
> Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records in Office 365](../get-help-with-domains/find-and-fix-issues.md). 
  
## Change your domain's nameserver (NS) records

To complete setting up your domain with Office 365, you change your domain's NS records at your domain registrar to point to the Office 365 primary and secondary name servers. This sets up Office 365 to update the domain's DNS records for you. We'll add all records so that email, Skype for Business Online, and your public website work with your domain, and you'll be all set.
  
> [!CAUTION]
> When you change your domain's NS records to point to the Office 365 name servers, all the services that are currently associated with your domain are affected. For example, all email sent to your domain (like rob@ *your_domain.* com) will start coming to Office 365 after you make this change. 
  
> [!IMPORTANT]
> The following procedure will show you how to delete any other, unwanted nameservers from the list, and also how to add the correct nameservers if they are not already in the list. <br/> When you have completed the steps in this section, the only nameservers that should be listed are these four:
  
1. To get started, go to your domains page at MyDomain by using [this link](https://www.mydomain.com/controlpanel). You'll be prompted to log in first.
    
2. In the **My Favorites** section, choose **Domain Central**.
    
3. Under **Domain**, choose the name of the domain that you want to edit.
    
4. In the **Overview** row, choose **Nameservers**.
    
    ![MyDomain-BP-Redelegate-1-1](../media/49e91235-44b5-46d6-a82e-8f11329db3d6.png)
  
5. In the **Update Name Servers** section, select **Use different name servers**.
    
    ![MyDomain-BP-Redelegate-1-2-1](../media/f869fb26-54dc-4b66-8378-a78a79b582bd.png)
  
6. Depending on whether or not there are already nameservers listed on the page that is displayed now, continue to one of the two following procedures.
    
### If the correct nameservers ARE already listed

- If the correct nameservers are already listed, you can skip this step.
    
    ![MyDomain-BP-Redelegate-1-2-2](../media/601f6a46-15bd-4a92-b792-ac628ff86628.png)
  
### If the correct nameservers are NOT already listed

> [!CAUTION]
> Follow these steps only if you have existing nameservers other than the four correct nameservers. (That is, delete only any current nameservers that are  *not*  named **ns1.bdm.microsoftonline.com**, **ns2.bdm.microsoftonline.com**, **ns3.bdm.microsoftonline.com**, or **ns4.bdm.microsoftonline.com**.) 
  
1. Delete the existing nameservers by selecting each entry in the **Nameserver:** field, and then pressing the **Delete** key on your keyboard. 
    
    ![MyDomain-BP-Redelegate-1-3-1](../media/5024cd27-a2b1-42a2-99e4-5ceb5e6eddb9.png)
  
2. Choose **Add More** twice to add two new Nameserver rows. 
    
    ![MyDomain-BP-Redelegate-1-3-2](../media/19307893-2f73-4e4d-9221-a5870e09ab48.png)
  
3. In the boxes for the records, type or copy and paste the nameserver values from the following table.
    
|||
|:-----|:-----|
|**Nameserver 1** <br/> |ns1.bdm.microsoftonline.com  <br/> |
|**Nameserver 2** <br/> |ns2.bdm.microsoftonline.com  <br/> |
|**Nameserver 3** <br/> |ns3.bdm.microsoftonline.com  <br/> |
|**Nameserver 4** <br/> |ns4.bdm.microsoftonline.com  <br/> |
   
   ![MyDomain-BP-Redelegate-1-4](../media/7427e99c-49c7-4a2e-a5bf-66fc46900cd1.png)
  
4. Choose **Save**.
    
    ![MyDomain-BP-Redelegate-1-5](../media/48473816-b881-47f0-9344-74622efa3bf8.png)
  
> [!NOTE]
> Your nameserver record updates may take up to several hours to update across the Internet's DNS system. Then your Office 365 email and other services will be all set to work with your domain. 
