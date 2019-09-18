---
description: Audience Manager の Admin ツールプロファイルの詳細情報の編集や、パスワードの変更をおこないます。
seo-description: Audience Manager の Admin ツールプロファイルの詳細情報の編集や、パスワードの変更をおこないます。
seo-title: プロファイル
title: プロファイル
uuid: ccaa611d-c855-484e-9696-081d9b4e0935
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# マイプロファイル {#my-profile}

Audience Manager の Admin ツールプロファイルの詳細情報の編集や、パスワードの変更をおこないます。

<!-- c_my_profile.xml -->

## プロファイルの編集 {#edit-profile}

View and edit your Audience Manager Admin tool profile, including first and last name, username, email address, phone number, [!UICONTROL IMS ID], user roles, and status.

<!-- t_edit_profile.xml -->

1. 「**[!UICONTROL My Profile]**」をクリックします。

   ![手順の結果](assets/profile.png)

2. 以下のフィールドを設定します。
   * **[!UICONTROL First Name]** :（必須）名を指定します。
   * **[!UICONTROL Last Name]** :（必須）姓を指定します。
   * **[!UICONTROL Username]** :（必須）最初のユーザー名を指定します。
   * **[!UICONTROL Email Address]** :（必須）電子メールアドレスを指定します。
   * **[!UICONTROL Phone Number]** :電話番号を指定します。
   * **[!UICONTROL IMS ID]** :インターネットメッセージングサービスIDを指定します。
   * **[!UICONTROL User Roles]** :目的のユーザーの役割を選択します。
      * **[!UICONTROL DEXADMIN]** :Audience Manager管理ツールでタスクを実行するための管理者アクセス権を提供します。 このオプションを選択しない場合、個別の役割を選択できます。These roles let users perform tasks using [!DNL API] calls, but not in the Admin tool.
      * **[!UICONTROL CREATE_USERS]** :ユーザーは呼び出しを使用して新しいユーザーを作成で [!DNL API] きます。
      * **[!UICONTROL DELETE_USERS]** :ユーザーが呼び出しを使用して既存のユーザーを削除で [!DNL API] きます。
      * **[!UICONTROL EDIT_USERS]** :ユーザーは、呼び出しを使用して既存のユーザーを編集で [!DNL API] きます。
      * **[!UICONTROL VIEW_USERS]** :呼び出しを使用して、Audience Manager設定内の他のユーザーを表示で [!DNL API] きます。
      * **[!UICONTROL CREATE_PARTNERS]** :ユーザーは、呼び出しを使用してAudience Managerパートナーを作成で [!DNL API] きます。
      * **[!UICONTROL DELETE_PARTNERS]** :ユーザーは、呼び出しを使用してAudience Managerパートナーを削除で [!DNL API] きます。
      * **[!UICONTROL EDIT_PARTNERS]** :ユーザーは、呼び出しを使用してAudience Managerパートナーを編集で [!DNL API] きます。
      * **[!UICONTROL VIEW_PARNTERS]** :ユーザーは、呼び出しを使用してAudience Managerのパートナーを表示で [!DNL API] きます。
   * **[!UICONTROL Status]** :目的のステータスを選択します。
      * **[!UICONTROL Active]** :アクティブなAudience Managerユーザーにこのユーザーを設定します。
      * **[!UICONTROL Deactivated]** :このユーザーがAudience Managementで非アクティブ化されたユーザーであることを指定します。
      * **[!UICONTROL Expired]** :Audience Managerでのこのユーザーのアカウントの有効期限が切れたことを指定します。
      * **[!UICONTROL Locked Out]** :Audience Managerでのこのユーザーのアカウントをロックすることを指定します。
3. 「**[!UICONTROL Submit]**」をクリックします。

## パスワードの変更 {#change-password}

Audience Manager の Admin ツールのパスワードを変更します。

<!-- t_change_password.xml -->

1. 「**[!UICONTROL My Profile]**」をクリックします。
1. 「**[!UICONTROL Change Password]**」をクリックします。

   ![](assets/change_password.png)

   Audience Manager のパスワードは次の条件を満たしている必要があります。

   * 8 文字以上である。、
   * 大文字を少なくとも1文字含む。
   * 最低1文字の小文字を含む。
   * 少なくとも1つの数字を含む。
   * 少なくとも1つの特殊文字を含む。
   * 英数字で始まり、終わります。
   * 先頭と末尾を英数字にします。

1. 元のパスワードを指定します。
1. 新しいパスワードを指定し、新しいパスワードをもう一度確認します。
1. 「**[!UICONTROL OK]**」をクリックします。