---
title: "Create DNS records at Crazy Domains for Office 365"
ms.author: pebaum
author: pebaum
manager: mnirkhe
ms.audience: Admin
ms.topic: get-started-article
f1_keywords:
- 'O365P_DOM_Crazy'
- 'O365M_DOM_Crazy'
- 'O365E_DOM_Crazy'
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
ms.assetid: 6386d63e-b78f-4736-90e7-b99a2c116a9f
description: "Learn to verify your domain and set up DNS records for email, Skype for Business Online, and other services at Crazy Domains for Office 365."
---

# Create DNS records at Crazy Domains for Office 365

 **[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for. 
  
If Crazy Domains is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.
  
After you add these records at Crazy Domains, your domain will be set up to work with Office 365 services.
  
To learn about webhosting and DNS for websites with Office 365, see [Use a public website with Office 365](https://support.office.com/article/a8178510-501d-4bd8-9921-b04f2e9517a5.aspx).
  
> [!NOTE]
> Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md). 
  
## Add a TXT record for verification
<a name="BKMK_verify"> </a>

Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.
  
> [!NOTE]
> This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like. 
  
1. To get started, go to your domains page at Crazy Domains by using [this link](https://manage.crazydomains.com/members/domains/). You'll be prompted to log in first.
    
    ![CrazyDomains-BP-Configure-1-1](../media/40c5117c-acad-4fe5-bf0d-d3c362b08a16.png)
  
2. In the **My Account** section, choose **Domains**.
    
    ![CrazyDomains-BP-Configure-1-2](../media/778576c3-560e-4ffb-b3b4-bd92fc6a6bd4.png)
  
3. On the **Domain Names** page, in the **Domain** section, choose the name of the domain that you are updating. 
    
    ![CrazyDomains-BP-Configure-1-3](../media/4dd7bb74-c8ed-4b4a-b4c1-d9538fc6bd9a.png)
  
4. In the **DNS Settings** section, choose the drop-down list icon. 
    
    ![CrazyDomains-BP-Configure-1-4-1](../media/c7573fbf-467d-49c1-abb6-8c7b9b4af83d.png)
  
5. Choose **Add Record**.
    
    ![CrazyDomains-BP-Configure-1-4-2](../media/7bef31f5-f180-4b61-a462-9326789e770f.png)
  
6. Choose **TXT Record** from the **Add Record** drop-down list. 
    
    ![CrazyDomains-BP-Verify-1-1](../media/f0ffdefb-d7a5-47df-bb5e-bf8a3bcc9b01.png)
  
7. Choose **Add**.
    
    ![CrazyDomains-BP-Verify-1-2](../media/b0cd623a-67f7-4bae-a5b5-507f5a106123.png)
  
8. In the boxes for the new record, type or copy and paste the values from the following table.
    
    |**Sub Domain**|**Text Record**|
    |:-----|:-----|
    |(Leave this field empty.)  <br/> |MS=ms *XXXXXXXX*  <br/> **Note:** This is an example. Use your specific **Destination or Points to Address** value here, from the table in Office 365.           [How do I find this?](../get-help-with-domains/information-for-dns-records.md)          |
   
    ![CrazyDomains-BP-Verify-1-3](../media/3867de97-6a98-4475-9bda-470bac75d483.png)
  
9. Choose **Update**.
    
    ![CrazyDomains-BP-Verify-1-4](../media/0e416df6-b7a2-4dd7-971c-f1cc31df30da.png)
  
10. Wait a few minutes before you continue, so that the record you just created can update across the Internet.
    
Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.
  
When Office 365 finds the correct TXT record, your domain is verified.
  
1. Choose **Setup** \> **Domains**.
    
2. On the **Domains** page, choose the domain that you are verifying. 
    
    ![Domain name selected in Office 365 Admin Center](../media/c61204f1-a025-448b-a2a1-c4d7abee7a06.png)
  
3. On the **Setup** page, choose **Start setup**.
    
    ![Start setup](../media/5f6578af-ae32-49e8-b283-ec2d080420da.png)
  
4. On the **Verify domain** page, choose **Verify**.
    
    ![Verify](../media/c256ab1d-03f2-498e-bb63-19e4d49a6b97.png)
  
> [!NOTE]
>  Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md). 
  
## Add an MX record so email for your domain will come to Office 365
<a name="BKMK_add_MX"> </a>

1. To get started, go to your domains page at Crazy Domains by using [this link](https://manage.crazydomains.com/members/domains/). You'll be prompted to log in first.
    
    ![CrazyDomains-BP-Configure-1-1](../media/40c5117c-acad-4fe5-bf0d-d3c362b08a16.png)
  
2. In the **My Account** section, choose **Domains**.
    
    ![CrazyDomains-BP-Configure-1-2](../media/778576c3-560e-4ffb-b3b4-bd92fc6a6bd4.png)
  
3. On the **Domain Names** page, in the **Domain** section, choose the name of the domain that you are updating. 
    
    ![CrazyDomains-BP-Configure-1-3](../media/4dd7bb74-c8ed-4b4a-b4c1-d9538fc6bd9a.png)
  
4. In the **DNS Settings** section, choose the drop-down list icon. 
    
    ![CrazyDomains-BP-Configure-1-4-1](../media/c7573fbf-467d-49c1-abb6-8c7b9b4af83d.png)
  
5. Choose **Add Record**.
    
    ![CrazyDomains-BP-Configure-1-4-2](../media/7bef31f5-f180-4b61-a462-9326789e770f.png)
  
6. Choose **MX Record** from the **Add Record:** drop-down list. 
    
    ![CrazyDomains-BP-Configure-2-1](../media/63f7ab77-e686-4e7b-a3a2-1ac28a02d5f3.png)
  
7. Choose **Add**.
    
    ![CrazyDomains-BP-Configure-2-2](../media/a60680a1-2513-498c-b42f-8ffa575ee48e.png)
  
8. In the boxes for the new record, type or copy and paste the values from the following table.
    
    (Select the **Priority** value from the drop-down list.) 
    
    |**Mail For Zone**|**Priority**|**Assigned To Server**|
    |:-----|:-----|:-----|
    |(Leave this field empty.)  <br/> |1  <br/> For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx) <br/> | *\<domain-key\>*  .mail.protection.outlook.com  <br/> **Note:** Get your  *\<domain-key\>*  from your Office 365 portal account.           [How do I find this?](../get-help-with-domains/information-for-dns-records.md)          |
       
   ![CrazyDomains-BP-Configure-2-3](../media/e27df6a6-19a6-4e58-9716-a74be1c3f8da.png)
  
9. Choose **Update**.
    
    ![CrazyDomains-BP-Configure-2-4](../media/ba25cdef-a436-48bf-b0e9-5dffd03234a4.png)
  
10. If there are any other MX records listed in the **MX Record** section, choose **Modify** for one of those records. 
    
    ![CrazyDomains-BP-Configure-2-5](../media/9acdda39-33ec-4b24-ad83-91c26f9c599b.png)
  
11. Choose **Delete**.
    
    ![CrazyDomains-BP-Configure-2-6](../media/50b0e263-6f21-41b3-8fa0-7dd55dbe6c2e.png)
  
12. Choose **Update** to confirm the deletion. 
    
    ![CrazyDomains-BP-Configure-2-7](../media/db751bfe-31c2-4632-a491-6893eda38a51.png)
  
13. Use the same process to remove any other MX records in the list, until only the one that you added earlier in this procedure remains.
    
## Add the six CNAME records that are required for Office 365
<a name="BKMK_add_CNAME"> </a>

1. To get started, go to your domains page at Crazy Domains by using [this link](https://manage.crazydomains.com/members/domains/). You'll be prompted to log in first.
    
    ![CrazyDomains-BP-Configure-1-1](../media/40c5117c-acad-4fe5-bf0d-d3c362b08a16.png)
  
2. In the **My Account** section, choose **Domains**.
    
    ![CrazyDomains-BP-Configure-1-2](../media/778576c3-560e-4ffb-b3b4-bd92fc6a6bd4.png)
  
3. On the **Domain Names** page, in the **Domain** section, choose the name of the domain that you are updating. 
    
    ![CrazyDomains-BP-Configure-1-3](../media/4dd7bb74-c8ed-4b4a-b4c1-d9538fc6bd9a.png)
  
4. In the **DNS Settings** section, choose the drop-down list icon. 
    
    ![CrazyDomains-BP-Configure-1-4-1](../media/c7573fbf-467d-49c1-abb6-8c7b9b4af83d.png)
  
5. Choose **Add Record**.
    
    ![CrazyDomains-BP-Configure-1-4-2](../media/7bef31f5-f180-4b61-a462-9326789e770f.png)
  
6. Choose **CNAME Record** from the **Add Record:** drop-down list. 
    
    ![CrazyDomains-BP-Configure-3-1](../media/2f02538b-fc79-46d2-a2b7-1022eaf0fb08.png)
  
7. Choose **Add**.
    
    ![CrazyDomains-BP-Configure-3-2](../media/4c5929cf-1c21-4af9-899b-e36091f0f14d.png)
  
8. Add the first of the six CNAME records.
    
    In the boxes for the new record, type or copy and paste the values from the first row of the following table.
    
    |**Sub Domain**|**Alias for**|
    |:-----|:-----|
    |autodiscover  <br/> |autodiscover.outlook.com  <br/> |
    |sip  <br/> |sipdir.online.lync.com  <br/> |
    |lyncdiscover  <br/> |webdir.online.lync.com  <br/> |
    |msoid  <br/> |clientconfig.microsoftonline-p.net  <br/> |
    |enterpriseregistration  <br/> |enterpriseregistration.windows.net  <br/> |
    |enterpriseenrollment  <br/> |enterpriseenrollment-s.manage.microsoft.com  <br/> |
   
    ![CrazyDomains-BP-Configure-3-3](../media/81a7b837-3f4d-4565-89a9-380e4d318acf.png)
  
9. Choose **Add CNAME Record**.
    
    ![CrazyDomains-BP-Configure-3-4](../media/9bcba729-7085-4ebc-8183-ecde82f5c364.png)
  
10. Add the second CNAME record.
    
    In the boxes for the new record, use the values from the next row in the table, and then again choose **Add CNAME Record**.
    
    Repeat this process until you have created all six CNAME records.
    
11. Choose **Update** to save your changes. 
    
    ![CrazyDomains-BP-Configure-3-5](../media/dbe578f6-359c-428c-b296-ca624cecfc3c.png)
  
## Add a TXT record for SPF to help prevent email spam
<a name="BKMK_add_TXT"> </a>

> [!IMPORTANT]
> You cannot have more than one TXT record for SPF for a domain. If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues. If you already have an SPF record for your domain, don't create a new one for Office 365. Instead, add the required Office 365 values to the current record so that you have a  *single*  SPF record that includes both sets of values. 
  
1. To get started, go to your domains page at Crazy Domains by using [this link](https://manage.crazydomains.com/members/domains/). You'll be prompted to log in first.
    
    ![CrazyDomains-BP-Configure-1-1](../media/40c5117c-acad-4fe5-bf0d-d3c362b08a16.png)
  
2. In the **My Account** section, choose **Domains**.
    
    ![CrazyDomains-BP-Configure-1-2](../media/778576c3-560e-4ffb-b3b4-bd92fc6a6bd4.png)
  
3. On the **Domain Names** page, in the **Domain** section, choose the name of the domain that you are updating. 
    
    ![CrazyDomains-BP-Configure-1-3](../media/4dd7bb74-c8ed-4b4a-b4c1-d9538fc6bd9a.png)
  
4. In the **DNS Settings** section, choose the drop-down list icon. 
    
    ![CrazyDomains-BP-Configure-1-4-1](../media/c7573fbf-467d-49c1-abb6-8c7b9b4af83d.png)
  
5. Choose **Add Record**.
    
    ![CrazyDomains-BP-Configure-1-4-2](../media/7bef31f5-f180-4b61-a462-9326789e770f.png)
  
6. Choose **TXT Record** from the **Add Record:** drop-down list. 
    
    ![CrazyDomains-BP-Configure-4-1](../media/7f2461e2-0468-49bd-9eb0-981e9b2f72d6.png)
  
7. Choose **Add**.
    
    ![CrazyDomains-BP-Configure-4-2](../media/64ef9e1f-676d-46e2-9253-a83d9bcd1c4e.png)
  
8. In the boxes for the new record, type or paste the values from the following table.
    
    |**Sub Domain**|**Text Record**|
    |:-----|:-----|
    |(Leave this field empty.)  <br/> |v=spf1 include:spf.protection.outlook.com -all  <br/> **Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.           |
   
    ![CrazyDomains-BP-Configure-4-3](../media/e7fd524a-c94b-4cdd-b264-67abb532a71b.png)
  
9. Choose **Update**.
    
    ![CrazyDomains-BP-Configure-4-4](../media/d4f378ee-0f14-46ae-ba32-1596660ecf91.png)
  
## Add the two SRV records that are required for Office 365
<a name="BKMK_add_SRV"> </a>

1. To get started, go to your domains page at Crazy Domains by using [this link](https://manage.crazydomains.com/members/domains/). You'll be prompted to log in first.
    
    ![CrazyDomains-BP-Configure-1-1](../media/40c5117c-acad-4fe5-bf0d-d3c362b08a16.png)
  
2. In the **My Account** section, choose **Domains**.
    
    ![CrazyDomains-BP-Configure-1-2](../media/778576c3-560e-4ffb-b3b4-bd92fc6a6bd4.png)
  
3. On the **Domain Names** page, in the **Domain** section, choose the name of the domain that you are updating. 
    
    ![CrazyDomains-BP-Configure-1-3](../media/4dd7bb74-c8ed-4b4a-b4c1-d9538fc6bd9a.png)
  
4. In the **DNS Settings** section, choose the drop-down list icon. 
    
    ![CrazyDomains-BP-Configure-1-4-1](../media/c7573fbf-467d-49c1-abb6-8c7b9b4af83d.png)
  
5. Choose **Add Record**.
    
    ![CrazyDomains-BP-Configure-1-4-2](../media/7bef31f5-f180-4b61-a462-9326789e770f.png)
  
6. Choose **SRV Record** from the **Add Record:** drop-down list. 
    
    ![CrazyDomains-BP-Configure-5-1](../media/156acebc-7f6d-4b5e-8493-6bc62ca0ee27.png)
  
7. Choose **Add**.
    
    ![CrazyDomains-BP-Configure-5-2](../media/6a711df7-4215-49b2-b58f-1cf1a242b383.png)
  
8. Add the first of the two SRV records.
    
    In the boxes for the new record, type or copy and paste the values from the first row of the following table.
    
    |**Record Type**|**Sub Domain**|**Priority**|**Weight**|**Port**|**Target**|
    |:-----|:-----|:-----|:-----|:-----|:-----|
    |SRV Record  <br/> |_sip._tls  <br/> |100  <br/> |1  <br/> |443  <br/> |sipdir.online.lync.com  <br/> |
    |SRV Record  <br/> |_sipfederationtls._tcp  <br/> |100  <br/> |1  <br/> |5061  <br/> |sipfed.online.lync.com  <br/> |
   
    ![CrazyDomains-BP-Configure-5-3](../media/cc0ea6eb-7358-434e-bd1a-2737725c6d41.png)
  
9. Choose **Add SRV Record**.
    
    ![CrazyDomains-BP-Configure-5-4](../media/de4ec312-6833-469a-b23a-f376140a35ca.png)
  
10. Add the other SRV record.
    
    In the boxes for the new record, use the values from the second row in the table.
    
11. Choose **Update** to save your changes. 
    
    ![CrazyDomains-BP-Configure-5-5](../media/f0bb1dd6-3772-4293-bf74-710f635e0658.png)
  
> [!NOTE]
> Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md). 
  
