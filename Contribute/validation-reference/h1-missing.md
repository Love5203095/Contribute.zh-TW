---
title: h1-missing
description: Docs 組建問題 h1-missing 的說明和解決方式。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: c920cc0f12a9fac41b640957d45452a7958d4b07
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459111"
---
# <a name="h1-missing"></a><span data-ttu-id="f1f87-103">h1-missing</span><span class="sxs-lookup"><span data-stu-id="f1f87-103">h1-missing</span></span>

## <a name="warning"></a><span data-ttu-id="f1f87-104">警告</span><span class="sxs-lookup"><span data-stu-id="f1f87-104">Warning</span></span>

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

<span data-ttu-id="f1f87-105">H1 指的是 Markdown 檔案中的第一個標題。</span><span class="sxs-lookup"><span data-stu-id="f1f87-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="f1f87-106">當發佈到 docs.microsoft.com 時，H1 會以大型字體顯示在頁面頂端。</span><span class="sxs-lookup"><span data-stu-id="f1f87-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="f1f87-107">H1 的建立方式為以單一井字 (#) 開始一行文字，其後跟隨一個空格，接著為標題文字。</span><span class="sxs-lookup"><span data-stu-id="f1f87-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="f1f87-108">解決方式</span><span class="sxs-lookup"><span data-stu-id="f1f87-108">Resolution</span></span>

<span data-ttu-id="f1f87-109">若要修正此問題，請新增 H1 作為您檔案中 YML 中繼資料區塊後的第一個內容：</span><span class="sxs-lookup"><span data-stu-id="f1f87-109">To fix this issue, add an H1 as the first content after the YML metadata block in your file:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> <span data-ttu-id="f1f87-110">此規則不適用於包含的檔案。</span><span class="sxs-lookup"><span data-stu-id="f1f87-110">This rule does not apply to included files.</span></span> <span data-ttu-id="f1f87-111">如果您在包含的檔案收到 H1 警告，您很可能必須將包含的檔案移到 `includes` 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="f1f87-111">If you get H1 warnings on included files, you most likely need to move your included files into an `includes` folder.</span></span> <span data-ttu-id="f1f87-112">`includes` 資料夾可以是檔案路徑中的任何層級。</span><span class="sxs-lookup"><span data-stu-id="f1f87-112">The `includes` folder can be at any level in the file path.</span></span> <span data-ttu-id="f1f87-113">根據路徑，Docs 組建會將檔案識別為包含的檔案，而且不會執行 H1 驗證。</span><span class="sxs-lookup"><span data-stu-id="f1f87-113">Based on the path, Docs build will recognize the file as an included file and H1 validations won't run.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]