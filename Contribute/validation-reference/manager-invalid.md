---
title: manager-invalid
description: Docs 組建問題 manager-invalid 的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 44174bde29b63bffe709596f9c2d6be994f252a3
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637222"
---
# <a name="manager-invalid"></a><span data-ttu-id="efa1c-103">manager-invalid</span><span class="sxs-lookup"><span data-stu-id="efa1c-103">manager-invalid</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="efa1c-104">建議</span><span class="sxs-lookup"><span data-stu-id="efa1c-104">Suggestion</span></span>

`Invalid value for manager: '{value}' is not a valid Microsoft alias.`

<span data-ttu-id="efa1c-105">某些內容群組需要 `manager` 屬性以識別作者的經理。</span><span class="sxs-lookup"><span data-stu-id="efa1c-105">Some content groups require the `manager` attribute to identify the author's manager.</span></span>

## <a name="resolution"></a><span data-ttu-id="efa1c-106">解決方式</span><span class="sxs-lookup"><span data-stu-id="efa1c-106">Resolution</span></span>

<span data-ttu-id="efa1c-107">`manager` 的值必須是個別 Microsoft 員工的有效別名。</span><span class="sxs-lookup"><span data-stu-id="efa1c-107">The value of `manager` must be a valid alias for an individual Microsoft employee.</span></span> <span data-ttu-id="efa1c-108">確認作者的經理別名，並更新該值。</span><span class="sxs-lookup"><span data-stu-id="efa1c-108">Verify the author's manager's alias and update the value.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
