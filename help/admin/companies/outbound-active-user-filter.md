---
description: Siga estas instruções para gerar um arquivo de sincronização completo que inclua somente usuários ativos recentemente. Talvez você queira filtrar os usuários ativos para enviar dados relevantes para um sistema de direcionamento no site ou para limitar o tamanho dos arquivos enviados para um DSP. Não é possível usar esse filtro com sincronização incremental.
seo-description: Siga estas instruções para gerar um arquivo de sincronização completo que inclua somente usuários ativos recentemente. Talvez você queira filtrar os usuários ativos para enviar dados relevantes para um sistema de direcionamento no site ou para limitar o tamanho dos arquivos enviados para um DSP. Não é possível usar esse filtro com sincronização incremental.
seo-title: Filtrar dados de saída somente por usuários ativos
title: Filtrar dados de saída somente por usuários ativos
uuid: a2b4a385-eee3-458c-b978-09509cacb397
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# Filtrar dados de saída somente por usuários ativos {#filter-outbound-data-by-active-users-only}

Siga estas instruções para gerar um arquivo de sincronização completo que inclua somente usuários ativos recentemente. Talvez você queira filtrar os usuários ativos para enviar dados relevantes para um sistema de direcionamento no site ou para limitar o tamanho dos arquivos enviados para um DSP. Não é possível usar esse filtro com sincronização incremental.

>[!NOTE]
>
>Um visitante não precisa ser visto em um site de cliente selecionado ou em seu tráfego de anúncio para se qualificar como "ativo". Eles podem ser vistos por qualquer [!DNL Audience Manager] cliente ou parceiro para se qualificar como "ativo".

Para filtrar somente por usuários ativos:

1. Clique em **[!UICONTROL Companies]**.
1. Selecione a empresa com a qual deseja trabalhar e clique em **[!UICONTROL Destinations]**.
1. Na [!UICONTROL Batch Data] seção, defina as seguintes opções:

   * **[!UICONTROL Sync Type]**: Selecione **[!UICONTROL Customer]** ou **[!UICONTROL Platform]**.
   * **[!UICONTROL Sync Type Lookback Period]**: Esse intervalo de tempo define o intervalo do arquivo de dados. As opções incluem **[!UICONTROL 24 hours]**, **[!UICONTROL 7 days]**, **[!UICONTROL 30 days]**.
   * **[!UICONTROL Incremental Sync Scheduled Run]**: Selecione **[!UICONTROL Never]**. Lembre-se, este filtro se aplica somente aos arquivos de sincronização completa.
   * **[!UICONTROL Full Sync Scheduled Run]**: Isso determina a frequência com que você deseja receber esse arquivo. As opções incluem **[!UICONTROL 24 hours]**, **[!UICONTROL 7 days]**, **[!UICONTROL 30 days]** ou **[!UICONTROL Never]** (para desativar).

1. Clique em **[!UICONTROL Save]**.
