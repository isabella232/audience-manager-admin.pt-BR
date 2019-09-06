---
description: Use a página Usuários de integração para exibir uma lista de usuários na configuração do Audience Manager. É possível editar ou excluir usuários existentes ou criar novos usuários, desde que você tenha as funções apropriadas de usuário atribuídas.
seo-description: Use a página Usuários de integração para exibir uma lista de usuários na configuração do Audience Manager. É possível editar ou excluir usuários existentes ou criar novos usuários, desde que você tenha as funções apropriadas de usuário atribuídas.
seo-title: Usuários de integração
title: Usuários de integração
uuid: 13 dcb 3 fb -4561-409 c -84 da -943 d 0 d 390 cf 3
translation-type: tm+mt
source-git-commit: 10adb6b06160f5a5c4068483b407e5798fc10150

---


# Usuários de integração {#integration-users}

Use [!UICONTROL Integration Users] a página para exibir uma lista de usuários na configuração do Audience Manager. É possível editar ou excluir usuários existentes ou criar novos usuários, desde que você tenha as funções apropriadas de usuário atribuídas.

<!-- c_integration_users.xml -->

É possível classificar cada coluna em ordem crescente ou decrescente clicando no cabeçalho da coluna desejada.
Use [!UICONTROL Search] a caixa ou os controles de paginação na parte inferior da lista para encontrar o usuário desejado.

## Criar ou editar um usuário {#create-edit-user}

Use [!UICONTROL Integration Users] a página na ferramenta do Audience Manager [!UICONTROL Admin] para criar um novo usuário ou editar a conta de um usuário existente.

<!-- t_create_user.xml -->

>[!NOTE]
>
>Você deve ter [!UICONTROL CREATE_USER] a função para criar novos usuários. Você deve ter [!UICONTROL EDIT_USER] a função para editar os usuários existentes.

1. Para criar um novo usuário, clique **[!UICONTROL Integration Users]** em &gt; **[!UICONTROL Create a New User]**. Para editar um usuário existente, clique no usuário desejado na **[!UICONTROL Username]** coluna.
2. Preencha os campos:
   * **[!UICONTROL First Name]**: (Obrigatório) Especifique o primeiro nome do usuário.
   * **[!UICONTROL Last Name]**: (Obrigatório) Especifique o sobrenome do usuário.
   * **[!UICONTROL Username]**: (Obrigatório) Especifique o nome de usuário do usuário.
   * **[!UICONTROL Email Address]**: (Obrigatório) Especifique o endereço de email do usuário.
   * **[!UICONTROL Phone Number]**: Especifique o número de telefone do usuário.
   * **[!UICONTROL IMS ID]**: Especifique [!UICONTROL Internet Messaging Service ID]o usuário.
   * **[!UICONTROL User Roles]**: Selecione as funções do usuário desejadas:
      * **[!UICONTROL DEXADMIN]**: Fornece ao administrador acesso para executar tarefas na [!UICONTROL Admin] ferramenta do Audience Manager. Se você não selecionar essa opção, poderá escolher funções individuais. Essas funções permitem que os usuários executem tarefas usando [!DNL API] chamadas, mas não na ferramenta Administração.
      * **[!UICONTROL CREATE_USERS]**: Permite que os usuários criem novos usuários usando [!DNL API] uma chamada.
      * **[!UICONTROL DELETE_USERS]**: Permite que os usuários excluam usuários existentes usando [!DNL API] uma chamada.
      * **[!UICONTROL EDIT_USERS]**: Permite que os usuários editem usuários existentes usando [!DNL API] uma chamada.
      * **[!UICONTROL VIEW_USERS]**: Permite que os usuários visualizem outros usuários na configuração do Audience Manager usando [!DNL API] uma chamada.
      * **[!UICONTROL CREATE_PARTNERS]**: Permite que os usuários criem parceiros do Audience Manager usando [!DNL API] uma chamada.
      * **[!UICONTROL DELETE_PARTNERS]**: Permite que os usuários excluam os parceiros do Audience Manager usando [!DNL API] uma chamada.
      * **[!UICONTROL EDIT_PARTNERS]**: Permite que os usuários editem os parceiros do Audience Manager usando [!DNL API] uma chamada.
      * **[!UICONTROL VIEW_PARNTERS]**: Permite que os usuários visualizem os parceiros do Audience Manager usando [!DNL API] uma chamada.
   * **Status:** Selecione **[!UICONTROL Active]** para tornar esse usuário um usuário ativado do Audience Manager.
3. Clique em **[!UICONTROL Submit]**.

## Delete a User {#delete-user}

Use [!UICONTROL Integration Users] a página na ferramenta do Audience Manager [!UICONTROL Admin] para excluir um usuário existente.

<!-- t_delete_user.xml -->

>[!NOTE]
>
>Você deve ter **[!UICONTROL DELETE_USER]** a função para criar novos usuários.

1. Clique em **[!UICONTROL Integration Users]**.
2. Clique ![](assets/icon_delete.png) na **[!UICONTROL Actions]** coluna do usuário desejado.
3. Clique em **[!UICONTROL OK]para confirmar a exclusão.**