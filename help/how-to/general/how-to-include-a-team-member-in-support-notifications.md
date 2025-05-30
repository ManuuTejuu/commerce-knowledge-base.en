---
title: How to include a team member in Support notifications
description: This article provides an explanation of how to include a team member in Support notifications.
feature: Cloud, Support, Admin Workspace
role: Admin, Developer
exl-id: 63ea3f60-a509-447c-ac3d-bb2133141c80
---
# How to include a team member in Support notifications

This article provides an explanation of how to include a team member to automatically receive Support updates via email notifications.

## Affected products and versions

* Adobe Commerce on cloud infrastructure, all [supported versions](https://www.adobe.com/content/dam/cc/en/legal/terms/enterprise/pdfs/Adobe-Commerce-Software-Lifecycle-Policy.pdf).

## Cause

* The team member has not been added to the [!DNL cloud project] with the necessary privileges.
* The team member doesn't have a Support account.

## Solution

1. Go to the **[!DNL Cloud Project URL]** (Example: `https://us-3.magento.cloud/projects/xxxxxx/edit`).
1. Verify whether the team member has been added to the project and is a [!DNL Super User].

If they have not been added to the project, you will need to add them as a [!DNL Super User] and grant [!DNL Shared Access]:

* [Manage user access](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) in our user guide.
* [Unable to add user to Adobe Commerce cloud project](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/unable-add-user-adobe-commerce-cloud-project.html) in our Commerce Knowledge Base.
* [Adobe Commerce Help Center User Guide: Shared Access](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#shared-access) in our Commerce Knowledge Base.

If they have been added to the [!DNL cloud project], but don't have the [!DNL Super User role], update their [!DNL role] accordingly in [Manage user access](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html).

If you wish to enable a team member to be a watcher on all cases opened for your organization, submit a [Support ticket](https://experienceleague.adobe.com/home?lang=en&support-tab=home#support).

## Related reading

[Former team members receive Adobe Commerce cloud notification emails](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/former-teammembers-receive-cloud-notification-emails.html)
