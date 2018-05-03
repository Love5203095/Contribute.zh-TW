---
title: 如何在文件中使用連結
description: 本文提供在 docs.microsoft.com 內建立內容連結的相關指引。
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 06/29/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 1699e57ac6a4dc4c5a1ef099ea183b3cbc6307cd
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2018
---
# <a name="using-links-in-documentation"></a><span data-ttu-id="f02df-103">在文件中使用連結</span><span class="sxs-lookup"><span data-stu-id="f02df-103">Using links in documentation</span></span>
<span data-ttu-id="f02df-104">本文描述如何在 docs.microsoft.com 上裝載的頁面中使用超連結。使用一些不同的慣例，可以輕易地將連結新增至 Markdown。</span><span class="sxs-lookup"><span data-stu-id="f02df-104">This article describes how to use hyperlinks from pages hosted at docs.microsoft.com. Links are easy to add into markdown with a few varying conventions.</span></span> <span data-ttu-id="f02df-105">連結可將使用者指向同一頁中的內容、指到其他相鄰頁面，或指向外部網站和 URL。</span><span class="sxs-lookup"><span data-stu-id="f02df-105">Links point users to content in the same page, point off into other neighboring pages, or point to external sites and URLs.</span></span>

<span data-ttu-id="f02df-106">docs.microsoft.com 網站後端會使用實作 DocFX 版 Markdown (DFM) 的開放式發行服務 (OPS)。</span><span class="sxs-lookup"><span data-stu-id="f02df-106">The docs.microsoft.com site backend uses Open Publishing Services (OPS) which implements DocFX Flavored Markdown (DFM).</span></span> <span data-ttu-id="f02df-107">DFM 與 GitHub 版 Markdown (GFM) 高度相容，因此 DFM 可透過 Markdown 延伸模組新增其他功能。</span><span class="sxs-lookup"><span data-stu-id="f02df-107">DFM is highly compatible with GitHub Flavored Markdown (GFM), and DFM adds additional functionality through Markdown extensions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f02df-108">只要目標有支援 (絕大部分都會支援) 安全協定，所有連結都必須使用安全協定 (`https` 相對於 `http`)。</span><span class="sxs-lookup"><span data-stu-id="f02df-108">All links must be secure (`https` vs `http`) whenever the target supports it (which the vast majority should).</span></span>

## <a name="link-text"></a><span data-ttu-id="f02df-109">連結文字</span><span class="sxs-lookup"><span data-stu-id="f02df-109">Link text</span></span>

<span data-ttu-id="f02df-110">您包含在連結文字中的字詞應該淺顯易懂。</span><span class="sxs-lookup"><span data-stu-id="f02df-110">The words that you include in link text should be friendly.</span></span> <span data-ttu-id="f02df-111">換句話說，它們應該是簡單的英文單字，或您要連結之網頁的標題。</span><span class="sxs-lookup"><span data-stu-id="f02df-111">In other words, they should be normal English words or the title of the page that you're linking to.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f02df-112">請勿使用「按一下這裡」。</span><span class="sxs-lookup"><span data-stu-id="f02df-112">Do not use "click here."</span></span> <span data-ttu-id="f02df-113">這對 SEO 而言是不好的，且沒有適當地描述目標。</span><span class="sxs-lookup"><span data-stu-id="f02df-113">It's bad for SEO and doesn't adequately describe the target.</span></span>

<span data-ttu-id="f02df-114">**正確：**</span><span class="sxs-lookup"><span data-stu-id="f02df-114">**Correct:**</span></span>

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://msdn.microsoft.com/library/ms173763.aspx) reference.`

<span data-ttu-id="f02df-115">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="f02df-115">**Incorrect:**</span></span>

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a><span data-ttu-id="f02df-116">文章之間的連結</span><span class="sxs-lookup"><span data-stu-id="f02df-116">Links from one article to another</span></span>

<span data-ttu-id="f02df-117">若要從 Docs 技術文章建立與相同 docset 中其他 Docs 技術文章的內嵌連結，請使用以下連結語法：</span><span class="sxs-lookup"><span data-stu-id="f02df-117">To create an inline link from a Docs technical article to another Docs technical article within the same docset, use the following link syntax:</span></span>

- <span data-ttu-id="f02df-118">目錄中的文章連結到相同目錄中的另一篇文章：</span><span class="sxs-lookup"><span data-stu-id="f02df-118">An article in a directory links to another article in the same directory:</span></span>

  `[link text](article-name.md)`

- <span data-ttu-id="f02df-119">從子目錄連結到根目錄中之文章的文章：</span><span class="sxs-lookup"><span data-stu-id="f02df-119">An article links from a subdirectory to an article in the root directory:</span></span>

  `[link text](../article-name.md)`

- <span data-ttu-id="f02df-120">根目錄中的文章連結到子目錄中的文章：</span><span class="sxs-lookup"><span data-stu-id="f02df-120">An article in the root directory links to an article in a subdirectory:</span></span>

  `[link text](./directory/article-name.md)`

- <span data-ttu-id="f02df-121">子目錄中的文章連結到另一個子目錄中的文章：</span><span class="sxs-lookup"><span data-stu-id="f02df-121">An article in a subdirectory links to an article in another subdirectory:</span></span>

  `[link text](../directory/article-name.md)`

- <span data-ttu-id="f02df-122">跨 docset 連結的文章 (即使在同一個存放庫)：`[link text](./directory/article-name)`</span><span class="sxs-lookup"><span data-stu-id="f02df-122">An article linking across docsets (even if in the same repository): `[link text](./directory/article-name)`</span></span>
  
## <a name="links-to-anchors"></a><span data-ttu-id="f02df-123">連結到錨點</span><span class="sxs-lookup"><span data-stu-id="f02df-123">Links to anchors</span></span>

<span data-ttu-id="f02df-124">您不需要建立錨點。</span><span class="sxs-lookup"><span data-stu-id="f02df-124">You do not have to create anchors.</span></span> <span data-ttu-id="f02df-125">它們在所有 H2 標題發佈時會自動產生。</span><span class="sxs-lookup"><span data-stu-id="f02df-125">They're automatically generated at publishing time for all H2 headings.</span></span> <span data-ttu-id="f02df-126">您唯一需要做的就是建立 H2 小節的連結。</span><span class="sxs-lookup"><span data-stu-id="f02df-126">The only thing you have to do is create links to the H2 sections.</span></span>

- <span data-ttu-id="f02df-127">連結到相同文章中的標題：</span><span class="sxs-lookup"><span data-stu-id="f02df-127">To link to a heading within the same article:</span></span>

  `[link](#the-text-of-the-H2-section-separated-by-hyphens)`
  `[Create cache](#create-cache)`

- <span data-ttu-id="f02df-128">連結到相同子目錄另一篇文章中的錨點：</span><span class="sxs-lookup"><span data-stu-id="f02df-128">To link to an anchor in another article in the same subdirectory:</span></span>

  `[link text](article-name.md#anchor-name)`
  `[Configure your profile](media-services-create-account.md#configure-your-profile)`

- <span data-ttu-id="f02df-129">連結到另一個服務子目錄中的錨點：</span><span class="sxs-lookup"><span data-stu-id="f02df-129">To link to an anchor in another service subdirectory:</span></span>

  `[link text](../directory/article-name.md#anchor-name)`
  `[Configure your profile](../directory/media-services-create-account.md#configure-your-profile)`

## <a name="links-from-includes"></a><span data-ttu-id="f02df-130">從包含檔案的連結</span><span class="sxs-lookup"><span data-stu-id="f02df-130">Links from includes</span></span>

<span data-ttu-id="f02df-131">因為包含檔案位於另一個目錄中，所以您必須使用較長的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="f02df-131">Because include files are located in another directory, you must use longer relative paths.</span></span> <span data-ttu-id="f02df-132">若要從包含檔案連結到文章，請使用此格式：</span><span class="sxs-lookup"><span data-stu-id="f02df-132">To link to an article from an include file, use this format:</span></span>

    [link text](../articles/folder/article-name.md)

## <a name="links-in-selectors"></a><span data-ttu-id="f02df-133">選取器中的連結</span><span class="sxs-lookup"><span data-stu-id="f02df-133">Links in selectors</span></span>

<span data-ttu-id="f02df-134">如果您和 Azure 文件小組一樣，擁有內嵌在包含檔案中的選擇器，則可以使用下列連結結構：</span><span class="sxs-lookup"><span data-stu-id="f02df-134">If you have selectors that are embedded in an include--as does the Azure documentation team--use the following link structure:</span></span>

    > <span data-ttu-id="f02df-135">[AZURE.SELECTOR-LIST (下拉式清單1 | 下拉式清單2 )]</span><span class="sxs-lookup"><span data-stu-id="f02df-135">[AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]</span></span>
    - [<span data-ttu-id="f02df-136">(文字1 | 範例1 )</span><span class="sxs-lookup"><span data-stu-id="f02df-136">(Text1 | Example1 )</span></span>](../articles/folder/article-name1.md)
    - [<span data-ttu-id="f02df-137">(文字1 | 範例2 )</span><span class="sxs-lookup"><span data-stu-id="f02df-137">(Text1 | Example2 )</span></span>](../articles/folder/article-name2.md)
    - [<span data-ttu-id="f02df-138">(文字2 | 範例3 )</span><span class="sxs-lookup"><span data-stu-id="f02df-138">(Text2 | Example3 )</span></span>](../articles/folder/article-name3.md)
    - <span data-ttu-id="f02df-139">[(文字2 | 範例4 )](../articles/folder/article-name4.md) --></span><span class="sxs-lookup"><span data-stu-id="f02df-139">[(Text2 | Example4 )](../articles/folder/article-name4.md) --></span></span>

## <a name="reference-style-links"></a><span data-ttu-id="f02df-140">參考風格連結</span><span class="sxs-lookup"><span data-stu-id="f02df-140">Reference-style links</span></span>

<span data-ttu-id="f02df-141">您可以使用參考風格連結，讓來源內容更容易閱讀。</span><span class="sxs-lookup"><span data-stu-id="f02df-141">You can use reference-style links to make your source content easier to read.</span></span> <span data-ttu-id="f02df-142">參考風格連結會將內嵌連結語法取代為簡化語法，允許您將較長的 URL 移動到文章的結尾。</span><span class="sxs-lookup"><span data-stu-id="f02df-142">Reference-style links replace inline link syntax with simplified syntax that allows you to move the long URLs to the end of the article.</span></span> <span data-ttu-id="f02df-143">以下是 [Daring Fireball](https://daringfireball.net/projects/markdown/) 的範例：</span><span class="sxs-lookup"><span data-stu-id="f02df-143">Here's [Daring Fireball](https://daringfireball.net/projects/markdown/) 's example:</span></span>

<span data-ttu-id="f02df-144">內嵌文字：</span><span class="sxs-lookup"><span data-stu-id="f02df-144">Inline text:</span></span>

    I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].

<span data-ttu-id="f02df-145">文章結尾處的連結參考：</span><span class="sxs-lookup"><span data-stu-id="f02df-145">Link references at the end of the article:</span></span>

    <!--Reference links in article-->
    [1]: http://google.com/
    [2]: http://search.yahoo.com/
    [3]: http://search.msn.com/

<span data-ttu-id="f02df-146">請確定您包含冒號之後的空格 (連結之前)。</span><span class="sxs-lookup"><span data-stu-id="f02df-146">Make sure that you include the space after the colon, before the link.</span></span> <span data-ttu-id="f02df-147">當您連結到其他技術文章時，如果忘記包含空格，已發佈的文章中的連結將會中斷。</span><span class="sxs-lookup"><span data-stu-id="f02df-147">When you link to other technical articles, if you forget to include the space, the link will be broken in the published article.</span></span>

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a><span data-ttu-id="f02df-148">連結到不屬於技術文件集的頁面</span><span class="sxs-lookup"><span data-stu-id="f02df-148">Links to pages that are not part of the technical documentation set</span></span>

<span data-ttu-id="f02df-149">若要連結到另一個 Microsoft 財產上的頁面 (例如定價頁面、SLA 頁面或任何不屬於文件文章的頁面)，請使用絕對 URL，但省略地區設定。</span><span class="sxs-lookup"><span data-stu-id="f02df-149">To link to a page on another Microsoft property (such as a pricing page, SLA page, or anything else that is not a documentation article), use an absolute URL, but omit the locale.</span></span> <span data-ttu-id="f02df-150">這裡的目標是連結可在 GitHub 和轉譯的網站上運作：</span><span class="sxs-lookup"><span data-stu-id="f02df-150">The goal here is that links work in GitHub and on the rendered site:</span></span>

    [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)

## <a name="links-to-third-party-sites"></a><span data-ttu-id="f02df-151">連結到協力廠商網站</span><span class="sxs-lookup"><span data-stu-id="f02df-151">Links to third-party sites</span></span>

<span data-ttu-id="f02df-152">最佳使用者體驗會減少將使用者傳送到其他網站的情況。</span><span class="sxs-lookup"><span data-stu-id="f02df-152">The best user experience minimizes sending users to another site.</span></span> <span data-ttu-id="f02df-153">因此，以此資訊作為我們有時需要之任何協力廠商網站連結的基礎：</span><span class="sxs-lookup"><span data-stu-id="f02df-153">So base any links to third-party sites, which we do sometimes need, on this info:</span></span>

- <span data-ttu-id="f02df-154">**責任：**當您想要共用的資訊是協力廠商資訊時，連結到協力廠商內容。</span><span class="sxs-lookup"><span data-stu-id="f02df-154">**Accountability**: Link to third-party content when it's the third-party's information to share.</span></span> <span data-ttu-id="f02df-155">例如，告知大家如何使用 Android 開發人員工具，並不是 Microsoft 的立場，那是 Google 的資訊。</span><span class="sxs-lookup"><span data-stu-id="f02df-155">For example, it's not Microsoft's place to tell people how to use Android developer tools--that is Google's story to tell.</span></span> <span data-ttu-id="f02df-156">如果有需要，我們可以解釋如何*搭配* Azure 使用 Android 開發人員工具，但 Google 應該說明如何使用其工具。</span><span class="sxs-lookup"><span data-stu-id="f02df-156">If we need to, we can explain how to use Android developer tools *with* Azure, but Google should tell the story of how to use their tools.</span></span>
- <span data-ttu-id="f02df-157">**PM 簽核**：要求 Microsoft 簽核協力廠商內容。</span><span class="sxs-lookup"><span data-stu-id="f02df-157">**PM signoff**: Request that Microsoft sign off on third-party content.</span></span> <span data-ttu-id="f02df-158">透過與之連結，表示我們對其信任以及我們在人們遵循指示時的義務。</span><span class="sxs-lookup"><span data-stu-id="f02df-158">By linking to it, we are saying something about our trust in it and our obligation if people follow the instructions.</span></span>
- <span data-ttu-id="f02df-159">**最新評論**：確定協力廠商資訊仍是最新、正確且相關，且連結並未變更。</span><span class="sxs-lookup"><span data-stu-id="f02df-159">**Freshness reviews**: Make sure that the third-party info is still current, correct, and relevant, and that the link hasn’t changed.</span></span>
- <span data-ttu-id="f02df-160">**異地**：讓使用者了解他們會前往另一個網站。</span><span class="sxs-lookup"><span data-stu-id="f02df-160">**Offsite**: Make users aware that they are going to another site.</span></span> <span data-ttu-id="f02df-161">如果上下文不清楚，請加入一個限定詞組。</span><span class="sxs-lookup"><span data-stu-id="f02df-161">If the context does not make that clear, add a qualifying phrase.</span></span> <span data-ttu-id="f02df-162">例如：「先決條件包括 Android 開發人員工具，您可以在 Android Studio 網站上下載。」</span><span class="sxs-lookup"><span data-stu-id="f02df-162">For example: “Prerequisites include the Android Developer Tools, which you can download on the Android Studio site.”</span></span>
- <span data-ttu-id="f02df-163">**後續步驟**：假設在 [後續步驟] 區段中加入 MVP 部落格連結，是可以接受的。</span><span class="sxs-lookup"><span data-stu-id="f02df-163">**Next steps**: It’s fine to add a link to, say, an MVP blog in a "Next steps" section.</span></span> <span data-ttu-id="f02df-164">同樣地，只要確認使用者了解他們將會離開網站。</span><span class="sxs-lookup"><span data-stu-id="f02df-164">Again, just make sure that users understand they’ll be leaving the site.</span></span>
- <span data-ttu-id="f02df-165">**合法**：我們在每個 ms.com 頁面的＜使用規定＞頁尾中合法地涵蓋了協力廠商網站的連結。</span><span class="sxs-lookup"><span data-stu-id="f02df-165">**Legal**: We are covered legally under **Links to Third Party Sites** in the **Terms of Use** footer on every ms.com page.</span></span>

## <a name="links-to-msdn-or-technet"></a><span data-ttu-id="f02df-166">連結到 MSDN 或 TechNet</span><span class="sxs-lookup"><span data-stu-id="f02df-166">Links to MSDN or TechNet</span></span>

<span data-ttu-id="f02df-167">當您需要連結到 MSDN 或 TechNet 時，請使用該主題的完整連結，並從連結中移除 "en-us" 語言地區設定。</span><span class="sxs-lookup"><span data-stu-id="f02df-167">When you need to link to MSDN or TechNet, use the full link to the topic, and remove the "en-us" language locale from the link.</span></span>

## <a name="links-to-azure-powershell-reference-content"></a><span data-ttu-id="f02df-168">連結到 Azure PowerShell 參考內容</span><span class="sxs-lookup"><span data-stu-id="f02df-168">Links to Azure PowerShell reference content</span></span>

<span data-ttu-id="f02df-169">自從 2016 年 11 月起，Azure PowerShell 參考內容已經過數次變更。</span><span class="sxs-lookup"><span data-stu-id="f02df-169">The Azure PowerShell reference content has been through several changes since November 2016.</span></span> <span data-ttu-id="f02df-170">使用以下指導方針，從 docs.microsoft.com 上其他文章連結到此內容。</span><span class="sxs-lookup"><span data-stu-id="f02df-170">Use the following guidelines for linking to this content from other articles on docs.microsoft.com.</span></span>

<span data-ttu-id="f02df-171">URL 的結構：</span><span class="sxs-lookup"><span data-stu-id="f02df-171">Structure of the URL:</span></span>

* <span data-ttu-id="f02df-172">針對 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f02df-172">For cmdlets:</span></span>
  - `/powershell/module/<module-name>/<cmdlet-name>[?view=<moniker-name>]`
* <span data-ttu-id="f02df-173">針對概念性主題：</span><span class="sxs-lookup"><span data-stu-id="f02df-173">For conceptual topics:</span></span>
  - `/powershell/azure/<topic-file-name>[?view=<moniker-name>]`
  - `/powershell/azure/<service-name>/<topic-file-name>[?view=<moniker-name>]`

<span data-ttu-id="f02df-174">&lt;moniker-name&gt; 部分是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="f02df-174">The &lt;moniker-name&gt; portion is optional.</span></span> <span data-ttu-id="f02df-175">如果省略，您將會被導向至最新版本的內容。</span><span class="sxs-lookup"><span data-stu-id="f02df-175">If it's omitted, you will be directed to the latest version of the content.</span></span> <span data-ttu-id="f02df-176">&lt;service-name&gt; 部分是下列基底 URL中顯示的範例之一：</span><span class="sxs-lookup"><span data-stu-id="f02df-176">The &lt;service-name&gt; portion is one of the examples shown in the following base URLs:</span></span>

- <span data-ttu-id="f02df-177">Azure PowerShell (AzureRM) 內容：https://docs.microsoft.com/powershell/azure/</span><span class="sxs-lookup"><span data-stu-id="f02df-177">Azure PowerShell (AzureRM) content: https://docs.microsoft.com/powershell/azure/</span></span>
- <span data-ttu-id="f02df-178">Azure PowerShell (ASM) 內容：https://docs.microsoft.com/powershell/azure/_servicemanagement_</span><span class="sxs-lookup"><span data-stu-id="f02df-178">Azure PowerShell (ASM) content: https://docs.microsoft.com/powershell/azure/_servicemanagement_</span></span>
- <span data-ttu-id="f02df-179">Azure Active Directory (AzureAD) PowerShell 內容：https://docs.microsoft.com/powershell/azure/_active-directory_</span><span class="sxs-lookup"><span data-stu-id="f02df-179">Azure Active Directory (AzureAD) PowerShell content: https://docs.microsoft.com/powershell/azure/_active-directory_</span></span>
- <span data-ttu-id="f02df-180">Azure Service Fabric PowerShell：https://docs.microsoft.com/powershell/azure/_service-fabric_</span><span class="sxs-lookup"><span data-stu-id="f02df-180">Azure Service Fabric PowerShell: https://docs.microsoft.com/powershell/azure/_service-fabric_</span></span>
- <span data-ttu-id="f02df-181">Azure 資訊保護 PowerShell：https://docs.microsoft.com/powershell/azure/_aip_</span><span class="sxs-lookup"><span data-stu-id="f02df-181">Azure Information Protection PowerShell: https://docs.microsoft.com/powershell/azure/_aip_</span></span>
- <span data-ttu-id="f02df-182">Azure Elastic DB Jobs PowerShell：https://docs.microsoft.com/powershell/azure/_elasticdbjobs_</span><span class="sxs-lookup"><span data-stu-id="f02df-182">Azure Elastic DB Jobs PowerShell: https://docs.microsoft.com/powershell/azure/_elasticdbjobs_</span></span>

<span data-ttu-id="f02df-183">當您使用這些 URL 時，將會被重新導向至最新版本的內容。</span><span class="sxs-lookup"><span data-stu-id="f02df-183">When you use these URLs, you will be redirected to the latest version of the content.</span></span> <span data-ttu-id="f02df-184">這樣您就不必指定版本 Moniker。</span><span class="sxs-lookup"><span data-stu-id="f02df-184">This way, you don't have to specify a version moniker.</span></span> <span data-ttu-id="f02df-185">這避免了在版本變更時，必須更新概念性內容連結的問題。</span><span class="sxs-lookup"><span data-stu-id="f02df-185">And you won't have links to conceptual content that must be updated when the version changes.</span></span>

<span data-ttu-id="f02df-186">若要建立正確的連結，請在瀏覽器中找到要連結的頁面並複製該 URL。</span><span class="sxs-lookup"><span data-stu-id="f02df-186">To create the correct link, find the page that you want to link to in your browser, and copy the URL.</span></span>
<span data-ttu-id="f02df-187">然後，移除 "https://docs.microsoft.com" 和地區設定資訊。</span><span class="sxs-lookup"><span data-stu-id="f02df-187">Then, remove "https://docs.microsoft.com" and the locale info.</span></span>

<span data-ttu-id="f02df-188">當您從 TOC 連結時，您必須使用不包含地區設定資訊的完整 URL。</span><span class="sxs-lookup"><span data-stu-id="f02df-188">When you're linking from a TOC, you must use the full URL without the locale information.</span></span>

<span data-ttu-id="f02df-189">範例 Markdown：</span><span class="sxs-lookup"><span data-stu-id="f02df-189">Example markdown:</span></span>

```markdown
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup)
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup?view=azurermps-4.1.0)
[New-AzureVM](/powershell/module/azure/new-azurevm?view=azuresmps-4.0.0)
[New-AzureRmVM](/powershell/module/azurerm.compute/new-azurermvm)
[Install Azure PowerShell for Service Management](/powershell/azure/servicemanagement/install-azurerm-ps)
[Install Azure PowerShell](/powershell/azure/install-azurerm-ps)
```
