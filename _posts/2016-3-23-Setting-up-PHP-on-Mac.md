---
layout: post
title:  Setting up PHP on Mac
---

Mac already has apache and php

#### Run Apache

	sudo apachectl start
	
It redirects to /Library/WebServer/Documents

#### Configure PHP

	sudo vi /etc/apache2/httpd.conf
	
In the config file, uncomment

	#LoadModule php5_module libexec/apache2/libphp5.so
	
	
Reference: http://blog.csdn.net/jdj_1027/article/details/7732578