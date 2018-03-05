---

copyright:
  years: 2017, 2018
lastupdated: "2018-01-11"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# Explorar los equilibradores de carga

IBM Cloud ofrece varias soluciones de equilibrio de carga entre las que elegir. La siguiente tabla compara las distintas soluciones de equilibrio de carga para ayudarle a elegir la más adecuada para usted. Para obtener más información sobre una oferta, pulse sobre su nombre en la tabla. 

Desplácese a la derecha para visualizar el resto de la tabla.


|        | [IBM Cloud Load Balancer](https://console.bluemix.net/docs/infrastructure/loadbalancer-service/getting-started.html#getting-started)| [Equilibrador de carga local](https://console.bluemix.net/docs/infrastructure/local-load-balancer/getting-started.html#getting-started) (compartido)| [Equilibrador de carga local](https://console.stage1.bluemix.net/docs/infrastructure/local-load-balancer/getting-started.html#getting-started) (dedicado)| [Citrix NetScaler](https://console.bluemix.net/docs/infrastructure/citrix-netscaler-vpx/getting-started.html#getting-started-with-citrix-netscaler) VPX/MPX (Estándar)| [Citrix NetScaler](https://console.bluemix.net/docs/infrastructure/citrix-netscaler-vpx/getting-started.html#getting-started-with-citrix-netscaler) VPX/MPX (Platinum) |
|------- | :------: | :------: | :------: | :------: | :------: |
|**VIP público**|Sí|Sí|Sí|Sí|Sí|
|**VIP privado**|No|No|Sí|Sí|Sí|
|**Capa de 4 LB**|Sí|Sí|Sí|Sí|Sí|
|**Capa de 7 LB**|No|Persistencia de cookies|Persistencia de cookies|Sí|Sí|
|**Comprobaciones de estado**|Sí|Sí|Sí|Sí|Sí|
|**Descarga SSL**|Sí|Sí|Sí|Sí|Sí|
|**Gestión**|a través de IBM Portal|a través de IBM Portal|a través de IBM Portal|Auto-gestión (GUI del proveedor)|Auto-gestión (GUI del proveedor)|
|**Alta disponibilidad**|Integrada|Integrada|Opcional|Opcional|Opcional|
|**LB avanzado (optimización de TCP, compresión, almacenamiento en memoria caché, WAF)**|No|No|No|Limitado|Sí|
|**LB global (GLB)**|No|No|No|No|Sí|
|**Precios**|Basado en uso|Tarifa mensual|Tarifa mensual|Tarifa mensual|Tarifa mensual|
