---
description: Use a página Servidores na ferramenta Audience Manager Admin para criar um novo servidor HTTP ou editar um servidor existente.
seo-description: Use the Servers page in the Audience Manager Admin tool to create a new HTTP server or to edit an existing server.
seo-title: Create or Edit an HTTP Server
title: Criar ou editar um servidor HTTP
uuid: 1ef0e751-e239-4dc6-a4f6-73cc05686807
exl-id: 8b3dfb1e-2dee-4a05-835e-3c32643336bc
source-git-commit: c7c5da62b32f6a56152e1c09a965facfc601cade
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 6%

---

# Criar ou editar um servidor HTTP {#create-or-edit-an-http-server}

Use o [!UICONTROL Servers] na ferramenta Audience Manager Admin para criar um novo servidor HTTP ou editar um servidor existente.

>[!NOTE]
>
>Você deve ter o [!UICONTROL DEXADMIN] para criar novos servidores ou editar servidores existentes.

1. Para criar um novo servidor, vá para **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**. Para editar um servidor existente, clique no servidor desejado na **[!UICONTROL Label]** coluna.
1. Especifique o rótulo desejado para este servidor.
1. No **[!UICONTROL Protocol]** selecione o protocolo desejado: [!DNL HTTP].
1. Preencha os campos:

   * **[!UICONTROL Domain]:** Especifique o domínio (host) desejado para este servidor.
   * **[!UICONTROL Port]:** Especifique a porta desejada para este servidor. A porta padrão é exibida para cada tipo de criptografia. Você pode alterar a porta padrão, se necessário
   * **[!UICONTROL Maximum Users Per Request]:** Especifique o número máximo de usuários por solicitação permitido para este servidor.
   * **[!UICONTROL URL Prefix]:** Especifique a [!DNL URL] prefixo a ser usado para este servidor.
   * **[!UICONTROL Authentication URL]:** Especifique a [!UICONTROL Authentication URL] para este `HTTP` servidor.
   * **[!UICONTROL Authentication]:** Especifique o método de autenticação desejado: **[!UICONTROL None]**, **[!UICONTROL Username/Password]** ou **[!UICONTROL SSH Key]**.
   * **[!UICONTROL HTTP Signature Header]:** O nome do [!DNL HTTP] cabeçalho, fornecido pelo cliente, que contém o [!DNL HTTP] chave de assinatura. O valor padrão é [!UICONTROL X-Signature], conforme mostrado no exemplo abaixo:

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

   * **[!UICONTROL HTTP Signature Key]:** A chave usada para assinar o [!DNL HTTP] pelo cliente.
   * **[!UICONTROL Show Signature Key]:** Alternar se deseja ou não exibir a assinatura no navegador.
   * **[!UICONTROL HTTP Signature Encryption Method]:** Especifique o método que usamos para criptografar a assinatura. Uso [!UICONTROL SHA1] a menos que o cliente prefira o contrário.

   >[!NOTE]
   >
   >Se quiser ativar [Autenticação OAuth 2.0 para transferências de dados em tempo real](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/real-time-outbound-transfers/oauth-in-outbound-transfers.html?lang=en) para um parceiro, preencha os campos conforme a tabela abaixo. Os campos em *itálico* precisa ser preenchido exatamente como na tabela.

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
   | [!UICONTROL Username] | [!UICONTROL *Autorização*] |
   | [!UICONTROL Password] | sua_senha_aqui |
   | [!UICONTROL HTTP Signature Header] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Key] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Encryption Method] | [!UICONTROL None] |

1. Clique em **[!UICONTROL Create]** se estiver criando um novo servidor, ou clique em **[!UICONTROL Update]** se você estiver editando um servidor existente.
