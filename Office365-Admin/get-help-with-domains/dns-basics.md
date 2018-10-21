---
title: "DNS basics"
ms.author: pebaum
author: pebaum
manager: mnirkhe

ms.audience: Admin
ms.topic: get-started-article
f1_keywords:
- 'TADNSbasics'
- 'O365P_DomainsSetup_WhyNeedDNSRecs'
- 'O365P_DNSMgrUI_AboutDNS'
- 'O365M_DomainsSetup_WhyNeedDNSRecs'
- 'O365E_DomainsSetup_WhyNeedDNSRecs'
ms.service: o365-administration
localization_priority: Priority
search.appverid:
- MET150
- MOE150
- GEA150
- BSA160
ms.assetid: 854b6b2b-0255-4089-8019-b765cff70377
description: "Learn about domains and their associated DNS records to help you manage your Office 365 domains."
---

# DNS basics

 **[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for. 
  
::: moniker range="o365-worldwide"

Domain names, like contoso.com, are managed by using a worldwide system of domain registrars and databases. The Domain Name System (DNS) provides a mapping between human-readable computer hostnames and the IP addresses used by networking equipment. An understanding of DNS and domain registrar basics can help you manage domains in Office 365.
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/c005f2a4-90ad-46fe-b1ab-90f41f2a9d53?autoplay=false]
  
::: moniker-end

::: moniker range="o365-germany"

Domain names, like contoso.com, are managed by using a worldwide system of domain registrars and databases. The Domain Name System (DNS) provides a mapping between human-readable computer hostnames and the IP addresses used by networking equipment. An understanding of DNS and domain registrar basics can help you manage domains in Office 365.
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/c005f2a4-90ad-46fe-b1ab-90f41f2a9d53?autoplay=false]
  
::: moniker-end

::: moniker range="o365-21vianet"

Domain names, like contoso.com, are managed by using a worldwide system of domain registrars and databases. The Domain Name System (DNS) provides a mapping between human-readable computer hostnames and the IP addresses used by networking equipment. An understanding of DNS and domain registrar basics will help admins manage domains in Office 365 operated by 21Vianet.
  
::: moniker-end

> [What are domain names?](#what-are-domain-names)
    
> [Understand DNS record types](#understand-dns-record-types)
    
> [How does DNS work?](#how-does-dns-work)
    
> [Why add a domain in Office 365?](#why-add-a-domain-in-office-365)
    
> [The DNS records required for Office 365](#the-dns-records-required-for-office-365)
> [How can I learn more?](#how-can-i-learn-more)
    
## What are domain names?
<a name="__toc386183972"> </a>

Domain names are used in URLs and email addresses, and they have different levels. For example, mail.contoso.com is a domain name with the following three levels:
  
- **.com** is the top-level domain 
    
- **contoso** is the second-level domain 
    
- **mail** is the third-level domain 
    
Why use a third-level domain? You might want to have different domain names for marketing or a blog. For example, blog.contoso.com. You typically add a second-level domain, like contoso.com, to use with Office 365 but you can also use third-level domains if you like.
  
Learn more about what you can do with domains for each type of offering in the [Office 365 service description for domains](https://go.microsoft.com/fwlink/?LinkId=402693).
  
## Understand DNS record types
<a name="__toc386183973"> </a>

DNS records stored at a DNS host for your domain are used to direct traffic for your domain. The following table describes frequently used DNS records and how they're used with Office 365.
  
|**NS (nameserver) record**|**Identifies the name servers that are the "authoritative nameservers" for a domain. When you change the nameservers for your domain, you change where your DNS records are managed and where the DNS system looks for information about mail servers and so on. Office 365 has its own nameservers, or you may decide to keep using the nameservers that are already set up with your domain.**|
|:-----|:-----|
|A record (address record)  <br/> |Associates a domain name with an IP address.  <br/> |
|CNAME (alias or canonical) record  <br/> |Redirects one domain to another in the DNS system. When a name server looks up a domain and finds that it has a CNAME record, the server replaces the first domain name with the CNAME, and then looks up the new name.  <br/> |
|MX (mail exchanger) record  <br/> |Points to where your email should be sent. It also has a priority field so that you can send mail to different servers in a priority order.  <br/> |
|SPF (sender policy framework) record  <br/> |A TXT record that helps prevent email spoofing and phishing.  <br/> |
|SRV (service) record  <br/> |Used by Skype for Business Online and Exchange Online to coordinate the flow of information between Office 365 services. For example, the SRV records are required to see presence in Outlook Web App, and to use Skype for Business Online, Skype, or other instant messaging tools with people in other companies.  <br/> |
|TTL (time-to-live)  <br/> |The amount of time that a nameserver keeps a DNS record before the server looks for an updated version.  <br/> |
   
## How does DNS work?
<a name="__toc386183974"> </a>

Part of setting up your domain with a cloud service like Office 365 includes changing or adding [DNS records](dns-basics.md) for the domain. These changes are required because of how the Internet works with the DNS, Domain Name System, and domain names, to know where to send or find things, like email and websites. 
  
The Internet is set up to use DNS, or Domain Name System, which lets us use familiar names, like contoso.com, to locate specific Internet locations that are actually, under the covers, labeled with hard-to-remember numbers called IP (Internet Protocol) addresses. IP addresses look something like 70.42.241.42, so you can see it's much easier to use a domain name to identify locations like email hosts and websites.
  
So that's the short answer: DNS records tell the Internet where to send email (like joe@contoso.com) or find websites (like www.contoso.com) that use your domain name. When you put the right information into the right DNS records for your domain, the DNS system routes everything correctly so your email, for example, arrives in Office 365 instead of somewhere else.
  
A domain's DNS records can be helpful in other ways, too. For example, Exchange checks a DNS record that lets Outlook automatically set up a connection to the right Exchange server.
  
### DNS records help the Internet send email to the right place

As you read above, DNS essentially directs traffic around the Internet, mapping friendly domain names to those hard-to-remember IP addresses. One DNS record, called the MX record, is specifically for sending email to the right host.
  
DNS records are like a database of information about your domain. The records and their values are kept in something called a zone file, which includes a list of each record for your domain and what its value is. Domain registrars and other DNS hosting companies provide a UI on their websites so you can edit the records in your domain's zone file. And that's where you update the MX record for your domain, to send email messages to Office 365.
  
 *When you change your email to Office 365, by updating your domain's MX record in the next step, ALL email sent to that domain will start coming to Office 365.*  If other people use your domain for email, you must set up Office 365 mailboxes for each of those people. 
  
Sound complicated? Well, it can be, but we walk you through each step in the Office 365 domain setup.
  
### DNS tells the Internet where to look for websites too

When you type in a website address, for example, www.contoso.com, the Internet first checks with one of the DNS servers for something called a name server (NS) record for (in this case) contoso.com. The NS record tells the Internet where it should look for the zone file that has all the other DNS record values for that domain. There are lots of DNS servers, all connected to each other. The servers work together to keep track of all registered domain names, which have to be unique, and where the domain's zone files are.
  
::: moniker range="o365-worldwide"

Let's say that the NS record for contoso.com says "godaddy.com." Now the Internet knows that GoDaddy.com is where to look for the zone file listing all the other DNS records for contoso.com. Those DNS records include the MX record that says where to send emails for contoso.com and other records. If the MX record has a value that says (but in technical terms) "send email to Office 365," that's where all the email messages sent to a contoso.com email address (like joe@contoso.com) will be sent. Then, as long as there's a mailbox called "joe" at that location, the email will be delivered.

::: moniker-end

::: moniker range="o365-germany"

Let's say that the NS record for contoso.com says "godaddy.com." Now the Internet knows that GoDaddy.com is where to look for the zone file listing all the other DNS records for contoso.com. Those DNS records include the MX record that says where to send emails for contoso.com and other records. If the MX record has a value that says (but in technical terms) "send email to Office 365," that's where all the email messages sent to a contoso.com email address (like joe@contoso.com) will be sent. Then, as long as there's a mailbox called "joe" at that location, the email will be delivered.

::: moniker-end

::: moniker range="o365-21vianet"

Let's say that the NS record for contoso.com says "hichina.com." Now the Internet knows that hichina.com is where to look for the zone file listing all the other DNS records for contoso.com. Those DNS records include the MX record that says where to send emails for contoso.com and other records. If the MX record has a value that says (but in technical terms) "send email to Office 365," that's where all the email messages sent to a contoso.com email address (like joe@contoso.com) will be sent. Then, as long as there's a mailbox called "joe" at that location, the email will be delivered.

::: moniker-end

The actual values that you must enter for all of this to work with Office 365 are listed for you when you're setting up your domain, in the domain setup steps. If you're doing the set up manually, you copy and paste the values into the correct DNS records (MX record, CNAME records, and so on) at your DNS host, which might be your domain registrar but doesn't have to be.
  
::: moniker range="o365-worldwide"

Why might your domain's zone file be somewhere besides at your domain registrar? Well, you might register your domain name at a domain registrar like GoDaddy, but your DNS records might be managed somewhere else, at a separate DNS hosting company or a web hosting company. The NS records for your domain store that information so all the DNS servers know where to look.

::: moniker-end

::: moniker range="o365-germany"

Why might your domain's zone file be somewhere besides at your domain registrar? Well, you might register your domain name at a domain registrar like GoDaddy, but your DNS records might be managed somewhere else, at a separate DNS hosting company or a web hosting company. The NS records for your domain store that information so all the DNS servers know where to look.

::: moniker-end

::: moniker range="o365-21vianet"

Why might your domain's zone file be somewhere besides at your domain registrar? Well, you might register your domain name at a domain registrar like HiChina, but your DNS records might be managed somewhere else, at a separate DNS hosting company or a web hosting company. The NS records for your domain store that information so all the DNS servers know where to look.

::: moniker-end

> [!NOTE]
> If you set up your domain in Office 365 so that [Office 365 sets up and manages your DNS records](https://support.office.com/article/5980474a-097f-4f21-a864-21245314957f.aspx) for you, then as part of setup, you'll [change your domain's NS records to point to Office 365 name servers](https://support.office.com/article/b3627432-6872-4645-9cb7-5528bf32d6b5.aspx). 
 

::: moniker range="o365-worldwide"
## Why add a domain in Office 365?
<a name="__toc386183974"> </a>



Adding a custom domain, like fourthcoffee.com, to Office 365 lets you use a shorter, more familiar email address and userID with the service. You're [given a domain to use](https://support.office.com/article/b9fc3018-8844-43f3-8db1-1b3a8e9cfd5a.aspx) when you sign up for a Office 365 account, but it includes "onmicrosoft.com." Many people prefer to add their organization or business domain if they plan to use Office 365 for email. 
  
> [!NOTE]
> If you just want to download and use Office 365 apps, like Outlook or Word, you don't need to add a domain: [Install Office on your PC or Mac](https://support.office.com/article/4414eaaf-0478-48be-9c42-23adc4716658.aspx). 
  
You can use your domain name in Office 365 with your email, public website, and instant messaging address.
  
- **Email:** Your domain name lets you customize your email, so you can use a shorter, easier-to-remember address than [the initial onmicrosoft.com email address](https://support.office.com/article/b9fc3018-8844-43f3-8db1-1b3a8e9cfd5a.aspx) that comes with your account. So instead of joe@contoso.onmicrosoft.com, the email address (which is also the work account that you use to sign in to Office 365) could be joe@contoso.com. 
    
- **Website:** If you have an Office 365 subscription that includes a SharePoint Online Public Website (no longer available for purchase), your public website comes with an initial address like this: contoso-public.sharepoint.com. If you set up your website for your business, you can use a custom domain name to rename the website address to something like www.contoso.com. 
    
- **Instant messaging:** Your Skype for Business Online address can also be customized to use your domain name, so people in your organization can connect with each other on Skype for Business Online by using a shorter, easier-to-remember address (like joe@contoso.com). 
    
::: moniker-end

::: moniker range="o365-germany"
## Why add a domain in Office 365?
<a name="__toc386183974"> </a>



Adding a custom domain, like fourthcoffee.com, to Office 365 lets you use a shorter, more familiar email address and userID with the service. You're [given a domain to use](https://support.office.com/article/b9fc3018-8844-43f3-8db1-1b3a8e9cfd5a.aspx) when you sign up for a Office 365 account, but it includes "onmicrosoft.com." Many people prefer to add their organization or business domain if they plan to use Office 365 for email. 
  
> [!NOTE]
> If you just want to download and use Office 365 apps, like Outlook or Word, you don't need to add a domain: [Install Office on your PC or Mac](https://support.office.com/article/4414eaaf-0478-48be-9c42-23adc4716658.aspx). 
  
You can use your domain name in Office 365 with your email, public website, and instant messaging address.
  
- **Email:** Your domain name lets you customize your email, so you can use a shorter, easier-to-remember address than [the initial onmicrosoft.com email address](https://support.office.com/article/b9fc3018-8844-43f3-8db1-1b3a8e9cfd5a.aspx) that comes with your account. So instead of joe@contoso.onmicrosoft.com, the email address (which is also the work account that you use to sign in to Office 365) could be joe@contoso.com. 
    
- **Website:** If you have an Office 365 subscription that includes a SharePoint Online Public Website (no longer available for purchase), your public website comes with an initial address like this: contoso-public.sharepoint.com. If you set up your website for your business, you can use a custom domain name to rename the website address to something like www.contoso.com. 
    
- **Instant messaging:** Your Skype for Business Online address can also be customized to use your domain name, so people in your organization can connect with each other on Skype for Business Online by using a shorter, easier-to-remember address (like joe@contoso.com). 
    
::: moniker-end

## The DNS records required for Office 365
<a name="__toc386183977"> </a>

There are a number of DNS records required for Office 365 to work with your domain. In addition to setting up your domain's MX record so email will be sent to Office 365, there are records to help with tasks like making sure Outlook can automatically connect to the right Exchange server, setting up instant messaging, and helping to prevent spam email.
  
You can [find a list of values](information-for-dns-records.md) to set up your domain. They're included right in the Office 365 portal. 
  
Or, if you're planning a deployment, you may want to review a list of all the DNS records required for Office 365, what their function is, and example values. Check out [External Domain Name System records for Office 365](https://support.office.com/article/c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0).
  
## How can I learn more?
<a name="bkmk_learnmore"> </a>

[Get help with using domains in Office 365](get-help-with-domains.md) or check out one of the following: 
  
- Not sure where your domain is registered? [Get help finding your domain registrar.](find-your-domain-registrar.md)
    
- [Learn what you should have on hand](https://support.office.com/article/5aaa52a3-ab4e-4a4e-80d8-dc5d4d80c8d1.aspx) before you get started setting up your domain in Office 365. 
    
- Find out [why you have to complete the wizard steps](https://support.office.com/article/c4207bb0-9ed5-4149-a9dd-f617e1477824.aspx) before you can use your domain with Office 365. 
    

