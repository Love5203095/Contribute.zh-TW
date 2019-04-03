---
title: deprecated-attribute
description: deprecated-attribute 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 113ca759af1765a2a51cadc721fa59743b699475
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636877"
---
# <a name="deprecated-attribute"></a><span data-ttu-id="95bb0-103">deprecated-attribute</span><span class="sxs-lookup"><span data-stu-id="95bb0-103">deprecated-attribute</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="95bb0-104">建議</span><span class="sxs-lookup"><span data-stu-id="95bb0-104">Suggestion</span></span>

`Deprecated attribute: ms.component. Use ms.subservice instead.`

<span data-ttu-id="95bb0-105">使用 `ms.service`來指定雲端服務。</span><span class="sxs-lookup"><span data-stu-id="95bb0-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="95bb0-106">若要指定有關 `ms.service` 的更詳細資訊，您可以視需要指定 `ms.subservice`。</span><span class="sxs-lookup"><span data-stu-id="95bb0-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="95bb0-107">請勿使用 `ms.component`；這對此內容來說已淘汰。</span><span class="sxs-lookup"><span data-stu-id="95bb0-107">Don't use `ms.component`; it's deprecated for this content.</span></span>

## <a name="resolution"></a><span data-ttu-id="95bb0-108">解決方式</span><span class="sxs-lookup"><span data-stu-id="95bb0-108">Resolution</span></span>

<span data-ttu-id="95bb0-109">確認 `ms.service` 值對您的文章而言是正確的值。</span><span class="sxs-lookup"><span data-stu-id="95bb0-109">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="95bb0-110">然後選擇一個有效的 `ms.subservice` 值。</span><span class="sxs-lookup"><span data-stu-id="95bb0-110">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="95bb0-111">您可以在[這個 Microsoft 內部網站](https://docsmetadatatool.azurewebsites.net/allowlists)找到有效的值。</span><span class="sxs-lookup"><span data-stu-id="95bb0-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
