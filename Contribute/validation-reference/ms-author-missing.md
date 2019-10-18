---
title: ms-author-missing
description: ms-author-missing 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: 6b313bd6b168b913d82721607126fcd4e6255009
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246244"
---
# <a name="ms-author-missing"></a><span data-ttu-id="55e0a-103">ms-author-missing</span><span class="sxs-lookup"><span data-stu-id="55e0a-103">ms-author-missing</span></span>

## <a name="warning"></a><span data-ttu-id="55e0a-104">警告</span><span class="sxs-lookup"><span data-stu-id="55e0a-104">Warning</span></span>

`Missing attribute: ms.author. Add the current author's Microsoft alias.`

## <a name="resolution"></a><span data-ttu-id="55e0a-105">解決方式</span><span class="sxs-lookup"><span data-stu-id="55e0a-105">Resolution</span></span>

<span data-ttu-id="55e0a-106">在 `ms.author` 新增目前作者的 Microsoft 別名。</span><span class="sxs-lookup"><span data-stu-id="55e0a-106">Add the current author's Microsoft alias for `ms.author`.</span></span> <span data-ttu-id="55e0a-107">請注意，如果擁有權曾經變更，這應該要是文章的「目前」  擁有者，而不是原始作者。</span><span class="sxs-lookup"><span data-stu-id="55e0a-107">Note that this should be the *current* owner of the article, not the original author if ownership has changed.</span></span> <span data-ttu-id="55e0a-108">建議使用全職員工或小組通訊群組清單 (DL) 而非短期廠商作為指定的作者。</span><span class="sxs-lookup"><span data-stu-id="55e0a-108">We recommend that the designated author be a full-time employee or team distribution list (DL), rather than a short-term vendor.</span></span> 

<span data-ttu-id="55e0a-109">如果別名為 DL，它必須也在 `ms.author` 允許清單上。</span><span class="sxs-lookup"><span data-stu-id="55e0a-109">If the alias is a DL, it must also be on the `ms.author` allow list.</span></span>

<span data-ttu-id="55e0a-110">如需 `ms.author` DL 的有效值，請參閱[這個 Microsoft 內部網站](https://docsmetadatatool.azurewebsites.net/allowlists)。</span><span class="sxs-lookup"><span data-stu-id="55e0a-110">Valid values for `ms.author` DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
