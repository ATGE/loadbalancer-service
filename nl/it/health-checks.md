---

copyright:
  years: 2017, 2018
lastupdated: "2018-11-12"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# Controlli di integrità

Le definizioni del controllo di integrità sono obbligatorie per ogni porta dell'applicazione di backend. La porta e il protocollo nella configurazione del controllo di integrità devono corrispondere alla porta e al protocollo di backend, altrimenti la configurazione viene rifiutata. 

Il programma di bilanciamento del carico effettua controlli di integrità periodici per monitorare l'integrità delle porte di backend e inoltra il traffico client ad esse di conseguenza. Se una porta del server di backend specificata viene trovata non integra, non viene più inoltrata alcuna nuova connessione ad essa. Il programma di bilanciamento del carico continua a monitorare l'integrità di queste porte non integre e riprende ad utilizzarle se vengono trovate nuovamente integre dopo aver superato due tentativi di controllo di integrità consecutivi. 

I controlli di integrità per le porte HTTP e TCP vengono eseguiti nel seguente modo:

* **HTTP:** viene inviata una richiesta `HTTP GET` per un URL pre-specificato alla porta del server di backend. La porta del server viene contrassegnata come integra se viene ricevuta una risposta `200 OK`. Il `GET` URL predefinito è “/” tramite la GUI e può essere personalizzato. 

* **TCP:** il programma di bilanciamento del carico tenta di aprire una connessione TCP con il server di backend su una porta TCP specificata. La porta del server viene contrassegnata come integra se il tentativo di connessione ha esito positivo e la connessione viene quindi chiusa. 

	**NOTA:** l'intervallo del controllo di integrità è 5 secondi, il timeout predefinito per una richiesta del controllo di integrità è 2 secondi e il numero di nuovi tentativi predefinito è 2. 
