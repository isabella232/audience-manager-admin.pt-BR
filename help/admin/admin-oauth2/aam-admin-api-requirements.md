---
description: As coisas que você deve incentivar seus clientes a saber quando estão trabalhando com as apis do Audience Manager.
seo-description: As coisas que você deve incentivar seus clientes a saber quando estão trabalhando com as apis do Audience Manager.
seo-title: Requisitos de API e Recomendações
title: Requisitos de API e Recomendações
uuid: eba 9 cf 92-f 0 c 8-4394-8532-0 de 9 a 2 e 7 b 103
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# Requisitos de API e Recomendações {#api-requirements-and-recommendations}

As coisas que você deve incentivar seus clientes a conhecerem quando estão trabalhando com o Audience Manager [!DNL API]s.

## Exigências {#requirements}

Observe o seguinte ao trabalhar com [!DNL Audience Manager][!DNL API] código:

* **Solicitar parâmetros:** Todos os parâmetros de solicitação são necessários, a menos que especificados caso contrário.
* **[!DNL JSON]tipo de conteúdo:** Especifique `content-type: application/json`*e* `accept: application/json` no código.

* **Solicitações e respostas:** Envie solicitações como um objeto formatado [!DNL JSON] corretamente. [!DNL Audience Manager] responde com [!DNL JSON] dados formatados. As respostas do servidor podem conter dados solicitados, um código de status ou ambos.

* **Acesso:** Seu [!DNL Audience Manager] consultor fornecerá uma ID de cliente e uma chave que permitem [!DNL API] fazer solicitações.

* **Documentação e amostras de código:** O texto em *itálico* representa uma variável que você fornece ou passa ao fazer ou receber [!DNL API] dados. Substitua *o texto em itálico* por seu próprio código, parâmetros ou outras informações necessárias.

## Recomendações: Criar um usuário de API genérico {#recommendations}

Recomendamos criar uma conta de usuário técnica separada para trabalhar com o Audience Manager [!DNL API]s. Esta é uma conta genérica que não está vinculada ou associada a um usuário específico na organização do cliente. Esse tipo de [!DNL API] conta de usuário ajuda a atingir 2 coisas:

* Identifique o serviço que está chamando o [!DNL API] (por exemplo, chamadas de um aplicativo cliente que usa nossos [!DNL API]s ou de fazer alterações em massa).
* Fornece acesso ininterrupto à [!DNL API]s. Uma conta vinculada a um funcionário específico pode ser excluída quando eles saem da empresa. Isso impedirá que seus clientes trabalhem com [!DNL API] o código disponível. Uma conta genérica que não está vinculada a um determinado funcionário ajuda a evitar esse problema.

Como exemplo ou caso de uso para esse tipo de conta, digamos que seus clientes queiram alterar muitos segmentos de uma vez com as Ferramentas de gerenciamento [em massa](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/bult-management-tools/bulk-management-intro.html). Para fazer isso, eles precisam [!DNL API] de acesso. Em vez de adicionar permissões a um usuário específico, crie uma conta [!DNL API] de usuário não específica, que tenha as credenciais, a chave e o segredo apropriados para fazer [!DNL API] chamadas. Isso também é útil se o cliente desenvolver seus próprios aplicativos que usam s [!DNL Audience Manager][!DNL API].
