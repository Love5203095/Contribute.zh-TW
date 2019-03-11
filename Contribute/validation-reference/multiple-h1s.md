---
title: multiple-h1
description: Docs 組建問題 multiple-h1 的說明和解決方式。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 55ce6260cb4d1e09f63e0540528576ed3fa165f8
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427238"
---
# <a name="multiple-h1"></a><span data-ttu-id="47000-103">multiple-h1</span><span class="sxs-lookup"><span data-stu-id="47000-103">multiple-h1</span></span>

## <a name="warning"></a><span data-ttu-id="47000-104">警告</span><span class="sxs-lookup"><span data-stu-id="47000-104">Warning</span></span>

`Multiple H1s are not allowed. You can only have one top-level heading.`

<span data-ttu-id="47000-105">H1 指的是 Markdown 檔案中的第一個標題。</span><span class="sxs-lookup"><span data-stu-id="47000-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="47000-106">當發佈到 docs.microsoft.com 時，H1 會以大型字體顯示在頁面頂端。</span><span class="sxs-lookup"><span data-stu-id="47000-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="47000-107">H1 的建立方式為以單一井字 (#) 開始一行文字，其後跟隨一個空格，接著為標題文字。</span><span class="sxs-lookup"><span data-stu-id="47000-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="47000-108">您在每個檔案中只能有一個 H1。</span><span class="sxs-lookup"><span data-stu-id="47000-108">You can only have one H1 in each file.</span></span>

## <a name="resolution"></a><span data-ttu-id="47000-109">解決方式</span><span class="sxs-lookup"><span data-stu-id="47000-109">Resolution</span></span>

<span data-ttu-id="47000-110">若要修正此問題，請將後續 H1 的標題層級變更為 H2 (`##`)，或重新組織您的檔案。</span><span class="sxs-lookup"><span data-stu-id="47000-110">To fix this issue, change the heading level of subsequent H1s to H2 (`##`), or otherwise reorganize your file.</span></span> <span data-ttu-id="47000-111">請注意，不允許略過標題層級，例如在 H1 後面接著 H3。</span><span class="sxs-lookup"><span data-stu-id="47000-111">Note that skipping heading levels, such as following H1 with H3, is not allowed.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1

Some content...

## This is an H2
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]