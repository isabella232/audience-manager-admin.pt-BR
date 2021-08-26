---
description: Informações para ajudar a configurar destinos no Audience Manager e evitar problemas comuns.
seo-description: Information to help you set up destinations in Audience Manager and avoid common problems.
seo-title: Destination Setup Troubleshooting
title: Solução de problemas de configuração de destino
uuid: 04080fb9-6c7b-4de7-960e-54482be2de83
exl-id: 53c72b1a-f1a1-4266-a595-e4821c2640b2
source-git-commit: 1f4dbf8f7b36e64c3015b98ef90b6726d0e7495a
workflow-type: tm+mt
source-wordcount: '1316'
ht-degree: 4%

---

# Solução de problemas de configuração de destino {#destination-setup-troubleshooting}

Informações para ajudar a configurar destinos no Audience Manager e evitar problemas comuns.

## Eu configurei um destino, mas não vejo nenhum arquivo. Onde eles estão? {#destination-no-files}

<!-- c_dest_tshooting.xml -->

Problemas comuns de configuração de destino incluem os seguintes problemas:

### Destino mal configurado

* **[!UICONTROL UserID] Chave incorreta:** a  [!UICONTROL UserID] chave é a  [!UICONTROL MasterDPID] do destino e é a base para os valores de ID que serão excluídos. Mesmo que uma tecla [!UICONTROL UserID] seja selecionável por meio da lista suspensa, isso não significa necessariamente que há IDs/características/segmentos mapeados para esse valor. Se o processo [!UICONTROL Outbound] (que é executado depois da criação dos destinos) não encontrar usuários mapeados para essa chave [!UICONTROL UserID], nenhum dado será excedido.
* **Não em fontes de dados de arquivo selecionadas:** ao escolher qualquer tipo de destino diferente de  [!UICONTROL S2S], uma seção é exibida na parte inferior da tela com o rótulo  [!UICONTROL Configure Data Sources]. Quando esta seção é exibida pela primeira vez, nenhum valor é selecionado. Caso se esqueça de clicar na caixa de seleção [!UICONTROL All First Party] ou selecionar fontes de dados individualmente na janela [!UICONTROL Available Data Sources], nenhum dado será exagerado.

### Formato mal configurado

Ao selecionar um formato para seus dados de saída, é melhor, se possível, reutilizar um formato existente. Usar um formato já comprovado garante que seus dados de saída sejam gerados com sucesso. Para ver exatamente como um formato existente é formatado, clique na opção [!UICONTROL Formats] na barra de menus e procure seu formato por nome ou por número de ID. Formatos mal formados ou macros usados em formatos fornecerão saída formatada incorretamente ou impedirão que as informações sejam totalmente geradas.

Para obter mais informações sobre como configurar formatos e usar macros, consulte [Macros de formato de arquivo](formats/file-formats.md#) e [Macros de formato HTTP](formats/web-formats.md).

### Servidor mal configurado

* **[!DNL FTP]**
   * **[!UICONTROL Domain]**
      * Não insira nenhum prefixo para nomes de host. Se você receber uma conta [!DNL ftp://hello.com], basta inserir [!DNL hello.com] neste campo.
   * **[!UICONTROL Port/Type Combination]**
      * Para uma transferência [!DNL FTP], o tipo de transferência preferencial é [!DNL SFTP].
      * Ao selecionar o tipo [!DNL SFTP], a porta é quase sempre 22.
      * Ao selecionar o tipo [!DNL FTPs/TLS], a porta é quase sempre 21.
      * O tipo [!DNL FTPs/TLS] não é o mesmo que uma transferência regular [!DNL FTP]. Não oferecemos suporte a transferências regulares (não seguras) [!DNL FTP].
   * **[!UICONTROL Remote Path]**
      * Ao escolher um subcaminho remoto, ele deve ser inserido sem barra à esquerda.
      * Se o arquivo transferido tiver que ser colocado na subpasta [!DNL (root)/inbound], basta adicionar [!DNL inbound] para o caminho remoto, não [!DNL /inbound].
      * Se você enviar seus arquivos para vários diretórios abaixo do caminho, digite barras entre cada diretório. Se a localização de [!DNL /inbound/subdirectory1/subdirectory2] for fornecida, digite [!DNL inbound/subdirectory1/subdirectory2] neste campo.
      * Se o arquivo deve ser colocado no diretório roteado automaticamente para o pelo servidor externo, deixe esse espaço em branco. Não insira um ponto ( . ), barra ( / ) ou qualquer outra coisa.

* **[!DNL S3]**
   * [!DNL S3] é o protocolo de transferência preferencial (em vez de  [!DNL FTP] ou  [!DNL HTTP]).
      * **[!UICONTROL Bucket]**
         * O nome do bucket deve ser listado sem barras, prefixos, sufixos, etc. Se o endereço [!DNL s3://your-bucket] for exibido, basta adicionar [!DNL your-bucket] a esse campo.
      * **[!UICONTROL Directory]**
         * Deixe esse campo em branco, a menos que você receba especificamente um subdiretório em que os dados devem ser colocados. Se você receber o endereço [!DNL s3://your-bucket/your-subdirectory], digite [!DNL your-bucket] no campo [!UICONTROL Bucket] e [!DNL your-subdirectory] deverá ser adicionado ao campo [!UICONTROL Directory]. Não adicione barras anteriores.
         * Se for necessário viajar vários diretórios para baixo no caminho, use barras como separadores. Portanto, um local de [!DNL s3://your-bucket/your-subdirectory1/your-subdirectory2] teria [!DNL your-bucket] no campo [!UICONTROL Bucket] e [!DNL your-subdirectory1/your-subdirectory2] inserido no campo [!UICONTROL Directory].
      * **[!UICONTROL Access / Secret Keys]**
         * Quando [!DNL TechOps] cria um bucket e fornece chaves de acesso/segredo para um consultor, essas credenciais geralmente são `READ-ONLY` credenciais que devem ser enviadas ao cliente. Essas credenciais não devem ser inseridas nos campos [!UICONTROL Access / Secret Key], pois isso causará a falha da transferência (porque essas credenciais são somente leitura, não graváveis). No caso em que [!DNL TechOps] cria um bucket e fornece credenciais, o consultor também deve solicitar um par de Adobe key - NÃO DEVE SER FORNECIDO AO CLIENTE - que permitirá a gravação de arquivos nesse bucket. Essa chave deve ser adicionada a esses campos.

* **[!DNL HTTP]**
   * **[!UICONTROL Domain]**
      * Insira informações de prefixo para entradas [!DNL HTTP]. Se você receber uma conta [!DNL https://superduper.com], digite [!DNL https://superduper.com] neste campo.
      * **[!UICONTROL URL Prefix]**
         * Ao adicionar um prefixo [!DNL URL], deixe a barra anterior desligada. Um endereço de [!DNL https://hello.com/r/x/y/z] deve ter [!DNL https://hello.com] inserido no campo [!UICONTROL Domain] e [!DNL r/x/y/z] inserido aqui no campo [!UICONTROL URL Prefix].
         * Se um [!UICONTROL URL Prefix] não for necessário, deixe esse valor em branco.
      * **[!UICONTROL Authentication - SSH Key]**
         * Insira o valor completo da chave `SSH PRIVATE` nessa caixa, incluindo cabeçalhos, rodapés e quebras de linha para garantir criptografia/armazenamento de chave precisa.

### Tempo insuficiente para geração de saída

O processo delimitador é executado duas vezes ao dia e vários processos (emulação, publicação, envio para locais externos etc.) deve ser executado antes que um arquivo seja enviado para seu destino final. Um princípio básico é que um destino deve ser totalmente configurado pelo menos 24 horas antes de você esperar que os dados sejam enviados para um local externo.

### Tamanhos de divisão de arquivo muito grandes

Ao enviar arquivos para destinos, você pode dividir arquivos de saída maiores em blocos de arquivo. Certifique-se de que os fragmentos de arquivo individuais não excedam 10 GB. Consulte também, [Nome do arquivo de dados de saída: Sintaxe e exemplos](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/outbound-file-name-contents.html?lang=en).


## Como configurar seus destinos para exportar IDs de Experience Cloud, IDs do cliente ou IDs de Audience Manager em arquivos de dados de saída {#set-up-destinations-export}

Esta página mostra como configurar destinos para exportar dados com o tipo de ID que você deseja em [!UICONTROL Outbound Data Files].

<!-- set-up-destinations-mcid-aamid.xml -->

Os destinos permitem que nossos clientes ativem seus dados em qualquer número de canais digitais. Por exemplo, eles podem exportar dados do público para outras soluções [!DNL Adobe Experience Cloud] ([!DNL Target], [!DNL Campaign], etc.). Ou podem enviar dados para [!UICONTROL DSP]s, [!UICONTROL SSP]s ou qualquer plataforma integrada ao Audience Manager. Mantemos uma lista de parceiros com os quais trabalhamos em nossa [página Wiki de Integrações](https://wiki.corp.adobe.com/display/MCPI).

>[!NOTE]
>
>Para obter uma apresentação detalhada sobre como criar destinos na interface do usuário do administrador, consulte o artigo [Criar ou editar destinos da empresa](companies/admin-manage-company-destinations.md#create-edit-company-destinations) .

Seus clientes desejam exportar diferentes tipos de ID, dependendo do destino. O gráfico de configuração abaixo mostra as opções que você deve selecionar para exportar informações de perfil relacionadas a tipos de ID diferentes. Recomendamos que você também se refira ao [Índice de IDs no Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html?lang=en). Há três configurações importantes a serem consideradas, [!UICONTROL User ID Key], [!UICONTROL Data Source Type] e [!UICONTROL Format]. Detalhamos todos abaixo.

* [!UICONTROL User ID Key]. No [!UICONTROL Admin UI], vá para **[!UICONTROL Companies]**. Procure a empresa do seu cliente e clique nela. Procure a guia **[!UICONTROL Destinations]** e pressione **[!UICONTROL Add Destination]**. No workflow **[!UICONTROL Add Destination]**, selecione o [!UICONTROL User ID Key]. O [!UICONTROL User ID Key] filtrará as IDs recebidas da fonte de dados de destino e permitirá que apenas as IDs sejam enviadas.

   ![](assets/user_id_key.PNG)

* [!UICONTROL Data Source Type]. Selecione essa opção ao criar um destino na interface do usuário do Audience Manager. Primeiro, selecione [!UICONTROL Inbound] e selecione o tipo de ID desejado. As opções são:

   ![](assets/data_source_settings.PNG)

* [!UICONTROL Format]. Essa opção determina o formato de arquivo que será exportado. No workflow **[!UICONTROL Add Destination]**, em **[!UICONTROL Batch Data]**, selecione o formato.

Para inspecionar um formato, vá para **[!UICONTROL Admin UI > Formats]** e procure pelo elemento [!UICONTROL Data Row]. Esse elemento contém uma macro do formato de arquivo, &lt;MCID> no exemplo abaixo.

![](assets/data_row.PNG)

<table id="table_DAEE5BC75DCB4FC690C4BAE41F627DEC"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> Nº de configuração </th> 
   <th colname="col1" class="entry"> <p>Chave de usuário </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo de fonte de dados </p> </th> 
   <th colname="col3" class="entry"> <p>Formato </p> </th> 
   <th colname="col4" class="entry"> <p>Tipo de ID exportado </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> 1 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 2 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 3 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 4 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 5 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 6 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 7 </td> 
   <td colname="col1"> <p>DPID (qualquer fonte de dados à qual a empresa tenha acesso) </p> </td> 
   <td colname="col2"> <p>Customer ID </p> </td> 
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
   <td colname="col4"> <p>ID do cliente (DPUUID) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 8 </td> 
   <td colname="col1"> <p>DPID (qualquer fonte de dados à qual a empresa tenha acesso) </p> </td> 
   <td colname="col2"> <p>Customer ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 9 </td> 
   <td colname="col1"> <p>DPID (qualquer fonte de dados à qual a empresa tenha acesso) </p> </td> 
   <td colname="col2"> <p>Customer ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 10 </td> 
   <td colname="col1"> <p>DPID (qualquer fonte de dados à qual a empresa tenha acesso) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 11 </td> 
   <td colname="col1"> <p>DPID (qualquer fonte de dados à qual a empresa tenha acesso) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 12 </td> 
   <td colname="col1"> <p>DPID (qualquer fonte de dados à qual a empresa tenha acesso) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
 </tbody> 
</table>

## Casos de uso

Digamos que você use Audience Manager e [!DNL Campaign]. Para tornar os dados do cliente acionáveis em [!DNL Campaign], é necessário exportar [!UICONTROL Experience Cloud IDs]. Nesse caso, você deve usar a configuração número 3.
