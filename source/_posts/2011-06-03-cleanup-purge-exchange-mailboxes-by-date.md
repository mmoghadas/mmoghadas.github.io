---
title: Cleanup (Purge) Exchange Mailboxes by date
author: Mike Moghadas
layout: post
permalink: /?p=279
categories:
  - Exchange
  - Windows
tags:
  - Exchange 2010
  - Mailbox
  - Purge
  - Windows 2008R2
---
**To cleanup an Exchange Mailbox and delete messages older than a certain date:**

Logon to Exchange Management Shell  
[crayon lang="sh" toolbar="true" nums="false"]  
Search-Mailbox -Identity “mailbox_name” -SearchQuery “Received:> $(’10/01/2008′) and Received:< $(’10/05/2010′)” -EstimateResultOnly  
Search-Mailbox -Identity “mailbox_name” -SearchQuery “Received:> $(’10/01/2008′) and Received:< $(’10/05/2010′)” -DeleteContent  
[/crayon]