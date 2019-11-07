---
title: validation-timeout
description: Docs 建置問題 validation-timeout 的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9f8074d3746ea375e29704853c82f48d95273cdc
ms.sourcegitcommit: 55624c641bea5367bcfa08655c085bc950e8beae
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/30/2019
ms.locfileid: "73166783"
---
# <a name="validation-timeout"></a>validation-timeout

## <a name="warning"></a>警告

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and re-open your PR, or force a full build of your branch via https://ops.microsoft.com. Note that forcing a full build requires admin permissions to the repo. If you don’t know who your repo admin is, or if you continue to see this message after a forced build, file an issue via https://SiteHelp.`

有時候，驗證服務中的暫時性問題 (例如伺服器處於無效狀態) 會防止 Docs Build 無法成功呼叫該服務。 在幾次嘗試之後，呼叫時間會逾時，而且系統會取消驗證，以避免建置延遲及建置管線堵塞。

## <a name="resolution"></a>解決方式

請嘗試關閉並重新開啟您的 PR，或透過 [Docs 入口網站](https://ops.microsoft.com/#/)強制執行完整組建。 通常服務問題會在初始重試之後釐清其本身。

請注意，您必須是存放庫系統管理員，才能透過 Docs 入口網站強制執行組建。 若您不知道您的存放庫系統管理員是誰，或在強制執行組建後持續收到此訊息，請透過 [https://SiteHelp](https://SiteHelp) 提出問題 (若您是 Microsoft 員工)，或在 PR 中以 @ 提及文章的作者以取得協助 (若您是外部參與者)。

如果您是存放庫系統管理員，您可以強制執行完整組建，如下所示：

1. 前往 [Docs 入口網站](https://ops.microsoft.com/#/)並登入。
1. 在左上角搜尋您的存放庫並予以選取。

   :::image type="content" source="media/find-repo.png" alt-text="透過 Docs 入口網站搜尋方塊尋找您的存放庫":::
1. 在 [組建歷程記錄]  索引標籤上，按一下 [+ 手動發佈]  。
1. 選取取得警告的分支 (例如主分支)。
1. 針對 [目標]，請保留預設 **Docs 網站**。
1. 選取 [強制發佈]  核取方塊。
1. 按一下 [發佈]  。

   :::image type="content" source="media/force-build.png" alt-text="強制執行完整組建的步驟":::

這會在分支上強制執行完整組建。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
