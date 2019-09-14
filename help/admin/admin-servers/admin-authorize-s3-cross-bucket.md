---
description: Alguns clientes talvez não queiram fornecer acesso ao Amazon Simple Storage Service (Amazon S3) ou chaves secretas à Adobe para autorizar o carregamento de dados de destino para seus baldes.
seo-description: Alguns clientes talvez não queiram fornecer acesso ao Amazon Simple Storage Service (Amazon S3) ou chaves secretas à Adobe para autorizar o carregamento de dados de destino para seus baldes.
seo-title: Como autorizar o acesso entre contas do bucket Amazon S3 para destinos de lote
title: Como autorizar o acesso entre contas do bucket Amazon S3 para destinos de lote
uuid: da2bcbda-a765-437a-bfe9-4355383a4730
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# Como autorizar o acesso entre contas do bucket Amazon S3 para destinos de lote{#authorize-cross-account-bucket-batch}

Alguns clientes talvez não queiram fornecer seu [!DNL Amazon S3] acesso ou chaves secretas para a Adobe autorizar o carregamento de dados de destino para seus compartimentos.

Uma alternativa que podemos oferecer aos nossos clientes está [!UICONTROL Cross-Account Bucket Permissions] em [!DNL Amazon S3]. Esse processo é descrito na documentação [do](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html)AWS. Para ativar essa alternativa no Audience Manager, siga as etapas abaixo:

1. Vá para **[!UICONTROL Servers]** e selecione **[!UICONTROL Create Server]**.
1. Selecione **[!UICONTROL S3]** na máscara **[!UICONTROL Protocol/Credentials]** suspensa.
1. Marque a **[!UICONTROL Use Internal Adobe Key]** opção.
1. Use a conta do cliente e o nome do bucket em [!DNL Amazon S3].
1. Certifique-se de que seu cliente liste a [!DNL Amazon S3] conta `975822914085` em branco no [!DNL S3] bucket.

>[!NOTE]
>
>Nosso editor externo garante que o nível de permissão `bucket-owner-full-control` seja definido nos dados carregados, para que o cliente possa ser o proprietário desses dados.
