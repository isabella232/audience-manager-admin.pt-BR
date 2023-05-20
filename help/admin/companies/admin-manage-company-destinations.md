---
description: Criar, editar e excluir destinos de Audience Manager.
seo-description: Create, edit, and delete Audience Manager destinations.
seo-title: Manage Company Destinations
title: Gerenciar destinos da empresa
uuid: d9a6bfb1-7629-44e0-b7d7-ece44f65ea2b
exl-id: a2e73613-07cd-4ab8-8c6e-be451ed50bfc
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '1068'
ht-degree: 1%

---

# Gerenciar destinos da empresa {#manage-company-destinations}

Criar, editar e excluir destinos de Audience Manager.

<!-- t_company_destinations.xml -->

Para obter informações detalhadas, consulte [Destinos](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/destinations/destinations.html) no *Guia do usuário do Audience Manager*.

## Criar ou editar destinos da empresa {#create-edit-company-destinations}

Percorra as seções para obter instruções passo a passo sobre como criar novos [!DNL Audience Manager] destinos ou editar destinos existentes.

<!-- create-edit-company-destinations.xml -->

Visite o [página de integração do parceiro Experience Cloud](https://wiki.corp.adobe.com/x/mPIMPw) antes de configurar destinos. A página contém as informações específicas que você precisa preencher para cada [!DNL Audience Manager] integração de parceiros.

Se o cliente quiser usar [!DNL Adobe Media Optimizer] como destino no [!DNL Audience Manager] , é necessário configurar isso em [!DNL Adobe Media Optimizer].

## Navegue até a guia Destinos {#navigate-destinations}

1. Clique em **[!UICONTROL Companies]**, localize e clique na empresa desejada para exibir sua [!UICONTROL Profile] página. Você pode usar o [!UICONTROL Search] ou nos controles de paginação na parte inferior da lista para localizar a empresa desejada. Você pode classificar cada coluna em ordem crescente ou decrescente clicando no cabeçalho da coluna desejada.
1. Clique em **[!UICONTROL Destinations]** guia.
1. Para criar um novo destino, clique **[!UICONTROL Add Destination]**. Para editar um destino existente, clique no nome do destino na **[!UICONTROL Name]** coluna.

## Configurações básicas {#basic-settings}

Preencha os campos no **[!UICONTROL Basic Settings]** janela.

* **[!UICONTROL Name]:** (Obrigatório) Especifique o nome deste destino.
* **[!UICONTROL Description]:** Especifique informações descritivas sobre este destino.
* **[!UICONTROL Type]:** (Obrigatório) Selecione o tipo de destino desejado:
   * **[!UICONTROL Bulk ID]**: IDs de sincronização entre plataformas diferentes.
   * **[!UICONTROL Bulk Trait]**: envia informações de características em massa para plataformas diferentes.
   * **[!UICONTROL Bulk Segment]**: envia informações de segmento em massa para plataformas diferentes.
   * **[!UICONTROL S2S]**: use destinos de servidor para servidor para enviar dados em lote e em tempo real para plataformas diferentes.
* **[!UICONTROL Auto-Fill Destination Mapping]:** ( [!UICONTROL S2S] somente) Selecione uma opção:
   * **[!UICONTROL Segment ID]:** Se você selecionar essa configuração, o mapeamento de valores de destino será preenchido com a variável [!DNL Audience Manager] ID do segmento.
   * **[!UICONTROL Integration Code Value]:** Se você selecionar essa configuração, o mapeamento de valores de destino será preenchido com a variável [!DNL Audience Manager] Código de integração do segmento.
* **[!UICONTROL User ID Key]:** (Obrigatório) Selecione a chave de ID de usuário desejada para esse destino na lista suspensa.

Essa ID é usada como a ID da fonte de dados principal. Isso determina as IDs de usuário a serem ultrapassadas no arquivo.

>[!NOTE]
>
>Para o [!UICONTROL Bulk ID] tipo de destino, não é possível usar o [!DNL Audience Manager] [!UICONTROL User ID] ou o [!DNL Adobe Experience Cloud] ID.

Se a ID da fonte de dados ( [!UICONTROL DPID]) não for exibida na lista suspensa, você deverá selecionar a variável **[!UICONTROL Outbound]** no nível da fonte de dados, na [Página Configurações da fonte de dados](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/manage-datasources.html).

* **[!UICONTROL Target Data Source]:** (Obrigatório) Selecione a origem de dados desejada para esse destino na lista suspensa. Essa configuração permite rotular os dados enviados, o que permite a assimilação em sistemas separados do lado do cliente.
* **[!UICONTROL Foreign Account ID]:** Especifique a ID da conta externa para este destino. Este é o valor de identificação no sistema do recipient para esses dados limitados.
* **[!UICONTROL Outbound Sample Rate Denominator]:** Quando a quantidade total de dados retornados for desconhecida, use essa configuração para retornar apenas uma quantidade de dados de amostra, em vez da quantidade total. Ajuste o número aqui para representar uma fração dos dados (por exemplo, um valor de &quot;100&quot; retorna 1/100 da quantidade regular de dados, um valor de &quot;10&quot; retorna 1/10 da quantidade regular de dados). O padrão é &#39;1&#39;, que retorna todos os dados.

## Dados em tempo real (para destinos S2S) {#realtime-s2s}

Se você estiver criando uma [!UICONTROL S2S] destino, preencha os campos abaixo:

**[!UICONTROL Servers]**: selecione o desejado `HTTP` servidor para este destino.
**[!UICONTROL Format]**: selecione o formato desejado para esse destino na lista suspensa: [!UICONTROL HTTP only].

>[!NOTE]
>
>Para [!DNL S2S] somente, você pode ativar ou desativar [!UICONTROL Realtime] ou [!UICONTROL Batch] destinos usando os controles deslizantes na tela Desligado/Ligado. Não é possível desativar as duas opções.

## Dados em lote {#batch-data}

Para [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] ou [!UICONTROL Bulk Segment] destinos, preencha os campos abaixo:

* **[!UICONTROL Protocol]**: (Obrigatório) Selecione o protocolo desejado para esse destino na lista suspensa:
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**: (Obrigatório) Selecione o servidor desejado para esse destino na lista suspensa.
* **[!UICONTROL Format]**: (Obrigatório) Selecione o formato desejado para esse destino na lista suspensa: [!DNL HTTP] ou tipo de arquivo, dependendo do protocolo escolhido acima.
* **[!UICONTROL Sync Type]**: (Obrigatório) Selecione o tipo de sincronização desejado para esse destino. Isso indica o nível de atividades de usuário que os clientes desejariam incluir nas ordens de saída. Selecionar **[!UICONTROL Customer]** se os clientes estiverem interessados apenas em analisar as qualificações de segmento de suas propriedades. Selecionar **[!UICONTROL Platform]** se quiserem incluir qualificações de segmento de atividades externas em todas as [!DNL Audience Manager] clientes.
* **[!UICONTROL Customer]**: o arquivo contém usuários ativos que têm pelo menos uma realização de característica apenas nas propriedades do cliente (associadas às propriedades do cliente) [!UICONTROL PID]) para o período selecionado. Seus clientes devem usar essa opção para enviar seus *tempo real* qualificações de segmento para destinos.
* **[!UICONTROL Platform]**: o arquivo contém usuários ativos que têm pelo menos uma interação em tempo real, seja ela de sincronização de ID ou de realização de características, em qualquer lugar em todo o [!DNL Audience Manager] propriedades dos clientes (associadas a todos os PIDs do cliente) para o período selecionado. Seus clientes devem usar essa opção para enviar seus *total* qualificações de segmento para destinos.
* **[!UICONTROL Lifetime]**: o arquivo contém usuários ativos vistos em qualquer lugar em todos os [!DNL Audience Manager] propriedades dos clientes desde a criação do destino.
* **[!UICONTROL Sync Type Lookback Period]**: Se você selecionar [!UICONTROL Customer] ou [!UICONTROL Platform], selecione um período. Os arquivos contêm usuários ativos para o período selecionado.
Em seguida, selecione o tipo de pedido. Isso indica a frequência e o escopo de cada integração de saída com parceiros. Selecione entre pedidos incrementais e completos.
* **[!UICONTROL Incremental Scheduled Run]**: com cada execução, [!DNL Audience Manager] só gerará a saída dos novos usuários qualificados desde a ordem de saída anterior. Selecione o período desejado [!DNL Audience Manager] para executar processos de sincronização incremental. Por exemplo, você pode selecionar a cada 24 horas, a cada sete dias, a cada 30 dias ou nunca.

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>A primeira ordem incremental é equivalente a uma ordem completa porque nenhum usuário anterior foi enviado ao destino.

* **[!UICONTROL Full Sync Scheduled Run]**: com cada execução, [!DNL Audience Manager] enviará todos os usuários ativos desde que o destino foi configurado pela primeira vez. Selecione o cronograma desejado [!DNL Audience Manager] a ser usado para executar processos de sincronização completos. Por exemplo, você pode selecionar a cada 24 horas, a cada sete dias, a cada 30 dias ou nunca.

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>Recomendamos usar sincronizações incrementais com mais frequência do que sincronizações completas. As sincronizações incrementais só enviam arquivos que contêm novas realizações de características ou sincronizações de ID. Sincronizações completas enviam todos os arquivos, independentemente de incluírem ou não novas realizações ou sincronizações de ID. Use somente o [!UICONTROL Full Sync Scheduled Run] quando os clientes precisam de uma cópia completa de todos os usuários, para reduzir o volume de dados de saída.

## Configurar fontes de dados {#configure-data-sources}

Para [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] ou [!UICONTROL Bulk Segment] destinos, preencha os campos abaixo. Essas configurações permitem enviar todos os dados (características, segmentos ou IDs, com base no tipo selecionado) associados às fontes de dados.

* **[!UICONTROL All Unrestricted First Party Data]**: selecione para usar todas as fontes de dados primárias. Se você selecionar essa opção, a variável [!UICONTROL Available Data Sources] opções estão desativadas.
* **[!UICONTROL Available Data Sources]**: use as setas para mover fontes de dados entre as **[!UICONTROL Available Data Sources]** e **[!UICONTROL In File Data Sources]** caixas.

## Salvar e finalizar {#save-and-finalize}

A variável **[!UICONTROL Save]** é ativado depois de preencher todos os campos obrigatórios. Clique em **[!UICONTROL Save]** para finalizar o processo de criação de destino.

## Excluir destinos da empresa {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

Para excluir um destino:

1. Clique em **[!UICONTROL Companies]**, localize e clique na empresa desejada e, em seguida, clique na **[!UICONTROL Destinations]** guia.
1. Clique em  ![](assets/icon_delete.png) no **[!UICONTROL Actions]** do destino desejado.
1. Clique em **[!UICONTROL OK]** para confirmar a exclusão.

>[!NOTE]
>
>Não é possível excluir um destino se ele tiver segmentos mapeados a ele.
