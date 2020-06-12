---
description: Use a página Servidores na ferramenta Admin do Audience Manager para criar um novo servidor FTP ou editar um servidor existente.
seo-description: Use a página Servidores na ferramenta Admin do Audience Manager para criar um novo servidor FTP ou editar um servidor existente.
seo-title: Criar ou editar um servidor FTP
title: Criar ou editar um servidor FTP
uuid: 9273abb2-963d-4d83-bf5a-b3817f0b90e6
translation-type: tm+mt
source-git-commit: e0dc190f8765ec91431a2c02a62c6bf5458c7e3d
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 5%

---


# Criar ou editar um servidor FTP {#create-or-edit-an-ftp-server}

Use a [!UICONTROL Servers] página na ferramenta de administração do Audience Manager para criar um novo servidor FTP ou editar um servidor existente.

>[!NOTE]
>
>Você deve ter a [!UICONTROL DEXADMIN] função de criar novos servidores ou editar servidores existentes.

1. Para criar um novo servidor, clique em **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**. Para editar um servidor existente, clique no servidor desejado na **[!UICONTROL Label]** coluna.
1. Especifique o rótulo desejado para este servidor.
1. Na lista **[!UICONTROL Protocol]** suspensa, selecione o protocolo desejado: **FTP**.

   >[!NOTE]
   >
   >Como prática recomendada, recomendamos usar [!DNL Amazon S3] como método para obter arquivos e fornecer arquivos aos parceiros. [!DNL Amazon S3] fornece uma interface simples de serviços da Web que pode ser usada para armazenar e recuperar qualquer quantidade de dados, a qualquer momento, de qualquer lugar na Web. Para obter mais informações, consulte [Sobre o Amazon S3](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/amazon-s3.html) no Guia *do usuário do* Audience Manager.

1. Preencha os campos:

   * **[!UICONTROL Type]:**Selecione o tipo de criptografia desejado:**[!UICONTROL SFTP]**ou **[!UICONTROL FTPs/TLS]**.
   * **[!UICONTROL Domain]:**Especifique o domínio desejado (host) para este servidor.
   * **[!UICONTROL Port]:**Especifique a porta desejada para este servidor. A porta padrão é exibida para cada tipo de criptografia. Você pode alterar a porta padrão, se necessário.
   * **[!UICONTROL Remote Path]:**Especifique o caminho remoto desejado para este servidor. Se você deixar esse campo vazio, o Audience Manager colocará os arquivos no diretório padrão.
   * **[!UICONTROL .tmp File Rename on Completion]:**Ative esta opção para renomear o`.tmp`arquivo após a conclusão.
   * **[!UICONTROL Filename Suffix]:**Especifique o texto que deseja anexar para transferir arquivos.
   * **[!UICONTROL Moved to When Finished]:**Especifique o caminho para o local onde deseja que o arquivo de transferência seja movido após a conclusão.
   * **[!UICONTROL Authentication]:**Especifique o método de autenticação do servidor desejado:**[!UICONTROL Username/Password]**ou **[!UICONTROL SSH Key]**.
   >[!NOTE]
   >
   >Lembre-se de adicionar nossa saída [!DNL FTP] [!DNL IP] à sua lista de IPs permitidos: **52.44.29.2004**.

1. Para **[!UICONTROL SSH Key]** autenticação:
   1. Gere o par de chaves públicas/privadas de qualquer [!DNL Linux] computador ou [!DNL Mac] .
   1. Atribua a chave **** pública ao cliente para atualizá-lo em seu [!DNL SFTP] servidor. Eles devem incluir todo o texto da chave pública em seu servidor, incluindo `-----BEGIN RSA PRIVATE KEY-----` e `-----END RSA PRIVATE KEY-----` . Em troca, eles devem fornecer o nome de usuário sob o qual estão instalando a chave.
   1. Atualize o campo de nome de usuário com o campo fornecido pelo cliente e o campo de chave com a chave **** privada.
1. Clique **[!UICONTROL Create]** se estiver criando um novo servidor ou clique **[!UICONTROL Update]** se estiver editando um servidor existente.
