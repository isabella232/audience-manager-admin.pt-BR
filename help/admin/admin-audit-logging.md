---
description: 'Use o Registro de auditoria como o primeiro lugar a ser acessado ao depurar problemas do cliente. '
seo-description: 'Use o Registro de auditoria como o primeiro lugar a ser acessado ao depurar problemas do cliente. '
seo-title: Registro de auditoria
title: Registro de auditoria
uuid: null
translation-type: tm+mt
source-git-commit: 190ba5c1215782e46c8e544c10679d451fbed134

---


# Registro de auditoria {#audit-logging}

Use [!UICONTROL  Audit Logging] como o primeiro local para solucionar problemas do cliente.

> [!NOTE]
>
>[!UICONTROL Audit Logging] está atualmente em desenvolvimento e sujeita a alterações. Registre todos os problemas encontrados [!DNL JIRA] ([!DNL UI] equipe)

![Exibição de registro de auditoria](assets/audit-logging-img.png)

No seletor suspenso Tipo **de** auditoria, escolha entre:

* [!UICONTROL Partner]
* [!UICONTROL User]
* [!UICONTROL Group]
* [!UICONTROL Datasource Summary]
* [!UICONTROL General Datasource]
* [!UICONTROL Merge Rule Datasource]
* [!UICONTROL Data Feed]
* [!UICONTROL Data Feed Subscription]
* [!UICONTROL Trait Summary]
* [!UICONTROL Trait Rule]
* [!UICONTROL Segment Summary]
* [!UICONTROL Destination Summary]
* [!UICONTROL Server to Server Destination]
* [!UICONTROL Derived Signal]
* [!UICONTROL Model]
* [!UICONTROL Segment Test Group]

A ID **do** objeto é a ID do item que você está pesquisando. Consulte a tabela abaixo para saber qual ID corresponde à ID do objeto em cada caso:

| Tipo de auditoria | ID do objeto |
---------|----------|
| [!UICONTROL Partner] | ID do parceiro - PID |
| [!UICONTROL User] | ID de usuário |
| [!UICONTROL Group] | B3 |
| [!UICONTROL Datasource Summary] | ID da fonte de dados |
| [!UICONTROL General Datasource] | ID da fonte de dados |
| [!UICONTROL Merge Rule Datasource] | ID da fonte de dados |
| [!UICONTROL Data Feed] | ID do feed de dados |
| [!UICONTROL Data Feed Subscription] | ID do feed de dados |
| [!UICONTROL Trait Summary] | SID (característica) |
| [!UICONTROL Trait Rule] | SID (característica) |
| [!UICONTROL Segment Summary] |  |
| [!UICONTROL Destination Summary] |  |
| [!UICONTROL Server-to-Server Destination] | N/A |
| [!UICONTROL Derived Signal] | N/A |
| [!UICONTROL Model] | N/A |
| [!UICONTROL Segment Test Group] | N/A |

Use [!UICONTROL Start Date] ([!DNL UTC]) e [!UICONTROL End Date] ([!DNL UTC]) para restringir o intervalo de tempo dos registros.