---
title: validation-timeout
description: Docs 建置問題 validation-timeout 的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: 018634b1c5fba0848fb36a70d81c46be9acf2ecd
ms.sourcegitcommit: 1e53d17639277bebd89b2e7cabeb45bdad526354
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/12/2019
ms.locfileid: "67024202"
---
# <a name="validation-timeout"></a>validation-timeout

## <a name="warning"></a>警告

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and open your PR. If you continue to see this message, file an issue via https://SiteHelp.`

有時候，驗證服務中的暫時性問題 (例如伺服器處於無效狀態) 會防止 Docs Build 無法成功呼叫該服務。 在三次嘗試之後，呼叫時間會逾時，而且系統會取消驗證，以避免建置延遲及建置管線堵塞。

## <a name="resolution"></a>解決方式

嘗試關閉並重新開啟您的 PR，或重新執行手動建置 (僅限存放庫系統管理員)。 通常服務問題會在初始重試之後釐清其本身。 若您繼續看到該訊息，請透過 [https://SiteHelp](https://SiteHelp) 建立問題 (若您是 Microsoft 員工)，或在 PR 中以 @ 方式提及文章的作者以取得協助 (若您是外部參與者)。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
