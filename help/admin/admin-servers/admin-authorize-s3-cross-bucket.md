---
description: 顧客によっては、バケットにアップロードされた保存先データを認証するための、Amazon Simple Storage Service（Amazon S3）へのアクセスや秘密鍵をアドビに提供したくないという場合があります。
seo-description: 顧客によっては、バケットにアップロードされた保存先データを認証するための、Amazon Simple Storage Service（Amazon S3）へのアクセスや秘密鍵をアドビに提供したくないという場合があります。
seo-title: 手順：バッチ保存先へのクロスアカウント Amazon S3 バケットアクセスを承認
title: 手順：バッチ保存先へのクロスアカウント Amazon S3 バケットアクセスを承認
uuid: da2bcbda-a765-437a-bfe9-4355383a4730
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 96%

---


# 手順：バッチ保存先へのクロスアカウント Amazon S3 バケットアクセスを承認{#authorize-cross-account-bucket-batch}

顧客によっては、バケットにアップロードされた保存先データを認証するための、[!DNL Amazon S3] へのアクセスや秘密鍵をアドビに提供したくないという場合があります。

代わりに、お客様に [!DNL Amazon S3] の [!UICONTROL Cross-Account Bucket Permissions] を提供できます。このプロセスについては、[AWS のドキュメント](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html)で説明しています。Audience Manager でこの代替手段を有効にするには、次の手順に従ってください。

1. **[!UICONTROL Servers]** に移動して、「**[!UICONTROL Create Server]**」を選択します。
1. **[!UICONTROL S3]**&#x200B;ドロップダウンマスクで「**[!UICONTROL Protocol/Credentials]**」を選択します。
1. **[!UICONTROL Use Internal Adobe Key]** オプションを選択します。
1. [!DNL Amazon S3] で顧客のアカウントとバケット名を使用します。
1. 顧客の [!DNL S3]バケットで [!DNL Amazon S3] アカウント `975822914085` がホワイトリストに入っていることを確認します。

>[!NOTE]
>
>送信公開者が、アップロードされたデータに権限レベル `bucket-owner-full-control` を設定し、顧客がそのデータを所有できるようにします。
