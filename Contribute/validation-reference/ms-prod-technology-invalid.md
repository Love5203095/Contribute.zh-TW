---
title: ms-prod-and-technology-invalid
description: ms-prod-and-technology-invalid 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 92e8b17c3b5c96d544d12d394534a494ada3b901
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713261"
---
# <a name="ms-prod-and-technology-invalid"></a><span data-ttu-id="c5a1a-103">ms-prod-and-technology-invalid</span><span class="sxs-lookup"><span data-stu-id="c5a1a-103">ms-prod-and-technology-invalid</span></span>

<span data-ttu-id="c5a1a-104">**即將推出！**</span><span class="sxs-lookup"><span data-stu-id="c5a1a-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="c5a1a-105">警告</span><span class="sxs-lookup"><span data-stu-id="c5a1a-105">Warning</span></span>

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

<span data-ttu-id="c5a1a-106">使用 `ms.prod` 來指定內部部署產品。</span><span class="sxs-lookup"><span data-stu-id="c5a1a-106">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="c5a1a-107">若要指定有關 `ms.prod` 的更詳細資訊，您可以視需要指定 `ms.technology`。</span><span class="sxs-lookup"><span data-stu-id="c5a1a-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="c5a1a-108">`ms.prod` 與 `ms.technology` 的值必須是有效的配對。</span><span class="sxs-lookup"><span data-stu-id="c5a1a-108">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span> <span data-ttu-id="c5a1a-109">您的 `ms.prod` 值無效，或您的 `ms.technology` 值不是 `ms.prod` 的有效配對。</span><span class="sxs-lookup"><span data-stu-id="c5a1a-109">Either your `ms.prod` value is invalid, or your `ms.technology` value is not a valid pair with your `ms.prod`.</span></span>

## <a name="resolution"></a><span data-ttu-id="c5a1a-110">解決方式</span><span class="sxs-lookup"><span data-stu-id="c5a1a-110">Resolution</span></span>

<span data-ttu-id="c5a1a-111">確認 `ms.prod` 值對您的文章而言是正確的值。</span><span class="sxs-lookup"><span data-stu-id="c5a1a-111">Confirm that your `ms.prod` value is correct for your article.</span></span> <span data-ttu-id="c5a1a-112">然後選擇一個有效的 `ms.technology` 值。</span><span class="sxs-lookup"><span data-stu-id="c5a1a-112">Then choose a valid `ms.technology` value.</span></span>

<span data-ttu-id="c5a1a-113">您可以在[這個 Microsoft 內部網站](https://docsmetadatatool.azurewebsites.net/whitelists)找到有效的值。</span><span class="sxs-lookup"><span data-stu-id="c5a1a-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!-- Can we link to whitelist externally? -->

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
