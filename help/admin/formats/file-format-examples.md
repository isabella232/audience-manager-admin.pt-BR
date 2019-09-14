---
description: Exemplos de como as macros são usadas para criar modelos de arquivos FTP externos.
seo-description: Exemplos de como as macros são usadas para criar modelos de arquivos FTP externos.
seo-title: Exemplos de Macro de Formato de Arquivo
title: Exemplos de Macro de Formato de Arquivo
uuid: f00d431d-7e43-457a-b633-c79cbc4c8f10
translation-type: tm+mt
source-git-commit: 4c6d1752ff10d2d3d12cab88e823f25f5ef4fcd0

---


# Exemplos de Macro de Formato de Arquivo {#file-format-macro-examples}

Exemplos de como as macros são usadas para criar modelos de arquivos externos [!DNL FTP] .

>[!NOTE]
>
>Nas tabelas, o tipo **em negrito** identifica cada macro com sua saída relacionada. Para os exemplos de formato, os &lt; &gt; símbolos foram adicionados para ajudar a separar visualmente cada macro.

## Macros comuns {#common-macros}

Essas macros podem ser usadas em qualquer campo de formato. Consulte Macros [de formato de](../formats/file-formats.md) arquivo para obter uma lista completa e definições.

<table id="table_B5073597219B470298EE614902DACAE8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Macro </th> 
   <th colname="col2" class="entry"> Exemplos de formato e saída </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>DPID </code> </p> </td> 
   <td colname="col2"> <p> Formato: <code>&lt;SYNC_TYPE&gt;_&lt;ORDER_ID&gt;_ &lt;DPID&gt;_&lt;SYNC_MODE&gt;_&lt;TIMESTAMP&gt;.sync </code> </p> <p>Saída: <code>ftp_215_ 888_iter_1449756724.sync </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MASTER_DPID </code> </p> </td> 
   <td colname="col2"> <p> Formato: <code>&lt;SYNC_TYPE&gt;_&lt;ORDER_ID&gt;_&lt;DPID&gt;_ &lt;MASTER_DPID&gt;_&lt;SYNC_MODE&gt;_&lt;TIMESTAMP&gt;.sync </code> </p> <p>Saída: <code>ftp_215_888_ 20915_iter_1449756724.sync </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ORDER_ID </code> </p> </td> 
   <td colname="col2"> <p> Formato: <code>&lt;SYNC_TYPE&gt;_ &lt;ORDER_ID&gt;_&lt;DPID&gt;_&lt;SYNC_MODE&gt;_&lt;TIMESTAMP&gt;.sync </code> </p> <p>Saída: <code>ftp_ 215_888_iter_1449756724.sync </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_MODE </code> </p> </td> 
   <td colname="col2"> <p> Formato: <code>&lt;SYNC_TYPE&gt;_&lt;ORDER_ID&gt;_&lt;DPID&gt;_ &lt;SYNC_MODE&gt;_&lt;TIMESTAMP&gt;.sync </code> </p> <p>Saída: 
     <ul id="ul_F63D7B78AF1246639D6ED85C1621B17C"> 
      <li id="li_4D0D7B4D047345FE861FCBA2BD0408ED">Total: <code>ftp_215_888_ full_1449756724.sync </code> </li> 
      <li id="li_23F4D1F6B2784E599EDA29AA457327E6">Incremental: <code>ftp_215_888_ iter_1449756724.sync </code> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_TYPE </code> </p> </td> 
   <td colname="col2"> <p> Formato: <code>&lt;SYNC_TYPE&gt;_&lt;ORDER_ID&gt;_&lt;DPID&gt;_&lt;SYNC_MODE&gt;_&lt;TIMESTAMP&gt;.sync </code> </p> <p>Saída: 
     <ul id="ul_11B14E740E40474F8302BDB809C428FE"> 
      <li id="li_54A3EAA468B44AC8B2528F855E03D04B">FTP: <code>ftp_215_888_iter_1449756724.sync </code> </li> 
      <li id="li_93468C56B661463CA7F62B1F5D3A53FF">https: <code>http_215_888_iter_1449756724.sync </code> </li> 
      <li id="li_8A204C7BEDBC41C096FE953B5F827DEC">S3: <code>s3_215_888_iter_1449756724.sync </code> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>CARIMBO DE DATA E HORA </code> </p> </td> 
   <td colname="col2"> <p> Formato: <code>&lt;SYNC_TYPE&gt;_&lt;ORDER_ID&gt;_&lt;DPID&gt;_&lt;SYNC_MODE&gt;_ &lt;TIMESTAMP&gt;.sync </code> </p> <p>Saída: <code>ftp_215_888_iter_ 1449756724.sync </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Macros de campo de cabeçalho {#header-field-macros}

Macros usadas somente em campos de cabeçalho. Consulte Macros [de formato de](../formats/file-formats.md) arquivo para obter uma lista completa e definições.

<table id="table_ABC31B3D660D47969E111EBC734D5BBC"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Macro </th> 
   <th colname="col2" class="entry"> Exemplos de formato e saída </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>GUIA </code> </p> </td> 
   <td colname="col2"> <p> Formato: <code>&lt;ORDER_ID&gt; &lt;TAB&gt;&lt;SYNC_TYPE&gt; </code> </p> <p>Saída: full.sync <code>888 </code> </p> <p>Na saída, o caractere de guia não imprimível separa cada elemento. </p> </td>
  </tr>
 </tbody>
</table>

## Macros de linha de dados {#data-row-macros}

Macros usadas somente em campos de cabeçalho. Consulte Macros [de formato de](../formats/file-formats.md) arquivo para obter uma lista completa e definições.

<table id="table_408C6DD2B9D54550B003EAC93562E64F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Macro </th> 
   <th colname="col2" class="entry"> Exemplos de formato e saída </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID </code> </p> </td> 
   <td colname="col2"> <p> Formato: <code>&lt;DP_UUID&gt;&lt;TAB&gt;&lt;DP_UUID_LIST;separador=TAB&gt; </code> </p> <p>Saída: UUID1 UUID2 UUID <code>123456 UID3 </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID_LIST </code> </p> </td> 
   <td colname="col2"> <p> Formato: <code>&lt;DP_UUID&gt;&lt;TAB&gt; &lt;DP_UUID_LIST;separator=TAB&gt; </code> </p> <p>Saída: UUID1 UUID2 UUID <code>123456 UID3 </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SEGMENT_LIST &amp;&amp; REMOVED_SEGMENT_LIST </code> </p> </td> 
   <td colname="col2"> <p>Este exemplo cria um formato que retorna segmentos removidos em um feed de servidor para servidor. </p> <p> 
     <code>
       {"AdvertiserId":"&lt;PIDALIAS&gt;", "DataCenterId": 2,"TDID":"&lt;DP_UID&gt;", "Dados":[&lt;SEGMENT_LIST:{seg|&lt;OPEN_CURLY_BRACKET&gt;"Nome":"&lt;s.alias&gt;"&lt;CLOSE_CURLY_BRACKET&gt;}; 
      separator=","&gt;&lt;if(SEGMENT_LIST &amp;&amp; REMOVED_SEGMENT_LIST)&gt;&lt;COMMA&gt;&lt;endif&gt; &lt;REMOVED_SEGMENT_LIST:{seg|&lt;OPEN_CURLY_BRACKET&gt;"Nome":"&lt;seg.alias&gt;", "TtlInMinutos":0&lt;CLOSE_CURLY_BRACKET&gt;}; separator=","&gt;]} </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SEGMENT_LIST </code> </p> </td> 
   <td colname="col2"> <p> Formato: <code>&lt;DP_UUID&gt; &lt;SEGMENT_LIST&gt;;separador=" "&gt; </code> </p> <p>Saída: <code>123456 105955 101183 101180 101179 </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SET_ATTRIBUTES </code> </p> </td> 
   <td colname="col2"> <p> Formato: <code>&lt;PID&gt;&lt;TAB&gt;&lt;UUID&gt;&lt;TAB&gt;&lt;DP_UUID&gt;&lt;TAB&gt; &lt;SET_ATTRIBUTES&gt;&lt;TAB&gt;&lt;OPT_OUT&gt;&lt;TAB&gt;&lt;SEGMENT_LIST:{seg|&lt;seg.type&gt;,&lt;seg.alias&gt;,&lt;OUTPUT_ATTRIBUTE_VALUE&gt;,&lt;seg.lastUpdateTime&gt;&amp;} </code> </p> <p>Saída: <code>1159 00088008579683653741516297509717335000 17t0aj01b122 0hp 1 0 5,103714,1,1344114661000&amp;5,103713,1,1343250661000 </code> </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p> <code>GUIA </code> </p> </td> 
   <td colname="col2"> <p> Formato: <code>&lt;DP_UUID&gt;&lt;TAB&gt;&lt;DP_UUID_LIST;separador=TAB&gt; </code> </p> <p>Saída: UUID1 UUID2 UUID <code>123456 UID3 </code> </p> <p>Na saída, o caractere de guia não imprimível separa cada elemento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TRAIT_LIST </code> </p> </td> 
   <td colname="col2"> <p> Formato: <code>&lt;PID&gt;&lt;TAB&gt;&lt;DP_UUID&gt;&lt;TAB&gt;&lt;SET_ATTRIBUTES&gt;&lt;TAB&gt; &lt;TRAIT_LIST;separator="|"&gt; </code> </p> <p>Saída: <code>1131 12345 1 123|456|789 </code> </p> </td> 
  </tr> 
 </tbody> 
</table>
