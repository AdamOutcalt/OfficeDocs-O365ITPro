---
title: "Create DNS records at Register.com for Office 365"
ms.author: pebaum
author: pebaum
manager: mnirkhe
ms.audience: Admin
ms.topic: get-started-article
f1_keywords:
- 'O365P_DOM_Reg'
- 'O365M_DOM_Reg'
- 'O365E_DOM_Reg'
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
ms.assetid: 55bd8c38-3316-48ae-a368-4959b2c1684e
description: "Learn to verify your domain and set up DNS records for email, Skype for Business Online, and other services at Register.com for Office 365."
---

# Create DNS records at Register.com for Office 365

 **[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for. 
  
If Register.com is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.
  
These are the main records to add. Follow the steps below or [watch the video](https://support.office.com/en-us/article/Video-Create-DNS-records-at-Register-com-for-Office-365-7448dd9e-c0e7-4d5e-a7e9-f0e4715433c4?ui=en-US&amp;rs=en-US&amp;ad=US).
  
- [Add a TXT record at Register.com to verify that you own the domain](#add-a-txt-record-at-registercom-to-verify-that-you-own-the-domain)
    
- [Add an MX record so email for your domain will come to Office 365](#add-an-mx-record-so-email-for-your-domain-will-come-to-office-365)
    
- [Add the CNAME records that are required for Office 365](#add-the-cname-records-that-are-required-for-office-365)
    
- [Add a TXT record for SPF to help prevent email spam](#add-a-txt-record-for-spf-to-help-prevent-email-spam)

- [Add the two SRV records that are required for Office 365](#add-the-two-srv-records-that-are-required-for-office-365)
    
After you add these records at Register.com, your domain will be set up to work with Office 365 services.
  
To learn about webhosting and DNS for websites with Office 365, see [Use a public website with Office 365](https://support.office.com/article/a8178510-501d-4bd8-9921-b04f2e9517a5.aspx).
  
> [!NOTE]
> Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records in Office 365](../get-help-with-domains/find-and-fix-issues.md). 
  
## Add a TXT record at Register.com to verify that you own the domain
<a name="BKMK_verify"> </a>

Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.
  
> [!NOTE]
> This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like. 
  
Follow the steps below or [watch the video (start at 0:44)](https://support.office.com/en-us/article/Video-Create-DNS-records-at-Register-com-for-Office-365-7448dd9e-c0e7-4d5e-a7e9-f0e4715433c4?ui=en-US&amp;rs=en-US&amp;ad=US).
  
1. To get started, go to your domains page at Register.com by using [this link](https://www.register.com/myaccount/). You'll be prompted to sign in.
    
2. Choose **Domains**.
    
3. Choose **Manage**.
    
4. Find the row that contains the name of the domain that you want to modify; and then, in that row, choose **Manage**.
    
5. Scroll down to the **Advanced Technical Settings** section, and then choose **Edit TXT Records (SPF)**.
    
6. In the boxes for the new record, type or copy and paste the values from the following table.
    
    |||
    |:-----|:-----|
    |**Host Name** <br/> |**TXT Record** <br/> |
    |@  <br/> |MS=ms *XXXXXXXX*  <br/> **Note:** This is an example. Use your specific **Destination or Points to Address** value here, from the table in Office 365. [How do I find this?](../get-help-with-domains/information-for-dns-records.md)          |
   
7. Choose **Continue**.
    
8. On the next page, choose **Continue** again to confirm your changes. 
    
9. Wait a few minutes before you continue, so that the record you just created can update across the Internet.
    
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

Follow the steps below or [watch the video (start at 3:32)](https://support.office.com/en-us/article/Video-Create-DNS-records-at-Register-com-for-Office-365-7448dd9e-c0e7-4d5e-a7e9-f0e4715433c4?ui=en-US&amp;rs=en-US&amp;ad=US).
  
1. To get started, go to your domains page at Register.com by using [this link](https://www.register.com/myaccount/). You'll be prompted to sign in.
    
2. Choose **Domains**.
    
3. Choose **Manage**.
    
4. Find the row that contains the name of the domain that you want to modify; and then, in that row, choose **Manage**.
    
5. Scroll to the **Advanced Technical Settings** section, and then choose **Edit Mail Exchanger Records**.
    
    ![Click Edit Mail Exchanger Records](../media/366b96a1-9147-4bbb-9f8f-50856466cc61.png)
  
6. In the boxes for the new record, type or copy and paste the values from the following table.
    
    (Select the **Priority** value from the drop-down list.) 
    
    |****Host Name****|****Priority****|****Mail Server****|
    |:-----|:-----|:-----|
    |@  <br/> |High  <br/> For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx) <br/> | *\<domain-key\>*  .mail.protection.outlook.com.  <br/> **This value MUST end with a period (.)** <br/>**Note:** Get your \<*domain-key*\> from your Office 365 account. <br> [How do I find this?](../get-help-with-domains/information-for-dns-records.md)          |
   
    ![Copy and paste the value from the table](../media/a1a15a14-c3dc-45dc-adcd-90fdb3f7455d.png)
  
7. If there were any other MX records already listed, select each of those records to be deleted.
    
    ![Select each record to delete](../media/0708d03e-346f-4ae7-8cc4-01589efc00ce.png)
  
8. Choose **Continue**.
    
    ![Click Continue](../media/6ef6ce01-ce21-4e3c-8209-4aa9a3dd4b76.png)
  
9. On the next page, choose **Continue** again to confirm and save your changes. 
    
    ![Click Continue](../media/adba4a60-bf61-44fc-9ad9-360e66f8a2ee.png)
  
## Add the CNAME records that are required for Office 365
<a name="BKMK_add_CNAME"> </a>

Follow the steps below or [watch the video (start at 4:23)](https://support.office.com/en-us/article/Video-Create-DNS-records-at-Register-com-for-Office-365-7448dd9e-c0e7-4d5e-a7e9-f0e4715433c4?ui=en-US&amp;rs=en-US&amp;ad=US).
  
1. To get started, go to your domains page at Register.com by using [this link](https://www.register.com/myaccount/). You'll be prompted to sign in.
    
2. Choose **Domains**.
    
3. Choose **Manage**.
    
4. Find the row that contains the name of the domain that you want to modify; and then, in that row, choose **Manage**.
    
5. Scroll to the **Advanced Technical Settings** section, and then choose **Edit Domain Aliases Records**.
    
    ![Click Edit Domain Aliases Records](../media/9fbc31ed-d67c-4828-8bd4-b51068f1e0ca.png)
  
6. Choose **Add more domain aliases**.
    
    ![Click Add more domains aliases](../media/b787505f-5566-4879-8552-13f9e89cbf6b.png)
  
7. Add the required CNAME records.
    
    In the boxes for the new record, type or copy and paste the values from the first row of the following table.
    
    |****First field (unlabeled)****|****Points to****|
    |:-----|:-----|
    |autodiscover  <br/> |autodiscover.outlook.com.  <br/> **This value MUST end with a period (.)** <br/> |
    |sip  <br/> |sipdir.online.lync.com.  <br/> **This value MUST end with a period (.)** <br/> |
    |lyncdiscover  <br/> |webdir.online.lync.com.  <br/> **This value MUST end with a period (.)** <br/> |
    |msoid  <br/> |clientconfig.microsoftonline-p.net.  <br/> **This value MUST end with a period (.)** <br/> |
    |enterpriseregistration  <br/> |enterpriseregistration.windows.net.  <br/> **This value MUST end with a period (.)** <br/> |
    |enterpriseenrollment  <br/> |enterpriseenrollment.manage.microsoft.com.  <br/> **This value MUST end with a period (.)** <br/> |
   
     ![Copy and paste the DNS values from the table](../media/0e2b36b2-8a0b-4019-addf-301763f9a626.png)
  
8. When you have added all of the CNAME records that you need, choose **Continue**.
    
    ![Click Continue](../media/1942612b-338a-48fa-a45d-2d5434516723.png)
  
9. On the next page, choose **Continue** again to confirm and save your changes. 
    
    ![Click Continue](../media/3342b570-0633-49c5-9175-5cc8e4a67b53.png)
  
## Add a TXT record for SPF to help prevent email spam
<a name="BKMK_add_TXT"> </a>

> [!IMPORTANT]
> You cannot have more than one TXT record for SPF for a domain. If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues. If you already have an SPF record for your domain, don't create a new one for Office 365. Instead, add the required Office 365 values to the current record so that you have a single SPF record that includes both sets of values.  
  
Follow the steps below or [watch the video (start at 5:12)](https://support.office.com/en-us/article/Video-Create-DNS-records-at-Register-com-for-Office-365-7448dd9e-c0e7-4d5e-a7e9-f0e4715433c4?ui=en-US&amp;rs=en-US&amp;ad=US).
  
1. To get started, go to your domains page at Register.com by using [this link](https://www.register.com/myaccount/). You'll be prompted to sign in.
    
2. Choose **Domains**.
    
3. Choose **Manage**.
    
4. Find the row that contains the name of the domain that you want to modify; and then, in that row, choose **Manage**.
    
5. Scroll to the **Advanced Technical Settings** section, and then choose **Edit TXT Records (SPF)**.
    
    ![Click Edit TXT Records (SPF)](../media/c917577a-8b3a-4210-ab6e-776e84f926d0.png)
  
6. In the boxes for the new record, type or copy and paste the values from the following table.
    
    |****Host Name****|****TXT Record****|
    |:-----|:-----|
    |@  <br/> |v=spf1 include:spf.protection.outlook.com -all  <br/> **Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.  |
   
     ![Copy and paste the values from the table](../media/b1dc5036-c13c-4306-b1e3-5a38a74643b7.png)
  
7. Choose **Continue**.
    
    ![Click Continue](../media/08250c98-1a86-48a8-ad94-f96cf338126b.png)
  
8. On the next page, choose **Continue** again to confirm and save your changes. 
    
    ![Click Continue](../media/56be3b0a-dc71-471c-9be3-6ab927296f67.png)
  
## Add the two SRV records that are required for Office 365
<a name="BKMK_add_SRV"> </a>

Follow the steps below or [watch the video (start at 5:55)](https://support.office.com/en-us/article/Video-Create-DNS-records-at-Register-com-for-Office-365-7448dd9e-c0e7-4d5e-a7e9-f0e4715433c4?ui=en-US&amp;rs=en-US&amp;ad=US).
  
1. To get started, go to your domains page at Register.com by using [this link](https://www.register.com/myaccount/). You'll be prompted to sign in.
    
2. Choose **Domains**.
    
3. Choose **Manage**.
    
4. Find the row that contains the name of the domain that you want to modify; and then, in that row, choose **Manage**.
    
5. Scroll to the **Advanced Technical Settings** section, and then choose **Edit SRV Records**.
    
    ![Click Edit SRV Records](../media/73c149ae-f0d6-460e-880a-7e04a995acc3.png)
  
6. Add the first of the two SRV records:
    
    In the boxes for the new record, type or copy and paste the values from the first row of the following table.
    
    (Select the **Priority** value from the drop-down list.) 
    
    |****Service****|****Proto****|****Name****|****Priority****|****Weight****|****Port****|****Target****|
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |_sip  <br/> |_tls  <br/> |@  <br/> |High  <br/> |1  <br/> |443  <br/> |sipdir.online.lync.com.  <br/> **This value MUST end with a period (.)** <br/> |
    |_sipfederationtls  <br/> |_tcp  <br/> |@  <br/> |High  <br/> |1  <br/> |5061  <br/> |sipfed.online.lync.com.  <br/> **This value MUST end with a period (.)** <br/> |
   
    ![Copy and paste the values from the table](../media/71304c81-5845-4a8f-b969-d9efc8721184.png)
  
7. Choose **Add more SRV records**.
    
    ![Click Add more SRV records](../media/823c6bd2-4af7-4079-bf8c-8d35a5c6730f.png)
  
8. Add the second SRV record:
    
    Type or copy and paste the values from the second row of the table above into the boxes for the second record.
    
9. When you have added both of the SRV records, choose **Continue**.
    
    ![Click Continue](../media/008b255a-42d3-442d-83ea-3ffcb7c8fc5d.png)
  
10. On the next page, choose **Continue** again to confirm and save your changes. 
    
    ![Click Continue](../media/b4166e3d-7e4b-41ef-b616-747e95aefc37.png)
  
> [!NOTE]
> Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records in Office 365](../get-help-with-domains/find-and-fix-issues.md). 
  
