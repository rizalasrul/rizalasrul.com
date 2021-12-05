---
title: 'Configure Tripwire As Host-based IDS'
date: '2015-04-30'
tags: ['linux', 'networking', 'ids']
ShowToc: false
---

IDS, or Intrusion Detection System is a program aimed at detecting and monitoring the state of network anomalies caused by one of them by intruders (intruders). After the detection stage, usually the IDS can be set to alert network administrators.

IDS types are broadly divided into two, namely host-based and network-based. This time we will discuss one program from host-based IDS, namely tripwire. The tripwire program functions to maintain the integrity of system files and directories, by recording every change that occurs in files and directories.

The way tripwire works is by comparing existing files and directories with the system database that was created when tripwire was installed. The comparison includes date changes, file sizes, deletions, and more. After tripwire is run, it will automatically create the system database. Then it will periodically report any changes to files and directories.

For more details, please see the link [here](https://onedrive.live.com/redir?resid=48dcd38b3e3b9734!725&authkey=!AJI7aYW-XJxELkc&ithint=file%2cpdf).
