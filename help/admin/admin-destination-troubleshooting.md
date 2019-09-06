---
description: Informações que ajudam a configurar destinos no Audience Manager e evitar problemas comuns.
seo-description: Informações que ajudam a configurar destinos no Audience Manager e evitar problemas comuns.
seo-title: Solução de problemas de instalação de destino
title: Solução de problemas de instalação de destino
uuid: 04080 fb 9-6 c 7 b -4 de 7-960 e -54482 be 2 de 83
translation-type: tm+mt
source-git-commit: 118e8fa3f35bc77846c6518268448d57d779a2ee

---


# Solução de problemas de instalação de destino {#destination-setup-troubleshooting}

Informações que ajudam a configurar destinos no Audience Manager e evitar problemas comuns.

## Eu configure um destino, mas não vejo nenhum arquivo. Onde estão? {#destination-no-files}

<!-- c_dest_tshooting.xml -->

Problemas comuns de configuração de destino incluem os seguintes problemas:

### Destino incorreto

* **Chave incorreta[!UICONTROL UserID]:** [!UICONTROL UserID] A chave é o [!UICONTROL MasterDPID] desse destino e é a base para os valores de ID que serão excluídos. Mesmo que uma [!UICONTROL UserID] tecla seja selecionável por meio da lista suspensa, ela não significa necessariamente que há IDs/características/segmentos mapeados para esse valor. Se [!UICONTROL Outbound] o processo (que é executado após a criação de destinos) não encontrar nenhum usuário mapeado para essa [!UICONTROL UserID] chave, nenhum dado será ignorado.
* **Não em Fontes de Dados de Arquivo Selecionadas:** Ao escolher qualquer tipo de destino diferente [!UICONTROL S2S]de, uma seção aparece na parte inferior da tela rotulada [!UICONTROL Configure Data Sources]. Quando esta seção é exibida pela primeira vez, nenhum valor é selecionado. Se você esquecer de clicar na [!UICONTROL All First Party] caixa de seleção ou selecionar individualmente as fontes de dados da [!UICONTROL Available Data Sources] janela, nenhum dado será ignorado.

### Formato incorreto

Ao selecionar um formato para seus dados delimitados, é melhor, se possível, reutilizar um formato existente. O uso de um formato já comprovado garante que seus dados de saída sejam gerados com sucesso. Para ver exatamente como um formato existente é formatado, clique na [!UICONTROL Formats] opção na barra de menus e procure seu formato por nome ou número de ID. Formatos malformados ou macros usados em formatos fornecerão uma saída formatada incorretamente ou impedirá a saída total das informações.

Para obter mais informações sobre como configurar formatos e usar macros, consulte [Formato de arquivo Macros](formats/file-formats.md#) e [Macros de formato HTTP](formats/web-formats.md).

### Servidor configurado

* **[!DNL FTP]**
   * **[!UICONTROL Domain]**
      * Não insira prefixos para nomes de hosts. Se tiver uma conta [!DNL ftp://hello.com], basta inserir [!DNL hello.com] neste campo.
   * **[!UICONTROL Port/Type Combination]**
      * Para [!DNL FTP] uma transferência, o tipo de transferência preferencial é [!DNL SFTP].
      * Ao selecionar o [!DNL SFTP] tipo, a porta é quase sempre 22.
      * Ao selecionar o [!DNL FTPs/TLS] tipo, a porta é quase sempre 21.
      * [!DNL FTPs/TLS] O tipo não é igual a [!DNL FTP] uma transferência regular. Não oferecemos suporte [!DNL FTP] a transferências regulares (não seguras).
   * **[!UICONTROL Remote Path]**
      * Ao escolher um subcaminho remoto, ele deve ser inserido sem uma barra lateral.
      * Se o seu arquivo transferido deve ser colocado na [!DNL (root)/inbound] subpasta, basta adicionar [!DNL inbound] apenas para o caminho remoto.[!DNL /inbound]
      * Se você enviar seus arquivos vários diretórios para baixo, insira barras entre cada diretório. Se você tiver o local de [!DNL /inbound/subdirectory1/subdirectory2], insira [!DNL inbound/subdirectory1/subdirectory2] nesse campo.
      * Se o seu arquivo deve ser colocado no diretório roteado automaticamente pelo servidor externo, deixe este espaço em branco. Não insira um ponto (. ), barra (/) ou qualquer outra coisa.

* **[!DNL S3]**
   * [!DNL S3] é o protocolo de transferência preferencial (over [!DNL FTP] ou [!DNL HTTP]).
      * **[!UICONTROL Bucket]**
         * O nome do bucket deve ser listado sem barras, prefixos, sufixos etc. Se você receber o endereço [!DNL s3://your-bucket] , basta adicionar [!DNL your-bucket] a esse campo.
      * **[!UICONTROL Directory]**
         * Deixe esse campo em branco, a menos que você esteja especificamente determinado um subdiretório no qual os dados devem ser colocados. Se for fornecido o endereço [!DNL s3://your-bucket/your-subdirectory], digite [!DNL your-bucket] no [!UICONTROL Bucket] campo e [!DNL your-subdirectory] deverá ser adicionado ao [!UICONTROL Directory] campo. Não adicione barras anteriores.
         * Se você precisar encaminhar vários diretórios para baixo, apenas então deverá usar barras como separadores. Portanto, um local de [!DNL s3://your-bucket/your-subdirectory1/your-subdirectory2] um local seria [!DNL your-bucket][!UICONTROL Bucket] inserido e [!DNL your-subdirectory1/your-subdirectory2] inserido no [!UICONTROL Directory] campo.
      * **[!UICONTROL Access / Secret Keys]**
         * Quando [!DNL TechOps] cria um bucket e fornece chaves de acesso/segredo para um consultor, essas credenciais geralmente `READ-ONLY` são credenciais destinadas a serem enviadas ao cliente. Essas credenciais não devem ser inseridas nos [!UICONTROL Access / Secret Key] campos, pois isso causará falha na transferência (porque essas credenciais são somente leitura, não graváveis). No caso em que [!DNL TechOps] cria um bucket e fornece credenciais, o consultor também deve solicitar um par de chave da Adobe - NOT A SER FORNECIDO AO CLIENTE - que permitirá a gravação de arquivos nesse bucket. Essa chave deve ser adicionada nesses campos.

* **[!DNL HTTP]**
   * **[!UICONTROL Domain]**
      * Insira informações de prefixo para [!DNL HTTP] entradas. Se tiver uma conta [!DNL https://superduper.com], insira [!DNL https://superduper.com] neste campo.
      * **[!UICONTROL URL Prefix]**
         * Ao adicionar um [!DNL URL] prefixo, deixe a barra anterior desativada. Um endereço de [!DNL https://hello.com/r/x/y/z] deve [!DNL https://hello.com] ter inserido no [!UICONTROL Domain] campo e [!DNL r/x/y/z] inserido aqui no [!UICONTROL URL Prefix] campo.
         * Se não [!UICONTROL URL Prefix] for necessário, deixe este valor em branco.
      * **[!UICONTROL Authentication - SSH Key]**
         * Digite o valor `SSH PRIVATE` de chave completo nesta caixa, incluindo cabeçalhos, rodapés e quebras de linha para garantir a criptografia/armazenamento de chaves precisos.

### Tempo insuficiente para geração de saída

O processo delimitador é executado duas vezes ao dia e vários processos (tempo limite, publicação, movimentação para locais externos etc.) deve ser executada antes de um arquivo ser enviado para o destino final. Uma boa regra de miniatura é que um destino deve ser totalmente configurado por 24 horas para que você possa esperar que os dados sejam encaminhados para um local externo.

### Tamanhos de divisão de arquivo muito grandes

Quando arquivos offline para destinos, você pode dividir arquivos de saída maiores nos intervalos de arquivo. Certifique-se de que os blocos de arquivo individuais não excedam 10 GB. Consulte também o [Nome do arquivo de dados de saída: Sintaxe e exemplos](https://docs.adobe.com/help/en/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/outbound-file-name-contents.html).


## Como configurar seus destinos para exportar IDs da Experience Cloud, IDs do cliente ou IDs do Audience Manager nos arquivos de dados de saída {#set-up-destinations-export}

Essa página mostra como configurar destinos para exportar dados com o texto da ID que [!UICONTROL Outbound Data Files]deseja.

<!-- set-up-destinations-mcid-aamid.xml -->

Os destinos permitem que nossos clientes ativem seus dados em qualquer número de canais digitais. Por exemplo, eles podem exportar dados de público-alvo para outras [!DNL Adobe Experience Cloud] soluções ([!DNL Target], [!DNL Campaign]etc.). Ou, eles podem enviar dados para [!UICONTROL DSP]s, [!UICONTROL SSP]s ou qualquer plataforma integrada com o Audience Manager. Mantemos uma lista de parceiros com os quais trabalhamos em nossa [página Wiki de Integrações](https://wiki.corp.adobe.com/display/MCPI).

>[!NOTE]
>
>Para obter uma apresentação detalhada sobre como criar destinos na interface do usuário do Admin, consulte o [artigo Criar ou editar destinos](companies/admin-manage-company-destinations.md#create-edit-company-destinations) da empresa.

Seus clientes desejam exportar diferentes tipos de ID, dependendo do destino. O gráfico de configuração abaixo mostra as opções que você deve selecionar para exportar informações de perfil relacionadas a tipos de ID diferentes. Recomendamos que você também se refira ao [Índice de IDs no Audience Manager](https://marketing.adobe.com/resources/help/en_US/aam/ids-in-aam.html). Há três configurações importantes a serem consideradas, a [!UICONTROL User ID Key], [!UICONTROL Data Source Type] a e [!UICONTROL Format]a. Detalhamos todos eles abaixo.

* [!UICONTROL User ID Key]. No [!UICONTROL Admin UI], vá **[!UICONTROL Companies]** para. Pesquise pela empresa do cliente e clique nela. Procure a **[!UICONTROL Destinations]** guia e pressione **[!UICONTROL Add Destination]**. No **[!UICONTROL Add Destination]** fluxo de trabalho, selecione o [!UICONTROL User ID Key]. O [!UICONTROL User ID Key] filtro filtrará as IDs de entrada da fonte de dados de destino e permitirá que as IDs sejam transmitidas.

   ![](assets/user_id_key.PNG)

* [!UICONTROL Data Source Type]. Selecione isso ao criar um destino na interface do usuário do Audience Manager. Primeiro, selecione [!UICONTROL Inbound]e selecione o tipo de ID desejado. As opções são:

   ![](assets/data_source_settings.PNG)

* [!UICONTROL Format]. Essa opção determina o formato de arquivo que será exportado. No **[!UICONTROL Add Destination]** fluxo de trabalho, em **[!UICONTROL Batch Data]**, selecione o formato.

Para inspecionar um formato, vá **[!UICONTROL Admin UI > Formats]** para e procure pelo [!UICONTROL Data Row] elemento. Esse elemento contém uma macro do formato de arquivo, &lt; MCID &gt; no exemplo abaixo.

![](assets/data_row.PNG)

<table id="table_DAEE5BC75DCB4FC690C4BAE41F627DEC"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> Configuração não. </th> 
   <th colname="col1" class="entry"> <p>Chave do usuário </p> </th> 
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
   <td colname="col3"> <p>&lt; DP_ UUID &gt; </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 2 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>UUID do Audience Manager </p> </td> 
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
   <td colname="col2"> <p>ID do Audience Manager </p> </td> 
   <td colname="col3"> <p>&lt; DP_ UUID &gt; </p> </td> 
   <td colname="col4"> <p>UUID do Audience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 5 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>ID do Audience Manager </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 6 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>ID do Audience Manager </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>UUID do Audience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 7 </td> 
   <td colname="col1"> <p>DPID (qualquer fonte de dados a que a empresa tenha acesso) </p> </td> 
   <td colname="col2"> <p>Customer ID </p> </td> 
   <td colname="col3"> <p>&lt; DP_ UUID &gt; </p> </td> 
   <td colname="col4"> <p>ID do cliente (DPUUID) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 8 </td> 
   <td colname="col1"> <p>DPID (qualquer fonte de dados a que a empresa tenha acesso) </p> </td> 
   <td colname="col2"> <p>Customer ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 9 </td> 
   <td colname="col1"> <p>DPID (qualquer fonte de dados a que a empresa tenha acesso) </p> </td> 
   <td colname="col2"> <p>Customer ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>UUID do Audience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 10 </td> 
   <td colname="col1"> <p>DPID (qualquer fonte de dados a que a empresa tenha acesso) </p> </td> 
   <td colname="col2"> <p>ID do Audience Manager </p> </td> 
   <td colname="col3"> <p>&lt; DP_ UUID &gt; </p> </td> 
   <td colname="col4"> <p>UUID do Audience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 11 </td> 
   <td colname="col1"> <p>DPID (qualquer fonte de dados a que a empresa tenha acesso) </p> </td> 
   <td colname="col2"> <p>ID do Audience Manager </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 12 </td> 
   <td colname="col1"> <p>DPID (qualquer fonte de dados a que a empresa tenha acesso) </p> </td> 
   <td colname="col2"> <p>ID do Audience Manager </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>UUID do Audience Manager </p> </td> 
  </tr> 
 </tbody> 
</table>

## Casos de uso

Digamos que você use o Audience Manager e [!DNL Campaign]. Para tornar os dados do cliente acionáveis, [!DNL Campaign]você deseja exportar [!UICONTROL Experience Cloud IDs]. Nesse caso, você deve usar o número 3 da configuração.