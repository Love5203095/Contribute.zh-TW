---
title: ms-prod-service-mismatch
description: ms-prod-service-mismatch 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a8d1698a4842ace0e5dd07db170f40a310c666a6
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636785"
---
# <a name="ms-prod-service-mismatch"></a><span data-ttu-id="d4b65-103">ms-prod-service-mismatch</span><span class="sxs-lookup"><span data-stu-id="d4b65-103">ms-prod-service-mismatch</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="d4b65-104">建議</span><span class="sxs-lookup"><span data-stu-id="d4b65-104">Suggestion</span></span>

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

<span data-ttu-id="d4b65-105">使用 `ms.prod` 來指定內部部署產品；`ms.service` 則用於雲端服務。</span><span class="sxs-lookup"><span data-stu-id="d4b65-105">Use `ms.prod` to specify on-premises products; `ms.service` for cloud services.</span></span> <span data-ttu-id="d4b65-106">若要指定有關 `ms.prod` 的更詳細資訊，您可以視需要指定 `ms.technology`。</span><span class="sxs-lookup"><span data-stu-id="d4b65-106">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="d4b65-107">若要指定有關 `ms.service` 的更詳細資訊，您可以指定 `ms.subservice`。</span><span class="sxs-lookup"><span data-stu-id="d4b65-107">To specify more detailed information about `ms.service`, you can specify `ms.subservice`.</span></span> <span data-ttu-id="d4b65-108">您無法將 `ms.prod` 與 `ms.subservice` 搭配使用，或將 `ms.service` 與 `ms.technology`搭配使用。</span><span class="sxs-lookup"><span data-stu-id="d4b65-108">You can't use `ms.prod` with `ms.subservice` or `ms.service` with `ms.technology`.</span></span>

## <a name="resolution"></a><span data-ttu-id="d4b65-109">解決方式</span><span class="sxs-lookup"><span data-stu-id="d4b65-109">Resolution</span></span>

<span data-ttu-id="d4b65-110">首先，確認您已為文章選取正確的父屬性 (`ms.prod` 或 `ms.service`)。</span><span class="sxs-lookup"><span data-stu-id="d4b65-110">First, verify that you have selected the correct parent attribute (`ms.prod` or `ms.service`) for your article.</span></span> <span data-ttu-id="d4b65-111">接著，新增具有有效配對值的適當子欄位。</span><span class="sxs-lookup"><span data-stu-id="d4b65-111">Then, add the appropriate child field with a valid paired value.</span></span> <span data-ttu-id="d4b65-112">移除任何額外的欄位。</span><span class="sxs-lookup"><span data-stu-id="d4b65-112">Remove any extra fields.</span></span>

<span data-ttu-id="d4b65-113">您可以在[這個 Microsoft 內部網站](https://docsmetadatatool.azurewebsites.net/allowlists)找到有效的值。</span><span class="sxs-lookup"><span data-stu-id="d4b65-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
