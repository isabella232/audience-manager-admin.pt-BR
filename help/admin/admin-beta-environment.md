---
description: O ambiente beta é para testar implementações do Audience Manager. As alterações feitas em beta não afetam os dados de produção. O ambiente beta do Audience Manager é uma versão em menor escala e independente do ambiente de produção. Todos os dados que você deseja testar devem ser inseridos e coletados neste ambiente.
seo-description: O ambiente beta é para testar implementações do Audience Manager. As alterações feitas em beta não afetam os dados de produção. O ambiente beta do Audience Manager é uma versão em menor escala e independente do ambiente de produção. Todos os dados que você deseja testar devem ser inseridos e coletados neste ambiente.
seo-title: Ambiente beta
solution: Audience Manager
title: Ambiente beta
uuid: 6 a 253 f 4 e -96 e 7-4395-a 783-a 8 eb 213 b 7 daf
translation-type: tm+mt
source-git-commit: 7765dbf79c2fb6ca8c4b52fe8090c1fd11f9db27

---


# Ambiente beta {#beta-environment}

O ambiente beta é para testar implementações do Audience Manager. As alterações feitas em beta não afetam os dados de produção. O ambiente beta do Audience Manager é uma versão em menor escala e independente do ambiente de produção. Todos os dados que você deseja testar devem ser inseridos e coletados neste ambiente.

## Visão geral {#overview}

<!-- beta_environment_admin.xml -->

| Serviço | URL/Nome do host | Etapas para a provisão |
|--- |--- |--- |
| S3 |  | Consulte [Provisionamento de buckets do Amazon S 3](admin-beta-environment.md#provision-s3-buckets). |
| DCS | https &amp; amp; dois pontos; // dcs-beta.demdex.net/.. | Nenhuma etapa extra necessária em nosso lado. Consulte [Acessar o DCS no ambiente beta](admin-beta-environment.md#access-dcs-beta-environment). |
| Interface do usuário | https &amp; amp; dois pontos; //bank-beta.demdex.com | Os dados são copiados da produção para o ambiente beta mensalmente. As credenciais de produção são válidas para beta. |
| API | https &amp; amp; dois pontos; // api-beta.demdex.com/.. | Os dados são copiados da produção para o ambiente beta mensalmente. As credenciais de produção são válidas para beta. |

## Provisão de buckets da Amazon S 3 {#provision-s3-buckets}

>[!NOTE]
>
>Estamos afastando de usar [!DNL FTP/SFTP]. Além disso, observe que as transferências de dados de saída não funcionam para o ambiente beta.

Para incluir [!DNL S3] grupos de dados de entrada:

1. Use o recurso [**de Ajuda**](https://skms.adobe.com/) techops da solicitação de SKMS.
1. Vá para **[!UICONTROL Request TechOps Help]** o painel de navegação esquerdo.
1. No **[!UICONTROL Request Search]**, digite no Audience Manager no campo de pesquisa.
1. Role para baixo nos resultados da pesquisa e clique em no **Audience Manager - Provisionamento de conta de entrada/saída S 3**.
1. Preencha os campos na janela de provisionamento e especifique **o ambiente Sandbox** no **[!UICONTROL Environment]** campo.

>[!NOTE]
>
>Desencorajamos o uso [!DNL FTP/SFTP] de e incentive o uso [!UICONTROL Amazon S3]de. Os motivos pelos quais recomendamos o uso [!UICONTROL Amazon S3] de estão listados no [Amazon S 3: Sobre](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/amazon-s3.html).

## Acesse o DCS no ambiente beta {#access-dcs-beta-environment}

Para acessar o [!UICONTROL DCS] ambiente beta:

1. [!UICONTROL DCS] Faça uma chamada usando o [!DNL curl][comando](https://curl.haxx.se/docs/manpage.html). [!DNL Curl] é uma ferramenta para transferir dados de ou para um servidor, usando um de muitos protocolos suportados.

   Por exemplo: `curl -v https://dcs-beta.demdex.net/event`

1. Verifique se a solicitação foi fornecida pelo beta [!UICONTROL DCS] procurando por "[!DNL sandbox]no cabeçalho [!UICONTROL DCS] de resposta.

   Por exemplo:

   ```
   curl -v http://dcs-beta.demdex.net/?event
   [...]
   < DCS: va6-sandbox-dcs-3.sandbox.demdex.com <release_number>
   [...]
   ```

<!--
1. Determine the load balancer's endpoint IP addresses.

   Run the `dig` [command](https://en.wikipedia.org/wiki/Dig_(command)) to determine the IP address of the nearest load balancer. The `dig` command queries the Domain Name System and returns the name and IP addresses of the Audience Manager [!UICONTROL Data Collection Servers (DCS)].

   ```
   dig dcs-beta.demdex.net
   ...
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 52.87.15.51
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 50.16.150.8
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 52.2.228.100
   ```

1. Using one of the addresses in the above table, add a static DNS entry in the [!DNL `/etc/hosts`] file.

   On Windows, modify [!DNL `c:\WINDOWS\system32\drivers\etc\hosts`].

   For example:

[!DNL `52.87.15.51 samplepartner.demdex.net`]

   >[!NOTE]
   >
   >The addresses change occasionally, so you must keep your [!DNL /etc/hosts] file up to date.

   Additionally, if you need to set up ID synchronization, you must add a similar entry for [!DNL dpm.demdex.net.]

[!DNL `52.87.15.51 dpm.demdex.net`] [!DNL]. 

1. Make a [!UICONTROL DCS] call, using the `curl` [command](https://curl.haxx.se/docs/manpage.html). Curl is a tool to transfer data from or to a server, using one of many supported protocols.

   For example:

[!DNL `https://<domain>/event?product=camera`] 

1. Verify that your request was served by the beta [!UICONTROL DCS] by looking for "sandbox" in the [!UICONTROL DCS] response header.

   For example:

   ```
   curl -v https://dcs-beta.demdex.net/?event
   [...]
   < DCS: va6-sandbox-dcs-3.sandbox.demdex.com <release_number>
   [...]
   ```
-->