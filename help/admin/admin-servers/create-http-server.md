---
description: Audience Manager の Admin ツールの Servers ページを使用して、新しい HTTP サーバーを作成するか、既存のサーバーを編集します。
seo-description: Audience Manager の Admin ツールの Servers ページを使用して、新しい HTTP サーバーを作成するか、既存のサーバーを編集します。
seo-title: HTTP サーバーの作成または編集
title: HTTP サーバーの作成または編集
uuid: 1ef0e751-e239-4dc6-a4f6-73cc05686807
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 60%

---


# HTTP サーバーの作成または編集 {#create-or-edit-an-http-server}

Audience Manager の Admin ツールの [!UICONTROL Servers] ページを使用して、新しい HTTP サーバーを作成するか、既存のサーバーを編集します。

>[!NOTE]
>
>新しいサーバーの作成や既存のサーバーの編集をおこなうには、[!UICONTROL DEXADMIN] の役割が必要です。

1. To create a new server, go to **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**. 既存のサーバーを編集するには、「**[!UICONTROL Label]**」列で目的のサーバーをクリックします。
1. このサーバーで使用するラベルを指定します。
1. **[!UICONTROL Protocol]**&#x200B;ドロップダウンリストで、目的のプロトコル（[!DNL HTTP]）を選択します。
1. 以下のフィールドを設定します。

   * **[!UICONTROL Domain]:**このサーバーに必要なドメイン（ホスト）を指定します。
   * **[!UICONTROL Port]:**このサーバーに必要なポートを指定します。 デフォルトのポートは、暗号化タイプごとに表示されます。必要があればデフォルトのポートを変更できます。
   * **[!UICONTROL Maximum Users Per Request]:**このサーバーに対して許可される、1回の要求あたりの最大ユーザー数を指定します。
   * **[!UICONTROL URL Prefix]:**このサーバーで使用する[!DNL URL]プレフィックスを指定します。
   * **[!UICONTROL Authentication URL]:**このサー[!UICONTROL Authentication URL]`HTTP`バーのを指定します。
   * **[!UICONTROL Authentication]:**必要な認証方法を指定します。**[!UICONTROL None]**、**[!UICONTROL Username/Password]**または&#x200B;**[!UICONTROL SSH Key]**。
   * **[!UICONTROL HTTP Signature Header]:**顧客が提供する、[!DNL HTTP]署名キーを含むヘッダーの名前[!DNL HTTP]。 デフォルト値は、次の例のように[!UICONTROL X-Signature]です。

      ```
      * Connected to partner.website.com (127.0.0.1) port 80 (#0)
      > POST /webpage HTTP/1.1
      > Host: partner.host.com
      > Accept: */*
      > Content-Type: application/json
      > Content-Length: 20
      > X-Signature: wxa2ByMWhhP328EvHQsVlOD5jTc=
      POST message content
      ```

   * **[!UICONTROL HTTP Signature Key]:**顧客が提供する、[!DNL HTTP]リクエストへの署名に使用するキー。
   * **[!UICONTROL Show Signature Key]:**署名をブラウザーに表示するかどうかを切り替えます。
   * **[!UICONTROL HTTP Signature Encryption Method]:**署名の暗号化に使用する方法を指定します。 顧客が別途指定しない限り、「[!UICONTROL SHA1]」を使用します。

   >[!NOTE]
   >
   >If you want to enable [OAuth 2.0 authentication for real-time data transfers](https://docs.adobe.com/help/en/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/real-time-outbound-transfers/oauth-in-outbound-transfers.html) for a partner, fill in the fields as in the table below. *斜体*&#x200B;のフィールドは、正確に表のとおりに入力する必要があります。

   | 名前 | Value |
   |---|---|
   | [!UICONTROL Label] | [!UICONTROL Server with OAuth 2.0 enabled] |
   | [!UICONTROL Protocol] | [!UICONTROL HTTP] |
   | [!UICONTROL Domain] | [!UICONTROL api.partner.com] |
   | [!UICONTROL Port] | [!UICONTROL 443] |
   | [!UICONTROL Maximum Users per Request] | [!UICONTROL 10] |
   | [!UICONTROL URL Prefix] | [!UICONTROL /segments/aam] |
   | [!UICONTROL Authentication URL] | [!UICONTROL api.partner.com/oauth2/token] |
   | [!UICONTROL Authentication] | [!UICONTROL Username/Password] |
   | [!UICONTROL Username] | [!UICONTROL *認証&#x200B;*] |
   | [!UICONTROL Password] | （パスワードをここに入力） |
   | [!UICONTROL HTTP Signature Header] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Key] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Encryption Method] | [!UICONTROL None] |

1. 新しいサーバーを作成する場合は「**[!UICONTROL Create]**」をクリックし、既存のサーバーを編集する場合は「**[!UICONTROL Update]**」をクリックします。