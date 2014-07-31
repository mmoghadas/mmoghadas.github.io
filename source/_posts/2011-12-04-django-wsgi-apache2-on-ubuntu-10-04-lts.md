---
title: Django, WSGI, Apache2 on Ubuntu 10.04 LTS
author: Mike Moghadas
layout: post
categories:
  - Linux
  - Web Server
tags:
  - apache
  - Django
  - wsgi
---
Install Apache2  
[crayon lang="sh" toolbar="true" nums="false"]  
sudo apt-get install apache2  
[/crayon]

<!--more-->

Install MOD_WSGI  
[crayon lang="sh" toolbar="true" nums="false"]  
sudo apt-get install libapache2-mod-wsgi  
[/crayon]

Install Python (Installed by default, but just in case)  
[crayon lang="sh" toolbar="true" nums="false"]  
sudo apt-get install python  
[/crayon]

Install Python Setup Tools  
[crayon lang="sh" toolbar="true" nums="false"]  
sudo apt-get install python-setuptools  
[/crayon]

Install Django  
[crayon lang="sh" toolbar="true" nums="false"]  
apt-get install python-pip  
pip install django  
[/crayon]
