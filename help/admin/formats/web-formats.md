---
description: Lista as macros que podem ser usadas para criar arquivos de dados HTTP. HTTP envia dados em um formato JSON.
seo-description: Lista as macros que podem ser usadas para criar arquivos de dados HTTP. HTTP envia dados em um formato JSON.
seo-title: Macros de formato HTTP
title: Macros de formato HTTP
uuid: 91021f60-75d0-4b1d-86ca-91c9dadafac1
translation-type: tm+mt
source-git-commit: 1a547e421346a6bf281e2b3ff3a0bcb5cf1d78df

---


# Macros de formato HTTP {#http-format-macros}

Lista as macros que podem ser usadas para criar arquivos [!DNL HTTP] de dados. [!DNL HTTP] envia dados em um [!DNL JSON] formato.

Consulte os Exemplos [de macro de formato](../formats/web-format-examples.md) HTTP para obter uma lista e exemplos de algumas combinações de macro comumente usadas.

<table id="table_72A72EA63C3643FB84B47A76CD2CC1CA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Macro </th> 
   <th colname="col2" class="entry"> Tipo de método </th> 
   <th colname="col3" class="entry"> Descrição </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>AAM_UUID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p> <span class="keyword"> Audience Manager </span> ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>ID de usuário único do parceiro de dados. Essa macro retorna a ID atribuída a um usuário se a ID já tiver sido sincronizada com uma ID de <span class="keyword"> </span> dispositivo do Audience Manager. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>ID do provedor de dados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ECID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>ID do provedor de dados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>GENERATION_TIME</code> </p> </td> 
   <td colname="col2"> <p> <code>OBTER, PUBLICAR</code> </p> </td> 
   <td colname="col3"> <p>Carimbo de data e hora UTC Unix. Um carimbo de data e hora interno representa o momento em que o AAM foi notificado para publicar o destino <span class="wintitle"> S2S </span> para nossos parceiros. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>IP</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>O endereço IP do usuário. </p> </td> 
  </tr>
    <tr> 
   <td colname="col1"> <p> <code>MCID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Experience Cloud ID. (MCID significa Marketing Cloud, que é o nome herdado da Experience Cloud) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>NUM_REMOVED_SEGMENTS</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>O número (inteiro) de segmentos aos quais um usuário não pertence mais. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>NUM_SEGMENTS</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>O número de segmentos aos quais um usuário pertence. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ORDER_ID</code> </p> </td> 
   <td colname="col2"> <p> <code>OBTER, PUBLICAR</code> </p> </td> 
   <td colname="col3"> <p>ID do pedido ou de destino. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PID_ALIAS</code> </p> </td> 
   <td colname="col2"> <p> <code>OBTER, PUBLICAR</code> </p> </td> 
   <td colname="col3"> <p>Um alias para a ID do parceiro. Também conhecido como ID de conta estrangeira. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ALEATORIA</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Gera um número aleatório. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REGION_ID_LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>A região DCS do <a href="https://docs.adobe.com/help/en/audience-manager/user-guide/api-and-sdk-code/dcs/dcs-api-reference/dcs-regions.html"> Audience Manager </a> onde a atividade se originou.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Retorna uma lista de IDs de segmento, se houver, para as quais um usuário não se qualifica mais. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_SEGMENTS</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Uma lista de segmentos para os quais um usuário não se qualifica mais. Você também pode retornar campos de segmento específicos que incluem: </p> <p> 
     <ul id="ul_29B83093A7624A908F0C06F2A248981A"> 
      <li id="li_57A60A54F5D44E38ACB4E2648095F246"> <code>traitAlias</code> </li> 
      <li id="li_4079F646493F40DBA0CE75D662A69454"> <code>legacySegmentId (antigo segmentId)</code> </li> 
      <li id="li_D3509A2D379E4C1FB3BC1B5E7D45A916"> <code>newSegmentId</code> </li> 
      <li id="li_EA901C20EEEB4CFAA39A5E0E822D2394"> <code>status</code> </li> 
      <li id="li_6310E21F88CC4691980DD3C9D551409F"> <code>dateTime</code> </li> 
     </ul> </p> <p>Especifique esses campos em uma matriz como mostrado neste exemplo: </p> <p> <code>[&lt;REMOVED_SEGMENTS:{seg|&lt;OPEN_BRACKET&gt;"Mapeamento":&lt;seg.traitAlias&gt;,"Estado:"&lt;seg.status&gt;, "Tempo":&lt;seg.dateTime&gt;,"LegacySegmentId":&lt;seg.LegacySegmentId&gt;, "NewSegmentId":&lt;seg.NewSegment Id&gt;&lt;CLOSE_BRACKET&gt;}; "separator=","&gt;]</code> </p> <p>Consulte também Exemplos de macro de formato <a href="../formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31"> HTTP </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_TIME_LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> Uma lista de últimas realizações para segmentos para os quais o usuário não se qualifica mais. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_TRAITALIAS_LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Uma lista de nomes com alias de segmentos para os quais um usuário não se qualifica mais. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Retorna uma lista de IDs de segmento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SEGMENTOS</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Uma lista de segmentos para os quais um usuário se qualifica. Você também pode retornar campos de segmento específicos que incluem: </p> <p> 
     <ul id="ul_9209683A8E0A4B8081E5EFA4602F743F"> 
      <li id="li_D796526C1C9E45BEA891D619539888C4"> <code>traitAlias</code> </li> 
      <li id="li_BF12E010E1AD432C84605B9817F209DD"> <code>legacySegmentId (antigo segmentId)</code> </li> 
      <li id="li_4A81E3B715254549B9EADB983A2FC32B"> <code>newSegmentId</code> </li> 
      <li id="li_1F01A60829DF4C87879D94299E1D589C"> <code>status</code> </li> 
      <li id="li_E52F10CD5A04487D81A4B1750B0DC4E3"> <code>dateTime</code> </li> 
     </ul> </p> <p>Especifique esses campos em uma matriz como mostrado neste exemplo: </p> <p> <code>[&lt;SEGMENTOS:{seg|&lt;OPEN_BRACKET&gt;"Mapeamento":&lt;seg.traitAlias&gt;,"Estado:"&lt;seg.status&gt;, "Tempo":&lt;seg.dateTime&gt;,"LegacySegmentId":&lt;seg.LegacySegmentId&gt;, "NewSegmentId":&lt;seg.NewSegmentId&gt; CLOSE_BRACKET&gt;}; "separator=","&gt;]</code> </p> <p>Consulte também Exemplos de macro de formato <a href="../formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31"> HTTP </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TIME_LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Uma lista das últimas realizações. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>CARIMBO DE DATA E HORA</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Unix, carimbo de data e hora UTC. Representa a última realização do segmento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TRAITALIAS_LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Uma lista de nomes com alias para um segmento específico. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>USER_AGENT</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Agente do usuário da solicitação inicial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>USER_LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>POSTAGEM</code> </p> </td> 
   <td colname="col3"> <p>Uma lista de IDs de <span class="keyword"> usuário do Audience Manager </span> . Também é possível retornar campos específicos que incluem: </p> 
    <ul id="ul_B6857D809FDC46749B7E745BD8C45F8E"> 
     <li id="li_F31CD82D16ED41FD82518141D90B5B35"> <code>user.aamUuid</code> </li> 
     <li id="li_623FA758C84D4A2D9B25C7FBE90F62B7"> <code>user.dpUuid</code> </li> 
     <li id="li_976B941908EB494EB476B5FB68B8972D"> <code>user.segment</code> </li> 
     <li id="li_D7E129833D1E4D59A554FFCE353924EE"> <code>user.removeSegments</code> </li> 
     <li id="li_8B3DD69D3FE3493492FC9F162812FCD5"> <code>user.userAgent</code> </li> 
     <li id="li_8C7EA05585A64141876DF169C31322FE"> <code>user.ip</code> </li> 
     <li id="li_678076A31A7743C480F718C9E7A07E99"> <code>user.dpuuids</code> </li> 
     <li id="li_B598A5AED28C4304972E51DBD4E480D8"> <code>user.timestamp</code> </li> 
     <li id="li_8424D540282F449CA5AF6B3CC343DDCB"> <code>user.random</code> </li>
     <li><code>user.regionIds</code></li> 
    </ul> <p>Especifique estes campos como mostrado neste exemplo: </p> <p> 
     <codeblock>
       "AAM_UUID": "&lt;user.aamUuid&gt;" "DataPartner_UUID": "&lt;user.dpUuid&gt;" 
     </codeblock> </p> <p>Consulte também Exemplos de macro de formato <a href="../formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31"> HTTP </a> para obter um exemplo completo. </p> </td> 
  </tr>
 </tbody>
</table>