---
title: deprecated-attribute
description: deprecated-attribute 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 564bd35c418fb9def6bf20240fca64265a477f46
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987782"
---
# <a name="deprecated-attribute"></a><span data-ttu-id="4adc6-103">deprecated-attribute</span><span class="sxs-lookup"><span data-stu-id="4adc6-103">deprecated-attribute</span></span>

<span data-ttu-id="4adc6-104">**即將推出！**</span><span class="sxs-lookup"><span data-stu-id="4adc6-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="4adc6-105">建議</span><span class="sxs-lookup"><span data-stu-id="4adc6-105">Suggestion</span></span>

`Deprecated attribute: ms.component. Use ms.subservice instead.`

<span data-ttu-id="4adc6-106">使用 `ms.service`來指定雲端服務。</span><span class="sxs-lookup"><span data-stu-id="4adc6-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="4adc6-107">若要指定有關 `ms.service` 的更詳細資訊，您可以視需要指定 `ms.subservice`。</span><span class="sxs-lookup"><span data-stu-id="4adc6-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="4adc6-108">請勿使用 `ms.component`；這對此內容來說已淘汰。</span><span class="sxs-lookup"><span data-stu-id="4adc6-108">Don't use `ms.component`; it's deprecated for this content.</span></span>

## <a name="resolution"></a><span data-ttu-id="4adc6-109">解決方式</span><span class="sxs-lookup"><span data-stu-id="4adc6-109">Resolution</span></span>

<span data-ttu-id="4adc6-110">確認 `ms.service` 值對您的文章而言是正確的值。</span><span class="sxs-lookup"><span data-stu-id="4adc6-110">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="4adc6-111">然後選擇一個有效的 `ms.subservice` 值。</span><span class="sxs-lookup"><span data-stu-id="4adc6-111">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="4adc6-112">您可以在[這個 Microsoft 內部網站](https://docsmetadatatool.azurewebsites.net/allowlists)找到有效的值。</span><span class="sxs-lookup"><span data-stu-id="4adc6-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
