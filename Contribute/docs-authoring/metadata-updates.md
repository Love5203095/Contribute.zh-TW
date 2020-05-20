---
title: 中繼資料更新 - Docs 編寫套件
description: 瞭解如何使用 Docs 編寫套件 (Visual Studio Code 延伸模組) 來更新中繼資料。
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 391ea6c523d1f1b82b21883cea5e3428e86633e9
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336627"
---
# <a name="update-metadata"></a>更新中繼資料

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>摘要

在 Markdown (.md *\** ) 檔案中，有兩個中繼資料專用的操作功能表項目。 當您以滑鼠右鍵按一下文字編輯器中的任何位置，會看到類似以下的功能表項目：

:::image type="content" source="media/update-metadata-menu.png" alt-text="更新中繼資料操作功能表":::

## <a name="update-msdate-metadata-value"></a>更新 `ms.date` 中繼資料值

選取 [更新 `ms.date` 中繼資料值] 選項會將目前的 Markdown 檔案 `ms.date` 值設定為今天的日期。 如果文件中沒有 `ms.date` 中繼資料欄位，就不會有任何動作。

## <a name="update-implicit-metadata-values"></a>更新隱含的中繼資料值

選取 更新隱含中繼資料值  選項將會尋找並取代所有可能隱含指定的中繼資料值。 隱含的中繼資料值是在 `build/fileMetadata` 節點下的 docfx.json 檔案中指定。 `fileMetadata` 節點中的每個索引鍵值組都代表中繼資料預設值。 例如，在省略 `ms.author` 中繼資料值的 top-level/sub-folder 目錄之中的 Markdown 檔案，可以隱含地指定要在 `fileMetadata` 節點中使用的預設值。

```json
{
    "build": {
        "fileMetadata": {
            "ms.author": {
                "top-level/sub-folder/**/**.md": "dapine"
            }
        }
    }
}
```

在此案例中，所有 Markdown 檔案都會隱含地採用 `ms.author: dapine` 中繼資料值。 此功能會作用在 docfx.json  檔案中找到的這些隱含設定。 如果 Markdown 檔案包含的中繼資料和值明確設定為隱含值以外的值，便會覆寫隱含值。

請看以下 Markdown 檔案中繼資料 (Markdown 檔案位於 **top-level/sub-folder/includes/example.md**)：

```markdown
---
ms.author: someone-else
---

# Content
```

如果已在這個檔案上執行 [更新隱含的中繼資料值]  選項，再加上前述指定的 docfx.json  內容，則中繼資料值會更新為 `ms.author: dapine`。

```markdown
---
ms.author: dapine
---

# Content
```

## <a name="in-action"></a>操作實況

以下是這項功能的簡短示範。

[![更新中繼資料示範](media/update-metadata.gif)](media/update-metadata.gif#lightbox)
