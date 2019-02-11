---
title: ms-prod-missing
description: ms-prod-missing 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: ee29396a20345f6884a5bbc94aa25f48dafaff52
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713215"
---
# <a name="ms-prod-missing"></a><span data-ttu-id="2e74a-103">ms-prod-missing</span><span class="sxs-lookup"><span data-stu-id="2e74a-103">ms-prod-missing</span></span>

<span data-ttu-id="2e74a-104">**即將推出！**</span><span class="sxs-lookup"><span data-stu-id="2e74a-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="2e74a-105">建議</span><span class="sxs-lookup"><span data-stu-id="2e74a-105">Suggestion</span></span>

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

<span data-ttu-id="2e74a-106">使用 `ms.prod` 來指定內部部署產品。</span><span class="sxs-lookup"><span data-stu-id="2e74a-106">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="2e74a-107">若要指定有關 `ms.prod` 的更詳細資訊，您可以視需要指定 `ms.technology`，但如果您指定 `ms.technology`，則必須一併指定 `ms.prod`。</span><span class="sxs-lookup"><span data-stu-id="2e74a-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`, but if you specify `ms.technology`, you must also specify `ms.prod`.</span></span> <span data-ttu-id="2e74a-108">`ms.prod` 與 `ms.technology` 的值必須是有效的配對。</span><span class="sxs-lookup"><span data-stu-id="2e74a-108">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="2e74a-109">解決方式</span><span class="sxs-lookup"><span data-stu-id="2e74a-109">Resolution</span></span>

<span data-ttu-id="2e74a-110">確認您所指定的 `ms.technology` 值對您的文章而言是正確的值。</span><span class="sxs-lookup"><span data-stu-id="2e74a-110">Confirm that the `ms.technology` value you've specified is correct for your article.</span></span> <span data-ttu-id="2e74a-111">然後新增是 `ms.technology` 之有效父系的適當 `ms.prod` 值。</span><span class="sxs-lookup"><span data-stu-id="2e74a-111">Then add the appropriate `ms.prod` value that is a valid parent for the `ms.technology`.</span></span>

<span data-ttu-id="2e74a-112">您可以在[這個 Microsoft 內部網站](https://docsmetadatatool.azurewebsites.net/whitelists)找到有效的值。</span><span class="sxs-lookup"><span data-stu-id="2e74a-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
