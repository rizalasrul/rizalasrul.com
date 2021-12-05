---
title: 'Configure web service security using htaccess'
date: '2015-06-08'
tags: ['linux', 'networking', 'htaccess']
ShowToc: false
---

The Apache Web server has a variety of configuration options for administrators. The problem is, when you have hosting, you don't have access to the apache configuration. As a result you cannot make changes to settings and are forced to use the default configuration. One alternative that can be done to overriding the default configuration is to do the settings via the .htaccess file.

The .htaccess file is an ASCII file placed in the www directory or www subdirectory. You can create this file via a text editor such as notepad and upload it in ASCII (not BINARY) format in whichever directory you want to modify the settings. Additionally, the file permissions are set as 644 (rw-r–r–). Its function is to allow servers to access files, but prevent visitors from accessing files via their browsers for security reasons.

For more details, please see [here](http://1drv.ms/1MBEeK5).
