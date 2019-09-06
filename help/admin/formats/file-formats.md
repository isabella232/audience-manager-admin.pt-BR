---
description: Lista as macros que você pode usar para criar arquivos de dados baseados em FTP. Algumas macros podem ser usadas para todos os campos de arquivo de dados e linhas. Outras macros são específicas apenas para linhas de cabeçalho e dados.
seo-description: Lista as macros que você pode usar para criar arquivos de dados baseados em FTP. Algumas macros podem ser usadas para todos os campos de arquivo de dados e linhas. Outras macros são específicas apenas para linhas de cabeçalho e dados.
seo-title: Macros de formato de arquivo
title: Macros de formato de arquivo
uuid: f 91 c 91 b 6-6581-4 ed 7-8 d 7 f-f 8532 bd 41 df 9
translation-type: tm+mt
source-git-commit: e1122a7f3d3e8c2d67616eb56cb186a4750ed29b

---


# Macros de formato de arquivo {#file-format-macros}

Lista as macros que você pode usar para criar [!DNL FTP]arquivos de dados com base em -. Algumas macros podem ser usadas para todos os campos de arquivo de dados e linhas. Outras macros são específicas apenas para linhas de cabeçalho e dados.

## Macros comuns {#common-macros}

Essas macros podem ser usadas em qualquer campo de formato. Para ver exemplos, consulte [Exemplos de formato de arquivo](../formats/file-format-examples.md).

<table id="table_A3309E175ABF4651BD11CE3632B3C553"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Macro </th> 
   <th colname="col2" class="entry"> Descrição </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>ASCII_ SOH</code> </p> </td> 
   <td colname="col2"> <p>Um caractere ASCII não imprimível. Indica o início de uma linha ou uma seção do conteúdo. Ele também pode ser usado para separar colunas de dados em um arquivo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPID</code> </p> </td> 
   <td colname="col2"> <p>ID do provedor de dados de destino. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MASTER_ DPID</code> </p> </td> 
   <td colname="col2"> <p>ID do provedor de dados chave de ID de usuário. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ORDER_ ID</code> </p> </td> 
   <td colname="col2"> <p>ID de pedido/destino. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PIDALIAS</code> </p> </td> 
   <td colname="col2"> <p>Um alias para uma ID de pedido/destino. </p> <p>O valor desse alias é definido no campo ID <span class="wintitle"></span> da conta externa para um destino (na seção Configurações <span class="wintitle"></span> básicas). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_ MODE</code> </p> </td> 
   <td colname="col2"> <p>Indica o tipo de sincronização. Aceita as seguintes variáveis opcionais: </p> 
    <ul id="ul_87E8E3CE6565447A9810B5119298CC7B"> 
     <li id="li_66F4889FB84E40AC92F69F3FF6B0042C"> <code>completo</code>: Sincronização completa. </li> 
     <li id="li_BFE2C2D9A33A44FB9A840A7232ECCFFF"> <code>iter</code>: Sincronização incremental. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_ TYPE</code> </p> </td> 
   <td colname="col2"> <p>Indica o método de transferência de dados. Aceita as seguintes variáveis opcionais: </p> 
    <ul id="ul_13BE35BBBF7C4C67AEFC514C5D192902"> 
     <li id="li_195FE9B4C5494600BD17D7172A8FB630"> <code>ftp</code> </li> 
     <li id="li_751AD59C4C934D66BC530D9806B500AF"> <code>http</code> </li> 
     <li id="li_4638AF7D1FB54E2C890045048B85309C"> <code>s3</code> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TIMESTAMP</code> </p> </td> 
   <td colname="col2"> <p>Um carimbo de data e hora de 10 dígitos, UTC, Unix. </p> <p>Também pode ser formatado como <code>aaaammddhhmmss</code> seguindo as regras de formatação de data/hora do Java. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Macros de campo de cabeçalho {#header-field-macros}

Macros usadas apenas em campos de cabeçalho. Para ver exemplos, consulte [Exemplos de formato de arquivo](../formats/file-format-examples.md).

<table id="table_1A8BD1750F4940B3A34E3F80371A447A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Macro </th> 
   <th colname="col2" class="entry"> Descrição </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>TAB</code> </p> </td> 
   <td colname="col2"> <p>Usado como separador, essa macro insere uma guia entre campos. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Macros de linha de dados {#data-row-macros}

Macros usadas apenas em linhas de dados. Para ver exemplos, consulte [Exemplos de formato de arquivo](../formats/file-format-examples.md).

<table id="table_E378F94A3907407AA8110C8EE6C10909"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Macro </th> 
   <th colname="col2" class="entry"> Descrição </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>CLOSE_ CURLY_ BRACKET</code> </p> </td> 
   <td colname="col2"> <p>Insere um caractere colchete fechado}. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>VÍRGULA</code> </p> </td> 
   <td colname="col2"> <p>Insere uma vírgula. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_ UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="term"> Identificador de usuário exclusivo do parceiro de dados </span>. Retorna a ID atribuída a um visitante do usuário/site se essa ID já tiver sido sincronizada com uma ID do dispositivo <span class="keyword"> do Audience Manager </span> . </p> <p>Se a DPID for 0, essa macro retornará a ID <span class="keyword"> do Audience Manager </span> em vez de sua ID para o usuário. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_ UUID_ LIST</code> </p> </td> 
   <td colname="col2"> <p>Retorna uma lista que contém várias IDs para um parceiro de dados. Isso é útil se você tiver uma grande organização com várias subdivisões ou outros grupos organizacionais com os quais você pode compartilhar dados. Essa macro retorna uma lista das IDs para esses grupos subordinados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPUUIDS</code> </p> </td> 
   <td colname="col2"> <p>A saída dessa macro mapeia a ID do provedor de dados (DPID) para IDs de usuário exclusivas relacionadas (DPUUID). Essa macro deve ter uma string de formatação para controlar sua saída. A saída de amostra seria semelhante ao seguinte: </p> <p> <code>" dpids = dpid 1, dpid 2,… dpid n | maxmappings = n | format = json "</code> </p> <p>A configuração <code>maxmaappings</code> determina quantos mapeamentos você deseja que a macro retorne. Quando <code>maxmappings = 0</code>, essa macro retorna todos os mapeamentos para cada DPID especificado. Os dados são classificados por carimbo de data e hora (mais recente primeiro) e retorna resultados com o maior carimbo de data e hora. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>endif</code> </p> </td> 
   <td colname="col2"> <p>Necessário ao usar as macros conditional <code>if</code> e <code>SEGMENT_ LIST</code> e <code>REMOVED_ SEGMENT_ LIST</code> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>if (SEGMENT_ LIST &amp; &amp; REMOVED_ SEGMENT_ LIST) endif</code> </p> </td> 
   <td colname="col2"> <p>Essa combinação de macros cria uma declaração condicional que lista os segmentos aos quais os usuários pertencem <i>e</i> foram removidos. Ela retorna uma string vazia se ambas as condições não forem atendidas ou não houver dados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MCID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Adobe Experience Cloud </span> ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPEN_ CURLY_ BRACKET</code> </p> </td> 
   <td colname="col2"> <p>Insere uma chave aberta {caractere. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPT_ OUT</code> </p> </td> 
   <td colname="col2"> <p>Obsoleto. Não use. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OUTPUT_ ATTRIBUTE_ TYPE</code> </p> </td> 
   <td colname="col2"> <p>Obsoleto. Não use. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OUTPUT_ ATTRIBUTE_ VALUE</code> </p> </td> 
   <td colname="col2"> <p>Retorna <code>1</code> como um valor estático e codificado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PID</code> </p> </td> 
   <td colname="col2"> <p>ID do parceiro (PID). A PID aparece na guia <span class="wintitle"> Perfil </span> na interface do usuário do administrador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_ SEGMENT_ LIST</code> </p> </td> 
   <td colname="col2"> <p>Retorna uma lista de segmentos, se houver, que foram removidos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SEGMENT_ LIST</code> </p> </td> 
   <td colname="col2"> <p>Retorna uma lista de segmentos em uma lista. Aceita as seguintes variáveis opcionais: </p> 
    <ul id="ul_B111AA0D6C18445598A1444B8B7E9325"> 
     <li id="li_8603B40229624856AF1FBC434DB8F16A"> <code>Segmentid</code>: ID herdada. Obsoleto. Use <code>sid</code> (apenas para letras minúsculas). </li> 
     <li id="li_1EF40DDCA3C5447586904CF021D8F912"> <code>csegid</code>: ID herdada. Obsoleto. Use <code>sid</code> (apenas para letras minúsculas). </li> 
     <li id="li_D85F0A5D16AE4DAFB55C17DBB35EA66E"> <code>sid</code>: ID do segmento. </li> 
     <li id="li_9BE103EFD8384464B46FAC00422431DB"> <code>type</code>: Retorna <code>5</code>, um valor estático e codificado que identifica dados como dados de segmento. </li> 
     <li id="li_FE5049089F2944FA9DB9F9D546DBA167"> <code>alias</code>: Mapeamento do segmento. Obsoleto. Use <code>sid</code> (apenas para letras minúsculas). </li> 
     <li id="li_DD778AA2D1DB4D409CF5026B5D9DBD27"> <code>Lastupdatetime</code>: Um carimbo de data e hora Unix que indica a última vez que um segmento foi realizado. </li> 
    </ul> <p>Coloque essas variáveis entre chaves após a macro. Por exemplo, esse código separa os resultados com uma barra vertical|" caractere: <code>&lt; SEGMENT_ LIST: {seg|&lt; seg. type &gt;, &lt; seg. sid &gt;}; separator = "|" &gt;</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SET_ ATTRIBUTES</code> </p> </td> 
   <td colname="col2"> <p>Retorna <code>1</code> como um valor estático e codificado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TAB</code> </p> </td> 
   <td colname="col2"> <p>Insere um separador de tabulação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TRAIT_ LIST</code> </p> </td> 
   <td colname="col2"> <p>Retorna uma lista de características. Aceita os seguintes argumentos opcionais: </p> 
    <ul id="ul_757DEB56E4F849768468F3C166B0D171"> 
     <li id="li_859E1F4F21D645519F150DC512B3EB1A"> <code>type</code>: Tipos de características identificadas por uma ID numérica. Essa variável retorna: 
      <ul id="ul_C9839266783D42CCADAAC3FEA33BE4D7"> 
       <li id="li_6996A218E3F04EC3BC70032559DD87FC"> <code>10</code> que identifica uma característica DPM (offline, onboarenviada por um trabalho de entrada). </li> 
       <li id="li_831FF929BF50434C8804C13E5786DF79"> <code>3</code> que identifica uma característica baseada em regras (em tempo real; no <span class="wintitle"> DCS </span>). </li> 
      </ul> </li> 
     <li id="li_E84D6BC80AEE4F10963C9882C4151ED4"> <code>Traitid</code>: ID de característica. </li> 
     <li id="li_D30A849BA35248E6B9110FA3ADEFC332"> <code>Lastrealized</code>: A última vez que a característica foi realizada. Carimbo de data e hora Unix. </li> 
    </ul> <p>Coloque essas variáveis entre chaves após a macro. Por exemplo, esse código separa os resultados com uma barra vertical|" caractere: <code>TRAIT_ LIST {type | traitid}; separator = "|"</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> ID </span> de usuário do Audience Manager. </p> </td> 
  </tr> 
 </tbody> 
</table>