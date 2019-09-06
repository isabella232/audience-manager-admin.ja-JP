---
description: Audience Manager API を使用しているクライアントへの注意事項。
seo-description: Audience Manager API を使用しているクライアントへの注意事項。
seo-title: API の要件と推奨事項
title: API の要件と推奨事項
uuid: ea9cf92- f0c8-4394-8532-0de9a2e7b103
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# API の要件と推奨事項 {#api-requirements-and-recommendations}

Things you should encourage your clients to be aware of when they're working with the Audience Manager [!DNL API]s.

## 要件 {#requirements}

Note the following when working with [!DNL Audience Manager] [!DNL API] code:

* **リクエストパラメーター：**&#x200B;特に指定のない限り、すべてのリクエストパラメーターが必要となります。
* **[!DNL JSON]コンテンツタイプ：**&#x200B;コード内で、`content-type: application/json` *および* `accept: application/json` を指定してください。

* **要求と応答：**&#x200B;適切な形式の [!DNL JSON] オブジェクトとして要求を送信してください。[!DNL Audience Manager] は [!DNL JSON] 形式のデータで応答します。サーバーの応答には要求されたデータもしくはステータスコード、またはその両方を含めることができます。

* **アクセス：**&#x200B;担当の[!DNL Audience Manager] コンサルタントによって、[!DNL API] 要求をおこなうために必要なクライアント ID およびキーが提供されます。

* **ドキュメントおよびコードサンプル：***斜体*&#x200B;のテキストは、[!DNL API] データを作成または受け取る際に指定または渡される変数を示します。*斜体*&#x200B;のテキストを独自のコード、パラメーターまたは他の必要な情報に置き換えてください。

## 推奨事項：汎用の API ユーザーを作成する {#recommendations}

We recommend creating a separate, technical user account for working with the Audience Manager [!DNL API]s. This is a generic account that is not tied to or associated with a specific user in your client's organization. This type of [!DNL API] user account helps accomplish 2 things:

* Identify what service is calling the [!DNL API] (e.g., calls from a client app that use our [!DNL API]s or from making bulk changes).
* [!DNL API]s.特定の従業員に関連付けられているアカウントは、会社の退出時に削除できます。This will prevent your customers from working with the available [!DNL API] code. 特定の従業員に結び付けられていない汎用アカウントを使用すると、この問題を回避できます。

このようなアカウントのユースケースとして、顧客が多数のセグメントを[一括管理ツール](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/bult-management-tools/bulk-management-intro.html)により一度に変更しようとしている場合を見てみましょう。To do this, they need [!DNL API] access. 特定のユーザーに対して権限を追加するのではなく、適切な資格情報、キー、および [!DNL API] 呼び出し用の暗号鍵を持つ汎用の [!DNL API] ユーザーアカウントを作成します。This is also useful if client's develop their own applications that use the [!DNL Audience Manager] [!DNL API]s.
