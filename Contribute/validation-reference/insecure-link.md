---
title: insecure-link
description: Docs 組建問題 issue-insecure-link 的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: b97d4c4a0f61e5f3448331a56fe4bde442ff1cca
ms.sourcegitcommit: 0cb0177c209abab1a72af4f411ef527fa5cf10f9
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2019
ms.locfileid: "72379523"
---
# <a name="insecure-link"></a><span data-ttu-id="bf70e-103">insecure-link</span><span class="sxs-lookup"><span data-stu-id="bf70e-103">insecure-link</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="bf70e-104">建議</span><span class="sxs-lookup"><span data-stu-id="bf70e-104">Suggestion</span></span>

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

<span data-ttu-id="bf70e-105">此訊息表示您與 `http` 搭配使用了明確的 Markdown 連結，或原始 URL (例如 `www.microsoft.com`)。</span><span class="sxs-lookup"><span data-stu-id="bf70e-105">This message means that you either used an explicit Markdown link with `http` or you used a raw URL, such as `www.microsoft.com`.</span></span> <span data-ttu-id="bf70e-106">原始 URL 會在發佈至 Docs 時轉換成不安全的連結，因此不應使用。</span><span class="sxs-lookup"><span data-stu-id="bf70e-106">Raw URLs are converted to insecure links when published to Docs, and should not be used.</span></span>

## <a name="resolution"></a><span data-ttu-id="bf70e-107">解決方式</span><span class="sxs-lookup"><span data-stu-id="bf70e-107">Resolution</span></span>

<span data-ttu-id="bf70e-108">將所有 Microsoft 網站的 URL 變更為使用 `https` 而非 `http`。</span><span class="sxs-lookup"><span data-stu-id="bf70e-108">Change all URLs to Microsoft sites to use `https` instead of `http`.</span></span>

<span data-ttu-id="bf70e-109">若您的連結是原始 URL，請將它變更為以 `https` 開頭的明確 Markdown 連結。</span><span class="sxs-lookup"><span data-stu-id="bf70e-109">If your link is a raw URL, change it to an explicit Markdown link beginning with `https`.</span></span>

> [!TIP]
> <span data-ttu-id="bf70e-110">VS Code 的 Docs Markdown 延伸模組包含清除指令碼 (適用於 Microsoft 連結)。</span><span class="sxs-lookup"><span data-stu-id="bf70e-110">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="bf70e-111">指令碼會檢查存放庫中所有 Microsoft 網站的連結，確保它們的開頭都是 `https` 而非 `http`，且未包含地區設定代碼 (例如 `en-us`)。</span><span class="sxs-lookup"><span data-stu-id="bf70e-111">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="bf70e-112">執行指令碼：</span><span class="sxs-lookup"><span data-stu-id="bf70e-112">To run the script:</span></span>
>
> 1. <span data-ttu-id="bf70e-113">安裝 VS Code 的 [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) 延伸模組。</span><span class="sxs-lookup"><span data-stu-id="bf70e-113">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="bf70e-114">按一下 alt + M 來開啟 Markdown 功能表。</span><span class="sxs-lookup"><span data-stu-id="bf70e-114">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="bf70e-115">選取 [Cleanup] \(清除\)  ，然後選取 [Microsoft links] \(Microsoft 連結\)  。</span><span class="sxs-lookup"><span data-stu-id="bf70e-115">Select **Cleanup**, then **Microsoft links**.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
