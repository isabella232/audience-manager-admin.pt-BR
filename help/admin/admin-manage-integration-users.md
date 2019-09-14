---
description: Use a página Usuários da integração para exibir uma lista de usuários na configuração do Audience Manager. É possível editar ou excluir usuários existentes ou criar novos usuários, desde que você tenha as funções de usuário apropriadas atribuídas.
seo-description: Use a página Usuários da integração para exibir uma lista de usuários na configuração do Audience Manager. É possível editar ou excluir usuários existentes ou criar novos usuários, desde que você tenha as funções de usuário apropriadas atribuídas.
seo-title: Usuários de integração
title: Usuários de integração
uuid: 13dcb3fb-4561-409c-84da-943d0d390cf3
translation-type: tm+mt
source-git-commit: 10adb6b06160f5a5c4068483b407e5798fc10150

---


# Usuários de integração {#integration-users}

Use a [!UICONTROL Integration Users] página para exibir uma lista de usuários na configuração do Audience Manager. É possível editar ou excluir usuários existentes ou criar novos usuários, desde que você tenha as funções de usuário apropriadas atribuídas.

<!-- c_integration_users.xml -->

É possível classificar cada coluna em ordem crescente ou decrescente clicando no cabeçalho da coluna desejada.
Use a [!UICONTROL Search] caixa ou os controles de paginação na parte inferior da lista para localizar o usuário desejado.

## Criar ou editar um usuário {#create-edit-user}

Use a [!UICONTROL Integration Users] página na ferramenta Audience Manager [!UICONTROL Admin] para criar um novo usuário ou editar uma conta de usuário existente.

<!-- t_create_user.xml -->

>[!NOTE]
>
>Você deve ter a [!UICONTROL CREATE_USER] função para criar novos usuários. É necessário ter a [!UICONTROL EDIT_USER] função para editar usuários existentes.

1. Para criar um novo usuário, clique em **[!UICONTROL Integration Users]** &gt; **[!UICONTROL Create a New User]**. Para editar um usuário existente, clique no usuário desejado na **[!UICONTROL Username]** coluna.
2. Preencha os campos:
   * **[!UICONTROL First Name]**: (Obrigatório) Especifique o nome do usuário.
   * **[!UICONTROL Last Name]**: (Obrigatório) Especifique o sobrenome do usuário.
   * **[!UICONTROL Username]**: (Obrigatório) Especifique o nome de usuário do usuário.
   * **[!UICONTROL Email Address]**: (Obrigatório) Especifique o endereço de email do usuário.
   * **[!UICONTROL Phone Number]**: Especifique o número de telefone do usuário.
   * **[!UICONTROL IMS ID]**: Especifique o do usuário [!UICONTROL Internet Messaging Service ID].
   * **[!UICONTROL User Roles]**: Selecione as funções de usuário desejadas:
      * **[!UICONTROL DEXADMIN]**: Fornece acesso de administrador para executar tarefas na [!UICONTROL Admin] ferramenta Audience Manager. Se você não selecionar essa opção, poderá escolher funções individuais. Essas funções permitem que os usuários executem tarefas usando [!DNL API] chamadas, mas não na ferramenta Admin.
      * **[!UICONTROL CREATE_USERS]**: Permite que os usuários criem novos usuários usando uma [!DNL API] chamada.
      * **[!UICONTROL DELETE_USERS]**: Permite que os usuários excluam usuários existentes usando uma [!DNL API] chamada.
      * **[!UICONTROL EDIT_USERS]**: Permite que os usuários editem usuários existentes usando uma [!DNL API] chamada.
      * **[!UICONTROL VIEW_USERS]**: Permite que os usuários vejam outros usuários na configuração do Audience Manager usando uma [!DNL API] chamada.
      * **[!UICONTROL CREATE_PARTNERS]**: Permite que os usuários criem parceiros do Audience Manager usando uma [!DNL API] chamada.
      * **[!UICONTROL DELETE_PARTNERS]**: Permite que os usuários excluam parceiros do Audience Manager usando uma [!DNL API] chamada.
      * **[!UICONTROL EDIT_PARTNERS]**: Permite que os usuários editem parceiros do Audience Manager usando uma [!DNL API] chamada.
      * **[!UICONTROL VIEW_PARNTERS]**: Permite que os usuários vejam os parceiros do Audience Manager usando uma [!DNL API] chamada.
   * **** Status: Selecione **[!UICONTROL Active]** para tornar esse usuário um usuário do Audience Manager ativado.
3. Clique em **[!UICONTROL Submit]**.

## Delete a User {#delete-user}

Use a [!UICONTROL Integration Users] página na ferramenta Audience Manager [!UICONTROL Admin] para excluir um usuário existente.

<!-- t_delete_user.xml -->

>[!NOTE]
>
>Você deve ter a **[!UICONTROL DELETE_USER]** função para criar novos usuários.

1. Clique em **[!UICONTROL Integration Users]**.
2. Clique ![](assets/icon_delete.png) na **[!UICONTROL Actions]** coluna do usuário desejado.
3. Clique em **[!UICONTROL OK]para confirmar a exclusão.**