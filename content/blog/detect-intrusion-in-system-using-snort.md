---
title: 'Detect intrusion in system using snort'
date: '2015-05-30'
tags: ['linux', 'networking', 'snort']
ShowToc: false
---

Intrusion detection is an activity to detect an intrusion quickly by using a special automatic program. The program used is usually called the Intrusion Detection System (IDS). Previously we have reviewed about host-based IDS [here](/blog/configure-tripwire-as-host-based-ids/).

The basic types of IDS are:

* Rule-based system – based on a database of known insertion marks or attacks. If the IDS records traffic that matches the existing database, it is immediately categorized as an intrusion.
* Adaptive system – uses more sophisticated methods. Not only based on the existing database, but also opens the possibility to detect new forms of intrusion.

This time we will try a new program for IDS, namely snort. There are three modes in Snort, namely:

1. **Sniffer mode**, to see packets passing through the network.
2. **Packet logger mode**, to record all packets that pass through the network for analysis in the future.
3. **Intrusion Detection mode**, in this mode snort will function to detect attacks carried out through computer networks. To use this IDS mode, it is necessary to setup various rules that will distinguish a normal packet from a packet that carries an attack.

For more details please see [here](https://onedrive.live.com/redir?resid=48dcd38b3e3b9734!728&authkey=!AD3pr3CkPaVA4so&ithint=file%2cpdf).
