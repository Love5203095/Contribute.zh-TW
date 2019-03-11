---
title: ms-author-invalid
description: Docs 組建問題 ms-author-invalid 的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 210ff6a18bd12585c81f461a87238aa8d20c0530
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427230"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="0c5eb-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="0c5eb-103">ms-author-invalid</span></span>

<span data-ttu-id="0c5eb-104">**即將推出！**</span><span class="sxs-lookup"><span data-stu-id="0c5eb-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="0c5eb-105">建議</span><span class="sxs-lookup"><span data-stu-id="0c5eb-105">Suggestion</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not a whitelisted distribution list.`

## <a name="resolution"></a><span data-ttu-id="0c5eb-106">解決方式</span><span class="sxs-lookup"><span data-stu-id="0c5eb-106">Resolution</span></span>

<span data-ttu-id="0c5eb-107">確認 `ms.author` 值是有效的 Microsoft 別名。</span><span class="sxs-lookup"><span data-stu-id="0c5eb-107">Verify that the `ms.author` value is a valid Microsoft alias.</span></span> <span data-ttu-id="0c5eb-108">如果別名是通訊群組清單，則也必須列入白名單。</span><span class="sxs-lookup"><span data-stu-id="0c5eb-108">If the alias is a distribution list, it must also be whitelisted.</span></span>

<span data-ttu-id="0c5eb-109">您可以在[這個 Microsoft 內部網站](https://docsmetadatatool.azurewebsites.net/whitelists)找到有效的值。</span><span class="sxs-lookup"><span data-stu-id="0c5eb-109">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
