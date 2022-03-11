---
description: Para evitar a integração acidental de arquivos e dados em fontes de dados de destino pertencentes a outros parceiros ou clientes, o Audience Manager adicionou um requisito de mapeamento entre a ID do parceiro (PID) e as fontes de dados de outros parceiros.
title: Gerenciar acesso de integração para dados de terceiros
source-git-commit: 6c88979f876909bc32b5238605cb4a352e327a00
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# Gerenciar acesso de integração para dados de terceiros {#manage-onboarding-access-for-second-party-data}

Para evitar a integração acidental de arquivos e dados em fontes de dados de destino pertencentes a outros parceiros, o Audience Manager adicionou um requisito de mapeamento entre a ID do parceiro (PID) e as fontes de dados (DPID) de propriedade de outros parceiros. Leia mais sobre PID e DPID no [índice de IDs de Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html).

Para fins de compartilhamento de dados de terceiros, se um parceiro de Audience Manager ou cliente quiser assimilar arquivos em uma fonte de dados de destino que não possui, será necessário solicitar um mapeamento entre a ID do parceiro (PID) e a fonte de dados específica (DPID). Se o mapeamento estiver ausente, os arquivos não serão processados pelo trabalho de dados de entrada e os dados não serão incorporados ao Audience Manager.

Para criar esse mapeamento, envie um tíquete Jira para a equipe de engenharia do Audience Manager. Exibir um exemplo de tíquete Jira [here](https://jira.corp.adobe.com/browse/AAM-60353). Não é necessário solicitar a criação de mapeamentos para qualquer relacionamento de compartilhamento de dados existente.
