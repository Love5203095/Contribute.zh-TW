---
title: hard-coded-locale
description: Docs 組建問題 hard-coded-locale 的說明和解決方式。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/18/2019
ms.prod: non-product-specific
ms.openlocfilehash: 1ab511398cbd622906ccb0a67e2b24968ee29374
ms.sourcegitcommit: 55624c641bea5367bcfa08655c085bc950e8beae
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/30/2019
ms.locfileid: "73166820"
---
# <a name="hard-coded-locale"></a><span data-ttu-id="d3091-103">hard-coded-locale</span><span class="sxs-lookup"><span data-stu-id="d3091-103">hard-coded-locale</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d3091-104">此規則一開始以「建議」的形式啟用，讓內容小組有時間可以評估影響，以及發展清理其存放庫的計劃。</span><span class="sxs-lookup"><span data-stu-id="d3091-104">This rule was initially enabled as a "Suggestion" to give content teams time to gauge impact and develop a plan to clean up their repos.</span></span> <span data-ttu-id="d3091-105">**在 2019/12/20，它將會提升為「警告」** 。</span><span class="sxs-lookup"><span data-stu-id="d3091-105">**It will be elevated to a "Warning" on 12/20/2019**.</span></span>

## <a name="suggestion"></a><span data-ttu-id="d3091-106">建議</span><span class="sxs-lookup"><span data-stu-id="d3091-106">Suggestion</span></span>

`Link '{URL}' contains locale code '{code}'. For localizability, remove '{code}' from links to most Microsoft sites.`

<span data-ttu-id="d3091-107">地區設定代碼 (例如 `en-us`) 不應包含在前往特定 Microsoft 網站的連結中。</span><span class="sxs-lookup"><span data-stu-id="d3091-107">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="d3091-108">若您在英文內容中的連結內包含地區設定代碼，它也會包含在當地語系化連結中，導致不良的當地語系化體驗。</span><span class="sxs-lookup"><span data-stu-id="d3091-108">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="d3091-109">例如，若德文當地語系化內容中的連結包含 `en-us`，則德國客戶會發現連結將他們導向英文文章 (即使有可用的德文版本)。</span><span class="sxs-lookup"><span data-stu-id="d3091-109">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="d3091-110">下列網站皆位於此驗證的範圍中：</span><span class="sxs-lookup"><span data-stu-id="d3091-110">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="d3091-111">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="d3091-111">azure.microsoft.com</span></span>
- <span data-ttu-id="d3091-112">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="d3091-112">docs.microsoft.com</span></span>
- <span data-ttu-id="d3091-113">msdn.microsoft.com (不包含 social.msdn.com，其需要地區設定，以確保連結到正確的論壇)</span><span class="sxs-lookup"><span data-stu-id="d3091-113">msdn.microsoft.com (excluding social.msdn.com, which needs locale to ensure the correct forum is linked to)</span></span>
- <span data-ttu-id="d3091-114">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="d3091-114">technet.microsoft.com</span></span>

## <a name="resolution"></a><span data-ttu-id="d3091-115">解決方式</span><span class="sxs-lookup"><span data-stu-id="d3091-115">Resolution</span></span>

<span data-ttu-id="d3091-116">請從前往 Microsoft 網站的連結移除地區設定代碼。</span><span class="sxs-lookup"><span data-stu-id="d3091-116">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="d3091-117">下列為範例。</span><span class="sxs-lookup"><span data-stu-id="d3091-117">The following is an example.</span></span>

<span data-ttu-id="d3091-118">之前：</span><span class="sxs-lookup"><span data-stu-id="d3091-118">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="d3091-119">之後：</span><span class="sxs-lookup"><span data-stu-id="d3091-119">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

> [!TIP]
> <span data-ttu-id="d3091-120">VS Code 的 Docs Markdown 延伸模組包含適用於 Microsoft 連結的清除指令碼。</span><span class="sxs-lookup"><span data-stu-id="d3091-120">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="d3091-121">指令碼會檢查存放庫中所有 Microsoft 網站的連結，確保它們的開頭都是 `https` 而非 `http`，且未包含地區設定代碼 (例如 `en-us`)。</span><span class="sxs-lookup"><span data-stu-id="d3091-121">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="d3091-122">執行指令碼：</span><span class="sxs-lookup"><span data-stu-id="d3091-122">To run the script:</span></span>
>
> 1. <span data-ttu-id="d3091-123">安裝 VS Code 的 [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) 延伸模組。</span><span class="sxs-lookup"><span data-stu-id="d3091-123">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="d3091-124">按一下 alt + M 來開啟 Markdown 功能表。</span><span class="sxs-lookup"><span data-stu-id="d3091-124">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="d3091-125">選取 [Cleanup] \(清除\)  ，然後選取 [Microsoft links] \(Microsoft 連結\)  。</span><span class="sxs-lookup"><span data-stu-id="d3091-125">Select **Cleanup**, then **Microsoft links**.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
