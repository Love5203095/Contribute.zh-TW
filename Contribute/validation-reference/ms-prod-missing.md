---
title: ms-prod-missing
description: ms-prod-missing 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 5f0b5964dd66946f87d4535e134905db731743f2
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236280"
---
# <a name="ms-prod-missing"></a><span data-ttu-id="40f1c-103">ms-prod-missing</span><span class="sxs-lookup"><span data-stu-id="40f1c-103">ms-prod-missing</span></span>

## <a name="warning"></a><span data-ttu-id="40f1c-104">警告</span><span class="sxs-lookup"><span data-stu-id="40f1c-104">Warning</span></span>

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

<span data-ttu-id="40f1c-105">使用 `ms.prod` 來指定內部部署產品。</span><span class="sxs-lookup"><span data-stu-id="40f1c-105">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="40f1c-106">若要指定有關 `ms.prod` 的更詳細資訊，您可以視需要指定 `ms.technology`，但如果您指定 `ms.technology`，則必須一併指定 `ms.prod`。</span><span class="sxs-lookup"><span data-stu-id="40f1c-106">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`, but if you specify `ms.technology`, you must also specify `ms.prod`.</span></span> <span data-ttu-id="40f1c-107">`ms.prod` 與 `ms.technology` 的值必須是有效的配對。</span><span class="sxs-lookup"><span data-stu-id="40f1c-107">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="40f1c-108">解決方式</span><span class="sxs-lookup"><span data-stu-id="40f1c-108">Resolution</span></span>

<span data-ttu-id="40f1c-109">確認您所指定的 `ms.technology` 值對您的文章而言是正確的值。</span><span class="sxs-lookup"><span data-stu-id="40f1c-109">Confirm that the `ms.technology` value you've specified is correct for your article.</span></span> <span data-ttu-id="40f1c-110">然後新增是 `ms.technology` 之有效父系的適當 `ms.prod` 值。</span><span class="sxs-lookup"><span data-stu-id="40f1c-110">Then add the appropriate `ms.prod` value that is a valid parent for the `ms.technology`.</span></span>

<span data-ttu-id="40f1c-111">您可以在[這個 Microsoft 內部網站](https://docsmetadatatool.azurewebsites.net/allowlists)找到有效的值。</span><span class="sxs-lookup"><span data-stu-id="40f1c-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="40f1c-112">若要要求新的值，請遵循[此程序](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master)。</span><span class="sxs-lookup"><span data-stu-id="40f1c-112">To request new values, follow [this process](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
