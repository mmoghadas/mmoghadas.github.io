---
title: F5 Log shipping to syslog server
author: Mike Moghadas
layout: post
permalink: /?p=286
categories:
  - Networking
tags:
  - F5
  - syslog
---
**To send a copy of your logs to a central log server from your F5:**

Logon to CLI and Issue the following commands  
[crayon lang="sh" toolbar="true" nums="false"]  
bigpipe syslog remote server {logs101 {host 10.10.10.99} }  
bigpipe save  
[/crayon]