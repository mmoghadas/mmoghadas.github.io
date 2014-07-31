---
title: How to install Homebrew on OSX Lion
author: Mike Moghadas
layout: post
permalink: /?p=371
categories:
  - Linux
  - Mac
tags:
  - brew
  - homebrew
  - Linux
  - OSX
---
Homebrew is a tool that allow you to install some missing open-source packages in OSX. This of Homebrew as apt-get for OSX.  It&#8217;s also an alternative to Port, but I think this just works better.

Assuming you&#8217;re installing Homebrew on OSX Lion, you&#8217;ll need the following:

- OSX Lion  
- Xcode (Can be installed via AppStore)  
- Xcode Command Line Tools (You&#8217;ll need an Apple Developers Account)

<!--more-->

**To install Xcode Command Line Tools**  
Launch Xcode > Preferences > Downloads > Command Line Tools > Install

**To install Homebrew**  
From Terminal  
[crayon lang="sh" toolbar="true" nums="false"]  
/usr/bin/ruby -e &#8220;$(/usr/bin/curl -fksSL https://raw.github.com/mxcl/homebrew/master/Library/Contributions/install_homebrew.rb)&#8221;  
[/crayon]

Now you should be able to install available Unix Tools.  
**To install packages**  
[crayon lang="sh" toolbar="true" nums="false"]  
brew install <tool_name>  
brew install git  
[/crayon]