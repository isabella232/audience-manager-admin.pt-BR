---
description: Crie, edite e exclua destinos de Audience Manager.
seo-description: Crie, edite e exclua destinos de Audience Manager.
seo-title: Gerenciar destinos da empresa
title: Gerenciar destinos da empresa
uuid: d9a6bfb1-7629-44e0-b7d7-ece44f65ea2b
translation-type: tm+mt
source-git-commit: f247457004a624297ddc8847dd256dbb7d8da418
workflow-type: tm+mt
source-wordcount: '1082'
ht-degree: 1%

---


# Gerenciar destinos da empresa {#manage-company-destinations}

Crie, edite e exclua destinos de Audience Manager.

<!-- t_company_destinations.xml -->

Para obter informações detalhadas, consulte [Destinos](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/destinations/destinations.html) no *Guia do Usuário do Audience Manager*.

## Criar ou editar destinos da empresa {#create-edit-company-destinations}

Percorra as seções para obter instruções passo a passo sobre como criar novos destinos [!DNL Audience Manager] ou editar destinos existentes.

<!-- create-edit-company-destinations.xml -->

Visite a [página de integração de parceiro de Experience Cloud](https://wiki.corp.adobe.com/x/mPIMPw) antes de configurar os destinos. A página contém as informações específicas que você precisa preencher para cada [!DNL Audience Manager] integração de parceiro.

Se seu cliente quiser usar [!DNL Adobe Media Optimizer] como um destino em [!DNL Audience Manager], você precisa configurar isso em [!DNL Adobe Media Optimizer].

## Navegue até a guia Destinos {#navigate-destinations}

1. Clique em **[!UICONTROL Companies]** e localize e clique na empresa desejada para exibir sua página [!UICONTROL Profile]. Você pode usar a caixa [!UICONTROL Search] ou os controles de paginação na parte inferior da lista para localizar a empresa desejada. É possível classificar cada coluna em ordem crescente ou decrescente clicando no cabeçalho da coluna desejada.
1. Clique na guia **[!UICONTROL Destinations]**.
1. Para criar um novo destino, clique em **[!UICONTROL Add Destination]**. Para editar um destino existente, clique no nome do destino na coluna **[!UICONTROL Name]**.

## Configurações básicas {#basic-settings}

Preencha os campos na janela **[!UICONTROL Basic Settings]**.

* **[!UICONTROL Name]:** (Obrigatório) Especifique o nome desse destino.
* **[!UICONTROL Description]:** Especifique informações descritivas sobre este destino.
* **[!UICONTROL Type]:** (Obrigatório) Selecione o tipo de destino desejado:
   * **[!UICONTROL Bulk ID]**: Sincronizar IDs entre plataformas diferentes.
   * **[!UICONTROL Bulk Trait]**: Envie informações características em massa para diferentes plataformas.
   * **[!UICONTROL Bulk Segment]**: Envie informações do segmento em massa para plataformas diferentes.
   * **[!UICONTROL S2S]**: Use destinos de servidor para servidor para enviar dados em tempo real e em lote para diferentes plataformas.
* **[!UICONTROL Auto-Fill Destination Mapping]:** ( [!UICONTROL S2S] somente) Selecione uma opção:
   * **[!UICONTROL Segment ID]:** Se você selecionar essa configuração, o mapeamento do valor de destino será preenchido com a ID do  [!DNL Audience Manager] segmento.
   * **[!UICONTROL Integration Code Value]:** Se você selecionar essa configuração, o mapeamento do valor de destino será preenchido com o código de integração do  [!DNL Audience Manager] segmento.
* **[!UICONTROL User ID Key]:** (Obrigatório) Selecione a chave de ID de usuário desejada para esse destino na lista suspensa.

Essa ID é usada como a ID da fonte de dados principal. Isso determina as IDs de usuário a serem exageradas no arquivo.

>[!NOTE]
>
>Para o tipo de destino [!UICONTROL Bulk ID], não é possível usar a ID [!DNL Audience Manager] [!UICONTROL User ID] ou [!DNL Adobe Experience Cloud].

Se a ID da fonte de dados ( [!UICONTROL DPID]) não for exibida na lista suspensa, você deverá marcar a caixa de seleção **[!UICONTROL Outbound]** no nível da fonte de dados na página [Configurações da fonte de dados](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/data-sources/manage-datasources.html).

* **[!UICONTROL Target Data Source]:** (Obrigatório) Selecione a fonte de dados desejada para esse destino na lista suspensa. Essa configuração permite a rotulação de dados externos, o que permite a ingestão em sistemas separados do lado do cliente.
* **[!UICONTROL Foreign Account ID]:** Especifique a ID da conta estrangeira para este destino. Esse é o valor de identificação no sistema do recipient para esses dados expirados.
* **[!UICONTROL Outbound Sample Rate Denominator]:** Quando a quantidade total de dados retornados for desconhecida, use essa configuração para retornar somente uma quantidade de dados de amostra, em vez da quantidade total. Ajuste o número aqui para representar uma fração dos dados (por exemplo, um valor de &#39;100&#39; retorna 1/100º a quantidade regular de dados, um valor de &#39;10&#39; retorna 1/10º a quantidade regular de dados). O padrão é &quot;1&quot;, que retorna todos os dados.

## Dados em tempo real (para destinos S2S) {#realtime-s2s}

Se você estiver criando um destino [!UICONTROL S2S], preencha os campos abaixo:

**[!UICONTROL Servers]**: Selecione o  `HTTP` servidor desejado para este destino.
**[!UICONTROL Format]**: Selecione o formato desejado para este destino na lista suspensa:  [!UICONTROL HTTP only].

>[!NOTE]
>
>Somente para [!DNL S2S], você pode ativar ou desativar os destinos [!UICONTROL Realtime] ou [!UICONTROL Batch] usando os controles deslizantes Off/On na tela. Não é possível desativar ambas as opções.

## Dados em lote {#batch-data}

Para destinos [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] ou [!UICONTROL Bulk Segment], preencha os campos abaixo:

* **[!UICONTROL Protocol]**: (Obrigatório) Selecione o protocolo desejado para este destino na lista suspensa:
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**: (Obrigatório) Selecione o servidor desejado para esse destino na lista suspensa.
* **[!UICONTROL Format]**: (Obrigatório) Selecione o formato desejado para este destino na lista suspensa:  [!DNL HTTP] ou tipo de arquivo, dependendo do protocolo escolhido acima.
* **[!UICONTROL Sync Type]**: (Obrigatório) Selecione o tipo de sincronização desejado para este destino. Isso indica o nível de atividades do usuário que os clientes desejam incluir nas ordens de saída. Selecione **[!UICONTROL Customer]** se os clientes só estiverem interessados em analisar as qualificações de segmento de suas propriedades. Selecione **[!UICONTROL Platform]** se quiser incluir qualificações de segmento de atividades fora do site em todos os [!DNL Audience Manager] clientes.
* **[!UICONTROL Customer]**: O arquivo contém usuários ativos que têm pelo menos 1 característica de realização somente nas propriedades do cliente (associadas às do cliente  [!UICONTROL PID]) para o período selecionado. Seus clientes devem usar essa opção para enviar suas qualificações de segmento *em tempo real* para destinos.
* **[!UICONTROL Platform]**: O arquivo contém usuários ativos que têm pelo menos 1 interação em tempo real, seja sincronização de ID ou realização de característica, em qualquer lugar nas propriedades de todos os  [!DNL Audience Manager] clientes (associadas a todos os PIDs do cliente) durante o período selecionado. Seus clientes devem usar essa opção para enviar suas qualificações de segmento *total* para destinos.
* **[!UICONTROL Lifetime]**: O arquivo contém usuários ativos vistos em qualquer lugar nas propriedades de todos os  [!DNL Audience Manager] clientes desde a criação do destino.
* **[!UICONTROL Sync Type Lookback Period]**: Se você selecionar  [!UICONTROL Customer] ou  [!UICONTROL Platform], selecione um período de tempo. Os arquivos contêm usuários ativos para o período selecionado.
Em seguida, selecione o tipo de pedido. Isso indica a frequência e o escopo de cada integração externa com parceiros. Selecione entre ordens incrementais e completas.
* **[!UICONTROL Incremental Scheduled Run]**: Com cada execução, somente  [!DNL Audience Manager] expulsarão os novos usuários líquidos qualificados desde a ordem de saída anterior. Selecione o período de tempo desejado para que [!DNL Audience Manager] execute processos de sincronização incrementais. Por exemplo, você pode selecionar a cada 24 horas, a cada sete dias, a cada 30 dias, ou nunca.

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>A primeira ordem incremental é equivalente a um pedido completo, pois nenhum usuário anterior foi enviado para o destino.

* **[!UICONTROL Full Sync Scheduled Run]**: Com cada execução, todos os usuários ativos  [!DNL Audience Manager] serão enviados desde que o destino foi configurado pela primeira vez. Selecione o agendamento desejado que você deseja que [!DNL Audience Manager] use para executar processos de sincronização completos. Por exemplo, você pode selecionar a cada 24 horas, a cada sete dias, a cada 30 dias, ou nunca.

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>Recomendamos usar sincronizações incrementais com mais frequência do que sincronizações completas. As sincronizações incrementais só enviam arquivos que contêm novas realizações de características ou sincronizações de ID. As sincronizações completas enviam todos os arquivos, independentemente de incluírem ou não novas realizações ou sincronizações de ID. Use a configuração [!UICONTROL Full Sync Scheduled Run] somente quando os clientes precisarem de uma cópia completa de todos os usuários, para reduzir o volume de dados de saída.

## Configurar fontes de dados {#configure-data-sources}

Para destinos [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] ou [!UICONTROL Bulk Segment], preencha os campos abaixo. Essas configurações permitem que você envie todos os dados (características, segmentos ou IDs, com base no tipo selecionado) associados às fontes de dados.

* **[!UICONTROL All Unrestricted First Party Data]**: Selecione para usar todas as fontes de dados originais. Se você selecionar essa opção, as opções [!UICONTROL Available Data Sources] serão desativadas.
* **[!UICONTROL Available Data Sources]**: Use as setas para mover fontes de dados entre as  **[!UICONTROL Available Data Sources]** caixas  **[!UICONTROL In File Data Sources]** e.

## Salvar e finalizar {#save-and-finalize}

O botão **[!UICONTROL Save]** é ativado depois de preencher todos os campos obrigatórios. Clique em **[!UICONTROL Save]** para finalizar o processo de criação de destino.

## Excluir destinos de Empresa {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

Para excluir um destino:

1. Clique em **[!UICONTROL Companies]**, localize e clique na empresa desejada e clique na guia **[!UICONTROL Destinations]**.
1. Clique em ![](assets/icon_delete.png) na coluna **[!UICONTROL Actions]** do destino desejado.
1. Clique em **[!UICONTROL OK]** para confirmar a exclusão.

>[!NOTE]
>
>Não é possível excluir um destino se ele tiver segmentos mapeados para ele.