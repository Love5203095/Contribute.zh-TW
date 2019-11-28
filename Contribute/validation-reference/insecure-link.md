---
title: insecure-link
description: Docs 組建問題 issue-insecure-link 的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4735d47cdf2029d2c613c9b333a393c7d978c58e
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528854"
---
# <a name="insecure-link"></a><span data-ttu-id="c594c-103">insecure-link</span><span class="sxs-lookup"><span data-stu-id="c594c-103">insecure-link</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c594c-104">此規則一開始以「建議」的形式啟用，讓內容小組有時間可以評估影響，以及發展清理其存放庫的計劃。</span><span class="sxs-lookup"><span data-stu-id="c594c-104">This rule was initially enabled as a "Suggestion" to give content teams time to gauge impact and develop a plan to clean up their repos.</span></span> <span data-ttu-id="c594c-105">**在 2019/12/20，它將會提升為「警告」** 。</span><span class="sxs-lookup"><span data-stu-id="c594c-105">**It will be elevated to a "Warning" on 12/20/2019**.</span></span>

## <a name="suggestion"></a><span data-ttu-id="c594c-106">建議</span><span class="sxs-lookup"><span data-stu-id="c594c-106">Suggestion</span></span>

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

<span data-ttu-id="c594c-107">此訊息表示您與 `http` 搭配使用了明確的 Markdown 連結，或原始 URL (例如 `www.microsoft.com`)。</span><span class="sxs-lookup"><span data-stu-id="c594c-107">This message means that you either used an explicit Markdown link with `http` or you used a raw URL, such as `www.microsoft.com`.</span></span> <span data-ttu-id="c594c-108">原始 URL 會在發佈至 Docs 時轉換成不安全的連結，因此不應使用。</span><span class="sxs-lookup"><span data-stu-id="c594c-108">Raw URLs are converted to insecure links when published to Docs, and should not be used.</span></span>

## <a name="resolution"></a><span data-ttu-id="c594c-109">解決方式</span><span class="sxs-lookup"><span data-stu-id="c594c-109">Resolution</span></span>

<span data-ttu-id="c594c-110">將所有 Microsoft 網站的 URL 變更為使用 `https` 而非 `http`。</span><span class="sxs-lookup"><span data-stu-id="c594c-110">Change all URLs to Microsoft sites to use `https` instead of `http`.</span></span>

<span data-ttu-id="c594c-111">若您的連結是原始 URL，請將其變更為以 `https` 開頭的明確 Markdown 連結，例如：</span><span class="sxs-lookup"><span data-stu-id="c594c-111">If your link is a raw URL, change it to an explicit Markdown link beginning with `https`, such as:</span></span>

```md
`[www.microsoft.com](https://www.microsoft.com)`.
```

> [!TIP]
> <span data-ttu-id="c594c-112">VS Code 的 Docs Markdown 延伸模組包含清除指令碼 (適用於 Microsoft 連結)。</span><span class="sxs-lookup"><span data-stu-id="c594c-112">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="c594c-113">指令碼會檢查存放庫中所有 Microsoft 網站的連結，確保它們的開頭都是 `https` 而非 `http`，且未包含地區設定代碼 (例如 `en-us`)。</span><span class="sxs-lookup"><span data-stu-id="c594c-113">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="c594c-114">執行指令碼：</span><span class="sxs-lookup"><span data-stu-id="c594c-114">To run the script:</span></span>
>
> 1. <span data-ttu-id="c594c-115">安裝 VS Code 的 [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) 延伸模組。</span><span class="sxs-lookup"><span data-stu-id="c594c-115">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="c594c-116">按一下 alt + M 來開啟 Markdown 功能表。</span><span class="sxs-lookup"><span data-stu-id="c594c-116">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="c594c-117">選取 [Cleanup] \(清除\)  ，然後選取 [Microsoft links] \(Microsoft 連結\)  。</span><span class="sxs-lookup"><span data-stu-id="c594c-117">Select **Cleanup**, then **Microsoft links**.</span></span>

<span data-ttu-id="c594c-118">在某些情況下，您可能需要記下沒有要建立成可按式連結的網址 (例如完整網域名稱)。</span><span class="sxs-lookup"><span data-stu-id="c594c-118">In some cases, you might need to document web addresses, such as fully-qualified domain names, that aren't meant to be clickable links.</span></span> <span data-ttu-id="c594c-119">這些網址的樣式應為內嵌程式碼，例如：</span><span class="sxs-lookup"><span data-stu-id="c594c-119">These should be styled as inline code, such as:</span></span>

```md
`www.microsoft.com:90`
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
