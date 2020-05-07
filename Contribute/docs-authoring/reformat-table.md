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
# <a name="reformat-markdown-tables"></a><span data-ttu-id="c0d83-103">重新格式化 Markdown 資料表</span><span class="sxs-lookup"><span data-stu-id="c0d83-103">Reformat Markdown tables</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="c0d83-104">摘要</span><span class="sxs-lookup"><span data-stu-id="c0d83-104">Summary</span></span>

<span data-ttu-id="c0d83-105">現在，當您在 Markdown (.md *\** ) 檔案中選取一個完整的資料表時，在操作功能表中有兩個格式化項目可使用。</span><span class="sxs-lookup"><span data-stu-id="c0d83-105">In a Markdown (*\*.md*) file, when you select a complete table - two table formatting context menu items are now available.</span></span> <span data-ttu-id="c0d83-106">以滑鼠右鍵按一下選取的 Markdown資料表即可開啟操作功能表。</span><span class="sxs-lookup"><span data-stu-id="c0d83-106">Right-click on the selected Markdown table to open the context menu.</span></span> <span data-ttu-id="c0d83-107">您會看到類似以下的功能表項目：</span><span class="sxs-lookup"><span data-stu-id="c0d83-107">You will see something similar to the following menu items:</span></span>

:::image type="content" source="media/reformat-table-menu.png" alt-text="重新格式化資料表操作功能表":::

> [!TIP]
> <span data-ttu-id="c0d83-109">這項功能**不能**用於選取多個資料表，只能適用於單一 Markdown 資料表。</span><span class="sxs-lookup"><span data-stu-id="c0d83-109">This feature **does not** work with multiple table selections, but rather is intended for a single Markdown table.</span></span> <span data-ttu-id="c0d83-110">您必須選取整個資料表 (包括標題)，才會同時顯示這兩個項目。</span><span class="sxs-lookup"><span data-stu-id="c0d83-110">You must select the entire table, including headings for desired results.</span></span>

## <a name="consolidate-selected-table"></a><span data-ttu-id="c0d83-111">合併選取的資料表</span><span class="sxs-lookup"><span data-stu-id="c0d83-111">Consolidate selected table</span></span>

<span data-ttu-id="c0d83-112">選取 [合併選取的資料表]  選項會摺疊資料表標題和內容，讓每個值的兩邊只有一個空格。</span><span class="sxs-lookup"><span data-stu-id="c0d83-112">Selecting the **Consolidate selected table** option will collapse the table headings and contents with only a single space on either side of each value.</span></span>

## <a name="evenly-distribute-selected-table"></a><span data-ttu-id="c0d83-113">平均分配選取的資料表</span><span class="sxs-lookup"><span data-stu-id="c0d83-113">Evenly distribute selected table</span></span>

<span data-ttu-id="c0d83-114">選取 [平均分配選取的資料表]  選項會計算每個資料行中的最長值，並據此平均分配所有其他值的空間。</span><span class="sxs-lookup"><span data-stu-id="c0d83-114">Selecting the **Evenly distribute selected table** option will calculate the longest value in each column and evenly distribute all the other values accordingly with space.</span></span>

## <a name="considerations"></a><span data-ttu-id="c0d83-115">考量</span><span class="sxs-lookup"><span data-stu-id="c0d83-115">Considerations</span></span>

<span data-ttu-id="c0d83-116">此功能不會影響資料表的轉譯，但有助於改善資料表的可讀性，進而讓您更容易維護。</span><span class="sxs-lookup"><span data-stu-id="c0d83-116">The feature will not impact the rendering of the table, but it will help to improve the readability of the table - thus making more maintainable.</span></span> <span data-ttu-id="c0d83-117">重新格式化資料表功能可將資料行對齊。</span><span class="sxs-lookup"><span data-stu-id="c0d83-117">The reformatting table feature will keep column alignment intact.</span></span>

<span data-ttu-id="c0d83-118">以下列資料表來說：</span><span class="sxs-lookup"><span data-stu-id="c0d83-118">Consider the following table:</span></span>

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

<span data-ttu-id="c0d83-119">「平均分配」之後：</span><span class="sxs-lookup"><span data-stu-id="c0d83-119">After being "evenly distributed":</span></span>

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

<span data-ttu-id="c0d83-120">「合併」之後：</span><span class="sxs-lookup"><span data-stu-id="c0d83-120">After being "consolidated":</span></span>

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

## <a name="in-action"></a><span data-ttu-id="c0d83-121">操作實況</span><span class="sxs-lookup"><span data-stu-id="c0d83-121">In action</span></span>

<span data-ttu-id="c0d83-122">以下是這項功能的簡短示範。</span><span class="sxs-lookup"><span data-stu-id="c0d83-122">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="c0d83-123">[![重新格式化資料表示範](media/reformat-table.gif)](media/reformat-table.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="c0d83-123">[![Reformat table demo](media/reformat-table.gif)](media/reformat-table.gif#lightbox)</span></span>
