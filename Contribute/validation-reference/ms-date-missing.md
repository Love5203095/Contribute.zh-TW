---
title: ms-date-missing
description: ms-date-missing 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: f5603dee7efe5c7ce3eaa4fa944031d94a9283d8
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713238"
---
# <a name="ms-date-missing"></a>ms-date-missing

**即將推出！**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>建議

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

此日期是用來表示「時效性」，也就是上次檢閱文章是否相關、是否正確、螢幕擷取畫面是否正確及連結是否有效的時間。 這與未明確指定 `ms.date` 時會顯示在頁面上的文章上次「發佈」日期不同。

## <a name="resolution"></a>解決方式

確認文章為最新狀態，其中沒有任何損毀的內容，然後以 MM/DD/YYYY 格式新增有效日期。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
