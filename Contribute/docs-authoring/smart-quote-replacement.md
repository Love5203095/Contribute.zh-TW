---
title: 自動智慧引號取代 - Docs 編寫套件
description: 瞭解如何使用 Docs 編寫套件 (Visual Studio Code 延伸模組) 來進行自動智慧引號取代。
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 048f244324d7dde540c78e6631ccb5abbed3e431
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336696"
---
# <a name="smart-quote-replacement"></a><span data-ttu-id="f1f44-103">智慧引號取代</span><span class="sxs-lookup"><span data-stu-id="f1f44-103">Smart quote replacement</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="f1f44-104">摘要</span><span class="sxs-lookup"><span data-stu-id="f1f44-104">Summary</span></span>

<span data-ttu-id="f1f44-105">內容開發人員負責撰寫現代化技術和情報的一些最先進的功能，然而現今的工具仍偏好在 Markdown 中使用「笨蛋引號」。</span><span class="sxs-lookup"><span data-stu-id="f1f44-105">Content developers are responsible for authoring some of the most advanced features of modern technology and intelligence, yet our tooling today prefers the usage of "dumb quotes" in Markdown.</span></span> <span data-ttu-id="f1f44-106">就怕「智慧引號」聰明反被聰明誤。</span><span class="sxs-lookup"><span data-stu-id="f1f44-106">The antonym of course being "smart quotes".</span></span> <span data-ttu-id="f1f44-107">智慧引號常見於完美的字型設計上，但在 Markdown 和轉譯 HTML 上並不常用。</span><span class="sxs-lookup"><span data-stu-id="f1f44-107">Smart quotes are common with ideal typographies, but not preferred with Markdown and rendered HTML.</span></span>

<span data-ttu-id="f1f44-108">例如，您可能已經注意到，在處理 Microsoft Word 文件時，當您按住 <kbd>Shift</kbd> 並輸入 <kbd>"</kbd> 時，Microsoft Word 會快速地將 `"` 字元取代為相當於 `“` 字元的智慧引號。</span><span class="sxs-lookup"><span data-stu-id="f1f44-108">When working on a Microsoft Word document for example, you may have noticed that when you hold the <kbd>Shift</kbd> and type a <kbd>"</kbd> Microsoft Word quickly replaces the `"` character with a smart quote equivalent `“` character.</span></span>

| <span data-ttu-id="f1f44-109">Description</span><span class="sxs-lookup"><span data-stu-id="f1f44-109">Description</span></span>        | <span data-ttu-id="f1f44-110">Unicode</span><span class="sxs-lookup"><span data-stu-id="f1f44-110">Unicode</span></span>  | <span data-ttu-id="f1f44-111">智慧引號</span><span class="sxs-lookup"><span data-stu-id="f1f44-111">Smart Quote</span></span> | <span data-ttu-id="f1f44-112">取代</span><span class="sxs-lookup"><span data-stu-id="f1f44-112">Replacement</span></span> |
|--------------------|----------|-------------|-------------|
| <span data-ttu-id="f1f44-113">左雙引號</span><span class="sxs-lookup"><span data-stu-id="f1f44-113">Double left quote</span></span>  | `\u201c` | `“`         | `"`         |
| <span data-ttu-id="f1f44-114">右雙引號</span><span class="sxs-lookup"><span data-stu-id="f1f44-114">Double right quote</span></span> | `\u201d` | `”`         | `"`         |
| <span data-ttu-id="f1f44-115">左單引號</span><span class="sxs-lookup"><span data-stu-id="f1f44-115">Single left quote</span></span>  | `\u2018` | `‘`         | `'`         |
| <span data-ttu-id="f1f44-116">右單引號</span><span class="sxs-lookup"><span data-stu-id="f1f44-116">Single right quote</span></span> | `\u2019` | `’`         | `'`         |

<span data-ttu-id="f1f44-117">在 Markdown (.md *\** ) 檔案中，當您貼上文字或更新內容時，這項功能會主動評估內容，並據此自動取代值。</span><span class="sxs-lookup"><span data-stu-id="f1f44-117">In a Markdown (*\*.md*) file, when you paste in text or as you update content - this feature will actively evaluate the content and automatically replace values accordingly.</span></span>

> [!NOTE]
> <span data-ttu-id="f1f44-118">「智慧引號取代」功能也會取代其他字元，例如但不限於 `©, ™, ®, •`、下標和上標字元。</span><span class="sxs-lookup"><span data-stu-id="f1f44-118">The smart quote replacement feature also replaces other characters, such as but not limited to; (`©, ™, ®, •`, subscript and superscript characters).</span></span> <span data-ttu-id="f1f44-119">從 Word 文件貼入文字時，這很有用。</span><span class="sxs-lookup"><span data-stu-id="f1f44-119">This is useful when pasting text from Word documents.</span></span>

## <a name="preferences"></a><span data-ttu-id="f1f44-120">喜好設定</span><span class="sxs-lookup"><span data-stu-id="f1f44-120">Preferences</span></span>

<span data-ttu-id="f1f44-121">這是選擇性功能，但預設為 `true`。</span><span class="sxs-lookup"><span data-stu-id="f1f44-121">This feature is optional, but defaults to `true`.</span></span> <span data-ttu-id="f1f44-122">開啟或關閉此功能：</span><span class="sxs-lookup"><span data-stu-id="f1f44-122">To toggle this feature on or off:</span></span>

1. <span data-ttu-id="f1f44-123">選取 [檔案]   >  [喜好設定]   >  [設定]  ，然後依 *Docs Markdown Extension* 篩選。</span><span class="sxs-lookup"><span data-stu-id="f1f44-123">Select **File** > **Preferences** > **Settings** and filter by *Docs Markdown Extension*.</span></span>
1. <span data-ttu-id="f1f44-124">開啟或關閉 [Markdown:  取代智慧引號] 區段中的設定。</span><span class="sxs-lookup"><span data-stu-id="f1f44-124">Toggle the setting in the **Markdown: Replace Smart Quotes** section.</span></span>

## <a name="in-action"></a><span data-ttu-id="f1f44-125">操作實況</span><span class="sxs-lookup"><span data-stu-id="f1f44-125">In action</span></span>

<span data-ttu-id="f1f44-126">以下是這項功能的簡短示範。</span><span class="sxs-lookup"><span data-stu-id="f1f44-126">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="f1f44-127">[![取代智慧引號示範](media/replace-smart-quotes.gif)](media/replace-smart-quotes.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="f1f44-127">[![Replace smart quotes demo](media/replace-smart-quotes.gif)](media/replace-smart-quotes.gif#lightbox)</span></span>
