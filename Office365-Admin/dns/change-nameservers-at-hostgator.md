---
title: "Change nameservers to set up Office 365 with Hostgator"
ms.author: pebaum
author: pebaum
manager: mnirkhe
ms.date: 5/2/2018
ms.audience: Admin
ms.topic: get-started-article
f1_keywords:
- 'O365P_DOM_Hostgator1'
- 'O365M_DOM_Hostgator1'
- 'O365E_DOM_Hostgator1'
ms.service: o365-administration
localization_priority: Normal
ms.custom:
- Adm_O365
- Adm_O365_Setup
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: f3bd3c62-0477-48e4-b2b5-21e329d67985

description: "Learn how you can set up Office 365 to manage the DNS records of your custom domain at Hostgator."
---

# Change nameservers to set up Office 365 with Hostgator

 **[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for. 
  
Follow these instructions if you want Office 365 to manage your Office 365 DNS records for you. (If you prefer, you can [manage all your Office 365 DNS records at Hostgator](create-dns-records-at-hostgator.md).)
  
> [!IMPORTANT]
> You must perform the first procedure in the following list, [Point your domain to your hosting account.](change-nameservers-at-hostgator.md#BKMK_PointDomain), before you add DNS records by using any of the other procedures in this article. > (Need more help? [Still need help?](change-nameservers-at-hostgator.md#BKMK_NeedHelp).) 
  
- [Point your domain to your hosting account.](change-nameservers-at-hostgator.md#BKMK_PointDomain)
    
- [Add a TXT record for verification](change-nameservers-at-hostgator.md#BKMK_verify)
    
- [Change your domain's nameserver (NS) records](change-nameservers-at-hostgator.md#BKMK_nameservers)
    
## Point your domain to your hosting account.
<a name="BKMK_PointDomain"> </a>

> [!IMPORTANT]
> You must perform this procedure before you perform the procedure in the following section, **Add a TXT record for verification**. 
  
Follow these steps to associate your domain and hosting accounts.
  
1. To get started, go to your customer portal page at Hostgator by using [this link](https://portal.hostgator.com/domain/manage). You'll be prompted to log in.
    
    ![Hostgator-BP-Redelegate-1-0](../media/6749ac23-4832-4daf-8f3b-bc3b9b1b979c.png)
  
2. Choose the **Domains** tab. 
    
    ![Hostgator-BP-Redelegate-1-1](../media/56d12bfd-3549-4033-90dc-077c76ca798c.png)
  
3. On the **Manage Domains** page, in the **My Domains** area, choose the domain you want to update. 
    
    ![Hostgator-BP-Redelegate-1-2](../media/2c2f8530-26a1-4e62-bb04-b3874bc1cf36.png)
  
4. On the **Domains Overview** page, in the **Name Servers** area, choose **Change**.
    
    ![Hostgator-BP-Redelegate-1-3](../media/c8979d8a-ee96-4064-a8df-c5b01054cb16.png)
  
5. On the **Name Servers** page for your domain, in the **Select Hosting Account** drop-down list, select the **hosting account** that is associated with your domain. 
    
    ![Hostgator-BP-Redelegate-1-4](../media/4cf61060-1e8a-4758-9892-32059ffc90c2.png)
  
6. Choose **Save Name Servers**.
    
    ![Hostgator-BP-Redelegate-1-9](../media/b52a825a-6d54-49ba-87c8-52f770fdfa0c.png)
  
## Add a TXT record for verification
<a name="BKMK_verify"> </a>

> [!IMPORTANT]
> Before you perform this procedure, you must first perform the procedure in the first section of this article, [Point your domain to your hosting account.](change-nameservers-at-hostgator.md#BKMK_PointDomain). 
  
Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.
  
> [!NOTE]
> This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like. 
  
1. To get started, go to your cPanel page at Hostgator. You'll be prompted to log in first.
    
    (Each hosted account at Hostgator is assigned a unique cPanel address. Your cPanel address should look like this: https://YourSiteAddress:secure-port-number. The sign-up email you received from Hostgator will specify that address.)
    
    > [!IMPORTANT]
    > To have a cPanel associated with your domain, you need a hosting account with Hostgator. To get started with Office 365, you can either purchase a hosting account from Hostgator or [Change your domain's nameserver (NS) records](change-nameservers-at-hostgator.md#BKMK_nameservers) to point to Office 365. 
  
2. On the **Control Panel** page, in the **Domains** area, choose **Advanced DNS Zone Editor**.
    
    (You may have to scroll down.) 
    
3. On the **Advanced DNS Zone Editor** page, in the **Add a Record** area, in the boxes for the new record, type or copy and paste the values from the following table. 
    
    (Select the **Type** value from the drop-down list.) 
    
|||||
|:-----|:-----|:-----|:-----|
|**Name** <br/> |**TTL** <br/> |**Type** <br/> |**TXT Data** <br/> |
|Use your  *domain_name*  . (for example, fourthcoffee.com.)  <br/> **This value MUST end with a period (.)** <br/> |1  <br/> |TXT  <br/> |MS=ms *XXXXXXXX*  <br/> > [!NOTE]> This is an example. Use your specific **Destination or Points to Address** value here, from the table in Office 365. [How do I find this?](../get-help-with-domains/information-for-dns-records.md)          |
   
4. Choose **Add Record**.
    
5. Wait a few minutes before you continue, so that the record you just created can update across the Internet.
    
Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.
  
When Office 365 finds the correct TXT record, your domain is verified.
  
1. In the Office 365 admin center, choose **Setup** \> **Domains**.
    
2. On the **Domains** page, choose the domain that you are verifying. 
    
3. On the **Setup** page, choose **Start setup**.
    
4. On the **Verify domain** page, choose **Verify**.
    
> [!NOTE]
> Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records in Office 365](../get-help-with-domains/find-and-fix-issues.md). 
  
## Change your domain's nameserver (NS) records
<a name="BKMK_nameservers"> </a>

To complete setting up your domain with Office 365, you change your domain's NS records at your domain registrar to point to the Office 365 primary and secondary name servers. This sets up Office 365 to update the domain's DNS records for you. We'll add all records so that email, Skype for Business Online, and your public website work with your domain, and you'll be all set.
  
> [!CAUTION]
> When you change your domain's NS records to point to the Office 365 name servers, all the services that are currently associated with your domain are affected. For example, all email sent to your domain (like rob@ *your_domain*  .com) will start coming to Office 365 after you make this change. 
  
> [!IMPORTANT]
> The following procedure will show you how to delete any other, unwanted nameservers from the list, and also how to add the correct nameservers if they are not already listed. > When you have completed the steps in this section, the only nameservers that should be listed are these four: 
  
1. To get started, go to your customer portal page at Hostgator by using [this link](https://portal.hostgator.com/domain/manage). You'll be prompted to log in.
    
    ![Hostgator-BP-Redelegate-1-0](../media/6749ac23-4832-4daf-8f3b-bc3b9b1b979c.png)
  
2. Choose the **Domains** tab. 
    
    ![Hostgator-BP-Redelegate-1-1](../media/56d12bfd-3549-4033-90dc-077c76ca798c.png)
  
3. On the **Manage Domains** page, in the **My Domains** area, choose the domain you want to update. 
    
    ![Hostgator-BP-Redelegate-1-2](../media/2c2f8530-26a1-4e62-bb04-b3874bc1cf36.png)
  
4. On the **Domain Overview** page, in the **Name Servers** area, choose **Change**.
    
    ![Hostgator-BP-Redelegate-1-3](../media/c8979d8a-ee96-4064-a8df-c5b01054cb16.png)
  
5. On the **Name Servers** page for your domain, in the **Select Hosting Account** drop-down list, select the **hosting account** that is associated with your domain. 
    
    ![Hostgator-BP-Redelegate-1-4](../media/4cf61060-1e8a-4758-9892-32059ffc90c2.png)
  
6. Choose **Manually set my name servers**.
    
    ![Hostgator-BP-Redelegate-1-5](../media/5b73ae32-f26e-48aa-b5ad-6da20f1c491a.png)
  
7.     > [!CAUTION]
    > Follow these steps only if you have existing nameservers other than the four correct nameservers. (That is, delete only any current nameservers that are  *not*  named **ns1.bdm.microsoftonline.com**, **ns2.bdm.microsoftonline.com**, **ns3.bdm.microsoftonline.com**, or **ns4.bdm.microsoftonline.com**.) 
  
    Still on the **Name Servers** page for your domain, in the list of nameservers, delete each nameserver in the list by selecting it and then pressing the **Delete** key on your keyboard. 
    
    ![Hostgator-BP-Redelegate-1-6](../media/fa9820e7-28bb-4792-b16c-51e54d83feb1.png)
  
8. Still in the list of nameservers, type or copy and paste the first two values from the following table.
    
|||
|:-----|:-----|
|**Name Server 1:** <br/> |ns1.bdm.microsoftonline.com  <br/> |
|**Name Server 2:** <br/> |ns2.bdm.microsoftonline.com  <br/> |
|**Name Server 3:** <br/> |ns3.bdm.microsoftonline.com  <br/> |
|**Name Server 4:** <br/> |ns4.bdm.microsoftonline.com  <br/> |
   
    ![Hostgator-BP-Redelegate-1-7-1](../media/a8c10aa7-30b0-4bc8-9596-20256d396274.png)
  
9. Add the other nameserver values.
    
    Choose **(+)** add, and then type or copy and paste the value from the next row of the table into the box for the record. 
    
    Repeat this process until you have created all four nameserver records.
    
    ![Hostgator-BP-Redelegate-1-7-2](../media/92159a39-e498-4220-9b0d-ae2e718c7fb9.png)
  
10. Choose **Save Name Servers**.
    
    ![Hostgator-BP-Redelegate-1-8](../media/bd6b0dfa-5d39-4805-970d-7ab153cff117.png)
  
> [!NOTE]
> Your nameserver record updates may take up to several hours to update across the Internet's DNS system. Then your Office 365 email and other services will be all set to work with your domain. 
  
## Still need help?
<a name="BKMK_NeedHelp"> </a>

[![Get help from the Office 365 community forums](../media/12a746cc-184b-4288-908c-f718ce9c4ba5.png)](https://go.microsoft.com/fwlink/p/?LinkId=518605)
  
[![Admins: Sign in and create a service request](../media/10862798-181d-47a5-ae4f-3f8d5a2874d4.png)]( https://go.microsoft.com/fwlink/p/?LinkId=519124)
  
[![Admins: Call Support](../media/9f262e67-e8c9-4fc0-85c2-b3f4cfbc064e.png)](https://go.microsoft.com/fwlink/p/?LinkID=518322)
  

