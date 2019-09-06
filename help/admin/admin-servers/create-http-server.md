---
description: Audience Manager の Admin ツールの Servers ページを使用して、新しい HTTP サーバーを作成するか、既存のサーバーを編集します。
seo-description: Audience Manager の Admin ツールの Servers ページを使用して、新しい HTTP サーバーを作成するか、既存のサーバーを編集します。
seo-title: HTTP サーバーの作成または編集
title: HTTP サーバーの作成または編集
uuid: 1ef0e751- e239-4dc6- a4f6-73cc05686807
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# HTTP サーバーの作成または編集 {#create-or-edit-an-http-server}

Audience Manager の Admin ツールの [!UICONTROL Servers] ページを使用して、新しい HTTP サーバーを作成するか、既存のサーバーを編集します。

>[!NOTE]
>
>You must have the [!UICONTROL DEXADMIN] role in order to create new servers or edit existing servers.

1. 新しいサーバーを作成するには、&gt;に **[!UICONTROL Servers]** 移動 **[!UICONTROL Create Server]**&#x200B;します。既存のサーバーを編集するには、「**[!UICONTROL Label]」列で目的のサーバーをクリックします。**
1. このサーバーで使用するラベルを指定します。
1. **[!UICONTROL Protocol]** ドロップダウンリストから、目的のプロトコルを選択します。 [!DNL HTTP]を参照してください。
1. 以下のフィールドを設定します。

   * **[!UICONTROL Domain]:** このサーバーの目的のドメイン（ホスト）を指定します。
   * **[!UICONTROL Port]:** このサーバーのポートを指定します。デフォルトのポートは、暗号化タイプごとに表示されます。必要があればデフォルトのポートを変更できます。
   * **[!UICONTROL Maximum Users Per Request]:** このサーバーで許可されているリクエストごとの最大ユーザー数を指定してください。
   * **[!UICONTROL URL Prefix]:** このサーバーに使用する [!DNL URL] プレフィックスを指定します。
   * **[!UICONTROL Authentication URL]:** このサーバー [!UICONTROL Authentication URL] を指定 `HTTP` します。
   * **[!UICONTROL Authentication]:** 目的の認証方法を指定します。 **[!UICONTROL None]**、 **[!UICONTROL Username/Password]**&#x200B;また **[!UICONTROL SSH Key]**&#x200B;は、または
   * **[!UICONTROL HTTP Signature Header]:** 署名キーを含む [!DNL HTTP] 、顧客が提供するヘッダー [!DNL HTTP] の名前。The default value is [!UICONTROL X-Signature], as shown in the example below:

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

   * **[!UICONTROL HTTP Signature Key]:** 顧客が要求する [!DNL HTTP] リクエストへの署名に使用されるキー。
   * **[!UICONTROL Show Signature Key]:** ブラウザーに署名を表示するかどうかを切り替えます。
   * **[!UICONTROL HTTP Signature Encryption Method]:** 署名の暗号化に使用するメソッドを指定します。Use [!UICONTROL SHA1] unless the customer prefers otherwise.
   >[!NOTE]
   >
   >If you want to enable [OAuth 2.0 authentication for real-time data transfers](https://docs.adobe.com/help/en/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/real-time-outbound-transfers/oauth-in-outbound-transfers.html) for a partner, fill in the fields as in the table below. *斜体*&#x200B;のフィールドは、正確に表のとおりに入力する必要があります。

   | 名前 | 値 |
   |---|---|
   | [!UICONTROL Label] | [!UICONTROL Server with OAuth 2.0 enabled] |
   | [!UICONTROL Protocol] | [!UICONTROL HTTP] |
   | [!UICONTROL Domain] | [!UICONTROL api.partner.com] |
   | [!UICONTROL Port] | [!UICONTROL 443] |
   | [!UICONTROL Maximum Users per Request] | [!UICONTROL 10] |
   | [!UICONTROL URL Prefix] | [!UICONTROL /segments/aam] |
   | [!UICONTROL Authentication URL] | [!UICONTROL api.partner.com/oauth2/token] |
   | [!UICONTROL Authentication] | [!UICONTROL Username/Password] |
   | [!UICONTROL Username] | [!UICONTROL *Authorization *] |
   | [!UICONTROL Password] | your_ password_ here |
   | [!UICONTROL HTTP Signature Header] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Key] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Encryption Method] | [!UICONTROL None] |

1. 新しいサーバーを作成する **[!UICONTROL Create]** 場合はクリックし、既存のサーバーを編集する場合はクリック **[!UICONTROL Update]** します。