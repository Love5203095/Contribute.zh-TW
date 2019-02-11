---
title: ms-prod-and-service
description: ms-prod-and-service 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 42e6f063c8b3d97386b2655b49a19a3e103d6b3b
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713192"
---
# <a name="ms-prod-and-service"></a><span data-ttu-id="27244-103">ms-prod-and-service</span><span class="sxs-lookup"><span data-stu-id="27244-103">ms-prod-and-service</span></span>

<span data-ttu-id="27244-104">**即將推出！**</span><span class="sxs-lookup"><span data-stu-id="27244-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="27244-105">建議</span><span class="sxs-lookup"><span data-stu-id="27244-105">Suggestion</span></span>

`Both ms.prod and ms.service can't be specified. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a><span data-ttu-id="27244-106">解決方式</span><span class="sxs-lookup"><span data-stu-id="27244-106">Resolution</span></span>

<span data-ttu-id="27244-107">需要 `ms.prod` 或 `ms.service` 其中之一，不可同時存在：`ms.prod` 用於內部部署產品；`ms.service` 則用於雲端服務。</span><span class="sxs-lookup"><span data-stu-id="27244-107">Either `ms.prod` or `ms.service` is required, and they can't both be present: `ms.prod` is used for on-premises products; `ms.service` is used for cloud services.</span></span> <span data-ttu-id="27244-108">請判斷哪一個適合您的文章，確認值正確，然後移除另一個欄位。</span><span class="sxs-lookup"><span data-stu-id="27244-108">Determine which is appropriate for your article, verify that the value is correct, and remove the other field.</span></span>

<span data-ttu-id="27244-109">您可以在[這個 Microsoft 內部網站](https://docsmetadatatool.azurewebsites.net/whitelists)找到有效的值。</span><span class="sxs-lookup"><span data-stu-id="27244-109">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
