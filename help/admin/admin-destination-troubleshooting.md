---
description: Audience Manager での宛先の設定と一般的な問題の解決に関する情報。
seo-description: Audience Manager での宛先の設定と一般的な問題の解決に関する情報。
seo-title: 宛先の設定に関するトラブルシューティング
title: 宛先の設定に関するトラブルシューティング
uuid: 04080fb9-6c7b-4de7-960e-54482be2de83
translation-type: tm+mt
source-git-commit: 118e8fa3f35bc77846c6518268448d57d779a2ee

---


# 宛先の設定に関するトラブルシューティング {#destination-setup-troubleshooting}

Audience Manager での宛先の設定と一般的な問題の解決に関する情報。

## 宛先を設定しましたが、ファイルが表示されません。どこにありますか？  {#destination-no-files}

<!-- c_dest_tshooting.xml -->

宛先の設定に関する一般的な問題として、次のようなものがあります。

### 宛先の設定が誤っている

* **[!UICONTROL UserID]不正な** キー：キ [!UICONTROL UserID] ーはこの宛 [!UICONTROL MasterDPID] 先のキーであり、境界を超えるID値の基になります。 Even if a [!UICONTROL UserID] key is selectable via the drop-down list, it doesn't necessarily mean that there are IDs/traits/segments mapped to this value. If the [!UICONTROL Outbound] process (which runs after destinations are created) does not find any users mapped to this [!UICONTROL UserID] key, no data will be outbounded.
* **** ファイルデータソース内にありません：リンク先のタイプを選択すると、 [!UICONTROL S2S]画面の下部にセクションが表示されます [!UICONTROL Configure Data Sources]。 このセクションが最初に表示される際には、値が選択されていません。If you forget to click the [!UICONTROL All First Party] checkbox or individually select data sources from the [!UICONTROL Available Data Sources] window, no data will be outbounded.

### 形式の設定が誤っている

送信データの形式を選択する場合は、できれば既存の形式を再利用するのが最善です。実績のある形式を使用すると、発信データを正常に生成できます。既存の形式がどのようにフォーマットされているかを正確に確認するには、メニューバーの「[!UICONTROL Formats]」オプションをクリックして、名前または ID 番号を使用して形式を検索します。形式、または形式で使用されているマクロが正しく設定されていない場合、出力が正しくフォーマットされなくなるか、情報が完全には出力されなくなります。

形式の設定とマクロの使用の詳細については、 ファ [イル形式マクロ](formats/file-formats.md#) 、 [HTTP形式マクロ](formats/web-formats.md)。

### サーバーの設定が誤っている

* **[!DNL FTP]**
   * **[!UICONTROL Domain]**
      * ホスト名のプレフィックスは入力しません。If you're given an account [!DNL ftp://hello.com], simply enter [!DNL hello.com] in this field.
   * **[!UICONTROL Port/Type Combination]**
      * For an [!DNL FTP] transfer, the preferred transfer type is [!DNL SFTP].
      * When selecting the [!DNL SFTP] type, the port is almost always 22.
      * When selecting the [!DNL FTPs/TLS] type, the port is almost always 21.
      * The [!DNL FTPs/TLS] type is not the same as a regular [!DNL FTP] transfer. We do not support regular (unsecured) [!DNL FTP] transfers.
   * **[!UICONTROL Remote Path]**
      * リモートサブパスを選択する場合、先頭にスラッシュを入力しないようにする必要があります。
      * If your transferred file is supposed to be placed in the [!DNL (root)/inbound] subfolder, simply add [!DNL inbound] for the remote path, not [!DNL /inbound].
      * パス上で複数階層下のディレクトリにあるファイルを送信する場合、各ディレクトリの間にスラッシュを入力します。の場所を指定した場合は、こ [!DNL /inbound/subdirectory1/subdirectory2]のフィールドに [!DNL inbound/subdirectory1/subdirectory2] 入力します。
      * このファイルを配置する場所が、外部サーバーにより自動的にルーティングされるディレクトリである場合は、このフィールドを空白にします。ピリオド（.）やスラッシュ（/）も含め、何も入力しないでください。

* **[!DNL S3]**
   * [!DNL S3] は、優先される転送プロトコル(または [!DNL FTP] )で [!DNL HTTP]す。
      * **[!UICONTROL Bucket]**
         * グループ名にはスラッシュ、プレフィックス、サフィックスなどを付けません。If you're given the address [!DNL s3://your-bucket] you should simply add [!DNL your-bucket] to this field.
      * **[!UICONTROL Directory]**
         * データを配置するサブディレクトリが指定されていない場合は、このフィールドを空白にします。If you're given the address [!DNL s3://your-bucket/your-subdirectory], enter [!DNL your-bucket] in the [!UICONTROL Bucket] field and [!DNL your-subdirectory] should be added into the [!UICONTROL Directory] field. 先頭にはスラッシュを追加しないでください。
         * パス上で複数階層下のディレクトリを参照する場合のみ、スラッシュを区切り記号として使用します。So a location of [!DNL s3://your-bucket/your-subdirectory1/your-subdirectory2] would have [!DNL your-bucket] in the [!UICONTROL Bucket] field and [!DNL your-subdirectory1/your-subdirectory2] entered into the [!UICONTROL Directory] field.
      * **[!UICONTROL Access / Secret Keys]**
         * When [!DNL TechOps] creates a bucket and provides access/secret keys to a consultant, those credentials are usually `READ-ONLY` credentials that are meant to be handed off to the client. これらの資格情報は「[!UICONTROL Access / Secret Key]」フィールドには入力しないでください。入力すると転送が失敗します（これらの資格情報は読み取り専用で、書き込み可能ではないため）。In the case where [!DNL TechOps] creates a bucket and provides credentials, the consultant should also request an Adobe key pair - NOT TO BE GIVEN TO THE CLIENT - that will allow for writing files to this bucket. このキーはこれらのフィールドに入力する必要があります。

* **[!DNL HTTP]**
   * **[!UICONTROL Domain]**
      * Do enter prefix information for [!DNL HTTP] entries. If you're given an account [!DNL https://superduper.com], enter [!DNL https://superduper.com] in this field.
      * **[!UICONTROL URL Prefix]**
         * When adding a [!DNL URL] prefix, leave the preceding slash off. の住所は、フィー [!DNL https://hello.com/r/x/y/z] ルドに入力し、ここに [!DNL https://hello.com] 入力する必要があり [!UICONTROL Domain][!DNL r/x/y/z][!UICONTROL URL Prefix] ます。
         * If a [!UICONTROL URL Prefix] is not needed, leave this value blank.
      * **[!UICONTROL Authentication - SSH Key]**
         * Enter the full `SSH PRIVATE` key value in this box, including headers, footers, and line breaks to ensure accurate encryption/key storage.

### 送信生成の時間が足りない

送信プロセスは 1 日に 2 回実行され、複数の処理（送信、パブリッシング、外部の場所へのプッシュなど）をファイルが最終的な宛先にプッシュされる前に実行します。データを外部の場所にプッシュする予定の 24 時間以上前に宛先を完全に設定しておくことを推奨します。

### ファイル分割サイズが大きすぎます

ファイルを宛先にバウンディングしない場合は、大きなアウトバウンドファイルをファイルチャンクに分割できます。 個々のファイルチャンクが10 GBを超えないようにします。 See also, [Outbound Data File Name: Syntax and Examples](https://docs.adobe.com/help/en/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/outbound-file-name-contents.html).


## Experience Cloud ID、顧客 ID、Audience Manager ID を送信データファイルにエクスポートするための宛先を設定する方法 {#set-up-destinations-export}

This page shows you how to set up destinations to export data keyed off the ID type you want in [!UICONTROL Outbound Data Files].

<!-- set-up-destinations-mcid-aamid.xml -->

ユーザーは宛先の設定により、自分のデータを任意の数のデジタルチャネルにわたって有効にすることができます。For example, they can export audience data to other [!DNL Adobe Experience Cloud] solutions ([!DNL Target], [!DNL Campaign], etc.). Or, they could send data to [!UICONTROL DSP]s, [!UICONTROL SSP]s, or any platform that is integrated with Audience Manager. 提携パートナーのリストは [Integrations Wiki ページ](https://wiki.corp.adobe.com/display/MCPI)にあります。

>[!NOTE]
>
>管理UIでの宛先の作成に関する詳細なチュートリアルについては、「会社の宛先を作成 [または編集](companies/admin-manage-company-destinations.md#create-edit-company-destinations) 」の記事を参照してください。

ユーザーは宛先ごとに別の ID タイプをエクスポートします。以下の図は、各 ID タイプに関連するプロファイル情報をエクスポートするために選択するオプションを示しています。さらに、[Audience Manager の ID のインデックス](https://marketing.adobe.com/resources/help/en_US/aam/ids-in-aam.html)も参照することをお勧めします。There are three important settings to consider, the [!UICONTROL User ID Key], the [!UICONTROL Data Source Type] and the [!UICONTROL Format]. 以下に詳細を示します。

* [!UICONTROL User ID Key]をインストールします。で、に [!UICONTROL Admin UI]進みます **[!UICONTROL Companies]**。 顧客の会社を検索し、クリックします。 Look for the **[!UICONTROL Destinations]** tab and press **[!UICONTROL Add Destination]**. ワークフロー **[!UICONTROL Add Destination]** で、を選択しま [!UICONTROL User ID Key]す。 The [!UICONTROL User ID Key] will filter the incoming IDs from the target data source and only allow the IDs to pass.

   ![](assets/user_id_key.PNG)

* [!UICONTROL Data Source Type]をインストールします。Audience Manager UI で宛先を作成する場合に選択します。First of all, select [!UICONTROL Inbound], then select the ID type you want. オプションは以下のとおりです。

   ![](assets/data_source_settings.PNG)

* [!UICONTROL Format]をインストールします。このオプションでは、エクスポートする形式を決定します。In the **[!UICONTROL Add Destination]** workflow, under **[!UICONTROL Batch Data]**, select the format.

形式を調べるには、に進み、 **[!UICONTROL Admin UI > Formats]** 要素を探し [!UICONTROL Data Row] ます。 この要素には、ファイル形式（以下の例では &lt;MCID&gt;）のマクロがあります。

![](assets/data_row.PNG)

<table id="table_DAEE5BC75DCB4FC690C4BAE41F627DEC"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> 設定番号 </th> 
   <th colname="col1" class="entry"> <p>ユーザーキー </p> </th> 
   <th colname="col2" class="entry"> <p>データソースタイプ </p> </th> 
   <th colname="col3" class="entry"> <p>形式 </p> </th> 
   <th colname="col4" class="entry"> <p>エクスポートする ID のタイプ </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> 1 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 2 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 3 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 4 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 5 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 6 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 7 </td> 
   <td colname="col1"> <p>DPID（会社がアクセス可能な任意のデータソース） </p> </td> 
   <td colname="col2"> <p>顧客 ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>顧客 ID（DPUUID） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 8 </td> 
   <td colname="col1"> <p>DPID（会社がアクセス可能な任意のデータソース） </p> </td> 
   <td colname="col2"> <p>顧客 ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 9 </td> 
   <td colname="col1"> <p>DPID（会社がアクセス可能な任意のデータソース） </p> </td> 
   <td colname="col2"> <p>顧客 ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 10 </td> 
   <td colname="col1"> <p>DPID（会社がアクセス可能な任意のデータソース） </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 11 </td> 
   <td colname="col1"> <p>DPID（会社がアクセス可能な任意のデータソース） </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 12 </td> 
   <td colname="col1"> <p>DPID（会社がアクセス可能な任意のデータソース） </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
 </tbody> 
</table>

## ユースケース

Let's say you use Audience Manager and [!DNL Campaign]. In order to make the customer data actionable in [!DNL Campaign], you want to export [!UICONTROL Experience Cloud IDs]. ここでは、設定番号 3 を使用します。