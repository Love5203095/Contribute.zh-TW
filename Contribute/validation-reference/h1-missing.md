---
title: h1-missing
description: Docs 組建問題 h1-missing 的說明和解決方式。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 2d0b766bba5b5ba32bff68f7ac185ab639fc7557
ms.sourcegitcommit: 7e73bef8bcdca39fd54cd79fbe8cb22da5566411
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/24/2019
ms.locfileid: "71247414"
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
> 此規則不適用於包含的檔案。 如果您在包含的檔案收到 H1 結果，您很可能必須將包含的檔案移到 `includes` 資料夾中。 `includes` 資料夾可以是檔案路徑中的任何層級。 根據路徑，Docs 組建會將檔案識別為包含的檔案，而且不會執行 H1 驗證。
>
> 父系檔案中缺少 H1s 的常見原因是誤用包含的檔案：H1 位於包含的檔案中，而不在父系檔案中。 不允許此情況，因為在包含的檔案中使用 H1 表示父系檔案中有重複的 H1s 或包含的檔案只使用一次。 H1s 在內容集中必須是唯一的，而且包含的檔案只應該用來在多個檔案之間共用內容。 若您因為 H1s 位於包含的檔案中而取得 `h1-missing` 結果，解決方式是將 H1 (與所有已包含的內容 (若已包含的檔案只使用一次)) 移動到父系檔案中。 如需有關 Docs 中包含檔案的詳細資訊，請參閱 Microsoft 內部文章[在文章中包括可重複使用的內容](https://review.docs.microsoft.com/en-us/help/contribute/includes-best-practices?branch=master).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
