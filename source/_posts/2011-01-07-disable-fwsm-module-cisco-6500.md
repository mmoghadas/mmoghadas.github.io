---
title: Disable FWSM Module Cisco 6500
author: Mike Moghadas
layout: post
permalink: /?p=283
categories:
  - Cisco
  - Networking
tags:
  - cisco
  - FWSM
  - Router
---
**To disable the FWSM Module on a Cisco 6500:**

Logon to Router  
[crayon lang="sh" toolbar="true" nums="false"]  
enable  
hw-module module 1 shutdown  
sh hw-module slot 1 tech-support  
[/crayon]