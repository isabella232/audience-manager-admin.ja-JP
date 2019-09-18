---
description: Audience Manager の Admin ツールの Companies ページを使用して、新しい会社を作成します。
seo-description: Audience Manager の Admin ツールの Companies ページを使用して、新しい会社を作成します。
seo-title: 会社プロファイルの作成
title: 会社プロファイルの作成
uuid: 55de18f8-883d-43fe-b37f-e8805bb92f7a
translation-type: tm+mt
source-git-commit: 71bf4cec222428686c1eab0998f66887db06da68

---


# Create a Company Profile {#create-a-company-profile}

Audience Manager の Admin ツールの [!UICONTROL Companies] ページを使用して、新しい会社を作成します。

<!-- t_create_company.xml -->

>[!NOTE]
>
>You must have the **[!UICONTROL DEXADMIN]** role in order to create new companies.

1. **[!UICONTROL Companies]**／**[!UICONTROL Add Company]** をクリックします。
1. 以下のフィールドを設定します。

   * **[!UICONTROL Name]**:（必須）会社名を指定します。
   * **[!UICONTROL Description]**:（必須）業界やフルネームなど、会社に関する説明情報を入力します。
   * **[!UICONTROL Subdomain]**:（必須）会社のサブドメインを指定します。 入力するテキストは、イベント呼び出しのサブドメインとして表示されます。これは変更できません。It must be a string of [!DNL URL]-valid characters.

      For example, if your company was named [!DNL AcmeCorp], the subdomain would be [!DNL acmecorp].

      Audience Managerは、 [!UICONTROL Data Collection Server]([!UICONTROL DCS]). In the previous example, if your company's full [!DNL URL] in [!UICONTROL DCS] would be [!DNL acmecorp.demdex.net].

   * **[!UICONTROL Lifecyle]**：会社の目的のステージを指定します。
      * **[!UICONTROL Active]**：会社がアクティブな Audience Manager クライアントであることを表します。An [!UICONTROL Active] account means a paying customer, not just for consulting, but for the Audience Manager SKU.
      * **[!UICONTROL Demo]**：会社がデモ目的のみであることを表します。架空のレポートデータが自動的に作成されます。
      * **[!UICONTROL Prospect]**:無料で提供される会社や、販売デモ用のアカウント設定など、Audience Managerの見込み客 [!DNL POC] の会社を指定します。
      * **[!UICONTROL Test]**：会社が内部テスト専用であることを表します。
   * **[!UICONTROL Account Types]**：この会社のすべてのアカウントタイプを指定します。どのアカウントタイプも、他のタイプと相互に排他的ではありません。
      * **[!UICONTROL Full AAM]**：会社が完全な Adobe Audience Manager アカウントを保有し、ユーザーにログインアクセス権が付与されることを表します。
      * **[!UICONTROL MMP]**:会社が()機能の使用を有効にしているこ [!UICONTROL Master Marketing Profile] とを[!UICONTROL MMP]指定します。 The [!UICONTROL MMP] allows audiences to be shared across the Experience Cloud using an [!UICONTROL Experience Cloud ID] ([!DNL MCID]) that is assigned to every visitor and then used by Audience Manager. If you select this account type, the [!UICONTROL Experience Cloud ID Service] is also automatically selected.

         詳しくは、[オーディエンスサービス - マスターマーケティングプロファイル](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html)を参照してください。
   * **[!UICONTROL Data Source]**：会社が Audience Manager 内のサードパーティのデータプロバイダーであることを表します。
   * **[!UICONTROL Targeting Partner]**：会社が Audience Manager ユーザーのターゲティングプラットフォームとして機能することを表します。
   * **[!UICONTROL Visitor ID Service]**:会社がを使用できるようになっていることを指定しま [!UICONTROL Experience Cloud Visitor ID Service]す。

      は、Experience cloudソ [!UICONTROL Experience Cloud Visitor ID Service] リューション全体で汎用の訪問者IDを提供します。 詳細については、『[Experience Cloud 訪問者 ID サービスユーザーガイド](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-overview.html)』を参照してください。

   * **[!UICONTROL Agency]**:会社にアカウントを割り当てるように指定 [!UICONTROL Agency] します。



1. 「**[!UICONTROL Create]**」をクリックします。「会社プロファイルの編集」の [手順に従って操作します](../companies/admin-manage-company-profiles.md#edit-company-profile)。

   ![手順の結果](assets/add_company.png)

## 会社プロファイルの編集 {#edit-company-profile}

会社の名前、説明、サブドメイン、ライフサイクルなどのプロファイルを編集します。

<!-- t_edit_company_profile.xml -->

1. 「**[!UICONTROL Companies]**」をクリックし、目的の会社を検索してからクリックして、[!UICONTROL Profile] ページを表示します。

   「[!UICONTROL Search]」ボックス、またはリストの最下部にあるページネーションコントロールを使用して、目的の会社を検索します。目的の列のヘッダーをクリックすると、その列を昇順または降順に並べ替えることができます。

   ![手順の結果](assets/profile_company.png)

1. 必要に応じてフィールドを編集します。

   * **[!UICONTROL Name]**：会社の名前を編集します。これは必須フィールドです。
   * **[!UICONTROL Description]**：会社の説明を編集します。これは必須フィールドです。
   * **[!UICONTROL Subdomain]**:（必須）会社のサブドメインを指定します。 入力するテキストは、イベント呼び出しのサブドメインとして表示されます。これは変更できません。It must be a string of [!DNL URL]-valid characters.

      For example, if your company was named [!DNL AcmeCorp], the subdomain would be [!DNL acmecorp].

      Audience Managerは、()のサブドメインを [!UICONTROL Data Collection Server] 使用し[!UICONTROL DCS]ます。 In the previous example, if your company's full [!DNL URL] in [!UICONTROL DCS] would be [!DNL acmecorp.demdex.net].

   * **[!UICONTROL imsOrgld]**:([!UICONTROL Identity Management System Organization ID])このIDを使用して、会社をAdobe Experience cloudに接続できます。
   * **[!UICONTROL Lifecyle]**：会社の目的のステージを指定します。
      * **[!UICONTROL Active]**：会社がアクティブな Audience Manager クライアントであることを表します。アクティブなアカウントとは、コンサルティングだけでなく、Audience Manager SKU についても取引がある顧客を指します。
      * **[!UICONTROL Demo]**：会社がデモ目的のみであることを表します。架空のレポートデータが自動的に作成されます。
      * **[!UICONTROL Prospect]**:無料で提供される会社や、販売デモ用のアカウント設定など、Audience Managerの見込み客 [!DNL POC] の会社を指定します。
      * **[!UICONTROL Test]**：会社が内部テスト専用であることを表します。
   * **[!UICONTROL Account Types]**：この会社のすべてのアカウントタイプを指定します。どのアカウントタイプも、他のタイプと相互に排他的ではありません。
      * **[!UICONTROL Full AAM]**：会社が完全な Adobe Audience Manager アカウントを保有し、ユーザーにログインアクセス権が付与されることを表します。
      * **[!UICONTROL MMP]**:会社がマスターマーケティングプロファイル([!UICONTROL MMP])機能の使用を有効にしていることを指定します。

         If you select this account type, **[!UICONTROL Visitor ID Service]** is also automatically selected.
詳しくは、[オーディエンスサービス - マスターマーケティングプロファイル](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html)を参照してください。
   * **[!UICONTROL Data Source]**：会社が Audience Manager 内のサードパーティのデータプロバイダーであることを表します。
   * **[!UICONTROL Targeting Partner]**：会社が Audience Manager ユーザーのターゲティングプラットフォームとして機能することを表します。
   * **[!UICONTROL Visitor ID Service]**：会社が Experience Cloud 訪問者 ID サービスを使用できる状態であることを表します。

      Experience Cloud 訪問者 ID サービスは、Experience Cloud ソリューション全体に汎用の訪問者 ID を提供します。詳細については、『[Experience Cloud 訪問者 ID サービスユーザーガイド](https://microsite.omniture.com/t2/help/en_US/mcvid/mcvid_service.html)』を参照してください。

   * **[!UICONTROL Agency]**：会社がエージェンシーアカウントを保有することを表します。
   * **[!UICONTROL Features]**:目的のオプションを選択します。
      * **[!UICONTROL Password Expiration]**：この会社内のすべてのユーザーパスワードが 90 日後に期限切れになるよう設定し、Audience Manager のセキュリティを強化します。
      * **[!UICONTROL Reporting]**：この会社での Audience Manager レポートを有効にします。
      * **[!UICONTROL Role Based Access Controls]**:この会社の役割に基づくアクセス制御を有効にします。 役割ベースのアクセス制御により、アクセス権がそれぞれ異なるユーザーグループを作成できます。これらのグループ内の個々のユーザーは、Audience Manager の特定の機能にしかアクセスできません。


1. 「**[!UICONTROL Submit Updates]**」をクリックします。

## Delete a Company Profile {#delete-company-profile}

Audience Manager の ツールの [!UICONTROL Companies][!UICONTROL Admin] ページを使用して、既存の会社を削除します。

<!-- t_delete_company.xml -->

>[!NOTE]
>
>You must have the [!UICONTROL DEXADMIN] role in order to delete existing companies.

1. To delete an existing company, click **[!UICONTROL Companies]**.

   ![手順の結果](assets/companies.png)

1. Click  ![](assets/icon_delete.png) in the **[!UICONTROL Actions]** column of the desired company.
1. 「**[!UICONTROL OK]」をクリックして削除を確定します。**
