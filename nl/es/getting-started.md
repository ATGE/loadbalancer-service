---

copyright:
  years: 2017
lastupdated: "2018-04-13"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}


# Guía de inicio
Para empezar a utilizar IBM Cloud Load Balancer necesitará dos elementos principales:

* Una cuenta con IBM: [IBMid](https://www.ibm.com/account/us-en/signup/register.html)
* Un servidor IBM, ya sea [nativo](https://console.bluemix.net/docs/bare-metal/about.html#getting-started-with-bare-metal-servers) o [una instancia de servidor virtual (VSI)](https://console.bluemix.net/docs/vsi/vsi_index.html#getting-started-with-virtual-servers)
 
Si necesita ayuda para obtener una cuenta de **IBMid**, póngase en contacto con su [representante de ventas de IBM](https://www.ibm.com/cloud-computing/bluemix/contact-us) para obtener instrucciones adicionales.

Si tiene una cuenta de infraestructura de IBM Cloud (SoftLayer) existente, puede [enlazar su cuenta](https://console.bluemix.net/docs/account/softlayerlink.html#unifyingaccounts) con el IBMid. 

## Realizar un pedido de un equilibrador de carga

Para realizar un pedido de un servicio IBM Cloud Load Balancer, seleccione **Red > Load Balancers > IBM Cloud Load Balancer** en el [catálogo de IBM Cloud](https://console.bluemix.net/catalog/infrastructure/load-balancer-group). Inicie la sesión o cree una cuenta nueva y, a continuación, realice el procedimiento siguiente:

1. Seleccione el centro de datos y revise el plan de servicio. Pulse **Siguiente**.
2. Seleccione la subred en la que desee desplegar el equilibrador de carga. La instancia del servicio de equilibrador de carga tendrá una de las interfaces de red en esta subred. Asegúrese de que los servidores de aplicaciones estén en esta subred o sean accesibles desde la misma. Si es necesario, habilite la expansión de VLAN. Pulse **Siguiente**.
3. Defina los parámetros de servicio básicos, como nombre, descripción, protocolos y puertos de aplicación frontal y back-end y método de equilibrio de carga. Puede definir un máximo de dos protocolos durante la creación inicial del servicio. Puede definir hasta diez protocolos después de haber creado el servicio. Además debe utilizar un puerto frontal exclusivo. Pulse **Siguiente**.
4. Ajuste los parámetros de la comprobación de estado si lo desea; de lo contrario, utilice los valores predeterminados. Pulse **Siguiente**.
5. Asocie una o más instancias de servidor detrás del equilibrador de carga. Solo verá las instancias del servidor local en su centro de datos. Pulse **Siguiente**.
6. Revise la página de resumen y, a continuación, pulse **Crear**. 


La página de resumen muestra la instancia del servicio de equilibrador de carga que se acaba de crear. Observe el campo **Estado**. El estado `Offline` significa que el equilibrador de carga no está en servicio. No se pueden crear configuraciones ni se puede proporcionar servicio de equilibrio de carga hasta que el estado cambie a `Online`. Puede que tenga que actualizar la pantalla para ver el estado actual.
 
Al pulsar el nombre de servicio en la página, irá a la página de visión general del servicio. Puede desplazarse por los separadores **Protocolos**, **Comprobaciones de estado** e **Instancias de servidor** para editar la configuración existente.
