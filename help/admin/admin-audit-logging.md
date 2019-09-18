---
description: '顧客の問題をデバッグする際は、まず「監査ログ」を使用します。 '
seo-description: '顧客の問題をデバッグする際は、まず「監査ログ」を使用します。 '
seo-title: 監査ログ
title: 監査ログ
uuid: null
translation-type: tm+mt
source-git-commit: 190ba5c1215782e46c8e544c10679d451fbed134

---


# 監査ログ {#audit-logging}

顧客の問 [!UICONTROL  Audit Logging] 題をデバッグする際は、まず最初にを使用します。

> [!NOTE]
>
>[!UICONTROL Audit Logging] は現在開発中で、変更される可能性があります。 （チーム）で発生した問題をログに記 [!DNL JIRA] 録して[!DNL UI] ください

![監査ログビュー](assets/audit-logging-img.png)

「監査タイ **プ** 」ドロップダウンセレクタで、次のいずれかを選択します。

* [!UICONTROL Partner]
* [!UICONTROL User]
* [!UICONTROL Group]
* [!UICONTROL Datasource Summary]
* [!UICONTROL General Datasource]
* [!UICONTROL Merge Rule Datasource]
* [!UICONTROL Data Feed]
* [!UICONTROL Data Feed Subscription]
* [!UICONTROL Trait Summary]
* [!UICONTROL Trait Rule]
* [!UICONTROL Segment Summary]
* [!UICONTROL Destination Summary]
* [!UICONTROL Server to Server Destination]
* [!UICONTROL Derived Signal]
* [!UICONTROL Model]
* [!UICONTROL Segment Test Group]

オブ **ジェクト** IDは、調査する品目のIDです。 次の表で、各ケースのIDがオブジェクトIDに対応するIDを確認します。

| 監査タイプ | オブジェクトID |
---------|----------|
| [!UICONTROL Partner] | パートナーID - PID |
| [!UICONTROL User] | ユーザー ID |
| [!UICONTROL Group] | B3 |
| [!UICONTROL Datasource Summary] | データソース ID |
| [!UICONTROL General Datasource] | データソース ID |
| [!UICONTROL Merge Rule Datasource] | データソース ID |
| [!UICONTROL Data Feed] | Data Feed ID |
| [!UICONTROL Data Feed Subscription] | Data Feed ID |
| [!UICONTROL Trait Summary] | SID（特性） |
| [!UICONTROL Trait Rule] | SID（特性） |
| [!UICONTROL Segment Summary] |  |
| [!UICONTROL Destination Summary] |  |
| [!UICONTROL Server-to-Server Destination] | なし |
| [!UICONTROL Derived Signal] | なし |
| [!UICONTROL Model] | なし |
| [!UICONTROL Segment Test Group] | なし |

( [!UICONTROL Start Date] )と[!DNL UTC]( [!UICONTROL End Date] )を使[!DNL UTC]用して、ログの時間間隔を短縮します。