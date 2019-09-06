---
description: Use a página Servidores na ferramenta de Administração do Audience Manager para criar um novo servidor HTTP ou editar um servidor existente.
seo-description: Use a página Servidores na ferramenta de Administração do Audience Manager para criar um novo servidor HTTP ou editar um servidor existente.
seo-title: Criar ou editar um servidor HTTP
title: Criar ou editar um servidor HTTP
uuid: 1 ef 0 e 751-e 239-4 dc 6-a 4 f 6-73 cc 05686807
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# Criar ou editar um servidor HTTP {#create-or-edit-an-http-server}

Use [!UICONTROL Servers] a página na ferramenta de administração do Audience Manager para criar um novo servidor HTTP ou editar um servidor existente.

>[!NOTE]
>
>Você deve ter [!UICONTROL DEXADMIN] a função para criar novos servidores ou editar servidores existentes.

1. Para criar um novo servidor, vá **[!UICONTROL Servers]** para &gt; **[!UICONTROL Create Server]**. Para editar um servidor existente, clique no servidor desejado na **[!UICONTROL Label]** coluna.
1. Especifique o rótulo desejado para este servidor.
1. Na lista **[!UICONTROL Protocol]** suspensa, selecione o protocolo desejado: [!DNL HTTP].
1. Preencha os campos:

   * **[!UICONTROL Domain]:** Especifique o domínio desejado (host) para este servidor.
   * **[!UICONTROL Port]:** Especifique a porta desejada para este servidor. A porta padrão é exibida para cada tipo de criptografia. Você pode alterar a porta padrão, se necessário.
   * **[!UICONTROL Maximum Users Per Request]:** Especifique o número máximo de usuários por solicitação permitida para este servidor.
   * **[!UICONTROL URL Prefix]:** Especifique o [!DNL URL] prefixo a ser usado para este servidor.
   * **[!UICONTROL Authentication URL]:** Especifique o [!UICONTROL Authentication URL] para este `HTTP` servidor.
   * **[!UICONTROL Authentication]:** Especifique o método de autenticação desejado: **[!UICONTROL None]**, **[!UICONTROL Username/Password]** ou **[!UICONTROL SSH Key]**.
   * **[!UICONTROL HTTP Signature Header]:** O nome do [!DNL HTTP] cabeçalho, fornecido pelo cliente, que contém a chave [!DNL HTTP] de assinatura. O valor padrão é [!UICONTROL X-Signature], como mostrado no exemplo abaixo:

      ```
      * Connected to partner.website.com (127.0.0.1) port 80 (#0)
      > POST /webpage HTTP/1.1
      > Host: partner.host.com
      > Accept: */*
      > Content-Type: application/json
      > Content-Length: 20
      > X-Signature: wxa2ByMWhhP328EvHQsVlOD5jTc=
      POST message content
      ```

   * **[!UICONTROL HTTP Signature Key]:** A chave usada para assinar [!DNL HTTP] a solicitação, fornecida pelo cliente.
   * **[!UICONTROL Show Signature Key]:** Alterne se deseja exibir a assinatura no navegador.
   * **[!UICONTROL HTTP Signature Encryption Method]:** Especifique o método usado para criptografar a assinatura. Use [!UICONTROL SHA1] a menos que o cliente prefere.
   >[!NOTE]
   >
   >Se você quiser ativar a autenticação [oauth 2.0 para transferências de dados em tempo real](https://docs.adobe.com/help/en/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/real-time-outbound-transfers/oauth-in-outbound-transfers.html) de um parceiro, preencha os campos como na tabela abaixo. Os campos em *itálico* precisam ser preenchidos exatamente como na tabela.

   | Nome | Valor |
   |---|---|
   | [!UICONTROL Label] | [!UICONTROL Server with OAuth 2.0 enabled] |
   | [!UICONTROL Protocol] | [!UICONTROL HTTP] |
   | [!UICONTROL Domain] | [!UICONTROL api.partner.com] |
   | [!UICONTROL Port] | [!UICONTROL 443] |
   | [!UICONTROL Maximum Users per Request] | [!UICONTROL 10] |
   | [!UICONTROL URL Prefix] | [!UICONTROL /segments/aam] |
   | [!UICONTROL Authentication URL] | [!UICONTROL api.partner.com/oauth2/token] |
   | [!UICONTROL Authentication] | [!UICONTROL Username/Password] |
   | [!UICONTROL Username] | [!UICONTROL *Autorização *] |
   | [!UICONTROL Password] | your_ password_ here |
   | [!UICONTROL HTTP Signature Header] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Key] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Encryption Method] | [!UICONTROL None] |

1. Clique **[!UICONTROL Create]** em se estiver criando um novo servidor ou clique **[!UICONTROL Update]** em caso esteja editando um servidor existente.