---
title: ms-author-invalid
description: Docs 組建問題 ms-author-invalid 的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 25428f93eaa7d36a5bbe35d77434ef33972e8944
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236551"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="cde93-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="cde93-103">ms-author-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="cde93-104">警告</span><span class="sxs-lookup"><span data-stu-id="cde93-104">Warning</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="cde93-105">解決方式</span><span class="sxs-lookup"><span data-stu-id="cde93-105">Resolution</span></span>

<span data-ttu-id="cde93-106">驗證 `ms.author` 值是目前作者的有效 Microsoft 別名。</span><span class="sxs-lookup"><span data-stu-id="cde93-106">Verify that the `ms.author` value is the current author's valid Microsoft alias.</span></span> <span data-ttu-id="cde93-107">如果別名是通訊群組清單，就也必須出現在允許清單上。</span><span class="sxs-lookup"><span data-stu-id="cde93-107">If the alias is a distribution list, it must also be on the allow list.</span></span>

<span data-ttu-id="cde93-108">您可以在[這個 Microsoft 內部網站](https://docsmetadatatool.azurewebsites.net/allowlists)找到 DL 的有效值。</span><span class="sxs-lookup"><span data-stu-id="cde93-108">Valid values for DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
