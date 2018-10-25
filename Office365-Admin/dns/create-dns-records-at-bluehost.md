---
title: "Create DNS records at Bluehost for Office 365"
ms.author: pebaum
author: pebaum
manager: mnirkhe
ms.audience: Admin
ms.topic: get-started-article
f1_keywords:
- 'O365P_DOM_Bluehost'
- 'O365M_DOM_Bluehost'
- 'O365E_DOM_Bluehost'
ms.service: o365-administration
localization_priority: Normal
ms.collection:
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
ms.assetid: 657934ff-d9d2-4563-9ccf-ef4832a03a99
description: "Learn to verify your domain and set up DNS records for email, Skype for Business Online, and other services at Bluehost for Office 365."
---

# Create DNS records at Bluehost for Office 365

 **[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for. 
  
If Bluehost is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.
  
These are the main records to add. (Need more help? [Still need help?](create-dns-records-at-bluehost.md#BKMK_NeedHelp).)
  
- [Add a TXT record for verification](create-dns-records-at-bluehost.md#BKMK_verify)
    
- [Add an MX record so email for your domain will come to Office 365](create-dns-records-at-bluehost.md#BKMK_add_MX)
    
- [Add the six CNAME records that are required for Office 365](create-dns-records-at-bluehost.md#BKMK_add_CNAME)
    
- [Add a TXT record for SPF to help prevent email spam](create-dns-records-at-bluehost.md#BKMK_add_TXT)
    
- [Add the two SRV records that are required for Office 365](create-dns-records-at-bluehost.md#BKMK_add_SRV)
    
After you add these records at Bluehost, your domain will be set up to work with Office 365 services.
  
To learn about webhosting and DNS for websites with Office 365, see [Use a public website with Office 365](https://support.office.com/article/a8178510-501d-4bd8-9921-b04f2e9517a5.aspx).
  
> [!NOTE]
> Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records in Office 365](../get-help-with-domains/find-and-fix-issues.md). 
  
## Add a TXT record for verification
<a name="BKMK_verify"> </a>

Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.
  
> [!NOTE]
> This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like. 
  
1. To get started, go to your domains page at Bluehost by using [this link](https://my.bluehost.com/cgi/dm). You'll be prompted to log in first.
    
2. On the **domains** page, in the **domain** area, find the row for the domain that you're changing, and then select the check box for that domain. 
    
    (You may have to scroll down.)
    
3. In the ** *domain_name* ** area, on the **DNS Zone Editor** row, choose **Manage DNS records**.
    
4. On the ** DNS Zone Editor ** page, in the **Add DNS Record** area, in the boxes for the new record, type or copy and paste the values from the following table. 
    
    (Select the **Type** value from the drop-down list.) 
    
|||||
|:-----|:-----|:-----|:-----|
|**Host Record** <br/> |**TTL** <br/> |**Type** <br/> |**TXT Value** <br/> |
|@  <br/> |14400  <br/> |TXT  <br/> |MS=ms *XXXXXXXX*  <br/> > [!NOTE]> This is an example. Use your specific **Destination or Points to Address** value here, from the table in Office 365. [How do I find this?](../get-help-with-domains/information-for-dns-records.md)          |
   
5. Choose ** add record **.
    
6. Wait a few minutes before you continue, so that the record you just created can update across the Internet.
    
Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.
  
When Office 365 finds the correct TXT record, your domain is verified.
  
1. In the Office 365 admin center, choose **Setup** \> **Domains**.
    
2. On the **Domains** page, choose the domain that you are verifying. 
    
3. On the **Setup** page, choose **Start setup**.
    
4. On the **Verify domain** page, choose **Verify**.
    
> [!NOTE]
> Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records in Office 365](../get-help-with-domains/find-and-fix-issues.md). 
  
## Add an MX record so email for your domain will come to Office 365
<a name="BKMK_add_MX"> </a>

1. To get started, go to your domains page at Bluehost by using [this link](https://my.bluehost.com/cgi/dm). You'll be prompted to log in first.
    
2. On the **domains** page, in the **domain** area, find the row for the domain that you're changing, and then select the check box for that domain. 
    
    (You may have to scroll down.)
    
3. In the ** *domain_name* ** area, on the **DNS Zone Editor** row, choose **Manage DNS records**.
    
4. On the **DNS Zone Editor** page, in the **Add DNS Record** area, in the boxes for the new record, type or copy and paste the values from the following table. 
    
    (Select the **Type** value from the drop-down list.) 
    
|**Host Record**|**TTL**|**Type**|**Points To**|**Priority**|
|:-----|:-----|:-----|:-----|:-----|
|@  <br/> |14400  <br/> |MX  <br/> | *\<domain-key\>*  .mail.protection.outlook.com  <br/> > [!NOTE]> Get your \< *domain-key*  \> from your Office 365 portal account. [How do I find this?](../get-help-with-domains/information-for-dns-records.md)          |0  <br/> For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx) <br/> |
   
   ![Select Type from the drop-down list](../media/70791420-d83c-4a5d-a46c-5cc3bc67f565.png)
  
5. Choose **add record**.
    
    ![Click Add Record](../media/c7ef9733-1665-4dbf-accc-caadf1574abc.png)
  
6. If there are any other MX records in the **MX (Mail Exchanger)** section, delete each of them. 
    
    For one of the other MX records, choose **Delete.**
    
    ![Click Delete for each additional MX record](../media/6be17f54-3f33-47af-a9db-4689141530c2.png)
  
7. In the confirmation dialog box, choose **OK**.
    
    ![Click OK](../media/a50df7a3-2906-4cc0-87d4-1231ab234230.png)
  
8. Use the same process to delete any other MX records that were already listed.
    
## Add the six CNAME records that are required for Office 365
<a name="BKMK_add_CNAME"> </a>

1. To get started, go to your domains page at Bluehost by using [this link](https://my.bluehost.com/cgi/dm). You'll be prompted to log in first.
    
2. On the **domains** page, in the **domain** area, find the row for the domain that you're changing, and then select the check box for that domain. 
    
    (You may have to scroll down.)
    
3. In the ** *domain_name* ** area, on the **DNS Zone Editor** row, choose **Manage DNS records**.
    
4. In the **A (Host)** records section, find the row for the **autodiscover** record, and then choose **delete** for that row. 
    
    > [!IMPORTANT]
    > You must delete the existing **autodiscover** record  *before*  adding the **autodiscover** record that is required by Office 365. Bluehost does not allow you to maintain two **autodiscover** records simultaneously. 
  
    ![Click Delete](../media/416a447e-3710-4ae7-8bf1-459381af4f6e.png)
  
5. Choose **OK**.
    
    ![Click OK](../media/0c8f409d-c39f-4ed2-9c95-9af3e61c2411.png)
  
6. Create the first of the six CNAME records.
    
    On the **DNS Zone Editor** page, in the **Add DNS Record** area, in the boxes for the new record, type or copy and paste the values from the first row in the following table. 
    
    (Select the **Type** value from the drop-down list.) 
    
|**Host Record**|**TTL**|**Type**|**Points To**|
|:-----|:-----|:-----|:-----|
|autodiscover  <br/> |14400  <br/> |CNAME  <br/> |autodiscover.outlook.com  <br/> |
|sip  <br/> |14400  <br/> |CNAME  <br/> |sipdir.online.lync.com  <br/> |
|lyncdiscover  <br/> |14400  <br/> |CNAME  <br/> |webdir.online.lync.com  <br/> |
|msoid  <br/> |14400  <br/> |CNAME  <br/> |clientconfig.microsoftonline-p.net  <br/> |
|enterpriseregistration  <br/> |14400  <br/> |CNAME  <br/> |enterpriseregistration.windows.net  <br/> |
|enterpriseenrollment  <br/> |14400  <br/> |CNAME  <br/> |enterpriseenrollment.manage.microsoft.com  <br/> |
   
   ![Create the first CNAME record](../media/4f12e9b1-9dec-4bc2-aa15-8bffa71fe131.png)
  
7. Choose **add record**.
    
    ![Click Add Record](../media/c2782250-a9a6-4aee-bb15-f57cb0008587.png)
  
8. Add each of the other five CNAME records.
    
    Still in the **Add DNS Record** section, create a record by using the values from the next row in the table, and then again choose **add record** to complete that record. 
    
    Repeat this process until you have created all six CNAME records.
    
## Add a TXT record for SPF to help prevent email spam
<a name="BKMK_add_TXT"> </a>

> [!IMPORTANT]
> You cannot have more than one TXT record for SPF for a domain. If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues. If you already have an SPF record for your domain, don't create a new one for Office 365. Instead, add the required Office 365 values to the current record so that you have a  *single*  SPF record that includes both sets of values. Need examples? Check out these [External Domain Name System records for Office 365](https://support.office.com/article/c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0). To validate your SPF record, you can use one of these[SPF validation tools](../setup/domains-faq.md). 
  
1. To get started, go to your domains page at Bluehost by using [this link](https://my.bluehost.com/cgi/dm). You'll be prompted to log in first.
    
2. On the **domains** page, in the **domain** area, find the row for the domain that you're changing, and then select the check box for that domain. 
    
    (You may have to scroll down.)
    
3. In the ** *domain_name* ** area, on the **DNS Zone Editor** row, choose **Manage DNS records**.
    
4. On the **DNS Zone Editor** page, in the **Add DNS Record** area, in the boxes for the new record, type or copy and paste the values from the following table. 
    
    (Select the **Type** value from the drop-down list.) 
    
|**Host Record**|**TTL**|**Type**|**TXT Value**|
|:-----|:-----|:-----|:-----|
|@  <br/> |14400  <br/> |TXT  <br/> |v=spf1 include:spf.protection.outlook.com -all  <br/> > [!NOTE]> We recommend copying and pasting this entry, so that all of the spacing stays correct.           |
   
   ![Copy the TXT value](../media/b2dabd7a-ee3d-4209-aa1e-0233eb8cf3b9.png)
  
5. Choose **add record**.
    
    ![Click Add Record](../media/c050e9a2-2274-4640-8f0f-6752d382df5d.png)
  
## Add the two SRV records that are required for Office 365
<a name="BKMK_add_SRV"> </a>

1. To get started, go to your domains page at Bluehost by using [this link](https://my.bluehost.com/cgi/dm). You'll be prompted to log in first.
    
2. On the **domains** page, in the **domain** area, find the row for the domain that you're changing, and then select the check box for that domain. 
    
    (You may have to scroll down.)
    
3. In the ** *domain_name* ** area, on the **DNS Zone Editor** row, choose **Manage DNS records**.
    
4. Create the first of the two SRV records.
    
    On the **DNS Zone Editor** page, in the **Add DNS Record** area, in the boxes for the new record, type or copy and paste the values from the first row in the following table. 
    
    (Select the **Type** value from the drop-down list.) 
    
|**Service**|**Protocol**|**Host**|**TTL**|**Type**|**Priority**|**Weight**|**Port**|**Points To**|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|_sip  <br/> |_tls  <br/> |@  <br/> |14400  <br/> |SRV  <br/> |100  <br/> |1  <br/> |443  <br/> |sipdir.online.lync.com  <br/> |
|_sipfederationtls  <br/> |_tcp  <br/> |@  <br/> |14400  <br/> |SRV  <br/> |100  <br/> |1  <br/> |5061  <br/> |sipfed.online.lync.com  <br/> |
   
   ![Copy the value for the new record](../media/e2911bca-c00b-4b8a-837f-f1d438c474c4.png)
  
5. Choose **add record**.
    
    ![Click Add Record](../media/0fd6a587-03fd-4bce-8321-b14e6ad21f5c.png)
  
6. Add the other SRV record.
    
    Still in the **Add DNS Record** section, create a record by using the values from the other row in the table, and then again choose **add record** to complete that record. 
    
> [!NOTE]
> Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records in Office 365](../get-help-with-domains/find-and-fix-issues.md). 
  

