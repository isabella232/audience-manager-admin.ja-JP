---
description: Audience Manager の Admin ツールの Servers ページを使用して、新しい FTP サーバーを作成するか、既存のサーバーを編集します。
seo-description: Audience Manager の Admin ツールの Servers ページを使用して、新しい FTP サーバーを作成するか、既存のサーバーを編集します。
seo-title: FTP サーバーの作成または編集
title: FTP サーバーの作成または編集
uuid: 9273abb2-963d-4d83- bf5a- b5a- b3817f0b90e6
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# FTP サーバーの作成または編集 {#create-or-edit-an-ftp-server}

Audience Manager の Admin ツールの [!UICONTROL Servers] ページを使用して、新しい FTP サーバーを作成するか、既存のサーバーを編集します。

>[!NOTE]
>
>You must have the [!UICONTROL DEXADMIN] role in order to create new servers or edit existing servers.

1. To create a new server, click **[!UICONTROL Servers]** &gt; **[!UICONTROL Create Server]**. 既存のサーバーを編集するには、「**[!UICONTROL Label]」列で目的のサーバーをクリックします。**
1. このサーバーで使用するラベルを指定します。
1. **[!UICONTROL Protocol]** ドロップダウンリストから、目的のプロトコルを選択します。 **FTP**.

   >[!NOTE]
   >
   >As best practice, we recommend using [!DNL Amazon S3] as a method for getting files from and delivering files to partners. [!DNL Amazon S3] が提供するシンプルな Web サービスのインターフェイスを使用することで、あらゆるサイズのデータの保存および取得が Web 上でいつ、どこでも可能になります。For more information, see [About Amazon S3](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/amazon-s3.html) in the *Audience Manager User Guide*.

1. 以下のフィールドを設定します。

   * **[!UICONTROL Type]:** 目的の暗号化タイプを選択します。 **[!UICONTROL SFTP]****[!UICONTROL FTPs/TLS]**&#x200B;または
   * **[!UICONTROL Domain]:** このサーバーの目的のドメイン（ホスト）を指定します。
   * **[!UICONTROL Port]:** このサーバーのポートを指定します。デフォルトのポートは、暗号化タイプごとに表示されます。必要があればデフォルトのポートを変更できます。
   * **[!UICONTROL Remote Path]:** このサーバのリモートパスを指定します。このフィールドを空白にすると、Audience Manager はファイルをデフォルトのディレクトリに配置します。
   * **[!UICONTROL .tmp File Rename on Completion]:** このオプションを有効にすると、ファイルの `.tmp` 名前が変更されます。
   * **[!UICONTROL Filename Suffix]:** ファイルの転送に追加するテキストを指定します。
   * **[!UICONTROL Moved to When Finished]:** 転送ファイルを移動する場所のパスを指定します。
   * **[!UICONTROL Authentication]:** 目的のサーバー認証方法を指定します。 **[!UICONTROL Username/Password]****[!UICONTROL SSH Key]**&#x200B;または
   >[!NOTE]
   >
   >次 [!DNL FTP][!DNL IP]のホワイトリストに登録してください。 **52.44.29.204**.

1. **[!UICONTROL SSH Key]** 認証の場合:
   1. Generate the public / private key pair from any [!DNL Linux] or [!DNL Mac] machine.
   1. **公開鍵**[!DNL SFTP]を、 サーバーで更新するクライアントに渡します。これらのテキストを、サーバー上の公開鍵の `-----BEGIN RSA PRIVATE KEY-----` すべてのテキストに含めておく必要 `-----END RSA PRIVATE KEY-----` があります。一方、クライアントは鍵のインストールに使用するユーザー名を指定する必要があります。
   1. ユーザー名フィールドにクライアントが指定したユーザー名を入力し、鍵フィールドには&#x200B;**秘密鍵**&#x200B;を入力します。
1. 新しいサーバーを作成する **[!UICONTROL Create]** 場合はクリックし、既存のサーバーを編集する場合はクリック **[!UICONTROL Update]** します。
