---
description: '顧客の問題をデバッグする際には、監査ログを出発点として使用してください。 '
seo-description: '顧客の問題をデバッグする際には、監査ログを出発点として使用してください。 '
seo-title: 監査ログ
title: 監査ログ
uuid: null
translation-type: ht
source-git-commit: 190ba5c1215782e46c8e544c10679d451fbed134

---


# 監査ログ {#audit-logging}

顧客の問題をデバッグする際には、[!UICONTROL  Audit Logging] を出発点として使用してください。

> [!NOTE]
>
>[!UICONTROL Audit Logging] は現在開発中で、変更される可能性があります。[!DNL JIRA]（[!DNL UI] チーム）で発生した問題があれば、記録してください。

![監査ログビュー](assets/audit-logging-img.png)

**Audit Type** ドロップダウンセレクターで、次のいずれかを選択します。

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

「**Object ID**」は、調査しているアイテムの ID です。次の表に、各ケースの「Object ID」に対応する ID を示します。

| Audit Type | Object ID |
---------|----------|
| [!UICONTROL Partner] | Partner ID - PID |
| [!UICONTROL User] | User ID |
| [!UICONTROL Group] | B3 |
| [!UICONTROL Datasource Summary] | Data Source ID |
| [!UICONTROL General Datasource] | Data Source ID |
| [!UICONTROL Merge Rule Datasource] | Data Source ID |
| [!UICONTROL Data Feed] | Data Feed ID |
| [!UICONTROL Data Feed Subscription] | Data Feed ID |
| [!UICONTROL Trait Summary] | SID (trait) |
| [!UICONTROL Trait Rule] | SID (trait) |
| [!UICONTROL Segment Summary] |  |
| [!UICONTROL Destination Summary] |  |
| [!UICONTROL Server-to-Server Destination] | なし |
| [!UICONTROL Derived Signal] | なし |
| [!UICONTROL Model] | なし |
| [!UICONTROL Segment Test Group] | なし |

ログの時間間隔を絞り込むには、[!UICONTROL Start Date]（[!DNL UTC]）および[!UICONTROL End Date]（[!DNL UTC]）を使用します。