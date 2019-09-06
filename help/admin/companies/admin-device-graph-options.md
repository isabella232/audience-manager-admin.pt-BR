---
description: As Opções de gráfico de dispositivos estão disponíveis para empresas que participam do Device Co-op da Adobe Experience Cloud. Se um cliente também tiver uma relação contratual com um provedor de gráfico de dispositivo de terceiros integrado com o Audience Manager, esta seção mostrará opções para esse gráfico de dispositivos. Essas opções estão localizadas em Empresas > Nome da empresa > Perfil > Opções de gráfico de dispositivo.
seo-description: As Opções de gráfico de dispositivos estão disponíveis para empresas que participam do Device Co-op da Adobe Experience Cloud. Se um cliente também tiver uma relação contratual com um provedor de gráfico de dispositivo de terceiros integrado com o Audience Manager, esta seção mostrará opções para esse gráfico de dispositivos. Essas opções estão localizadas em Empresas > Nome da empresa > Perfil > Opções de gráfico de dispositivo.
seo-title: Opções de gráfico de dispositivo para empresas
title: Opções de gráfico de dispositivo para empresas
uuid: a 8 ced 3-710 c -4 a 8 f-a 0 d 7-ea 89 d 010 a 7 a 5
translation-type: tm+mt
source-git-commit: 10adb6b06160f5a5c4068483b407e5798fc10150

---


# Opções de gráfico de dispositivo para empresas {#device-graph-options-for-companies}

Estão [!UICONTROL Device Graph Options] disponíveis para empresas que participam [!DNL Adobe Experience Cloud Device Co-op]do. Se um cliente também tiver uma relação contratual com um provedor de gráfico de dispositivo de terceiros integrado com o Audience Manager, esta seção mostrará opções para esse gráfico de dispositivos. Essas opções estão localizadas [!UICONTROL Companies] em &gt; nome da empresa &gt; [!UICONTROL Profile] &gt; [!UICONTROL Device Graph Options].

![](assets/adminUIdataSource.png)

Essa ilustração usa nomes genéricos para as opções de gráfico de dispositivo de terceiros. Na produção, esses nomes vêm do provedor de gráfico de dispositivos e podem variar em relação ao que é mostrado aqui. Por exemplo, [!DNL LiveRamp] as opções normalmente (mas nem sempre):

* Comece com "[!DNL LiveRamp]"
* Contém um nome do meio que varia
* Terminar com "[!UICONTROL - Household]ou"[!UICONTROL -Person]

## Opções de gráfico de dispositivo definidas {#device-graph-options-defined}

As opções de gráfico de dispositivos selecionadas aqui expõem ou ocultam [!UICONTROL Device Options] as opções disponíveis para um [!DNL Audience Manager] cliente quando criam [!UICONTROL Profile Merge Rule]a.

### Gráfico de dispositivos de cooperação {#co-op-graph}

Os clientes que participam do [Device Co-op da Adobe Experience Cloud](https://marketing.adobe.com/resources/help/en_US/mcdc/) usam essas opções para criar um [!UICONTROL Profile Merge Rule] com [dados determinísticos e probabilísticos](https://marketing.adobe.com/resources/help/en_US/mcdc/mcdc-links.html). Os [!DNL Corporate Provisioning Team] ativa e desativa essa opção por uma [!DNL API] chamada back-end. Não é possível marcar nem limpar essas caixas no [!DNL Admin UI]. Além disso, as **[!UICONTROL Co-op Device Graph]** opções e as **[!UICONTROL Company Device Graph]** opções são mutuamente exclusivas. Os clientes podem nos solicitar ativar um ou o outro, mas não ambos. Quando marcado, isso expõe **[!UICONTROL Co-op Device Graph]** o controle nas [!UICONTROL Device Options] configurações para a [!UICONTROL Profile Merge Rule].

![](assets/adminUI1.png)

### Gráfico de dispositivo de empresa {#company-graph}

Essa opção é para [!DNL Analytics] clientes que usam [!UICONTROL People] a métrica em seu [!DNL Analytics] conjunto de relatórios. Os [!DNL Corporate Provisioning Team] ativa e desativa essa opção por uma [!DNL API] chamada back-end. Não é possível marcar nem limpar essas caixas no [!DNL Admin UI]. Além disso, as **[!UICONTROL Company Device Graph]** opções e as **[!UICONTROL Co-op Device Graph]** opções são mutuamente exclusivas. Os clientes podem nos solicitar ativar um ou o outro, mas não ambos. Quando marcado:

* Este gráfico de dispositivos usa dados determinísticos que pertencem à empresa que você está configurando (sem dados probabilísticos).
* [!DNL Audience Manager] cria automaticamente um [!UICONTROL Data Source] nome de `*`parceiro chamado`*-Company Device Graph-Person`. Na página [!UICONTROL Data Source] de detalhes, [!DNL Audience Manager] os clientes podem alterar o nome do parceiro, a descrição e aplicar [os Controles de exportação de dados](https://marketing.adobe.com/resources/help/en_US/aam/c_dec.html) a essa fonte de dados.
* [!DNL Audience Manager] clientes *não* veem uma nova configuração na [!UICONTROL Device Options] seção para [!UICONTROL Profile Merge Rule]a.

### Gráfico de dispositivo do liveramp (Person ou Doméstico) {#liveramp-device-graph}

Essas caixas de seleção são ativadas no [!DNL Admin UI] momento em que um parceiro cria um [!UICONTROL Data Source] e seleciona **[!UICONTROL Use as an Authenticated Profile]** e/ou **[!UICONTROL Use as a Device Graph]**. Os nomes dessas configurações são determinados pelo provedor de gráfico de dispositivo de terceiros (por exemplo [!DNL LiveRamp], [!DNL TapAd]etc.). Quando marcado, isso significa que a empresa que você está configurando irá usar os dados fornecidos pelos gráficos de dispositivos.

![](assets/adminUI2.png)

>[!MORE_ LIKE_ THIS]
>
>* [Opções de regra de mesclagem de perfil definidas](https://marketing.adobe.com/resources/help/en_US/aam/merge-rule-definitions.html)
>* [Configurações de fonte de dados e opções de menu](https://marketing.adobe.com/resources/help/en_US/aam/datasource-settings-definitions.html)

