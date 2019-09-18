---
description: Integration Users ページを使用して、Audience Manager 設定のユーザーのリストを表示します。適切な役割が割り当てられているユーザーは、既存のユーザーの編集や削除、新しいユーザーの作成ができます。
seo-description: Integration Users ページを使用して、Audience Manager 設定のユーザーのリストを表示します。適切な役割が割り当てられているユーザーは、既存のユーザーの編集や削除、新しいユーザーの作成ができます。
seo-title: 統合ユーザー
title: 統合ユーザー
uuid: 13dcb3fb-4561-409c-84da-943d0d390cf3
translation-type: ht
source-git-commit: 10adb6b06160f5a5c4068483b407e5798fc10150

---


# 統合ユーザー {#integration-users}

[!UICONTROL Integration Users] ページを使用して、Audience Manager 設定のユーザーのリストを表示します。適切な役割が割り当てられているユーザーは、既存のユーザーの編集や削除、新しいユーザーの作成ができます。

<!-- c_integration_users.xml -->

目的の列のヘッダーをクリックすると、その列を昇順または降順に並べ替えることができます。「[!UICONTROL Search]」ボックス、またはリストの最下部にあるページネーションコントロールを使用して、目的のユーザーを検索します。

## ユーザーの作成または編集 {#create-edit-user}

Audience Manager の ツールの [!UICONTROL Integration Users][!UICONTROL Admin] ページを使用して、新しいユーザーを作成するか、既存のユーザーアカウントを編集します。

<!-- t_create_user.xml -->

>[!NOTE]
>
>新しいユーザーを作成するには、[!UICONTROL CREATE_USER] の役割が必要です。既存のユーザーを編集するには、[!UICONTROL EDIT_USER] の役割が必要です。

1. 新しいユーザーを作成するには、**[!UICONTROL Integration Users]**／**[!UICONTROL Create a New User]** の順にクリックします。既存のユーザーを編集するには、「**[!UICONTROL Username]**」列で目的のユーザーをクリックします。
2. 以下のフィールドを設定します。
   * **[!UICONTROL First Name]**：（必須）ユーザーの名を指定します。
   * **[!UICONTROL Last Name]**：（必須）ユーザーの姓を指定します。
   * **[!UICONTROL Username]**：（必須）ユーザー名を指定します。
   * **[!UICONTROL Email Address]**：（必須）ユーザーの電子メールアドレスを指定します。
   * **[!UICONTROL Phone Number]**：ユーザーの電話番号を指定します。
   * **[!UICONTROL IMS ID]**：ユーザーの[!UICONTROL Internet Messaging Service ID]を指定します。
   * **[!UICONTROL User Roles]**：目的のユーザーの役割を選択します。
      * **[!UICONTROL DEXADMIN]**：Audience Manager の [!UICONTROL Admin] ツールでタスクを実行するための管理者アクセス権を付与します。このオプションを選択しない場合、個別の役割を選択できます。これらの役割を使用すると、ユーザーは [!DNL API] 呼び出しを使用してタスクをおこなえますが、Admin ツールではおこなえません。
      * **[!UICONTROL CREATE_USERS]**：ユーザーは [!DNL API] 呼び出しを使用して新しいユーザーを作成できます。
      * **[!UICONTROL DELETE_USERS]**：ユーザーは [!DNL API] 呼び出しを使用して既存のユーザーを削除できます。
      * **[!UICONTROL EDIT_USERS]**：ユーザーは [!DNL API] 呼び出しを使用して既存のユーザーを削除できます。
      * **[!UICONTROL VIEW_USERS]**：ユーザーは [!DNL API] 呼び出しを使用して、Audience Manager 構成内の他のユーザーを表示できます。
      * **[!UICONTROL CREATE_PARTNERS]**：ユーザーは [!DNL API] 呼び出しを使用して Audience Manager パートナーを作成できます。
      * **[!UICONTROL DELETE_PARTNERS]**：ユーザーは [!DNL API] 呼び出しを使用して Audience Manager パートナーを削除できます。
      * **[!UICONTROL EDIT_PARTNERS]**：ユーザーは [!DNL API] 呼び出しを使用して Audience Manager パートナーを編集できます。
      * **[!UICONTROL VIEW_PARNTERS]**：ユーザーは [!DNL API] 呼び出しを使用して Audience Manager パートナーを表示できます。
   * **ステータス：**「**[!UICONTROL Active]**」を選択すると、このユーザーは Audience Manager のアクティブなユーザーとなります。
3. 「**[!UICONTROL Submit]**」をクリックします。

## ユーザーの削除 {#delete-user}

Audience Manager [!UICONTROL Admin] の ツールの [!UICONTROL Integration Users] ページを使用して、既存のユーザーを削除します。

<!-- t_delete_user.xml -->

>[!NOTE]
>
>新しいユーザーを作成するには、**[!UICONTROL DELETE_USER]** の役割が必要です。

1. 「**[!UICONTROL Integration Users]**」をクリックします。
2. 目的のユーザーの「![](assets/icon_delete.png)」列で **[!UICONTROL Actions]** をクリックします。
3. 「**[!UICONTROL OK]**」をクリックして削除を確定します。