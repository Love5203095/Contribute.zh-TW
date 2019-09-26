---
title: h1-missing
description: Docs 組建問題 h1-missing 的說明和解決方式。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 2d0b766bba5b5ba32bff68f7ac185ab639fc7557
ms.sourcegitcommit: 7e73bef8bcdca39fd54cd79fbe8cb22da5566411
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/24/2019
ms.locfileid: "71247414"
---
# <a name="h1-missing"></a><span data-ttu-id="4e642-103">h1-missing</span><span class="sxs-lookup"><span data-stu-id="4e642-103">h1-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="4e642-104">建議</span><span class="sxs-lookup"><span data-stu-id="4e642-104">Suggestion</span></span>

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

<span data-ttu-id="4e642-105">H1 指的是 Markdown 檔案中的第一個標題。</span><span class="sxs-lookup"><span data-stu-id="4e642-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="4e642-106">當發佈到 docs.microsoft.com 時，H1 會以大型字體顯示在頁面頂端。</span><span class="sxs-lookup"><span data-stu-id="4e642-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="4e642-107">H1 的建立方式為以單一井字 (#) 開始一行文字，其後跟隨一個空格，接著為標題文字。</span><span class="sxs-lookup"><span data-stu-id="4e642-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="4e642-108">解決方式</span><span class="sxs-lookup"><span data-stu-id="4e642-108">Resolution</span></span>

<span data-ttu-id="4e642-109">若要修正此問題，請新增 H1 作為您檔案中 YML 中繼資料區塊後的第一個內容：</span><span class="sxs-lookup"><span data-stu-id="4e642-109">To fix this issue, add an H1 as the first content after the YML metadata block in your file:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> <span data-ttu-id="4e642-110">此規則不適用於包含的檔案。</span><span class="sxs-lookup"><span data-stu-id="4e642-110">This rule does not apply to included files.</span></span> <span data-ttu-id="4e642-111">如果您在包含的檔案收到 H1 結果，您很可能必須將包含的檔案移到 `includes` 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="4e642-111">If you get H1 results on included files, you most likely need to move your included files into an `includes` folder.</span></span> <span data-ttu-id="4e642-112">`includes` 資料夾可以是檔案路徑中的任何層級。</span><span class="sxs-lookup"><span data-stu-id="4e642-112">The `includes` folder can be at any level in the file path.</span></span> <span data-ttu-id="4e642-113">根據路徑，Docs 組建會將檔案識別為包含的檔案，而且不會執行 H1 驗證。</span><span class="sxs-lookup"><span data-stu-id="4e642-113">Based on the path, Docs build will recognize the file as an included file and H1 validations won't run.</span></span>
>
> <span data-ttu-id="4e642-114">父系檔案中缺少 H1s 的常見原因是誤用包含的檔案：H1 位於包含的檔案中，而不在父系檔案中。</span><span class="sxs-lookup"><span data-stu-id="4e642-114">A common cause of missing H1s in parent files is misuse of included files: the H1 is in the included file, not in the parent file.</span></span> <span data-ttu-id="4e642-115">不允許此情況，因為在包含的檔案中使用 H1 表示父系檔案中有重複的 H1s 或包含的檔案只使用一次。</span><span class="sxs-lookup"><span data-stu-id="4e642-115">This isn't allowed, because using an H1 in an included file either means there are duplicate H1s in parent files or the included file is used only once.</span></span> <span data-ttu-id="4e642-116">H1s 在內容集中必須是唯一的，而且包含的檔案只應該用來在多個檔案之間共用內容。</span><span class="sxs-lookup"><span data-stu-id="4e642-116">H1s should be unique within a content set and included files should only be used to share content among multiple files.</span></span> <span data-ttu-id="4e642-117">若您因為 H1s 位於包含的檔案中而取得 `h1-missing` 結果，解決方式是將 H1 (與所有已包含的內容 (若已包含的檔案只使用一次)) 移動到父系檔案中。</span><span class="sxs-lookup"><span data-stu-id="4e642-117">If you get `h1-missing` results because the H1 is in an included file, the solution is to move the H1 - and all the included content if the included file is used only once - into the parent file.</span></span> <span data-ttu-id="4e642-118">如需有關 Docs 中包含檔案的詳細資訊，請參閱 Microsoft 內部文章[在文章中包括可重複使用的內容](https://review.docs.microsoft.com/en-us/help/contribute/includes-best-practices?branch=master).</span><span class="sxs-lookup"><span data-stu-id="4e642-118">For more information about included files in Docs, see the Microsoft-internal article [Include reusable content in articles](https://review.docs.microsoft.com/en-us/help/contribute/includes-best-practices?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
