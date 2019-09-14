---
description: Lista as macros que podem ser usadas para criar arquivos de dados baseados em FTP. Algumas macros podem ser usadas para todos os campos e linhas do arquivo de dados. Outras macros são específicas somente para linhas de cabeçalho e de dados.
seo-description: Lista as macros que podem ser usadas para criar arquivos de dados baseados em FTP. Algumas macros podem ser usadas para todos os campos e linhas do arquivo de dados. Outras macros são específicas somente para linhas de cabeçalho e de dados.
seo-title: Macros de formato de arquivo
title: Macros de formato de arquivo
uuid: f91c91b6-6581-4ed7-8d7f-f8532bd41df9
translation-type: tm+mt
source-git-commit: e1122a7f3d3e8c2d67616eb56cb186a4750ed29b

---


# Macros de formato de arquivo {#file-format-macros}

Lista as macros que podem ser usadas para criar arquivos de dados [!DNL FTP]baseados. Algumas macros podem ser usadas para todos os campos e linhas do arquivo de dados. Outras macros são específicas somente para linhas de cabeçalho e de dados.

## Macros comuns {#common-macros}

Essas macros podem ser usadas em qualquer campo de formato. Para obter exemplos, consulte Exemplos [de macro de formato de](../formats/file-format-examples.md)arquivo.

<table id="table_A3309E175ABF4651BD11CE3632B3C553"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Macro </th> 
   <th colname="col2" class="entry"> Descrição </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>ASCII_SOH</code> </p> </td> 
   <td colname="col2"> <p>Um caractere ASCII não imprimível. Indica o início de uma linha ou de uma seção de conteúdo. Também pode ser usado para separar colunas de dados em um arquivo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPID</code> </p> </td> 
   <td colname="col2"> <p>ID do provedor de dados do Target. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MASTER_DPID</code> </p> </td> 
   <td colname="col2"> <p>ID do provedor de dados da chave de ID do usuário. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ORDER_ID</code> </p> </td> 
   <td colname="col2"> <p>ID do pedido / de destino. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PIDALIAS</code> </p> </td> 
   <td colname="col2"> <p>Um alias para uma ID de pedido/destino. </p> <p>O valor desse alias é definido no campo ID da conta <span class="wintitle"> estrangeira </span> para um destino (na seção Configurações <span class="wintitle"> básicas </span> ). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_MODE</code> </p> </td> 
   <td colname="col2"> <p>Indica o tipo de sincronização. Aceita as seguintes variáveis opcionais: </p> 
    <ul id="ul_87E8E3CE6565447A9810B5119298CC7B"> 
     <li id="li_66F4889FB84E40AC92F69F3FF6B0042C"> <code>completo</code>: Sincronização completa. </li> 
     <li id="li_BFE2C2D9A33A44FB9A840A7232ECCFFF"> <code>iter</code>: Sincronização incremental. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_TYPE</code> </p> </td> 
   <td colname="col2"> <p>Indica o método de transferência de dados. Aceita as seguintes variáveis opcionais: </p> 
    <ul id="ul_13BE35BBBF7C4C67AEFC514C5D192902"> 
     <li id="li_195FE9B4C5494600BD17D7172A8FB630"> <code>ftp</code> </li> 
     <li id="li_751AD59C4C934D66BC530D9806B500AF"> <code>http</code> </li> 
     <li id="li_4638AF7D1FB54E2C890045048B85309C"> <code>s3</code> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>CARIMBO DE DATA E HORA</code> </p> </td> 
   <td colname="col2"> <p>Um carimbo de data e hora de 10 dígitos, UTC, Unix. </p> <p>Também pode ser formatado como <code>AAAMMDDhmmmss</code> após as regras de formatação de data/hora do Java. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Macros de campo de cabeçalho {#header-field-macros}

Macros usadas somente em campos de cabeçalho. Para obter exemplos, consulte Exemplos [de macro de formato de](../formats/file-format-examples.md)arquivo.

<table id="table_1A8BD1750F4940B3A34E3F80371A447A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Macro </th> 
   <th colname="col2" class="entry"> Descrição </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>GUIA</code> </p> </td> 
   <td colname="col2"> <p>Usada como separador, essa macro insere uma guia entre os campos. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Macros de linha de dados {#data-row-macros}

Macros usadas somente em linhas de dados. Para obter exemplos, consulte Exemplos [de macro de formato de](../formats/file-format-examples.md)arquivo.

<table id="table_E378F94A3907407AA8110C8EE6C10909"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Macro </th> 
   <th colname="col2" class="entry"> Descrição </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>CLOSE_CURLY_BRACKET</code> </p> </td> 
   <td colname="col2"> <p>Insere um caractere de chave fechada }. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>VÍRGULA</code> </p> </td> 
   <td colname="col2"> <p>Insere uma vírgula. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="term"> Identificador de Usuário Único do Parceiro de Dados </span>. Retorna a ID atribuída a um usuário/visitante do site se essa ID já tiver sido sincronizada com uma ID de <span class="keyword"> dispositivo do </span> Audience Manager. </p> <p>Se o DPID for 0, essa macro retornará a <span class="keyword"> ID do Audience Manager </span> em vez da ID do usuário. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID_LIST</code> </p> </td> 
   <td colname="col2"> <p>Retorna uma lista que contém várias IDs para um parceiro de dados. Isso é útil se você tiver uma organização grande com várias subdivisões ou outros grupos organizacionais com os quais você pode compartilhar dados. Essa macro retorna uma lista das IDs para esses grupos subordinados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPUUIDS</code> </p> </td> 
   <td colname="col2"> <p>A saída dessa macro mapeia a ID do provedor de dados (DPID) para IDs de usuário exclusivas relacionadas (DPUUID). Essa macro deve ter uma string de formatação para controlar sua saída. A saída da amostra seria semelhante ao seguinte: </p> <p> <code>"dpids=dpid1,dpid2,...dpid n|maxMappings= n|format=json"</code> </p> <p>A configuração <code>maxMappings</code> determina quantos mapeamentos você deseja que a macro retorne. Quando <code>maxMappings=0</code>, essa macro retorna todos os mapeamentos de cada DPID especificado. Os dados são classificados por carimbo de data e hora (o mais recente primeiro) e retorna os resultados com o maior carimbo de data e hora primeiro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>endif</code> </p> </td> 
   <td colname="col2"> <p>Obrigatório ao usar as macros condicional <code>if</code> e <code>SEGMENT_LIST</code> e <code>REMOVED_SEGMENT_LIST</code> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>if(SEGMENT_LIST &amp;&amp; REMOVED_SEGMENT_LIST)endif</code> </p> </td> 
   <td colname="col2"> <p>Essa combinação de macros cria uma declaração condicional que lista os segmentos aos quais os usuários pertencem <i>e dos quais</i> foram removidos. Retorna uma string vazia se ambas as condições não forem atendidas ou não houver dados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MCID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Adobe Experience Cloud </span> ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPEN_CURLY_BRACKET</code> </p> </td> 
   <td colname="col2"> <p>Insere um caractere { colchetes abertos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPT_OUT</code> </p> </td> 
   <td colname="col2"> <p>Obsoleto. Não utilizar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OUTPUT_ATTRIBUTE_TYPE</code> </p> </td> 
   <td colname="col2"> <p>Obsoleto. Não utilizar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OUTPUT_ATTRIBUTE_VALUE</code> </p> </td> 
   <td colname="col2"> <p>Retorna <code>1</code> como um valor estático codificado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PID</code> </p> </td> 
   <td colname="col2"> <p>ID do parceiro (PID). O PID é exibido sob a <span class="wintitle"> guia Perfil </span> na interface do usuário do administrador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p>Retorna uma lista de segmentos, se houver, que foram removidos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p>Retorna uma lista de segmentos em uma lista. Aceita as seguintes variáveis opcionais: </p> 
    <ul id="ul_B111AA0D6C18445598A1444B8B7E9325"> 
     <li id="li_8603B40229624856AF1FBC434DB8F16A"> <code>segmentId</code>: ID herdada. Obsoleto. Use <code>sid</code> (apenas minúsculas). </li> 
     <li id="li_1EF40DDCA3C5447586904CF021D8F912"> <code>csegid</code>: ID herdada. Obsoleto. Use <code>sid</code> (apenas minúsculas). </li> 
     <li id="li_D85F0A5D16AE4DAFB55C17DBB35EA66E"> <code>sid</code>: ID do segmento. </li> 
     <li id="li_9BE103EFD8384464B46FAC00422431DB"> <code>tipo</code>: Retorna <code>5</code>, um valor estático e codificado que identifica dados como dados de segmento. </li> 
     <li id="li_FE5049089F2944FA9DB9F9D546DBA167"> <code>alias</code>: Mapeamento do segmento. Obsoleto. Use <code>sid</code> (apenas minúsculas). </li> 
     <li id="li_DD778AA2D1DB4D409CF5026B5D9DBD27"> <code>lastUpdateTime</code>: Um carimbo de data e hora Unix que indica a última vez que um segmento foi realizado. </li> 
    </ul> <p>Coloque essas variáveis entre chaves após a macro. Por exemplo, esse código separa os resultados com um caractere de barra vertical "|": <code>&lt;SEGMENT_LIST:{seg|&lt;seg.type&gt;,&lt;seg.sid&gt;}; separador="|"&gt;</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SET_ATTRIBUTES</code> </p> </td> 
   <td colname="col2"> <p>Retorna <code>1</code> como um valor estático codificado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>GUIA</code> </p> </td> 
   <td colname="col2"> <p>Insere um separador de tabulação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TRAIT_LIST</code> </p> </td> 
   <td colname="col2"> <p>Retorna uma lista de características. Aceita os seguintes argumentos opcionais: </p> 
    <ul id="ul_757DEB56E4F849768468F3C166B0D171"> 
     <li id="li_859E1F4F21D645519F150DC512B3EB1A"> <code>tipo</code>: Tipos de características identificados por uma ID numérica. Essa variável retorna: 
      <ul id="ul_C9839266783D42CCADAAC3FEA33BE4D7"> 
       <li id="li_6996A218E3F04EC3BC70032559DD87FC"> <code>10</code> que identifica uma característica do DPM (offline, integrada por uma tarefa de entrada). </li> 
       <li id="li_831FF929BF50434C8804C13E5786DF79"> <code>3</code> que identifica uma característica baseada em regras (tempo real,; a bordo através do <span class="wintitle"> DCS </span>). </li> 
      </ul> </li> 
     <li id="li_E84D6BC80AEE4F10963C9882C4151ED4"> <code>traitId</code>: ID da característica. </li> 
     <li id="li_D30A849BA35248E6B9110FA3ADEFC332"> <code>lastRealized</code>: A última vez que o traço foi realizado. Carimbo de data e hora Unix. </li> 
    </ul> <p>Coloque essas variáveis entre chaves após a macro. Por exemplo, esse código separa os resultados com um caractere de barra vertical "|": <code>TRAIT_LIST{type|traitId};separator="|"</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> ID de </span> usuário do Audience Manager. </p> </td> 
  </tr> 
 </tbody> 
</table>