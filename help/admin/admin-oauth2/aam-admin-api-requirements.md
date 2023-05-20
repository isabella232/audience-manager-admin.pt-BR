---
description: Aspectos que você deve incentivar seus clientes a estarem cientes quando estiverem trabalhando com as APIs do Audience Manager.
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

Aspectos que você deve incentivar seus clientes a estarem cientes quando estiverem trabalhando com o Audience Manager [!DNL API]s

## Requisitos {#requirements}

Observe o seguinte ao trabalhar com o [!DNL Audience Manager] [!DNL API] código:

* **Parâmetros de solicitação:** Todos os parâmetros de solicitação são obrigatórios, a menos que especificado de outra forma.
* **[!DNL JSON]tipo de conteúdo:** Especificar `content-type: application/json` *e* `accept: application/json` em seu código.

* **Solicitações e respostas:** Enviar solicitações como um formulário corretamente formatado [!DNL JSON] objeto. [!DNL Audience Manager] responde com [!DNL JSON] dados formatados. As respostas do servidor podem conter dados solicitados, um código de status ou ambos.

* **Acesso:** Seu [!DNL Audience Manager] consultor fornecerá uma ID do cliente e uma chave que permitirá que você faça [!DNL API] solicitações.

* **Documentação e amostras de código:** Texto em *itálico* representa uma variável que você fornece ou transmite ao criar ou receber [!DNL API] dados. Substituir *itálico* texto com seu próprio código, parâmetros ou outras informações necessárias.

## Recommendations: criar um usuário da API genérica {#recommendations}

Recomendamos criar uma conta de usuário técnica separada para trabalhar com o Audience Manager [!DNL API]s. Esta é uma conta genérica que não está vinculada a ou associada a um usuário específico na organização do cliente. Esse tipo de [!DNL API] A conta de usuário do ajuda a realizar duas coisas:

* Identificar o serviço que está chamando o [!DNL API] (por exemplo, chamadas de um aplicativo cliente que usam nosso [!DNL API]s ou de fazer alterações em massa).
* Fornecer acesso ininterrupto à [!DNL API]s. Uma conta vinculada a um funcionário específico pode ser deletada quando ele sair da empresa. Isso impedirá que seus clientes trabalhem com os [!DNL API] código. Uma conta genérica que não esteja vinculada a um funcionário específico ajuda a evitar esse problema.

Como exemplo ou caso de uso para esse tipo de conta, considere que seus clientes desejam alterar muitos segmentos de uma só vez com o [Ferramentas de gerenciamento em massa](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/bulk-management-tools/bulk-management-intro.html?lang=en). Para fazer isso, eles precisam [!DNL API] acesso. Em vez de adicionar permissões a um usuário específico, crie um [!DNL API] conta de usuário que tenha as credenciais, a chave e o segredo apropriados para fazer [!DNL API] chamadas. Isso também é útil se os clientes desenvolverem seus próprios aplicativos que usam o [!DNL Audience Manager] [!DNL API]s
