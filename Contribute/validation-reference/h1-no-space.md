---
title: h1-no-space
description: Docs 建置問題 h1-no-space 的說明和解決方式。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7058367a6edd7f663ea42a4fc2e9fafd9cbfb34f
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528963"
---
# <a name="h1-no-space"></a>h1-no-space

## <a name="warning"></a>警告

`A space is required after the hash (#) in H1.`

H1 指的是 Markdown 檔案中的第一個標題。 當發佈到 docs.microsoft.com 時，H1 會以大型字體顯示在頁面頂端。 H1 的建立方式為以單一井字 (#) 開始一行文字，其後跟隨一個空格，接著為標題文字。 井字後面若沒有空格，Docs 將無法識別 H1。

## <a name="resolution"></a>解決方式

若要修正此錯誤，請在您 H1 中井字後面新增一個空格。

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
