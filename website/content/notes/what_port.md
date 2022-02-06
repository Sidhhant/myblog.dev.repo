---
title: "Port Flow"
date: 2022-02-06T22:25:27+09:00
draft: true
authorImage: "images/ProfilePic.jpg"
---

Port Connection Flow

Port 80: Default http 
Port 443: Default https (TLS encrypted)
Port 53: Default DNS 

This flow is when your brower wants to connect to a site example.com for the very first time and your local DNS is unencrypted.

As browser doesn't know the IP address related to example.com it will do a DNS query which will connect to default DNS port 53. Then it will try to connect via HTTP to example.com but will receive header that example.com would prefer to connect on HTTPS. So finally it will connect to its defalut HTTPS port 443.

<div class="mermaid">
graph LR;
  Browser-->53;
  53-->80;
  80-->443;
</div>
<script async src="https://unpkg.com/mermaid@8.2.3/dist/mermaid.min.js"></script>

Reference: [What port is it?](https://www.youtube.com/watch?v=XtIDFaFU_po)