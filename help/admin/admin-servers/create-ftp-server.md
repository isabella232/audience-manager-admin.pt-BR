---
description: Use a página Servidores na ferramenta Audience Manager Admin para criar um novo servidor FTP ou editar um servidor existente.
seo-description: Use the Servers page in the Audience Manager Admin tool to create a new FTP server or to edit an existing server.
seo-title: Create or Edit an FTP Server
title: Criar ou editar um servidor FTP
uuid: 9273abb2-963d-4d83-bf5a-b3817f0b90e6
exl-id: 9eae4ecf-ccde-483a-ae53-1cbac033d8d6
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 4%

---

# Criar ou editar um servidor FTP {#create-or-edit-an-ftp-server}

Use o [!UICONTROL Servers] na ferramenta Audience Manager Admin para criar um novo servidor FTP ou editar um servidor existente.

>[!NOTE]
>
>Você deve ter o [!UICONTROL DEXADMIN] para criar novos servidores ou editar servidores existentes.

1. Para criar um novo servidor, clique em **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**. Para editar um servidor existente, clique no servidor desejado na **[!UICONTROL Label]** coluna.
1. Especifique o rótulo desejado para este servidor.
1. No **[!UICONTROL Protocol]** selecione o protocolo desejado: **FTP**.

   >[!NOTE]
   >
   >Como prática recomendada, recomendamos usar [!DNL Amazon S3] como um método para obter arquivos do e entregá-los a parceiros. [!DNL Amazon S3] O fornece uma interface simples de serviços da web que pode ser usada para armazenar e recuperar qualquer quantidade de dados, a qualquer momento, de qualquer lugar na web. Para obter mais informações, consulte [Sobre o Amazon S3](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/amazon-s3.html) no *Guia do usuário do Audience Manager*.

1. Preencha os campos:

   * **[!UICONTROL Type]:** Selecione o tipo de criptografia desejado: **[!UICONTROL SFTP]** ou **[!UICONTROL FTPs/TLS]**.
   * **[!UICONTROL Domain]:** Especifique o domínio (host) desejado para este servidor.
   * **[!UICONTROL Port]:** Especifique a porta desejada para este servidor. A porta padrão é exibida para cada tipo de criptografia. Você pode alterar a porta padrão, se necessário.
   * **[!UICONTROL Remote Path]:** Especifique o caminho remoto desejado para este servidor. Se você deixar esse campo vazio, o Audience Manager colocará os arquivos no diretório padrão.
   * **[!UICONTROL .tmp File Rename on Completion]:** Habilite esta opção para renomear o `.tmp` arquivo na conclusão.
   * **[!UICONTROL Filename Suffix]:** Especifique o texto que deseja anexar para transferir arquivos.
   * **[!UICONTROL Moved to When Finished]:** Especifique o caminho para o local para onde deseja mover o arquivo de transferência na conclusão.
   * **[!UICONTROL Authentication]:** Especifique o método de autenticação de servidor desejado: **[!UICONTROL Username/Password]** ou **[!UICONTROL SSH Key]**.

   >[!NOTE]
   >
   >Lembre-se de adicionar nossa saída [!DNL FTP] [!DNL IP] à sua lista de IPs permitidos: **52.44.29.204**.

1. Para **[!UICONTROL SSH Key]** autenticação:
   >[!NOTE]
   >
   >Ao configurar a autenticação da Chave SSH, sempre gere as chaves públicas e privadas somente no formato OpenSSH.
   1. Gerar o par de chave pública/privada a partir de qualquer [!DNL Linux] ou [!DNL Mac] máquina.
   1. Dê a **chave pública** ao cliente para atualizar em seus [!DNL SFTP] servidor. Eles devem incluir todo o texto da chave pública no servidor, incluindo `-----BEGIN RSA PRIVATE KEY-----` e  `-----END RSA PRIVATE KEY-----` . No Exchange, eles devem fornecer o nome de usuário com o qual estão instalando a chave.
   1. Atualize o campo de nome de usuário com o fornecido pelo cliente e o campo de chave com o **chave privada**.
1. Clique em **[!UICONTROL Create]** se estiver criando um novo servidor, ou clique em **[!UICONTROL Update]** se você estiver editando um servidor existente.
