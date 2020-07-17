---
description: Audience Manager の Admin ツールプロファイルの詳細情報の編集や、パスワードの変更をおこないます。
seo-description: Audience Manager の Admin ツールプロファイルの詳細情報の編集や、パスワードの変更をおこないます。
seo-title: マイプロファイル
title: マイプロファイル
uuid: ccaa611d-c855-484e-9696-081d9b4e0935
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 52%

---


# マイプロファイル {#my-profile}

Audience Manager の Admin ツールプロファイルの詳細情報の編集や、パスワードの変更をおこないます。

<!-- c_my_profile.xml -->

## プロファイルの編集 {#edit-profile}

Audience Manager の Admin ツールプロファイル（氏名、ユーザー名、電子メールアドレス、電話番号、[!UICONTROL IMS ID]、ユーザーの役割、ステータスなど）の表示と編集をおこないます。

<!-- t_edit_profile.xml -->

1. 「**[!UICONTROL My Profile]**」をクリックします。

   ![手順の結果](assets/profile.png)

2. 以下のフィールドを設定します。
   * **[!UICONTROL First Name]:**（必須）名を指定します。
   * **[!UICONTROL Last Name]:**（必須）姓を指定します。
   * **[!UICONTROL Username]:**（必須）最初のユーザー名を指定します。
   * **[!UICONTROL Email Address]:**（必須）電子メールアドレスを指定します。
   * **[!UICONTROL Phone Number]:**電話番号を指定します。
   * **[!UICONTROL IMS ID]:**インターネットメッセージサービスIDを指定します。
   * **[!UICONTROL User Roles]:**目的のユーザーの役割を選択します。
      * **[!UICONTROL DEXADMIN]:**Audience Manager管理ツールでタスクを実行するための管理者アクセス権を提供します。 このオプションを選択しない場合、個別の役割を選択できます。これらの役割を使用すると、ユーザーは[!DNL API]呼び出しを使用してタスクをおこなえますが、Admin ツールではおこなえません。
      * **[!UICONTROL CREATE_USERS]:**ユーザーは、呼び出しを使用して新しいユーザーを作成でき[!DNL API]ます。
      * **[!UICONTROL DELETE_USERS]:**ユーザーは、[!DNL API]呼び出しを使用して既存のユーザーを削除できます。
      * **[!UICONTROL EDIT_USERS]:**ユーザーは、[!DNL API]呼び出しを使用して既存のユーザーを編集できます。
      * **[!UICONTROL VIEW_USERS]:**ユーザーは、Audience Manager設定で呼び出しを使用して他のユーザーを表示でき[!DNL API]ます。
      * **[!UICONTROL CREATE_PARTNERS]:**呼び出しを使用してAudience Managerパートナーを作成でき[!DNL API]ます。
      * **[!UICONTROL DELETE_PARTNERS]:**呼び出しを使用してAudience Managerパートナーを削除でき[!DNL API]ます。
      * **[!UICONTROL EDIT_PARTNERS]:**Audience Managerは、[!DNL API]呼び出しを使用してパートナーを編集できます。
      * **[!UICONTROL VIEW_PARNTERS]:**呼び出しを使用して表示Audience Managerパートナーを[!DNL API]指定できます。
   * **[!UICONTROL Status]:**目的のステータスを選択します。
      * **[!UICONTROL Active]:**アクティブなAudience Managerユーザーにこのユーザーを指定します。
      * **[!UICONTROL Deactivated]:**オーディエンス管理で、このユーザーを非アクティブ化したユーザーにすることを指定します。
      * **[!UICONTROL Expired]:**Audience Manager内のこのユーザーのアカウントの有効期限が切れたことを指定します。
      * **[!UICONTROL Locked Out]:**Audience Manager内のこのユーザーのアカウントがロックされていることを指定します。
3. 「**[!UICONTROL Submit]**」をクリックします。

## パスワードの変更 {#change-password}

Audience Manager の Admin ツールのパスワードを変更します。

<!-- t_change_password.xml -->

1. 「**[!UICONTROL My Profile]**」をクリックします。
1. 「**[!UICONTROL Change Password]**」をクリックします。

   ![](assets/change_password.png)

   Audience Manager のパスワードは次の条件を満たしている必要があります。

   * 8 文字以上である;
   * 少なくとも 1 文字の大文字を含める。
   * 少なくとも 1 文字の小文字を含める。
   * 少なくとも 1 文字の数字を含める。
   * 少なくとも 1 文字の特殊文字を含める。
   * 先頭および末尾には英数字を使用する。
   * 先頭および末尾には英数字を使用する。

1. 元のパスワードを指定します。
1. 新しいパスワードを指定し、新しいパスワードをもう一度確認します。
1. 「**[!UICONTROL OK]**」をクリックします。