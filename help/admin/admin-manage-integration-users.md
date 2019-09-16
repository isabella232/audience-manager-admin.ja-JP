---
description: Integration Users ページを使用して、Audience Manager 設定のユーザーのリストを表示します。所定のユーザーの役割が割り当てられていれば、既存のユーザーの編集や削除、新しいユーザーの作成ができます。
seo-description: Integration Users ページを使用して、Audience Manager 設定のユーザーのリストを表示します。所定のユーザーの役割が割り当てられていれば、既存のユーザーの編集や削除、新しいユーザーの作成ができます。
seo-title: 統合ユーザー
title: 統合ユーザー
uuid: 13dcb3fb-4561-409c-84da-943d0d390cf3
translation-type: tm+mt
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
>You must have the [!UICONTROL CREATE_USER] role in order to create new users. You must have the [!UICONTROL EDIT_USER] role in order to edit existing users.

1. To create a new user, click **[!UICONTROL Integration Users]** &gt; **[!UICONTROL Create a New User]**. 既存のユーザーを編集するには、「**[!UICONTROL Username]」列で目的のユーザーをクリックします。**
2. 以下のフィールドを設定します。
   * **[!UICONTROL First Name]**: (Required) Specify the user's first name.
   * **[!UICONTROL Last Name]**: (Required) Specify the user's last name.
   * **[!UICONTROL Username]**: (Required) Specify the user's username.
   * **[!UICONTROL Email Address]**: (Required) Specify the user's email address.
   * **[!UICONTROL Phone Number]**: Specify the user's phone number.
   * **[!UICONTROL IMS ID]**:ユーザーのを指定しま [!UICONTROL Internet Messaging Service ID]す。
   * **[!UICONTROL User Roles]**: Select the desired user roles:
      * **[!UICONTROL DEXADMIN]**: Provides administrator access to perform tasks in the Audience Manager [!UICONTROL Admin] tool. このオプションを選択しない場合、個別の役割を選択できます。These roles let users perform tasks using [!DNL API] calls, but not in the Admin tool.
      * **[!UICONTROL CREATE_USERS]**: Lets users create new users using an [!DNL API] call.
      * **[!UICONTROL DELETE_USERS]**: Lets users delete existing users using an [!DNL API] call.
      * **[!UICONTROL EDIT_USERS]**: Lets users edit existing users using an [!DNL API] call.
      * **[!UICONTROL VIEW_USERS]**: Lets users view other users in your Audience Manager configuration using an [!DNL API] call.
      * **[!UICONTROL CREATE_PARTNERS]**: Lets users create Audience Manager partners using an [!DNL API] call.
      * **[!UICONTROL DELETE_PARTNERS]**: Lets users delete Audience Manager partners using an [!DNL API] call.
      * **[!UICONTROL EDIT_PARTNERS]**: Lets users edit Audience Manager partners using an [!DNL API] call.
      * **[!UICONTROL VIEW_PARNTERS]**: Lets users view Audience Manager partners using an [!DNL API] call.
   * **ステータス：**「**[!UICONTROL Active]**」を選択すると、このユーザーは Audience Manager のアクティブなユーザーとなります。
3. 「**[!UICONTROL Submit]**」をクリックします。

## ユーザーの削除 {#delete-user}

Audience Manager の ツールの [!UICONTROL Integration Users][!UICONTROL Admin] ページを使用して、既存のユーザーを削除します。

<!-- t_delete_user.xml -->

>[!NOTE]
>
>You must have the **[!UICONTROL DELETE_USER]** role in order to create new users.

1. 「**[!UICONTROL Integration Users]**」をクリックします。
2. 目的のユーザーの「![](assets/icon_delete.png)」列で **[!UICONTROL Actions]をクリックします。**
3. 「**[!UICONTROL OK]」をクリックして削除を確定します。**