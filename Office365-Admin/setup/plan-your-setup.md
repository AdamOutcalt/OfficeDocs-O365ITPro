---
title: "Plan your setup of Office 365 for business"
ms.author: cmcatee
author: cmcatee-MSFT
manager: mnirkhe
audience: Admin
ms.topic: get-started-article
f1_keywords:
- 'O365P_1stInfoRqrd'
- 'O365P_1stDNSHoster'
ms.service: o365-administration
localization_priority: Normal
ms.collection: 
- M365-subscription-management
- Adm_O365
- Adm_TOC
- Adm_O365_Setup
search.appverid:
- MET150
- MOE150
ms.assetid: eb926624-018b-4486-bf11-5fba6ee4d645
description: "Learn what what you need to do to set up your Office 365 for business."
---

# Plan your setup of Office 365 for business

This article is for people who have subscribed to an Office 365 business plan.
  
There are a few things you need to decide, and info you need to have on hand, before moving your business to Office 365.
  
## Info to have on hand before you run the Office 365 setup wizard

When you're ready to run the Office 365 setup wizard and move your domain to Office 365, here's the info you'll need to have on hand:
  
- List of people you want to add to Office 365. Even if you've already added them to Office 365, if you're updating your domain information, you need to enter their names here.

- How you're going to notify your employees of their Office 365 user ID and password so they can sign in. Are you going to call them with the info? Or send it to their personal email address? They won't have access to their Office 365 email, so you can't use that.

- If you have a domain name for your business (such as contoso.com) **and** you plan on using Office 365 email, you'll need to know where your domain is registered and have sign-in information.

## What happens when you run the Office 365 setup wizard

The setup wizard walks you through installing the Office 365 apps on your computer, adding and verifying your domain, adding users and assigning licenses to them, and connecting your domain.

> [!NOTE]
> If you need to [Assign admin roles in Office 365 for business](../add-users/assign-admin-roles.md) to the users you add in the wizard, you can do that later on the **Users** page. 
  
Now you can go to [admin center](https://go.microsoft.com/fwlink/p/?linkid=2024339) > **Setup**, where you can migrate email and contacts from another email service, change the domain of your admin account, manage your billing information, add or remove users, reset passwords, and do other business functions. For more information about the differences between the setup wizard and The Setup page, see [Differences between the Office 365 setup wizard and the setup page](o365-setup-wizard-and-setup-page.md)

If you get stuck at any point, call us. [We're here to help!](../contact-support-for-business-products.md)
  
## When not to use the setup wizard: Active Directory synchronization and hybrid environments

There are a couple of scenarios that include either migrating data or users from on-premises environments or setting up a hybrid system that includes directory synchronization. If you are in either category, follow the instructions in these articles:
  
- To set up directory synchronization with your on-premises Active Directory, see [Set up directory synchronization for Office 365](https://docs.microsoft.com/office365/enterprise/set-up-directory-synchronization), and to understand the different identity models in Office 365, read [Understanding Office 365 identity and Azure Active Directory](https://docs.microsoft.com/office365/enterprise/about-office-365-identity).

- To set-up an Exchange hybrid, the full set of instructions that guide you through all the different ways of setting up a hybrid exchange (including setting up DNS records) can be found here: [Exchange Server Deployment Assistant](https://aka.ms/exdeploy)

- To set up a SharePoint hybrid, particularly hybrid search and site features, see [Hybrid Search in SharePoint](https://docs.microsoft.com/SharePoint/hybrid/hybrid-search-in-sharepoint).

## Move to Office 365 all at once or in stages

- **Do you want to move your business to Office 365 all at once?** If so, then plan to move your domain to Office 365 right away. Start by running the Office 365 setup wizard; it will prompt you to set up your domain.

- **Or do you want to move to Office 365 gradually?** If you want to move to Office 365 in stages, then skip running the Office 365 setup wizard and consider adopting Office 365 features in the following order:

1. [Add your employees to Office 365](../add-users/add-users.md) so they can download and install the Office apps.

2. [Download and install the Office apps](https://support.office.com/article/4414eaaf-0478-48be-9c42-23adc4716658.aspx) to use Word, Excel, and PowerPoint on your computer and devices.

3. [Set up Microsoft Teams](#plan-for-teams) to use for your meetings.

4. [Move your content to Office 365 cloud storage](set-up-file-storage-and-sharing.md) (OneDrive or team sites).

5. And, when you're ready, in the [admin center](https://go.microsoft.com/fwlink/p/?linkid=2024339), select **Setup** in the left navigation pane, and use the Setup page to [move your domain and email](add-domain.md).

## Check that your devices meet system requirements

Each person in your business can install the Office 2016 suite of apps (Word, Excel, PowerPoint, and so on) on up to 5 PCs and Macs. See the operating system and computer requirements for installing [Office 2016 suites](https://go.microsoft.com/fwlink/?LinkId=534827) for business.
  
Mobile apps can be installed on iOS, Android, and Windows devices. You can find information on mobile device and browser support in [System requirements for Office](https://go.microsoft.com/fwlink/?LinkId=534827).
  
## Plan for email

If you're planning to move from an existing email service to Office 365, it usually takes 2 days to make the switch.
  
### Plan for email downtime
  
If you're going to use Office 365 for your email:
  
- To move your business email address (such as *rob@contoso.com*) from another email service to Office 365, you need to direct your mail to be delivered to your new Office 365 mailbox. You do this by selecting **Migrate your users' data** on the Setup page, where we guide you through the updates you need to make at your domain host, step by step.

- After you update your domain host, the changes typically take effect in just an hour or two. But be aware that it can sometimes take up to 72 hours for the changes to update across the internet.

- Because you might have email downtime, we recommend you plan to switch to Office 365 email during an evening or weekend when you receive fewer emails.

### Plan to move your existing email, contacts, and calendar
  
If you're going to use Office 365 for your email account, you can bring your existing email, contacts, and calendar with you. The Office 365 setup page helps you move your existing email and contacts for most scenarios. We also have step-by-step guides to move one or many mailboxes.
  
|**How many mailboxes?**|**Recommendation**|
|:-----|:-----|
|Just a few  <br/> |If you don't want to use the Setup page to migrate the mailboxes, you can let mailbox owners migrate their own email and contacts. See [Migrate email and contacts to Office 365 for business](migrate-email-and-contacts-admin.md).  <br/> |
|Several  <br/> |If you are migrating from Gmail, see [Migrate G Suite mailboxes to Office 365](https://docs.microsoft.com/Exchange/mailbox-migration/migrating-imap-mailboxes/migrate-g-suite-mailboxes).  <br/> If you are migrating from another email provider, including Exchange, see [Ways to migrate multiple email accounts to Office 365](https://docs.microsoft.com/Exchange/mailbox-migration/mailbox-migration).  <br/> |

## Plan for file storage and migration

Office 365 provides cloud storage for individuals, small businesses, and enterprises. For guidance about what to store where, see [Where you can store documents in Office 365](https://support.office.com/article/c7c20284-bc94-47f4-9728-d28e9daf0790.aspx).
  
- **You can move hundreds files** to [OneDrive](https://support.office.com/article/45114744-6D42-45CD-8975-F9617819BDEB.aspx) or to an Office 365 [team site](https://support.office.com/article/da549fb1-1fcb-4167-87d0-4693e93cb7a0.aspx#__toc384119242). You can upload 100 files at a time. Avoid uploading files larger than 2GB, which is the maximum file size by default.
  
- **If you want to move several thousand files** to Office 365 storage, review the [SharePoint Online Limits](https://go.microsoft.com/fwlink/p/?LinkID=856113). We recommend that you use a migration tool or consider hiring a [partner](https://go.microsoft.com/fwlink/?linkid=391089) to help you with the migration. For information about how to migrate a large number of files, see [SharePoint Online and OneDrive Migration User Guide](https://go.microsoft.com/fwlink/?LinkId=723574).
  
## Plan for Teams

You can use Microsoft Teams to make calls to other people in your business who are on your subscription. For example, if your business has 10 people, you can call and IM each other using Teams without any special setup. For more information, see [Get started with Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/get-started-with-teams-quick-start).

For larger organizations or if you are starting from Skype for Business, on-premises, or hybrid deployments, see [How to roll out Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/how-to-roll-out-teams).
  
## Plan for integration with Active Directory or other software

- **Do you want to integrate with your on-premises Active Directory?** You can integrate your on-premises Active Directory with Office 365 by using Azure Active Directory Connect. For instructions, see [Set up directory synchronization for Office 365](https://docs.microsoft.com/office365/enterprise/set-up-directory-synchronization).
  
- **Do you want to integrate Office 365 with software made by other companies?** If you need to integrate Office 365 with other software in your business, we recommend you consider [hiring a partner](https://go.microsoft.com/fwlink/?linkid=391089) to help you with your deployment.
  
## Do you want someone to help you set up Office 365?

- **If you have fewer than 50 employees:**

  - **Ask for help and we'll call you**. After you buy Office 365, you can access your Microsoft 365 admin center (you don't need to run setup to get to it). At the bottom of your admin center page, select **Need help?** Describe your problem, and we'll call you. 
  - **Call [Office 365 for Business Support](../contact-support-for-business-products.md) with your questions**. We're here to help! 
  - **Consider hiring a [Microsoft partner](https://go.microsoft.com/fwlink/?linkid=391089)**. If you're short on time, or have advanced requirements (like moving thousands of files to Office 365 cloud storage or integrating with other software), an experienced partner can be a big help. 

- **If you have more than 50 employees**, the [FastTrack Onboarding Center](https://go.microsoft.com/fwlink/?LinkId=517115) is available to help you with your deployment. 
