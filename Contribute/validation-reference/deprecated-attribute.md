---
title: deprecated-attribute
description: deprecated-attribute 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 15d285159b361b7fb9dbc1774e6c4b2f5f5758ed
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236222"
---
# <a name="deprecated-attribute"></a><span data-ttu-id="b77f5-103">deprecated-attribute</span><span class="sxs-lookup"><span data-stu-id="b77f5-103">deprecated-attribute</span></span>

## <a name="warning"></a><span data-ttu-id="b77f5-104">警告</span><span class="sxs-lookup"><span data-stu-id="b77f5-104">Warning</span></span>

`Deprecated attribute: ms.component. Use ms.subservice instead.`

<span data-ttu-id="b77f5-105">使用 `ms.service`來指定雲端服務。</span><span class="sxs-lookup"><span data-stu-id="b77f5-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="b77f5-106">若要指定有關 `ms.service` 的更詳細資訊，您可以視需要指定 `ms.subservice`。</span><span class="sxs-lookup"><span data-stu-id="b77f5-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="b77f5-107">請勿使用 `ms.component`；這對此內容來說已淘汰。</span><span class="sxs-lookup"><span data-stu-id="b77f5-107">Don't use `ms.component`; it's deprecated for this content.</span></span>

## <a name="resolution"></a><span data-ttu-id="b77f5-108">解決方式</span><span class="sxs-lookup"><span data-stu-id="b77f5-108">Resolution</span></span>

<span data-ttu-id="b77f5-109">確認 `ms.service` 值對您的文章而言是正確的值。</span><span class="sxs-lookup"><span data-stu-id="b77f5-109">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="b77f5-110">然後選擇一個有效的 `ms.subservice` 值。</span><span class="sxs-lookup"><span data-stu-id="b77f5-110">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="b77f5-111">您可以在[這個 Microsoft 內部網站](https://docsmetadatatool.azurewebsites.net/allowlists)找到有效的值。</span><span class="sxs-lookup"><span data-stu-id="b77f5-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
