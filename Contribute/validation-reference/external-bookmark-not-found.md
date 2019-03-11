---
title: external-bookmark-not-found
description: Docs 組建問題 external-bookmark-not-found 的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: b533a463ac38d6445ab84c74bf14b2065a0a63f3
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427214"
---
# <a name="external-bookmark-not-found"></a><span data-ttu-id="224f7-103">external-bookmark-not-found</span><span class="sxs-lookup"><span data-stu-id="224f7-103">external-bookmark-not-found</span></span>

## <a name="warning"></a><span data-ttu-id="224f7-104">警告</span><span class="sxs-lookup"><span data-stu-id="224f7-104">Warning</span></span>

`File '{file name}' doesn't contain a bookmark named '{bookmark text}'.`

<span data-ttu-id="224f7-105">您正在嘗試連結到另一個檔案中不存在的標題。</span><span class="sxs-lookup"><span data-stu-id="224f7-105">You're trying to link to a heading in another file that doesn't exist.</span></span>

## <a name="resolution"></a><span data-ttu-id="224f7-106">解決方式</span><span class="sxs-lookup"><span data-stu-id="224f7-106">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="224f7-107">檢閱您要連結的檔案，並更新您的書籤連結以指向檔案中的有效區段。</span><span class="sxs-lookup"><span data-stu-id="224f7-107">Review the file you're linking to and update your bookmark link to point to a valid section in the file.</span></span>

<span data-ttu-id="224f7-108">若要連結到另一篇文章中的章節標題，請使用檔案相對或網站相對連結加上井字符號，後面接著標題文字。</span><span class="sxs-lookup"><span data-stu-id="224f7-108">To link to a section heading in another article, use the file-relative or site-relative link plus a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="224f7-109">移除標題中的標點符號，並以破折號取代空格。</span><span class="sxs-lookup"><span data-stu-id="224f7-109">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="224f7-110">以下是範例：</span><span class="sxs-lookup"><span data-stu-id="224f7-110">The following is an example:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
