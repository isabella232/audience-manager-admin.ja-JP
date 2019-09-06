---
description: 次の手順に従って、最近アクティブなユーザーのみが含まれる、完全な同期ファイルを生成します。アクティブユーザーをフィルタリングして、関連するデータをオンサイトのターゲット設定システムにプッシュしたり、DSP に送信するファイルのサイズを制限することが必要となる場合があります。このフィルターを増分同期で使用することはできません。
seo-description: 次の手順に従って、最近アクティブなユーザーのみが含まれる、完全な同期ファイルを生成します。アクティブユーザーをフィルタリングして、関連するデータをオンサイトのターゲット設定システムにプッシュしたり、DSP に送信するファイルのサイズを制限することが必要となる場合があります。このフィルターを増分同期で使用することはできません。
seo-title: 発信データをアクティブユーザーのみにフィルタリング
title: 発信データをアクティブユーザーのみにフィルタリング
uuid: a2b4a385- eee3-458c- b978-09509cacb397
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# 発信データをアクティブユーザーのみにフィルタリング {#filter-outbound-data-by-active-users-only}

次の手順に従って、最近アクティブなユーザーのみが含まれる、完全な同期ファイルを生成します。アクティブユーザーをフィルタリングして、関連するデータをオンサイトのターゲット設定システムにプッシュしたり、DSP に送信するファイルのサイズを制限することが必要となる場合があります。このフィルターを増分同期で使用することはできません。

>[!NOTE]
>
>訪問者は、選択した顧客サイトまたは広告トラフィックの「アクティブ」として表示される必要がありません。任意の [!DNL Audience Manager] ユーザーまたはパートナーに認識されれば、「アクティブ」と認定されます。

アクティブなユーザーのみをフィルタリングするには、次の手順に従います。

1. 「**[!UICONTROL Companies]**」をクリックします。
1. Select the company you want to work with and click **[!UICONTROL Destinations]**.
1. [!UICONTROL Batch Data] セクションで、次のオプションを設定します。

   * **[!UICONTROL Sync Type]**:また **[!UICONTROL Customer]****[!UICONTROL Platform]**&#x200B;はを選択します。
   * **[!UICONTROL Sync Type Lookback Period]**:この時間間隔は、データファイルの範囲を定義します。選択肢 **[!UICONTROL 24 hours]****[!UICONTROL 7 days]****[!UICONTROL 30 days]**&#x200B;には、などがあります。
   * **[!UICONTROL Incremental Sync Scheduled Run]**:選択 **[!UICONTROL Never]**&#x200B;します。このフィルターは完全同期ファイルに対してのみ適用されます。
   * **[!UICONTROL Full Sync Scheduled Run]**:これにより、このファイルを受信する頻度が決まります。選択肢には **[!UICONTROL 24 hours]****[!UICONTROL 7 days]**、 **[!UICONTROL 30 days]**&#x200B;または（を無効にする） **[!UICONTROL Never]** オプションがあります。

1. 「**[!UICONTROL Save]**」をクリックします。
