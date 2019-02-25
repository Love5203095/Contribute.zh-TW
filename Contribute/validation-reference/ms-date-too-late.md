---
title: ms-date-too-late
description: ms-date-too-late 文件組建問題的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: b38392e9f297e4ee4147ca7fc65f938b5cd53403
ms.sourcegitcommit: f374ad2607360f46d88982b4b7ecc63d3ab08235
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2019
ms.locfileid: "56431476"
---
# <a name="ms-date-too-late"></a><span data-ttu-id="ce5d0-103">ms-date-too-late</span><span class="sxs-lookup"><span data-stu-id="ce5d0-103">ms-date-too-late</span></span>

<span data-ttu-id="ce5d0-104">**即將推出！**</span><span class="sxs-lookup"><span data-stu-id="ce5d0-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="ce5d0-105">警告</span><span class="sxs-lookup"><span data-stu-id="ce5d0-105">Warning</span></span>

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

<span data-ttu-id="ce5d0-106">此 `ms.date` 屬性是用來表示「時效性」，也就是上次檢閱文章是否相關、是否正確、螢幕擷取畫面是否正確及連結是否有效的時間。</span><span class="sxs-lookup"><span data-stu-id="ce5d0-106">The `ms.date` attribute is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="ce5d0-107">因此，不可以是未來的日期！</span><span class="sxs-lookup"><span data-stu-id="ce5d0-107">Therefore, it can't be in the future!</span></span> <span data-ttu-id="ce5d0-108">允許在發行時間中佔用 5 天的時間，例如當凍結內容來進行 QA 以針對重大事件做準備時。</span><span class="sxs-lookup"><span data-stu-id="ce5d0-108">Five days are allowed to account for release time, such as when content is frozen for QA in preparation for a major event.</span></span>

## <a name="resolution"></a><span data-ttu-id="ce5d0-109">解決方式</span><span class="sxs-lookup"><span data-stu-id="ce5d0-109">Resolution</span></span>

<span data-ttu-id="ce5d0-110">以 MM/DD/YYYY 格式指定一個從今天算起不超過 5 天的 `ms.date`：</span><span class="sxs-lookup"><span data-stu-id="ce5d0-110">Specify an `ms.date` no more than five days from today, in format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
