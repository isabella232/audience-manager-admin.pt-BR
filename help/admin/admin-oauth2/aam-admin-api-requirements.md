---
description: O que você deve incentivar seus clientes a ficarem cientes quando estiverem trabalhando com as APIs do Audience Manager.
seo-description: Things you should encourage your clients to be aware of when they're working with the Audience Manager APIs.
seo-title: API Requirements and Recommendations
title: Requisitos da API e recomendações
uuid: eba9cf92-f0c8-4394-8532-0de9a2e7b103
exl-id: 24f90732-31a6-436d-862b-e6871d279c7a
source-git-commit: c7c5da62b32f6a56152e1c09a965facfc601cade
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 2%

---

# Requisitos da API e recomendações {#api-requirements-and-recommendations}

O que você deve incentivar seus clientes a estarem cientes quando estiverem trabalhando com o Audience Manager [!DNL API]s.

## Requisitos {#requirements}

Observe o seguinte ao trabalhar com o código [!DNL Audience Manager] [!DNL API]:

* **Parâmetros da solicitação:** todos os parâmetros da solicitação são obrigatórios, a menos que especificado de outra forma.
* **[!DNL JSON]tipo de conteúdo:** especifique  `content-type: application/json` ** `accept: application/json` e no seu código.

* **Solicitações e respostas:** envia solicitações como um  [!DNL JSON] objeto formatado corretamente. [!DNL Audience Manager] responde com dados  [!DNL JSON] formatados. As respostas do servidor podem conter dados solicitados, um código de status ou ambos.

* **Acesso:** seu  [!DNL Audience Manager] consultor fornecerá uma ID de cliente e uma chave que permitem fazer  [!DNL API] solicitações.

* **Documentação e exemplos de código:** o texto em  ** itálico representa uma variável que você fornece ou transmite ao criar ou receber  [!DNL API] dados. Substitua o texto *em itálico* por seu próprio código, parâmetros ou outras informações necessárias.

## Recommendations: Criar um usuário de API genérico {#recommendations}

Recomendamos criar uma conta de usuário técnica e separada para trabalhar com o Audience Manager [!DNL API]s. Esta é uma conta genérica que não está vinculada ou associada a um usuário específico na organização do cliente. Esse tipo de conta de usuário [!DNL API] ajuda a realizar duas coisas:

* Identifique qual serviço está chamando o [!DNL API] (por exemplo, chamadas de um aplicativo cliente que usam nossos [!DNL API]s ou de fazer alterações em massa).
* Forneça acesso ininterrupto aos [!DNL API]s. Uma conta vinculada a um funcionário específico pode ser excluída quando ele deixa a empresa. Isso impedirá que seus clientes trabalhem com o código [!DNL API] disponível. Uma conta genérica não vinculada a um funcionário específico ajuda a evitar esse problema.

Como exemplo ou caso de uso para esse tipo de conta, considere que seus clientes desejam alterar muitos segmentos ao mesmo tempo com as [Ferramentas de gerenciamento em massa](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/bulk-management-tools/bulk-management-intro.html?lang=en). Para fazer isso, eles precisam de acesso [!DNL API]. Em vez de adicionar permissões a um usuário específico, crie uma conta de usuário [!DNL API] não específica que tenha as credenciais, a chave e o segredo apropriados para fazer chamadas [!DNL API]. Isso também é útil se o cliente desenvolver seus próprios aplicativos que usam o [!DNL Audience Manager] [!DNL API]s.
