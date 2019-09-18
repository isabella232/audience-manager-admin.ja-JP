---
description: デバイスグラフオプションは、Adobe Experience Cloud Device Co-op に加入している会社が使用できます。顧客が Audience Manager と統合されているサードパーティのデバイスグラフのプロバイダーとも契約関係にある場合、このセクションにはそのデバイスグラフのオプションが表示されます。これらのオプションは Companies／<会社名>／Profile／Device Graph Options にあります。
seo-description: デバイスグラフオプションは、Adobe Experience Cloud Device Co-op に加入している会社が使用できます。顧客が Audience Manager と統合されているサードパーティのデバイスグラフのプロバイダーとも契約関係にある場合、このセクションにはそのデバイスグラフのオプションが表示されます。これらのオプションは Companies／<会社名>／Profile／Device Graph Options にあります。
seo-title: 会社のデバイスグラフオプション
title: 会社のデバイスグラフオプション
uuid: a8ced843-710c-4a8f-a0d7-ea89d010a7a5
translation-type: ht
source-git-commit: 10adb6b06160f5a5c4068483b407e5798fc10150

---


# 会社のデバイスグラフオプション {#device-graph-options-for-companies}

[!UICONTROL Device Graph Options] は、[!DNL Adobe Experience Cloud Device Co-op] に参加する会社が利用できます。顧客が Audience Manager と統合されているサードパーティのデバイスグラフのプロバイダーとも契約関係にある場合、このセクションにはそのデバイスグラフのオプションが表示されます。これらのオプションは、[!UICONTROL Companies]／会社名／[!UICONTROL Profile]／[!UICONTROL Device Graph Options] にあります。

![](assets/adminUIdataSource.png)

この図では、サードパーティのデバイスグラフオプションの一般的な名前を使用しています。実際には、これらの名前はデバイスグラフのプロバイダーが決定するので、ここで示されているものとは異なる場合があります。例えば、[!DNL LiveRamp] オプションは通常（必ずではありません）次のようになります。

* 「[!DNL LiveRamp]」で始まる
* それぞれ異なるミドルネームが付く
* 「[!UICONTROL - Household]」または「[!UICONTROL -Person]」で終わる

## 定義されたデバイスグラフオプション {#device-graph-options-defined}

ここで選択する [!UICONTROL Device Options] により、[!DNL Audience Manager] の顧客が[!UICONTROL Profile Merge Rule] の作成時に使用できるデバイスオプションの表示と非表示が設定されます。

### Co-op Device Graph {#co-op-graph}

[Adobe Experience Cloud Device Co-op](https://marketing.adobe.com/resources/help/ja_JP/mcdc/) に参加しているお客様は、これらのオプションを使用して[決定論的データと確率論的データ](https://marketing.adobe.com/resources/help/ja_JP/mcdc/mcdc-links.html)で [!UICONTROL Profile Merge Rule] を作成します。[!DNL Corporate Provisioning Team] は、バックエンドの [!DNL API] 呼び出しを介してこのオプションをアクティブ化および非アクティブ化します。これらのボックスを [!DNL Admin UI] でオンまたはオフにすることはできません。また、「**[!UICONTROL Co-op Device Graph]**」オプションと「**[!UICONTROL Company Device Graph]**」オプションは相互に排他的です。顧客はいずれか一方のみをアクティブ化するよう要請することはできますが、両方をアクティブ化することはできません。このオプションを選択すると、**[!UICONTROL Co-op Device Graph]** コントロールが [!UICONTROL Profile Merge Rule] の [!UICONTROL Device Options] 設定に表示されます。

![](assets/adminUI1.png)

### Company Device Graph {#company-graph}

このオプションは、[!DNL Analytics] レポートスイートで「[!UICONTROL People]」指標を使用する [!DNL Analytics] ユーザー向けのものです。[!DNL Corporate Provisioning Team] は、バックエンドの [!DNL API] 呼び出しを介してこのオプションをアクティブ化および非アクティブ化します。これらのボックスを [!DNL Admin UI] でオンまたはオフにすることはできません。また、「**[!UICONTROL Company Device Graph]**」オプションと「**[!UICONTROL Co-op Device Graph]**」オプションは相互に排他的です。顧客はいずれか一方のみをアクティブ化するよう要請することはできますが、両方をアクティブ化することはできません。オンにすると、次のようになります。

* このデバイスグラフは、設定中の会社に属する決定的データ（確率的データではありません）を使用します。
* [!DNL Audience Manager] は、`*`パートナー名`*-Company Device Graph-Person`と呼ばれる [!UICONTROL Data Source] を自動的に作成します。[!UICONTROL Data Source] の詳細ページでは、[!DNL Audience Manager] のお客様はパートナー名や説明を変更し、[データ書き出しコントロール](https://marketing.adobe.com/resources/help/ja_JP/aam/c_dec.html)をこのデータソースに適用することができます。
* [!DNL Audience Manager] のお客様の場合、[!UICONTROL Profile Merge Rule] の [!UICONTROL Device Options] セクションには新しい設定が表示&#x200B;*されません*。

### LiveRamp Device Graph（「Person」または「Household」） {#liveramp-device-graph}

これらのチェックボックスは、 パートナーが [!UICONTROL Data Source] を作成し、「**[!UICONTROL Use as an Authenticated Profile]**」および／あるいは「**[!UICONTROL Use as a Device Graph]**」を選択すると [!DNL Admin UI] で有効になります。これらの設定の名前は、サードパーティのデバイスグラフのプロバイダー（[!DNL LiveRamp] や [!DNL TapAd] など）によって異なります。オンにすると、設定中の会社はこれらのデバイスグラフにより提供されるデータを使用します。

![](assets/adminUI2.png)

>[!MORE_LIKE_THIS]
>
>* [定義済みプロファイルの結合ルールオプション](https://marketing.adobe.com/resources/help/ja_JP/aam/merge-rule-definitions.html)
>* [データソースの設定とメニューオプション](https://marketing.adobe.com/resources/help/ja_JP/aam/datasource-settings-definitions.html)

