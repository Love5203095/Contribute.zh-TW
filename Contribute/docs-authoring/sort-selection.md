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
# <a name="sort-selection"></a><span data-ttu-id="c281c-103">排序選取項目</span><span class="sxs-lookup"><span data-stu-id="c281c-103">Sort selection</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="c281c-104">摘要</span><span class="sxs-lookup"><span data-stu-id="c281c-104">Summary</span></span>

<span data-ttu-id="c281c-105">現在，當您在 Markdown (.md *\** ) 檔案中選取部分內容時，在操作功能表中有兩個排序項目可使用。</span><span class="sxs-lookup"><span data-stu-id="c281c-105">In a Markdown (*\*.md*) file, when you've made a selection - two sorting context menu items are now available.</span></span> <span data-ttu-id="c281c-106">以滑鼠右鍵按一下選取的文字即可開啟操作功能表。</span><span class="sxs-lookup"><span data-stu-id="c281c-106">Right-click on the selected text to open the context menu.</span></span> <span data-ttu-id="c281c-107">您會看到類似以下的功能表項目：</span><span class="sxs-lookup"><span data-stu-id="c281c-107">You will see something similar to the following menu items:</span></span>

:::image type="content" source="media/sort-selection-menu.png" alt-text="排序選取項目操作功能表":::

> [!TIP]
> <span data-ttu-id="c281c-109">排序操作功能表的項目會隱藏，直到 Visual Studio Code 文字編輯器中有有效的選取項目為止。</span><span class="sxs-lookup"><span data-stu-id="c281c-109">The sorting context menu items are hidden until there is a valid selection in the Visual Studio Code text editor.</span></span>

## <a name="sort-selection-ascending-a-to-z"></a><span data-ttu-id="c281c-110">遞增排序選取項目 (A 到 Z)</span><span class="sxs-lookup"><span data-stu-id="c281c-110">Sort selection ascending (A to Z)</span></span>

<span data-ttu-id="c281c-111">選取 [遞增排序選取項目 (A 到 Z)]  選項會將整個選取項目以遞增順序排序，從 A 到 Z 依字母順序排列。</span><span class="sxs-lookup"><span data-stu-id="c281c-111">Selecting the **Sort selection ascending (A to Z)** option will sort the entire selection ascending, alphabetically from A to Z.</span></span>

## <a name="sort-selection-descending-z-to-a"></a><span data-ttu-id="c281c-112">遞減排序選取項目 (Z 到 A)</span><span class="sxs-lookup"><span data-stu-id="c281c-112">Sort selection descending (Z to A)</span></span>

<span data-ttu-id="c281c-113">選取 [遞減排序選取項目 (A 到 Z)]  選項會將整個選取項目以遞減順序排序，從 Z 到 A 依字母順序排列。</span><span class="sxs-lookup"><span data-stu-id="c281c-113">Selecting the **Sort selection descending (Z to A)** option will sort the entire selection ascending, alphabetically from Z to A.</span></span>

## <a name="considerations"></a><span data-ttu-id="c281c-114">考量</span><span class="sxs-lookup"><span data-stu-id="c281c-114">Considerations</span></span>

<span data-ttu-id="c281c-115">功能底層的排序機制使用「自然語言」  排序。</span><span class="sxs-lookup"><span data-stu-id="c281c-115">The underlying sorting mechanism uses *natural language* sorting.</span></span> <span data-ttu-id="c281c-116">使得它比標準排序更強大且完整。</span><span class="sxs-lookup"><span data-stu-id="c281c-116">This makes it more powerful and comprehensive than standard sorting.</span></span> <span data-ttu-id="c281c-117">以下列資料表來說：</span><span class="sxs-lookup"><span data-stu-id="c281c-117">Consider the following table:</span></span>

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

<span data-ttu-id="c281c-118">如果沒有自然語言排序，`Column1` 的順序會是 1、11、2 等。然而實際操作則是 11 大於 2，故產生下列遞增順序：</span><span class="sxs-lookup"><span data-stu-id="c281c-118">Without natural language sorting, the order for `Column1` would have been 1, 11, 2, etc. but instead it understands that 11 is greater than 2 - resulting in the following ascending order:</span></span>

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

## <a name="in-action"></a><span data-ttu-id="c281c-119">操作實況</span><span class="sxs-lookup"><span data-stu-id="c281c-119">In action</span></span>

<span data-ttu-id="c281c-120">以下是這項功能的簡短示範。</span><span class="sxs-lookup"><span data-stu-id="c281c-120">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="c281c-121">[![排序選取項目示範](media/sort-selection.gif)](media/sort-selection.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="c281c-121">[![Sort selection demo](media/sort-selection.gif)](media/sort-selection.gif#lightbox)</span></span>
