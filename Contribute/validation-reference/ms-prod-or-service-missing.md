---
title: ms-prod-or-service-missing
description: ms-prod-or-service-missing 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: f4d5bc7537ec851ce7ac1de3be2208fd74cbe37f
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713537"
---
# <a name="ms-prod-or-service-missing"></a><span data-ttu-id="7890e-103">ms-prod-or-service-missing</span><span class="sxs-lookup"><span data-stu-id="7890e-103">ms-prod-or-service-missing</span></span>

<span data-ttu-id="7890e-104">**即將推出！**</span><span class="sxs-lookup"><span data-stu-id="7890e-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="7890e-105">建議</span><span class="sxs-lookup"><span data-stu-id="7890e-105">Suggestion</span></span>

`Missing attribute: either ms.prod or ms.service is required. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a><span data-ttu-id="7890e-106">解決方式</span><span class="sxs-lookup"><span data-stu-id="7890e-106">Resolution</span></span>

<span data-ttu-id="7890e-107">需要 `ms.prod` 或 `ms.service` 其中之一，不可同時存在：`ms.prod` 用於內部部署產品；`ms.service` 則用於雲端服務。</span><span class="sxs-lookup"><span data-stu-id="7890e-107">Either `ms.prod` or `ms.service` is required, and they can't both be present: `ms.prod` is used for on-premises products; `ms.service` is used for cloud services.</span></span> <span data-ttu-id="7890e-108">請判斷哪一個適合您的文章，確認值正確，然後移除另一個欄位。</span><span class="sxs-lookup"><span data-stu-id="7890e-108">Determine which is appropriate for your article, verify that the value is correct, and remove the other field.</span></span>

<span data-ttu-id="7890e-109">您可以在[這個 Microsoft 內部網站](https://docsmetadatatool.azurewebsites.net/whitelists)找到有效的值。</span><span class="sxs-lookup"><span data-stu-id="7890e-109">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]