---
title: 開發語言完成 - Docs 編寫套件
description: 瞭解開發語言完成如何協助 Docs 編寫套件 (Visual Studio Code 延伸模組) 的參與者。
author: scottaddie
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: scaddie
ms.openlocfilehash: f81dc2315dc09256639c98ed72484517ff2c6ff3
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336788"
---
# <a name="dev-lang-completion"></a><span data-ttu-id="6c382-103">開發語言完成</span><span class="sxs-lookup"><span data-stu-id="6c382-103">Dev lang completion</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="6c382-104">摘要</span><span class="sxs-lookup"><span data-stu-id="6c382-104">Summary</span></span>

<span data-ttu-id="6c382-105">參與者需要協助，來判斷 Markdown 檔案中跟在三個倒引號 (程式碼柵欄的開頭) 之後的有效語言識別碼 (dev lang)。</span><span class="sxs-lookup"><span data-stu-id="6c382-105">Contributors need assistance determining the valid language identifiers (dev langs) that can follow triple-backticks (code fence openings) in a Markdown file.</span></span> <span data-ttu-id="6c382-106">可惜的是，開發語言的組建階段驗證並不存在。</span><span class="sxs-lookup"><span data-stu-id="6c382-106">Unfortunately, build-time validation of dev langs doesn't exist.</span></span> <span data-ttu-id="6c382-107">結果是相同概念文件集中的同一語言卻有不同的表示法。</span><span class="sxs-lookup"><span data-stu-id="6c382-107">The result is disparate representations of a single language within the same conceptual docset.</span></span>

<span data-ttu-id="6c382-108">以 C# 為例。</span><span class="sxs-lookup"><span data-stu-id="6c382-108">Consider C# as an example.</span></span> <span data-ttu-id="6c382-109">參與者已使用 `c#`、`C#`、`cs`、`csharp` 和其他字眼做為該語言的開發語言表示法。</span><span class="sxs-lookup"><span data-stu-id="6c382-109">Contributors have used `c#`, `C#`, `cs`, `csharp`, and others as dev lang representations of the language.</span></span> <span data-ttu-id="6c382-110">這些表示法中哪一個正確？</span><span class="sxs-lookup"><span data-stu-id="6c382-110">Which of the preceding representations is correct?</span></span>

<span data-ttu-id="6c382-111">「開發語言完成」  功能會顯示已知的開發語言清單來消除混淆。</span><span class="sxs-lookup"><span data-stu-id="6c382-111">The *Dev lang completion* feature dispels the confusion by displaying a list of known dev langs.</span></span> <span data-ttu-id="6c382-112">從 IntelliSense 中選取開發語言名稱時：</span><span class="sxs-lookup"><span data-stu-id="6c382-112">Upon selecting a dev lang name from IntelliSense:</span></span>

* <span data-ttu-id="6c382-113">程式碼隔離已結尾。</span><span class="sxs-lookup"><span data-stu-id="6c382-113">The code fence is closed.</span></span>
* <span data-ttu-id="6c382-114">插入點位於程式碼隔離中。</span><span class="sxs-lookup"><span data-stu-id="6c382-114">The caret is positioned in the code fence.</span></span>

## <a name="preferences"></a><span data-ttu-id="6c382-115">喜好設定</span><span class="sxs-lookup"><span data-stu-id="6c382-115">Preferences</span></span>

<span data-ttu-id="6c382-116">無法停用此功能。</span><span class="sxs-lookup"><span data-stu-id="6c382-116">It's not possible to disable this feature.</span></span> <span data-ttu-id="6c382-117">可用的設定如下：</span><span class="sxs-lookup"><span data-stu-id="6c382-117">The following settings are available:</span></span>

* [<span data-ttu-id="6c382-118">顯示常用的開發語言</span><span class="sxs-lookup"><span data-stu-id="6c382-118">Display commonly used dev langs</span></span>](#display-commonly-used-dev-langs)
* [<span data-ttu-id="6c382-119">顯示所有已知的開發語言</span><span class="sxs-lookup"><span data-stu-id="6c382-119">Display all known dev langs</span></span>](#display-all-known-dev-langs)

### <a name="display-commonly-used-dev-langs"></a><span data-ttu-id="6c382-120">顯示常用的開發語言</span><span class="sxs-lookup"><span data-stu-id="6c382-120">Display commonly used dev langs</span></span>

<span data-ttu-id="6c382-121">只有有效開發語言的子集會用於單一文件集中。</span><span class="sxs-lookup"><span data-stu-id="6c382-121">Only a subset of the valid dev langs will be used in a single docset.</span></span> <span data-ttu-id="6c382-122">若要提升使用者體驗：</span><span class="sxs-lookup"><span data-stu-id="6c382-122">To enhance the user experience:</span></span>

1. <span data-ttu-id="6c382-123">在 Visual Studio Code 中，開啟文件集根目錄。</span><span class="sxs-lookup"><span data-stu-id="6c382-123">In Visual Studio Code, open the docset to the root directory.</span></span>
1. <span data-ttu-id="6c382-124">選取 [檔案]   >  [喜好設定]   >  [設定]  ，然後依 *Docs Markdown Extension* 篩選。</span><span class="sxs-lookup"><span data-stu-id="6c382-124">Select **File** > **Preferences** > **Settings** and filter by *Docs Markdown Extension*.</span></span>
1. <span data-ttu-id="6c382-125">按一下 [在 settings.json 中編輯]  連結 (位於 [Markdown:  文件集語言] 區段中)。</span><span class="sxs-lookup"><span data-stu-id="6c382-125">Click the **Edit in settings.json** link in the **Markdown: Docset Languages** section.</span></span>
1. <span data-ttu-id="6c382-126">在 settings.json  檔案中加入以下 `markdown.docsetLanguages` 屬性：</span><span class="sxs-lookup"><span data-stu-id="6c382-126">Add the following `markdown.docsetLanguages` property to the *settings.json* file:</span></span>

    ```json
    {
        "markdown.docsetLanguages": [

        ]
    }
    ```

1. <span data-ttu-id="6c382-127">將插入點放在屬性的空白陣列中，然後啟動 IntelliSense (透過 <kbd>Ctrl</kbd> + <kbd>Space</kbd>)。</span><span class="sxs-lookup"><span data-stu-id="6c382-127">Position your caret in the property's empty array, and activate IntelliSense (via <kbd>Ctrl</kbd> + <kbd>Space</kbd>).</span></span> <span data-ttu-id="6c382-128">已知的開發語言名稱清單隨即出現。</span><span class="sxs-lookup"><span data-stu-id="6c382-128">A list of known dev lang names appears.</span></span>
1. <span data-ttu-id="6c382-129">將開發語言名稱新增至陣列，直到您滿意清單為止。</span><span class="sxs-lookup"><span data-stu-id="6c382-129">Add dev lang names to the array until you're satisfied with the list.</span></span> <span data-ttu-id="6c382-130">例如，下列清單會在使用者輸入三個倒引號之後，對使用者顯示四個開發語言名稱：</span><span class="sxs-lookup"><span data-stu-id="6c382-130">For example, the following list will display four dev lang names to the user after typing triple-ticks:</span></span>

    ```json
    {
        "markdown.docsetLanguages": [
            ".NET Core CLI",
            "C#",
            "Markdown",
            "YAML"
        ]
    }
    ```

1. <span data-ttu-id="6c382-131">將您的變更儲存到 settings.json  檔案。</span><span class="sxs-lookup"><span data-stu-id="6c382-131">Save your changes to the *settings.json* file.</span></span>

> [!WARNING]
> <span data-ttu-id="6c382-132">空的 `markdown.docsetLanguages` 陣列會使所有已知的開發語言都顯示出來。</span><span class="sxs-lookup"><span data-stu-id="6c382-132">An empty `markdown.docsetLanguages` array causes all known dev langs to display.</span></span>

### <a name="display-all-known-dev-langs"></a><span data-ttu-id="6c382-133">顯示所有已知的開發語言</span><span class="sxs-lookup"><span data-stu-id="6c382-133">Display all known dev langs</span></span>

<span data-ttu-id="6c382-134">根據預設，所有已知的開發語言名稱都會顯示在 IntelliSense 中。</span><span class="sxs-lookup"><span data-stu-id="6c382-134">By default, all known dev lang names are displayed in IntelliSense.</span></span> <span data-ttu-id="6c382-135">此設定會覆寫 [顯示常用的開發語言](#display-commonly-used-dev-langs)中所述的 `markdown.docsetLanguages` 屬性。</span><span class="sxs-lookup"><span data-stu-id="6c382-135">This setting overrides the `markdown.docsetLanguages` property described in [Display commonly used dev langs](#display-commonly-used-dev-langs).</span></span>

<span data-ttu-id="6c382-136">變更此設定：</span><span class="sxs-lookup"><span data-stu-id="6c382-136">To change this setting:</span></span>

1. <span data-ttu-id="6c382-137">選取 [檔案]   >  [喜好設定]   >  [設定]  ，然後依 *Docs Markdown Extension* 篩選。</span><span class="sxs-lookup"><span data-stu-id="6c382-137">Select **File** > **Preferences** > **Settings** and filter by *Docs Markdown Extension*.</span></span>
1. <span data-ttu-id="6c382-138">開啟或關閉 [Markdown:  所有可用的語言] 區段中的設定。</span><span class="sxs-lookup"><span data-stu-id="6c382-138">Toggle the setting in the **Markdown: All Available Languages** section.</span></span>

## <a name="in-action"></a><span data-ttu-id="6c382-139">操作實況</span><span class="sxs-lookup"><span data-stu-id="6c382-139">In action</span></span>

<span data-ttu-id="6c382-140">以下是這項功能的簡短示範：</span><span class="sxs-lookup"><span data-stu-id="6c382-140">Below is a brief demonstration of this feature:</span></span>

<span data-ttu-id="6c382-141">[![開發語言完成](media/dev-lang-completion.gif)](media/dev-lang-completion.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="6c382-141">[![Dev lang completion](media/dev-lang-completion.gif)](media/dev-lang-completion.gif#lightbox)</span></span>
