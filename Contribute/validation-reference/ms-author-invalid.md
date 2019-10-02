---
title: ms-author-invalid
description: Docs 組建問題 ms-author-invalid 的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/27/2019
ms.prod: non-product-specific
ms.openlocfilehash: b3100b4a304356aee3c50f805628890b8c738fe1
ms.sourcegitcommit: d2f5b68b6a6d1ac902dba5063482ff5955a5b1f7
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/28/2019
ms.locfileid: "71481709"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="af4e9-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="af4e9-103">ms-author-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="af4e9-104">警告</span><span class="sxs-lookup"><span data-stu-id="af4e9-104">Warning</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="af4e9-105">解決方式</span><span class="sxs-lookup"><span data-stu-id="af4e9-105">Resolution</span></span>

<span data-ttu-id="af4e9-106">驗證 `ms.author` 值是目前作者的有效 Microsoft 別名。</span><span class="sxs-lookup"><span data-stu-id="af4e9-106">Verify that the `ms.author` value is the current author's valid Microsoft alias.</span></span> <span data-ttu-id="af4e9-107">建議使用全職員工或小組通訊群組清單 (DL) 而非短期廠商作為指定的作者。</span><span class="sxs-lookup"><span data-stu-id="af4e9-107">We recommend that the designated author be a full-time employee or team distrubution list (DL), rather than a short-term vendor.</span></span> <span data-ttu-id="af4e9-108">如果別名為 DL，它必須也在 `ms.author` 允許清單上。</span><span class="sxs-lookup"><span data-stu-id="af4e9-108">If the alias is a DL, it must also be on the `ms.author` allow list.</span></span>

<span data-ttu-id="af4e9-109">如需 `ms.author` DL 的有效值，請參閱[這個 Microsoft 內部網站](https://docsmetadatatool.azurewebsites.net/allowlists)。</span><span class="sxs-lookup"><span data-stu-id="af4e9-109">Valid values for `ms.author` DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
