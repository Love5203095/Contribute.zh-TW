---
title: multiple-h1s
description: Docs 建置問題 multiple-h1s 的說明和解決方式。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: e2912066895494e221181f2de2bb117ff9ed1636
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528932"
---
# <a name="multiple-h1s"></a><span data-ttu-id="373b1-103">multiple-h1s</span><span class="sxs-lookup"><span data-stu-id="373b1-103">multiple-h1s</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="373b1-104">建議</span><span class="sxs-lookup"><span data-stu-id="373b1-104">Suggestion</span></span>

`Multiple H1s are not allowed. You can only have one top-level heading.`

<span data-ttu-id="373b1-105">H1 指的是 Markdown 檔案中的第一個標題。</span><span class="sxs-lookup"><span data-stu-id="373b1-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="373b1-106">當發佈到 docs.microsoft.com 時，H1 會以大型字體顯示在頁面頂端。</span><span class="sxs-lookup"><span data-stu-id="373b1-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="373b1-107">H1 的建立方式為以單一井字 (#) 開始一行文字，其後跟隨一個空格，接著為標題文字。</span><span class="sxs-lookup"><span data-stu-id="373b1-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="373b1-108">您在每個檔案中只能有一個 H1。</span><span class="sxs-lookup"><span data-stu-id="373b1-108">You can only have one H1 in each file.</span></span>

<span data-ttu-id="373b1-109">若您的文章包含一行組成雙底線的等號 (`=======`)，您可能也會收到此訊息。</span><span class="sxs-lookup"><span data-stu-id="373b1-109">You might also get this message if your article contains a line of equals signs making a double underline, like this: `=======`.</span></span> <span data-ttu-id="373b1-110">這是 H1 的替代 Markdown 語法。</span><span class="sxs-lookup"><span data-stu-id="373b1-110">This is an alternative Markdown syntax for an H1.</span></span> <span data-ttu-id="373b1-111">在合併衝突中也經常會看到它：</span><span class="sxs-lookup"><span data-stu-id="373b1-111">It's also commonly seen in merge conflicts:</span></span>

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

## <a name="resolution"></a><span data-ttu-id="373b1-112">解決方式</span><span class="sxs-lookup"><span data-stu-id="373b1-112">Resolution</span></span>

<span data-ttu-id="373b1-113">若要修正此問題，請將後續 H1 的標題層級變更為 H2 (`##`)，或重新組織您的檔案。</span><span class="sxs-lookup"><span data-stu-id="373b1-113">To fix this issue, change the heading level of subsequent H1s to H2 (`##`), or otherwise reorganize your file.</span></span> <span data-ttu-id="373b1-114">請注意，不允許略過標題層級，例如在 H1 後面接著 H3。</span><span class="sxs-lookup"><span data-stu-id="373b1-114">Note that skipping heading levels, such as following H1 with H3, isn't allowed.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1

Some content...

## This is an H2
```

<span data-ttu-id="373b1-115">若額外的 H1 實際上是雙底線 (`=======`)，請移除它或適當地將它替換成主題標籤標頭 (例如 `##`)。</span><span class="sxs-lookup"><span data-stu-id="373b1-115">If an additional H1 is actually a double underline (`=======`), remove it or replace it with a hashtag heading, such as `##`, as appropriate.</span></span> <span data-ttu-id="373b1-116">若雙底線是合併衝突的一部分，請務必也移除合併衝突的開頭和結尾標記，以及已淘汰的文字。</span><span class="sxs-lookup"><span data-stu-id="373b1-116">If the double underline is part of a merge conflict, make sure to also remove the merge conflict beginning and ending markers and the obsolete text.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
