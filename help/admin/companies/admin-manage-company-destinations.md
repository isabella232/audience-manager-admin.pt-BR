---
description: Crie, edite e exclua destinos do Audience Manager.
seo-description: Crie, edite e exclua destinos do Audience Manager.
seo-title: Gerenciar destinos da empresa
title: Gerenciar destinos da empresa
uuid: d 9 a 6 bfb 1-7629-44 e 0-b 7 d 7-ece 44 f 65 ea 2 b
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# Gerenciar destinos da empresa {#manage-company-destinations}

Crie, edite e exclua destinos do Audience Manager.

<!-- t_company_destinations.xml -->

Para obter informações detalhadas, consulte [Destinos](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/destinations/destinations.html) no Guia do usuário *do Audience Manager*.

## Criar ou editar destinos da empresa {#create-edit-company-destinations}

Role pelas seções para obter instruções passo a passo sobre como criar novos [!DNL Audience Manager] destinos ou editar destinos existentes.

<!-- create-edit-company-destinations.xml -->

Visite a [página de integração de parceiros da Experience Cloud](https://wiki.corp.adobe.com/x/mPIMPw) antes de configurar destinos. A página contém as informações específicas que você precisa preencher para cada [!DNL Audience Manager] integração de parceiro.

Se o cliente quiser usar [!DNL Adobe Media Optimizer] como destino, [!DNL Audience Manager] é necessário definir isso [!DNL Adobe Media Optimizer].

## Navigate to the Destinations Tab {#navigate-destinations}

1. Clique **[!UICONTROL Companies]** em, em seguida localize e clique na empresa desejada para exibir sua [!UICONTROL Profile] página. Você pode usar a [!UICONTROL Search] caixa ou os controles de paginação na parte inferior da lista para encontrar a empresa desejada. É possível classificar cada coluna em ordem crescente ou decrescente clicando no cabeçalho da coluna desejada.
1. Click the **[!UICONTROL Destinations]** tab.
1. Para criar um novo destino, clique **[!UICONTROL Add Destination]** em. To edit an existing destination, click the destination's name in the **[!UICONTROL Name]** column.

## Configurações básicas {#basic-settings}

Fill in the fields in the **[!UICONTROL Basic Settings]** window.

* **[!UICONTROL Name]:** (Obrigatório) Especifique o nome desse destino.
* **[!UICONTROL Description]:** Especifique informações descritivas sobre esse destino.
* **[!UICONTROL Type]:** (Obrigatório) Selecione o tipo de destino desejado:
   * **[!UICONTROL Bulk ID]**: Sincronizar IDs entre plataformas diferentes.
   * **[!UICONTROL Bulk Trait]**: Envie informações de características em massa para plataformas diferentes.
   * **[!UICONTROL Bulk Segment]**: Enviar informações de segmento em massa para plataformas diferentes.
   * **[!UICONTROL S2S]**: Use destinos de servidor para servidor para enviar dados em tempo real e em lote para plataformas diferentes.
* **[!UICONTROL Auto-Fill Destination Mapping]:** ( [!UICONTROL S2S] somente) Selecione uma opção:
   * **[!UICONTROL Segment ID]:** Se você selecionar essa configuração, o mapeamento de valor de destino será preenchido com a ID [!DNL Audience Manager] do segmento.
   * **[!UICONTROL Integration Code Value]:** Se você selecionar essa configuração, o mapeamento de valor de destino será preenchido com o código de integração [!DNL Audience Manager] Segmento.
* **[!UICONTROL User ID Key]:** (Obrigatório) Selecione a chave de ID de usuário desejada para este destino na lista suspensa.

Essa ID é usada como a ID de fonte de dados mestre. Isso determina as IDs de usuário a serem excluídas no arquivo.

>[!NOTE]
>
>Para o [!UICONTROL Bulk ID] tipo de destino, não é possível usar a [!DNL Audience Manager][!UICONTROL User ID] ID ou a [!DNL Adobe Experience Cloud] ID.

Se a sua ID de fonte de dados ( [!UICONTROL DPID]) não for exibida na lista suspensa, você deverá selecionar a **[!UICONTROL Outbound]** caixa de seleção no nível da fonte de dados na página Configurações da fonte [de dados](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/data-sources/manage-datasources.html).

* **[!UICONTROL Target Data Source]:** (Obrigatório) Selecione a fonte de dados desejada para esse destino na lista suspensa. Essa configuração permite a identificação de dados externos, o que permite a ingestão em sistemas separados no lado dos clientes.
* **[!UICONTROL Foreign Account ID]:** Especifique a ID da conta externa para este destino. Esse é o valor de identificação no sistema do destinatário para esses dados externos.
* **[!UICONTROL Outbound Sample Rate Denominator]:** Quando a quantidade total de dados retornados for desconhecida, use essa configuração para retornar apenas uma amostra de dados, em vez da quantia completa. Ajuste o número aqui para representar uma fração dos dados (por exemplo, um valor de "100" retorna 1/100 ª a quantidade regular de dados, um valor de "10" retorna 1/10 th ª a quantidade regular de dados). O padrão é ' 1 ', que retorna todos os dados.

## Dados em tempo real (para destinos S 2 S) {#realtime-s2s}

Se estiver criando um [!UICONTROL S2S] destino, preencha os campos abaixo:

**[!UICONTROL Servers]**: Selecione o `HTTP` servidor desejado para este destino.
**[!UICONTROL Format]**: Selecione o formato desejado para esse destino na lista suspensa: [!UICONTROL HTTP only].

>[!NOTE]
>
>Para [!DNL S2S] isso, é possível ativar ou desativar qualquer ou [!UICONTROL Realtime][!UICONTROL Batch] os destinos usando os controles deslizantes Off-line/Ligado. Não é possível desativar ambas as opções.

## Dados em lote {#batch-data}

Para [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] ou [!UICONTROL Bulk Segment] destinos, preencha os campos abaixo:

* **[!UICONTROL Protocol]**: (Obrigatório) Selecione o protocolo desejado para esse destino na lista suspensa:
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**: (Obrigatório) Selecione o servidor desejado para este destino na lista suspensa.
* **[!UICONTROL Format]**: (Obrigatório) Selecione o formato desejado para esse destino na lista suspensa: [!DNL HTTP] ou o tipo de arquivo, dependendo do protocolo escolhido acima.
* **[!UICONTROL Sync Type]**: (Obrigatório) Selecione o tipo de sincronização desejado para esse destino. Isso indica o nível de atividades do usuário que os clientes gostariam de incluir nos pedidos de saída. Selecione **[!UICONTROL Customer]** se os clientes estão interessados em analisar qualificações de segmentos de suas propriedades. Selecione **[!UICONTROL Platform]** se deseja incluir qualificações de segmento de atividades fora do site em todos [!DNL Audience Manager] os clientes.
* **[!UICONTROL Customer]**: O arquivo contém usuários ativos que têm pelo menos 1 execução característica somente nas propriedades do cliente (associadas ao's [!UICONTROL PID]) para o período selecionado. Seus clientes devem usar essa opção para ignorar *suas qualificações* de segmento em tempo real para destinos.
* **[!UICONTROL Platform]**: O arquivo contém usuários ativos que têm pelo menos 1 interação em tempo real, seja de sincronização de ID ou realização de características, em qualquer lugar em todas as propriedades [!DNL Audience Manager] dos clientes (associadas a todos os pids do cliente) para o período selecionado. Seus clientes devem usar essa opção para excluir suas *qualificações totais* de segmento para destinos.
* **[!UICONTROL Lifetime]**: O arquivo contém usuários ativos vistos em qualquer lugar nas propriedades [!DNL Audience Manager] dos clientes desde a criação do destino.
* **[!UICONTROL Sync Type Lookback Period]**: Se você selecionar [!UICONTROL Customer] ou [!UICONTROL Platform], selecionar um período de tempo. Os arquivos contêm usuários ativos para o período selecionado.
Em seguida, selecione o tipo de pedido. Isso indica a frequência e o escopo de cada integração de saída com parceiros. Selecione entre pedidos incrementais e completos.
* **[!UICONTROL Incremental Scheduled Run]**: Com cada execução, [!DNL Audience Manager] somente os novos usuários líquidos serão qualificados desde a ordem de saída anterior. Selecione o período de tempo desejado para [!DNL Audience Manager] executar processos de sincronização incremental. Por exemplo, você pode selecionar a cada 24 horas, a cada sete dias, a cada 30 dias, ou nunca.

>[!NOTE] {importance = "high"}
>
>A primeira ordem incremental é equivalente a uma ordem completa, pois nenhum usuário anterior foi enviado para o destino.

* **[!UICONTROL Full Sync Scheduled Run]**: A cada execução, [!DNL Audience Manager] será excluído todos os usuários ativos desde que o destino foi configurado pela primeira vez. Selecione o agendamento desejado que deseja usar [!DNL Audience Manager] para realizar processos completos de sincronização. Por exemplo, você pode selecionar a cada 24 horas, a cada sete dias, a cada 30 dias, ou nunca.

>[!NOTE] {importance = "high"}
>
>Recomendamos usar sincronizações incrementais com mais frequência do que sincronizações completas. As sincronizações incrementais apenas enviam arquivos que contêm novos recursos de características ou sincronizações de ID. As sincronizações completas enviam todos os arquivos, independentemente de estarem ou não incluídos novos realizações ou sincronizações de ID. Use apenas a [!UICONTROL Full Sync Scheduled Run] configuração quando os clientes precisam de uma cópia completa de todos os usuários para reduzir o volume de dados de saída.

## Configurar fontes de dados {#configure-data-sources}

Para [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] ou [!UICONTROL Bulk Segment] destinos, preencha os campos abaixo. Essas configurações permitem enviar todos os dados (características, segmentos ou IDs, com base no tipo selecionado) associado às fontes de dados.

* **[!UICONTROL All Unrestricted First Party Data]**: Selecione para usar todas as fontes de dados originais. Se você selecionar essa opção, [!UICONTROL Available Data Sources] as opções serão desativadas.
* **[!UICONTROL Available Data Sources]**: Use as setas para mover fontes de dados entre as caixas **[!UICONTROL Available Data Sources]** e as **[!UICONTROL In File Data Sources]** caixas.

## Salvar e finalizar {#save-and-finalize}

O **[!UICONTROL Save]** botão é ativado depois de preencher todos os campos obrigatórios. Clique **[!UICONTROL Save]** em para finalizar o processo de criação de destino.

## Excluir destinos da empresa {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

Para excluir um destino:

1. Clique **[!UICONTROL Companies]**, localize e clique na empresa desejada e clique na **[!UICONTROL Destinations]** guia.
1. Clique ![](assets/icon_delete.png) na **[!UICONTROL Actions]** coluna do destino desejado.
1. Clique em **[!UICONTROL OK]para confirmar a exclusão.**

>[!NOTE]
>
>Não é possível excluir um destino se ele tiver segmentos mapeados para ele.