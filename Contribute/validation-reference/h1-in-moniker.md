---
title: h1-in-moniker
description: Docs 組建問題 h1-in-moniker 的說明和解決方式。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: f22ce2c9e2a014e4d8bf0ae9b61fa48b11d8c9a1
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528814"
---
# <a name="h1-in-moniker"></a><span data-ttu-id="69ebe-103">h1-in-moniker</span><span class="sxs-lookup"><span data-stu-id="69ebe-103">h1-in-moniker</span></span>

## <a name="warning"></a><span data-ttu-id="69ebe-104">警告</span><span class="sxs-lookup"><span data-stu-id="69ebe-104">Warning</span></span>

`H1s are not allowed in moniker sections. Each article should have one and only one H1.`

<span data-ttu-id="69ebe-105">H1 指的是 Markdown 檔案中的第一個標題。</span><span class="sxs-lookup"><span data-stu-id="69ebe-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="69ebe-106">當發佈到 docs.microsoft.com 時，H1 會以大型字體顯示在頁面頂端。</span><span class="sxs-lookup"><span data-stu-id="69ebe-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="69ebe-107">H1 的建立方式為以單一井字 (#) 開始一行文字，其後跟隨一個空格，接著為標題文字。</span><span class="sxs-lookup"><span data-stu-id="69ebe-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="69ebe-108">您在每個檔案中只能有一個 H1。</span><span class="sxs-lookup"><span data-stu-id="69ebe-108">You can only have one H1 in each file.</span></span> <span data-ttu-id="69ebe-109">Moniker 區段中不允許 H1，因為取決於版本設定的設定方式，Moniker 中的 H1 容易造成重複或遺漏項目。</span><span class="sxs-lookup"><span data-stu-id="69ebe-109">H1s aren't allowed in moniker sections, because H1s in monikers can easily cause duplicate or missing H1s depending on how versioning is configured.</span></span>

<span data-ttu-id="69ebe-110">若 Moniker 區段包含一行組成雙底線的等號 (`=======`)，您可能也會收到此訊息。</span><span class="sxs-lookup"><span data-stu-id="69ebe-110">You might also get this message if a moniker section contains a line of equals signs making a double underline, like this: `=======`.</span></span> <span data-ttu-id="69ebe-111">這是 H1 的替代 Markdown 語法。</span><span class="sxs-lookup"><span data-stu-id="69ebe-111">This is an alternative Markdown syntax for an H1.</span></span> <span data-ttu-id="69ebe-112">在合併衝突中也經常會看到它：</span><span class="sxs-lookup"><span data-stu-id="69ebe-112">It's also commonly seen in merge conflicts:</span></span>

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

## <a name="resolution"></a><span data-ttu-id="69ebe-113">解決方式</span><span class="sxs-lookup"><span data-stu-id="69ebe-113">Resolution</span></span>

<span data-ttu-id="69ebe-114">若要修正此問題，請從所有 Moniker 區段移除 H1，並確保文章頂端的 H1 對所有 Moniker 區段均為適當。</span><span class="sxs-lookup"><span data-stu-id="69ebe-114">To fix this issue, remove H1s from all moniker sections, and make sure the H1 at the top of the article is appropriate for all moniker sections.</span></span> <span data-ttu-id="69ebe-115">請注意，不允許略過標題層級，例如在 H1 後面接著 H3。</span><span class="sxs-lookup"><span data-stu-id="69ebe-115">Note that skipping heading levels, such as following H1 with H3, isn't allowed.</span></span>

<span data-ttu-id="69ebe-116">若 Moniker 區段中的 H1 實際上是雙底線 (`=======`)，請移除它或適當地將它替換成主題標籤標頭 (例如 `##`)。</span><span class="sxs-lookup"><span data-stu-id="69ebe-116">If an H1 in a moniker section is actually a double underline (`=======`), remove it or replace it with a hashtag heading, such as `##`, as appropriate.</span></span> <span data-ttu-id="69ebe-117">若雙底線是合併衝突的一部分，請務必也移除合併衝突的開頭和結尾標記，以及已淘汰的文字。</span><span class="sxs-lookup"><span data-stu-id="69ebe-117">If the double underline is part of a merge conflict, make sure to also remove the merge conflict beginning and ending markers and the obsolete text.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
