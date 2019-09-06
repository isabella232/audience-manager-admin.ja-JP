---
description: 顧客によっては、バケットにアップロードされた保存先データの承認のための Amazon Simple Storage Service（Amazon S3）へのアクセスやシークレットキーをアドビに提供しない場合があります。
seo-description: 顧客によっては、バケットにアップロードされた保存先データの承認のための Amazon Simple Storage Service（Amazon S3）へのアクセスやシークレットキーをアドビに提供しない場合があります。
seo-title: How To  Authorize Cross-Account Amazon S3 Bucket Access for Batch Destinations
title: アカウントを横断したAmazon S3バケットへのアクセスを許可する方法
uuid: da2bcbda- a765-437a- bfe9-4355383a4730
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# How To Authorize Cross-Account Amazon S3 Bucket Access for Batch Destinations{#authorize-cross-account-bucket-batch}

Some customers may not want to provide their [!DNL Amazon S3] access or secret keys to Adobe to authorize destination data upload to their buckets.

お客様が提供することのできる代替 [!UICONTROL Cross-Account Bucket Permissions][!DNL Amazon S3]手段です。このプロセスについては、[AWS のドキュメント](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html)で説明しています。Audience Manager でこの代替手段を有効にするには、次の手順に従ってください。

1. 選択して **[!UICONTROL Servers]** 選択 **[!UICONTROL Create Server]**&#x200B;します。
1. Select **[!UICONTROL S3]** in the **[!UICONTROL Protocol/Credentials]** drop-down mask.
1. **[!UICONTROL Use Internal Adobe Key]** このオプションを選択します。
1. Use your customer's account and bucket name in [!DNL Amazon S3].
1. Make sure that your customer white lists the [!DNL Amazon S3] account `975822914085` on their [!DNL S3] bucket.

>[!NOTE]
>
>送信公開者が、アップロードされたデータに権限レベル `bucket-owner-full-control` を設定し、顧客がそのデータを所有できるようにします。
