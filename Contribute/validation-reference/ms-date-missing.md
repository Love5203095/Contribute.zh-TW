---
title: ms-date-missing
description: ms-date-missing 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: bb352552c133a77ec003bb54f3ab0f3bddfa1be6
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236272"
---
# <a name="ms-date-missing"></a>ms-date-missing

## <a name="warning"></a>警告

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

某些內容群組需要 `ms.date` 屬性來指出「時效性」，也就是上次檢閱文章是否相關、是否正確、螢幕擷取畫面是否正確與連結是否有效的時間。 這與未明確指定 `ms.date` 時會顯示在頁面上的文章上次「發佈」  日期不同。

## <a name="resolution"></a>解決方式

確認文章為最新狀態，其中沒有任何損毀的內容，然後以 MM/DD/YYYY 格式新增有效日期：

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
