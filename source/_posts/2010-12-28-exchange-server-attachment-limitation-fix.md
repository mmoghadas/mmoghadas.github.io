---
title: Exchange Server Attachment Limitation Fix
author: Mike Moghadas
layout: post
permalink: /?p=292
categories:
  - Exchange
  - Windows
tags:
  - Attachments
  - Exchange 2010
  - OWA
---
**Problem**  
On a new Exchange installation Mail Clients might fail to send large attachments. This is doe to the default values set by OWA, IMAP, EWS.

**Fix**  
1. Run the following commands from c:windowssystem32inetsrv

<!--more-->

[crayon lang="sh" toolbar="true" nums="false"]  
appcmd set config “Default Web Site/ews” -section:requestFiltering -requestLimits.maxAllowedContentLength:30000000  
appcmd set config “Default Web Site/owa” -section:requestFiltering -requestLimits.maxAllowedContentLength:30000000  
appcmd set config “Default Web Site/Microsoft-Server-Activesync” -section:requestFiltering -requestLimits.maxAllowedContentLength:30000000  
[/crayon]

2. Edit C:Program FilesMicrosoftExchange ServerV14ClientAccessexchwebewsweb.config and Modify  
[crayon lang="sh" toolbar="true" nums="false"]  
<httpRuntime maxRequestLength=”2097151″ />  
to  
<httpRuntime executionTimeout=”1200″ maxRequestLength=”30720″ />  
[/crayon]

3. Edit C:Program FilesMicrosoftExchange ServerV14ClientAccessexchwebewsweb.config and Modify  
[crayon lang="sh" toolbar="true" nums="false"]  
<EWSMessageEncoderSoap11Element />  
<httpsTransport maxReceivedMessageSize=”13600000″ authenticationScheme=”Anonymous” maxBufferSize=”81920″ transferMode=”Streamed”>  
to  
<EWSMessageEncoderSoap11Element />  
<httpsTransport maxReceivedMessageSize=”31457280″ authenticationScheme=”Anonymous” maxBufferSize=”81920″ transferMode=”Streamed”>  
[/crayon]

4. Edit C:Program FilesMicrosoftExchange ServerV14ClientAccessOwaweb.config and Modify  
[crayon lang="sh" toolbar="true" nums="false"]  
</system.webServer>  
<system.web>  
<httpRuntime maxRequestLength=”30000″ />  
to  
</system.webServer>  
<system.web>  
<httpRuntime maxRequestLength=”30000″ />  
[/crayon]