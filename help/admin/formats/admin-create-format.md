---
description: Use a página Formatos na ferramenta Admin do Audience Manager para criar um novo formato ou editar um formato existente.
seo-description: Use a página Formatos na ferramenta Admin do Audience Manager para criar um novo formato ou editar um formato existente.
seo-title: Criar ou editar um formato
title: Criar ou editar um formato
uuid: ca 1 b 1 feb-bcd 3-4 a 41-b 1 e 8-80565 f 6 c 23 ae
translation-type: tm+mt
source-git-commit: 71bf4cec222428686c1eab0998f66887db06da68

---


# Criar ou editar um formato {#create-or-edit-a-format}

Use [!UICONTROL Formats] a página na ferramenta de administração do Audience Manager para criar um novo formato ou editar um formato existente.

<!-- t_create_format.xml -->

>[!TIP]
>
>Ao selecionar um formato para seus dados delimitados, é melhor, se possível, reutilizar um formato existente. O uso de um formato já comprovado garante que seus dados de saída sejam gerados com sucesso. Para ver exatamente como um formato existente é formatado, clique na [!UICONTROL Formats] opção na barra de menus e procure seu formato por nome ou número de ID. Formatos malformados ou macros usados em formatos fornecerão uma saída formatada incorretamente ou impedirá a saída total das informações.

1. Para criar um novo formato, clique **[!UICONTROL Formats]** em &gt; **[!UICONTROL Add Format]**. Para editar um formato existente, clique no formato desejado na **[!UICONTROL Name]** coluna.

   ![](assets/create_format.png)

1. Preencha os campos:
   * **Nome:** (Obrigatório) Forneça um nome descritivo para o formato.
   * **Tipo:** (Obrigatório) Selecione o formato desejado:
      * **[!UICONTROL File]**: Envia dados por [!DNL FTP] arquivos.
      * **[!UICONTROL HTTP]**: Engloba os dados em [!DNL JSON] um vínculo.

1. (Condicional) Se você escolher **[!UICONTROL File]**, preencha os campos:

   >[!NOTE]
   >
   >Para obter uma lista de macros disponíveis, consulte [Formato de arquivo Macros](../formats/file-formats.md#concept_A867101505074418A58DE325949E5089) e [Macros de formato HTTP](../formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE).

   * **[!UICONTROL File Name]:** Especifique o nome do arquivo para o arquivo de transferência de dados.
   * **Cabeçalho:** Especifique o texto que aparece na primeira linha do arquivo de transferência de dados.
   * **[!UICONTROL Data Row]:** Especifique o texto que aparece em cada linha excedente do arquivo.
   * **[!UICONTROL Maximum File Size (In MB)]:** Especifique o tamanho máximo de arquivo para arquivos de transferência de dados. Arquivos compactados devem ser menores que 100 MB. Não há limite de tamanho de arquivo descompactado.
   * **[!UICONTROL Compression]:** Selecione o tipo de compactação desejado: gz ou zip para seus arquivos de dados. Para entrega, [!UICONTROL AWS S3]você deve usar.gz ou arquivos descompactados.
   * **[!UICONTROL .info Receipt]:** Especifica que um arquivo de controle de transferência ([!DNL .info]) é gerado. [!DNL .info] O arquivo fornece informações de metadados sobre transferências de arquivos para que os parceiros possam verificar se o Audience Manager manipulou as transferências de arquivo corretamente. Para obter mais informações, consulte [Arquivos de controle de transferência para transferências de arquivo de log](https://marketing.adobe.com/resources/help/en_US/aam/c_s2s_add_transfer_control_files.html).
   * **[!UICONTROL MD5 Checksum Receipt]:** Especifica que um recibo [!DNL MD5] de soma de verificação é gerado. O recibo [!DNL MD5] de soma de verificação para que os parceiros possam verificar se o Audience Manager manipulou a transferência completa corretamente.

1. (Condicional) Se você escolher **[!UICONTROL HTTP]**, preencha os campos:

   * **[!UICONTROL Method]:** Escolha o [!DNL API] método que deseja usar para o processo de transferência:
      * **[!UICONTROL POST]:** Se selecionar [!DNL POST], selecione o tipo de conteúdo ([!DNL XML] ou [!DNL JSON]) e especifique o corpo da solicitação.
      * **[!UICONTROL GET]:** Se você selecionar [!DNL GET], especifique os parâmetros de consulta.

1. Clique **[!UICONTROL Create]** em se estiver criando um novo formato ou clique **[!UICONTROL Save Updates]** em caso esteja editando um formato existente.

## Excluir um formato {#delete-format}

1. Clique em **[!UICONTROL Formats]**.
2. Clique ![](assets/icon_delete.png) na **[!UICONTROL Actions]** coluna do formato desejado.
3. Clique em **[!UICONTROL OK]para confirmar a exclusão.**
