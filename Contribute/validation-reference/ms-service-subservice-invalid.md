---
title: ms-service-and-subservice-invalid
description: ms-service-and-subservice-invalid 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 3f165d16eed7e937c7db912a9c5e0ee0809e3031
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637291"
---
# <a name="ms-service-and-subservice-invalid"></a><span data-ttu-id="b3af8-103">ms-service-and-subservice-invalid</span><span class="sxs-lookup"><span data-stu-id="b3af8-103">ms-service-and-subservice-invalid</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="b3af8-104">建議</span><span class="sxs-lookup"><span data-stu-id="b3af8-104">Suggestion</span></span>

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

<span data-ttu-id="b3af8-105">使用 `ms.service`來指定雲端服務。</span><span class="sxs-lookup"><span data-stu-id="b3af8-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="b3af8-106">若要指定有關 `ms.service` 的更詳細資訊，您可以視需要指定 `ms.subservice`。</span><span class="sxs-lookup"><span data-stu-id="b3af8-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="b3af8-107">`ms.service` 與 `ms.subservice` 的值必須是有效的配對。</span><span class="sxs-lookup"><span data-stu-id="b3af8-107">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span> <span data-ttu-id="b3af8-108">您的 `ms.service` 值無效，或您的 `ms.subservice` 值不是 `ms.service` 的有效配對。</span><span class="sxs-lookup"><span data-stu-id="b3af8-108">Either your `ms.service` value is invalid, or your `ms.subservice` value is not a valid pair with your `ms.service`.</span></span>

## <a name="resolution"></a><span data-ttu-id="b3af8-109">解決方式</span><span class="sxs-lookup"><span data-stu-id="b3af8-109">Resolution</span></span>

<span data-ttu-id="b3af8-110">確認 `ms.service` 值對您的文章而言是正確的值。</span><span class="sxs-lookup"><span data-stu-id="b3af8-110">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="b3af8-111">然後選擇一個有效的 `ms.subservice` 值。</span><span class="sxs-lookup"><span data-stu-id="b3af8-111">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="b3af8-112">您可以在[這個 Microsoft 內部網站](https://docsmetadatatool.azurewebsites.net/allowlists)找到有效的值。</span><span class="sxs-lookup"><span data-stu-id="b3af8-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
