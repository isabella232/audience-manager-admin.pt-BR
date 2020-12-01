---
description: Alguns clientes talvez não queiram fornecer seu acesso ao Serviço de Armazenamento Simples da Amazon (Amazon S3) ou chaves secretas ao Adobe para autorizar o carregamento de dados de destino para seus buckets.
seo-description: Alguns clientes talvez não queiram fornecer seu acesso ao Serviço de Armazenamento Simples da Amazon (Amazon S3) ou chaves secretas ao Adobe para autorizar o carregamento de dados de destino para seus buckets.
seo-title: Como autorizar o acesso entre contas do bucket Amazon S3 para destinos de lote
title: Como autorizar o acesso entre contas do bucket Amazon S3 para destinos de lote
uuid: da2bcbda-a765-437a-bfe9-4355383a4730
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---


# Como autorizar o acesso entre contas do bucket Amazon S3 para destinos de lote{#authorize-cross-account-bucket-batch}

Alguns clientes talvez não queiram fornecer seu acesso [!DNL Amazon S3] ou chaves secretas ao Adobe para autorizar o carregamento de dados de destino para seus compartimentos.

Uma alternativa que podemos oferta nossos clientes é [!UICONTROL Cross-Account Bucket Permissions] em [!DNL Amazon S3]. Esse processo é descrito na documentação [AWS](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html). Para ativar essa alternativa no Audience Manager, siga as etapas abaixo:

1. Vá para **[!UICONTROL Servers]** e selecione **[!UICONTROL Create Server]**.
1. Selecione **[!UICONTROL S3]** na máscara suspensa **[!UICONTROL Protocol/Credentials]**.
1. Verifique a opção **[!UICONTROL Use Internal Adobe Key]**.
1. Use a conta do cliente e o nome do bucket em [!DNL Amazon S3].
1. Certifique-se de que sua conta [!DNL Amazon S3] branca do cliente lista a `975822914085` em seu bucket [!DNL S3].

>[!NOTE]
>
>Nosso editor externo garante que o nível de permissão `bucket-owner-full-control` seja definido nos dados carregados, para que o cliente possa ser o proprietário desses dados.
