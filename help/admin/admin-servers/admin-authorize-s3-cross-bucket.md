---
description: Alguns clientes podem não querer fornecer suas chaves de acesso a Amazon Simple Storage Service (Amazon S 3) ou chaves secretas para a Adobe autorizar o upload dos dados de destino em seus compartimentos.
seo-description: Alguns clientes podem não querer fornecer suas chaves de acesso a Amazon Simple Storage Service (Amazon S 3) ou chaves secretas para a Adobe autorizar o upload dos dados de destino em seus compartimentos.
seo-title: Como autorizar o acesso a bucket da Amazon S 3 de conta cruzada para destinos em lote
title: Como autorizar o acesso a bucket da Amazon S 3 de conta cruzada para destinos em lote
uuid: da 2 bcbda-a 765-437 a-bfe 9-4355383 a 4730
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# Como autorizar o acesso a bucket da Amazon S 3 de conta cruzada para destinos em lote{#authorize-cross-account-bucket-batch}

Alguns clientes podem não querer fornecer suas chaves [!DNL Amazon S3] de acesso ou segredo à Adobe para autorizar o upload dos dados de destino em seus compartimentos.

Uma alternativa que podemos oferecer [!UICONTROL Cross-Account Bucket Permissions] aos nossos clientes [!DNL Amazon S3]. Esse processo é descrito na documentação [AWS](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html). Para habilitar essa alternativa no Audience Manager, siga as etapas abaixo:

1. Ir para e **[!UICONTROL Servers]** selecionar **[!UICONTROL Create Server]**.
1. Selecione **[!UICONTROL S3]** na máscara **[!UICONTROL Protocol/Credentials]** suspensa.
1. Verifique a **[!UICONTROL Use Internal Adobe Key]** opção.
1. Use a conta do cliente e o nome do bucket em [!DNL Amazon S3].
1. Certifique-se de que o branco do cliente lista a [!DNL Amazon S3] conta `975822914085` no [!DNL S3] bucket.

>[!NOTE]
>
>Nosso editor de saída garante que o nível `bucket-owner-full-control` de permissão seja definido nos dados carregados para que o cliente possa ter esses dados.
