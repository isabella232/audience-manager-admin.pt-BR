---
description: As coisas de que você deve incentivar seus clientes a estarem cientes quando estiverem trabalhando com as APIs do Audience Manager.
seo-description: As coisas de que você deve incentivar seus clientes a estarem cientes quando estiverem trabalhando com as APIs do Audience Manager.
seo-title: ' Requisitos e recomendações da API'
title: ' Requisitos e recomendações da API'
uuid: eba9cf92-f0c8-4394-8532-0de9a2e7b103
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# Requisitos e recomendações da API {#api-requirements-and-recommendations}

Coisas de que você deve incentivar seus clientes a estarem cientes quando estiverem trabalhando com os Audience Manager [!DNL API]s.

## Exigências {#requirements}

Observe o seguinte ao trabalhar com [!DNL Audience Manager] [!DNL API] código:

* **** Parâmetros de solicitação: Todos os parâmetros de solicitação são necessários, a menos que especificado de outra forma.
* **[!DNL JSON]** tipo de conteúdo: Especifique `content-type: application/json` e *especifique* `accept: application/json` no seu código.

* **** Solicitações e respostas: Envie solicitações como um [!DNL JSON] objeto formatado corretamente. [!DNL Audience Manager] responde com dados [!DNL JSON] formatados. As respostas do servidor podem conter dados solicitados, um código de status ou ambos.

* **** Acesso: Seu [!DNL Audience Manager] consultor fornecerá uma ID de cliente e uma chave que permite fazer [!DNL API] solicitações.

* **** Documentação e amostras de código: O texto em *itálico* representa uma variável fornecida ou transmitida ao criar ou receber [!DNL API] dados. Substitua o texto *em itálico* por seu próprio código, parâmetros ou outras informações necessárias.

## Recomendações: Criar um usuário de API genérico {#recommendations}

Recomendamos criar uma conta de usuário técnica e separada para trabalhar com o Audience Manager [!DNL API]s. Esta é uma conta genérica que não está vinculada ou associada a um usuário específico na organização do cliente. Esse tipo de conta de [!DNL API] usuário ajuda a realizar duas coisas:

* Identifique o serviço que está chamando o [!DNL API] (por exemplo, chamadas de um aplicativo cliente que usam nossos [!DNL API]s ou fazem alterações em massa).
* Fornecer acesso ininterrupto aos [!DNL API]s. Uma conta vinculada a um funcionário específico pode ser excluída ao sair da empresa. Isso impedirá que seus clientes trabalhem com o [!DNL API] código disponível. Uma conta genérica que não está vinculada a um determinado funcionário ajuda a evitar esse problema.

Como exemplo ou caso de uso para esse tipo de conta, digamos que seus clientes queiram alterar muitos segmentos ao mesmo tempo com as Ferramentas [de Gerenciamento em](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/bult-management-tools/bulk-management-intro.html)massa. Para isso, eles precisam de [!DNL API] acesso. Em vez de adicionar permissões a um usuário específico, crie uma conta de usuário não específica, [!DNL API] que tenha as credenciais, a chave e o segredo apropriados para fazer [!DNL API] chamadas. Isso também é útil se o cliente desenvolver seus próprios aplicativos que usam os [!DNL Audience Manager] [!DNL API]s.
