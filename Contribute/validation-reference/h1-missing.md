---
title: h1-missing
description: Docs 組建問題 h1-missing 的說明和解決方式。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 677127d09349445bb80778dfb501d7d4294ea46b
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848458"
---
# <a name="h1-missing"></a>h1-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>建議

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

H1 指的是 Markdown 檔案中的第一個標題。 當發佈到 docs.microsoft.com 時，H1 會以大型字體顯示在頁面頂端。 H1 的建立方式為以單一井字 (#) 開始一行文字，其後跟隨一個空格，接著為標題文字。

## <a name="resolution"></a>解決方式

若要修正此問題，請新增 H1 作為您檔案中 YML 中繼資料區塊後的第一個內容：

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> 此規則不適用於包含的檔案。 如果您在包含的檔案收到 H1 警告，您很可能必須將包含的檔案移到 `includes` 資料夾中。 `includes` 資料夾可以是檔案路徑中的任何層級。 根據路徑，Docs 組建會將檔案識別為包含的檔案，而且不會執行 H1 驗證。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]