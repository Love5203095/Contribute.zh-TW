---
title: h1-no-space
description: Docs 建置問題 h1-no-space 的說明和解決方式。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 7dd6a3d5cfc6def000d5bf7a5bf7810a16625cae
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/10/2019
ms.locfileid: "70856235"
---
# <a name="h1-no-space"></a><span data-ttu-id="10b88-103">h1-no-space</span><span class="sxs-lookup"><span data-stu-id="10b88-103">h1-no-space</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="10b88-104">建議</span><span class="sxs-lookup"><span data-stu-id="10b88-104">Suggestion</span></span>

`A space is required after the hash (#) in H1.`

<span data-ttu-id="10b88-105">H1 指的是 Markdown 檔案中的第一個標題。</span><span class="sxs-lookup"><span data-stu-id="10b88-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="10b88-106">當發佈到 docs.microsoft.com 時，H1 會以大型字體顯示在頁面頂端。</span><span class="sxs-lookup"><span data-stu-id="10b88-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="10b88-107">H1 的建立方式為以單一井字 (#) 開始一行文字，其後跟隨一個空格，接著為標題文字。</span><span class="sxs-lookup"><span data-stu-id="10b88-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="10b88-108">井字後面若沒有空格，Docs 將無法識別 H1。</span><span class="sxs-lookup"><span data-stu-id="10b88-108">Without the space after the hash, Docs will not recognize an H1.</span></span>

## <a name="resolution"></a><span data-ttu-id="10b88-109">解決方式</span><span class="sxs-lookup"><span data-stu-id="10b88-109">Resolution</span></span>

<span data-ttu-id="10b88-110">若要修正此錯誤，請在您 H1 中井字後面新增一個空格。</span><span class="sxs-lookup"><span data-stu-id="10b88-110">To fix this error, add a space after the hash in your H1.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
