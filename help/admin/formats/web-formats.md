---
description: Lista as macros que podem ser usadas para criar arquivos de dados HTTP. O HTTP envia dados em um formato JSON.
seo-description: Lista as macros que podem ser usadas para criar arquivos de dados HTTP. O HTTP envia dados em um formato JSON.
seo-title: Macros de formato HTTP
title: Macros de formato HTTP
uuid: 91021 f 60-75 d 0-4 b 1 d -86 ca -91 c 9 dadafac 1
translation-type: tm+mt
source-git-commit: 1a547e421346a6bf281e2b3ff3a0bcb5cf1d78df

---


# Macros de formato HTTP {#http-format-macros}

Lista as macros que podem ser usadas para criar [!DNL HTTP] arquivos de dados. [!DNL HTTP] envia dados em um [!DNL JSON] formato.

Consulte Exemplos de macro [HTTP](../formats/web-format-examples.md) para uma lista e exemplos de algumas combinações de macro frequentemente usadas.

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
   <td colname="col1"> <p> <code>AAM_ UUID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p> <span class="keyword"> ID do Audience Manager </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_ UUID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>ID de usuário exclusiva do parceiro de dados. Essa macro retorna a ID atribuída a um usuário se a ID já tiver sido sincronizada com uma ID de dispositivo <span class="keyword"> do Audience Manager </span> . </p> </td> 
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
   <td colname="col1"> <p> <code>GENERATION_ TIME</code> </p> </td> 
   <td colname="col2"> <p> <code>GET, POST</code> </p> </td> 
   <td colname="col3"> <p>Carimbo de data e hora Unix UTC. Um carimbo de data e hora interno representa o tempo de notificação do AAM para publicar o <span class="wintitle"></span> destino S 2 S nos parceiros. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>IP</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>O endereço IP do usuário. </p> </td> 
  </tr>
    <tr> 
   <td colname="col1"> <p> <code>MCID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Experience Cloud ID. (MCID corresponde à Marketing Cloud, que é o nome herdado da Experience Cloud) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>NUM_ REMOVED_ SEGMENTS</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>O número (número inteiro) de segmentos aos quais um usuário não pertence mais. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>NUM_ SEGMENTS</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>O número de segmentos aos quais um usuário pertence. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ORDER_ ID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET, POST</code> </p> </td> 
   <td colname="col3"> <p>ID de pedido ou de destino. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PID_ ALIAS</code> </p> </td> 
   <td colname="col2"> <p> <code>GET, POST</code> </p> </td> 
   <td colname="col3"> <p>Um alias para a ID do parceiro. Também conhecida como ID de conta externa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>RANDOM</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Gera um número aleatório. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REGION_ ID_ LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>A região DCS <a href="https://docs.adobe.com/help/en/audience-manager/user-guide/api-and-sdk-code/dcs/dcs-api-reference/dcs-regions.html"> do Audience Manager </a> onde a atividade se originou.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_ SEGMENT_ LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Retorna uma lista de IDs de segmento, se houver, que um usuário não é mais qualificado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_ SEGMENTS</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Uma lista de segmentos para os quais um usuário não é mais qualificado. Também é possível retornar campos de segmento específicos que incluem: </p> <p> 
     <ul id="ul_29B83093A7624A908F0C06F2A248981A"> 
      <li id="li_57A60A54F5D44E38ACB4E2648095F246"> <code>Traitalias</code> </li> 
      <li id="li_4079F646493F40DBA0CE75D662A69454"> <code>Legacysegmentid (antigo segmentid)</code> </li> 
      <li id="li_D3509A2D379E4C1FB3BC1B5E7D45A916"> <code>Newsegmentid</code> </li> 
      <li id="li_EA901C20EEEB4CFAA39A5E0E822D2394"> <code>status</code> </li> 
      <li id="li_6310E21F88CC4691980DD3C9D551409F"> <code>Datetime</code> </li> 
     </ul> </p> <p>Especifique esses campos em uma matriz, como mostra este exemplo: </p> <p> <code>[&lt; REMOVED_ SEGMENTS: {seg|&lt; OPEN_ BRACKET &gt; "Mapeamento": &lt; seg. traitalias &gt;, "Status: " &lt; seg. status &gt;, "Time": &lt; seg. datetime &gt;, "legacysegmentid": &lt; seg. legacysegmentid &gt;, "newsegmentid": &lt; seg. newsegmentid &gt; &lt; CLOSE_ BRACKET &gt;}; " separator = "," &gt;]</code> </p> <p>Consulte também Exemplos macro de formato <a href="../formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31"> HTTP </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_ TIME_ LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> Uma lista de últimos realizações para segmentos para os quais o usuário não é mais adequado. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_ TRAITALIAS_ LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Uma lista de nomes com alias de segmentos para os quais um usuário não é mais qualificado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SEGMENT_ LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Retorna uma lista de IDs de segmento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SEGMENTOS</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Uma lista de segmentos para os quais um usuário é qualificado. Também é possível retornar campos de segmento específicos que incluem: </p> <p> 
     <ul id="ul_9209683A8E0A4B8081E5EFA4602F743F"> 
      <li id="li_D796526C1C9E45BEA891D619539888C4"> <code>Traitalias</code> </li> 
      <li id="li_BF12E010E1AD432C84605B9817F209DD"> <code>Legacysegmentid (antigo segmentid)</code> </li> 
      <li id="li_4A81E3B715254549B9EADB983A2FC32B"> <code>Newsegmentid</code> </li> 
      <li id="li_1F01A60829DF4C87879D94299E1D589C"> <code>status</code> </li> 
      <li id="li_E52F10CD5A04487D81A4B1750B0DC4E3"> <code>Datetime</code> </li> 
     </ul> </p> <p>Especifique esses campos em uma matriz, como mostra este exemplo: </p> <p> <code>[&lt; SEGMENTOS: {seg|&lt; OPEN_ BRACKET &gt; "Mapeamento": &lt; seg. traitalias &gt;, "Status: " &lt; seg. status &gt;, "Time": &lt; seg. datetime &gt;, "legacysegmentid": &lt; seg. legacysegmentid &gt;, "newsegmentid": &lt; seg. newsegmentid &gt; &lt; CLOSE_ BRACKET &gt;}; " separator = "," &gt;]</code> </p> <p>Consulte também Exemplos macro de formato <a href="../formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31"> HTTP </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TIME_ LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Uma lista dos últimos realizações. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TIMESTAMP</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Unix, carimbo de data e hora UTC. Representa a última execução do segmento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TRAITALIAS_ LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Uma lista de nomes com alias para um segmento específico. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>USER_ AGENT</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Agente do usuário da solicitação inicial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>USER_ LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>POST</code> </p> </td> 
   <td colname="col3"> <p>Uma lista de IDs de usuário <span class="keyword"> do Audience Manager </span> . Você também pode retornar campos específicos que incluem o seguinte: </p> 
    <ul id="ul_B6857D809FDC46749B7E745BD8C45F8E"> 
     <li id="li_F31CD82D16ED41FD82518141D90B5B35"> <code>user. aamuuid</code> </li> 
     <li id="li_623FA758C84D4A2D9B25C7FBE90F62B7"> <code>user. dpuuid</code> </li> 
     <li id="li_976B941908EB494EB476B5FB68B8972D"> <code>user. segments</code> </li> 
     <li id="li_D7E129833D1E4D59A554FFCE353924EE"> <code>user. removedsegments</code> </li> 
     <li id="li_8B3DD69D3FE3493492FC9F162812FCD5"> <code>user. useragent</code> </li> 
     <li id="li_8C7EA05585A64141876DF169C31322FE"> <code>user. ip</code> </li> 
     <li id="li_678076A31A7743C480F718C9E7A07E99"> <code>user. dpuuids</code> </li> 
     <li id="li_B598A5AED28C4304972E51DBD4E480D8"> <code>user. timestamp</code> </li> 
     <li id="li_8424D540282F449CA5AF6B3CC343DDCB"> <code>user. random</code> </li>
     <li><code>user. regionids</code></li> 
    </ul> <p>Especifique esses campos como mostrado neste exemplo: </p> <p> 
     <codeblock>
       " AAM_ UUID ": " &lt; user. aamuuid &gt; "datapartner_ 
UUID": " &lt; user. dpuuid &gt; " 
     </codeblock> </p> <p>Consulte também Exemplos macro de formato <a href="../formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31"> HTTP </a> para obter um exemplo completo. </p> </td> 
  </tr>
 </tbody>
</table>