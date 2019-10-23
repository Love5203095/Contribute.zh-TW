---
title: insecure-link
description: Docs 組建問題 issue-insecure-link 的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: c22404e624ae85369d7b0b95f44e37d51f847368
ms.sourcegitcommit: ab31cbb17c64a06cab4ffb37b157fd812417a499
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/18/2019
ms.locfileid: "72587689"
---
# <a name="insecure-link"></a><span data-ttu-id="83571-103">insecure-link</span><span class="sxs-lookup"><span data-stu-id="83571-103">insecure-link</span></span>

> [!IMPORTANT]
> <span data-ttu-id="83571-104">此規則一開始以「建議」的形式啟用，讓內容小組有時間可以評估影響，以及發展清理其存放庫的計劃。</span><span class="sxs-lookup"><span data-stu-id="83571-104">This rule was initially enabled as a "Suggestion" to give content teams time to gauge impact and develop a plan to clean up their repos.</span></span> <span data-ttu-id="83571-105">**在 2019/12/20，它將會提升為「警告」** 。</span><span class="sxs-lookup"><span data-stu-id="83571-105">**It will be elevated to a "Warning" on 12/20/2019**.</span></span>

## <a name="suggestion"></a><span data-ttu-id="83571-106">建議</span><span class="sxs-lookup"><span data-stu-id="83571-106">Suggestion</span></span>

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

<span data-ttu-id="83571-107">此訊息表示您與 `http` 搭配使用了明確的 Markdown 連結，或原始 URL (例如 `www.microsoft.com`)。</span><span class="sxs-lookup"><span data-stu-id="83571-107">This message means that you either used an explicit Markdown link with `http` or you used a raw URL, such as `www.microsoft.com`.</span></span> <span data-ttu-id="83571-108">原始 URL 會在發佈至 Docs 時轉換成不安全的連結，因此不應使用。</span><span class="sxs-lookup"><span data-stu-id="83571-108">Raw URLs are converted to insecure links when published to Docs, and should not be used.</span></span>

## <a name="resolution"></a><span data-ttu-id="83571-109">解決方式</span><span class="sxs-lookup"><span data-stu-id="83571-109">Resolution</span></span>

<span data-ttu-id="83571-110">將所有 Microsoft 網站的 URL 變更為使用 `https` 而非 `http`。</span><span class="sxs-lookup"><span data-stu-id="83571-110">Change all URLs to Microsoft sites to use `https` instead of `http`.</span></span>

<span data-ttu-id="83571-111">若您的連結是原始 URL，請將它變更為以 `https` 開頭的明確 Markdown 連結。</span><span class="sxs-lookup"><span data-stu-id="83571-111">If your link is a raw URL, change it to an explicit Markdown link beginning with `https`.</span></span>

> [!TIP]
> <span data-ttu-id="83571-112">VS Code 的 Docs Markdown 延伸模組包含清除指令碼 (適用於 Microsoft 連結)。</span><span class="sxs-lookup"><span data-stu-id="83571-112">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="83571-113">指令碼會檢查存放庫中所有 Microsoft 網站的連結，確保它們的開頭都是 `https` 而非 `http`，且未包含地區設定代碼 (例如 `en-us`)。</span><span class="sxs-lookup"><span data-stu-id="83571-113">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="83571-114">執行指令碼：</span><span class="sxs-lookup"><span data-stu-id="83571-114">To run the script:</span></span>
>
> 1. <span data-ttu-id="83571-115">安裝 VS Code 的 [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) 延伸模組。</span><span class="sxs-lookup"><span data-stu-id="83571-115">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="83571-116">按一下 alt + M 來開啟 Markdown 功能表。</span><span class="sxs-lookup"><span data-stu-id="83571-116">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="83571-117">選取 [Cleanup] \(清除\)  ，然後選取 [Microsoft links] \(Microsoft 連結\)  。</span><span class="sxs-lookup"><span data-stu-id="83571-117">Select **Cleanup**, then **Microsoft links**.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
