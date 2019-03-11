---
title: external-bookmark-not-found
description: Docs 組建問題 external-bookmark-not-found 的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: b533a463ac38d6445ab84c74bf14b2065a0a63f3
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427214"
---
# <a name="external-bookmark-not-found"></a>external-bookmark-not-found

## <a name="warning"></a>警告

`File '{file name}' doesn't contain a bookmark named '{bookmark text}'.`

您正在嘗試連結到另一個檔案中不存在的標題。

## <a name="resolution"></a>解決方式

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

檢閱您要連結的檔案，並更新您的書籤連結以指向檔案中的有效區段。

若要連結到另一篇文章中的章節標題，請使用檔案相對或網站相對連結加上井字符號，後面接著標題文字。 移除標題中的標點符號，並以破折號取代空格。 以下是範例：

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
