---
description: Audience Managerの宛先を作成、編集および削除します。
seo-description: Audience Managerの宛先を作成、編集および削除します。
seo-title: 会社宛先の管理
title: 会社宛先の管理
uuid: d9a6bfb1-7629-44e0-b7d7-ece44f65ea2b
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# 会社宛先の管理 {#manage-company-destinations}

Audience Managerの宛先を作成、編集および削除します。

<!-- t_company_destinations.xml -->

For detailed information, see [Destinations](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/destinations/destinations.html) in the *Audience Manager User Guide*.

## 会社宛先の作成または編集 {#create-edit-company-destinations}

各セクションにスクロールして、[!DNL Audience Manager] の宛先の新規作成、または既存の宛先の編集手順を参照してください。

<!-- create-edit-company-destinations.xml -->

Visit the [Experience Cloud partner integration page](https://wiki.corp.adobe.com/x/mPIMPw) before setting up destinations. このページには、[!DNL Audience Manager] パートナー統合のそれぞれについて入力する必要がある個別の情報について記載されています。

クライアントがで宛先とし [!DNL Adobe Media Optimizer] て使用する場合は、 [!DNL Audience Manager] で設定する必要があります [!DNL Adobe Media Optimizer]。

## 「Destination」タブに移動{#navigate-destinations}

1. 「**[!UICONTROL Companies]**」をクリックし、目的の会社を検索してからクリックして、[!UICONTROL Profile] ページを表示します。「[!UICONTROL Search]」ボックス、またはリストの最下部にあるページネーションコントロールを使用すると、目的の会社を検索できます。目的の列のヘッダーをクリックすると、その列を昇順または降順に並べ替えることができます。
1. 「**[!UICONTROL Destinations]**」タブをクリックします。
1. To create a new destination, click **[!UICONTROL Add Destination]**. 既存の宛先を編集するには、「**[!UICONTROL Name]」列で宛先の名前をクリックします。**

## 基本設定 {#basic-settings}

Fill in the fields in the **[!UICONTROL Basic Settings]** window.

* **[!UICONTROL Name]** :（必須）この宛先の名前を指定します。
* **[!UICONTROL Description]** :この宛先に関する説明情報を指定します。
* **[!UICONTROL Type]** :（必須）目的の宛先タイプを選択します。
   * **[!UICONTROL Bulk ID]**:異なるプラットフォーム間での同期ID。
   * **[!UICONTROL Bulk Trait]**:特性情報を様々なプラットフォームに一括して送信します。
   * **[!UICONTROL Bulk Segment]**:セグメント情報を様々なプラットフォームに一括して送信します。
   * **[!UICONTROL S2S]**：サーバー間宛先を使用して、リアルタイムデータとバッチデータを複数のプラットフォームに送信します。
* **[!UICONTROL Auto-Fill Destination Mapping]** :(の [!UICONTROL S2S] み)次のオプションを選択します。
   * **[!UICONTROL Segment ID]** :この設定を選択した場合、宛先の値のマッピングにセグメントIDが入 [!DNL Audience Manager] 力されます。
   * **[!UICONTROL Integration Code Value]** :この設定を選択すると、宛先の値のマッピングにセグメント統合コードが [!DNL Audience Manager] 入力されます。
* **[!UICONTROL User ID Key]** :（必須）ドロップダウンリストから、この宛先に使用する目的のユーザーIDキーを選択します。

この ID はマスターデータソース ID として使用します。これにより、ファイルに送信されるユーザー ID が決定されます。

>[!NOTE]
>
>宛先のタ [!UICONTROL Bulk ID] イプに対しては、またはIDを使用 [!DNL Audience Manager] でき [!UICONTROL User ID] ませ [!DNL Adobe Experience Cloud] ん。

If your data source ID ( [!UICONTROL DPID]) does not display in the drop-down list, you must select the **[!UICONTROL Outbound]** checkbox at the data-source level on the [Data Source Settings page](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/data-sources/manage-datasources.html).

* **[!UICONTROL Target Data Source]** :（必須）ドロップダウンリストから、この宛先に使用するデータソースを選択します。 この設定により、送信データのラベル付けができるようになり、クライアント側で別々のシステムに取り込めるようになります。
* **[!UICONTROL Foreign Account ID]** :この宛先の外部アカウントIDを指定します。 これは、受信者側のシステムでこの送信データの識別値となります。
* **[!UICONTROL Outbound Sample Rate Denominator]** :返されたデータの合計量が不明な場合は、この設定を使用して、全額ではなくサンプルのデータ量のみを返します。 この数値を調整して、データの比率を指定します（例えば、100 と指定すると標準のデータ量の 100 分の 1 が返され、10 と指定すると標準のデータ量の 10 分の 1 が返されます）。デフォルト値は 1 です。この場合、すべてのデータが返されます。

## リアルタイムデータ（S2S の宛先の場合） {#realtime-s2s}

If you are creating an [!UICONTROL S2S] destination, fill in the fields below:

**[!UICONTROL Servers]**:この宛先に使用する `HTTP` サーバーを選択します。
**[!UICONTROL Format]**:ドロップダウンリストから、この宛先に使用する形式を選択します。 [!UICONTROL HTTP only].

>[!NOTE]
>
>For [!DNL S2S] only, you can enable or disable either [!UICONTROL Realtime] or [!UICONTROL Batch] destinations using the onscreen Off/On sliders. 両方のオプションを無効にすることはできません。

## バッチデータ {#batch-data}

For [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] or [!UICONTROL Bulk Segment] destinations, fill in the fields below:

* **[!UICONTROL Protocol]**:（必須）ドロップダウンリストから、この宛先に使用するプロトコルを選択します。
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**:（必須）ドロップダウンリストから、この宛先に使用するサーバーを選択します。
* **[!UICONTROL Format]**:（必須）ドロップダウンリストから、この宛先に使用する形式を選択します。またはフ [!DNL HTTP] ァイルの種類を指定します。
* **[!UICONTROL Sync Type]**:（必須）この宛先の同期タイプを選択します。 これは、クライアントが送信オーダーに含めるユーザーアクティビティのレベルを表します。クライアントがプロパティからのセグメント認定のみをおこなう場合は、「**[!UICONTROL Customer]」を選択します。**&#x200B;すべての **ユーザーにまたがるオフサイトアクティビティからのセグメント認定を含める場合は、「[!UICONTROL Platform]**[!DNL Audience Manager]」を選択します。
* **[!UICONTROL Customer]**:ファイルには、選択した期間において、クライアントのプロパティ（クライアントに関連付けられた）に対してのみ1つ以上の特性実現を持つアクテ [!UICONTROL PID]ィブなユーザーが含まれます。 *リアルタイム*&#x200B;セグメント認識を宛先に送信する場合、クライアントはこのオプションを使用する必要があります。
* **[!UICONTROL Platform]**：選択した期間について、すべての [!DNL Audience Manager] クライアントのプロパティの任意の箇所で（すべてのクライアント PID に関連付けられている）リアルタイムインタラクションが、ID 同期か特性認識かを問わず、少なくとも 1 件あるアクティブユーザーがファイルに含まれます。*完全な*&#x200B;セグメント認識を宛先に送信する場合、クライアントはこのオプションを使用する必要があります。
* **[!UICONTROL Lifetime]**：宛先が作成された後の、すべての [!DNL Audience Manager] クライアントプロパティの任意の箇所で見られるアクティブユーザーがファイルに含まれます。
* **[!UICONTROL Sync Type Lookback Period]**:またはを選択し [!UICONTROL Customer] た場合 [!UICONTROL Platform]は、期間を選択します。 ファイルには選択した期間のアクティブユーザーが含まれます。次に、オーダータイプを選択します。これは、パートナーとの各送信統合の頻度と範囲を表します。差分オーダーと完全オーダーのいずれかを選択します。
* **[!UICONTROL Incremental Scheduled Run]**:各実行では、前回のア [!DNL Audience Manager] ウトバウンドオーダー以降に認定された純新規ユーザーのみがアウトバウンドされます。 [!DNL Audience Manager] で差分同期処理を実行する間隔を選択します。例えば、24 時間ごと、7 日ごと、30 日ごとを選択できます。また、実行しないようにすることもできます。

>[!NOTE] {importance="high"}
>
>最初の増分順序は、宛先に以前のユーザーが送信されなかったので、完全な順序と同じです。

* **[!UICONTROL Full Sync Scheduled Run]**:各実行では、宛先が最初に設 [!DNL Audience Manager] 定されてから、アクティブなすべてのユーザーが送信されます。 [!DNL Audience Manager] が完全同期処理の実行に使用するスケジュールを選択します。例えば、24 時間ごと、7 日ごと、30 日ごとを選択できます。また、実行しないようにすることもできます。

>[!NOTE] {importance="high"}
>
>完全同期よりも増分同期の方が頻繁に使用することをお勧めします。 差分同期では、新しい特性認識または ID の同期を含むファイルしか送信されません。完全同期では、新しい認識や ID の同期の有無にかかわらず、すべてのファイルが送信されます。Only use the [!UICONTROL Full Sync Scheduled Run] configuration when clients need a full copy of all their users, to reduce the outbound data volume.

## データソースの設定 {#configure-data-sources}

For [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] or [!UICONTROL Bulk Segment] destinations, fill in the fields below. これらの設定により、データソースに関連付けられているすべてのデータ（選択したタイプにより、特性、セグメント、ID のいずれか）を送信できます。

* **[!UICONTROL All Unrestricted First Party Data]**:すべてのファーストパーティデータソースを使用する場合に選択します。 If you select this option, the [!UICONTROL Available Data Sources] options are disabled.
* **[!UICONTROL Available Data Sources]**:矢印を使用して、データソースをボックスとボックスの間 **[!UICONTROL Available Data Sources]** で移動 **[!UICONTROL In File Data Sources]** します。

## 保存とファイナライズ {#save-and-finalize}

すべての必須フィールドに入力すると、「**[!UICONTROL Save]」がアクティブ化されます。**「**[!UICONTROL Save]」をクリックすると、宛先の作成処理がファイナライズされます。**

## 会社宛先の削除 {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

宛先を削除するには：

1. 「**[!UICONTROL Companies]**」をクリックし、目的の会社を特定してからクリックして、その後「**[!UICONTROL Destinations]」タブをクリックします。**
1. 目的の宛先の「![](assets/icon_delete.png)」列で **[!UICONTROL Actions]をクリックします。**
1. 「**[!UICONTROL OK]」をクリックして削除を確定します。**

>[!NOTE]
>
>宛先にセグメントがマッピングされている場合は、宛先を削除できません。