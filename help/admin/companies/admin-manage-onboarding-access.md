---
description: 他のパートナーや顧客が所有するターゲットデータソースへのファイルやデータの誤ったオンボーディングを防ぐため、Audience Managerでは、パートナー ID(PID) と他のパートナーが所有するデータソースとのマッピング要件を追加しました。
title: セカンドパーティデータのオンボーディングアクセスの管理
source-git-commit: 6c88979f876909bc32b5238605cb4a352e327a00
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# セカンドパーティデータのオンボーディングアクセスの管理 {#manage-onboarding-access-for-second-party-data}

他のパートナーが所有するターゲットデータソースへのファイルやデータの誤ったオンボーディングを防ぐために、Audience Managerでは、他のパートナーが所有するパートナー ID(PID) とデータソース (DPID) の間にマッピング要件を追加しました。 の PID と DPID について詳しくは、 [Audience ManagerID のインデックス](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html).

セカンドパーティのデータ共有の目的で、Audience Managerのパートナーまたはお客様が、所有していないターゲットデータソースにファイルを取り込む場合、自社のパートナー ID(PID) とその特定のデータソース (DPID) の間のマッピングをリクエストする必要があります。 マッピングがない場合、ファイルは受信データジョブで処理されず、データはAudience Managerに転送されません。

そのマッピングを作成するには、Jira チケットをAudience Managerエンジニアリングチームに送信します。 Jira チケットのサンプルを表示 [ここ](https://jira.corp.adobe.com/browse/AAM-60353). 既存のデータ共有関係に対してマッピングを作成する必要はありません。
