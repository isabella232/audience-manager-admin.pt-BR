---
description: Use a página Empresas na ferramenta Admin do Audience Manager para criar uma nova empresa.
seo-description: Use a página Empresas na ferramenta Admin do Audience Manager para criar uma nova empresa.
seo-title: Criar um perfil de empresa
title: Criar um perfil de empresa
uuid: 55de18f8-883d-43fe-b37f-e8805bb92f7a
translation-type: tm+mt
source-git-commit: 71bf4cec222428686c1eab0998f66887db06da68

---


# Criar um perfil de empresa {#create-a-company-profile}

Use a [!UICONTROL Companies] página na ferramenta de administração do Audience Manager para criar uma nova empresa.

<!-- t_create_company.xml -->

>[!NOTE]
>
>Você deve ter o **[!UICONTROL DEXADMIN]** papel para criar novas empresas.

1. Click **[!UICONTROL Companies]** &gt; **[!UICONTROL Add Company]**.
1. Preencha os campos:

   * **[!UICONTROL Name]**: (Obrigatório) Especifique o nome da empresa.
   * **[!UICONTROL Description]**: (Obrigatório) Forneça informações descritivas sobre a empresa, como a indústria ou seu nome completo.
   * **[!UICONTROL Subdomain]**: (Obrigatório) Especifique o subdomínio da empresa. O texto inserido é o que aparece como subdomínio da chamada de evento. Isso não pode ser mudado. Deve ser uma string de caracteres [!DNL URL]válidos.

      Por exemplo, se sua empresa tivesse o nome [!DNL AcmeCorp], o subdomínio seria [!DNL acmecorp].

      O Audience Manager usa o subdomínio para o [!UICONTROL Data Collection Server]([!UICONTROL DCS]). No exemplo anterior, se sua empresa estiver cheia [!DNL URL] em [!UICONTROL DCS] estará [!DNL acmecorp.demdex.net].

   * **[!UICONTROL Lifecyle]**: Especifique o estágio desejado para a empresa:
      * **[!UICONTROL Active]**: Especifique se a empresa será um cliente do Audience Manager ativo. Uma [!UICONTROL Active] conta significa um cliente pagador, não apenas para consultoria, mas para o SKU do Audience Manager.
      * **[!UICONTROL Demo]**: Especifique que a empresa será apenas para fins de demonstração. Os dados de relatório serão automaticamente falsificados.
      * **[!UICONTROL Prospect]**: Especifique se a empresa é um cliente potencial do Audience Manager, como uma empresa que recebe uma configuração gratuita [!DNL POC] ou de conta para uma demonstração de vendas.
      * **[!UICONTROL Test]**: Especifique que a empresa será apenas para fins de teste interno.
   * **[!UICONTROL Account Types]**: Especifique o conjunto completo de tipos de conta para esta empresa. Nenhum tipo de conta é mutuamente exclusivo com qualquer outro tipo.
      * **[!UICONTROL Full AAM]**: Especifique se a empresa terá uma conta completa do Adobe Audience Manager e os usuários terão acesso ao logon.
      * **[!UICONTROL MMP]**: Especifique se a empresa foi habilitada a usar os [!UICONTROL Master Marketing Profile] ([!UICONTROL MMP]) recursos. O [!UICONTROL MMP] permite que os públicos-alvo sejam compartilhados na Experience Cloud usando um [!UICONTROL Experience Cloud ID] ([!DNL MCID]) que é atribuído a cada visitante e usado pelo Audience Manager. Se você selecionar esse tipo de conta, a conta também [!UICONTROL Experience Cloud ID Service] será selecionada automaticamente.

         Para obter mais informações, consulte [Serviços de público-alvo - Perfil](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html)principal de marketing.
   * **[!UICONTROL Data Source]**: Especifique se a empresa é um provedor de dados de terceiros no Audience Manager.
   * **[!UICONTROL Targeting Partner]**: Especifique se a empresa atua como uma plataforma de direcionamento para clientes do Audience Manager.
   * **[!UICONTROL Visitor ID Service]**: Especifique se a empresa foi habilitada a usar o [!UICONTROL Experience Cloud Visitor ID Service].

      O [!UICONTROL Experience Cloud Visitor ID Service] fornece uma ID de visitante universal nas soluções da Experience Cloud. For more information, see the [Experience Cloud Visitor ID Service user guide](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-overview.html).

   * **[!UICONTROL Agency]**: Especifique que a empresa terá uma [!UICONTROL Agency] conta.



1. Clique em **[!UICONTROL Create]**. Continue com as instruções em [Editar um perfil](../companies/admin-manage-company-profiles.md#edit-company-profile)de empresa.

   ![Resultado da etapa](assets/add_company.png)

## Editar um perfil de empresa {#edit-company-profile}

Edite o perfil de uma empresa, incluindo seu nome, descrição, subdomínio, ciclo de vida e muito mais.

<!-- t_edit_company_profile.xml -->

1. Clique em **[!UICONTROL Companies]**, localize e clique na empresa desejada para exibir sua [!UICONTROL Profile] página.

   Use a [!UICONTROL Search] caixa ou os controles de paginação na parte inferior da lista para localizar a empresa desejada. É possível classificar cada coluna em ordem crescente ou decrescente clicando no cabeçalho da coluna desejada.

   ![Resultado da etapa](assets/profile_company.png)

1. Edite os campos conforme necessário:

   * **[!UICONTROL Name]**: Edite o nome da empresa. Este campo é obrigatório.
   * **[!UICONTROL Description]**: Edite a descrição da empresa. Este campo é obrigatório.
   * **[!UICONTROL Subdomain]**: (Obrigatório) Especifique o subdomínio da empresa. O texto inserido é o que aparece como subdomínio da chamada de evento. Isso não pode ser mudado. Deve ser uma string de caracteres [!DNL URL]válidos.

      Por exemplo, se sua empresa tivesse o nome [!DNL AcmeCorp], o subdomínio seria [!DNL acmecorp].

      O Audience Manager usa o subdomínio para o [!UICONTROL Data Collection Server] ([!UICONTROL DCS]). No exemplo anterior, se sua empresa estiver cheia [!DNL URL] em [!UICONTROL DCS] estará [!DNL acmecorp.demdex.net].

   * **[!UICONTROL imsOrgld]**: ([!UICONTROL Identity Management System Organization ID]) Essa ID permite que você conecte sua empresa à Adobe Experience Cloud.
   * **[!UICONTROL Lifecyle]**: Especifique o estágio desejado para a empresa:
      * **[!UICONTROL Active]**: Especifique se a empresa será um cliente do Audience Manager ativo. Uma conta ativa significa um cliente que paga, não apenas para consultoria, mas para o SKU do Audience Manager.
      * **[!UICONTROL Demo]**: Especifique que a empresa será apenas para fins de demonstração. Os dados de relatório serão automaticamente falsificados.
      * **[!UICONTROL Prospect]**: Especifique se a empresa é um cliente potencial do Audience Manager, como uma empresa que recebe uma configuração gratuita [!DNL POC] ou de conta para uma demonstração de vendas.
      * **[!UICONTROL Test]**: Especifique que a empresa será apenas para fins de teste interno.
   * **[!UICONTROL Account Types]**: Especifique o conjunto completo de tipos de conta para esta empresa. Nenhum tipo de conta é mutuamente exclusivo com qualquer outro tipo.
      * **[!UICONTROL Full AAM]**: Especifique se a empresa terá uma conta completa do Adobe Audience Manager e os usuários terão acesso ao logon.
      * **[!UICONTROL MMP]**: Especifique se a empresa foi habilitada a usar os recursos do Perfil principal de marketing ([!UICONTROL MMP]).

         Se você selecionar esse tipo de conta, também **[!UICONTROL Visitor ID Service]** será selecionado automaticamente.
Para obter mais informações, consulte [Serviços de público-alvo - Perfil](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html)principal de marketing.
   * **[!UICONTROL Data Source]**: Especifique se a empresa é um provedor de dados de terceiros no Audience Manager.
   * **[!UICONTROL Targeting Partner]**: Especifique se a empresa atua como uma plataforma de direcionamento para clientes do Audience Manager.
   * **[!UICONTROL Visitor ID Service]**: Especifique se a empresa foi habilitada a usar o Serviço de ID de visitante da Experience Cloud.

      O serviço de ID de visitante da Experience Cloud fornece uma ID de visitante universal em todas as soluções da Experience Cloud. For more information, see the [Experience Cloud Visitor ID Service user guide](https://microsite.omniture.com/t2/help/en_US/mcvid/mcvid_service.html).

   * **[!UICONTROL Agency]**: Especifique que a empresa terá uma conta da Agência.
   * **[!UICONTROL Features]**: Selecione as opções desejadas:
      * **[!UICONTROL Password Expiration]**: Define todas as senhas de usuário nesta empresa para expirar após 90 dias para aumentar a segurança do Audience Manager.
      * **[!UICONTROL Reporting]**: Habilita o relatório do Audience Manager para esta empresa.
      * **[!UICONTROL Role Based Access Controls]**: Ative os controles de acesso baseados em funções para esta empresa. Os controles de acesso baseados em funções permitem que você crie grupos de usuários com permissões de acesso diferentes. Os usuários individuais nesses grupos podem acessar somente recursos específicos no Audience Manager.


1. Clique em **[!UICONTROL Submit Updates]**.

## Excluir um perfil de empresa {#delete-company-profile}

Use a [!UICONTROL Companies] página na ferramenta Audience Manager [!UICONTROL Admin] para excluir uma empresa existente.

<!-- t_delete_company.xml -->

>[!NOTE]
>
>Você deve ter a [!UICONTROL DEXADMIN] função para excluir empresas existentes.

1. Para excluir uma empresa existente, clique em **[!UICONTROL Companies]**.

   ![Resultado da etapa](assets/companies.png)

1. Clique ![](assets/icon_delete.png) na **[!UICONTROL Actions]** coluna da empresa desejada.
1. Clique em **[!UICONTROL OK]para confirmar a exclusão.**
