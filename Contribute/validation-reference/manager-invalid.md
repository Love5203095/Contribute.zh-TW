---
title: manager-invalid
description: Docs 組建問題 manager-invalid 的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7eac188b16b402767bbec551a6dec8b5877680af
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427202"
---
# <a name="manager-invalid"></a><span data-ttu-id="d4de0-103">manager-invalid</span><span class="sxs-lookup"><span data-stu-id="d4de0-103">manager-invalid</span></span>

<span data-ttu-id="d4de0-104">**即將推出！**</span><span class="sxs-lookup"><span data-stu-id="d4de0-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="d4de0-105">建議</span><span class="sxs-lookup"><span data-stu-id="d4de0-105">Suggestion</span></span>

`Invalid value for manager: '{value}' is not a valid Microsoft alias.`

<span data-ttu-id="d4de0-106">某些內容群組需要 `manager` 屬性以識別作者的經理。</span><span class="sxs-lookup"><span data-stu-id="d4de0-106">Some content groups require the `manager` attribute to identify the author's manager.</span></span>

## <a name="resolution"></a><span data-ttu-id="d4de0-107">解決方式</span><span class="sxs-lookup"><span data-stu-id="d4de0-107">Resolution</span></span>

<span data-ttu-id="d4de0-108">`manager` 的值必須是個別 Microsoft 員工的有效別名。</span><span class="sxs-lookup"><span data-stu-id="d4de0-108">The value of `manager` must be a valid alias for an individual Microsoft employee.</span></span> <span data-ttu-id="d4de0-109">確認作者的經理別名，並更新該值。</span><span class="sxs-lookup"><span data-stu-id="d4de0-109">Verify the author's manager's alias and update the value.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
