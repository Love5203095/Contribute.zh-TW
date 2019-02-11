---
title: ms-service-and-subservice-invalid
description: ms-service-and-subservice-invalid 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 6a2efc5cee04d7721e7a8fe1602ca24dc09ca7fd
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713123"
---
# <a name="ms-service-and-subservice-invalid"></a><span data-ttu-id="b33c9-103">ms-service-and-subservice-invalid</span><span class="sxs-lookup"><span data-stu-id="b33c9-103">ms-service-and-subservice-invalid</span></span>

<span data-ttu-id="b33c9-104">**即將推出！**</span><span class="sxs-lookup"><span data-stu-id="b33c9-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="b33c9-105">警告</span><span class="sxs-lookup"><span data-stu-id="b33c9-105">Warning</span></span>

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

<span data-ttu-id="b33c9-106">使用 `ms.service`來指定雲端服務。</span><span class="sxs-lookup"><span data-stu-id="b33c9-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="b33c9-107">若要指定有關 `ms.service` 的更詳細資訊，您可以視需要指定 `ms.subservice`。</span><span class="sxs-lookup"><span data-stu-id="b33c9-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="b33c9-108">`ms.service` 與 `ms.subservice` 的值必須是有效的配對。</span><span class="sxs-lookup"><span data-stu-id="b33c9-108">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span> <span data-ttu-id="b33c9-109">您的 `ms.service` 值無效，或您的 `ms.subservice` 值不是 `ms.service` 的有效配對。</span><span class="sxs-lookup"><span data-stu-id="b33c9-109">Either your `ms.service` value is invalid, or your `ms.subservice` value is not a valid pair with your `ms.service`.</span></span>

## <a name="resolution"></a><span data-ttu-id="b33c9-110">解決方式</span><span class="sxs-lookup"><span data-stu-id="b33c9-110">Resolution</span></span>

<span data-ttu-id="b33c9-111">確認 `ms.service` 值對您的文章而言是正確的值。</span><span class="sxs-lookup"><span data-stu-id="b33c9-111">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="b33c9-112">然後選擇一個有效的 `ms.subservice` 值。</span><span class="sxs-lookup"><span data-stu-id="b33c9-112">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="b33c9-113">您可以在[這個 Microsoft 內部網站](https://docsmetadatatool.azurewebsites.net/whitelists)找到有效的值。</span><span class="sxs-lookup"><span data-stu-id="b33c9-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
