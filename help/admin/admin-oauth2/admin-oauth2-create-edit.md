---
description: Use a página Clientes OAuth2 para exibir uma lista de clientes OAuth2 na configuração do Audience Manager. É possível editar ou excluir clientes existentes ou criar novos clientes, desde que você tenha as funções de usuário apropriadas atribuídas.
seo-description: Use a página Clientes OAuth2 para exibir uma lista de clientes OAuth2 na configuração do Audience Manager. É possível editar ou excluir clientes existentes ou criar novos clientes, desde que você tenha as funções de usuário apropriadas atribuídas.
seo-title: Clientes OAuth2
title: Clientes OAuth2
uuid: 3e654053-fb2f-4d8f-a53c-b5c3b8dbdaaa
translation-type: tm+mt
source-git-commit: 2998dc049971b2fac8c45ca6e3118ea607ae3f92

---


# Clientes OAuth2 {#oauth-clients}

Use a [!UICONTROL OAuth2 Clients] página para exibir uma lista de [!UICONTROL OAuth2] clientes na sua [!DNL Audience Manager] configuração. É possível editar ou excluir clientes existentes ou criar novos clientes, desde que você tenha as funções de usuário apropriadas atribuídas.

## Visão geral {#overview}

<!-- c_oauth.xml -->

>[!NOTE]
>
>Certifique-se de que seu cliente leia a documentação [OAuth2](https://docs.adobe.com/content/help/en/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.html#oauth) no [!DNL Audience Manager User Guide.

[!DNL OAuth2] é uma norma aberta para a autorização de conceder acesso delegado seguro aos [!DNL Audience Manager] recursos em nome de um proprietário de recursos.

![](assets/oauth.png)

É possível classificar cada coluna em ordem crescente ou decrescente clicando no cabeçalho da coluna desejada.

Use a [!UICONTROL Search] caixa ou os controles de paginação na parte inferior da lista para localizar o cliente desejado.

## Criar ou editar um cliente OAuth2 {#create-edit-client}

<!-- t_create_edit_auth.xml -->

Use a [!UICONTROL OAuth2 Clients] página na ferramenta Audience Manager [!UICONTROL Admin] para criar um novo [!UICONTROL Oauth2] cliente ou editar um cliente existente.

1. Para criar um novo [!UICONTROL OAuth2] cliente, clique em **[!UICONTROL OAuth2 Clients]** &gt; **[!UICONTROL Add OAuth2 Client]**. Para editar um [!UICONTROL OAuth2] cliente existente, clique no cliente desejado na **[!UICONTROL Client ID]** coluna.
1. Especifique o nome desejado para este [!UICONTROL OAuth2] cliente. Observe que este é um nome somente para o registro.
1. Especifique o endereço de email do [!UICONTROL OAuth2] cliente. Há um limite de um endereço de email.
1. Na lista **[!UICONTROL Partner]** suspensa, selecione o parceiro desejado.
1. Na **[!UICONTROL Client ID]** caixa, especifique a ID desejada. Esse é o valor usado ao enviar [!DNL API] solicitações. O prefixo é preenchido automaticamente quando você começa a digitar depois de escolher um item [!UICONTROL Partner] da lista suspensa na etapa anterior. O formato correto é &lt; *`partner subdomain`*&gt; - &lt; *`Audience Manager username`*&gt;.
1. Marque ou desmarque a caixa de **[!UICONTROL Restrict to Partner Users]** seleção, conforme desejado. Se essa caixa de seleção estiver selecionada, o usuário deverá ser um [!DNL Audience Manager] usuário listado para o parceiro selecionado. Como prática recomendada, recomendamos que você selecione essa opção.
1. Na **[!UICONTROL Scope]** seção, marque ou desmarque as caixas de seleção **[!UICONTROL Read]** e **[!UICONTROL Write]** , conforme desejado.
1. Na **[!UICONTROL Grant Type]** seção, selecione os meios desejados para a autorização. Recomendamos que você use as configurações padrão de [!UICONTROL Password] e [!UICONTROL Refresh-token] opções.

   * **[!UICONTROL Implicit]**: Se você selecionar essa opção, a [!UICONTROL Redirect URI] caixa será ativada. O usuário recebe um token de acesso automático depois de ser autenticado e é enviado imediatamente para o redirecionamento [!DNL URI].
   * **[!UICONTROL Authorization Code]**: Se você selecionar essa opção, a [!UICONTROL Redirect URI] caixa será ativada. O usuário é retornado ao cliente depois de ser autenticado e, em seguida, enviado para o redirecionamento [!DNL URI].
   * **[!UICONTROL Password]**: O usuário é autenticado com uma senha digitada pelo usuário em vez de uma tentativa de validação automática por meio de um servidor de autorização.
   * **[!UICONTROL Refresh_token]**: Usado para atualizar um token de acesso expirado por um período de tempo prolongado.

1. Na **[!UICONTROL Redirect URI]** caixa, especifique o desejado [!DNL URI]. Essa opção é ativada somente se você selecionar os tipos de concessão **[!UICONTROL Implicit]** e **[!UICONTROL Authorization_code]** . A **[!UICONTROL Redirect URI]** caixa permite especificar um valor separado por vírgulas de [!DNL URI] valores aceitáveis. Este é o [!DNL URI] usuário para o qual um cliente é redirecionado após aprovar o cliente para [!DNL API] acesso.
1. Especifique o tempo de expiração desejado (em segundos) para acesso e atualização da expiração do token.

   * **[!UICONTROL Access Token Expiration Time]**: O número de segundos em que um token de acesso é válido após ser emitido. Pode ser nulo para usar o padrão da plataforma (12 horas). Também pode ser -1 para indicar que o token de acesso não expira.
   * **[!UICONTROL Refresh Token Expiration Time]**: O número de segundos em que um token de atualização é válido após ser emitido. Pode ser nulo para usar o padrão da plataforma (30 dias).

1. Clique em **[!UICONTROL Save]**.

Para excluir um [!UICONTROL OAuth2] cliente, clique em **[!UICONTROL OAuth2 Clients]** e, em seguida, clique ![](assets/icon_delete.png) na **[!UICONTROL Actions]** coluna do cliente desejado.

>[!MORELIKETHIS]
>
>* [Requisitos e recomendações da API](../admin-oauth2/aam-admin-api-requirements.md)

