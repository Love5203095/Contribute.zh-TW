---
title: ms-prod-missing
description: ms-prod-missing 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 2578ab47dab315a446529d24357e9489d7fd0bad
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987690"
---
# <a name="ms-prod-missing"></a><span data-ttu-id="dbb44-103">ms-prod-missing</span><span class="sxs-lookup"><span data-stu-id="dbb44-103">ms-prod-missing</span></span>

<span data-ttu-id="dbb44-104">**即將推出！**</span><span class="sxs-lookup"><span data-stu-id="dbb44-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="dbb44-105">建議</span><span class="sxs-lookup"><span data-stu-id="dbb44-105">Suggestion</span></span>

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

<span data-ttu-id="dbb44-106">使用 `ms.prod` 來指定內部部署產品。</span><span class="sxs-lookup"><span data-stu-id="dbb44-106">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="dbb44-107">若要指定有關 `ms.prod` 的更詳細資訊，您可以視需要指定 `ms.technology`，但如果您指定 `ms.technology`，則必須一併指定 `ms.prod`。</span><span class="sxs-lookup"><span data-stu-id="dbb44-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`, but if you specify `ms.technology`, you must also specify `ms.prod`.</span></span> <span data-ttu-id="dbb44-108">`ms.prod` 與 `ms.technology` 的值必須是有效的配對。</span><span class="sxs-lookup"><span data-stu-id="dbb44-108">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="dbb44-109">解決方式</span><span class="sxs-lookup"><span data-stu-id="dbb44-109">Resolution</span></span>

<span data-ttu-id="dbb44-110">確認您所指定的 `ms.technology` 值對您的文章而言是正確的值。</span><span class="sxs-lookup"><span data-stu-id="dbb44-110">Confirm that the `ms.technology` value you've specified is correct for your article.</span></span> <span data-ttu-id="dbb44-111">然後新增是 `ms.technology` 之有效父系的適當 `ms.prod` 值。</span><span class="sxs-lookup"><span data-stu-id="dbb44-111">Then add the appropriate `ms.prod` value that is a valid parent for the `ms.technology`.</span></span>

<span data-ttu-id="dbb44-112">您可以在[這個 Microsoft 內部網站](https://docsmetadatatool.azurewebsites.net/allowlists)找到有效的值。</span><span class="sxs-lookup"><span data-stu-id="dbb44-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
