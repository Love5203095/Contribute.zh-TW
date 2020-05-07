---
title: 如何在文件中使用連結
description: 本文提供在 docs.microsoft.com 內建立內容連結的相關指引。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: gewarren
ms.author: gewarren
ms.date: 03/31/2020
ms.openlocfilehash: ca29d4b9e81f8af3b680367b210bd1734860687d
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/04/2020
ms.locfileid: "80624774"
---
# <a name="use-links-in-documentation"></a><span data-ttu-id="917dd-103">在文件中使用連結</span><span class="sxs-lookup"><span data-stu-id="917dd-103">Use links in documentation</span></span>

<span data-ttu-id="917dd-104">本文描述如何在 docs.microsoft.com 上裝載的頁面中使用超連結。</span><span class="sxs-lookup"><span data-stu-id="917dd-104">This article describes how to use hyperlinks from pages hosted at docs.microsoft.com.</span></span> <span data-ttu-id="917dd-105">使用一些不同的慣例，可以輕易地將連結新增至 Markdown。</span><span class="sxs-lookup"><span data-stu-id="917dd-105">Links are easy to add into markdown with a few varying conventions.</span></span> <span data-ttu-id="917dd-106">連結可將使用者指向相同頁面、其他相鄰頁面，或外部網站與 URL 中的內容。</span><span class="sxs-lookup"><span data-stu-id="917dd-106">Links point users to content in the same page, in other neighboring pages, or on external sites and URLs.</span></span>

<span data-ttu-id="917dd-107">docs.microsoft.com 網站後端使用「開放式發行服務」(OPS)，可支援透過 [Markdig][] 剖析引擎且符合 [CommonMark][] 規範的 Markdown。</span><span class="sxs-lookup"><span data-stu-id="917dd-107">The docs.microsoft.com site backend uses Open Publishing Services (OPS), which supports [CommonMark][]-compliant markdown parsed through the [Markdig][] parsing engine.</span></span> <span data-ttu-id="917dd-108">這個 Markdown 變體大多與 [GitHub 變體 Markdown (GFM)][GFM] 相容，因為大多數文件都儲存在 GitHub 中並可在該處編輯。</span><span class="sxs-lookup"><span data-stu-id="917dd-108">This markdown flavor is mostly compatible with [GitHub Flavored Markdown (GFM)][GFM], as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="917dd-109">額外的功能可透過 Markdown 延伸模組新增。</span><span class="sxs-lookup"><span data-stu-id="917dd-109">Additional functionality is added through Markdown extensions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="917dd-110">只要目標有支援 (絕大部分都會支援) 安全協定，所有連結都必須使用安全協定 (`https` 相對於 `http`)。</span><span class="sxs-lookup"><span data-stu-id="917dd-110">All links must be secure (`https` vs `http`) whenever the target supports it (which the vast majority should).</span></span>

## <a name="link-text"></a><span data-ttu-id="917dd-111">連結文字</span><span class="sxs-lookup"><span data-stu-id="917dd-111">Link text</span></span>

<span data-ttu-id="917dd-112">您包含在連結文字中的字詞應該淺顯易懂。</span><span class="sxs-lookup"><span data-stu-id="917dd-112">The words that you include in link text should be friendly.</span></span> <span data-ttu-id="917dd-113">換句話說，它們應該是簡單的英文單字，或您要連結之網頁的標題。</span><span class="sxs-lookup"><span data-stu-id="917dd-113">In other words, they should be normal English words or the title of the page that you're linking to.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="917dd-114">請勿使用「按一下這裡」。</span><span class="sxs-lookup"><span data-stu-id="917dd-114">Do not use "click here."</span></span> <span data-ttu-id="917dd-115">這對搜尋引擎最佳化而言並不是一個好的選擇，且沒有適當地描述目標。</span><span class="sxs-lookup"><span data-stu-id="917dd-115">It's bad for search engine optimization and doesn't adequately describe the target.</span></span>

<span data-ttu-id="917dd-116">**正確：**</span><span class="sxs-lookup"><span data-stu-id="917dd-116">**Correct:**</span></span>

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://docs.microsoft.com/sql/t-sql/statements/set-transaction-isolation-level-transact-sql) reference.`

<span data-ttu-id="917dd-117">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="917dd-117">**Incorrect:**</span></span>

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a><span data-ttu-id="917dd-118">文章之間的連結</span><span class="sxs-lookup"><span data-stu-id="917dd-118">Links from one article to another</span></span>

<span data-ttu-id="917dd-119">發佈系統支援兩種超連結類型：**URL** 和**檔案連結**。</span><span class="sxs-lookup"><span data-stu-id="917dd-119">There are two types of hyperlinks supported by the publishing system: **URLs** and **file links**.</span></span>

<span data-ttu-id="917dd-120">URL 連結可以是相對於 docs.microsoft.com 根目錄的 URL 路徑，或包含完整 URL 語法的絕對 URL (例如 `https://github.com/MicrosoftDocs/PowerShell-Docs`)。</span><span class="sxs-lookup"><span data-stu-id="917dd-120">A URL link can be a URL path that is relative to the root of docs.microsoft.com, or an absolute URL that includes the full URL syntax (for example, `https://github.com/MicrosoftDocs/PowerShell-Docs`).</span></span>

- <span data-ttu-id="917dd-121">連結到目前 _docset_ 的外部內容，或在 docset 內自動產生的參照與概念性文章之間連結時，請使用 URL 連結。</span><span class="sxs-lookup"><span data-stu-id="917dd-121">Use URL links when linking to content outside of the current _docset_ or between autogenerated reference and conceptual articles within the docset.</span></span>
- <span data-ttu-id="917dd-122">建立相對連結的最簡單方式，就是從瀏覽器複製 URL，然後將 `https://docs.microsoft.com/en-us` 從貼到 Markdown 的值中移除。</span><span class="sxs-lookup"><span data-stu-id="917dd-122">The simplest way to create a relative link is to copy the URL from your browser, then remove `https://docs.microsoft.com/en-us` from the value you paste into markdown.</span></span>
   - <span data-ttu-id="917dd-123">請勿在 Microsoft 屬性的 URL 中包含地區設定 (例如，請移除 URL 中的 "/en-us")。</span><span class="sxs-lookup"><span data-stu-id="917dd-123">Do not include locales in URLs for Microsoft properties (for example, remove "/en-us" from the URL).</span></span>

<span data-ttu-id="917dd-124">檔案連結是用來將 docset 內的某篇文章連結到另一篇文章。</span><span class="sxs-lookup"><span data-stu-id="917dd-124">A file link is used to link from one article to another within the docset.</span></span>

- <span data-ttu-id="917dd-125">所有檔案路徑都會使用正斜線 (`/`) 字元，而不是反斜線字元。</span><span class="sxs-lookup"><span data-stu-id="917dd-125">All file paths use forward-slash (`/`) characters instead of back-slash characters.</span></span>
- <span data-ttu-id="917dd-126">將文章連結到相同目錄中的另一篇文章：</span><span class="sxs-lookup"><span data-stu-id="917dd-126">An article links to another article in the same directory:</span></span>

  `[link text](article-name.md)`

- <span data-ttu-id="917dd-127">將文章連結到當前目錄的父目錄中文章：</span><span class="sxs-lookup"><span data-stu-id="917dd-127">An article links to an article in the parent directory of the current directory:</span></span>

  `[link text](../article-name.md)`

- <span data-ttu-id="917dd-128">將文章連結到當前目錄的子目錄中文章：</span><span class="sxs-lookup"><span data-stu-id="917dd-128">An article links to an article in a subdirectory of the current directory:</span></span>

  `[link text](directory/article-name.md)`

- <span data-ttu-id="917dd-129">將文章連結到當前目錄的父目錄中，其他子目錄中文章：</span><span class="sxs-lookup"><span data-stu-id="917dd-129">An article links to an article in a subdirectory of the parent directory of the current directory:</span></span>

  `[link text](../directory/article-name.md)`

> [!NOTE]
> <span data-ttu-id="917dd-130">上述範例均未在連結中使用 `~/`。</span><span class="sxs-lookup"><span data-stu-id="917dd-130">None of the previous examples use the `~/` as part of the link.</span></span> <span data-ttu-id="917dd-131">若要連結到從存放庫根開始的絕對路徑，請使用 `/` 來啟動連結。</span><span class="sxs-lookup"><span data-stu-id="917dd-131">To link to an absolute path that begins at the root of the repository, start the link with `/`.</span></span> <span data-ttu-id="917dd-132">瀏覽 GitHub 上的原始碼存放庫時，置入 `~/` 會產生無效的連結。</span><span class="sxs-lookup"><span data-stu-id="917dd-132">Including the `~/` produces invalid links when navigating the source repositories on GitHub.</span></span> <span data-ttu-id="917dd-133">在路徑的開頭使用 `/` 即可正確解決。</span><span class="sxs-lookup"><span data-stu-id="917dd-133">Starting the path with `/` resolves correctly.</span></span>

### <a name="structure-of-links-on-docsmicrosoftcom"></a><span data-ttu-id="917dd-134">docs.microsoft.com 上的連結結構</span><span class="sxs-lookup"><span data-stu-id="917dd-134">Structure of links on docs.microsoft.com</span></span>

<span data-ttu-id="917dd-135">在 docs.microsoft.com 上發佈的內容具有下列 URL 結構：</span><span class="sxs-lookup"><span data-stu-id="917dd-135">Content published on docs.microsoft.com has the following URL structure:</span></span>

```
https://docs.microsoft.com/<locale>/<product-service>/[<feature-service>]/[<subfolder>]/<topic>[?view=<view-name>]
```

<span data-ttu-id="917dd-136">範例：</span><span class="sxs-lookup"><span data-stu-id="917dd-136">Examples:</span></span>

```
https://docs.microsoft.com/en-us/azure/load-balancer/load-balancer-overview
https://docs.microsoft.com/en-us/powershell/azure/overview?view=azurermps-5.1.1
```

- <span data-ttu-id="917dd-137">`<locale>` - 識別文章的語言 (例如：en-us 或 de-de)</span><span class="sxs-lookup"><span data-stu-id="917dd-137">`<locale>` - identifies the language of the article (example: en-us or de-de)</span></span>
- <span data-ttu-id="917dd-138">`<product-service>` - 產品或服務的名稱 (例如：powershell、dotnet 或 azure)</span><span class="sxs-lookup"><span data-stu-id="917dd-138">`<product-service>` - the name of the product or service (example: powershell, dotnet, or azure)</span></span>
- <span data-ttu-id="917dd-139">`[<feature-service>]` - (選用) 產品的功能或子服務名稱 (例如：csharp 或 load-balancer)</span><span class="sxs-lookup"><span data-stu-id="917dd-139">`[<feature-service>]` - (optional) the name of the product's feature or subservice (example: csharp or load-balancer)</span></span>
- <span data-ttu-id="917dd-140">`[<subfolder>]` - (選用) 功能內的子資料夾名稱</span><span class="sxs-lookup"><span data-stu-id="917dd-140">`[<subfolder>]` - (optional) the name of a subfolder within a feature</span></span>
- <span data-ttu-id="917dd-141">`<topic>` - 主題的文章檔案名稱 (例如：load-balancer-overview 或 overview)</span><span class="sxs-lookup"><span data-stu-id="917dd-141">`<topic>` - the name of the article file for the topic (example: load-balancer-overview or overview)</span></span>
- <span data-ttu-id="917dd-142">`[?view=\<view-name>]` - (選用) 版本選取器針對具有多個可用版本的內容所使用檢視名稱 (例如：azps-3.5.0)</span><span class="sxs-lookup"><span data-stu-id="917dd-142">`[?view=\<view-name>]` - (optional) the view name used by the version selector for content that has multiple versions available (example: azps-3.5.0)</span></span>

> [!TIP]
> <span data-ttu-id="917dd-143">在大部分情況下，相同 _docset_ 中的文章會有相同 `<product-service>` URL 片段。</span><span class="sxs-lookup"><span data-stu-id="917dd-143">In most cases, articles in the same _docset_ have the same `<product-service>` URL fragment.</span></span> <span data-ttu-id="917dd-144">例如：</span><span class="sxs-lookup"><span data-stu-id="917dd-144">For example:</span></span>
> - <span data-ttu-id="917dd-145">相同的 docset</span><span class="sxs-lookup"><span data-stu-id="917dd-145">Same docset</span></span>
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/dotnet/framework/install`
> - <span data-ttu-id="917dd-146">不同的 docset</span><span class="sxs-lookup"><span data-stu-id="917dd-146">Different docset</span></span>
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/visualstudio/whats-new`

## <a name="bookmark-links"></a><span data-ttu-id="917dd-147">書籤連結</span><span class="sxs-lookup"><span data-stu-id="917dd-147">Bookmark links</span></span>

<span data-ttu-id="917dd-148">若要讓書籤連結到「目前」  檔案中的標題，請使用井字符號，後面接著小寫標題文字。</span><span class="sxs-lookup"><span data-stu-id="917dd-148">For a bookmark link to a heading in the *current* file, use a hash symbol followed by the lowercase words of the heading.</span></span> <span data-ttu-id="917dd-149">移除標題中的標點符號，並以破折號取代空格：</span><span class="sxs-lookup"><span data-stu-id="917dd-149">Remove punctuation from the heading and replace spaces with dashes:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<span data-ttu-id="917dd-150">若要連結到另一篇文章中的書籤標題，請使用檔案相對或網站相對連結加上井字符號，後面接著標題文字。</span><span class="sxs-lookup"><span data-stu-id="917dd-150">To link to a bookmark heading in another article, use the file-relative or site-relative link plus a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="917dd-151">移除標題中的標點符號，並以破折號取代空格：</span><span class="sxs-lookup"><span data-stu-id="917dd-151">Remove punctuation from the heading and replace spaces with dashes:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<span data-ttu-id="917dd-152">您也可以從 URL 複製書籤連結。</span><span class="sxs-lookup"><span data-stu-id="917dd-152">You can also copy the bookmark link from the URL.</span></span> <span data-ttu-id="917dd-153">若要尋找 URL，請將滑鼠暫留在 docs.microsoft.com 的標題列上。</span><span class="sxs-lookup"><span data-stu-id="917dd-153">To find the URL, hover your mouse over the heading line on docs.microsoft.com.</span></span> <span data-ttu-id="917dd-154">您應該會看到出現一個連結圖示：</span><span class="sxs-lookup"><span data-stu-id="917dd-154">You should see a link icon appear:</span></span>

![文章標題中的連結圖示](media/how-to-write-links/bookmark-link.png)

<span data-ttu-id="917dd-156">按一下連結圖示，然後從 URL 複製書籤錨點文字 (也就是井字符號後面的部分)。</span><span class="sxs-lookup"><span data-stu-id="917dd-156">Click the link icon and then copy the bookmark anchor text from the URL (that is, the part after the hash).</span></span>

> [!NOTE]
> <span data-ttu-id="917dd-157">Docs 延伸模組也有協助建立連結的工具。</span><span class="sxs-lookup"><span data-stu-id="917dd-157">The Docs Extension also has tools to help create links.</span></span>

### <a name="explicit-anchor-links"></a><span data-ttu-id="917dd-158">明確錨點連結</span><span class="sxs-lookup"><span data-stu-id="917dd-158">Explicit anchor links</span></span>

<span data-ttu-id="917dd-159">除非在中樞和登陸頁面中，否則沒有必要也不建議新增使用 `<a>` HTML 標籤的明確錨點連結。</span><span class="sxs-lookup"><span data-stu-id="917dd-159">Adding explicit anchor links using the `<a>` HTML tag isn't required or recommended, except in hub and landing pages.</span></span> <span data-ttu-id="917dd-160">相反地，請使用自動產生的書籤，如[書籤連結](#bookmark-links)中所述。</span><span class="sxs-lookup"><span data-stu-id="917dd-160">Instead, use the auto-generated bookmarks as described in [bookmark links](#bookmark-links).</span></span> <span data-ttu-id="917dd-161">針對中樞和登陸頁面，請如下所示宣告錨點：</span><span class="sxs-lookup"><span data-stu-id="917dd-161">For hub and landing pages, declare anchors as follows:</span></span>

```markdown
## <a id="anchortext" />Header text
```

<span data-ttu-id="917dd-162">或</span><span class="sxs-lookup"><span data-stu-id="917dd-162">or</span></span>

```markdown
## <a name="anchortext" />Header text
```

<span data-ttu-id="917dd-163">且下列會連結到錨點：</span><span class="sxs-lookup"><span data-stu-id="917dd-163">And the following to link to the anchor:</span></span>

```markdown
To go to a section on the same page:
[text](#anchortext)

To go to a section on another page.
[text](filename.md#anchortext)
```

> [!NOTE]
> <span data-ttu-id="917dd-164">錨點文字必須一律為小寫，且不能包含空格。</span><span class="sxs-lookup"><span data-stu-id="917dd-164">Anchor text must always be lowercase and not contain spaces.</span></span>

## <a name="xref-cross-reference-links"></a><span data-ttu-id="917dd-165">XRef (交互參照) 連結</span><span class="sxs-lookup"><span data-stu-id="917dd-165">XRef (cross reference) links</span></span>

<span data-ttu-id="917dd-166">XRef 連結是連結到 API 的建議方式，因為這些連結會在建置時進行驗證。</span><span class="sxs-lookup"><span data-stu-id="917dd-166">XRef links are the recommended way to link to APIs, because they're validated at build time.</span></span> <span data-ttu-id="917dd-167">若要連結到目前 docset 或其他 docset 中自動產生的 API 參照頁面，請搭配類型或成員的唯一識別碼 ([UID](#determine-the-uid)) 來使用 XRef 連結。</span><span class="sxs-lookup"><span data-stu-id="917dd-167">To link to auto-generated API reference pages in the current docset or other docsets, use XRef links with the unique ID ([UID](#determine-the-uid)) of the type or member.</span></span>

> [!TIP]
> <span data-ttu-id="917dd-168">您可使用[適用於 VS Code 的 Docs Markdown 延伸模組][docsextension] (Docs Authoring Pack 的一部分)，以插入 [.NET API 瀏覽器][]中呈現的 .NET XRref 連結。</span><span class="sxs-lookup"><span data-stu-id="917dd-168">You can use the [Docs Markdown extension for VS Code][docsextension] (part of the Docs Authoring Pack) to insert .NET XRref links that are surfaced in the [.NET API Browser][].</span></span>

<span data-ttu-id="917dd-169">在 [.NET API 瀏覽器][] 或 [Windows UWP][] 搜尋方塊中鍵入完整名稱或其中一部分，以檢查所要連結的 API 是否在 [docs.microsoft.com][docs] 上。</span><span class="sxs-lookup"><span data-stu-id="917dd-169">Check if the API you want to link to is on [docs.microsoft.com][docs] by typing all or some of its full name in the [.NET API browser][] or [Windows UWP][] search box.</span></span> <span data-ttu-id="917dd-170">如果沒有看到任何顯示的結果，則該類型目前還不在 docs.microsoft.com 上。</span><span class="sxs-lookup"><span data-stu-id="917dd-170">If you don't see any results displayed, the type isn't yet on docs.microsoft.com.</span></span>

<span data-ttu-id="917dd-171">您可以使用下列其中一個語法：</span><span class="sxs-lookup"><span data-stu-id="917dd-171">You can use one of the following syntaxes:</span></span>

- <span data-ttu-id="917dd-172">自動連結：</span><span class="sxs-lookup"><span data-stu-id="917dd-172">Auto-links:</span></span>

   ```markdown
   <xref:UID>
   <xref:UID?displayProperty=nameWithType>
   ```

   <span data-ttu-id="917dd-173">根據預設，連結文字只會顯示成員或型別名稱。</span><span class="sxs-lookup"><span data-stu-id="917dd-173">By default, link text shows only the member or type name.</span></span> <span data-ttu-id="917dd-174">選用的 `displayProperty=nameWithType` 查詢參數會產生完整連結文字；亦即，**namespace.type** 表示類型，而 **type.member** 表示類型成員 (包括列舉類型成員)。</span><span class="sxs-lookup"><span data-stu-id="917dd-174">The optional `displayProperty=nameWithType` query parameter produces fully qualified link text, that is, **namespace.type** for types, and **type.member** for type members, including enumeration type members.</span></span>

- <span data-ttu-id="917dd-175">Markdown 式連結：</span><span class="sxs-lookup"><span data-stu-id="917dd-175">Markdown-style links:</span></span>

   ```markdown
   [link text](xref:UID)
   ```

   <span data-ttu-id="917dd-176">當想要自訂顯示的連結文字時，請針對 XRef 使用 Markdown 式連結。</span><span class="sxs-lookup"><span data-stu-id="917dd-176">Use Markdown-style links for XRef when you want to customize the link text that's displayed.</span></span>

<span data-ttu-id="917dd-177">範例：</span><span class="sxs-lookup"><span data-stu-id="917dd-177">Examples:</span></span>

- <span data-ttu-id="917dd-178">**\<xref:System.String>** 會顯示為 <xref:System.String></span><span class="sxs-lookup"><span data-stu-id="917dd-178">**\<xref:System.String>** displays as <xref:System.String></span></span>

- <span data-ttu-id="917dd-179">**\<xref:System.String?displayProperty=nameWithType>** 會顯示為 <xref:System.String?displayProperty=nameWithType></span><span class="sxs-lookup"><span data-stu-id="917dd-179">**\<xref:System.String?displayProperty=nameWithType>** displays as <xref:System.String?displayProperty=nameWithType></span></span>

- <span data-ttu-id="917dd-180">**\[String 類別](xref:System.String)** 會顯示為 [String 類別](xref:System.String)。</span><span class="sxs-lookup"><span data-stu-id="917dd-180">**\[String class](xref:System.String)** displays as [String class](xref:System.String).</span></span>

<span data-ttu-id="917dd-181">在類別中，`displayProperty=fullName` 查詢參數的運作方式與 `displayProperty=nameWithType` 相同。</span><span class="sxs-lookup"><span data-stu-id="917dd-181">The `displayProperty=fullName` query parameter works the same way as `displayProperty=nameWithType` for classes.</span></span> <span data-ttu-id="917dd-182">亦即，連結文字會變成 **namespace.classname**。</span><span class="sxs-lookup"><span data-stu-id="917dd-182">That is, the link text becomes **namespace.classname**.</span></span> <span data-ttu-id="917dd-183">不過，若是成員，則連結文字會顯示為 **namespace.classname.membername**，這可能不適當。</span><span class="sxs-lookup"><span data-stu-id="917dd-183">However, for members, the link text displays as **namespace.classname.membername**, which may be undesirable.</span></span>

> [!NOTE]
> <span data-ttu-id="917dd-184">UID 會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="917dd-184">UIDs are case sensitive.</span></span> <span data-ttu-id="917dd-185">例如，`<xref:System.Object>` 會正確解析，但 `<xref:system.object>` 則不會。</span><span class="sxs-lookup"><span data-stu-id="917dd-185">For example, `<xref:System.Object>` resolves correctly but `<xref:system.object>` does not.</span></span>

### <a name="xref-build-warnings-and-incremental-builds"></a><span data-ttu-id="917dd-186">XRef 建置警告和累加建置</span><span class="sxs-lookup"><span data-stu-id="917dd-186">XRef build warnings and incremental builds</span></span>

<span data-ttu-id="917dd-187">累加建置只會建置已變更或受變更影響的檔案。</span><span class="sxs-lookup"><span data-stu-id="917dd-187">An incremental build only builds files that have changed or been affected by a change.</span></span> <span data-ttu-id="917dd-188">如果看到有關 XREF 連結無效的建置警告，但此連結實際上有效，這可能是因為建置是累加的。</span><span class="sxs-lookup"><span data-stu-id="917dd-188">If you see a build warning about an invalid XREF link, but the link is actually valid, this could be because the build was incremental.</span></span> <span data-ttu-id="917dd-189">造成警告的檔案並未變更，因此不會建置，且會重新顯示過去的警告。</span><span class="sxs-lookup"><span data-stu-id="917dd-189">The file causing the warning didn't change, so it wasn't built and past warnings were replayed.</span></span> <span data-ttu-id="917dd-190">當檔案變更時，或如果觸發完整建置 (可在 ops.microsoft.com 上啟動完整建置)，警告就會消失。</span><span class="sxs-lookup"><span data-stu-id="917dd-190">The warning will disappear when the file changes or if you trigger a full build (you can start a full build on ops.microsoft.com).</span></span> <span data-ttu-id="917dd-191">這是累加建置的缺點，因為 DocFX 無法偵測到 XREF 服務內的資料更新。</span><span class="sxs-lookup"><span data-stu-id="917dd-191">This is a drawback to incremental builds, because DocFX can't detect a data update inside the XREF service.</span></span>

### <a name="determine-the-uid"></a><span data-ttu-id="917dd-192">判斷 UID</span><span class="sxs-lookup"><span data-stu-id="917dd-192">Determine the UID</span></span>

<span data-ttu-id="917dd-193">UID 通常是完整類別或成員名稱。</span><span class="sxs-lookup"><span data-stu-id="917dd-193">The UID is usually the fully qualified class or member name.</span></span> <span data-ttu-id="917dd-194">至少有兩種方式可判斷 UID：</span><span class="sxs-lookup"><span data-stu-id="917dd-194">There are at least two ways to determine the UID:</span></span>

- <span data-ttu-id="917dd-195">以滑鼠右鍵按一下類型或成員的 [Docs][docs] 頁面，選取 [檢視原始檔]  ，然後複製 **ms.assetid** 的 **content** 值：</span><span class="sxs-lookup"><span data-stu-id="917dd-195">Right-click on the [Docs][docs] page for a type or member, select **View source**, and then copy the **content** value for **ms.assetid**:</span></span>

  ![網頁原始檔中的 ms.assetid](media/how-to-write-links/ms-assetid.png)

- <span data-ttu-id="917dd-197">將部分或完整的類型名稱附加到 URL，以使用[自動完成網站][]。</span><span class="sxs-lookup"><span data-stu-id="917dd-197">Use the [autocomplete site][] by appending some or all of the name of the type to the URL.</span></span> <span data-ttu-id="917dd-198">例如，在瀏覽器的網址列中輸入 `https://xref.docs.microsoft.com/autocomplete?text=Writeline`，會顯示其名稱中包含 **Writeline** 的所有類型和方法，以及其 UID。</span><span class="sxs-lookup"><span data-stu-id="917dd-198">For example, entering `https://xref.docs.microsoft.com/autocomplete?text=Writeline` in the address bar of your browser displays all the types and methods that contain **Writeline** in their name, along with their UID.</span></span>

#### <a name="verify-the-uid"></a><span data-ttu-id="917dd-199">驗證 UID</span><span class="sxs-lookup"><span data-stu-id="917dd-199">Verify the UID</span></span>

<span data-ttu-id="917dd-200">若要測試是否有正確的 UID，請以 UID 取代下列 URL 中的 **System.String**，然後將其貼到瀏覽器的網址列中：</span><span class="sxs-lookup"><span data-stu-id="917dd-200">To test if you have the correct UID, replace **System.String** in the following URL with your UID, and then paste it into the address bar of a browser:</span></span>

`https://xref.docs.microsoft.com/query?uid=System.String`

> [!TIP]
> <span data-ttu-id="917dd-201">URL 中的 UID 會區分大小寫，且如果正在檢查方法多載 UID，請不要在參數類型之間加入空格。</span><span class="sxs-lookup"><span data-stu-id="917dd-201">The UID in the URL is case-sensitive, and if you're checking a method overload UID, don't include spaces between the parameter types.</span></span>

<span data-ttu-id="917dd-202">如果看到類似如下的內容，表示具有正確的 UID：</span><span class="sxs-lookup"><span data-stu-id="917dd-202">If you see something like the following, you have the correct UID:</span></span>

```text
[{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,...xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"},{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,netframework-4.6,netframework-4.6.1,...,xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"}]
```

<span data-ttu-id="917dd-203">如果只看到頁面上顯示 `[]`，則表示具有錯誤的 UID。</span><span class="sxs-lookup"><span data-stu-id="917dd-203">If you just see `[]` displayed on the page, you have the wrong UID.</span></span>

### <a name="percent-encoding-of-urls"></a><span data-ttu-id="917dd-204">URL 的百分號編碼</span><span class="sxs-lookup"><span data-stu-id="917dd-204">Percent-encoding of URLs</span></span>

<span data-ttu-id="917dd-205">UID 中的特殊字元必須以 HTML 編碼，如下所示：</span><span class="sxs-lookup"><span data-stu-id="917dd-205">Special characters in the UID need to be HTML encoded as follows:</span></span>

| <span data-ttu-id="917dd-206">字元</span><span class="sxs-lookup"><span data-stu-id="917dd-206">Character</span></span> | <span data-ttu-id="917dd-207">HTML 編碼</span><span class="sxs-lookup"><span data-stu-id="917dd-207">HTML encoding</span></span> |
| --------- | ------------- |
| `` ` ``   | <span data-ttu-id="917dd-208">%60</span><span class="sxs-lookup"><span data-stu-id="917dd-208">%60</span></span>           |
| `#`       | <span data-ttu-id="917dd-209">%23</span><span class="sxs-lookup"><span data-stu-id="917dd-209">%23</span></span>           |
| `*`       | <span data-ttu-id="917dd-210">%2A</span><span class="sxs-lookup"><span data-stu-id="917dd-210">%2A</span></span>           |

<span data-ttu-id="917dd-211">請參閱[百分號編碼](https://en.wikipedia.org/wiki/Percent-encoding)的完整清單。</span><span class="sxs-lookup"><span data-stu-id="917dd-211">See a full list of [percent-codes](https://en.wikipedia.org/wiki/Percent-encoding).</span></span>

<span data-ttu-id="917dd-212">編碼範例：</span><span class="sxs-lookup"><span data-stu-id="917dd-212">Encoding examples:</span></span>

- <span data-ttu-id="917dd-213">`System.Threading.Tasks.Task``1` 會編碼為 `System.Threading.Tasks.Task%601` (請參閱[泛型型別](#generic-types)一節)</span><span class="sxs-lookup"><span data-stu-id="917dd-213">`System.Threading.Tasks.Task``1` encodes as `System.Threading.Tasks.Task%601` (see the [section on generic types](#generic-types))</span></span>

- <span data-ttu-id="917dd-214">`System.Exception.#ctor` 會編碼為 `System.Exception.%23ctor`</span><span class="sxs-lookup"><span data-stu-id="917dd-214">`System.Exception.#ctor` encodes as `System.Exception.%23ctor`</span></span>

- <span data-ttu-id="917dd-215">`System.Object.Equals*` 會編碼為 `System.Object.Equals%2A`</span><span class="sxs-lookup"><span data-stu-id="917dd-215">`System.Object.Equals*` encodes as `System.Object.Equals%2A`</span></span>

### <a name="generic-types"></a><span data-ttu-id="917dd-216">泛型型別</span><span class="sxs-lookup"><span data-stu-id="917dd-216">Generic types</span></span>

<span data-ttu-id="917dd-217">泛型型別是指 `System.Collections.Generic.List<T>` 之類的類型。</span><span class="sxs-lookup"><span data-stu-id="917dd-217">Generic types are those types such as `System.Collections.Generic.List<T>`.</span></span> <span data-ttu-id="917dd-218">如果在 [.NET API 瀏覽器](https://docs.microsoft.com/dotnet/api/)中瀏覽至此類型並查看其 URL，則會看到 `<T>` 在 URL 中寫成 `-1`，這實際上代表 **\`1**：</span><span class="sxs-lookup"><span data-stu-id="917dd-218">If you browse to this type in the [.NET API browser](https://docs.microsoft.com/dotnet/api/) and look at its URL, you see that `<T>` is written as `-1` in the URL, which actually represents **\`1**:</span></span>

`https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1`

<span data-ttu-id="917dd-219">若要連結到泛型型別 (例如 **List\<T>** )，請將 **\`** 倒單引號字元編碼為 **%60**，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="917dd-219">To link to a generic type such as **List\<T>**, encode the **\`** backtick character as **%60**, as shown in the following example:</span></span>

```markdown
<xref:System.Collections.Generic.List%601>
```

### <a name="methods"></a><span data-ttu-id="917dd-220">方法</span><span class="sxs-lookup"><span data-stu-id="917dd-220">Methods</span></span>

<span data-ttu-id="917dd-221">若要連結到方法，可在方法名稱後面加上星號 (`*`) 來連結到一般方法，或連結到特定多載。</span><span class="sxs-lookup"><span data-stu-id="917dd-221">To link to a method, you can either link to the general method page by adding an asterisk (`*`) after the method name, or to a specific overload.</span></span> <span data-ttu-id="917dd-222">例如，當想要連結到不含特定參數類型的 `<xref:System.Object.Equals%2A?displayProperty=nameWithType>` 方法時，請使用一般頁面。</span><span class="sxs-lookup"><span data-stu-id="917dd-222">For example, use the general page when you want to link to the `<xref:System.Object.Equals%2A?displayProperty=nameWithType>` method without specific parameter types.</span></span> <span data-ttu-id="917dd-223">星號字元會編碼為 `%2A`。</span><span class="sxs-lookup"><span data-stu-id="917dd-223">The asterisk character is encoded as `%2A`.</span></span> <span data-ttu-id="917dd-224">例如：</span><span class="sxs-lookup"><span data-stu-id="917dd-224">For example:</span></span>

<span data-ttu-id="917dd-225">`<xref:System.Object.Equals%2a?displayProperty=nameWithType>` 會連結到 <xref:System.Object.Equals%2A?displayProperty=nameWithType></span><span class="sxs-lookup"><span data-stu-id="917dd-225">`<xref:System.Object.Equals%2a?displayProperty=nameWithType>` links to <xref:System.Object.Equals%2A?displayProperty=nameWithType></span></span>

<span data-ttu-id="917dd-226">若要連結到特定多載，請在方法名稱後面加上括弧，並包含每個參數的完整類型名稱。</span><span class="sxs-lookup"><span data-stu-id="917dd-226">To link to a specific overload, add parenthesis after the method name and include the full type name of each parameter.</span></span> <span data-ttu-id="917dd-227">請勿在類型名稱之間加入空白字元，否則連結將無法使用。</span><span class="sxs-lookup"><span data-stu-id="917dd-227">Do not put a space character between the type names or the link won't work.</span></span> <span data-ttu-id="917dd-228">例如：</span><span class="sxs-lookup"><span data-stu-id="917dd-228">For example:</span></span>

<span data-ttu-id="917dd-229">`<xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>` 會連結到 <xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType></span><span class="sxs-lookup"><span data-stu-id="917dd-229">`<xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>` links to <xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType></span></span>

## <a name="links-from-includes"></a><span data-ttu-id="917dd-230">從包含檔案的連結</span><span class="sxs-lookup"><span data-stu-id="917dd-230">Links from includes</span></span>

<span data-ttu-id="917dd-231">因為包含檔案位於另一個目錄中，所以您必須使用較長的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="917dd-231">Because include files are located in another directory, you must use longer relative paths.</span></span> <span data-ttu-id="917dd-232">若要從包含檔案連結到文章，請使用此格式：</span><span class="sxs-lookup"><span data-stu-id="917dd-232">To link to an article from an include file, use this format:</span></span>

```markdown
[link text](../articles/folder/article-name.md)
```

> [!TIP]
> <span data-ttu-id="917dd-233">適用於 Visual Studio Code 的 [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) 延伸模組有助於正確插入相對連結和書籤，而不需與冗長的路徑奮戰。</span><span class="sxs-lookup"><span data-stu-id="917dd-233">The [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) extension for Visual Studio Code helps you insert relative links and bookmarks correctly without the tedium of figuring out paths.</span></span>

## <a name="links-in-selectors"></a><span data-ttu-id="917dd-234">選取器中的連結</span><span class="sxs-lookup"><span data-stu-id="917dd-234">Links in selectors</span></span>

<span data-ttu-id="917dd-235">選取器是在文件文章中顯示為下拉式清單的導覽元件。</span><span class="sxs-lookup"><span data-stu-id="917dd-235">A selector is a navigation component that appears in a docs article as a drop-down list.</span></span> <span data-ttu-id="917dd-236">當讀者在下拉式清單中選取一個值時，瀏覽器會開啟選取的文章。</span><span class="sxs-lookup"><span data-stu-id="917dd-236">When a reader selects a value in the drop-down, the browser opens the selected article.</span></span> <span data-ttu-id="917dd-237">一般而言，選取器清單會包含密切相關的文章連結，例如多種程式設計語言的相同主題，或密切相關的系列文章。</span><span class="sxs-lookup"><span data-stu-id="917dd-237">Typically the selector list contains links to closely related articles, for example the same subject matter in multiple programming languages or a closely related series of articles.</span></span>

<span data-ttu-id="917dd-238">如果您擁有內嵌在包含檔案中的選取器，則可以使用下列連結結構：</span><span class="sxs-lookup"><span data-stu-id="917dd-238">If you have selectors that are embedded in an include, use the following link structure:</span></span>

   ```markdown
   > [AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]
   - [(Text1 | Example1 )](../articles/folder/article-name1.md)
   - [(Text1 | Example2 )](../articles/folder/article-name2.md)
   - [(Text2 | Example3 )](../articles/folder/article-name3.md)
   - [(Text2 | Example4 )](../articles/folder/article-name4.md)
   ```

## <a name="reference-style-links"></a><span data-ttu-id="917dd-239">參考風格連結</span><span class="sxs-lookup"><span data-stu-id="917dd-239">Reference-style links</span></span>

<span data-ttu-id="917dd-240">您可以使用參考風格連結，讓來源內容更容易閱讀。</span><span class="sxs-lookup"><span data-stu-id="917dd-240">You can use reference-style links to make your source content easier to read.</span></span> <span data-ttu-id="917dd-241">參考風格連結會將內嵌連結語法取代為簡化語法，允許您將較長的 URL 移動到文章的結尾。</span><span class="sxs-lookup"><span data-stu-id="917dd-241">Reference-style links replace inline link syntax with simplified syntax that allows you to move the long URLs to the end of the article.</span></span> <span data-ttu-id="917dd-242">以下是 [Daring Fireball](https://daringfireball.net/projects/markdown/) 的範例：</span><span class="sxs-lookup"><span data-stu-id="917dd-242">Here's [Daring Fireball](https://daringfireball.net/projects/markdown/) 's example:</span></span>

<span data-ttu-id="917dd-243">內嵌文字：</span><span class="sxs-lookup"><span data-stu-id="917dd-243">Inline text:</span></span>

   ```markdown
   I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].
   ```

<span data-ttu-id="917dd-244">文章結尾處的連結參考：</span><span class="sxs-lookup"><span data-stu-id="917dd-244">Link references at the end of the article:</span></span>

   ```markdown
   <!--Reference links in article-->
   [1]: http://google.com/
   [2]: http://search.yahoo.com/
   [3]: http://search.msn.com/
   ```

<span data-ttu-id="917dd-245">請確定您包含冒號之後的空格 (連結之前)。</span><span class="sxs-lookup"><span data-stu-id="917dd-245">Make sure that you include the space after the colon, before the link.</span></span> <span data-ttu-id="917dd-246">當您連結到其他技術文章時，如果忘記包含空格，已發佈的文章中的連結將會中斷。</span><span class="sxs-lookup"><span data-stu-id="917dd-246">When you link to other technical articles, if you forget to include the space, the link will be broken in the published article.</span></span>

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a><span data-ttu-id="917dd-247">連結到不屬於技術文件集的頁面</span><span class="sxs-lookup"><span data-stu-id="917dd-247">Links to pages that are not part of the technical documentation set</span></span>

<span data-ttu-id="917dd-248">若要連結到 Microsoft 網站上的另一個頁面 (例如定價頁面、SLA 頁面或任何不屬於文件文章的頁面)，請使用絕對 URL，但省略地區設定。</span><span class="sxs-lookup"><span data-stu-id="917dd-248">To link to a page on another Microsoft property (such as a pricing page, SLA page, or anything else that is not a documentation article), use an absolute URL, but omit the locale.</span></span> <span data-ttu-id="917dd-249">此目的為本連結可於 GitHub 和轉譯的網站上運作：</span><span class="sxs-lookup"><span data-stu-id="917dd-249">The goal here is that links work in GitHub and on the rendered site:</span></span>

   ```markdown
   [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)
   ```

## <a name="links-to-third-party-sites"></a><span data-ttu-id="917dd-250">連結到協力廠商網站</span><span class="sxs-lookup"><span data-stu-id="917dd-250">Links to third-party sites</span></span>

<span data-ttu-id="917dd-251">最佳使用者體驗會減少將使用者傳送到其他網站的情況。</span><span class="sxs-lookup"><span data-stu-id="917dd-251">The best user experience minimizes sending users to another site.</span></span> <span data-ttu-id="917dd-252">因此，以此資訊作為我們有時需要之任何協力廠商網站連結的基礎：</span><span class="sxs-lookup"><span data-stu-id="917dd-252">So base any links to third-party sites, which we do sometimes need, on this info:</span></span>

- <span data-ttu-id="917dd-253">**責任**：當所要共用的資訊是協力廠商資訊時，連結到協力廠商內容。</span><span class="sxs-lookup"><span data-stu-id="917dd-253">**Accountability**: Link to third-party content when it's the third-party's information to share.</span></span> <span data-ttu-id="917dd-254">例如，告知大家如何使用 Android 開發人員工具，並不是 Microsoft 的立場，那是 Google 的資訊。</span><span class="sxs-lookup"><span data-stu-id="917dd-254">For example, it's not Microsoft's place to tell people how to use Android developer tools--that is Google's story to tell.</span></span> <span data-ttu-id="917dd-255">如果有需要，我們可以解釋如何*搭配* Azure 使用 Android 開發人員工具，但 Google 應該說明如何使用其工具。</span><span class="sxs-lookup"><span data-stu-id="917dd-255">If we need to, we can explain how to use Android developer tools *with* Azure, but Google should tell the story of how to use their tools.</span></span>
- <span data-ttu-id="917dd-256">**PM 簽核**：要求 Microsoft 簽核協力廠商內容。</span><span class="sxs-lookup"><span data-stu-id="917dd-256">**PM signoff**: Request that Microsoft sign off on third-party content.</span></span> <span data-ttu-id="917dd-257">透過與之連結，表示我們對其信任以及我們在人們遵循指示時的義務。</span><span class="sxs-lookup"><span data-stu-id="917dd-257">By linking to it, we are saying something about our trust in it and our obligation if people follow the instructions.</span></span>
- <span data-ttu-id="917dd-258">**時效性檢閱**：確定協力廠商資訊仍是最新、正確且相關，且連結並未變更。</span><span class="sxs-lookup"><span data-stu-id="917dd-258">**Freshness reviews**: Make sure that the third-party info is still current, correct, and relevant, and that the link hasn't changed.</span></span>
- <span data-ttu-id="917dd-259">**異地**：讓使用者了解他們將前往另一個網站。</span><span class="sxs-lookup"><span data-stu-id="917dd-259">**Offsite**: Make users aware that they are going to another site.</span></span> <span data-ttu-id="917dd-260">如果上下文不清楚，請加入一個限定詞組。</span><span class="sxs-lookup"><span data-stu-id="917dd-260">If the context does not make that clear, add a qualifying phrase.</span></span> <span data-ttu-id="917dd-261">例如：「必要條件包括 Android 開發人員工具，其可在 Android Studio 網站上下載」。</span><span class="sxs-lookup"><span data-stu-id="917dd-261">For example: "Prerequisites include the Android Developer Tools, which you can download on the Android Studio site."</span></span>
- <span data-ttu-id="917dd-262">**後續步驟**：舉例來說，可在＜後續步驟＞一節中新增一個 MVP 部落格連結。</span><span class="sxs-lookup"><span data-stu-id="917dd-262">**Next steps**: It's fine to add a link to, say, an MVP blog in a "Next steps" section.</span></span> <span data-ttu-id="917dd-263">同樣地，請確認使用者了解他們將會離開網站。</span><span class="sxs-lookup"><span data-stu-id="917dd-263">Again, just make sure that users understand they'll be leaving the site.</span></span>
- <span data-ttu-id="917dd-264">**法律**：在所有 microsoft.com 頁面的**使用條款**頁尾中，**第三方網站的連結**規定了相關法律事宜。</span><span class="sxs-lookup"><span data-stu-id="917dd-264">**Legal**: We are covered legally under **Links to Third Party Sites** in the **Terms of Use** footer on every microsoft.com page.</span></span>

<!-- link references -->
[CommonMark]: https://commonmark.org/
[Markdig]: https://github.com/lunet-io/markdig
[GFM]: https://help.github.com/categories/writing-on-github/
[docs]: https://docs.microsoft.com
[.NET API 瀏覽器]: https://docs.microsoft.com/dotnet/api/
[.NET API browser]: https://docs.microsoft.com/dotnet/api/
[Windows UWP]: https://docs.microsoft.com/uwp/api
[docsextension]: https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown
[自動完成網站]: https://xref.docs.microsoft.com/autocomplete?text=
[autocomplete site]: https://xref.docs.microsoft.com/autocomplete?text=
