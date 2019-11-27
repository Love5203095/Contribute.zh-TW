---
title: h1-not-first
description: Docs 組建問題 h1-not-first 的說明與解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: 09b91577f4c87125a92c0c116bc07bc7206c6833
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528923"
---
# <a name="h1-not-first"></a><span data-ttu-id="ed568-103">h1-not-first</span><span class="sxs-lookup"><span data-stu-id="ed568-103">h1-not-first</span></span>

## <a name="warning"></a><span data-ttu-id="ed568-104">警告</span><span class="sxs-lookup"><span data-stu-id="ed568-104">Warning</span></span>

`Markdown content is not allowed before H1.`

<span data-ttu-id="ed568-105">只有 YAML 中繼資料標頭可以位於 Markdown 檔案的 H1 之前。</span><span class="sxs-lookup"><span data-stu-id="ed568-105">Only the YAML metadata header can come before the H1 in a Markdown file.</span></span> <span data-ttu-id="ed568-106">例如，若希望在文章一開頭加入備註或影像，其必須位於 H1 之後。</span><span class="sxs-lookup"><span data-stu-id="ed568-106">For example, if you want to add a note or an image at the top of the article, it must come after H1.</span></span> <span data-ttu-id="ed568-107">不允許下列情況：</span><span class="sxs-lookup"><span data-stu-id="ed568-107">The following is not allowed:</span></span>

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
> [!NOTE]
> You can't do this.

# This is the H1
```

<span data-ttu-id="ed568-108">請改為執行：</span><span class="sxs-lookup"><span data-stu-id="ed568-108">Do this instead:</span></span>

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
# This is the H1

> [!NOTE]
> This is OK.
```

<span data-ttu-id="ed568-109">此問題的另一個常見原因是，在 YAML 標頭之前出現[位元組順序標記 (BOM)](http://www.websina.com/bugzero/kb/unicode-bom.html)。</span><span class="sxs-lookup"><span data-stu-id="ed568-109">Another common cause of this issue is [byte order marks (BOMs)](http://www.websina.com/bugzero/kb/unicode-bom.html) before the YAML header.</span></span> <span data-ttu-id="ed568-110">將內容認可至存放庫時，編碼問題有時候會引入這些情況。</span><span class="sxs-lookup"><span data-stu-id="ed568-110">These are sometimes introduced by encoding issues when committing content to repos.</span></span> <span data-ttu-id="ed568-111">因為如此會導致 GitHub 中轉譯不正確，因此應予以移除。</span><span class="sxs-lookup"><span data-stu-id="ed568-111">They result in bad rendering in GitHub and should be removed.</span></span>

## <a name="resolution"></a><span data-ttu-id="ed568-112">解決方式</span><span class="sxs-lookup"><span data-stu-id="ed568-112">Resolution</span></span>

<span data-ttu-id="ed568-113">移除 H1 之前 YAML 中繼資料標頭以外的所有內容。</span><span class="sxs-lookup"><span data-stu-id="ed568-113">Remove any content other than the YAML metadata header from before the H1.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
