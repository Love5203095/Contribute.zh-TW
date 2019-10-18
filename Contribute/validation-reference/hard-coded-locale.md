---
title: hard-coded-locale
description: Docs 組建問題 hard-coded-locale 的說明和解決方式。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: eb9ae17673b3da5f921139d88cc9af469423c9c3
ms.sourcegitcommit: d357977935b432381f3df6297164417ed59ab434
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2019
ms.locfileid: "72310339"
---
# <a name="hard-coded-locale"></a><span data-ttu-id="73bec-103">hard-coded-locale</span><span class="sxs-lookup"><span data-stu-id="73bec-103">hard-coded-locale</span></span>

## <a name="warning"></a><span data-ttu-id="73bec-104">警告</span><span class="sxs-lookup"><span data-stu-id="73bec-104">Warning</span></span>

`Link '{URL}' contains locale code '{code}'. For localizability, remove '{code}' from links to Microsoft sites.`

<span data-ttu-id="73bec-105">地區設定代碼 (例如 `en-us`) 不應包含在前往特定 Microsoft 網站的連結中。</span><span class="sxs-lookup"><span data-stu-id="73bec-105">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="73bec-106">若您在英文內容中的連結內包含地區設定代碼，它也會包含在當地語系化連結中，導致不良的當地語系化體驗。</span><span class="sxs-lookup"><span data-stu-id="73bec-106">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="73bec-107">例如，若德文當地語系化內容中的連結包含 `en-us`，則德國客戶會發現連結將他們導向英文文章 (即使有可用的德文版本)。</span><span class="sxs-lookup"><span data-stu-id="73bec-107">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="73bec-108">下列網站皆位於此驗證的範圍中：</span><span class="sxs-lookup"><span data-stu-id="73bec-108">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="73bec-109">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="73bec-109">azure.microsoft.com</span></span>
- <span data-ttu-id="73bec-110">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="73bec-110">docs.microsoft.com</span></span>
- <span data-ttu-id="73bec-111">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="73bec-111">msdn.microsoft.com</span></span>
- <span data-ttu-id="73bec-112">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="73bec-112">technet.microsoft.com</span></span>

## <a name="resolution"></a><span data-ttu-id="73bec-113">解決方式</span><span class="sxs-lookup"><span data-stu-id="73bec-113">Resolution</span></span>

<span data-ttu-id="73bec-114">請從前往 Microsoft 網站的連結移除地區設定代碼。</span><span class="sxs-lookup"><span data-stu-id="73bec-114">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="73bec-115">下列為範例。</span><span class="sxs-lookup"><span data-stu-id="73bec-115">The following is an example.</span></span>

<span data-ttu-id="73bec-116">之前：</span><span class="sxs-lookup"><span data-stu-id="73bec-116">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="73bec-117">之後：</span><span class="sxs-lookup"><span data-stu-id="73bec-117">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

> [!TIP]
> <span data-ttu-id="73bec-118">VS Code 的 Docs Markdown 延伸模組包含適用於 Microsoft 連結的清除指令碼。</span><span class="sxs-lookup"><span data-stu-id="73bec-118">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="73bec-119">指令碼會檢查存放庫中所有 Microsoft 網站的連結，確保它們的開頭都是 `https` 而非 `http`，且未包含地區設定代碼 (例如 `en-us`)。</span><span class="sxs-lookup"><span data-stu-id="73bec-119">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="73bec-120">執行指令碼：</span><span class="sxs-lookup"><span data-stu-id="73bec-120">To run the script:</span></span>
>
> 1. <span data-ttu-id="73bec-121">安裝 VS Code 的 [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) 延伸模組。</span><span class="sxs-lookup"><span data-stu-id="73bec-121">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="73bec-122">按一下 alt + M 來開啟 Markdown 功能表。</span><span class="sxs-lookup"><span data-stu-id="73bec-122">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="73bec-123">選取 [Cleanup] \(清除\)  ，然後選取 [Microsoft links] \(Microsoft 連結\)  。</span><span class="sxs-lookup"><span data-stu-id="73bec-123">Select **Cleanup**, then **Microsoft links**.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]