---
description: Audience Manager の Admin ツールの Servers ページを使用して、新しい FTP サーバーを作成するか、既存のサーバーを編集します。
seo-description: Audience Manager の Admin ツールの Servers ページを使用して、新しい FTP サーバーを作成するか、既存のサーバーを編集します。
seo-title: FTP サーバーの作成または編集
title: FTP サーバーの作成または編集
uuid: 9273abb2-963d-4d83-bf5a-b3817f0b90e6
translation-type: tm+mt
source-git-commit: 78d694670e7abdc18938c5be729ad499e2647825
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 69%

---


# FTP サーバーの作成または編集 {#create-or-edit-an-ftp-server}

Audience Manager の Admin ツールの [!UICONTROL Servers] ページを使用して、新しい FTP サーバーを作成するか、既存のサーバーを編集します。

>[!NOTE]
>
>新しいサーバーの作成や既存のサーバーの編集をおこなうには、[!UICONTROL DEXADMIN] の役割が必要です。

1. To create a new server, click **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**. 既存のサーバーを編集するには、「**[!UICONTROL Label]**」列で目的のサーバーをクリックします。
1. このサーバーで使用するラベルを指定します。
1. 「**[!UICONTROL Protocol]**」ドロップダウンリストで、目的のプロトコル **FTP** を選択します。

   >[!NOTE]
   >
   >ベストプラクティスとして、パートナー間でのファイルのやり取りには、[!DNL Amazon S3] を推奨します。[!DNL Amazon S3] が提供するシンプルな Web サービスのインターフェイスを使用することで、あらゆるサイズのデータの保存および取得が Web 上でいつ、どこでも可能になります。For more information, see [About Amazon S3](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/amazon-s3.html) in the *Audience Manager User Guide*.

1. 以下のフィールドを設定します。

   * **[!UICONTROL Type]:**目的の暗号化タイプを選択します。**[!UICONTROL SFTP]**または&#x200B;**[!UICONTROL FTPs/TLS]**。
   * **[!UICONTROL Domain]:**このサーバーに必要なドメイン（ホスト）を指定します。
   * **[!UICONTROL Port]:**このサーバーに必要なポートを指定します。 デフォルトのポートは、暗号化タイプごとに表示されます。必要があればデフォルトのポートを変更できます。
   * **[!UICONTROL Remote Path]:**このサーバーに必要なリモートパスを指定します。 このフィールドを空白にすると、Audience Manager はファイルをデフォルトのディレクトリに配置します。
   * **[!UICONTROL .tmp File Rename on Completion]:**完了時に`.tmp`ファイルの名前を変更するには、このオプションを有効にします。
   * **[!UICONTROL Filename Suffix]:**ファイルの転送に追加するテキストを指定します。
   * **[!UICONTROL Moved to When Finished]:**転送ファイルを完了時に移動する場所のパスを指定します。
   * **[!UICONTROL Authentication]:**目的のサーバー認証方法を指定します。**[!UICONTROL Username/Password]**または&#x200B;**[!UICONTROL SSH Key]**。

   >[!NOTE]
   >
   >許可されているIPのリスト [!DNL FTP][!DNL IP] にOmnitureの出口を追加してください。 **52.44.29.204**.

1. **[!UICONTROL SSH Key]** 認証の場合：
   >[!NOTE]
   >
   >SSHキー認証を設定する場合は、常にOpenSSH形式でのみ公開鍵と秘密鍵を生成するようにしてください。
   1. 任意の [!DNL Linux]または [!DNL Mac] マシンから、公開鍵／秘密鍵のペアを生成します。
   1. **公開鍵**&#x200B;をクライアントに渡して、[!DNL SFTP] サーバーで更新します。これには、サーバー上にある公開鍵 （`-----BEGIN RSA PRIVATE KEY-----` や `-----END RSA PRIVATE KEY-----` を含む）のすべてのテキストを含める必要があります。一方、クライアントは鍵のインストールに使用するユーザー名を指定する必要があります。
   1. ユーザー名フィールドにクライアントが指定したユーザー名を入力し、鍵フィールドには&#x200B;**秘密鍵**&#x200B;を入力します。
1. 新しいサーバーを作成する場合は「**[!UICONTROL Create]**」をクリックし、既存のサーバーを編集する場合は「**[!UICONTROL Update]**」をクリックします。
