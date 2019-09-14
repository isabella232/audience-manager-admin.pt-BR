---
description: Crie, edite e exclua destinos do Audience Manager.
seo-description: Crie, edite e exclua destinos do Audience Manager.
seo-title: Gerenciar destinos da empresa
title: Gerenciar destinos da empresa
uuid: d9a6bfb1-7629-44e0-b7d7-ece44f65ea2b
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# Gerenciar destinos da empresa {#manage-company-destinations}

Crie, edite e exclua destinos do Audience Manager.

<!-- t_company_destinations.xml -->

Para obter informações detalhadas, consulte [Destinos](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/destinations/destinations.html) no Guia *do usuário do* Audience Manager.

## Criar ou editar destinos da empresa {#create-edit-company-destinations}

Percorra as seções para obter instruções passo a passo sobre como criar novos [!DNL Audience Manager] destinos ou editar destinos existentes.

<!-- create-edit-company-destinations.xml -->

Visite a página [de integração de parceiros da](https://wiki.corp.adobe.com/x/mPIMPw) Experience Cloud antes de configurar os destinos. A página contém as informações específicas que você precisa preencher para cada integração de [!DNL Audience Manager] parceiro.

Se o cliente quiser usar [!DNL Adobe Media Optimizer] como destino no [!DNL Audience Manager] , é necessário configurá-lo no [!DNL Adobe Media Optimizer].

## Navigate to the Destinations Tab {#navigate-destinations}

1. Clique em **[!UICONTROL Companies]**, localize e clique na empresa desejada para exibir sua [!UICONTROL Profile] página. Você pode usar a [!UICONTROL Search] caixa ou os controles de paginação na parte inferior da lista para localizar a empresa desejada. É possível classificar cada coluna em ordem crescente ou decrescente clicando no cabeçalho da coluna desejada.
1. Click the **[!UICONTROL Destinations]** tab.
1. Para criar um novo destino, clique em **[!UICONTROL Add Destination]**. To edit an existing destination, click the destination's name in the **[!UICONTROL Name]** column.

## Configurações básicas {#basic-settings}

Fill in the fields in the **[!UICONTROL Basic Settings]** window.

* **[!UICONTROL Name]** : (Obrigatório) Especifique o nome desse destino.
* **[!UICONTROL Description]** : Especifique informações descritivas sobre este destino.
* **[!UICONTROL Type]** : (Obrigatório) Selecione o tipo de destino desejado:
   * **[!UICONTROL Bulk ID]**: Sincronizar IDs entre plataformas diferentes.
   * **[!UICONTROL Bulk Trait]**: Envie informações características em massa para diferentes plataformas.
   * **[!UICONTROL Bulk Segment]**: Envie informações do segmento em massa para plataformas diferentes.
   * **[!UICONTROL S2S]**: Use destinos de servidor para servidor para enviar dados em tempo real e em lote para diferentes plataformas.
* **[!UICONTROL Auto-Fill Destination Mapping]** : ( [!UICONTROL S2S] somente) Selecione uma opção:
   * **[!UICONTROL Segment ID]** : Se você selecionar essa configuração, o mapeamento do valor de destino será preenchido com a ID do [!DNL Audience Manager] segmento.
   * **[!UICONTROL Integration Code Value]** : Se você selecionar essa configuração, o mapeamento do valor de destino será preenchido com o código de integração do [!DNL Audience Manager] segmento.
* **[!UICONTROL User ID Key]** : (Obrigatório) Selecione a chave de ID de usuário desejada para esse destino na lista suspensa.

Essa ID é usada como a ID da fonte de dados mestre. Isso determina as IDs de usuário a serem exageradas no arquivo.

>[!NOTE]
>
>Para o tipo de [!UICONTROL Bulk ID] destino, não é possível usar a ID [!DNL Audience Manager] ou a [!UICONTROL User ID] [!DNL Adobe Experience Cloud] .

Se a ID da fonte de dados ( [!UICONTROL DPID]) não for exibida na lista suspensa, você deverá marcar a caixa de **[!UICONTROL Outbound]** seleção no nível da fonte de dados na página [Configurações da fonte de](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/data-sources/manage-datasources.html)dados.

* **[!UICONTROL Target Data Source]** : (Obrigatório) Selecione a fonte de dados desejada para esse destino na lista suspensa. Essa configuração permite a rotulação de dados externos, o que permite a ingestão em sistemas separados do lado do cliente.
* **[!UICONTROL Foreign Account ID]** : Especifique a ID da conta estrangeira para este destino. Esse é o valor de identificação no sistema do destinatário para esses dados delimitados.
* **[!UICONTROL Outbound Sample Rate Denominator]** : Quando a quantidade total de dados retornados for desconhecida, use essa configuração para retornar apenas uma quantidade de dados de amostra, em vez da quantidade total. Ajuste o número aqui para representar uma fração dos dados (por exemplo, um valor de '100' retorna 1/100º a quantidade regular de dados, um valor de '10' retorna 1/10º a quantidade regular de dados). O padrão é "1", que retorna todos os dados.

## Dados em tempo real (para destinos S2S) {#realtime-s2s}

Se você estiver criando um [!UICONTROL S2S] destino, preencha os campos abaixo:

**[!UICONTROL Servers]**: Selecione o `HTTP` servidor desejado para este destino.
**[!UICONTROL Format]**: Selecione o formato desejado para este destino na lista suspensa: [!UICONTROL HTTP only].

>[!NOTE]
>
>Somente [!DNL S2S] para, você pode ativar ou desativar [!UICONTROL Realtime] ou [!UICONTROL Batch] destinos usando os controles deslizantes Off/On na tela. Não é possível desativar ambas as opções.

## Dados em lote {#batch-data}

Para [!UICONTROL Bulk ID]ou [!UICONTROL Bulk Trait] [!UICONTROL Bulk Segment] destinos, preencha os campos abaixo:

* **[!UICONTROL Protocol]**: (Obrigatório) Selecione o protocolo desejado para este destino na lista suspensa:
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**: (Obrigatório) Selecione o servidor desejado para este destino na lista suspensa.
* **[!UICONTROL Format]**: (Obrigatório) Selecione o formato desejado para este destino na lista suspensa: [!DNL HTTP] ou tipo de arquivo, dependendo do protocolo escolhido acima.
* **[!UICONTROL Sync Type]**: (Obrigatório) Selecione o tipo de sincronização desejado para este destino. Isso indica o nível de atividades do usuário que os clientes desejam incluir nas ordens de saída. Selecione **[!UICONTROL Customer]** se os clientes estão interessados apenas em analisar as qualificações de segmento de suas propriedades. Selecione **[!UICONTROL Platform]** se deseja incluir qualificações de segmento de atividades fora do site em todos os [!DNL Audience Manager] clientes.
* **[!UICONTROL Customer]**: O arquivo contém usuários ativos que têm pelo menos 1 característica de realização somente nas propriedades do cliente (associadas às do cliente [!UICONTROL PID]) para o período selecionado. Seus clientes devem usar essa opção para enviar suas qualificações de segmento em tempo *real* para destinos.
* **[!UICONTROL Platform]**: O arquivo contém usuários ativos que têm pelo menos 1 interação em tempo real, seja sincronização de ID ou realização de característica, em qualquer lugar nas propriedades de todos os [!DNL Audience Manager] clientes (associadas a todos os PIDs do cliente) durante o período selecionado. Seus clientes devem usar essa opção para enviar suas qualificações *totais* de segmento para destinos.
* **[!UICONTROL Lifetime]**: O arquivo contém usuários ativos vistos em qualquer lugar nas propriedades de todos os [!DNL Audience Manager] clientes desde a criação do destino.
* **[!UICONTROL Sync Type Lookback Period]**: Se você selecionar [!UICONTROL Customer] ou [!UICONTROL Platform], selecione um período de tempo. Os arquivos contêm usuários ativos para o período selecionado.
Em seguida, selecione o tipo de pedido. Isso indica a frequência e o escopo de cada integração externa com parceiros. Selecione entre ordens incrementais e completas.
* **[!UICONTROL Incremental Scheduled Run]**: Com cada execução, somente [!DNL Audience Manager] expulsará os novos usuários qualificados da rede desde a ordem de saída anterior. Selecione o período de tempo desejado para [!DNL Audience Manager] executar processos de sincronização incremental. Por exemplo, você pode selecionar a cada 24 horas, a cada sete dias, a cada 30 dias, ou nunca.

>[!NOTE] {important="high"}
>
>A primeira ordem incremental é equivalente a um pedido completo, pois nenhum usuário anterior foi enviado para o destino.

* **[!UICONTROL Full Sync Scheduled Run]**: Com cada execução, todos os usuários ativos [!DNL Audience Manager] serão enviados desde que o destino foi configurado pela primeira vez. Selecione o agendamento desejado que deseja usar [!DNL Audience Manager] para executar processos de sincronização completos. Por exemplo, você pode selecionar a cada 24 horas, a cada sete dias, a cada 30 dias, ou nunca.

>[!NOTE] {important="high"}
>
>Recomendamos usar sincronizações incrementais com mais frequência do que sincronizações completas. As sincronizações incrementais só enviam arquivos que contêm novas realizações de características ou sincronizações de ID. As sincronizações completas enviam todos os arquivos, independentemente de incluírem ou não novas realizações ou sincronizações de ID. Use a [!UICONTROL Full Sync Scheduled Run] configuração somente quando os clientes precisarem de uma cópia completa de todos os usuários, para reduzir o volume de dados de saída.

## Configurar fontes de dados {#configure-data-sources}

Para [!UICONTROL Bulk ID]ou para [!UICONTROL Bulk Trait] [!UICONTROL Bulk Segment] destinos, preencha os campos abaixo. Essas configurações permitem que você envie todos os dados (características, segmentos ou IDs, com base no tipo selecionado) associados às fontes de dados.

* **[!UICONTROL All Unrestricted First Party Data]**: Selecione para usar todas as fontes de dados originais. Se você selecionar essa opção, as [!UICONTROL Available Data Sources] opções serão desativadas.
* **[!UICONTROL Available Data Sources]**: Use as setas para mover fontes de dados entre as caixas **[!UICONTROL Available Data Sources]** e **[!UICONTROL In File Data Sources]** .

## Salvar e finalizar {#save-and-finalize}

O **[!UICONTROL Save]** botão é ativado depois de preencher todos os campos obrigatórios. Clique em **[!UICONTROL Save]** para finalizar o processo de criação de destino.

## Excluir destinos da empresa {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

Para excluir um destino:

1. Clique em **[!UICONTROL Companies]**, localize e clique na empresa desejada, em seguida, clique na **[!UICONTROL Destinations]** guia.
1. Clique ![](assets/icon_delete.png) na **[!UICONTROL Actions]** coluna do destino desejado.
1. Clique em **[!UICONTROL OK]para confirmar a exclusão.**

>[!NOTE]
>
>Não é possível excluir um destino se ele tiver segmentos mapeados para ele.