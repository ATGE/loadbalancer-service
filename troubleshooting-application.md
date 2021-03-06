---

copyright:
  years: 2018
lastupdated: "2018-08-30"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# Application Server Troubleshooting
This topic provides information on common issues you may encounter while using the load balancer.

## The back-end server is unhealthy
If your back-end server's health is failing, try verifying the following list to try and fix it:

* Does the port of the configured back-end protocol match the port your application is listening on?
* Does the configured health-check have the correct protocol (TCP or HTTP), port, and URL (for HTTP) information? For HTTP, ensure your application responds with `200 OK` for the configured health check URL.
* Is the back-end server on a different subnet than the load balancer? If not, ensure that VLAN spanning is enabled.
* Is the back-end server a virtual server with an enabled security group? If so, ensure that the security group rules allow traffic between the load balancer and the virtual server.