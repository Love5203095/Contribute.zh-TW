---
title: manager-missing
description: Docs 組建問題 manager-missing 的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 16da241a21d400d5a5dfb101e247e55d95567485
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427223"
---
# <a name="manager-missing"></a><span data-ttu-id="cc0ed-103">manager-missing</span><span class="sxs-lookup"><span data-stu-id="cc0ed-103">manager-missing</span></span>

<span data-ttu-id="cc0ed-104">**即將推出！**</span><span class="sxs-lookup"><span data-stu-id="cc0ed-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="cc0ed-105">建議</span><span class="sxs-lookup"><span data-stu-id="cc0ed-105">Suggestion</span></span>

`Missing attribute: manager. Add a valid Microsoft alias for the author's manager.`

<span data-ttu-id="cc0ed-106">某些內容群組需要 `manager` 屬性以識別作者的經理。</span><span class="sxs-lookup"><span data-stu-id="cc0ed-106">Some content groups require the `manager` attribute to identify the author's manager.</span></span>

## <a name="resolution"></a><span data-ttu-id="cc0ed-107">解決方式</span><span class="sxs-lookup"><span data-stu-id="cc0ed-107">Resolution</span></span>

<span data-ttu-id="cc0ed-108">為 `manager` 新增有效的 Microsoft 別名：</span><span class="sxs-lookup"><span data-stu-id="cc0ed-108">Add a valid Microsoft alias for `manager`:</span></span>

```yml
---
ms.author: mbradley
manager: jemash
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
