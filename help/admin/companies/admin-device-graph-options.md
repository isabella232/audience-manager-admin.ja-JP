---
description: デバイスグラフオプションは、Adobe Experience Cloud Device Co-op に加入している会社が使用できます。顧客が Audience Manager と統合されているサードパーティのデバイスグラフのプロバイダーとも契約関係にある場合、このセクションにはそのデバイスグラフのオプションが表示されます。これらのオプションは Companies／<会社名>／Profile／Device Graph Options にあります。
seo-description: デバイスグラフオプションは、Adobe Experience Cloud Device Co-op に加入している会社が使用できます。顧客が Audience Manager と統合されているサードパーティのデバイスグラフのプロバイダーとも契約関係にある場合、このセクションにはそのデバイスグラフのオプションが表示されます。これらのオプションは Companies／<会社名>／Profile／Device Graph Options にあります。
seo-title: 会社のデバイスグラフオプション
title: 会社のデバイスグラフオプション
uuid: a8stailed843-710c-4a8f- a0d7- ea89d010a7a5
translation-type: tm+mt
source-git-commit: 10adb6b06160f5a5c4068483b407e5798fc10150

---


# 会社のデバイスグラフオプション {#device-graph-options-for-companies}

これ [!UICONTROL Device Graph Options] は、に参加する会社で利用 [!DNL Adobe Experience Cloud Device Co-op]できます。顧客が Audience Manager と統合されているサードパーティのデバイスグラフのプロバイダーとも契約関係にある場合、このセクションにはそのデバイスグラフのオプションが表示されます。これらのオプションは [!UICONTROL Companies] 、/会社名/ [!UICONTROL Profile] &gt;にあり [!UICONTROL Device Graph Options]ます。

![](assets/adminUIdataSource.png)

この図では、サードパーティのデバイスグラフオプションの一般的な名前を使用しています。実際には、これらの名前はデバイスグラフのプロバイダーが決定するので、ここで示されているものとは異なる場合があります。For example, the [!DNL LiveRamp] options usually (but not always):

* 最初に "[!DNL LiveRamp]"
* それぞれ異なるミドルネームが付く。
* 「[!UICONTROL - Household]または」で終わる[!UICONTROL -Person]

## 定義されたデバイスグラフオプション {#device-graph-options-defined}

The device graph options you select here expose or hide the [!UICONTROL Device Options] choices available to an [!DNL Audience Manager] customer when they create a [!UICONTROL Profile Merge Rule].

### Co-op Device Graph {#co-op-graph}

[Adobe Experience Cloud Device Co- opに参加するお客様は、これらのオプション](https://marketing.adobe.com/resources/help/en_US/mcdc/) を使用して、確定的で確率的なデータ [!UICONTROL Profile Merge Rule] を使用 [して作成](https://marketing.adobe.com/resources/help/en_US/mcdc/mcdc-links.html)します。この [!DNL Corporate Provisioning Team] オプションは、バックエンド [!DNL API] 呼び出しを介してアクティブ化および非アクティブ化します。You cannot check or clear these boxes in the [!DNL Admin UI]. Also, the **[!UICONTROL Co-op Device Graph]** and **[!UICONTROL Company Device Graph]** options are mutually exclusive. 顧客はいずれか一方のみをアクティブ化するよう要請することはできますが、両方をアクティブ化することはできません。このオプションを選択すると、 **[!UICONTROL Co-op Device Graph]** コントロールの [!UICONTROL Device Options] 設定が表示 [!UICONTROL Profile Merge Rule]されます。

![](assets/adminUI1.png)

### Company Device Graph {#company-graph}

This option is for [!DNL Analytics] customers who use the [!UICONTROL People] metric in their [!DNL Analytics] report suite. この [!DNL Corporate Provisioning Team] オプションは、バックエンド [!DNL API] 呼び出しを介してアクティブ化および非アクティブ化します。You cannot check or clear these boxes in the [!DNL Admin UI]. Also, the **[!UICONTROL Company Device Graph]** and **[!UICONTROL Co-op Device Graph]** options are mutually exclusive. 顧客はいずれか一方のみをアクティブ化するよう要請することはできますが、両方をアクティブ化することはできません。オンにすると、次のようになります。

* このデバイスグラフは、設定中の会社に属する決定的データ（確率的データではありません）を使用します。
* [!DNL Audience Manager] は、自動的にパートナー名 [!UICONTROL Data Source] と呼ば `*``*-Company Device Graph-Person`れます。[!UICONTROL Data Source] ユーザーは、「[!DNL Audience Manager]」詳細ページで、パートナー名や説明を変更したり、[データエクスポートコントロール](https://marketing.adobe.com/resources/help/en_US/aam/c_dec.html)をこのデータソースに適用することができます。
* [!DNL Audience Manager] の場合、ユーザーの *セクションには新しい設定*[!UICONTROL Device Options] が表示 [!UICONTROL Profile Merge Rule]されません。

### LiveRamp Device Graph (Person or Household) {#liveramp-device-graph}

これらのチェックボックスは、パートナーが [!DNL Admin UI] 作成 [!UICONTROL Data Source] して選択または選択 **[!UICONTROL Use as an Authenticated Profile]** するときに有効になり **[!UICONTROL Use as a Device Graph]**&#x200B;ます。The names for these settings are determined by the third-party device graph provider (e.g., [!DNL LiveRamp], [!DNL TapAd], etc.). オンにすると、設定中の会社はこれらのデバイスグラフにより提供されるデータを使用します。

![](assets/adminUI2.png)

>[!MORE_LIKE_THIS]
>
>* [定義済みのプロファイルの結合ルールオプション](https://marketing.adobe.com/resources/help/en_US/aam/merge-rule-definitions.html)
>* [データソース設定とメニューオプション](https://marketing.adobe.com/resources/help/en_US/aam/datasource-settings-definitions.html)

