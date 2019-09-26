---
title: "Create DNS records at eNomCentral for Office 365"
ms.author: pebaum
author: pebaum
manager: mnirkhe
audience: Admin
ms.topic: get-started-article
f1_keywords:
- 'O365P_DOM_eNom'
- 'O365M_DOM_eNom'
- 'O365E_DOM_eNom'
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
ms.assetid: a6626053-a9c8-445b-81ee-eeb6672fae77
description: "Learn to verify your domain and set up DNS records for email, Skype for Business Online, and other services at eNomCentral for Office 365."
---

# Create DNS records at eNomCentral for Office 365

 **[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for. 
  
If eNomCentral is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.
  
After you add these records at eNomCentral, your domain will be set up to work with Office 365 services.
  
To learn about webhosting and DNS for websites with Office 365, see [Use a public website with Office 365](https://support.office.com/article/a8178510-501d-4bd8-9921-b04f2e9517a5.aspx).
  
> [!NOTE]
>  Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md). 
  
## Add a TXT record for verification
<a name="BKMK_verify"> </a>

Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.
  
> [!NOTE]
> This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like. 
  
Follow the steps below or [watch the video (start at 0:46)](https://support.office.com/en-us/article/Video-Create-DNS-records-at-eNomCentral-for-Office-365-3766a9e8-77dd-4a42-908d-89b076143e7d?ui=en-US&amp;rs=en-US&amp;ad=US).
  
1. To get started, go to your domains page at eNom Central by using [this link](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered). You'll be prompted to login.
    
    ![eNom-BP-Configure-1-1](../media/6f754710-fd29-4a0a-b362-fa7a5c5ff74f.png)
  
2. Under **my domains**, select the name of the domain that you want to edit.
    
    ![eNom-BP-Configure-1-2](../media/09d53e84-371c-4704-a8ce-e429ce9e133a.png)
  
3. On the **Manage Domain** drop-down list, choose **Host Records**.
    
    ![eNom-BP-Verify-1-1](../media/6e4184a1-9525-47a6-8a8a-9600126c0db4.png)
  
4. In the boxes for the new record, type or copy and paste the values from the following table.
    
    (Choose the **Record Type** value from the drop-down list.) 
    
    ||||
    |:-----|:-----|:-----|
    |**Host Name** <br/> |**Record Type** <br/> |**Address** <br/> |
    |@  <br/> |TXT  <br/> |MS=ms *XXXXXXXX*  <br/> **Note:** This is an example. Use your specific **Destination or Points to Address** value here, from the table in Office 365.           [How do I find this?](../get-help-with-domains/information-for-dns-records.md)          |
       
   ![eNom-BP-Verify-1-2](../media/e1f95529-46a6-40f9-9709-9fe66f373bcf.png)
  
5. Select **save**.
    
    ![eNom-BP-Verify-1-3](../media/d6277ab0-5d03-44e0-968f-fd5de1905423.png)
  
6. Wait a few minutes before you continue, so that the record you just created can update across the Internet.
    
Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.
  
When Office 365 finds the correct TXT record, your domain is verified.
  
1. In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.

    
2. On the **Domains** page, select the domain that you are verifying. 
    
    
  
3. On the **Setup** page, select **Start setup**.
    
    
  
4. On the **Verify domain** page, select **Verify**.
    
    
  
> [!NOTE]
>  Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md). 
  
## Add an MX record so email for your domain will come to Office 365
<a name="BKMK_add_MX"> </a>

Follow the steps below or [watch the video (start at 3:40)](https://support.office.com/en-us/article/Video-Create-DNS-records-at-eNomCentral-for-Office-365-3766a9e8-77dd-4a42-908d-89b076143e7d?ui=en-US&amp;rs=en-US&amp;ad=US).
  
1. To get started, go to your domains page at eNom Central by using [this link](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered). You'll be prompted to login.
    
    ![eNom-BP-Configure-1-1](../media/6f754710-fd29-4a0a-b362-fa7a5c5ff74f.png)
  
2. Under **my domains**, select the name of the domain that you want to edit.
    
    ![eNom-BP-Configure-1-2](../media/09d53e84-371c-4704-a8ce-e429ce9e133a.png)
  
3. On the **Manage Domain** drop-down list, choose **Email Settings**.
    
    ![eNom-BP-Configure-1-3](../media/4b438629-afdf-4a47-ab11-56644cdb6158.png)
  
4. On the **Service Selection** drop-down list, choose **User (MX)**.
    
    ![eNom-BP-Configure-1-4](../media/7680ab48-b8d1-4573-b20f-4745a5d7c079.png)
  
5. In the boxes for the new record, type or copy and paste the values from the following table.
    
    |**Host Name**|**Address**|**Pref**|
    |:-----|:-----|:-----|
    |@  <br/> | *\<domain-key\>*  .mail.protection.outlook.com.  <br/> **This value MUST end with a period (.)** <br/> **Note:** Get your  *\<domain-key\>*  from your Office 365 account.           [How do I find this?](../get-help-with-domains/information-for-dns-records.md)          |10  <br/> For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx) <br/> |
       
   ![eNom-BP-Configure-2-1](../media/c32e8954-8209-4f77-a3a8-4b7aeea325d5.png)
  
6. Select **save**.
    
    ![eNom-BP-Configure-2-2](../media/cf3058ea-9d30-4747-8cf0-2bc13d5ec6be.png)
  
7. If there are any other existing MX records, select the check boxes for those records to select them.
    
    ![eNom-BP-Configure-2-3](../media/5017ed03-ca76-4c5c-93a7-84ffe24125dc.png)
  
8. Select **delete checked**.
    
    ![eNom-BP-Configure-2-4](../media/072dc039-bddb-4c1f-bb44-5660e77f14b0.png)
  
## Add the CNAME records that are required for Office 365
<a name="BKMK_add_CNAME"> </a>

Follow the steps below or [watch the video (start at 4:24)](https://support.office.com/en-us/article/Video-Create-DNS-records-at-eNomCentral-for-Office-365-3766a9e8-77dd-4a42-908d-89b076143e7d?ui=en-US&amp;rs=en-US&amp;ad=US).
  
1. To get started, go to your domains page at eNom Central by using [this link](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered). You'll be prompted to login.
    
    ![eNom-BP-Configure-1-1](../media/6f754710-fd29-4a0a-b362-fa7a5c5ff74f.png)
  
2. Under **my domains**, select the name of the domain that you want to edit.
    
    ![eNom-BP-Configure-1-2](../media/09d53e84-371c-4704-a8ce-e429ce9e133a.png)
  
3. On the **Manage Domain** drop-down list, choose **Host Records**.
    
    ![eNom-BP-Configure-1-5](../media/c92c514c-8166-4cba-97e3-ee1d9847d255.png)
  
4. Select **new row**.
    
    ![eNom-BP-Configure-3-1](../media/a30f0a88-7b09-411e-9133-e7965bcf1de0.png)
  
5. In the boxes for the six new records, type or copy and paste the following values.
    
        (Choose the **Record Type** value from the drop-down list.) 
        
    |**Host Name**|**Record Type**|**Address**|
    |:-----|:-----|:-----|
    |autodiscover  <br/> |CNAME (Alias)  <br/> |autodiscover.outlook.com.  <br/> **This value MUST end with a period (.)** <br/> |
    |sip  <br/> |CNAME (Alias)  <br/> |sipdir.online.lync.com.  <br/> **This value MUST end with a period (.)** <br/> |
    |lyncdiscover  <br/> |CNAME (Alias)  <br/> |webdir.online.lync.com.  <br/> **This value MUST end with a period (.)** <br/> |
    |enterpriseregistration  <br/> |CNAME (Alias)  <br/> |enterpriseregistration.windows.net.  <br/> **This value MUST end with a period (.)** <br/> |
    |enterpriseenrollment  <br/> |CNAME (Alias)  <br/> |enterpriseenrollment-s.manage.microsoft.com.  <br/> **This value MUST end with a period (.)** <br/> |
   
    ![eNom-BP-Configure-3-2](../media/672371c0-51af-44ba-bb18-80286b7676c1.png)
  
6. Select **save**.
    
    ![eNom-BP-Configure-3-3](../media/027b57ce-5699-408b-993b-e46a9ac31090.png)
  
## Add a TXT record for SPF to help prevent email spam
<a name="BKMK_add_TXT"> </a>

> [!IMPORTANT]
> You cannot have more than one TXT record for SPF for a domain. If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues. If you already have an SPF record for your domain, don't create a new one for Office 365. Instead, add the required Office 365 values to the current record so that you have a  *single*  SPF record that includes both sets of values.
  
Follow the steps below or [watch the video (start at 5:12)](https://support.office.com/en-us/article/Video-Create-DNS-records-at-eNomCentral-for-Office-365-3766a9e8-77dd-4a42-908d-89b076143e7d?ui=en-US&amp;rs=en-US&amp;ad=US).
  
1. To get started, go to your domains page at eNom Central by using [this link](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered). You'll be prompted to login.
    
    ![eNom-BP-Configure-1-1](../media/6f754710-fd29-4a0a-b362-fa7a5c5ff74f.png)
  
2. Under **my domains**, select the name of the domain that you want to edit.
    
    ![eNom-BP-Configure-1-2](../media/09d53e84-371c-4704-a8ce-e429ce9e133a.png)
  
3. On the **Manage Domain** drop-down list, choose **Host Records**.
    
    ![eNom-BP-Configure-1-5](../media/c92c514c-8166-4cba-97e3-ee1d9847d255.png)
  
4. In the boxes for the new record, type or copy and paste the values from the following table.
    
    (Choose the **Record Type** value from the drop-down list.) 
    
    |**Host Name**|**Record Type**|**Address**|
    |:-----|:-----|:-----|
    |@  <br/> |TXT  <br/> |v=spf1 include:spf.protection.outlook.com -all  <br/>**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.           |
   
   ![eNom-BP-Configure-4-1](../media/64c68697-258d-4044-84b1-c28f4a402e3b.png)
  
5. Select **save**.
    
    ![eNom-BP-Configure-4-2](../media/89f4effa-349e-4734-96a5-cd80b0cecd60.png)
  
## Add the two SRV records that are required for Office 365
<a name="BKMK_add_SRV"> </a>

Follow the steps below or [watch the video (start at 5:50)](https://support.office.com/en-us/article/Video-Create-DNS-records-at-eNomCentral-for-Office-365-3766a9e8-77dd-4a42-908d-89b076143e7d?ui=en-US&amp;rs=en-US&amp;ad=US).
  
1. To get started, go to your domains page at eNom Central by using [this link](https://www.enomcentral.com/domains/Domain-Manager.aspx?tab=registered). You'll be prompted to login.
    
    ![eNom-BP-Configure-1-1](../media/6f754710-fd29-4a0a-b362-fa7a5c5ff74f.png)
  
2. Under **my domains**, select the name of the domain that you want to edit.
    
    ![eNom-BP-Configure-1-2](../media/09d53e84-371c-4704-a8ce-e429ce9e133a.png)
  
3. On the **Manage Domain** drop-down list, choose **Host Records**.
    
    ![eNom-BP-Configure-1-5](../media/c92c514c-8166-4cba-97e3-ee1d9847d255.png)
  
4. To the right of **new row**, select **add SRV or SPF record**.
    
    ![eNom-BP-Configure-5-1](../media/c73c154d-5aa0-41ef-be25-f43129eb178c.png)
  
5. In the boxes for the two new records, type or copy and paste the values from the following table.
    
    |**Service**|**Protocol**|**Priority**|**Weight**|**Port**|**Target          (Hostname)**|
    |:-----|:-----|:-----|:-----|:-----|:-----|
    |_sip  <br/> |_tls  <br/> |100  <br/> |1  <br/> |443  <br/> |sipdir.online.lync.com.  <br/> **This value MUST end with a period (.)** <br/> |
    |_sipfederationtls  <br/> |_tcp  <br/> |100  <br/> |1  <br/> |5061  <br/> |sipfed.online.lync.com.  <br/> **This value MUST end with a period (.)** <br/> |
   
    ![eNom-BP-Configure-5-2](../media/4d478f40-780f-43b9-940b-712b09da8c63.png)
  
6. Select **save**
    
    ![eNom-BP-Configure-5-3](../media/d03b6f75-49f2-471d-978d-d32c47cd6aa7.png)
  
> [!NOTE]
>  Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md). 
  

