---
title: h1-empty
description: Docs 組建問題 h1-empty 的說明和解決方式。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: d0b3ab2206d66ff68a967d7868353b5b399da80a
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528798"
---
# <a name="h1-empty"></a><span data-ttu-id="9e7ed-103">h1-empty</span><span class="sxs-lookup"><span data-stu-id="9e7ed-103">h1-empty</span></span>

## <a name="warning"></a><span data-ttu-id="9e7ed-104">警告</span><span class="sxs-lookup"><span data-stu-id="9e7ed-104">Warning</span></span>

`H1 is required. Add content to your top-level heading.`

<span data-ttu-id="9e7ed-105">H1 指的是 Markdown 檔案中的第一個標題。</span><span class="sxs-lookup"><span data-stu-id="9e7ed-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="9e7ed-106">當發佈到 docs.microsoft.com 時，H1 會以大型字體顯示在頁面頂端。</span><span class="sxs-lookup"><span data-stu-id="9e7ed-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="9e7ed-107">H1 的建立方式為以單一井字 (#) 開始一行文字，其後跟隨一個空格，接著為標題文字。</span><span class="sxs-lookup"><span data-stu-id="9e7ed-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="9e7ed-108">解決方式</span><span class="sxs-lookup"><span data-stu-id="9e7ed-108">Resolution</span></span>

<span data-ttu-id="9e7ed-109">若要修正此問題，請確定您的 H1 包含內容，而不只是一個井字。</span><span class="sxs-lookup"><span data-stu-id="9e7ed-109">To fix this issue, make sure your H1 includes content, not just a hash.</span></span>

<span data-ttu-id="9e7ed-110">不良：</span><span class="sxs-lookup"><span data-stu-id="9e7ed-110">Bad:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
#
This is not an H1
```

<span data-ttu-id="9e7ed-111">良好：</span><span class="sxs-lookup"><span data-stu-id="9e7ed-111">Good:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
