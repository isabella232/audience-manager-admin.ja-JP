---
description: ベータ環境は Audience Manager の実装のテストに使用します。ベータ環境でおこなった変更は実稼動データに影響しません。Audience Manager ベータ環境は、実稼動環境の小規模なスタンドアロンバージョンです。テストするデータはすべてこの環境で入力および収集する必要があります。
seo-description: ベータ環境は Audience Manager の実装のテストに使用します。ベータ環境でおこなった変更は実稼動データに影響しません。Audience Manager ベータ環境は、実稼動環境の小規模なスタンドアロンバージョンです。テストするデータはすべてこの環境で入力および収集する必要があります。
seo-title: ベータ環境
solution: Audience Manager
title: ベータ環境
uuid: 6a253f4e-96e7-4395- a783- a8eb213b7daf
translation-type: tm+mt
source-git-commit: 7765dbf79c2fb6ca8c4b52fe8090c1fd11f9db27

---


# ベータ環境 {#beta-environment}

ベータ環境は Audience Manager の実装のテストに使用します。ベータ環境でおこなった変更は実稼動データに影響しません。Audience Manager ベータ環境は、実稼動環境の小規模なスタンドアロンバージョンです。テストするデータはすべてこの環境で入力および収集する必要があります。

## 概要 {#overview}

<!-- beta_environment_admin.xml -->

| サービス | URL／ホスト名 | プロビジョニングの手順 |
|--- |--- |--- |
| S3 |  | [Amazon S3バケットのプロビジョニングを参照](admin-beta-environment.md#provision-s3-buckets)してください。 |
| DCS | https&amp; amp;コロン;//dcs-beta.demdex.net/.. | 当社側から余分な手順は必要ありません。See [Access the DCS in the Beta Environment](admin-beta-environment.md#access-dcs-beta-environment). |
| UI | https&amp; amp;コロン;//bank-beta.demdex.com | データは、実稼動環境からベータ環境に、毎月コピーされます。実稼動用の資格情報はベータ版で有効です。 |
| API | https&amp; amp;コロン;//api-beta.demdex.com/.. | データは、実稼動環境からベータ環境に、毎月コピーされます。実稼動用の資格情報はベータ版で有効です。 |

## Amazon S3Bucketのプロビジョニング {#provision-s3-buckets}

>[!NOTE]
>
>現在は、使用 [!DNL FTP/SFTP]を停止しています。また、アウトバウンドデータ転送はベータ環境では動作しません。

受信データ用 [!DNL S3] のバケットをプロビジョニングするには:

1. [**SKUリクエストテクニカルオペレーションのヘルプ**](https://skms.adobe.com/) 機能を使用します。
1. 左 **[!UICONTROL Request TechOps Help]** のナビゲーションパネルに移動します。
1. で **[!UICONTROL Request Search]**、検索フィールドにAudience Managerを入力します。
1. 検索結果を下にスクロールして **、Audience Manager- S3Inbound/Outout Account Provisioningをクリック**&#x200B;します。
1. プロビジョニングウィンドウのフィールドに入力し、フィールド内の **サンドボックス環境** を指定 **[!UICONTROL Environment]** します。

>[!NOTE]
>
>使用を妨害し、 [!DNL FTP/SFTP] 使用を促進 [!UICONTROL Amazon S3]します。使用を推奨する理由は、Amazon [!UICONTROL Amazon S3] S3に [記載されています。概要](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/amazon-s3.html)。

## Access the DCS in the Beta Environment {#access-dcs-beta-environment}

To access the [!UICONTROL DCS] in the beta environment:

1. Make a [!UICONTROL DCS] call, using the [!DNL curl] [command](https://curl.haxx.se/docs/manpage.html). [!DNL Curl] は、サポートされている様々なプロトコルの中から 1 つを使用して、サーバー間データ転送をおこなうためのツールです。

   例えば、`curl -v https://dcs-beta.demdex.net/event`

1. Verify that your request was served by the beta [!UICONTROL DCS] by looking for "[!DNL sandbox]" in the [!UICONTROL DCS] response header.

   次に例を示します。

   ```
   curl -v http://dcs-beta.demdex.net/?event
   [...]
   < DCS: va6-sandbox-dcs-3.sandbox.demdex.com <release_number>
   [...]
   ```

<!--
1. Determine the load balancer's endpoint IP addresses.

   Run the `dig` [command](https://en.wikipedia.org/wiki/Dig_(command)) to determine the IP address of the nearest load balancer. The `dig` command queries the Domain Name System and returns the name and IP addresses of the Audience Manager [!UICONTROL Data Collection Servers (DCS)].

   ```
   dig dcs-beta.demdex.net
   ...
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 52.87.15.51
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 50.16.150.8
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 52.2.228.100
   ```

1. Using one of the addresses in the above table, add a static DNS entry in the [!DNL `/etc/hosts`] file.

   On Windows, modify [!DNL `c:\WINDOWS\system32\drivers\etc\hosts`].

   For example:

[!DNL `52.87.15.51 samplepartner.demdex.net`]

   >[!NOTE]
   >
   >The addresses change occasionally, so you must keep your [!DNL /etc/hosts] file up to date.

   Additionally, if you need to set up ID synchronization, you must add a similar entry for [!DNL dpm.demdex.net.]

[!DNL `52.87.15.51 dpm.demdex.net`] [!DNL]. 

1. Make a [!UICONTROL DCS] call, using the `curl` [command](https://curl.haxx.se/docs/manpage.html). Curl is a tool to transfer data from or to a server, using one of many supported protocols.

   For example:

[!DNL `https://<domain>/event?product=camera`] 

1. Verify that your request was served by the beta [!UICONTROL DCS] by looking for "sandbox" in the [!UICONTROL DCS] response header.

   For example:

   ```
   curl -v https://dcs-beta.demdex.net/?event
   [...]
   < DCS: va6-sandbox-dcs-3.sandbox.demdex.com <release_number>
   [...]
   ```
-->