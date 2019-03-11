---
title: internal-bookmark-not-found
description: Docs 組建問題 internal-bookmark-not-found 的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9073603d4e745db2f49b57a8901e00a03d8f570f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427226"
---
# <a name="internal-bookmark-not-found"></a><span data-ttu-id="f9399-103">internal-bookmark-not-found</span><span class="sxs-lookup"><span data-stu-id="f9399-103">internal-bookmark-not-found</span></span>

<span data-ttu-id="f9399-104">**即將推出！**</span><span class="sxs-lookup"><span data-stu-id="f9399-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="f9399-105">建議</span><span class="sxs-lookup"><span data-stu-id="f9399-105">Suggestion</span></span>

`Current file doesn't contain a bookmark named '{bookmark}'.`

<span data-ttu-id="f9399-106">您正在嘗試連結到目前檔案中不存在的標題。</span><span class="sxs-lookup"><span data-stu-id="f9399-106">You're trying to link to a heading in the current file that doesn't exist.</span></span>

## <a name="resolution"></a><span data-ttu-id="f9399-107">解決方式</span><span class="sxs-lookup"><span data-stu-id="f9399-107">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="f9399-108">確認您要連結的標題，並更新該連結。</span><span class="sxs-lookup"><span data-stu-id="f9399-108">Verify the heading you want to link to and update the link.</span></span>

<span data-ttu-id="f9399-109">若要連結到目前文章中的章節，請使用井字符號，後面接著標題文字。</span><span class="sxs-lookup"><span data-stu-id="f9399-109">To link to a section in the current article, use a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="f9399-110">移除標題中的標點符號，並以破折號取代空格。</span><span class="sxs-lookup"><span data-stu-id="f9399-110">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="f9399-111">以下是範例：</span><span class="sxs-lookup"><span data-stu-id="f9399-111">The following is an example:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
