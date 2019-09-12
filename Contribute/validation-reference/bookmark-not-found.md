---
title: internal-bookmark-not-found
description: Docs 建置問題 internal-bookmark-not-found 的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 53b98f8da199e3495cc00b2388d983191268eee6
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/10/2019
ms.locfileid: "70856212"
---
# <a name="bookmark-not-found"></a><span data-ttu-id="1a1d0-103">bookmark-not-found</span><span class="sxs-lookup"><span data-stu-id="1a1d0-103">bookmark-not-found</span></span>

## <a name="warning"></a><span data-ttu-id="1a1d0-104">警告</span><span class="sxs-lookup"><span data-stu-id="1a1d0-104">Warning</span></span>

`Cannot find bookmark '{bookmark-id}' in '{parent-file}'.`

<span data-ttu-id="1a1d0-105">您正在嘗試連結到目前檔案或另一個檔案中不存在的標題。</span><span class="sxs-lookup"><span data-stu-id="1a1d0-105">You're trying to link to a heading in the current file or another file that doesn't exist.</span></span>

## <a name="resolution"></a><span data-ttu-id="1a1d0-106">解決方式</span><span class="sxs-lookup"><span data-stu-id="1a1d0-106">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="1a1d0-107">確認您要連結的標題，並更新該連結。</span><span class="sxs-lookup"><span data-stu-id="1a1d0-107">Verify the heading you want to link to and update the link.</span></span>

<span data-ttu-id="1a1d0-108">若要連結到目前文章中的章節，請使用井字符號，後面接著標題文字。</span><span class="sxs-lookup"><span data-stu-id="1a1d0-108">To link to a section in the current article, use a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="1a1d0-109">移除標題中的標點符號，並以破折號取代空格。</span><span class="sxs-lookup"><span data-stu-id="1a1d0-109">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="1a1d0-110">以下是範例：</span><span class="sxs-lookup"><span data-stu-id="1a1d0-110">The following is an example:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<span data-ttu-id="1a1d0-111">若要連結到另一個檔案中的標題，請使用該檔案的相對連結，後面接著雜湊符號和標題的文字。</span><span class="sxs-lookup"><span data-stu-id="1a1d0-111">To link to a heading in another file, use a relative link to that file, followed by a hash symbol and the words of the heading.</span></span> <span data-ttu-id="1a1d0-112">移除標題中的標點符號，並以破折號取代空格。</span><span class="sxs-lookup"><span data-stu-id="1a1d0-112">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="1a1d0-113">以下是範例：</span><span class="sxs-lookup"><span data-stu-id="1a1d0-113">The following is an example:</span></span>

```markdown
See [the Resolution section in h1-empty](h1-empty.md#resolution).
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
