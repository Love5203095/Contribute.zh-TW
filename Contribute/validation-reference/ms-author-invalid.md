---
title: ms-author-invalid
description: Docs 組建問題 ms-author-invalid 的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 6d6c77b9b378865913e2055abf2b64ccba8ca482
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636716"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="d5288-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="d5288-103">ms-author-invalid</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="d5288-104">建議</span><span class="sxs-lookup"><span data-stu-id="d5288-104">Suggestion</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="d5288-105">解決方式</span><span class="sxs-lookup"><span data-stu-id="d5288-105">Resolution</span></span>

<span data-ttu-id="d5288-106">確認 `ms.author` 值是有效的 Microsoft 別名。</span><span class="sxs-lookup"><span data-stu-id="d5288-106">Verify that the `ms.author` value is a valid Microsoft alias.</span></span> <span data-ttu-id="d5288-107">如果別名是通訊群組清單，就也必須出現在允許清單上。</span><span class="sxs-lookup"><span data-stu-id="d5288-107">If the alias is a distribution list, it must also be on the allow list.</span></span>

<span data-ttu-id="d5288-108">您可以在[這個 Microsoft 內部網站](https://docsmetadatatool.azurewebsites.net/allowlists)找到 DL 的有效值。</span><span class="sxs-lookup"><span data-stu-id="d5288-108">Valid values for DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
