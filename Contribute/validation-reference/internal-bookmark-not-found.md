---
title: internal-bookmark-not-found
description: Docs 組建問題 internal-bookmark-not-found 的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9073603d4e745db2f49b57a8901e00a03d8f570f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427226"
---
# <a name="internal-bookmark-not-found"></a>internal-bookmark-not-found

**即將推出！**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>建議

`Current file doesn't contain a bookmark named '{bookmark}'.`

您正在嘗試連結到目前檔案中不存在的標題。

## <a name="resolution"></a>解決方式

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

確認您要連結的標題，並更新該連結。

若要連結到目前文章中的章節，請使用井字符號，後面接著標題文字。 移除標題中的標點符號，並以破折號取代空格。 以下是範例：

```markdown
[Managed Disks](#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
