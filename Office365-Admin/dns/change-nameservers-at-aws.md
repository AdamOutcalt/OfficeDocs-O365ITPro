---
title: "Change nameservers to set up Office 365 with Amazon Web Services (AWS)"
ms.author: pebaum
author: pebaum
manager: mnirkhe
ms.date: 5/2/2018
ms.audience: Admin
ms.topic: get-started-article
f1_keywords:
- 'O365P_DOM_AWS1'
- 'O365M_DOM_AWS1'
- 'O365E_DOM_AWS1'
ms.service: o365-administration
localization_priority: Normal
ms.custom:
- Adm_O365
- Adm_O365_Setup
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 0ddbe33c-81ea-4c02-8db9-e71d3810c0ec

description: "Learn how you can set up Office 365 to manage your DNS records at Amazon Web Services (AWS). "
---

# Change nameservers to set up Office 365 with Amazon Web Services (AWS)

 **[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for. 
  
Follow these instructions if you want Office 365 to manage your Office 365 DNS records for you. (If you prefer, you can [manage all your Office 365 DNS records at AWS](create-dns-records-at-aws.md).)
  
Here's what you need to do.
  
- [Add a TXT record for verification](change-nameservers-at-aws.md#BKMK_verify)
    
- [Change your domain's nameserver (NS) records](change-nameservers-at-aws.md#BKMK_nameservers)
    
## Add a TXT record for verification
<a name="BKMK_verify"> </a>

Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.
  
> [!NOTE]
> This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like. 
  
1. To get started, go to your domains page at AWS by using [this link](https://console.aws.amazon.com/route53/home). You'll be prompted to log in first.
    
2. On the **Resources** page, choose **Hosted Zones**.
    
3. On the **Hosted Zones** page, in the **Domain Name** column, choose the name of the domain that you want to edit. 
    
4. Choose **Create Record Set**.
    
5. In the **Create Record Set** area, in the boxes for the new record, type or copy and paste the values from the following table. 
    
    (Choose the **Type** and **Routing Policy** values from the drop-down lists.) 
    
    > [!TIP]
    > The quotation marks required by the onscreen instructions are supplied automatically. You don't need to type them manually. 
  
|||||||
|:-----|:-----|:-----|:-----|:-----|:-----|
|**Name** <br/> |**Type** <br/> |**Alias** <br/> |**TTL (Seconds)** <br/> |**Value** <br/> |**Routing Policy** <br/> |
|(Leave this field empty)  <br/> |TXT - Text  <br/> |No  <br/> |300  <br/> |MS=ms *XXXXXXXX*  <br/> > [!NOTE]> This is an example. Use your specific **Destination or Points to Address** value here, from the table in Office 365. [How do I find this?](../get-help-with-domains/information-for-dns-records.md)          |Simple  <br/> |
   
6. Choose **Create**.
    
7. Wait a few minutes before you continue, so that the record you just created can update across the Internet.
    
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
>  The following procedure will show you how to delete any other, unwanted nameservers from the list, and also how to add the correct nameservers if they are not already listed. >  When you have completed the steps in this section, the only nameservers that should be listed are these four: >  ns1.bdm.microsoftonline.com >  ns2.bdm.microsoftonline.com >  ns3.bdm.microsoftonline.com >  ns4.bdm.microsoftonline.com 
  
1. To get started, go to your domains page at AWS by using [this link](https://console.aws.amazon.com/route53/home). You'll be prompted to log in first.
    
2. On the **Resources** page, choose **Hosted Zones**.
    
3. On the **Hosted Zones** page, in the **Domain Name** column, choose the name of the domain that you want to edit. 
    
4. Select the **Nameserver** record set. 
    
    ![Select the recordset](../media/24e618e4-0a16-43a2-9886-f4f5dac79374.png)
  
5. In the **NS - Name server** record set in the **Value** box, delete all of the nameservers by selecting them all and then pressing the **Delete** key on your keyboard. 
    
    > [!CAUTION]
    > Follow these steps only if you have existing nameservers other than the four correct nameservers. (That is, delete only any current nameservers that are  *not*  named **ns1.bdm.microsoftonline.com**, **ns2.bdm.microsoftonline.com**, **ns3.bdm.microsoftonline.com**, or **ns4.bdm.microsoftonline.com**.) 
  
    ![Select and delete all of the nameservers in the Value box](../media/ecf1e897-fa7d-4abc-b00b-bf55b8ed2139.png)
  
6. In the **TTL (Seconds):** area, choose **1h** (1 Hour). 
    
    ![Click 1H for one hour](../media/c70070e1-4bde-41a7-b271-9d22c475edf6.png)
  
7. Still in the **NS - Name server** record set, in the **Value** box, type or copy and paste the **First line** value from the following table, then press the **Enter** key on your keyboard and type or copy and paste the next **line** value. 
    
    > [!IMPORTANT]
    > Each nameserver value  *must*  be on its own separate line within the **Value** box, as shown in the following illustration. 
  
|||
|:-----|:-----|
|**First line** <br/> |ns1.bdm.microsoftonline.com.  <br/> **This value MUST end with a period (.)** <br/> |
|**Second line** <br/> |ns2.bdm.microsoftonline.com.  <br/> **This value MUST end with a period (.)** <br/> |
|**Third line** <br/> |ns3.bdm.microsoftonline.com.  <br/> **This value MUST end with a period (.)** <br/> |
|**Fourth line** <br/> |ns4.bdm.microsoftonline.com.  <br/> **This value MUST end with a period (.)** <br/> |
   
    ![Ttype or paste the First line value in the Value box](../media/b63f41e0-51ef-4ab2-a4b8-ee7380e5ab35.png)
  
8. Choose **Save Record Set**.
    
    ![Click Save Record Set](../media/ab3c0558-bb7c-41e4-871e-ea82f1553476.png)
  
> [!NOTE]
> Your nameserver record updates may take up to several hours to update across the Internet's DNS system. Then your Office 365 email and other services will be all set to work with your domain. 
