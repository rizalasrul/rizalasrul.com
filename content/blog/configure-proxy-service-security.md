---
title: 'Configure proxy service security'
date: '2015-05-30'
tags: ['linux', 'networking', 'proxy']
ShowToc: false
---

Proxies are generally used to provide caching services to the local network using the Squid cache. Proxy clients do not need to directly access the web page they are going to, but simply by retrieving them in the server cache (proxy).

The way it works is that when a client accesses a web address, Squid will store the web page files in the proxy's local cache and then give it back to the client who accesses the same web page, when a client accesses the same web page. , the proxy server only checks to the destination server, whether the objects stored in the local proxy cache are still the same as those on the destination web server, if it turns out that there has been a change then the proxy server requests it for clients who access the destination web server, meanwhile the files given to the client will also be stored in the cache directory on the proxy server, and so on so that indirectly this method will save bandwidth and will indirectly speed up internet connections, in addition to the above functions the proxy server can also be used to create security policies for local networks. . The proxy server also has a function to block certain sites and block some words that are not allowed to be accessed.

The most popular proxy server application used is Squid, because Squid has a good level of performance and relatively better security than other proxy server applications.

Authentication on Squid can be used to limit which users can access the proxy server and which users are allowed, to enable authentication we need an authenticator who will handle authentication, one of which is by using RADIUS as proxy user authentication.

More details see [here](https://onedrive.live.com/redir?resid=48dcd38b3e3b9734!729&authkey=!ANMSEOAUPH2nXTs&ithint=file%2cpdf).
