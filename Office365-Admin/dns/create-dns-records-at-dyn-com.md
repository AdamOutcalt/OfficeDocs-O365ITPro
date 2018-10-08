---
title: "Create DNS records at Dyn.com for Office 365"
ms.author: pebaum
author: pebaum
manager: mnirkhe
ms.date: 3/28/2018
ms.audience: Admin
ms.topic: get-started-article
f1_keywords:
- 'O365P_DOM_Nett'
- 'O365P_DOM_DynCom'
- 'O365M_DOM_Nett'
- 'O365M_DOM_DynCom'
- 'O365E_DOM_Nett'
- 'O365E_DOM_DynCom'
ms.service: o365-administration
localization_priority: Normal
ms.custom:
- Adm_O365
- Adm_O365_Setup
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 34e57a00-2a7d-469c-beec-089423f18369

description: "Learn to verify your domain and set up DNS records for email, Skype for Business Online, and other services at Dyn.com for Office 365."
---

# Create DNS records at Dyn.com for Office 365

 **[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for. 
  
If Dyn.com is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.
  
These are the main records to add. (Need more help? [Still need help?](create-dns-records-at-dyn-com.md#BKMK_NeedHelp).)
  
- [Add a TXT record for verification](create-dns-records-at-dyn-com.md#BKMK_verify)
    
- [Add an MX record so email for your domain will come to Office 365](create-dns-records-at-dyn-com.md#BKMK_add_MX)
    
- [Add the six CNAME records that are required for Office 365](create-dns-records-at-dyn-com.md#BKMK_add_CNAME)
    
- [Add a TXT record for SPF to help prevent email spam](create-dns-records-at-dyn-com.md#BKMK_add_TXT)
    
- [Add the two SRV records that are required for Office 365](create-dns-records-at-dyn-com.md#BKMK_add_SRV)
    
After you add these records at Dyn.com, your domain will be set up to work with Office 365 services.
  
To learn about webhosting and DNS for websites with Office 365, see [Use a public website with Office 365](https://support.office.com/article/a8178510-501d-4bd8-9921-b04f2e9517a5.aspx).
  
> [!NOTE]
>  Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md). 
  
## Add a TXT record for verification
<a name="BKMK_verify"> </a>

1. To get started, go to your domains page at Dyn.com by using [this link](https://account.dyn.com/dns/)﻿. You'll be prompted to login first.
    
    ![Dyn-BP-Configure-1-1](../media/77597d44-9b04-43b1-8e23-d4fad238def2.png)
  
2. On the **Zone Level Services** page, choose **Dyn Standard DNS Service** for the domain that you want to edit. 
    
3. On the **DNS** page for your domain, choose **Preferences**.
    
4. Choose **Enable Expert Interface**.
    
5. In the **Add DNS Record** section, in the boxes for the new record, type or copy and paste the values from the following table. 
    
    (Choose the **Type** value from the drop-down list.) 
    
|**﻿Host**|**﻿TTL**|**﻿Type**|**﻿Data**|
|:-----|:-----|:-----|:-----|
|(Leave this field empty.)  <br/> |﻿600  <br/> |﻿TXT  <br/> |MS=ms *XXXXXXXX*  <br/> > [!NOTE]> This is an example. Use your specific **Destination or Points to Address** value here, from the table in Office 365.           [How do I find this?](../get-help-with-domains/information-for-dns-records.md)          |
   
    ![Dyn-BP-Verify-1-1](../media/b3730b15-a313-4b4c-b91e-646eebb649e8.png)
  
6. ﻿Choose **Create Record**.
    
    ![Dyn-BP-Verify-1-2](../media/8b63b4ee-dbd7-44a7-b1e6-c6892b02f13e.png)
  
7. Wait a few minutes before you continue, so that the record you just created can update across the Internet.
    
Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.
  
When Office 365 finds the correct TXT record, your domain is verified.
  
1. Choose **Setup** \> **Domains**.
    
2. On the **Domains** page, choose the domain that you are verifying. 
    
    ![Domain name selected in Office 365 Admin Center](../media/c61204f1-a025-448b-a2a1-c4d7abee7a06.png)
  
3. On the **Setup** page, choose **Start setup**.
    
    ![Start setup button](../media/5f6578af-ae32-49e8-b283-ec2d080420da.png)
  
4. On the **Verify domain** page, choose **Verify**.
    
    ![Verify button](../media/c256ab1d-03f2-498e-bb63-19e4d49a6b97.png)
  
> [!NOTE]
>  Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md). 
  
## Add an MX record so email for your domain will come to Office 365
<a name="BKMK_add_MX"> </a>

1. To get started, go to your domains page at Dyn.com by using [this link](https://account.dyn.com/dns/). You'll be prompted to login first.
    
    ![Dyn-BP-Configure-1-1](../media/77597d44-9b04-43b1-8e23-d4fad238def2.png)
  
2. On the **Zone Level Services** page, choose **Dyn Standard DNS Service** for the domain that you want to edit. 
    
3. On the DNS page for your domain, choose **Preferences﻿**.
    
4. Choose **Enable Expert Interface﻿**.
    
5. In the **Add DNS Record** section, in the boxes for the new record, type or copy and paste the values from the following table. 
    
    (Choose the **Type** value from the drop-down list.) 
    
|**Host**|**TTL**|**Type**|**Data**|
|:-----|:-----|:-----|:-----|
|(Leave this field empty.)  <br/> |600  <br/> |MX  <br/> |10  *\<domain-key\>*  .mail.protection.outlook.com.  <br/> **This value MUST end with a period (.)** <br/> The **10** is the MX priority value. Add it to the beginning of the MX value, separated from the remainder of the value by a space.  <br/> > [!NOTE]> Get your  *\<domain-key\>*  from your Office 365 portal account.           [How do I find this?](../get-help-with-domains/information-for-dns-records.md)          For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx) <br/> |
   
    ![Dyn-BP-Configure-2-1](../media/62ac77b7-c84d-426d-9ec4-a28d6479ad04.png)
  
6. Choose **Create Record**.
    
    ![Dyn-BP-Configure-2-2](../media/e84e2cca-75e3-4584-8a98-f2f89cb71bd3.png)
  
7. If there are any other MX records, remove them by selecting the check box for each one in the **Delete** column. 
    
    ![Dyn-BP-Configure-2-3](../media/f24f02cc-c0b7-42cf-a2ff-4d0fc203e4de.png)
  
8. Choose **Apply Changes**.
    
    ![Dyn-BP-Configure-2-4](../media/0cc23c2b-b6f2-4f58-af20-4c6506de7b43.png)
  
## Add the six CNAME records that are required for Office 365
<a name="BKMK_add_CNAME"> </a>

1. To get started, go to your domains page at Dyn.com by using [this link](https://account.dyn.com/dns/). You'll be prompted to login first.
    
    ![Dyn-BP-Configure-1-1](../media/77597d44-9b04-43b1-8e23-d4fad238def2.png)
  
2. On the **Zone Level Services** page, choose **Dyn Standard DNS Service** for the domain that you want to edit﻿. 
    
3. On the **DNS** page for your domain, choose **Preferences﻿**.
    
4. Choose **Enable Expert Interface**.
    
5. Add the first of the six CNAME records.
    
    In the **Add DNS Record** section, in the boxes for the new record, type or copy and paste the values from the first row of the following table. 
    
    (Choose the **Type** value from the drop-down list.) 
    
|**Host**|**TTL**|**Type**|**Data**|
|:-----|:-----|:-----|:-----|
|autodiscover  <br/> |600  <br/> |CNAME  <br/> |autodiscover.outlook.com.  <br/> **This value MUST end with a period (.)** <br/> |
|sip  <br/> |600  <br/> |CNAME  <br/> |sipdir.online.lync.com.  <br/> **This value MUST end with a period (.)** <br/> |
|lyncdiscover  <br/> |600  <br/> |CNAME  <br/> |webdir.online.lync.com.  <br/> **This value MUST end with a period (.)** <br/> |
|msoid  <br/> |600  <br/> |CNAME  <br/> |clientconfig.microsoftonline-p.net.  <br/> **This value MUST end with a period (.)** <br/> |
|enterpriseregistration  <br/> |600  <br/> |CNAME  <br/> |enterpriseregistration.windows.net.  <br/> **This value MUST end with a period (.)** <br/> |
|enterpriseenrollment  <br/> |600  <br/> |CNAME  <br/> |enterpriseenrollment-s.manage.microsoft.com.  <br/> **This value MUST end with a period (.)** <br/> |
   
    ![Dyn-BP-Configure-3-1](../media/1fd80695-d3d7-4298-9ebe-97a69f46f1b2.png)
  
6. Choose **Create Record**.
    
    ![Dyn-BP-Configure-3-2](../media/89551495-3fa5-44ab-96b2-855f70be0880.png)
  
7. Add the remaining five CNAME records.
    
    In the **Add DNS Record** section, create a record by using the values from the next row in the table, and then again choose **Create Record** to complete that record. 
    
    Repeat this process until you have created all six CNAME records.
    
## Add a TXT record for SPF to help prevent email spam
<a name="BKMK_add_TXT"> </a>

> [!IMPORTANT]
> You cannot have more than one TXT record for SPF for a domain. If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues. If you already have an SPF record for your domain, don't create a new one for Office 365. Instead, add the required Office 365 values to the current record so that you have a  *single*  SPF record that includes both sets of values. Need examples? Check out these [](external-domain-name-system-records.md#BKMK_SPFrecords). To validate your SPF record, you can use one of these [SPF validation tools](92a43f6a-4651-455a-a1cc-300684bedcfa.md). 
  
1. To get started, go to your domains page at Dyn.com by using [this link](https://account.dyn.com/dns/). You'll be prompted to login first﻿.
    
    ![Dyn-BP-Configure-1-1](../media/77597d44-9b04-43b1-8e23-d4fad238def2.png)
  
2. On the **Zone Level Services** page, choose **Dyn Standard DNS Service** for the domain that you want to edit﻿. 
    
3. On the **DNS** page for your domain, choose **Preferences**.
    
4. Choose **Enable Expert Interface**.
    
5. In the **Add DNS Record** section, in the boxes for the new record, type or copy and paste the values from the following table. 
    
    (Choose the **Type** value from the drop-down list.) 
    
|**Host**|**TTL**|**Type**|**Data**|
|:-----|:-----|:-----|:-----|
|(Leave this field empty.)  <br/> |600  <br/> |TXT  <br/> |v=spf1 include:spf.protection.outlook.com -all  <br/> > [!NOTE]> We recommend copying and pasting this entry, so that all of the spacing stays correct.           |
   
    ![Dyn-BP-Configure-4-1](../media/f8511349-3ea2-40c3-9853-98e1a58a91b5.png)
  
6. Choose **Create Record**.
    
    ![Dyn-BP-Configure-4-2](../media/bbe04835-d3c0-4146-8123-9781bb9eca51.png)
  
## Add the two SRV records that are required for Office 365
<a name="BKMK_add_SRV"> </a>

1. To get started, go to your domains page at Dyn.com by using [this link](https://account.dyn.com/dns/). You'll be prompted to login first 
    
    ![Dyn-BP-Configure-1-1](../media/77597d44-9b04-43b1-8e23-d4fad238def2.png)
  
2. On the **Zone Level Services** page, choose **Dyn Standard DNS Service** for the domain that you want to edit﻿. 
    
3. On the **DNS** page for your domain, choose **Preferences﻿**.
    
4. Choose **Enable Expert Interface﻿**.
    
5. Add the first of the two SRV records.
    
    In the **Add DNS Record** section, in the boxes for the new record, type or copy and paste the values from the first row of the following table. 
    
    (Choose the **Type** value from the drop-down list.) 
    
|**Host**|**TTL**|**Type**|**Data**|
|:-----|:-----|:-----|:-----|
|_sip._tls|600|SRV|100 1 443 sipdir.online.lync.com. **This value MUST end with a period (.)**> [!NOTE]> We recommend copying and pasting this entry, so that all of the spacing stays correct.           |
|_sipfederationtls._tcp|600|SRV|100 1 5061 sipfed.online.lync.com. **This value MUST end with a period (.)**> [!NOTE]> We recommend copying and pasting this entry, so that all of the spacing stays correct.           |
   
    ![Dyn-BP-Configure-5-1](../media/a6873411-f4ce-4327-9145-02d435930976.png)
  
6. Choose **Create Record**.
    
    ![Dyn-BP-Configure-5-2](../media/e6f33452-e527-473b-a645-b31ed70b0d43.png)
  
7. Add the other SRV record.
    
    In the **Add DNS Record** section, create a record by using the values from the second row in the table, and then again choose **Create Record** to complete that record. 
    
> [!NOTE]
>  Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md). 
  
## Still need help?
<a name="BKMK_NeedHelp"> </a>

[![Get help from the Office 365 community forums](../media/12a746cc-184b-4288-908c-f718ce9c4ba5.png)](https://go.microsoft.com/fwlink/p/?LinkId=518605)
  
[![Admins: Sign in and create a service request](../media/10862798-181d-47a5-ae4f-3f8d5a2874d4.png)]( https://go.microsoft.com/fwlink/p/?LinkId=519124)
  
[![Admins: Call Support](../media/9f262e67-e8c9-4fc0-85c2-b3f4cfbc064e.png)](https://go.microsoft.com/fwlink/p/?LinkID=518322)
  

