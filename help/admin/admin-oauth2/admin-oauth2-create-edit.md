---
description: Use a página Clientes OAuth2 para exibir uma lista de clientes OAuth2 em sua configuração de Audience Manager. Você pode editar ou excluir clientes existentes ou criar novos clientes, desde que tenha as funções de usuário apropriadas atribuídas.
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

Use a página [!UICONTROL OAuth2 Clients] para visualizar uma lista de clientes [!UICONTROL OAuth2] em sua configuração [!DNL Audience Manager]. Você pode editar ou excluir clientes existentes ou criar novos clientes, desde que tenha as funções de usuário apropriadas atribuídas.

## Visão geral {#overview}

<!-- c_oauth.xml -->

>[!NOTE]
>
>Certifique-se de que o cliente leia a documentação [OAuth2](https://experienceleague.adobe.com/docs/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.html#oauth) no Guia do Usuário do Audience Manager.

[!DNL OAuth2] é uma norma aberta de autorização para proporcionar acesso delegado seguro a  [!DNL Audience Manager] recursos em nome de um proprietário de recursos.

![](assets/oauth.png)

Você pode classificar cada coluna em ordem crescente ou decrescente clicando no cabeçalho da coluna desejada.

Use a caixa [!UICONTROL Search] ou os controles de paginação na parte inferior da lista para localizar o cliente desejado.

## Criar ou editar um cliente OAuth2 {#create-edit-client}

<!-- t_create_edit_auth.xml -->

Use a página [!UICONTROL OAuth2 Clients] na ferramenta Audience Manager [!UICONTROL Admin] para criar um novo cliente [!UICONTROL Oauth2] ou editar um cliente existente.

1. Para criar um novo cliente [!UICONTROL OAuth2], clique em **[!UICONTROL OAuth2 Clients]** > **[!UICONTROL Add OAuth2 Client]**. Para editar um cliente [!UICONTROL OAuth2] existente, clique no cliente desejado na coluna **[!UICONTROL Client ID]**.
1. Especifique o nome desejado para este cliente [!UICONTROL OAuth2]. Observe que esse é um nome somente para o registro.
1. Especifique o endereço de email do cliente [!UICONTROL OAuth2]. Existe um limite de um endereço de email.
1. Na lista suspensa **[!UICONTROL Partner]**, selecione o parceiro desejado.
1. Na caixa **[!UICONTROL Client ID]**, especifique a ID desejada. Esse é o valor usado ao enviar solicitações [!DNL API]. O prefixo é preenchido automaticamente ao começar a digitar depois de escolher um [!UICONTROL Partner] na lista suspensa na etapa anterior. O formato correto é &lt; *`partner subdomain`* - &lt; *`Audience Manager username`*>.
1. Marque ou desmarque a caixa de seleção **[!UICONTROL Restrict to Partner Users]**, conforme desejado. Se esta caixa de seleção estiver selecionada, o usuário deve ser [!DNL Audience Manager] usuário listado para o parceiro selecionado. Como prática recomendada, recomendamos que você selecione essa opção.
1. Na seção **[!UICONTROL Scope]**, marque ou desmarque as caixas de seleção **[!UICONTROL Read]** e **[!UICONTROL Write]**, conforme desejado.
1. Na seção **[!UICONTROL Grant Type]**, selecione os meios desejados para autorização. Recomendamos que você use as configurações padrão das opções [!UICONTROL Password] e [!UICONTROL Refresh-token].

   * **[!UICONTROL Implicit]**: Se você selecionar essa opção, a  [!UICONTROL Redirect URI] caixa será ativada. O usuário recebe um token de acesso automático depois de ser autenticado e é enviado imediatamente para o redirecionamento [!DNL URI].
   * **[!UICONTROL Authorization Code]**: Se você selecionar essa opção, a  [!UICONTROL Redirect URI] caixa será ativada. O usuário é retornado ao cliente depois de ser autenticado e é enviado ao redirecionamento [!DNL URI].
   * **[!UICONTROL Password]**: O usuário é autenticado com uma senha digitada pelo usuário em vez de uma tentativa de validação automática por meio de um servidor de autorização.
   * **[!UICONTROL Refresh_token]**: Usado para atualizar um token de acesso expirado por um período estendido.

1. Na caixa **[!UICONTROL Redirect URI]**, especifique o [!DNL URI] desejado. Essa opção será ativada somente se você selecionar os tipos de concessão **[!UICONTROL Implicit]** e **[!UICONTROL Authorization_code]** . A caixa **[!UICONTROL Redirect URI]** permite especificar um valor separado por vírgulas com valores aceitáveis [!DNL URI]. Este é o [!DNL URI] para o qual um usuário de um cliente é redirecionado após aprovar o cliente para acesso [!DNL API].
1. Especifique o tempo de expiração desejado (em segundos) para acessar e atualizar a expiração do token.

   * **[!UICONTROL Access Token Expiration Time]**: O número de segundos que um token de acesso é válido após ser emitido. Pode ser nulo para usar o padrão da plataforma (12 horas). Também pode ser -1 para indicar que o token de acesso não expira.
   * **[!UICONTROL Refresh Token Expiration Time]**: O número de segundos que um token de atualização é válido após ser emitido. Pode ser nulo para usar o padrão da plataforma (30 dias).

1. Clique em **[!UICONTROL Save]**.

Para excluir um cliente [!UICONTROL OAuth2], clique em **[!UICONTROL OAuth2 Clients]** e em ![](assets/icon_delete.png) na coluna **[!UICONTROL Actions]** do cliente desejado.

>[!MORELIKETHIS]
>
>* [Requisitos da API e recomendações](../admin-oauth2/aam-admin-api-requirements.md)

