---
description: As Opções de gráfico de dispositivo estão disponíveis para empresas que participam do Adobe Experience Cloud Device Co-op. Se um cliente também tiver uma relação contratual com um provedor de gráficos de dispositivos de terceiros que esteja integrado ao Audience Manager, esta seção mostrará opções para esse gráfico de dispositivos. Essas opções estão localizadas em Empresa > Nome da empresa > Perfil > Opções do Gráfico de dispositivos.
seo-description: As Opções de gráfico de dispositivo estão disponíveis para empresas que participam do Adobe Experience Cloud Device Co-op. Se um cliente também tiver uma relação contratual com um provedor de gráficos de dispositivos de terceiros que esteja integrado ao Audience Manager, esta seção mostrará opções para esse gráfico de dispositivos. Essas opções estão localizadas em Empresa > Nome da empresa > Perfil > Opções do Gráfico de dispositivos.
seo-title: Opções de gráfico de dispositivo para empresas
title: Opções de gráfico de dispositivo para empresas
uuid: a8ced843-710c-4a8f-a0d7-ea89d010a7a5
translation-type: tm+mt
source-git-commit: 2998dc049971b2fac8c45ca6e3118ea607ae3f92
workflow-type: tm+mt
source-wordcount: '538'
ht-degree: 4%

---


# Opções de gráfico de dispositivo para empresas {#device-graph-options-for-companies}

Os [!UICONTROL Device Graph Options] estão disponíveis para empresas que participam no [!DNL Adobe Experience Cloud Device Co-op]. Se um cliente também tiver uma relação contratual com um provedor de gráficos de dispositivos de terceiros que esteja integrado ao Audience Manager, esta seção mostrará opções para esse gráfico de dispositivos. Essas opções estão localizadas em [!UICONTROL Companies] > nome da empresa > [!UICONTROL Profile] > [!UICONTROL Device Graph Options].

![](assets/adminUIdataSource.png)

Esta ilustração usa nomes genéricos para as opções de gráficos de dispositivos de terceiros. Na produção, esses nomes vêm do provedor de gráficos de dispositivos e podem variar do que é mostrado aqui. Por exemplo, as opções [!DNL LiveRamp] normalmente (mas nem sempre):

* Comece com &quot;[!DNL LiveRamp]&quot;
* Contém um nome do meio que varia
* Terminar com &quot;[!UICONTROL - Household]&quot; ou &quot;[!UICONTROL -Person]&quot;

## Definição das opções do gráfico de dispositivos {#device-graph-options-defined}

As opções de gráfico de dispositivo que você seleciona aqui expõem ou ocultam as [!UICONTROL Device Options] opções disponíveis para um cliente [!DNL Audience Manager] ao criar um [!UICONTROL Profile Merge Rule].

### Gráfico de dispositivos cooperativos {#co-op-graph}

Os clientes que participam do [Adobe Experience Cloud Device Co-op](https://marketing.adobe.com/resources/help/en_US/mcdc/) usam essas opções para criar um [!UICONTROL Profile Merge Rule] com [dados determinísticos e probabilísticos](https://marketing.adobe.com/resources/help/en_US/mcdc/mcdc-links.html). O [!DNL Corporate Provisioning Team] ativa e desativa essa opção por meio de uma chamada back-end [!DNL API]. Não é possível marcar nem desmarcar essas caixas em [!DNL Admin UI]. Além disso, as opções **[!UICONTROL Co-op Device Graph]** e **[!UICONTROL Company Device Graph]** são mutuamente exclusivas. Os clientes podem nos pedir para ativar um ou o outro, mas não ambos. Quando marcado, isso expõe o controle **[!UICONTROL Co-op Device Graph]** nas configurações [!UICONTROL Device Options] de um [!UICONTROL Profile Merge Rule].

![](assets/adminUI1.png)

### Gráfico de dispositivos de empresa {#company-graph}

Esta opção é para clientes [!DNL Analytics] que usam a métrica [!UICONTROL People] em seu conjunto de relatórios [!DNL Analytics]. O [!DNL Corporate Provisioning Team] ativa e desativa essa opção por meio de uma chamada back-end [!DNL API]. Não é possível marcar nem desmarcar essas caixas em [!DNL Admin UI]. Além disso, as opções **[!UICONTROL Company Device Graph]** e **[!UICONTROL Co-op Device Graph]** são mutuamente exclusivas. Os clientes podem nos pedir para ativar um ou o outro, mas não ambos. Quando marcado:

* Este gráfico de dispositivos usa dados determinísticos que pertencem à empresa que você está configurando (sem dados probabilísticos).
* [!DNL Audience Manager] cria automaticamente um nome  [!UICONTROL Data Source] chamado de  `*`parceiro`*-Company Device Graph-Person`. Na página de detalhes [!UICONTROL Data Source], [!DNL Audience Manager] os clientes podem alterar o nome do parceiro, a descrição e aplicar [Controles de Exportação de Dados](https://marketing.adobe.com/resources/help/en_US/aam/c_dec.html) a esta fonte de dados.
* [!DNL Audience Manager] os clientes  *não* veem uma nova configuração na  [!UICONTROL Device Options] seção para uma  [!UICONTROL Profile Merge Rule].

### LiveRamp Device Graph (Pessoa ou Família) {#liveramp-device-graph}

Essas caixas de seleção são ativadas em [!DNL Admin UI] quando um parceiro cria um [!UICONTROL Data Source] e seleciona **[!UICONTROL Use as an Authenticated Profile]** e/ou **[!UICONTROL Use as a Device Graph]**. Os nomes dessas configurações são determinados pelo provedor de gráficos de dispositivo de terceiros (por exemplo, [!DNL LiveRamp], [!DNL TapAd] etc.). Quando marcada, isso significa que a empresa que você está configurando usará os dados fornecidos por esses gráficos de dispositivo.

![](assets/adminUI2.png)

>[!MORELIKETHIS]
>
>* [Definição das opções da regra de mesclagem de perfis](https://marketing.adobe.com/resources/help/en_US/aam/merge-rule-definitions.html)
>* [Configurações da fonte de dados e opções de menu](https://marketing.adobe.com/resources/help/en_US/aam/datasource-settings-definitions.html)

