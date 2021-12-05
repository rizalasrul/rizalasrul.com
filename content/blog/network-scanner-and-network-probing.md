---
title: 'Network Scanner and Network Probing'
date: '2015-05-30'
tags: ['linux', 'networking', 'scanner', 'probing']
ShowToc: false
---

The second phase in ethical hacking is the network scanning phase. Network scanning is the phase where a hacker identifies hosts, ports, and services on the target network.

In socket-based programming, the server is the host that provides a service and the client is the host that accesses or uses the service. Socket itself is a combination of IP address and port number, for example is the mail service that uses socket `202.9.85.49:25`.

This time we will scan the ports (port scanning) that are open on a host.

Network services can be attacked in a variety of ways. The service application itself may have several weaknesses such as programming errors, use of weak authentication/passwords, unencrypted sensitive data or allowing connections from various IP addresses and so on. These vulnerabilities allow the host providing the service to be vulnerable to attack. Therefore, the host should only provide the necessary services, or in other words, minimize the open ports.

There are several types of scanning using nmap, namely:

* Connect scan (-sT).
* TCP SYN scan (-sS).
* TCP FIN scan (-sF).
* TCP Xmas Tree scan (-sX).
* TCP Null scan (-sN).
* TCP ACK scan (-sA).
* TCP Windows scan.
* TCP RPC scan.

For more details, please see [here](https://onedrive.live.com/redir?resid=48dcd38b3e3b9734!726&authkey=!AEWWmAyvt_JdblY&ithint=file%2cpdf).
