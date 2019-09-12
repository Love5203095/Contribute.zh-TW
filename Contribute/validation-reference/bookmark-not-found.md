---
title: internal-bookmark-not-found
description: Docs 建置問題 internal-bookmark-not-found 的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 53b98f8da199e3495cc00b2388d983191268eee6
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/10/2019
ms.locfileid: "70856212"
---
# <a name="bookmark-not-found"></a>bookmark-not-found

## <a name="warning"></a>警告

`Cannot find bookmark '{bookmark-id}' in '{parent-file}'.`

您正在嘗試連結到目前檔案或另一個檔案中不存在的標題。

## <a name="resolution"></a>解決方式

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

確認您要連結的標題，並更新該連結。

若要連結到目前文章中的章節，請使用井字符號，後面接著標題文字。 移除標題中的標點符號，並以破折號取代空格。 以下是範例：

```markdown
[Managed Disks](#managed-disks)
```

若要連結到另一個檔案中的標題，請使用該檔案的相對連結，後面接著雜湊符號和標題的文字。 移除標題中的標點符號，並以破折號取代空格。 以下是範例：

```markdown
See [the Resolution section in h1-empty](h1-empty.md#resolution).
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
