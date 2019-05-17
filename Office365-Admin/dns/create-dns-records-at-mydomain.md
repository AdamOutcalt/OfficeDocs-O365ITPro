---
title: "Create DNS records at MyDomain for Office 365"
ms.author: pebaum
author: pebaum
manager: mnirkhe
audience: Admin
ms.topic: get-started-article
f1_keywords:
- 'O365P_DOM_MD'
- 'O365M_DOM_MD'
- 'O365E_DOM_MD'
ms.service: o365-administration
localization_priority: Priority
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
ms.assetid: 9982191d-ed79-46a9-b2e7-317d1a3a9867
description: "Learn to verify your domain and set up DNS records for email, Skype for Business Online, and other services at My Domain for Office 365."
---

# Create DNS records at MyDomain for Office 365

¤
  
 **[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for. 
  
> [!CAUTION]
> The MyDomain website doesn't support SRV records, which means several Skype for Business Online and Outlook Web App features won't work. No matter which Office 365 plan you use, if you manage your DNS records at MyDomain, there are [significant service limitations](https://support.office.com/article/7ae9a655-041d-4724-aa92-60392ee390c2.aspx), and you might want to switch to a different DNS hosting provider. 
  
If you choose to manage your own Office 365 DNS records at MyDomain despite the service limitations, follow the steps in this article to set up your DNS records for email, Skype for Business Online, and so on.
    
After you add these records at MyDomain, your domain will be set up to work with Office 365 services.
  
To learn about webhosting and DNS for websites with Office 365, see [Use a public website with Office 365](https://support.office.com/article/a8178510-501d-4bd8-9921-b04f2e9517a5.aspx).
  
> [!NOTE]
> Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records in Office 365](../get-help-with-domains/find-and-fix-issues.md). 
  
## Add a TXT record for verification
<a name="BKMK_verify"> </a>

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
    |MS=ms *XXXXXXXX*  <br/> **Note:** This is an example. Use your specific **Destination or Points to Address** value here, from the table in Office 365. [How do I find this?](../get-help-with-domains/information-for-dns-records.md)          |
   
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
  
## Add an MX record so email for your domain will come to Office 365
<a name="BKMK_add_MX"> </a>

1. To get started, go to your domains page at MyDomain by using [this link](https://www.mydomain.com/controlpanel). You'll be prompted to log in first.
    
2. In the **My Favorites** section, choose **Domain Central**.
    
3. Under **Domain**, choose the name of the domain that you want to edit.
    
4. In the **Overview** row, choose **DNS**.
    
5. From the **Modify** drop-down list, choose **MX Record**.
    
    ![MyDomain-BP-Configure-2-1](../media/bbfba978-8c53-471b-8c9e-8ae62e559d15.png)
  
6. In the boxes for the new record, type or copy and paste the values from the following table.
    
    |**Priority**|**Host**|**Points To:**|
    |:-----|:-----|:-----|
    |0  <br/> For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx) <br/> |@  <br/> | *\<domain-key\>*  .mail.protection.outlook.com  <br/> **Note:** Get your \<*domain-key*\> from your Office 365 portal account. > [How do I find this?](../get-help-with-domains/information-for-dns-records.md)          |
   
    ![MyDomain-BP-Configure-2-2](../media/3e19cec3-7f3b-493d-81f7-cda30ba007d5.png)
  
7. Choose **Add**.
    
    ![MyDomain-BP-Configure-2-3](../media/1a1951a8-11d7-405d-bef5-285bbb053ce8.png)
  
8. If there are any other existing MX records, select **Remove** in the **Action** column for each one to delete it. 
    
    ![MyDomain-BP-Configure-2-4](../media/42576149-e056-4a81-a5fd-2c5dfac44e2e.png)
  
9. Choose **OK**.
    
    ![MyDomain-BP-Configure-2-5](../media/d6b70eb7-b79c-499e-82ff-ecef2e300368.png)
  
## Add the CNAME records that are required for Office 365
<a name="BKMK_add_CNAME"> </a>

1. To get started, go to your domains page at MyDomain by using [this link](https://www.mydomain.com/controlpanel). You'll be prompted to log in first.
    
2. In the **My Favorites** section, choose **Domain Central**.
    
3. Under **Domain**, choose the name of the domain that you want to edit.
    
4. In the **Overview** row, choose **DNS**.
    
5. From the **Modify** drop-down list, choose **CNAME Alias**.
    
    ![MyDomain-BP-Configure-3-1](../media/628267fc-d37b-42ef-bb92-265284e339ac.png)
  
6. Add the first CNAME record.
    
    In the boxes for the new record, type or copy and paste the values from the first row of the following table.
    
    |**Host**|**Points To:**|
    |:-----|:-----|
    |autodiscover  <br/> |autodiscover.outlook.com  <br/> |
    |sip  <br/> |sipdir.online.lync.com  <br/> |
    |lyncdiscover  <br/> |webdir.online.lync.com  <br/> |
    |msoid  <br/> |clientconfig.microsoftonline-p.net  <br/> |
    |enterpriseregistration  <br/> |enterpriseregistration.windows.net  <br/> |
    |enterpriseenrollment  <br/> |enterpriseenrollment-s.manage.microsoft.com  <br/> |
   
    ![MyDomain-BP-Configure-3-2](../media/3c8660b3-40bb-453d-8b99-4d22032bc4b3.png)
  
7. Choose **Add** to add the first record. 
    
    ![MyDomain-BP-Configure-3-3](../media/103a1d99-70da-4fdf-9291-7dd058ec6c4a.png)
  
8. Add the second CNAME record.
    
    Use the values from the second row of the table above, and then choose **Add** to add the second record. 
    
    Add the remaining records in the same way, using the values from the third, fourth, fifth, and sixth rows of the table.
    
## Add a TXT record for SPF to help prevent email spam
<a name="BKMK_add_TXT"> </a>

> [!IMPORTANT]
> You cannot have more than one TXT record for SPF for a domain. If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues. If you already have an SPF record for your domain, don't create a new one for Office 365. Instead, add the required Office 365 values to the current record so that you have a single SPF record that includes both sets of values. Need examples? Check out these [External Domain Name System records for Office 365](https://support.office.com/article/c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0#bkmk_spfrecords). To validate your SPF record, you can use one of these [SPF validation tools](../setup/domains-faq.md). 
  
1. To get started, go to your domains page at MyDomain by using [this link](https://www.mydomain.com/controlpanel). You'll be prompted to log in first.
    
2. In the **My Favorites** section, choose **Domain Central**.
    
3. Under **Domain**, choose the name of the domain that you want to edit.
    
4. In the **Overview** row, choose **DNS**.
    
5. From the **Modify** drop-down list, choose **TXT/SPF Record**.
    
    ![MyDomain-BP-Configure-4-1](../media/c461c762-52e6-4fde-b5bc-4dd5e5d62ed3.png)
  
6. Under **Content**, in the box for the new record, type or copy and paste the value from the following table.
    
    |**Content**|
    |:-----|
    |v=spf1 include:spf.protection.outlook.com -all  <br/> **Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.           |
   
    ![MyDomain-BP-Configure-4-2](../media/17d43106-88e6-47e5-aeba-0f18484acf3e.png)
  
7. Choose **Add**.
    
    ![MyDomain-BP-Configure-4-3](../media/b3670563-b620-470c-a42b-2c77888981f8.png)
  
## Add the two SRV records that are required for Office 365
<a name="BKMK_add_SRV"> </a>

> [!CAUTION]
> The MyDomain website doesn't support SRV records, which means several Skype for Business Online and Outlook Web App features won't work. No matter which Office 365 plan you use, if you manage your DNS records at MyDomain, there are [significant service limitations](https://support.office.com/article/7ae9a655-041d-4724-aa92-60392ee390c2.aspx), and you might want to switch to a different DNS hosting provider. 
  
> [!NOTE]
> Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records in Office 365](../get-help-with-domains/find-and-fix-issues.md). 
  
