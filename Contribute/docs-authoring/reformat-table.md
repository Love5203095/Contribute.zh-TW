---
title: 重新格式化 Markdown 資料表 - Docs 編寫套件
description: 瞭解如何使用 Docs 編寫套件 (Visual Studio Code 延伸模組) 中的各種 Markdown 資料表格式化功能。
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 07c95f2a0d24a49f59eaffe1bec64ee872530c2f
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336765"
---
# <a name="reformat-markdown-tables"></a>重新格式化 Markdown 資料表

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>摘要

現在，當您在 Markdown (.md *\** ) 檔案中選取一個完整的資料表時，在操作功能表中有兩個格式化項目可使用。 以滑鼠右鍵按一下選取的 Markdown資料表即可開啟操作功能表。 您會看到類似以下的功能表項目：

:::image type="content" source="media/reformat-table-menu.png" alt-text="重新格式化資料表操作功能表":::

> [!TIP]
> 這項功能**不能**用於選取多個資料表，只能適用於單一 Markdown 資料表。 您必須選取整個資料表 (包括標題)，才會同時顯示這兩個項目。

## <a name="consolidate-selected-table"></a>合併選取的資料表

選取 [合併選取的資料表]  選項會摺疊資料表標題和內容，讓每個值的兩邊只有一個空格。

## <a name="evenly-distribute-selected-table"></a>平均分配選取的資料表

選取 [平均分配選取的資料表]  選項會計算每個資料行中的最長值，並據此平均分配所有其他值的空間。

## <a name="considerations"></a>考量

此功能不會影響資料表的轉譯，但有助於改善資料表的可讀性，進而讓您更容易維護。 重新格式化資料表功能可將資料行對齊。

以下列資料表來說：

```markdown
| Column1 | This is a long column name | Column3 |  |
|--:|---------|:--:|:----|
||         |  |         |
|     |  |         |   a value      |
||         |         |         |
|     |         | This is a long value |       but why? |
|     |         |         |         |
|     |                                           |         | Here is something |
|  |         |   |         |
```

「平均分配」之後：

```markdown
| Column1 | This is a long column name | Column3              |                   |
|--------:|----------------------------|:--------------------:|:------------------|
|         |                            |                      |                   |
|         |                            |                      | a value           |
|         |                            |                      |                   |
|         |                            | This is a long value | but why?          |
|         |                            |                      |                   |
|         |                            |                      | Here is something |
|         |                            |                      |                   |
```

「合併」之後：

```markdown
| Column1 | This is a long column name | Column3 |  |
|-:|--|:-:|:-|
|  |  |  |  |
|  |  |  | a value |
|  |  |  |  |
|  |  | This is a long value | but why? |
|  |  |  |  |
|  |  |  | Here is something |
|  |  |  |  |
```

## <a name="in-action"></a>操作實況

以下是這項功能的簡短示範。

[![重新格式化資料表示範](media/reformat-table.gif)](media/reformat-table.gif#lightbox)
