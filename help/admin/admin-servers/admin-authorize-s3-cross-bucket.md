---
description: 顧客によっては、バケットにアップロードされた保存先データの承認のための Amazon Simple Storage Service（Amazon S3）へのアクセスやシークレットキーをアドビに提供しない場合があります。
seo-description: 顧客によっては、バケットにアップロードされた保存先データの承認のための Amazon Simple Storage Service（Amazon S3）へのアクセスやシークレットキーをアドビに提供しない場合があります。
seo-title: バッチ宛先に対するアカウント間のAmazon S3バケットアクセスを承認する方法
title: バッチ宛先に対するアカウント間のAmazon S3バケットアクセスを承認する方法
uuid: da2bcbda-a765-437a-bfe9-4355383a4730
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# How To Authorize Cross-Account Amazon S3 Bucket Access for Batch Destinations{#authorize-cross-account-bucket-batch}

Some customers may not want to provide their [!DNL Amazon S3] access or secret keys to Adobe to authorize destination data upload to their buckets.

お客様に提供できる代替案が入って [!UICONTROL Cross-Account Bucket Permissions] います [!DNL Amazon S3]。 このプロセスについては、[AWS のドキュメント](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html)で説明しています。Audience Manager でこの代替手段を有効にするには、次の手順に従ってください。

1. に移動し、を **[!UICONTROL Servers]** 選択しま **[!UICONTROL Create Server]**&#x200B;す。
1. Select **[!UICONTROL S3]** in the **[!UICONTROL Protocol/Credentials]** drop-down mask.
1. オプションをオン **[!UICONTROL Use Internal Adobe Key]** にします。
1. Use your customer's account and bucket name in [!DNL Amazon S3].
1. Make sure that your customer white lists the [!DNL Amazon S3] account `975822914085` on their [!DNL S3] bucket.

>[!NOTE]
>
>送信公開者が、アップロードされたデータに権限レベル `bucket-owner-full-control` を設定し、顧客がそのデータを所有できるようにします。
