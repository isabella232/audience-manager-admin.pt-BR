---
description: Use a página Clientes OAuth2 para exibir uma lista de clientes OAuth2 na configuração de Audience Manager. É possível editar ou excluir clientes existentes ou criar novos clientes, contanto que você tenha as funções de usuário apropriadas atribuídas.
seo-description: Use the OAuth2 Clients page to view a list of OAuth2 clients in your Audience Manager configuration. You can edit or delete existing clients or create new clients, providing that you have the appropriate user roles assigned.
seo-title: OAuth2 Clients
title: Clientes OAuth2
uuid: 3e654053-fb2f-4d8f-a53c-b5c3b8dbdaaa
exl-id: 993eae04-02e8-4554-a6fe-cf599053bfc9
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 1%

---

# Clientes OAuth2 {#oauth-clients}

Use o [!UICONTROL OAuth2 Clients] página para exibir uma lista de [!UICONTROL OAuth2] clientes em seu [!DNL Audience Manager] configuração. É possível editar ou excluir clientes existentes ou criar novos clientes, contanto que você tenha as funções de usuário apropriadas atribuídas.

## Visão geral {#overview}

<!-- c_oauth.xml -->

>[!NOTE]
>
>Certifique-se de que o cliente leia a [OAuth2](https://experienceleague.adobe.com/docs/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.html#oauth) no Guia do usuário do Audience Manager.

[!DNL OAuth2] é uma norma aberta para a autorização de fornecer acesso delegado seguro a [!DNL Audience Manager] recursos em nome de um proprietário de recurso.

![](assets/oauth.png)

Você pode classificar cada coluna em ordem crescente ou decrescente clicando no cabeçalho da coluna desejada.

Use o [!UICONTROL Search] ou nos controles de paginação na parte inferior da lista para encontrar o cliente desejado.

## Criar ou editar um cliente OAuth2 {#create-edit-client}

<!-- t_create_edit_auth.xml -->

Use o [!UICONTROL OAuth2 Clients] página no Audience Manager [!UICONTROL Admin] ferramenta para criar um novo [!UICONTROL Oauth2] cliente ou para editar um cliente existente.

1. Para criar um novo [!UICONTROL OAuth2] cliente, clique em **[!UICONTROL OAuth2 Clients]** > **[!UICONTROL Add OAuth2 Client]**. Para editar um existente [!UICONTROL OAuth2] cliente, clique no cliente desejado na caixa **[!UICONTROL Client ID]** coluna.
1. Especifique o nome desejado para este [!UICONTROL OAuth2] cliente. Observe que esse é um nome somente para o registro.
1. Especifique a [!UICONTROL OAuth2] endereço de email do cliente. Há um limite de um endereço de email.
1. No **[!UICONTROL Partner]** selecione o parceiro desejado.
1. No **[!UICONTROL Client ID]** especifique a ID desejada. Este é o valor usado ao enviar [!DNL API] solicitações. O prefixo é preenchido automaticamente quando você começa a digitar depois de escolher um [!UICONTROL Partner] na lista suspensa na etapa anterior. O formato correto é &lt; *`partner subdomain`*> - &lt; *`Audience Manager username`*>.
1. Marque ou desmarque a opção **[!UICONTROL Restrict to Partner Users]** conforme desejado. Se esta caixa de seleção estiver marcada, o usuário deverá ser um [!DNL Audience Manager] usuário listado para o parceiro selecionado. Como prática recomendada, selecione essa opção.
1. No **[!UICONTROL Scope]** selecione ou desmarque a opção **[!UICONTROL Read]** e **[!UICONTROL Write]** caixas de seleção, conforme desejado.
1. No **[!UICONTROL Grant Type]** selecione o meio de autorização desejado. Recomendamos que você use as configurações padrão de [!UICONTROL Password] e [!UICONTROL Refresh-token] opções.

   * **[!UICONTROL Implicit]**: Se você selecionar essa opção, a variável [!UICONTROL Redirect URI] está ativada. O usuário recebe um token de acesso automático após a autenticação e é enviado imediatamente para o redirecionamento [!DNL URI].
   * **[!UICONTROL Authorization Code]**: Se você selecionar essa opção, a variável [!UICONTROL Redirect URI] está ativada. O usuário é retornado ao cliente após ser autenticado e, em seguida, enviado para o redirecionamento [!DNL URI].
   * **[!UICONTROL Password]**: o usuário é autenticado com uma senha inserida pelo usuário em vez de uma tentativa de validação automática por meio de um servidor de autorização.
   * **[!UICONTROL Refresh_token]**: usado para atualizar um token de acesso expirado por um período de tempo estendido.

1. No **[!UICONTROL Redirect URI]** especifique o valor desejado [!DNL URI]. Essa opção só será ativada se você selecionar a opção **[!UICONTROL Implicit]** e **[!UICONTROL Authorization_code]** tipos de concessão. A variável **[!UICONTROL Redirect URI]** permite especificar um valor de aceitável separado por vírgulas [!DNL URI] valores. Este é o [!DNL URI] um usuário de um cliente é redirecionado para o depois de aprovar o cliente para [!DNL API] acesso.
1. Especifique o tempo de expiração desejado (em segundos) para a expiração do token de acesso e atualização.

   * **[!UICONTROL Access Token Expiration Time]**: O número de segundos que um token de acesso é válido após ser emitido. Pode ser nulo para usar o padrão da plataforma (12 horas). Além disso, pode ser -1 para indicar que o token de acesso não expira.
   * **[!UICONTROL Refresh Token Expiration Time]**: O número de segundos que um token de atualização é válido após ser emitido. Pode ser nulo para usar o padrão da plataforma (30 dias).

1. Clique em **[!UICONTROL Save]**.

Para excluir um [!UICONTROL OAuth2] cliente, clique em **[!UICONTROL OAuth2 Clients]** e, em seguida, clique em  ![](assets/icon_delete.png) no **[!UICONTROL Actions]** para o cliente desejado.

>[!MORELIKETHIS]
>
>* [Requisitos da API e recomendações](../admin-oauth2/aam-admin-api-requirements.md)

