---
title: 'Configuring web services security (SSL/TLS) using OpenSSL'
date: '2015-06-05'
tags: ['linux', 'networking', 'openssl']
ShowToc: false
---

Transport Layer Security (TLS) adalah protokol untuk mengamankan komunikasi antar aplikasi lewat internet. TLS mengamankan konten pada layer aplikasi, seperti halaman web dan diimplementasikan pada layer transport, yaitu TCP. Untuk menjamin keamanan, data yang dikirim dienkripsi dan diotentikasi pada sisi server dan client. Secure Socket Layer (SSL) adalah protocol yang diciptakan sebelum TLS yang mengaplikasikan hal ini.

SSL/TLS is usually operated together with HTTP, thus forming a new protocol called HTTPS, to secure transactions over the web. In addition, this protocol can be used for other applications such as email, file transfer and virtual private networks (VPN).

This time we will try to use OpenSSL to create your own certificate in the browser. For more details can be seen [here](https://onedrive.live.com/redir?resid=48dcd38b3e3b9734!730&authkey=!ALHf-8dl4VDcWTY&ithint=file%2cpdf).
