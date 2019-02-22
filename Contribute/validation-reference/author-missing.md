---
title: author-missing
description: author-missing 文件組建問題的說明和解決方式。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 89725dcfbd4ec266071c45a003748021b480bbc2
ms.sourcegitcommit: f374ad2607360f46d88982b4b7ecc63d3ab08235
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2019
ms.locfileid: "56431522"
---
# <a name="author-missing"></a><span data-ttu-id="80098-103">author-missing</span><span class="sxs-lookup"><span data-stu-id="80098-103">author-missing</span></span>

<span data-ttu-id="80098-104">**即將推出！**</span><span class="sxs-lookup"><span data-stu-id="80098-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="80098-105">建議</span><span class="sxs-lookup"><span data-stu-id="80098-105">Suggestion</span></span>

`Missing attribute: author. Add a valid GitHub ID.`

<span data-ttu-id="80098-106">`author` 屬性會依 GitHub 識別碼來識別文章的作者。</span><span class="sxs-lookup"><span data-stu-id="80098-106">The `author` attribute identifies the author of the article by GitHub ID.</span></span> 

## <a name="resolution"></a><span data-ttu-id="80098-107">解決方式</span><span class="sxs-lookup"><span data-stu-id="80098-107">Resolution</span></span>

<span data-ttu-id="80098-108">將作者的 GitHub 識別碼新增至 YML 標頭：</span><span class="sxs-lookup"><span data-stu-id="80098-108">Add the author's GitHub ID to the YML header:</span></span>

```yml
---
author: meganbradley
ms.author: mbradley
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]