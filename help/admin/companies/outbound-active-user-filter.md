---
description: 次の手順に従って、最近アクティブなユーザーのみが含まれる、完全な同期ファイルを生成します。アクティブユーザーをフィルタリングして、関連するデータをオンサイトのターゲット設定システムにプッシュしたり、DSP に送信するファイルのサイズを制限することが必要となる場合があります。このフィルターを増分同期で使用することはできません。
seo-description: 次の手順に従って、最近アクティブなユーザーのみが含まれる、完全な同期ファイルを生成します。アクティブユーザーをフィルタリングして、関連するデータをオンサイトのターゲット設定システムにプッシュしたり、DSP に送信するファイルのサイズを制限することが必要となる場合があります。このフィルターを増分同期で使用することはできません。
seo-title: 発信データをアクティブユーザーのみにフィルタリング
title: 発信データをアクティブユーザーのみにフィルタリング
uuid: a2b4a385-eee3-458c-b978-09509cacb397
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# 発信データをアクティブユーザーのみにフィルタリング {#filter-outbound-data-by-active-users-only}

次の手順に従って、最近アクティブなユーザーのみが含まれる、完全な同期ファイルを生成します。アクティブユーザーをフィルタリングして、関連するデータをオンサイトのターゲット設定システムにプッシュしたり、DSP に送信するファイルのサイズを制限することが必要となる場合があります。このフィルターを増分同期で使用することはできません。

>[!NOTE]
>
>訪問者が「アクティブ」と見なされるために、選択した顧客サイトや広告トラフィックに訪問者を見る必要はありません。 任意の [!DNL Audience Manager] ユーザーまたはパートナーに認識されれば、「アクティブ」と認定されます。

アクティブなユーザーのみをフィルタリングするには、次の手順に従います。

1. 「**[!UICONTROL Companies]**」をクリックします。
1. Select the company you want to work with and click **[!UICONTROL Destinations]**.
1. In the [!UICONTROL Batch Data] section, set the following options:

   * **[!UICONTROL Sync Type]**:またはを **[!UICONTROL Customer]** 選択しま **[!UICONTROL Platform]**&#x200B;す。
   * **[!UICONTROL Sync Type Lookback Period]**: This time interval defines the range of your data file. 、、などを選 **[!UICONTROL 24 hours]**&#x200B;択でき **[!UICONTROL 7 days]**&#x200B;ます **[!UICONTROL 30 days]**。
   * **[!UICONTROL Incremental Sync Scheduled Run]**: Select **[!UICONTROL Never]**. このフィルターは完全同期ファイルに対してのみ適用されます。
   * **[!UICONTROL Full Sync Scheduled Run]**: This determines how often you want to receive this file. 、、、ま **[!UICONTROL 24 hours]**&#x200B;たは(無 **[!UICONTROL 7 days]**&#x200B;効にす **[!UICONTROL 30 days]**&#x200B;る場合 **[!UICONTROL Never]** )を選択できます。

1. 「**[!UICONTROL Save]**」をクリックします。
