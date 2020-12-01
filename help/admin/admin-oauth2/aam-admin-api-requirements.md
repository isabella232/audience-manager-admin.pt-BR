---
description: As coisas que você deve incentivar seus clientes a terem em mente quando estiverem trabalhando com as APIs do Audience Manager.
seo-description: As coisas que você deve incentivar seus clientes a terem em mente quando estiverem trabalhando com as APIs do Audience Manager.
seo-title: Requisitos da API e recomendações
title: Requisitos da API e recomendações
uuid: eba9cf92-f0c8-4394-8532-0de9a2e7b103
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 3%

---


# Requisitos da API e recomendações {#api-requirements-and-recommendations}

As coisas que você deve incentivar seus clientes a terem em mente quando estiverem trabalhando com o Audience Manager [!DNL API]s.

## Requisitos {#requirements}

Observe o seguinte ao trabalhar com o código [!DNL Audience Manager] [!DNL API]:

* **Parâmetros de solicitação:** Todos os parâmetros de solicitação são obrigatórios, a menos que especificado de outra forma.
* **[!DNL JSON]tipo de conteúdo:** especifique  `content-type: application/json` ** `accept: application/json` e no seu código.

* **Solicitações e respostas:** envia solicitações como um  [!DNL JSON] objeto formatado corretamente. [!DNL Audience Manager] responde com dados  [!DNL JSON] formatados. As respostas do servidor podem conter dados solicitados, um código de status ou ambos.

* **Acesso:** seu  [!DNL Audience Manager] consultor fornecerá uma ID de cliente e uma chave que permite que você faça  [!DNL API] solicitações.

* **Documentação e exemplos de código:O** texto em  ** itálico representa uma variável que você fornece ou transmite ao fazer ou receber  [!DNL API] dados. Substitua o texto *em itálico* por seu próprio código, parâmetros ou outras informações necessárias.

## Recommendations: Criar um usuário de API genérico {#recommendations}

Recomendamos criar uma conta de usuário técnica e separada para trabalhar com o Audience Manager [!DNL API]s. Esta é uma conta genérica que não está vinculada ou associada a um usuário específico na organização do cliente. Esse tipo de conta de usuário [!DNL API] ajuda a realizar duas coisas:

* Identifique o serviço que está chamando [!DNL API] (por exemplo, chamadas de um aplicativo cliente que usam nossos [!DNL API]s ou que fazem alterações em massa).
* Forneça acesso ininterrupto aos [!DNL API]s. Uma conta vinculada a um funcionário específico pode ser excluída ao deixar a empresa. Isso impedirá que seus clientes trabalhem com o código [!DNL API] disponível. Uma conta genérica que não está vinculada a um determinado funcionário ajuda a evitar esse problema.

Como exemplo ou caso de uso para esse tipo de conta, digamos que seus clientes queiram alterar muitos segmentos ao mesmo tempo com as [Ferramentas de Gerenciamento em Massa](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/bult-management-tools/bulk-management-intro.html). Para fazer isso, eles precisam de [!DNL API] acesso. Em vez de adicionar permissões a um usuário específico, crie uma conta de usuário [!DNL API] não específica que tenha as credenciais, a chave e o segredo apropriados para fazer chamadas [!DNL API]. Isso também é útil se o cliente desenvolver seus próprios aplicativos que usam [!DNL Audience Manager] [!DNL API]s.
