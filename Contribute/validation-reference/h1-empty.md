---
title: h1-empty
description: Docs 組建問題 h1-empty 的說明和解決方式。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: d0b3ab2206d66ff68a967d7868353b5b399da80a
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528798"
---
# <a name="h1-empty"></a>h1-empty

## <a name="warning"></a>警告

`H1 is required. Add content to your top-level heading.`

H1 指的是 Markdown 檔案中的第一個標題。 當發佈到 docs.microsoft.com 時，H1 會以大型字體顯示在頁面頂端。 H1 的建立方式為以單一井字 (#) 開始一行文字，其後跟隨一個空格，接著為標題文字。

## <a name="resolution"></a>解決方式

若要修正此問題，請確定您的 H1 包含內容，而不只是一個井字。

不良：

```markdown
---
author: meganbradley
ms.author: mbradley
---
#
This is not an H1
```

良好：

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
