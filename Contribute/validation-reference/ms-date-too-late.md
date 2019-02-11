---
title: ms-date-too-late
description: ms-date-too-late 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 863b13e55c2aaa2057920e3bd77ec75ab5945277
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713100"
---
# <a name="ms-date-too-late"></a><span data-ttu-id="4c364-103">ms-date-too-late</span><span class="sxs-lookup"><span data-stu-id="4c364-103">ms-date-too-late</span></span>

<span data-ttu-id="4c364-104">**即將推出！**</span><span class="sxs-lookup"><span data-stu-id="4c364-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="4c364-105">警告</span><span class="sxs-lookup"><span data-stu-id="4c364-105">Warning</span></span>

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

<span data-ttu-id="4c364-106">此 `ms.date` 屬性是用來表示「時效性」，也就是上次檢閱文章是否相關、是否正確、螢幕擷取畫面是否正確及連結是否有效的時間。</span><span class="sxs-lookup"><span data-stu-id="4c364-106">The `ms.date` attribute is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="4c364-107">因此，不可以是未來的日期！</span><span class="sxs-lookup"><span data-stu-id="4c364-107">Therefore, it can't be in the future!</span></span> <span data-ttu-id="4c364-108">允許在發行時間中佔用 5 天的時間，例如當凍結內容來進行 QA 以針對重大事件做準備時。</span><span class="sxs-lookup"><span data-stu-id="4c364-108">Five days are allowed to account for release time, such as when content is frozen for QA in preparation for a major event.</span></span>

## <a name="resolution"></a><span data-ttu-id="4c364-109">解決方式</span><span class="sxs-lookup"><span data-stu-id="4c364-109">Resolution</span></span>

<span data-ttu-id="4c364-110">以 MM/DD/YYYY 格式指定一個從今天算起不超過 5 天的 `ms.date`。</span><span class="sxs-lookup"><span data-stu-id="4c364-110">Specify an `ms.date` no more than five days from today, in format MM/DD/YYYY.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
