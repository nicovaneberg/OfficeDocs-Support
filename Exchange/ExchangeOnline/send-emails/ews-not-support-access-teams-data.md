---
title: EWS isn't supported when accessing Teams data
description: Describes an issue in which EWS isn't supported for accessing Teams data. EWS is supported only by using Microsoft Graph API.
author: cloud-writer
ms.author: meerak
manager: dcscontentpm
audience: ITPro
ms.topic: troubleshooting
ms.custom: 
  - sap:Mail Flow
  - Exchange Online
  - CI 119824
  - CSSTroubleshoot
ms.reviewer: danba, v-six
appliesto: 
  - Exchange Online
search.appverid: 
  - MET150
ms.date: 03/06/2024
---
# EWS isn't supported when accessing Teams data

## Summary

Microsoft Exchange Web Services (EWS) and other messaging application programming interfaces (API) aren't supported when you access the Microsoft Teams data that's stored in a user's mailbox. Third-party applications aren't allowed to access or use Teams data in mailboxes. Teams can change its location and use of data at any time. Therefore, using email APIs such as EWS, Exchange REST, MAPI, or Outlook Object Model makes the process vulnerable to code failure.

Access to Teams data is supported only by Microsoft Graph. Fully supported access to Teams message data is available through the [Microsoft Teams Export APIs](/microsoftteams/export-teams-content). Teams Export APIs enable you to export one-on-one (1:1) chats, group chats, meeting chats, and channel messages from Microsoft Teams.

## More information

If your organization's applications have to export Microsoft Teams messages, you can extract them by using the [Teams Export APIs](/microsoftteams/export-teams-content). For more information about the API references for Microsoft Teams, see [Use the Microsoft Graph API to work with Microsoft Teams](/graph/api/resources/teams-api-overview). You can also subscribe to change notifications by [creating a subscription](/graph/api/subscription-post-subscriptions) for Teams resources.
