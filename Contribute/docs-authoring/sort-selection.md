---
title: 排序選取項目 - Docs 編寫套件
description: 瞭解如何使用 Docs 編寫套件 (Visual Studio Code 延伸模組) 中的排序選取項目功能。
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: b4bd1761dc1bd9326275f011bb1935f6b695404d
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336742"
---
# <a name="sort-selection"></a>排序選取項目

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>摘要

現在，當您在 Markdown (.md *\** ) 檔案中選取部分內容時，在操作功能表中有兩個排序項目可使用。 以滑鼠右鍵按一下選取的文字即可開啟操作功能表。 您會看到類似以下的功能表項目：

:::image type="content" source="media/sort-selection-menu.png" alt-text="排序選取項目操作功能表":::

> [!TIP]
> 排序操作功能表的項目會隱藏，直到 Visual Studio Code 文字編輯器中有有效的選取項目為止。

## <a name="sort-selection-ascending-a-to-z"></a>遞增排序選取項目 (A 到 Z)

選取 [遞增排序選取項目 (A 到 Z)]  選項會將整個選取項目以遞增順序排序，從 A 到 Z 依字母順序排列。

## <a name="sort-selection-descending-z-to-a"></a>遞減排序選取項目 (Z 到 A)

選取 [遞減排序選取項目 (A 到 Z)]  選項會將整個選取項目以遞減順序排序，從 Z 到 A 依字母順序排列。

## <a name="considerations"></a>考量

功能底層的排序機制使用「自然語言」  排序。 使得它比標準排序更強大且完整。 以下列資料表來說：

```markdown
| Column1 | Column2                                |
|---------|----------------------------------------|
| 1       | Number 1                               |
| Aa      | The first letter in the alphabet       |
| Ab      | The first letter in the alphabet       |
| C       | The a letter after A in the alphabet   |
| M       | Somewhere in the middle?               |
| 2       | Number 2                               |
| X       | The alphabet letter is towards the end |
| Z       | The last letter in the alphabet        |
| 11      | Number 11                              |
```

如果沒有自然語言排序，`Column1` 的順序會是 1、11、2 等。然而實際操作則是 11 大於 2，故產生下列遞增順序：

```markdown
| Column1 | Column2                                |
|---------|----------------------------------------|
| 1       | Number 1                               |
| 2       | Number 2                               |
| 11      | Number 11                              |
| Aa      | The first letter in the alphabet       |
| Ab      | The first letter in the alphabet       |
| C       | The a letter after A in the alphabet   |
| M       | Somewhere in the middle?               |
| X       | The alphabet letter is towards the end |
| Z       | The last letter in the alphabet        |
```

## <a name="in-action"></a>操作實況

以下是這項功能的簡短示範。

[![排序選取項目示範](media/sort-selection.gif)](media/sort-selection.gif#lightbox)
