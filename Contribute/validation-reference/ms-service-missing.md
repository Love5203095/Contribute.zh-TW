---
title: ms-service-missing
description: ms-service-missing 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 2bc425726f82840565978072b2efdf13a1284ec0
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713077"
---
# <a name="ms-service-missing"></a><span data-ttu-id="443c6-103">ms-service-missing</span><span class="sxs-lookup"><span data-stu-id="443c6-103">ms-service-missing</span></span>

<span data-ttu-id="443c6-104">**即將推出！**</span><span class="sxs-lookup"><span data-stu-id="443c6-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="443c6-105">建議</span><span class="sxs-lookup"><span data-stu-id="443c6-105">Suggestion</span></span>

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

<span data-ttu-id="443c6-106">使用 `ms.service`來指定雲端服務。</span><span class="sxs-lookup"><span data-stu-id="443c6-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="443c6-107">若要指定有關 `ms.service` 的更詳細資訊，您可以視需要指定 `ms.subservice`，但如果您指定 `ms.subservice`，則必須一併指定 `ms.service`。</span><span class="sxs-lookup"><span data-stu-id="443c6-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`, but if you specify `ms.subservice`, you must also specify `ms.service`.</span></span> <span data-ttu-id="443c6-108">`ms.service` 與 `ms.subservice` 的值必須是有效的配對。</span><span class="sxs-lookup"><span data-stu-id="443c6-108">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="443c6-109">解決方式</span><span class="sxs-lookup"><span data-stu-id="443c6-109">Resolution</span></span>

<span data-ttu-id="443c6-110">確認您所指定的 `ms.subservice` 值對您的文章而言是正確的值。</span><span class="sxs-lookup"><span data-stu-id="443c6-110">Confirm that the `ms.subservice` value you've specified is correct for your article.</span></span> <span data-ttu-id="443c6-111">然後新增是 `ms.subservice` 之有效父系的適當 `ms.service` 值。</span><span class="sxs-lookup"><span data-stu-id="443c6-111">Then add the appropriate `ms.service` value that is a valid parent for the `ms.subservice`.</span></span>

<span data-ttu-id="443c6-112">您可以在[這個 Microsoft 內部網站](https://docsmetadatatool.azurewebsites.net/whitelists)找到有效的值。</span><span class="sxs-lookup"><span data-stu-id="443c6-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
