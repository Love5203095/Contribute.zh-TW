---
title: ms-prod-and-technology-invalid
description: ms-prod-and-technology-invalid 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 25a2b6a5bcb63388c119863ea82fb932dda4eec8
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236311"
---
# <a name="ms-prod-and-technology-invalid"></a><span data-ttu-id="2272f-103">ms-prod-and-technology-invalid</span><span class="sxs-lookup"><span data-stu-id="2272f-103">ms-prod-and-technology-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="2272f-104">警告</span><span class="sxs-lookup"><span data-stu-id="2272f-104">Warning</span></span>

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

<span data-ttu-id="2272f-105">使用 `ms.prod` 來指定內部部署產品。</span><span class="sxs-lookup"><span data-stu-id="2272f-105">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="2272f-106">若要指定有關 `ms.prod` 的更詳細資訊，您可以視需要指定 `ms.technology`。</span><span class="sxs-lookup"><span data-stu-id="2272f-106">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="2272f-107">`ms.prod` 與 `ms.technology` 的值必須是有效的配對。</span><span class="sxs-lookup"><span data-stu-id="2272f-107">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span> <span data-ttu-id="2272f-108">您的 `ms.prod` 值無效，或您的 `ms.technology` 值不是 `ms.prod` 的有效配對。</span><span class="sxs-lookup"><span data-stu-id="2272f-108">Either your `ms.prod` value is invalid, or your `ms.technology` value is not a valid pair with your `ms.prod`.</span></span>

## <a name="resolution"></a><span data-ttu-id="2272f-109">解決方式</span><span class="sxs-lookup"><span data-stu-id="2272f-109">Resolution</span></span>

<span data-ttu-id="2272f-110">確認 `ms.prod` 值對您的文章而言是正確的值。</span><span class="sxs-lookup"><span data-stu-id="2272f-110">Confirm that your `ms.prod` value is correct for your article.</span></span> <span data-ttu-id="2272f-111">然後選擇一個有效的 `ms.technology` 值。</span><span class="sxs-lookup"><span data-stu-id="2272f-111">Then choose a valid `ms.technology` value.</span></span>

<span data-ttu-id="2272f-112">您可以在[這個 Microsoft 內部網站](https://docsmetadatatool.azurewebsites.net/allowlists)找到有效的值。</span><span class="sxs-lookup"><span data-stu-id="2272f-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="2272f-113">若要要求新的值，請遵循[此程序](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master)。</span><span class="sxs-lookup"><span data-stu-id="2272f-113">To request new values, follow [this process](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
