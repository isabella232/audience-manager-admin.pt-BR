---
description: É possível que alguns clientes não queiram fornecer acesso ao Amazon Simple Storage Service (Amazon S3) ou chaves secretas para o Adobe para autorizar o upload de dados de destino para seus buckets.
seo-description: Some customers may not want to provide their Amazon Simple Storage Service (Amazon S3) access or secret keys to Adobe to authorize destination data upload to their buckets.
seo-title: How To  Authorize Cross-Account Amazon S3 Bucket Access for Batch Destinations
title: Como autorizar acesso ao bucket do Amazon S3 entre contas para destinos em lote
uuid: da2bcbda-a765-437a-bfe9-4355383a4730
exl-id: f3b97c31-714f-4841-884b-bc507267a932
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# Como autorizar acesso ao bucket do Amazon S3 entre contas para destinos em lote{#authorize-cross-account-bucket-batch}

Alguns clientes podem não querer fornecer seus [!DNL Amazon S3] acesse ou guarde chaves secretas para o Adobe para autorizar o upload de dados de destino para seus buckets.

Uma alternativa que podemos oferecer aos nossos clientes é [!UICONTROL Cross-Account Bucket Permissions] in [!DNL Amazon S3]. Esse processo é descrito na seção [Documentação do AWS](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html). Para ativar essa alternativa no Audience Manager, siga as etapas abaixo:

1. Ir para **[!UICONTROL Servers]** e selecione **[!UICONTROL Create Server]**.
1. Selecionar **[!UICONTROL S3]** no **[!UICONTROL Protocol/Credentials]** máscara suspensa.
1. Verifique a **[!UICONTROL Use Internal Adobe Key]** opção.
1. Use a conta e o nome do período do cliente no [!DNL Amazon S3].
1. Certifique-se de que o cliente liste as [!DNL Amazon S3] account `975822914085` em seu [!DNL S3] balde.

>[!NOTE]
>
>Nosso editor de saída garante que o nível de permissão `bucket-owner-full-control` O está configurado nos dados carregados, para que o cliente possa ser o proprietário desses dados.
