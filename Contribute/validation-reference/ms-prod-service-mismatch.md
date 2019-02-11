---
title: ms-prod-service-mismatch
description: ms-prod-service-mismatch 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4a3cf8bc5435972f0442ca1d41d4147e1ea00d78
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713169"
---
# <a name="ms-prod-service-mismatch"></a><span data-ttu-id="70f0b-103">ms-prod-service-mismatch</span><span class="sxs-lookup"><span data-stu-id="70f0b-103">ms-prod-service-mismatch</span></span>

<span data-ttu-id="70f0b-104">**即將推出！**</span><span class="sxs-lookup"><span data-stu-id="70f0b-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="70f0b-105">建議</span><span class="sxs-lookup"><span data-stu-id="70f0b-105">Suggestion</span></span>

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

<span data-ttu-id="70f0b-106">使用 `ms.prod` 來指定內部部署產品；`ms.service` 則用於雲端服務。</span><span class="sxs-lookup"><span data-stu-id="70f0b-106">Use `ms.prod` to specify on-premises products; `ms.service` for cloud services.</span></span> <span data-ttu-id="70f0b-107">若要指定有關 `ms.prod` 的更詳細資訊，您可以視需要指定 `ms.technology`。</span><span class="sxs-lookup"><span data-stu-id="70f0b-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="70f0b-108">若要指定有關 `ms.service` 的更詳細資訊，您可以指定 `ms.subservice`。</span><span class="sxs-lookup"><span data-stu-id="70f0b-108">To specify more detailed information about `ms.service`, you can specify `ms.subservice`.</span></span> <span data-ttu-id="70f0b-109">您無法將 `ms.prod` 與 `ms.subservice` 搭配使用，或將 `ms.service` 與 `ms.technology`搭配使用。</span><span class="sxs-lookup"><span data-stu-id="70f0b-109">You can't use `ms.prod` with `ms.subservice` or `ms.service` with `ms.technology`.</span></span>

## <a name="resolution"></a><span data-ttu-id="70f0b-110">解決方式</span><span class="sxs-lookup"><span data-stu-id="70f0b-110">Resolution</span></span>

<span data-ttu-id="70f0b-111">首先，確認您已為文章選取正確的父屬性 (`ms.prod` 或 `ms.service`)。</span><span class="sxs-lookup"><span data-stu-id="70f0b-111">First, verify that you have selected the correct parent attribute (`ms.prod` or `ms.service`) for your article.</span></span> <span data-ttu-id="70f0b-112">接著，新增具有有效配對值的適當子欄位。</span><span class="sxs-lookup"><span data-stu-id="70f0b-112">Then, add the appropriate child field with a valid paired value.</span></span> <span data-ttu-id="70f0b-113">移除任何額外的欄位。</span><span class="sxs-lookup"><span data-stu-id="70f0b-113">Remove any extra fields.</span></span>

<span data-ttu-id="70f0b-114">您可以在[這個 Microsoft 內部網站](https://docsmetadatatool.azurewebsites.net/whitelists)找到有效的值。</span><span class="sxs-lookup"><span data-stu-id="70f0b-114">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
