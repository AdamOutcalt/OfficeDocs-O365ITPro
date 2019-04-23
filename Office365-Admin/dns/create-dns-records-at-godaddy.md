---
title: "Create DNS records at GoDaddy for Office 365"
ms.author: pebaum
author: pebaum
manager: mnirkhe
ms.audience: Admin
ms.topic: get-started-article
f1_keywords:
- 'O365P_DOM_GD'
- 'O365M_DOM_GD'
- 'O365M_AddDNSRecords_GoDaddySteps'
- 'O365E_DOM_GD'
- 'O365E_AddDNSRecords_GoDaddySteps'
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
ms.assetid: f40a9185-b6d5-4a80-bb31-aa3bb0cab48a
description: "Learn to verify your domain and set up DNS records for email, Skype for Business Online, and other services at GoDaddy for Office 365."
---

# Create DNS records at GoDaddy for Office 365

 **[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for. 
  
If GoDaddy is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.
  
After you add these records at GoDaddy, your domain will be set up to work with Office 365 services.
  
To learn about webhosting and DNS for websites with Office 365, see [Use a public website with Office 365](https://support.office.com/article/a8178510-501d-4bd8-9921-b04f2e9517a5.aspx).
  
> [!NOTE]
> Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md). 
  
## Add a TXT record for verification
<a name="BKMK_verify"> </a>

Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.
  
> [!NOTE]
> This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like. 
  
Follow the steps below.
  
1. To get started, go to your domains page at GoDaddy by using [this link](https://account.godaddy.com/products/?go_redirect=disabled). You'll be prompted to log in.
    
    ![GoDaddy-BP-Configure-1-1](../media/d6833ec7-9904-43fd-a877-7c663e5f5c25.png)
  
2. Under **Domains**, choose DNS under the domain that you want to edit.
    
    ![GoDaddy-BP-Configure-1-2](https://user-images.githubusercontent.com/45987684/56528038-94b6ac00-651c-11e9-8874-12db60cc7ea6.PNG)
   
3. Choose **Add**.
    
    ![GoDaddy-BP-Configure-1-4](https://user-images.githubusercontent.com/45987684/56527673-ffb3b300-651b-11e9-91c2-83dc9fe5ca30.PNG)
  
4. Choose **TXT (Text)** from the drop-down list. In the boxes for the new record, type or copy and paste the values from the following table.
    
    |||||
    |:-----|:-----|:-----|:-----|
    |Record type  <br/> |Host  <br/> |TXT Value  <br/> |TTL  <br/> |
    |TXT (Text)  <br/> |@  <br/> |MS=ms *XXXXXXXX*  <br/> **Note:** This is an example. Use your specific **Destination or Points to Address** value here, from the table in Office 365.           [How do I find this?](../get-help-with-domains/information-for-dns-records.md)          |1 hour  <br/> |
      (Select the **TTL** value from the drop-down list.) 
    
      ![GoDaddy-BP-Verify-1-0](https://user-images.githubusercontent.com/45987684/56526870-d6465780-651a-11e9-9cf0-d6fff71e2f62.PNG)
   
5. Choose **Save **.

6. Wait a few minutes before you continue, so that the record you just created can update across the Internet.
    
Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.
  
When Office 365 finds the correct TXT record, your domain is verified.
  
1. Choose **Setup** \> **Domains**.
    
2. On the **Domains** page, choose the domain that you are verifying. 
    
    ![Domain name selected in Microsoft 365 admin center](../media/c61204f1-a025-448b-a2a1-c4d7abee7a06.png)
  
3. On the **Setup** page, choose **Start setup**.
    
    ![Start setup](../media/5f6578af-ae32-49e8-b283-ec2d080420da.png)
  
4. On the **Verify domain** page, choose **Verify**.
    
    ![Verify](../media/c256ab1d-03f2-498e-bb63-19e4d49a6b97.png)
  
> [!NOTE]
>  Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md). 
  
## Add an MX record so email for your domain will come to Office 365
<a name="BKMK_add_MX"> </a>

Follow the steps below.
  
1. To get started, go to your domains page at GoDaddy by using [this link](https://account.godaddy.com/products/?go_redirect=disabled). You'll be prompted to log in.
    
    ![GoDaddy-BP-Configure-1-1](../media/d6833ec7-9904-43fd-a877-7c663e5f5c25.png)
  
2. Under **Domains**, choose DNS under the domain that you want to edit.
    
    ![GoDaddy-BP-Configure-1-2](https://user-images.githubusercontent.com/45987684/56528038-94b6ac00-651c-11e9-8874-12db60cc7ea6.PNG)
   
3. Choose **Add**,
    
    ![GoDaddy-BP-Configure-1-4](https://user-images.githubusercontent.com/45987684/56527673-ffb3b300-651b-11e9-91c2-83dc9fe5ca30.PNG)
  
4. Choose **MX (Mail Exchanger)** from the drop-down list. 
    
    ![GoDaddy-BP-Configure-2-0](https://user-images.githubusercontent.com/45987684/56528642-85842e00-651d-11e9-8dd8-217f468f9a18.PNG)
  
5. In the boxes for the new record, type or copy and paste the values from the following table.
    
    (Select the **TTL** value from the drop-down list.) 
    
    |**Record type**|**Host**|**Points to**|**Priority**|**TTL**|
    |:-----|:-----|:-----|:-----|:-----|
    |MX (Mail Exchanger)  <br/> |@  <br/> | *\<domain-key\>*  .mail.protection.outlook.com  <br/> **Note:** Get your  *\<domain-key\>*  from your Office 365 portal account.           [How do I find this?](../get-help-with-domains/information-for-dns-records.md)          |10  <br/> For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx) <br/> |1 hour  <br/> |
   
6. Choose **Save**.


  
## Add the CNAME records that are required for Office 365
<a name="BKMK_add_CNAME"> </a>

Follow the steps below 
  
1. To get started, go to your domains page at GoDaddy by using [this link](https://account.godaddy.com/products/?go_redirect=disabled). You'll be prompted to log in.
    
    ![GoDaddy-BP-Configure-1-1](../media/d6833ec7-9904-43fd-a877-7c663e5f5c25.png)
  
2. Under **Domains**, choose DNS under the domain that you want to edit.
    
    ![GoDaddy-BP-Configure-1-2](https://user-images.githubusercontent.com/45987684/56528038-94b6ac00-651c-11e9-8874-12db60cc7ea6.PNG)
   
3. Choose **Add**,
    
    ![GoDaddy-BP-Configure-1-4](https://user-images.githubusercontent.com/45987684/56527673-ffb3b300-651b-11e9-91c2-83dc9fe5ca30.PNG)
 
  
4. Choose **CNAME (Alias)** from the drop-down list. 
    
    ![GoDaddy-BP-Configure-3-0](https://user-images.githubusercontent.com/45987684/56528891-e7449800-651d-11e9-8eac-112285b8e38c.PNG)
  
5. Create the first CNAME record.
    
    In the boxes for the new record, type or copy and paste the values from the first row of the following table.
    
    (Select the **TTL** value from the drop-down list.) 
    
    |**Record type**|**Host**|**Points to**|**TTL**|
    |:-----|:-----|:-----|:-----|
    |CNAME (Alias)  <br/> |autodiscover  <br/> |autodiscover.outlook.com  <br/> |1 hour  <br/> |
    |CNAME (Alias)  <br/> |sip  <br/> |sipdir.online.lync.com  <br/> |1 hour  <br/> |
    |CNAME (Alias)  <br/> |lyncdiscover  <br/> |webdir.online.lync.com  <br/> |1 hour  <br/> |
    |CNAME (Alias)  <br/> |msoid  <br/> |clientconfig.microsoftonline-p.net  <br/> |1 hour  <br/> |
    |CNAME (Alias)  <br/> |enterpriseregistration  <br/> |enterpriseregistration.windows.net  <br/> |1 hour  <br/> |
    |CNAME (Alias)  <br/> |enterpriseenrollment  <br/> |enterpriseenrollment.manage.microsoft.com  <br/> |1 hour  <br/> |
   

  
7. Repeat these step to add the CNAME record until you have created all six of the CNAME records.
    

  
## Add a TXT record for SPF to help prevent email spam
<a name="BKMK_add_TXT"> </a>

> [!IMPORTANT]
> You cannot have more than one TXT record for SPF for a domain. If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues. If you already have an SPF record for your domain, don't create a new one for Office 365. Instead, add the required Office 365 values to the current record so that you have a  *single*  SPF record that includes both sets of values. 
  
Follow the steps below 
  
1. To get started, go to your domains page at GoDaddy by using [this link](https://account.godaddy.com/products/?go_redirect=disabled). You'll be prompted to log in.
    
    ![GoDaddy-BP-Configure-1-1](../media/d6833ec7-9904-43fd-a877-7c663e5f5c25.png)
  
2. Under **Domains**, choose DNS under the domain that you want to edit.
    
    ![GoDaddy-BP-Configure-1-2](https://user-images.githubusercontent.com/45987684/56528038-94b6ac00-651c-11e9-8874-12db60cc7ea6.PNG)
   
3. Choose **Add**,
    
    ![GoDaddy-BP-Configure-1-4](https://user-images.githubusercontent.com/45987684/56527673-ffb3b300-651b-11e9-91c2-83dc9fe5ca30.PNG)
  
4. Choose **TXT (Text)** from the drop-down list. 
    
    ![GoDaddy-BP-Configure-4-0](https://user-images.githubusercontent.com/45987684/56529449-c0d32c80-651e-11e9-90e9-895aa1c4bbf1.PNG)
  
5. In the boxes for the new record, type or copy and paste the following values.
    
    (Select the **TTL** value from the drop-down lists.) 
    
    |**Record type**|**Host**|**TXT Value**|**TTL**|
    |:-----|:-----|:-----|:-----|
    |TXT (Text)  <br/> |@  <br/> |v=spf1 include:spf.protection.outlook.com -all  <br/> **Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.           |1 hour  <br/> |
   
    ![GoDaddy-BP-Configure-4-1](../media/7c724f02-c9b3-42ab-b9c0-78959fa6ffad.png)
  
6. Choose **Save**.
    
  
## Add the two SRV records that are required for Office 365
<a name="BKMK_add_SRV"> </a>

Follow the steps below 
  
1. To get started, go to your domains page at GoDaddy by using [this link](https://account.godaddy.com/products/?go_redirect=disabled). You'll be prompted to log in.
    
    ![GoDaddy-BP-Configure-1-1](../media/d6833ec7-9904-43fd-a877-7c663e5f5c25.png)
  
2. Under **Domains**, choose DNS under the domain that you want to edit.
    
    ![GoDaddy-BP-Configure-1-2](https://user-images.githubusercontent.com/45987684/56528038-94b6ac00-651c-11e9-8874-12db60cc7ea6.PNG)
   
3. Choose **Add**,
    
    ![GoDaddy-BP-Configure-1-4](https://user-images.githubusercontent.com/45987684/56527673-ffb3b300-651b-11e9-91c2-83dc9fe5ca30.PNG)

4. Choose **SRV (Service)** from the drop-down list. 
    
    ![GoDaddy-BP-Configure-5-0](https://user-images.githubusercontent.com/45987684/56529669-1dcee280-651f-11e9-8ba2-ecf4fc2f6dca.PNG)
  
5. Create the first SRV record.
    
    In the boxes for the new record, type or copy and paste the values from the first row of the following table.
    
    (Select the **Record type** and **TTL** values from the drop-down lists.) 
    
    |**Record type**|**Name**|**Target**|**Protocol**|**Service**|**Priority**|**Weight**|**Port**|**TTL**|
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |SRV (Service)  <br/> |@  <br/> |sipdir.online.lync.com  <br/> |_tls  <br/> |_sip  <br/> |100  <br/> |1  <br/> |443  <br/> |1 hour  <br/> |
    |SRV (Service)  <br/> |@  <br/> |sipfed.online.lync.com  <br/> |_tcp  <br/> |_sipfederationtls  <br/> |100  <br/> |1  <br/> |5061  <br/> |1 hour  <br/> |
   
    ![GoDaddy-BP-Configure-5-1](../media/a1b15ab1-eb6a-4672-90d1-7ac3e0beb223.png)
  

6. Repeat **Step 5** to Create the other SRV record.
     
7. Choose **Save**.
  
> [!NOTE]
> Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md). 
  

