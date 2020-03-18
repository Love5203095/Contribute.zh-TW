---
title: 排序重新導向 - Docs 編寫套件
description: 瞭解如何使用 Docs 編寫套件 (Visual Studio Code 延伸模組) 來排序重新導向。
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 4924c631c8720743c283083e53b3a1e9af86b00a
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336673"
---
# <a name="sort-redirects"></a><span data-ttu-id="9c48f-103">排序重新導向</span><span class="sxs-lookup"><span data-stu-id="9c48f-103">Sort redirects</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="9c48f-104">摘要</span><span class="sxs-lookup"><span data-stu-id="9c48f-104">Summary</span></span>

<span data-ttu-id="9c48f-105">隨著 docs.microsoft.com 文件集的演進，部分 Markdown 檔案最後會被刪除。</span><span class="sxs-lookup"><span data-stu-id="9c48f-105">With the evolution of a docs.microsoft.com docset, some Markdown files eventually will be deleted.</span></span> <span data-ttu-id="9c48f-106">刪除 Markdown 檔案時，我們必須提供重新導向，透過重新導向正確地處理指向已刪除文章的任何參考連結。</span><span class="sxs-lookup"><span data-stu-id="9c48f-106">When a Markdown file is deleted, we're required to provide a redirect so that any reference to the deleted article is properly resolved via the redirect.</span></span> <span data-ttu-id="9c48f-107">重新導向是在 .openpublishing.redirection.json  檔案中指定。</span><span class="sxs-lookup"><span data-stu-id="9c48f-107">Redirections are specified in the *.openpublishing.redirection.json* file.</span></span>

1. <span data-ttu-id="9c48f-108">開啟命令選擇區，按 <kbd>F1</kbd> (或 macOS 上的 <kbd>⇧⌘ P</kbd>)</span><span class="sxs-lookup"><span data-stu-id="9c48f-108">Open the Command Palette, press <kbd>F1</kbd> (or <kbd>⇧⌘P</kbd> on macOS)</span></span>
1. <span data-ttu-id="9c48f-109">輸入：**Docs:Sort master redirection file**</span><span class="sxs-lookup"><span data-stu-id="9c48f-109">Type: **Docs: Sort master redirection file**</span></span>
1. <span data-ttu-id="9c48f-110">選取要執行的命令</span><span class="sxs-lookup"><span data-stu-id="9c48f-110">Select the command to execute it</span></span>
1. <span data-ttu-id="9c48f-111">觀察 .openpublishing.redirection.json  檔案的變更</span><span class="sxs-lookup"><span data-stu-id="9c48f-111">Observe changes to *.openpublishing.redirection.json* file</span></span>

## <a name="considerations"></a><span data-ttu-id="9c48f-112">考量</span><span class="sxs-lookup"><span data-stu-id="9c48f-112">Considerations</span></span>

<span data-ttu-id="9c48f-113">.openpublishing.redirection.json  檔案設計之初便有「菊鍊」的概念。</span><span class="sxs-lookup"><span data-stu-id="9c48f-113">The concept of "daisy chaining" exists with how the *.openpublishing.redirection.json* file was originally designed.</span></span> <span data-ttu-id="9c48f-114">一段時間後，以重新導向新增的檔案終將過時。</span><span class="sxs-lookup"><span data-stu-id="9c48f-114">Over time, files added as a redirect will eventually become stale.</span></span> <span data-ttu-id="9c48f-115">刪除檔案 A 需要重新導向至檔案 B，之後刪除檔案 B 再重新導向至檔案 C，就是這種情況。理想情況下，前兩個項目都會指向 C：讓 A 重新導向至 C，而 B 保持導向至 C。</span><span class="sxs-lookup"><span data-stu-id="9c48f-115">This happens when file A is deleted and needs a redirect to file B, then later file B is deleted and then redirects to file C. Ideally, both entries would point to C - so that A redirects to C, and B remains the same.</span></span> <span data-ttu-id="9c48f-116">這是小幅的效能提升，我們正積極改善此功能。</span><span class="sxs-lookup"><span data-stu-id="9c48f-116">This is a minor performance gain, and the feature is actively being worked on.</span></span>

## <a name="in-action"></a><span data-ttu-id="9c48f-117">操作實況</span><span class="sxs-lookup"><span data-stu-id="9c48f-117">In action</span></span>

<span data-ttu-id="9c48f-118">以下是這項功能的簡短示範。</span><span class="sxs-lookup"><span data-stu-id="9c48f-118">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="9c48f-119">[![排序重新導向示範](media/sort-redirect.gif)](media/sort-redirect.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="9c48f-119">[![Sort redirects demo](media/sort-redirect.gif)](media/sort-redirect.gif#lightbox)</span></span>
