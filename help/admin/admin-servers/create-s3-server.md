---
description: Audience Manager の Admin ツールの Servers ページを使用して、新しい S3 サーバーを作成するか、既存のサーバーを編集します。
seo-description: Audience Manager の Admin ツールの Servers ページを使用して、新しい S3 サーバーを作成するか、既存のサーバーを編集します。
seo-title: S3 サーバーの作成または編集
title: S3 サーバーの作成または編集
uuid: 94fee787-eb26-45aa-b602-d61ab12969ea
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 78%

---


# S3 サーバーの作成または編集 {#create-or-edit-an-s-server}

Audience Manager の Admin ツールの [!UICONTROL Servers][!DNL S3] ページを使用して、新しい サーバーを作成するか、既存のサーバーを編集します。

>[!NOTE]
>
>新しいサーバーの作成や既存のサーバーの編集をおこなうには、[!UICONTROL DEXADMIN] の役割が必要です。

1. To create a new server, click **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**. 既存のサーバーを編集するには、「**[!UICONTROL Label]**」列で目的のサーバーをクリックします。
1. このサーバーで使用するラベルを指定します。
1. **[!UICONTROL Protocol]**&#x200B;ドロップダウンリストで、目的のプロトコル（**[!UICONTROL S3]**）を選択します。

   >[!NOTE]
   >
   >パートナー間でのファイルのやり取りには、[!DNL Amazon S3] を使用する方法を推奨します。[!DNL Amazon S3] が提供するシンプルな Web サービスのインターフェイスを使用することで、あらゆるサイズのデータの保存および取得が Web 上でいつ、どこでも可能になります。For more information, see [About Amazon S3](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/amazon-s3.html) in the *Audience Manager User Guide*.

1. 以下のフィールドを設定します。

   * **[!UICONTROL Account]:** 目的の [!DNL S3] アカウントを指定します。
   * **[!UICONTROL Bucket]:** 目的の [!DNL S3] グループを指定します。
   * **[!UICONTROL Directory]:** 目的の [!DNL S3] ディレクトリを指定します。
   * **[!UICONTROL Access Key]:** 目的の [!DNL S3] アクセスキーを指定します。
   * **[!UICONTROL Secret Key]:** 目的の [!DNL S3] 秘密キーを指定します。

1. 新しいサーバーを作成する場合は「**[!UICONTROL Create]**」をクリックし、既存のサーバーを編集する場合は「**[!UICONTROL Update]**」をクリックします。