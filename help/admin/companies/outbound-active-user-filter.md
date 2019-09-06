---
description: Siga estas instruções para gerar um arquivo completo de sincronização que inclua apenas usuários ativos recentemente. Você pode desejar filtrar por usuários ativos para enviar dados relevantes para um sistema de direcionamento no site ou limitar o tamanho dos arquivos enviados para um DSP. Não é possível usar esse filtro com a sincronização incremental.
seo-description: Siga estas instruções para gerar um arquivo completo de sincronização que inclua apenas usuários ativos recentemente. Você pode desejar filtrar por usuários ativos para enviar dados relevantes para um sistema de direcionamento no site ou limitar o tamanho dos arquivos enviados para um DSP. Não é possível usar esse filtro com a sincronização incremental.
seo-title: Filtrar dados de saída somente por usuários ativos
title: Filtrar dados de saída somente por usuários ativos
uuid: a 2 b 4 a 385-eee 3-458 c-b 978-09509 cacb 397
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# Filtrar dados de saída somente por usuários ativos {#filter-outbound-data-by-active-users-only}

Siga estas instruções para gerar um arquivo completo de sincronização que inclua apenas usuários ativos recentemente. Você pode desejar filtrar por usuários ativos para enviar dados relevantes para um sistema de direcionamento no site ou limitar o tamanho dos arquivos enviados para um DSP. Não é possível usar esse filtro com a sincronização incremental.

>[!NOTE]
>
>Um visitante não precisa ser visto em um site do cliente selecionado ou em seu tráfego de anúncios para se qualificar como "ativo". Eles podem ser vistos por qualquer [!DNL Audience Manager] cliente ou parceiro para se qualificar como "ativo".

Para filtrar apenas por usuários ativos:

1. Clique em **[!UICONTROL Companies]**.
1. Selecione a empresa com a qual deseja trabalhar e clique **[!UICONTROL Destinations]**.
1. Na [!UICONTROL Batch Data] seção, defina as seguintes opções:

   * **[!UICONTROL Sync Type]**: Selecione **[!UICONTROL Customer]** ou **[!UICONTROL Platform]**.
   * **[!UICONTROL Sync Type Lookback Period]**: Esse intervalo de tempo define o intervalo de seu arquivo de dados. As escolhas incluem **[!UICONTROL 24 hours]****[!UICONTROL 7 days]**.**[!UICONTROL 30 days]**
   * **[!UICONTROL Incremental Sync Scheduled Run]**: Selecione **[!UICONTROL Never]**. Lembre-se, este filtro se aplica somente aos arquivos completos de sincronização.
   * **[!UICONTROL Full Sync Scheduled Run]**: Isso determina com que frequência você deseja receber esse arquivo. As escolhas incluem **[!UICONTROL 24 hours]****[!UICONTROL 7 days]**, **[!UICONTROL 30 days]** ou **[!UICONTROL Never]** (para desativar).

1. Clique em **[!UICONTROL Save]**.
