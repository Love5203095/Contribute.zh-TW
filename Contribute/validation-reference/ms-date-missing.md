---
title: ms-date-missing
description: ms-date-missing 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: f5603dee7efe5c7ce3eaa4fa944031d94a9283d8
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713238"
---
# <a name="ms-date-missing"></a><span data-ttu-id="115fa-103">ms-date-missing</span><span class="sxs-lookup"><span data-stu-id="115fa-103">ms-date-missing</span></span>

<span data-ttu-id="115fa-104">**即將推出！**</span><span class="sxs-lookup"><span data-stu-id="115fa-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="115fa-105">建議</span><span class="sxs-lookup"><span data-stu-id="115fa-105">Suggestion</span></span>

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

<span data-ttu-id="115fa-106">此日期是用來表示「時效性」，也就是上次檢閱文章是否相關、是否正確、螢幕擷取畫面是否正確及連結是否有效的時間。</span><span class="sxs-lookup"><span data-stu-id="115fa-106">This date is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="115fa-107">這與未明確指定 `ms.date` 時會顯示在頁面上的文章上次「發佈」日期不同。</span><span class="sxs-lookup"><span data-stu-id="115fa-107">This is not the same as the last date the article was *published*, which will show on the page if `ms.date` is not explicitly specified.</span></span>

## <a name="resolution"></a><span data-ttu-id="115fa-108">解決方式</span><span class="sxs-lookup"><span data-stu-id="115fa-108">Resolution</span></span>

<span data-ttu-id="115fa-109">確認文章為最新狀態，其中沒有任何損毀的內容，然後以 MM/DD/YYYY 格式新增有效日期。</span><span class="sxs-lookup"><span data-stu-id="115fa-109">Confirm that the article is up-to-date with no broken content, then add a valid date in the format MM/DD/YYYY.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
