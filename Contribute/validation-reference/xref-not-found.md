---
title: xref-not-found
description: Docs 組建問題 xref-not-found 的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: d51eace291bfac179be2701463d113c06627f92f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427234"
---
# <a name="xref-not-found"></a><span data-ttu-id="8ac9d-103">xref-not-found</span><span class="sxs-lookup"><span data-stu-id="8ac9d-103">xref-not-found</span></span>

## <a name="warning"></a><span data-ttu-id="8ac9d-104">警告</span><span class="sxs-lookup"><span data-stu-id="8ac9d-104">Warning</span></span>

`Cross reference not found: '<xref: {uid}>'.`

`Cross reference not found: '@{uid}'.`

<span data-ttu-id="8ac9d-105">您連結的 UID 不存在，或無法供您的存放庫使用。</span><span class="sxs-lookup"><span data-stu-id="8ac9d-105">The UID you linked to doesn't exist, or isn't available to your repo.</span></span>

## <a name="resolution"></a><span data-ttu-id="8ac9d-106">解決方式</span><span class="sxs-lookup"><span data-stu-id="8ac9d-106">Resolution</span></span>

<span data-ttu-id="8ac9d-107">確認 UID 正確，而且您存放庫上的 Xref 服務已正確設定，如 Microsoft 內部 [Xref 服務](https://review.docs.microsoft.com/en-us/help/onboard/admin/xref-service?branch=master)文件中所述。</span><span class="sxs-lookup"><span data-stu-id="8ac9d-107">Confirm that the UID is correct and that the Xref Service is properly configured on your repo, as described in the Microsoft-internal [Xref Service](https://review.docs.microsoft.com/en-us/help/onboard/admin/xref-service?branch=master) documentation.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
