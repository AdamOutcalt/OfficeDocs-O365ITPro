---
title: "Create DNS records at Network Solutions for Office 365"
ms.author: pebaum
author: pebaum
manager: mnirkhe
ms.date: 3/28/2018
ms.audience: Admin
ms.topic: get-started-article
f1_keywords:
- 'O365P_DOM_NetS'
- 'O365M_DOM_NetS'
- 'O365E_DOM_NetS'
ms.service: o365-administration
localization_priority: Normal
ms.custom:
- Adm_O365
- Adm_O365_Setup
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 1dc55f9f-5309-450f-acc3-b2b4119c8be3

description: "Learn to verify your domain and set up DNS records for email, Skype for Business Online, and other services at Network Solutions for Office 365."
---

# Create DNS records at Network Solutions for Office 365

 **[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for. 
  
If Network Solutions is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.
  
These are the main records to add. Follow the steps below or [watch the video](https://support.office.com/en-us/article/Video-Create-DNS-records-at-Network-Solutions-for-Office-365-c49698c2-6991-47fb-b5ac-18e49a505099?ui=en-US&amp;rs=en-US&amp;ad=US). (Need more help? [Still need help?](create-dns-records-at-network-solutions.md#BKMK_NeedHelp).)
  
- [Add a TXT record for verification](create-dns-records-at-network-solutions.md#BKMK_verify)
    
- [Add an MX record so email for your domain will come to Office 365](create-dns-records-at-network-solutions.md#BKMK_add_MX)
    
- [Add the CNAME records that are required for Office 365](create-dns-records-at-network-solutions.md#BKMK_add_CNAME)
    
- [Add a TXT record for SPF to help prevent email spam](create-dns-records-at-network-solutions.md#BKMK_add_TXT)
    
- [Add the two SRV records that are required for Office 365](create-dns-records-at-network-solutions.md#BKMK_add_SRV)
    
After you add these records at Network Solutions, your domain will be set up to work with Office 365 services.
  
To learn about webhosting and DNS for websites with Office 365, see [Use a public website with Office 365](https://support.office.com/article/a8178510-501d-4bd8-9921-b04f2e9517a5.aspx).
  
> [!NOTE]
>  Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md). 
  
## Add a TXT record for verification
<a name="BKMK_verify"> </a>

Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.
  
> [!NOTE]
> This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like. 
  
Follow the steps below or [watch the video (start at 0:47)](https://support.office.com/en-us/article/Video-Create-DNS-records-at-Network-Solutions-for-Office-365-c49698c2-6991-47fb-b5ac-18e49a505099?ui=en-US&amp;rs=en-US&amp;ad=US).
  
1. To get started, go to your domains page at Network Solutions by using [this link](https://www.networksolutions.com/manage-it). You'll be prompted to log in.
    
    > [!IMPORTANT]
    > Before you choose the **Login** button, first choose **Manage My Domain Names** in the **Log In to:** drop-down list. 
  
    ![Choose Manage My Domain Names and log in to Network Solutions](../media/fda7d4a1-9445-4086-be9c-87c6983ef2aa.png)
  
2. Select the check box next to the name of the domain that you are modifying.
    
    ![Select the check box for your domain](../media/2c13d2ba-4a31-44da-812c-2cc90900a183.png)
  
3. Choose **Edit DNS**.
    
    ![Click Edit DNS](../media/9d7c269f-48d1-442c-9d7b-63bd384a36a9.png)
  
4. Choose **Manage Advanced DNS Records**.
    
    (You may have to scroll down.)
    
    ![Click Manage Advanced DNS Records](../media/fd2956d6-eec3-47ea-b60a-266bab14f51f.png)
  
5. Scroll down to the **Text (TXT Records)** section, and then choose **Edit TXT Records**.
    
    ![Click Edit TXT Records](../media/240a01d6-750a-4da6-8554-641b571e4b71.png)
  
6. In the boxes for the new record, type or copy and paste the values in the following table.
    
|**Host**|**TTL**|**Text**|
|:-----|:-----|:-----|
|@  <br/> (The system will change this value to **@ (None)** when you save the record.)  <br/> |3600  <br/> |MS=ms *XXXXXXXX*  <br/> > [!NOTE]> This is an example. Use your specific **Destination or Points to Address** value here, from the table in Office 365.           [How do I find this?](../get-help-with-domains/information-for-dns-records.md)          |
   
    ![Type or paste values in the boxes for the new record](../media/8a76daab-b6ff-4c82-ba68-192b24fbb934.png)
  
7. Choose **Continue**.
    
    ![Click Continue](../media/89e7fb38-b4d9-4949-a1bb-d0dd10b361e0.png)
  
8. Choose **Save Changes**.
    
    ![Click Save Changes](../media/bd4d7cd0-c8a3-497a-b080-cfd5a5c60dc5.png)
  
9. Wait a few minutes before you continue, so that the record you just created can update across the Internet.
    
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

Follow the steps below or [watch the video (start at 3:51)](https://support.office.com/en-us/article/Video-Create-DNS-records-at-Network-Solutions-for-Office-365-c49698c2-6991-47fb-b5ac-18e49a505099?ui=en-US&amp;rs=en-US&amp;ad=US).
  
1. To get started, go to your domains page at Network Solutions by using [this link](https://www.networksolutions.com/manage-it). You'll be prompted to log in.
    
    > [!IMPORTANT]
    > Before you choose the **Login** button, first choose **Manage My Domain Names** in the **Log In to:** drop-down list. 
  
    ![Choose Manage My Domain Names and log in to Network Solutions](../media/fda7d4a1-9445-4086-be9c-87c6983ef2aa.png)
  
2. Select the check box next to the name of the domain that you are modifying.
    
    ![Select the check box for your domain](../media/2c13d2ba-4a31-44da-812c-2cc90900a183.png)
  
3. Choose **Edit DNS**.
    
    ![Click Edit DNS](../media/9d7c269f-48d1-442c-9d7b-63bd384a36a9.png)
  
4. Choose **Manage Advanced DNS Records**.
    
    (You may have to scroll down.)
    
    ![Click Manage Advanced DNS Records](../media/fd2956d6-eec3-47ea-b60a-266bab14f51f.png)
  
5. Scroll down to the **Mail Servers (MX Records)** section, and then choose **Edit MX Records**.
    
    ![Click Edit MX Records](../media/74b4e412-9073-4d2d-8710-fe340b223798.png)
  
6. In the boxes for the new record, type or copy and paste the values from the following table.
    
|**Priority**|**TTL**|**Mail Server**|
|:-----|:-----|:-----|
|10  <br/> For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx) <br/> |3600  <br/> | *\<domain-key\>*  .mail.protection.outlook.com.  <br/> **This value MUST end with a period (.)** <br/> > [!NOTE]> Get your  *\<domain-key\>*  from your Office 365 portal account.           [How do I find this?](../get-help-with-domains/information-for-dns-records.md)          |
   
    ![Type or paste values in the boxes for the new record](../media/0bb96872-cc6e-4dfa-a649-fb7efbbf0012.png)
  
7. Choose **Continue**.
    
    ![Click Continue](../media/963f758b-e79d-4452-8340-7eba8a3972c9.png)
  
8. Choose **Save Changes**.
    
    ![Click Save Changes](../media/7c2f784a-6dee-4364-866c-ad7202ef1fc2.png)
  
9. If there are any other MX records, delete all of them by selecting **Delete** for each record. 
    
    ![Select the Delete check box for other MX records](../media/709d6133-9f5d-490a-a91e-95e21ca94695.png)
  
10. When they are all selected, choose **Continue**.
    
    ![Click Continue](../media/4710f988-0bbc-4ba7-bf31-ca2392b2900e.png)
  
11. Choose **Save Changes**.
    
    ![Click Save Changes](../media/24432ec6-666b-4612-9488-37c06437959b.png)
  
## Add the CNAME records that are required for Office 365
<a name="BKMK_add_CNAME"> </a>

Follow the steps below or [watch the video (start at 4:43)](https://support.office.com/en-us/article/Video-Create-DNS-records-at-Network-Solutions-for-Office-365-c49698c2-6991-47fb-b5ac-18e49a505099?ui=en-US&amp;rs=en-US&amp;ad=US).
  
1. To get started, go to your domains page at Network Solutions by using [this link](https://www.networksolutions.com/manage-it). You'll be prompted to log in.
    
    > [!IMPORTANT]
    > Before you choose the **Login** button, first choose **Manage My Domain Names** in the **Log In to:** drop-down list. 
  
    ![Choose Manage My Domain Names and log in to Network Solutions](../media/fda7d4a1-9445-4086-be9c-87c6983ef2aa.png)
  
2. Select the check box next to the name of the domain that you are modifying.
    
    ![Select the check box for your domain](../media/2c13d2ba-4a31-44da-812c-2cc90900a183.png)
  
3. Choose **Edit DNS**.
    
    ![Click Edit DNS](../media/9d7c269f-48d1-442c-9d7b-63bd384a36a9.png)
  
4. Choose **Manage Advanced DNS Records**.
    
    (You may have to scroll down.)
    
    ![Click Manage Advanced DNS Records](../media/fd2956d6-eec3-47ea-b60a-266bab14f51f.png)
  
5. Scroll down to the **Host Aliases (CNAME Records)** section, and then choose **Edit CNAME Records**.
    
    ![Click Edit CNAME Records under Host Aliases](../media/2d0a4666-8d40-48f4-886c-64a5157baaf5.png)
  
6. In the boxes for the four new records, type or copy and paste the values from the following table.
    
|**Alias**|**TTL**|**Refers to Host Name**|**Other Host          (select the **Other Host** option button)**|
|:-----|:-----|:-----|:-----|
|autodiscover  <br/> |3600  <br/> |(No setting)  <br/> |autodiscover.outlook.com.  <br/> **This value MUST end with a period (.)** <br/> |
|sip  <br/> |3600  <br/> |(No setting)  <br/> |sipdir.online.lync.com.  <br/> **This value MUST end with a period (.)** <br/> |
|lyncdiscover  <br/> |3600  <br/> |(No setting)  <br/> |webdir.online.lync.com.  <br/> **This value MUST end with a period (.)** <br/> |
|msoid  <br/> |3600  <br/> |(No setting)  <br/> |clientconfig.microsoftonline-p.net.  <br/> **This value MUST end with a period (.)** <br/> |
|enterpriseregistration  <br/> |3600  <br/> |(No setting)  <br/> |enterpriseregistration.windows.net  <br/> **This value MUST end with a period (.)** <br/> |
|enterpriseenrollment  <br/> |3600  <br/> |(No setting)  <br/> |enterpriseenrollment.manage.microsoft.com  <br/> **This value MUST end with a period (.)** <br/> |
   
    ![Type or paste values for the new records](../media/5ce0b30c-b46c-4778-aa5a-fb5e2f0961c1.png)
  
7. When you have added all of the CNAME records that you need, choose **Continue**.
    
    ![Click Continue](../media/4978bd8b-f6a6-458d-9522-ad612b301c4a.png)
  
8. Choose **Save Changes**.
    
    ![Click Save Changes](../media/f005c38a-0d8d-4c61-bec6-15e60c89aa5a.png)
  
## Add a TXT record for SPF to help prevent email spam
<a name="BKMK_add_TXT"> </a>

> [!IMPORTANT]
> You cannot have more than one TXT record for SPF for a domain. If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues. If you already have an SPF record for your domain, don't create a new one for Office 365. Instead, add the required Office 365 values to the current record so that you have a  *single*  SPF record that includes both sets of values. Need examples? Check out these [](external-domain-name-system-records.md#BKMK_SPFrecords). To validate your SPF record, you can use one of these [SPF validation tools](92a43f6a-4651-455a-a1cc-300684bedcfa.md). 
  
Follow the steps below or [watch the video (start at 5:35)](https://support.office.com/en-us/article/Video-Create-DNS-records-at-Network-Solutions-for-Office-365-c49698c2-6991-47fb-b5ac-18e49a505099?ui=en-US&amp;rs=en-US&amp;ad=US).
  
1. To get started, go to your domains page at Network Solutions by using [this link](https://www.networksolutions.com/manage-it). You'll be prompted to log in.
    
    > [!IMPORTANT]
    > Before you choose the **Login** button, first choose **Manage My Domain Names** in the **Log In to:** drop-down list. 
  
    ![Choose Manage My Domain Names and log in to Network Solutions](../media/fda7d4a1-9445-4086-be9c-87c6983ef2aa.png)
  
2. Select the check box next to the name of the domain that you are modifying.
    
    ![Select the check box for your domain](../media/2c13d2ba-4a31-44da-812c-2cc90900a183.png)
  
3. Choose **Edit DNS**.
    
    ![Click Edit DNS](../media/9d7c269f-48d1-442c-9d7b-63bd384a36a9.png)
  
4. Choose **Manage Advanced DNS Records**.
    
    (You may have to scroll down.)
    
    ![Click Manage Advanced DNS Records](../media/fd2956d6-eec3-47ea-b60a-266bab14f51f.png)
  
5. Scroll down to the **Text (TXT Records)** section, and then choose **Edit TXT Records**.
    
    ![Click Edit TXT Records under Text](../media/a69a2631-6da2-4e81-99ab-9a9ab9b30b07.png)
  
6. In the boxes for the new record, type or copy and paste the following values.
    
|**Host**|**TTL**|**Text**|
|:-----|:-----|:-----|
|@  <br/> (The system will change this value to **@ (None)** when you save the record.)  <br/> |3600  <br/> |v=spf1 include:spf.protection.outlook.com -all  <br/> > [!NOTE]> We recommend copying and pasting this entry, so that all of the spacing stays correct.           |
   
    ![Type or paste values for the new record](../media/11564eca-e2ee-4f17-af2b-a00eb7c157db.png)
  
7. Choose **Continue**.
    
    ![Click Continue](../media/482a8dae-0c79-47c4-8bd8-87965683de24.png)
  
8. Choose **Save Changes**.
    
    ![Click Save Changes](../media/600b8c6d-184f-4213-a50e-8f119ebf3ff0.png)
  
## Add the two SRV records that are required for Office 365
<a name="BKMK_add_SRV"> </a>

Follow the steps below or [watch the video (start at 6:18)](https://support.office.com/en-us/article/Video-Create-DNS-records-at-Network-Solutions-for-Office-365-c49698c2-6991-47fb-b5ac-18e49a505099?ui=en-US&amp;rs=en-US&amp;ad=US).
  
1. To get started, go to your domains page at Network Solutions by using [this link](https://www.networksolutions.com/manage-it). You'll be prompted to log in.
    
    > [!IMPORTANT]
    > Before you choose the **Login** button, first choose **Manage My Domain Names** in the **Log In to:** drop-down list. 
  
    ![Choose Manage My Domain Names and log in to Network Solutions](../media/fda7d4a1-9445-4086-be9c-87c6983ef2aa.png)
  
2. Select the check box next to the name of the domain that you are modifying.
    
    ![Select the check box for your domain](../media/2c13d2ba-4a31-44da-812c-2cc90900a183.png)
  
3. Choose **Edit DNS**.
    
    ![Click Edit DNS](../media/9d7c269f-48d1-442c-9d7b-63bd384a36a9.png)
  
4. Choose **Manage Advanced DNS Records**.
    
    (You may have to scroll down.)
    
    ![Click Manage Advanced DNS Records](../media/fd2956d6-eec3-47ea-b60a-266bab14f51f.png)
  
5. Scroll down to the **Service (SRV Records)** section, and then choose **Edit SRV Records**.
    
    ![Click Edit SRV Records under Service](../media/9a9248ea-5de5-4e16-9364-f7600fa371f5.png)
  
6. In the boxes for the two new records, type or copy and paste the values from the following table.
    
    (Choose the **Service** and **Protocol** values from the drop-down lists.) 
    
|**Service**|**Protocol**|**TTL**|**Priority**|**Weight**|**Port**|**Target**|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|_sip  <br/> |_tls  <br/> |3600  <br/> |100  <br/> |1  <br/> |443  <br/> |sipdir.online.lync.com.  <br/> **This value MUST end with a period (.)** <br/> |
|_sipfederationtls  <br/> |_tcp  <br/> |3600  <br/> |100  <br/> |1  <br/> |5061  <br/> |sipfed.online.lync.com.  <br/> **This value MUST end with a period (.)** <br/> |
   
    ![Type or paste values for the new records](../media/86968d1c-8e43-4e61-aeaa-37fc7d7ef7a7.png)
  
7. Choose **Continue**.
    
    ![Click Continue](../media/bfe2c778-5d2b-4bb6-a79d-c3ff9caf9e1e.png)
  
8. Choose **Save Changes**.
    
    ![Click Save Changes](../media/6d323126-0ebe-45ab-8567-c234711d84c7.png)
  
> [!NOTE]
>  Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md). 
  
