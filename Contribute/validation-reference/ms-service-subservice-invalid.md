---
title: ms-service-and-subservice-invalid
description: ms-service-and-subservice-invalid 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a6059d592212b271780344a086ee68c7133e15cd
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236523"
---
# <a name="ms-service-and-subservice-invalid"></a><span data-ttu-id="cf24a-103">ms-service-and-subservice-invalid</span><span class="sxs-lookup"><span data-stu-id="cf24a-103">ms-service-and-subservice-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="cf24a-104">警告</span><span class="sxs-lookup"><span data-stu-id="cf24a-104">Warning</span></span>

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

<span data-ttu-id="cf24a-105">使用 `ms.service`來指定雲端服務。</span><span class="sxs-lookup"><span data-stu-id="cf24a-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="cf24a-106">若要指定有關 `ms.service` 的更詳細資訊，您可以視需要指定 `ms.subservice`。</span><span class="sxs-lookup"><span data-stu-id="cf24a-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="cf24a-107">`ms.service` 與 `ms.subservice` 的值必須是有效的配對。</span><span class="sxs-lookup"><span data-stu-id="cf24a-107">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span> <span data-ttu-id="cf24a-108">您的 `ms.service` 值無效，或您的 `ms.subservice` 值不是 `ms.service` 的有效配對。</span><span class="sxs-lookup"><span data-stu-id="cf24a-108">Either your `ms.service` value is invalid, or your `ms.subservice` value is not a valid pair with your `ms.service`.</span></span>

## <a name="resolution"></a><span data-ttu-id="cf24a-109">解決方式</span><span class="sxs-lookup"><span data-stu-id="cf24a-109">Resolution</span></span>

<span data-ttu-id="cf24a-110">確認 `ms.service` 值對您的文章而言是正確的值。</span><span class="sxs-lookup"><span data-stu-id="cf24a-110">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="cf24a-111">然後選擇一個有效的 `ms.subservice` 值。</span><span class="sxs-lookup"><span data-stu-id="cf24a-111">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="cf24a-112">您可以在[這個 Microsoft 內部網站](https://docsmetadatatool.azurewebsites.net/allowlists)找到有效的值。</span><span class="sxs-lookup"><span data-stu-id="cf24a-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="cf24a-113">若要要求新的值，請遵循[此程序](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master)。</span><span class="sxs-lookup"><span data-stu-id="cf24a-113">To request new values, follow [this process](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
