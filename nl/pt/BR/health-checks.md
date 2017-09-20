---

copyright:
  years: 2017
lastupdated: "2017-08-21"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# Verificações de funcionamento

As definições de verificação de funcionamento são obrigatórias para cada uma das portas do aplicativo backend. A porta e o protocolo na configuração de verificação de funcionamento deverão corresponder à porta e ao protocolo de backend definidos, caso contrário, a configuração será rejeitada. 

O balanceador de carga realiza verificações de funcionamento periódicas para monitorar o funcionamento das portas backend e encaminha o tráfego do cliente para elas adequadamente. Se uma determinada porta do servidor de backend for encontrada inoperante, nenhuma nova conexão será encaminhada para ela. O balanceador de carga continuará monitorando o funcionamento dessas portas inoperantes e continuará seu uso se novamente se tornarem funcionais passando com sucesso por duas tentativas de verificação de funcionamento consecutivas. 

As verificações de funcionamento em portas HTTP e TCP são realizadas conforme a seguir:

* **HTTP:** uma solicitação de `HTTP GET` em uma URL pré-especificada é enviada para a porta do servidor de backend. A porta do servidor é marcada como funcional ao receber uma resposta `200 OK`. A URL `GET` padrão é "/" por meio da GUI e pode ser customizada. 

* **TCP:** o Balanceador de carga tenta abrir uma conexão TCP com o servidor de backend em uma porta TCP especificada. A porta do servidor será marcada como funcional se a tentativa de conexão for bem-sucedida e a conexão será então encerrada. 

	**NOTA:** o intervalo de verificação de funcionamento padrão é de 5 segundos, o tempo limite padrão em uma solicitação de verificação de funcionamento é de 2 segundos e o número padrão de novas tentativas é 2. 
