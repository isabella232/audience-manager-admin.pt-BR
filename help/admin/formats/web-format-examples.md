---
description: Exemplos de algumas combinações de macro HTTP comumente usadas.
seo-description: Exemplos de algumas combinações de macro HTTP comumente usadas.
seo-title: Exemplos de macro HTTP
title: Exemplos de macro HTTP
uuid: a 81 a 2 e 2 a-de 7 e -4 b 6 a -8771-fcfa 0 dc 74570
translation-type: tm+mt
source-git-commit: 4c6d1752ff10d2d3d12cab88e823f25f5ef4fcd0

---


# Exemplos de macro HTTP {#http-format-macro-examples}

Exemplos de algumas combinações [!DNL HTTP] de macro frequentemente usadas.

Consulte Macros de formato [HTTP](../formats/web-formats.md) para obter uma lista de macros e suas definições.

<table id="table_D5FAC5D056ED49D79FA883197EF8F42E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Exemplos de macro </th> 
   <th colname="col2" class="entry"> Formato de saída </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; PID_ ALIAS &gt;|&lt; DP_ UUID &gt;|&lt; TRAITALIAS_ LIST; separator = "," &gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>pid_ alias | dp_ uuid | trait_ 1, trait_ 2</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; PID_ ALIAS &gt;| count: &lt; NUM_ USERS &gt;| usuários: [&lt; USER_ LIST: {usuário|&lt; user. aamuuid &gt;: &lt; user. dpuuid &gt;}; separator = "," &gt;]</code> </p> </td> 
   <td colname="col2"> <p> <code>" pid_ alias | count: 2 | usuários: [uuid 1: dpuuid 1, uuid 2: dpuuid 2] "</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; USER_ AGENT &gt;|&lt; IP &gt;|&lt; TIMESTAMP &gt;|&lt; RANDOM &gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>" Firefox | 255.255.255.255 | 1395758143 | 42341 "</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; USER_ LIST: {u|&lt; u. useragent &gt;|&lt; u. ip &gt;|&lt; u. timestamp &gt;|&lt; u. random &gt;}; separator = "," &gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>" Firefox | 255.255.255.255 | 1395758143 | 42341 "</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; DP_ UUIDS .1 &gt; AND &lt; DP_ UUIDS .2 &gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>dpuuid 1 AND dpuuid 2</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>usuários: [&lt; USER_ LIST: {usuário|&lt; user. dpuuids .1 &gt; AND &lt; user. dpuuids .2 &gt;}; separator = "," &gt;]</code> </p> </td> 
   <td colname="col2"> <p> <code>usuários: [dpuuid 1 AND dpuuid 2]</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>test_ known_ string = loremlipsum &amp; segid = &lt; TRAITALIAS_ LIST; separator = "," &gt; &amp; test_ dpuuid_ 1000 = &lt; DP_ UUIDS .1000 &gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>test_ known_ string = loremlipsum &amp; segid = trait_ 1, trait_ 2 &amp; test_ dpuuid_ 1000 = dpuuid_ 1000</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>test_ dpuuids = &lt; DP_ UUIDS.(DPID)&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>test_ dpuuids = dpuuid 2</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>" &lt; PID_ ALIAS &gt;|&lt; DP_ UUID &gt;|&lt; TRAITALIAS_ LIST; separator = "," &gt;|&lt; REMOVED_ TRAITALIAS_ LIST; separator = "," &gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>pid_ alias | dp_ uuid | trait_ 1, trait_ 2 | trait_ 3, trait_ 4</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 
     <code>{"Usuários": [&lt; USER_ LIST: {usuário|&lt; OPEN_ BRACKET &gt; 
 " AAM_ UUID ": " &lt; user. aamuuid &gt; ", 
 " Datapartner_ UUID ": " &lt; user. dpuuid &gt; ", 
 " Segmentos ": [&lt; user. segments: {seg|&lt; OPEN_ BRACKET &gt; "Segmento": " &lt; seg. traitalias &gt; " &lt; CLOSE_ BRACKET &gt;}; separator = "," &gt;] 
 " Removed_ Segments ": [&lt; user. removedsegments: {rseg|&lt; OPEN_ BRACKET &gt; "Segmento": " &lt; rseg. traitalias &gt; " &lt; CLOSE_ BRACKET &gt;}; separator = "," &gt;] 
 &lt; CLOSE_ BRACKET &gt;}; separator = "," &gt;]} </code>
  </p> </td> 
   <td colname="col2"> <p> 
     <code>{{ 
 " Usuários ": [ 
 {{ 
 " AAM_ UUID ": " uuid 1 ", 
 " Datapartner_ UUID ": " dpuuid 1 ", 
 " Segmentos ": [ 
 {{ 
 " Segmento ": " alias 1 " 
 }, 
 {{ 
 " Segmento ": " alias 2 " 
 }} 
 ], 
 " Removed_ Segments ": [ 
 {{ 
 " Segmento ": " alias 3 " 
 }, 
 {{ 
 " Segmento ": " alias 4 " 
 }} 
 ] 
 }} 
 ] 
 }} </code>
  </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 
     <code>{"Usuários": [&lt; USER_ LIST: {usuário|&lt; OPEN_ BRACKET &gt; 
 " AAM_ UUID ": " &lt; user. aamuuid &gt; ", 
 " Datapartner_ UUID ": " &lt; user. dpuuid &gt; ", 
 " Segmentos ": [&lt; user. segments: {seg|&lt; OPEN_ BRACKET &gt; "Segmento": " &lt; seg. traitalias &gt; "," Status ": " &lt; seg. status &gt; " &lt; CLOSE_ BRACKET &gt;}; separator = "," &gt;] 
 &lt; CLOSE_ BRACKET &gt;}; separator = "," &gt;]} </code>
  </p> </td> 
   <td colname="col2"> <p> 
     <code>{{ 
 " Usuários ": [ 
 {{ 
 " AAM_ UUID ": " uuid 1 ", 
 " Datapartner_ UUID ": " dpuuid 1 ", 
 " Segmentos ": [ 
 {{ 
 " Segmento ": " alias 1 " 
 " Status ": " 1 " 
 }, 
 {{ 
 " Segmento ": " alias 2 " 
 " Status ": " 0 " 
 }} 
 ] 
 }} 
 ] 
 }} </code>
  </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; PID_ ALIAS &gt;|&lt; DP_ UUID &gt;|&lt; SEGMENTOS: {seg|&lt; seg. traitalias &gt;}; separator =\ ",\" &gt;|&lt; REMOVED_ SEGMENTS: {seg|&lt; seg. traitalias &gt;}; separator =\ ",\" &gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>pid_ alias | dp_ uuid | trait_ 1, trait_ 2 | trait_ 3, trait_ 4</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; if (user. segments &amp; &amp; user. removedsegments) &gt; &lt; VÍRA &gt; &lt; endif &gt;</code> </p> </td> 
   <td colname="col2"> <p>Imprime uma vírgula se <code>os segmentos de campos</code> e <code>removedsegments</code> não estiverem vazios. Esse condicional pode ser usado para solicitações POST ao concatenar listas para segmentos e segmentos removidos. </p> </td> 
  </tr> 
 </tbody> 
</table>
