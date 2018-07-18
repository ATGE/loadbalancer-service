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

# SSL 卸載

對於所有送入的 HTTPS 連線，負載平衡器服務會終止 SSL 連線，並建立與後端伺服器的純文字 HTTP 通訊。CPU 密集 SSL 信號交換及加密/解密作業會從後端伺服器移開，如此可讓它們使用其所有 CPU 週期來處理應用程式資料流量。 

需要有 SSL 憑證，負載平衡器才能執行 SSL 卸載作業。您可以使用預先存在的 SSL 憑證或購買新的 SSL 憑證，然後透過 [IBM Cloud 憑證庫](https://control.softlayer.com/security/sslcerts)進行管理。 

# SSL 密碼組合
負載平衡器服務支援 TLS 1.2 版搭配 SSL 卸載。

您的負載平衡器支援下列 SSL 密碼：

* ECDHE-RSA-AES256-GCM-SHA384
* ECDHE-RSA-AES256-SHA384
* AES256-GCM-SHA384
* AES256-SHA256
* ECDHE-RSA-AES128-GCM-SHA256
* ECDHE-RSA-AES128-SHA256
* AES128-GCM-SHA256
* AES128-SHA256

如果您的負載平衡器已配置一個以上的 HTTPS 前端應用程式埠（通訊協定），則依預設，將針對您的負載平衡器啟用所有上述預先定義的 SSL 密碼。您可能選擇必要時針對負載平衡器啟用不同的 SSL 密碼。
