---
layout: post
title:  Useful Commands for Server
---


### How to check the process that is using a specific port?

Speficy the port number as you wish. Here we use 8080.

	$ netstat -nlptu |awk '{print $4,$7}' | grep 8080
	
	
	
	
_More will be added here..._

PPS: Question: How to write Markdown instruction with Markdown Language? Must be very inconvient...