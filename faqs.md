---

copyright:
  years: 2017
lastupdated: "2018-03-14"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# FAQs

This section contains answers to some frequently asked questions about the IBM Cloud Load Balancer Service.

## How many load balancing options are available in {{site.data.keyword.BluSoftlayer_notm}}?

For a detailed comparison of IBM's Load Balancer offerings, refer to [Explore Load Balancers](https://dev-console.bluemix.net/docs/infrastructure/loadbalancer-service/explore-load-balancers.html#explore-load-balancers).

## Can I use a different DNS name for my load balancer?

While the auto-assigned DNS name for the load balancer is not customizable, you can add a CNAME (Canonical Name) record that points your preferred DNS name to the auto-assigned load balancer DNS name. For example, your account number is 123456, your load balancer is deployed in "dal09" datacenter and its name is "myapp", the auto-assigned load balancer DNS name is "myapp-123456-dal09.lb.bluemix.net". Your preferred DNS name is "www.myapp.com". You may add a CNAME record (via the DNS provider that you use to manage myapp.com) pointing "www.myapp.com" to the load balancer DNS name "myapp-12345-dal09.lb.bluemix.net".

## What's the maximum number of virtual ports I can define with my load balancer service?

While trying to create a new load balancer service, you may define up to two virtual ports. You can define additional virtual ports after the service is created. The maximum number of virtual ports allowed is 10. 

## What's the maximum number of compute instances I can associate with my load balancer?

50.

## What are the default settings and allowed values for various health check parameters?

The default settings and allowed values are listed below:

* **Health check interval:** Default is 5 seconds, range is 2 – 60 seconds
* **Health check response timeout:** Default is 2 seconds, range is 1 – 59 seconds
* **Max retry attempts:** Default is 2 retry attempts, range is 1 to 10 retry attempts

**NOTE:** The health check response timeout value must always be less than the health check interval value. 

## Can I use compute instances residing in remote data centers with this service? 

We recommend that your load balancer service and your compute instances reside locally within the same data center. The load balancer service’s graphical interface (GUI) will not show compute instances from other remote data centers. However, the GUI will include compute instances from other data centers within the same city (for example, data centers whose names share the first three letters, such as DALxx). You may use the API interface to add compute instances from any remote data center, though. 

## Which TLS version is supported with SSL offload?

The Cloud Load Balancer Service supports TLS 1.2 with SSL termination. 

The following list details the supported ciphers (listed in order of precedence):  

* ECDHE-RSA-AES256-GCM-SHA384
* ECDHE-RSA-AES256-SHA384
* AES256-GCM-SHA384
* AES256-SHA256
* ECDHE-RSA-AES128-GCM-SHA256
* ECDHE-RSA-AES128-SHA256
* AES128-GCM-SHA256
* AES128-SHA256

## What is the maximum number of Load Balancer service instances I can create within my account? 

Currently, you may create up to 20 service instances. If you need more instances, please contact IBM Support. 

## Can the IBM Cloud Load Balancer Service be used with VMWare? 

VMWare virtual machines that are assigned SoftLayer portable private addresses can be specified as backend servers to the load balancer. This feature is currently available only using the API, and not the web UI (GUI). Portable private IPs added using the API appear as "Unknown" in the GUI, as they are not assigned by SoftLayer. Note that this kind of configuration can be used with other Hypervisors such as Xen and KVM as well.

VMWare virtual machines assigned non-SoftLayer addresses (such as VMWare NSX networks) cannot be added directly as backend servers to the load balancer. However, depending on your configuration, it may be possible to configure an intermediary, such as an NSX gateway, that has a SoftLayer private address as the backend server to the load balancer (with the actual servers being VMs attached to network(s) managed by VMware NSX).

## If I choose to use a public VLAN under my account to deploy my load balancer and I have a firewall deployed on my public VLAN, what configurations are required on my firewall to work with my load balancer service?

TCP port 56501 is used for management. Please ensure that traffic to this port, as well as your application's ports, are not blocked by your firewall, otherwise load balancer provisioning will fail.

## What do I need to do when I get an error "This SoftLayer account is not linked to any Bluemix account"?

Ensure that your SoftLayer account is linked with your Bluemix account. Refer to [Softlayer Link](https://console.bluemix.net/docs/account/softlayerlink.html#switching-to-ibmid) for further instructions.
