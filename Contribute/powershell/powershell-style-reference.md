---
title: 撰寫 Cmdlet 參考的特定指導
description: 本文提供格式化 PowerShell 程式碼範例的特定規則。 這適用於包含範例的概念文章，以及 Cmdlet 參考。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 793a3c02ae0edf192416ae514585d5161e8c1f98
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290280"
---
# <a name="updating-reference-articles"></a><span data-ttu-id="f3c80-104">更新參考文章</span><span class="sxs-lookup"><span data-stu-id="f3c80-104">Updating reference articles</span></span>

<span data-ttu-id="f3c80-105">Cmdlet 參考文章具有特定結構。</span><span class="sxs-lookup"><span data-stu-id="f3c80-105">Cmdlet reference articles have a specific structure.</span></span> <span data-ttu-id="f3c80-106">此結構是由 [PlatyPS][] 定義。</span><span class="sxs-lookup"><span data-stu-id="f3c80-106">This structure is defined by [PlatyPS][].</span></span>
<span data-ttu-id="f3c80-107">PlatyPS 是我們用來產生 PowerShell 模組 Cmdlet 說明的工具。</span><span class="sxs-lookup"><span data-stu-id="f3c80-107">PlatyPS is the tool we use to generate cmdlet help for PowerShell modules.</span></span> <span data-ttu-id="f3c80-108">PlatyPS 會為 Cmdlet 建立基底 Markdown 檔案。</span><span class="sxs-lookup"><span data-stu-id="f3c80-108">PlatyPS creates the base Markdown file for a cmdlet.</span></span> <span data-ttu-id="f3c80-109">在編輯 Markdown 檔案後，PlatyPS 會用來建立 `Get-Help` Cmdlet 使用的 MAML 說明檔。</span><span class="sxs-lookup"><span data-stu-id="f3c80-109">After editing the Markdown files, PlatyPS is used create the MAML help files used by the `Get-Help` cmdlet.</span></span>

<span data-ttu-id="f3c80-110">PlatyPS 包含寫入程式碼中 Cmdlet 參考的硬式編碼結構描述。</span><span class="sxs-lookup"><span data-stu-id="f3c80-110">PlatyPS has a hard-coded schema for cmdlet reference that is written into the code.</span></span> <span data-ttu-id="f3c80-111">[platyPS.schema.md][] 文件會嘗試描述此結構。</span><span class="sxs-lookup"><span data-stu-id="f3c80-111">The [platyPS.schema.md][] document attempts to describe this structure.</span></span> <span data-ttu-id="f3c80-112">結構描述違規會造成建置錯誤；您必須先修正這些錯誤，我們才可以接受您的貢獻。</span><span class="sxs-lookup"><span data-stu-id="f3c80-112">Schema violations cause build errors that must be fixed before we can accept your contribution.</span></span>

## <a name="general-guidelines"></a><span data-ttu-id="f3c80-113">一般方針</span><span class="sxs-lookup"><span data-stu-id="f3c80-113">General guidelines</span></span>

- <span data-ttu-id="f3c80-114">請勿移除任何標頭結構。</span><span class="sxs-lookup"><span data-stu-id="f3c80-114">Do not remove any of the header structures.</span></span> <span data-ttu-id="f3c80-115">PlatyPS 需要一組特定的標頭。</span><span class="sxs-lookup"><span data-stu-id="f3c80-115">PlatyPS expects a specific set of headers.</span></span>
- <span data-ttu-id="f3c80-116">**輸入類型**和**輸出類型**標頭必須具備類型。</span><span class="sxs-lookup"><span data-stu-id="f3c80-116">The **Input type** and **Output type** headers must have a type.</span></span> <span data-ttu-id="f3c80-117">若 Cmdlet 不會接受輸入或是傳回任何值，請使用 "None" 值。</span><span class="sxs-lookup"><span data-stu-id="f3c80-117">If the cmdlet does not take input or return a value then use the value "None".</span></span>
- <span data-ttu-id="f3c80-118">只有[範例](#format-for-examples)區段才允許圍住的程式碼區塊。</span><span class="sxs-lookup"><span data-stu-id="f3c80-118">Fenced code blocks are only allowed in the [Examples](#format-for-examples) section.</span></span>
- <span data-ttu-id="f3c80-119">內嵌的程式碼範圍則可用於任何段落。</span><span class="sxs-lookup"><span data-stu-id="f3c80-119">Inline code spans can be used in any paragraph.</span></span>

## <a name="formatting-about_-files"></a><span data-ttu-id="f3c80-120">格式化 About_ 檔案</span><span class="sxs-lookup"><span data-stu-id="f3c80-120">Formatting About_ files</span></span>

<span data-ttu-id="f3c80-121">`About_*` 檔案現在會由 [Pandoc][] 處理，而非 PlatyPS。</span><span class="sxs-lookup"><span data-stu-id="f3c80-121">`About_*` files are now processed by [Pandoc][], instead of PlatyPS.</span></span> <span data-ttu-id="f3c80-122">`About_*` 檔案會針對 PowerShell 所有版本及發行工具的最佳相容性進行格式化。</span><span class="sxs-lookup"><span data-stu-id="f3c80-122">`About_*` files are formatted for the best compatibility across with all versions of PowerShell and with the publishing tools.</span></span>
<span data-ttu-id="f3c80-123">請不要在沒有和存放庫維護人員進行確認的情況下改變 `about_*` 檔案的格式。</span><span class="sxs-lookup"><span data-stu-id="f3c80-123">Please do not alter the formatting of `about_*` files without checking in with a repository maintainer.</span></span>

<span data-ttu-id="f3c80-124">基本格式化指導方針：</span><span class="sxs-lookup"><span data-stu-id="f3c80-124">Basic formatting guidelines:</span></span>

- <span data-ttu-id="f3c80-125">將行限制在 80 個字元</span><span class="sxs-lookup"><span data-stu-id="f3c80-125">Limit lines to 80 characters</span></span>
- <span data-ttu-id="f3c80-126">程式碼區塊、區塊引述和表格會限制在 76 個字元，因為 Pandoc 會在轉換時針對這些內容以四個空格進行縮排</span><span class="sxs-lookup"><span data-stu-id="f3c80-126">Code blocks, block quotes, and tables are limited to 76 characters because Pandoc indents these by four spaces during conversion</span></span>
- <span data-ttu-id="f3c80-127">表格需要容納在 76 個字元內</span><span class="sxs-lookup"><span data-stu-id="f3c80-127">Tables need fit within 76 characters</span></span>
  - <span data-ttu-id="f3c80-128">針對多行的儲存格內容手動進行換行</span><span class="sxs-lookup"><span data-stu-id="f3c80-128">Manually wrap contents of cells across multiple lines</span></span>
  - <span data-ttu-id="f3c80-129">在每一行使用開頭和結尾的 `|` 字元</span><span class="sxs-lookup"><span data-stu-id="f3c80-129">Use opening and closing `|` characters on each line</span></span>
  - <span data-ttu-id="f3c80-130">請參閱 [about_Comparison_Operators][about-example] 中的運作範例</span><span class="sxs-lookup"><span data-stu-id="f3c80-130">See a working example in [about_Comparison_Operators][about-example]</span></span>
- <span data-ttu-id="f3c80-131">使用 Pandoc 的特殊字元 `\`、`$`、`` ` `` 和 `<`</span><span class="sxs-lookup"><span data-stu-id="f3c80-131">When using Pandoc's special characters `\`,`$`,`` ` ``, and `<`</span></span>
  - <span data-ttu-id="f3c80-132">在標頭內 - 這些字元必須使用前置 `\` 字元進行逸出</span><span class="sxs-lookup"><span data-stu-id="f3c80-132">Within a header - these characters must be escaped using a leading `\` character</span></span>
  - <span data-ttu-id="f3c80-133">在段落內 - 這些字元應放在程式碼範圍內。</span><span class="sxs-lookup"><span data-stu-id="f3c80-133">Within a paragraph - these characters should be put into code spans.</span></span> <span data-ttu-id="f3c80-134">例如：</span><span class="sxs-lookup"><span data-stu-id="f3c80-134">For example:</span></span>

    ~~~markdown
    ### The purpose of the \$foo variable

    The `$foo` variable is used to store ...
    ~~~

## <a name="format-for-examples"></a><span data-ttu-id="f3c80-135">範例格式</span><span class="sxs-lookup"><span data-stu-id="f3c80-135">Format for examples</span></span>

<span data-ttu-id="f3c80-136">在 PlatyPS 結構描述中，**EXAMPLES** 標頭為 H2 標頭，且每個範例為 H3 標頭。</span><span class="sxs-lookup"><span data-stu-id="f3c80-136">In the PlatyPS schema, the **EXAMPLES** header is an H2 header and each example is an H3 header.</span></span>

<span data-ttu-id="f3c80-137">在範例中，結構描述不允許使用段落來分隔程式碼區塊。</span><span class="sxs-lookup"><span data-stu-id="f3c80-137">Within an example, the schema does not allow code blocks to be separated by paragraphs.</span></span> <span data-ttu-id="f3c80-138">有效的結構描述為：</span><span class="sxs-lookup"><span data-stu-id="f3c80-138">The valid schema is:</span></span>

```
### Example #X title

0 or more paragraphs
1 or more code blocks
0 or more paragraphs.
```

<span data-ttu-id="f3c80-139">為每個範例加上編號，並新增簡短標題。</span><span class="sxs-lookup"><span data-stu-id="f3c80-139">Number each example and add a brief title.</span></span>

<span data-ttu-id="f3c80-140">例如：</span><span class="sxs-lookup"><span data-stu-id="f3c80-140">For example:</span></span>

~~~markdown
### Example 1: Get cmdlets, functions, and aliases

This example gets the PowerShell cmdlets, functions, and aliases that are installed on the
computer.

```powershell
Get-Command
```
~~~


[PlatyPS]: https://github.com/powershell/platyps
[platyPS.schema.md]: https://github.com/PowerShell/platyPS/blob/master/platyPS.schema.md
[issue1806]: https://github.com/PowerShell/PowerShell-Docs/issues/1806
[about-example]: https://github.com/MicrosoftDocs/PowerShell-Docs/blob/staging/reference/6/Microsoft.PowerShell.Core/About/about_Comparison_Operators.md
[Pandoc]: https://pandoc.org