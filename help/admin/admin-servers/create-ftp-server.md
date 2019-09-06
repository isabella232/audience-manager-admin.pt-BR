---
description: Use a página Servidores na ferramenta de Administração do Audience Manager para criar um novo servidor FTP ou editar um servidor existente.
seo-description: Use a página Servidores na ferramenta de Administração do Audience Manager para criar um novo servidor FTP ou editar um servidor existente.
seo-title: Criar ou editar um servidor FTP
title: Criar ou editar um servidor FTP
uuid: 9273 abb 2-963 d -4 d 83-bf 5 a-b 3817 f 0 b 90 e 6
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# Criar ou editar um servidor FTP {#create-or-edit-an-ftp-server}

Use [!UICONTROL Servers] a página na ferramenta de administração do Audience Manager para criar um novo servidor FTP ou editar um servidor existente.

>[!NOTE]
>
>Você deve ter [!UICONTROL DEXADMIN] a função para criar novos servidores ou editar servidores existentes.

1. Para criar um novo servidor, clique **[!UICONTROL Servers]** em &gt; **[!UICONTROL Create Server]**. Para editar um servidor existente, clique no servidor desejado na **[!UICONTROL Label]** coluna.
1. Especifique o rótulo desejado para este servidor.
1. Na lista **[!UICONTROL Protocol]** suspensa, selecione o protocolo desejado: **FTP**.

   >[!NOTE]
   >
   >Como prática recomendada, recomendamos usar [!DNL Amazon S3] como um método para obter arquivos de e entregar arquivos para parceiros. [!DNL Amazon S3] fornece uma interface simples de serviços da Web que pode ser usada para armazenar e recuperar qualquer quantidade de dados, a qualquer momento, de qualquer lugar na Web. Para obter mais informações, consulte [Sobre o Amazon S 3](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/amazon-s3.html) no Guia do usuário *do Audience Manager*.

1. Preencha os campos:

   * **[!UICONTROL Type]:** Selecione o tipo de criptografia desejado: **[!UICONTROL SFTP]** ou **[!UICONTROL FTPs/TLS]**.
   * **[!UICONTROL Domain]:** Especifique o domínio desejado (host) para este servidor.
   * **[!UICONTROL Port]:** Especifique a porta desejada para este servidor. A porta padrão é exibida para cada tipo de criptografia. Você pode alterar a porta padrão, se necessário.
   * **[!UICONTROL Remote Path]:** Especifique o caminho remoto desejado para esse servidor. Se você deixar esse campo vazio, o Audience Manager colocará os arquivos no diretório padrão.
   * **[!UICONTROL .tmp File Rename on Completion]:** Habilite essa opção para renomear `.tmp` o arquivo na conclusão.
   * **[!UICONTROL Filename Suffix]:** Especifique o texto que você deseja anexar para transferir arquivos.
   * **[!UICONTROL Moved to When Finished]:** Especifique o caminho para o local onde você deseja que o arquivo de transferência seja movido na conclusão.
   * **[!UICONTROL Authentication]:** Especifique o método de autenticação do servidor desejado: **[!UICONTROL Username/Password]** ou **[!UICONTROL SSH Key]**.
   >[!NOTE]
   >
   >Lembre-se da lista de permissões [!DNL FTP][!DNL IP]: **52.44.29.204**.

1. Para **[!UICONTROL SSH Key]** autenticação:
   1. Gere o par de chave pública/privada de qualquer computador [!DNL Linux] ou [!DNL Mac] máquina.
   1. Dê a chave **pública** ao cliente para atualizar em seu [!DNL SFTP] servidor. Eles devem incluir todo o texto da chave pública no servidor, incluindo `-----BEGIN RSA PRIVATE KEY-----` e `-----END RSA PRIVATE KEY-----` . Em troca, eles devem fornecer o nome de usuário no qual estão instalando a chave.
   1. Atualize o campo de nome de usuário com aquele fornecido pelo cliente e pelo campo-chave com a **chave privada**.
1. Clique **[!UICONTROL Create]** em se estiver criando um novo servidor ou clique **[!UICONTROL Update]** em caso esteja editando um servidor existente.
