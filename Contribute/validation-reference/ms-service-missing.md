---
title: ms-service-missing
description: ms-service-missing 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: b50d9d6f57c953569a4e5dd873961b8c511a8bb1
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236485"
---
# <a name="ms-service-missing"></a><span data-ttu-id="71b3e-103">ms-service-missing</span><span class="sxs-lookup"><span data-stu-id="71b3e-103">ms-service-missing</span></span>

## <a name="warning"></a><span data-ttu-id="71b3e-104">警告</span><span class="sxs-lookup"><span data-stu-id="71b3e-104">Warning</span></span>

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

<span data-ttu-id="71b3e-105">使用 `ms.service`來指定雲端服務。</span><span class="sxs-lookup"><span data-stu-id="71b3e-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="71b3e-106">若要指定有關 `ms.service` 的更詳細資訊，您可以視需要指定 `ms.subservice`，但如果您指定 `ms.subservice`，則必須一併指定 `ms.service`。</span><span class="sxs-lookup"><span data-stu-id="71b3e-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`, but if you specify `ms.subservice`, you must also specify `ms.service`.</span></span> <span data-ttu-id="71b3e-107">`ms.service` 與 `ms.subservice` 的值必須是有效的配對。</span><span class="sxs-lookup"><span data-stu-id="71b3e-107">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="71b3e-108">解決方式</span><span class="sxs-lookup"><span data-stu-id="71b3e-108">Resolution</span></span>

<span data-ttu-id="71b3e-109">確認您所指定的 `ms.subservice` 值對您的文章而言是正確的值。</span><span class="sxs-lookup"><span data-stu-id="71b3e-109">Confirm that the `ms.subservice` value you've specified is correct for your article.</span></span> <span data-ttu-id="71b3e-110">然後新增是 `ms.subservice` 之有效父系的適當 `ms.service` 值。</span><span class="sxs-lookup"><span data-stu-id="71b3e-110">Then add the appropriate `ms.service` value that is a valid parent for the `ms.subservice`.</span></span>

<span data-ttu-id="71b3e-111">您可以在[這個 Microsoft 內部網站](https://docsmetadatatool.azurewebsites.net/allowlists)找到有效的值。</span><span class="sxs-lookup"><span data-stu-id="71b3e-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="71b3e-112">若要要求新的值，請遵循[此程序](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master)。</span><span class="sxs-lookup"><span data-stu-id="71b3e-112">To request new values, follow [this process](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
