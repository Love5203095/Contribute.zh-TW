---
title: PowerShell 文章的範本和速查表
description: 本文包含一個方便的範本，您可以使用該範本為 PowerShell 文件建立新文章
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 073a44240b1aa4baa9e655dab069097d21cdd66d
ms.sourcegitcommit: 804a99b89785e5c8f056a9da3f0fbde9f0a56a51
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2020
ms.locfileid: "78331921"
---
# <a name="markdown-style-guide-for-powershell-docs"></a><span data-ttu-id="56d3d-103">適用於 PowerShell 文件的 Markdown 樣式指南</span><span class="sxs-lookup"><span data-stu-id="56d3d-103">Markdown style guide for PowerShell-Docs</span></span>

<span data-ttu-id="56d3d-104">本文提供一些 PowerShell 文件內容特定的樣式指導。</span><span class="sxs-lookup"><span data-stu-id="56d3d-104">This article provides some style guidance specific to the PowerShell-Docs content.</span></span>

<span data-ttu-id="56d3d-105">如需其他撰寫樣式指導，請參閱 [Microsoft 樣式指南](https://docs.microsoft.com/style-guide/welcome/)。</span><span class="sxs-lookup"><span data-stu-id="56d3d-105">For other writing style guidance, see the [Microsoft Style Guide](https://docs.microsoft.com/style-guide/welcome/).</span></span>

## <a name="metadata"></a><span data-ttu-id="56d3d-106">中繼資料</span><span class="sxs-lookup"><span data-stu-id="56d3d-106">Metadata</span></span>

<span data-ttu-id="56d3d-107">此範本包含 Markdown 語法的範例，以及設定中繼資料的指導。</span><span class="sxs-lookup"><span data-stu-id="56d3d-107">This template contains examples of Markdown syntax, as well as guidance on setting the metadata.</span></span>
<span data-ttu-id="56d3d-108">當建立 Markdown 檔案時，您應將包含的範本複製到新檔案中、依照如下指定來填寫中繼資料，並將以上 H1 標題設為文章標題。</span><span class="sxs-lookup"><span data-stu-id="56d3d-108">When creating a Markdown file, you should copy the included template to a new file, fill out the metadata as specified below, and set the H1 heading above to the title of the article.</span></span>

<span data-ttu-id="56d3d-109">所需的中繼資料區塊位於下列範例中繼資料區塊中：</span><span class="sxs-lookup"><span data-stu-id="56d3d-109">The required metadata block is in the following sample metadata block:</span></span>

```md
---
author: [GITHUB USERNAME]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
title: [ARTICLE TITLE]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- <span data-ttu-id="56d3d-110">冒號 (:) 和中繼資料項目的值之間**必須**有空格。</span><span class="sxs-lookup"><span data-stu-id="56d3d-110">You **must** have a space between the colon (:) and the value for a metadata element.</span></span>
- <span data-ttu-id="56d3d-111">值中的冒號 (例如標題) 會中斷中繼資料解析器。</span><span class="sxs-lookup"><span data-stu-id="56d3d-111">Colons in a value (for example, a title) break the metadata parser.</span></span> <span data-ttu-id="56d3d-112">在此情況下，請使用雙引號來括住標題 (例如 `title: "Writing .NET Core console apps: An advanced step-by-step guide"`)。</span><span class="sxs-lookup"><span data-stu-id="56d3d-112">In this case, surround the title with double quotes (for example, `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span></span>
- <span data-ttu-id="56d3d-113">**作者**：作者欄位應包含作者的 **GitHub 使用者名稱**。</span><span class="sxs-lookup"><span data-stu-id="56d3d-113">**author**: The author field should contain the **GitHub username** of the author.</span></span>
- <span data-ttu-id="56d3d-114">**描述**：會摘要文章的內容。</span><span class="sxs-lookup"><span data-stu-id="56d3d-114">**description**: Summarizes the content of the article.</span></span> <span data-ttu-id="56d3d-115">通常會顯示於搜尋結果頁面，但不會用於搜尋排名。</span><span class="sxs-lookup"><span data-stu-id="56d3d-115">It's usually shown in the search results page, but it isn't used for search ranking.</span></span> <span data-ttu-id="56d3d-116">長度應為 115-145 個字元，包括空格。</span><span class="sxs-lookup"><span data-stu-id="56d3d-116">Its length should be 115-145 characters including spaces.</span></span>
- <span data-ttu-id="56d3d-117">**ms.date**：上次重大更新的日期。</span><span class="sxs-lookup"><span data-stu-id="56d3d-117">**ms.date**: The date of the last significant update.</span></span> <span data-ttu-id="56d3d-118">如果您已檢閱並更新整篇文章，請在現有文章中對此進行更新。</span><span class="sxs-lookup"><span data-stu-id="56d3d-118">Update this on existing articles if you reviewed and updated the entire article.</span></span> <span data-ttu-id="56d3d-119">錯字或類似內容的小修正不保證會更新。</span><span class="sxs-lookup"><span data-stu-id="56d3d-119">Small fixes, such as typos or similar don't warrant an update.</span></span>
- <span data-ttu-id="56d3d-120">**標題**：會出現在搜尋引擎結果中。</span><span class="sxs-lookup"><span data-stu-id="56d3d-120">**title**: Appears in search engine results.</span></span> <span data-ttu-id="56d3d-121">標題不應與 H1 標題中的標題相同，且不應超過 60 個字元。</span><span class="sxs-lookup"><span data-stu-id="56d3d-121">The title shouldn't be identical to the title in your H1 heading, and it should contain 60 characters or fewer.</span></span>

<span data-ttu-id="56d3d-122">其他中繼資料會附加至每篇文章，但我們通常會在資料夾層級套用大多數中繼資料值 (在 **docfx.json** 中指定)。</span><span class="sxs-lookup"><span data-stu-id="56d3d-122">Other metadata is attached to each article, but we typically apply most metadata values at the folder level, specified in **docfx.json**.</span></span>

## <a name="product-terminology"></a><span data-ttu-id="56d3d-123">產品術語</span><span class="sxs-lookup"><span data-stu-id="56d3d-123">Product Terminology</span></span>

<span data-ttu-id="56d3d-124">PowerShell 的變數有好幾種。</span><span class="sxs-lookup"><span data-stu-id="56d3d-124">There are several variants of PowerShell.</span></span> <span data-ttu-id="56d3d-125">下表定義一些用來討論 PowerShell 的不同字詞。</span><span class="sxs-lookup"><span data-stu-id="56d3d-125">This table defines some of the different terms used to discuss PowerShell.</span></span>

- <span data-ttu-id="56d3d-126">**PowerShell** - 此為預設值。</span><span class="sxs-lookup"><span data-stu-id="56d3d-126">**PowerShell** - This is the default.</span></span> <span data-ttu-id="56d3d-127">PowerShell 是我們的隨附產品。</span><span class="sxs-lookup"><span data-stu-id="56d3d-127">PowerShell is the product we ship.</span></span> <span data-ttu-id="56d3d-128">PowerShell 一詞可用於描述產品的任何版本。</span><span class="sxs-lookup"><span data-stu-id="56d3d-128">The term PowerShell can be used to describe any edition of the product.</span></span>
- <span data-ttu-id="56d3d-129">**PowerShell Core** - 針對任何支援的平台，以 .NET Core Common Language Runtime (CoreCLR) 為基礎建置的 PowerShell。</span><span class="sxs-lookup"><span data-stu-id="56d3d-129">**PowerShell Core** - PowerShell built on .NET Core Common Language Runtime (CoreCLR) for any of the supported platforms.</span></span>
- <span data-ttu-id="56d3d-130">**Windows PowerShell** - 以 .NET Framework Common Language Runtime (CLR) 為基礎建置的 PowerShell。</span><span class="sxs-lookup"><span data-stu-id="56d3d-130">**Windows PowerShell** - PowerShell built on .NET Framework Common Language Runtime (CLR).</span></span> <span data-ttu-id="56d3d-131">Windows PowerShell 只隨附於 Windows，且需要完整的 .Net Framework CLR。</span><span class="sxs-lookup"><span data-stu-id="56d3d-131">Windows PowerShell ships only on Windows and requires the full .Net Framework CLR.</span></span>

<span data-ttu-id="56d3d-132">一般而言，文件中的 "Windows PowerShell" 參考可以變更為 "PowerShell"。</span><span class="sxs-lookup"><span data-stu-id="56d3d-132">In general, references to "Windows PowerShell" in documentation can be changed to "PowerShell".</span></span>
<span data-ttu-id="56d3d-133">但在討論 Windows 特定技術時，**不**應該變更 "Windows PowerShell"。</span><span class="sxs-lookup"><span data-stu-id="56d3d-133">"Windows PowerShell" should **not** be changed when Windows-specific technology is being discussed.</span></span>

## <a name="basic-markdown-gfm-and-special-characters"></a><span data-ttu-id="56d3d-134">基本 Markdown、GFM 和特殊字元</span><span class="sxs-lookup"><span data-stu-id="56d3d-134">Basic Markdown, GFM, and special characters</span></span>

<span data-ttu-id="56d3d-135">您可以透過 [Markdown 參考](../markdown-reference.md)一文了解 Markdown、GitHub Flavored Markdown (GFM) 和 OPS 特定延伸模組的基本知識。</span><span class="sxs-lookup"><span data-stu-id="56d3d-135">You can learn the basics of Markdown, GitHub Flavored Markdown (GFM), and OPS specific extensions in the [Markdown reference](../markdown-reference.md) article.</span></span>

<span data-ttu-id="56d3d-136">Markdown 使用 \*、\` 和 \# 等特殊字元來格式化。</span><span class="sxs-lookup"><span data-stu-id="56d3d-136">Markdown uses special characters such as \*, \`, and \# for formatting.</span></span> <span data-ttu-id="56d3d-137">如果您希望將其中一個字元包含在內容中，則必須執行以下兩項作業之一：</span><span class="sxs-lookup"><span data-stu-id="56d3d-137">If you wish to include one of these characters in your content, you must do one of two things:</span></span>

- <span data-ttu-id="56d3d-138">在特殊字元前加上一個反斜線以將其「逸出」 (例如 `\*` 對於 \*)</span><span class="sxs-lookup"><span data-stu-id="56d3d-138">Put a backslash before the special character to "escape" it (for example, `\*` for a \*)</span></span>
- <span data-ttu-id="56d3d-139">為字元使用 [HTML 實體程式碼](http://www.ascii.cl/htmlcodes.htm) (例如，`&#42;` 對於 &#42;)。</span><span class="sxs-lookup"><span data-stu-id="56d3d-139">Use the [HTML entity code](http://www.ascii.cl/htmlcodes.htm) for the character (for example, `&#42;` for a &#42;).</span></span>
- <span data-ttu-id="56d3d-140">Markdown 檔案應使用 ASCII 純文字或 UTF-8 編碼。</span><span class="sxs-lookup"><span data-stu-id="56d3d-140">Markdown files should use plain ASCII text or UTF-8 encoding.</span></span> <span data-ttu-id="56d3d-141">不過，需避免使用多位元組 UTF-8 字元。</span><span class="sxs-lookup"><span data-stu-id="56d3d-141">However, avoid using multi-byte UTF-8 characters.</span></span> <span data-ttu-id="56d3d-142">請改用 HTML 實體。</span><span class="sxs-lookup"><span data-stu-id="56d3d-142">Instead use an HTML entity.</span></span> <span data-ttu-id="56d3d-143">例如，若為著作權符號，請使用 `&copy;`。</span><span class="sxs-lookup"><span data-stu-id="56d3d-143">For example, for the copyright symbols use `&copy;`.</span></span>
  <span data-ttu-id="56d3d-144">其呈現為："&copy;"。</span><span class="sxs-lookup"><span data-stu-id="56d3d-144">It is rendered as: "&copy;".</span></span>

## <a name="hyperlinks"></a><span data-ttu-id="56d3d-145">超連結</span><span class="sxs-lookup"><span data-stu-id="56d3d-145">Hyperlinks</span></span>

- <span data-ttu-id="56d3d-146">請避免使用裸機 URL。</span><span class="sxs-lookup"><span data-stu-id="56d3d-146">Avoid using bare URLs.</span></span> <span data-ttu-id="56d3d-147">連結應使用 Markdown 語法 `[friendlyname](url-or-path)`</span><span class="sxs-lookup"><span data-stu-id="56d3d-147">Links should use Markdown syntax `[friendlyname](url-or-path)`</span></span>
- <span data-ttu-id="56d3d-148">連結必須具有易記名稱，通常是連結主題的標題</span><span class="sxs-lookup"><span data-stu-id="56d3d-148">Links must have a friendly name, usually the title of the linked topic</span></span>
- <span data-ttu-id="56d3d-149">底部＜相關連結＞一節中的所有項目都應該是超連結。</span><span class="sxs-lookup"><span data-stu-id="56d3d-149">All items in the "related links" section at the bottom should be hyperlinked.</span></span>
- <span data-ttu-id="56d3d-150">連結至裝載於 **docs.microsoft.com** 的其他內容時，請使用相對連結。</span><span class="sxs-lookup"><span data-stu-id="56d3d-150">Use relative links when linking to other content that is hosted on **docs.microsoft.com**.</span></span>
- <span data-ttu-id="56d3d-151">請勿在超連結的括弧內使用倒引號、粗體或其他標記。</span><span class="sxs-lookup"><span data-stu-id="56d3d-151">Do not use backticks, bold, or other markup inside the brackets of a hyperlink.</span></span>

<span data-ttu-id="56d3d-152">如需連結的詳細資訊，請參閱[在文件中使用連結](../how-to-write-links.md)。</span><span class="sxs-lookup"><span data-stu-id="56d3d-152">For more detailed information about linking, see [Using links in documentation](../how-to-write-links.md).</span></span>

## <a name="filenames"></a><span data-ttu-id="56d3d-153">檔案名稱</span><span class="sxs-lookup"><span data-stu-id="56d3d-153">Filenames</span></span>

<span data-ttu-id="56d3d-154">檔案名稱使用下列規則：</span><span class="sxs-lookup"><span data-stu-id="56d3d-154">Filenames use the following rules:</span></span>

- <span data-ttu-id="56d3d-155">只包含字母、數字和連字號。</span><span class="sxs-lookup"><span data-stu-id="56d3d-155">Contain only letters, numbers, and hyphens.</span></span>
- <span data-ttu-id="56d3d-156">沒有空格或標點符號字元。</span><span class="sxs-lookup"><span data-stu-id="56d3d-156">No spaces or punctuation characters.</span></span> <span data-ttu-id="56d3d-157">檔案名稱中使用連字號來分隔文字和數字。</span><span class="sxs-lookup"><span data-stu-id="56d3d-157">Use the hyphens to separate words and numbers in the file name.</span></span>
- <span data-ttu-id="56d3d-158">使用特定的動作動詞，例如 develop、buy、build、troubleshoot。</span><span class="sxs-lookup"><span data-stu-id="56d3d-158">Use action verbs that are specific, such as develop, buy, build, troubleshoot.</span></span> <span data-ttu-id="56d3d-159">沒有 -ing 字詞。</span><span class="sxs-lookup"><span data-stu-id="56d3d-159">No -ing words.</span></span>
- <span data-ttu-id="56d3d-160">不包含 a、and、the、in、or 等短字。</span><span class="sxs-lookup"><span data-stu-id="56d3d-160">No small words - don't include a, and, the, in, or, etc.</span></span>
- <span data-ttu-id="56d3d-161">必須是 Markdown 格式且使用 .md 副檔名。</span><span class="sxs-lookup"><span data-stu-id="56d3d-161">Must be in Markdown and use the .md file extension.</span></span>
- <span data-ttu-id="56d3d-162">保持檔案名稱合理簡短。</span><span class="sxs-lookup"><span data-stu-id="56d3d-162">Keep file names reasonably short.</span></span> <span data-ttu-id="56d3d-163">它們是您文章 URL 的一部分。</span><span class="sxs-lookup"><span data-stu-id="56d3d-163">They are part of the URL for your articles.</span></span>

## <a name="blank-lines-spaces-and-tabs"></a><span data-ttu-id="56d3d-164">空白行、空格及索引標籤</span><span class="sxs-lookup"><span data-stu-id="56d3d-164">Blank lines, spaces, and tabs</span></span>

<span data-ttu-id="56d3d-165">請移除重複的空白行。</span><span class="sxs-lookup"><span data-stu-id="56d3d-165">Remove duplicate blank lines.</span></span> <span data-ttu-id="56d3d-166">多個空白行在 HTML 中會轉譯為單一空白行，因此不會有多個空白行的用途。</span><span class="sxs-lookup"><span data-stu-id="56d3d-166">Multiple blank lines render as a single blank line in HTML so there is not purpose for multiple blank lines.</span></span>

<span data-ttu-id="56d3d-167">空白行還表示 Markdown 中的區塊結尾。</span><span class="sxs-lookup"><span data-stu-id="56d3d-167">Blank lines also signal the end of a block in Markdown.</span></span> <span data-ttu-id="56d3d-168">不同類型的 Markdown 組塊之間 (例如，段落與清單或標頭之間) 應該有一個空白。</span><span class="sxs-lookup"><span data-stu-id="56d3d-168">There should be a single blank between Markdown blocks of different types (for example, between a paragraph and a list or header).</span></span>

> [!NOTE]
> <span data-ttu-id="56d3d-169">間距在 Markdown 中很重要。</span><span class="sxs-lookup"><span data-stu-id="56d3d-169">Spacing is significant in Markdown.</span></span> <span data-ttu-id="56d3d-170">應一律使用空格，而不是硬性索引標籤。</span><span class="sxs-lookup"><span data-stu-id="56d3d-170">Always uses spaces instead of hard tabs.</span></span> <span data-ttu-id="56d3d-171">請移除行尾的多餘空格。</span><span class="sxs-lookup"><span data-stu-id="56d3d-171">Remove extra spaces at the end of lines.</span></span>

## <a name="titles-and-headings"></a><span data-ttu-id="56d3d-172">標題 (Title) 和標題 (heading)</span><span class="sxs-lookup"><span data-stu-id="56d3d-172">Titles and headings</span></span>

<span data-ttu-id="56d3d-173">僅使用 [ATX 標題][atx] (# 樣式，而不是 `=` 或 `-` 樣式標頭)。</span><span class="sxs-lookup"><span data-stu-id="56d3d-173">Only use [ATX headings][atx] (# style, as opposed to `=` or `-` style headers).</span></span>

- <span data-ttu-id="56d3d-174">使用句首大寫 - 只有專有名詞與標題或標頭的第一個字母應為大寫</span><span class="sxs-lookup"><span data-stu-id="56d3d-174">Use sentence case - only proper nouns and the first letter of a title or header should be capitalized</span></span>
- <span data-ttu-id="56d3d-175">`#` 與標題的第一個字母之間必須有一個空格</span><span class="sxs-lookup"><span data-stu-id="56d3d-175">There must be a single space between the `#` and the first letter of the heading</span></span>
- <span data-ttu-id="56d3d-176">標題應該以單一空白行括住</span><span class="sxs-lookup"><span data-stu-id="56d3d-176">Headings should be surrounded by a single blank line</span></span>
- <span data-ttu-id="56d3d-177">每份文件只能有一個 H1</span><span class="sxs-lookup"><span data-stu-id="56d3d-177">Only one H1 per document</span></span>
- <span data-ttu-id="56d3d-178">標頭層級應該遞增一 - 不要略過層級</span><span class="sxs-lookup"><span data-stu-id="56d3d-178">Header levels should increment by one - do not skip levels</span></span>
- <span data-ttu-id="56d3d-179">請勿在標頭中使用倒引號、粗體或其他標記</span><span class="sxs-lookup"><span data-stu-id="56d3d-179">Do not use backticks, bold, or other markup in headers</span></span>

> [!CAUTION]
> <span data-ttu-id="56d3d-180">[PlatyPS][platyPS] 對 Cmdlet 參考強制執行的結構描述需要特定 H2 和 H3 標頭。</span><span class="sxs-lookup"><span data-stu-id="56d3d-180">The schema enforced by [PlatyPS][platyPS] for cmdlet reference requires specific H2 and H3 headers.</span></span> <span data-ttu-id="56d3d-181">新增或移除標頭可能會中斷組建。</span><span class="sxs-lookup"><span data-stu-id="56d3d-181">Adding or removing headers can break the build.</span></span> <span data-ttu-id="56d3d-182">如需詳細資訊，請參閱 [Cmdlet 參考樣式指南](powershell-style-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="56d3d-182">For more information, see the [cmdlet reference style guide](powershell-style-reference.md).</span></span>

## <a name="limit-line-length-to-100-characters"></a><span data-ttu-id="56d3d-183">將行長度限制為 100 個字元</span><span class="sxs-lookup"><span data-stu-id="56d3d-183">Limit line length to 100 characters</span></span>

<span data-ttu-id="56d3d-184">這可簡化差異和歷程記錄的命令列輸出。</span><span class="sxs-lookup"><span data-stu-id="56d3d-184">This simplifies the command-line output of diffs and history.</span></span>

<span data-ttu-id="56d3d-185">此規則不會對 PowerShell 文件中的大部分現有內容強制執行，但我們正朝著此一方向努力。</span><span class="sxs-lookup"><span data-stu-id="56d3d-185">This rule was not in force for much of the existing content in PowerShell-Docs, but we are working towards it over time.</span></span> <span data-ttu-id="56d3d-186">歡迎您提供協助。Visual Studio Code (VSCode) 中的[自動重排延伸模組][reflow]，可讓您輕鬆地將段落重新格式化為此限制。</span><span class="sxs-lookup"><span data-stu-id="56d3d-186">Feel free to help out. The [reflow extension][reflow] in Visual Studio Code (VSCode) makes it easy to reformat paragraphs to this limit.</span></span>

## <a name="lists"></a><span data-ttu-id="56d3d-187">清單</span><span class="sxs-lookup"><span data-stu-id="56d3d-187">Lists</span></span>

<span data-ttu-id="56d3d-188">如果您的清單包含多個句子或段落，請考慮使用子層級標頭，而不是清單。</span><span class="sxs-lookup"><span data-stu-id="56d3d-188">If your list contains multiple sentences or paragraphs, consider using a sub-level header rather than a list.</span></span>

<span data-ttu-id="56d3d-189">清單應該以單一空白行括住。</span><span class="sxs-lookup"><span data-stu-id="56d3d-189">List should be surrounded by a single blank line.</span></span>

### <a name="unordered-lists"></a><span data-ttu-id="56d3d-190">未排序清單</span><span class="sxs-lookup"><span data-stu-id="56d3d-190">Unordered lists</span></span>

<span data-ttu-id="56d3d-191">請勿以句點結束清單項目，除非它們包含多個句子。</span><span class="sxs-lookup"><span data-stu-id="56d3d-191">Do not end list items with a period unless they contain multiple sentences.</span></span> <span data-ttu-id="56d3d-192">針對清單項目的項目符號，請使用連字號字元 (`-`)。</span><span class="sxs-lookup"><span data-stu-id="56d3d-192">Use the hyphen character (`-`) for list item bullets.</span></span> <span data-ttu-id="56d3d-193">這可避免與使用星號 `*` 的粗體或斜體標記混淆。</span><span class="sxs-lookup"><span data-stu-id="56d3d-193">This avoids confusion with bold or italic markup that uses the asterisk [`*`].</span></span> <span data-ttu-id="56d3d-194">若要在項目符號項目下包含段落或其他項目，請插入分行符號，並與項目符號後面的第一個字元對齊縮排。</span><span class="sxs-lookup"><span data-stu-id="56d3d-194">To include a paragraph or other elements under a bullet item, insert a line break and align indentation with the first character after the bullet.</span></span>

<span data-ttu-id="56d3d-195">例如：</span><span class="sxs-lookup"><span data-stu-id="56d3d-195">For example:</span></span>

```markdown
This is a list that contain sub-elements under a bullet item.

- First bullet item

  Sentence explaining the first bullet.

  - Sub-bullet item

    Sentence explaining the sub-bullet.

- Second bullet item
- Third bullet item
```

<span data-ttu-id="56d3d-196">這是一個清單，其中包含項目符號項目下的子項目。</span><span class="sxs-lookup"><span data-stu-id="56d3d-196">This is a list that contains sub-elements under a bullet item.</span></span>

- <span data-ttu-id="56d3d-197">第一個項目符號項目</span><span class="sxs-lookup"><span data-stu-id="56d3d-197">First bullet item</span></span>

  <span data-ttu-id="56d3d-198">說明第一個項目符號的句子。</span><span class="sxs-lookup"><span data-stu-id="56d3d-198">Sentence explaining the first bullet.</span></span>

  - <span data-ttu-id="56d3d-199">子項目符號項目</span><span class="sxs-lookup"><span data-stu-id="56d3d-199">Sub-bullet item</span></span>

    <span data-ttu-id="56d3d-200">說明子項目符號的句子。</span><span class="sxs-lookup"><span data-stu-id="56d3d-200">Sentence explaining the sub-bullet.</span></span>

- <span data-ttu-id="56d3d-201">第二個項目符號項目</span><span class="sxs-lookup"><span data-stu-id="56d3d-201">Second bullet item</span></span>
- <span data-ttu-id="56d3d-202">第三個項目符號項目</span><span class="sxs-lookup"><span data-stu-id="56d3d-202">Third bullet item</span></span>

### <a name="ordered-lists"></a><span data-ttu-id="56d3d-203">排序清單</span><span class="sxs-lookup"><span data-stu-id="56d3d-203">Ordered lists</span></span>

<span data-ttu-id="56d3d-204">若要在編號項目下包含段落或其他項目，請與項目編號後面的第一個字元對齊縮排。</span><span class="sxs-lookup"><span data-stu-id="56d3d-204">To include a paragraph or other elements under a numbered item, align indentation with the first character after the item number.</span></span>

```markdown
1. For the first element, insert a single space after the 1. Long sentences should be
   wrapped to the next line and must line up with the first character after the numbered
   list marker.

   To include a second element (like this one), insert a line break after the first
   and align indentations. The indentation of the second element must line up with
   the first character after the numbered list marker. For single digit items, like
   this one, you indent to column 4. For double digits items, for example item number
   10, you indent to column 5.

1. The next numbered item starts here.
```

<span data-ttu-id="56d3d-205">取得此輸出：</span><span class="sxs-lookup"><span data-stu-id="56d3d-205">to get this output:</span></span>

> 1. <span data-ttu-id="56d3d-206">針對第一個項目，在 1 之後插入一個空格。</span><span class="sxs-lookup"><span data-stu-id="56d3d-206">For the first element, insert a single space after the 1.</span></span> <span data-ttu-id="56d3d-207">長句子應該換行到下一行，且必須與編號清單標記之後的第一個字元對齊。</span><span class="sxs-lookup"><span data-stu-id="56d3d-207">Long sentences should be wrapped to the next line and must line up with the first character after the numbered list marker.</span></span>
>
>    <span data-ttu-id="56d3d-208">若要包含第二個項目 (例如這一個)，請在第一個項目之後插入分行符號，並對齊縮排。</span><span class="sxs-lookup"><span data-stu-id="56d3d-208">To include a second element (like this one), insert a line break after the first and align indentations.</span></span> <span data-ttu-id="56d3d-209">第二個項目的縮排必須與編號清單標記之後第一個字元對齊。</span><span class="sxs-lookup"><span data-stu-id="56d3d-209">The indentation of the second element must line up with the first character after the numbered list marker.</span></span> <span data-ttu-id="56d3d-210">針對單位數項目 (例如這一個)，您可以縮排到第 4 欄。</span><span class="sxs-lookup"><span data-stu-id="56d3d-210">For single digit items, like this one, you indent to column 4.</span></span> <span data-ttu-id="56d3d-211">針對雙位數項目 (例如項目編號 10)，則會縮排到第 5 欄。</span><span class="sxs-lookup"><span data-stu-id="56d3d-211">For double digits items, for example item number 10, you indent to column 5.</span></span>
>
> 1. <span data-ttu-id="56d3d-212">下一個編號項目會從這裡開始。</span><span class="sxs-lookup"><span data-stu-id="56d3d-212">The next numbered item starts here.</span></span>

<span data-ttu-id="56d3d-213">列出編號中的所有項目都應該使用數字 `1.`，而不是針對每個項目遞增。</span><span class="sxs-lookup"><span data-stu-id="56d3d-213">All items in a numbered listed should use the number `1.` instead of incrementing for each item.</span></span>
<span data-ttu-id="56d3d-214">Markdown 轉譯會自動遞增值。</span><span class="sxs-lookup"><span data-stu-id="56d3d-214">Markdown rendering increments the value automatically.</span></span> <span data-ttu-id="56d3d-215">這會讓重新排列項目變得更加容易，並將附屬內容的縮排標準化。</span><span class="sxs-lookup"><span data-stu-id="56d3d-215">This makes reordering items easier and standardizes the indentation of subordinate content.</span></span>

## <a name="formatting-command-syntax-elements"></a><span data-ttu-id="56d3d-216">格式化命令語法項目</span><span class="sxs-lookup"><span data-stu-id="56d3d-216">Formatting command syntax elements</span></span>

- <span data-ttu-id="56d3d-217">PowerShell Cmdlet 名稱使用 [Pascal 命名法][pascal-case]。</span><span class="sxs-lookup"><span data-stu-id="56d3d-217">PowerShell cmdlet names are [Pascal Cased][pascal-case].</span></span> <span data-ttu-id="56d3d-218">動詞會以連字號與名詞分隔。</span><span class="sxs-lookup"><span data-stu-id="56d3d-218">Verbs are separated from nouns by a hyphen.</span></span> <span data-ttu-id="56d3d-219">請針對 Cmdlet 和參數一律使用完整的 Pascal 命名法名稱。</span><span class="sxs-lookup"><span data-stu-id="56d3d-219">Always use the full Pascal Case name for cmdlets and parameters.</span></span> <span data-ttu-id="56d3d-220">除非您特別討論別名，否則請避免使用別名。</span><span class="sxs-lookup"><span data-stu-id="56d3d-220">Avoid using aliases unless you are specifically talking about an alias.</span></span>

- <span data-ttu-id="56d3d-221">在段落內，語言關鍵字、Cmdlet 名稱及變數參考都應該包裝在倒引號 (`` ` ``) 字元中。</span><span class="sxs-lookup"><span data-stu-id="56d3d-221">Within a paragraph, language keywords, cmdlet names, and variable references should be wrapped in backtick (`` ` ``) characters.</span></span> <span data-ttu-id="56d3d-222">屬性、參數及類別名稱應該是**粗體**。</span><span class="sxs-lookup"><span data-stu-id="56d3d-222">Property, parameter, and class names should be **bold**.</span></span>

  <span data-ttu-id="56d3d-223">例如：</span><span class="sxs-lookup"><span data-stu-id="56d3d-223">For example:</span></span>

  ~~~markdown
  The following code assigns the output of `Get-ChildItem` to the `$files` variable.

  ```powershell
  $files = Get-ChildItem C:\Windows
  ```
  ~~~

- <span data-ttu-id="56d3d-224">透過名稱參考參數時，名稱應該是**粗體**。</span><span class="sxs-lookup"><span data-stu-id="56d3d-224">When referring to a parameter by name, the name should be **bold**.</span></span> <span data-ttu-id="56d3d-225">在說明使用含連字號前置詞的參數時，參數應包裝在倒引號中。</span><span class="sxs-lookup"><span data-stu-id="56d3d-225">When illustrating the use of a parameter with the hyphen prefix, the parameter should be wrapped in backticks.</span></span> <span data-ttu-id="56d3d-226">例如：</span><span class="sxs-lookup"><span data-stu-id="56d3d-226">For example:</span></span>

  ```markdown
  The parameter's name is **Name**, but it is typed as `-Name` when used on the command
  line as a parameter.
  ```

- <span data-ttu-id="56d3d-227">參考外部命令 (EXE、指令碼等) 時，命令名稱應為粗體、全部小寫 (如果在句子開頭則為大寫)，並包含適當的副檔名。</span><span class="sxs-lookup"><span data-stu-id="56d3d-227">When referring to external commands (EXEs, scripts, etc.), the command name should be bold, all lowercase (or capitalized if at the beginning of a sentence), and include the appropriate file extension.</span></span> <span data-ttu-id="56d3d-228">例如：</span><span class="sxs-lookup"><span data-stu-id="56d3d-228">For example:</span></span>

  ```markdown
  For example, on Windows systems, you can use the `net start` and `net stop` commands
  to start and stop a service. **Sc.exe** is another service control tool for Windows.
  That name does not fit into the naming pattern for the **net.exe** service commands.
  ```

- <span data-ttu-id="56d3d-229">顯示外部命令的範例使用方式時，應將此範例包裝在倒引號中。</span><span class="sxs-lookup"><span data-stu-id="56d3d-229">When showing example usage of an external command, the example should be wrapped in backticks.</span></span>
  <span data-ttu-id="56d3d-230">當名稱與別名發生衝突時，您必須在命令範例中包含副檔名。</span><span class="sxs-lookup"><span data-stu-id="56d3d-230">When there is a name collision with an alias you must include the file extension in the command example.</span></span> <span data-ttu-id="56d3d-231">例如：</span><span class="sxs-lookup"><span data-stu-id="56d3d-231">For example:</span></span>

  ```markdown
  To start the spooler service on a remote computer named DC01, you type `sc.exe \\DC01 start spooler`.
  ```

- <span data-ttu-id="56d3d-232">在撰寫概念性文章 (相對於參考內容) 時，Cmdlet 名稱的第一個執行個體應該會以超連結方式連至 Cmdlet 文件。</span><span class="sxs-lookup"><span data-stu-id="56d3d-232">When writing a conceptual article (as opposed to reference content), the first instance of a cmdlet name should be hyperlinked to the cmdlet documentation.</span></span> <span data-ttu-id="56d3d-233">請勿在超連結的括弧內使用倒引號、粗體或其他標記。</span><span class="sxs-lookup"><span data-stu-id="56d3d-233">Do not use backticks, bold, or other markup inside the brackets of a hyperlink.</span></span>

  <span data-ttu-id="56d3d-234">例如：</span><span class="sxs-lookup"><span data-stu-id="56d3d-234">For example:</span></span>

  ```markdown
  This [Write-Host](/powershell/module/Microsoft.PowerShell.Utility/Write-Host) cmdlet
  uses the **Object** parameter to ...
  ```

  <span data-ttu-id="56d3d-235">如需詳細資訊，請參閱樣式指南的＜超連結＞[](#hyperlinks)一節。</span><span class="sxs-lookup"><span data-stu-id="56d3d-235">For more information, see [Hyperlinks](#hyperlinks) section of the Style Guide.</span></span>

## <a name="images"></a><span data-ttu-id="56d3d-236">影像</span><span class="sxs-lookup"><span data-stu-id="56d3d-236">Images</span></span>

<span data-ttu-id="56d3d-237">包含影像的語法如下：</span><span class="sxs-lookup"><span data-stu-id="56d3d-237">The syntax to include an image is:</span></span>

```Syntax
![[alt text]](<folderPath>)
```

<span data-ttu-id="56d3d-238">範例：</span><span class="sxs-lookup"><span data-stu-id="56d3d-238">Example:</span></span>

```markdown
![Introduction](./media/overview/Introduction.png)
```

<span data-ttu-id="56d3d-239">其中，`alt text` 是影像的簡短描述，而 `<folder path>` 是影像的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="56d3d-239">Where `alt text` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="56d3d-240">適用於視障者的螢幕助讀程式需要使用替代文字。</span><span class="sxs-lookup"><span data-stu-id="56d3d-240">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="56d3d-241">若發生影像無法呈現的網站 Bug 時，替代文字也很實用。</span><span class="sxs-lookup"><span data-stu-id="56d3d-241">It is also useful in case there is a site bug where the image cannot be rendered.</span></span>

<span data-ttu-id="56d3d-242">影像應儲存在包含您文章的資料夾內 `media/<article-name>` 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="56d3d-242">Images should be stored in a `media/<article-name>` folder within the folder containing your article.</span></span> <span data-ttu-id="56d3d-243">不應在文章之間共用影像。</span><span class="sxs-lookup"><span data-stu-id="56d3d-243">Images should not be shared between articles.</span></span> <span data-ttu-id="56d3d-244">請在 `media` 資料夾底下，建立符合您文章檔案名稱的資料夾。</span><span class="sxs-lookup"><span data-stu-id="56d3d-244">Create a folder that matches the filename of your article under the `media` folder.</span></span> <span data-ttu-id="56d3d-245">將該文章的影像複製到該新資料夾。</span><span class="sxs-lookup"><span data-stu-id="56d3d-245">Copy the images for that article to that new folder.</span></span> <span data-ttu-id="56d3d-246">如果有多個文章使用某個影像，則每個影像資料夾都必須有該影像檔案的複本。</span><span class="sxs-lookup"><span data-stu-id="56d3d-246">If an image is used by multiple articles, each image folder must have a copy of that image file.</span></span> <span data-ttu-id="56d3d-247">這種做法可防止某篇文章中的影像變更影響另一篇文章。</span><span class="sxs-lookup"><span data-stu-id="56d3d-247">This practice prevents a change to an image in one article affecting another article.</span></span>

<span data-ttu-id="56d3d-248">在某些情況下，您會想要跨多篇文章共用影像，例如標誌和圖示。</span><span class="sxs-lookup"><span data-stu-id="56d3d-248">In some cases, you want to share images, like logos and icons, across multiple articles.</span></span> <span data-ttu-id="56d3d-249">這些影像會儲存在存放庫根目錄的 `/media/shared` 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="56d3d-249">These images are stored in the `/media/shared` folder at the root of the repository.</span></span>

<span data-ttu-id="56d3d-250">支援下列影像檔案類型：*.png"、*.gif"、*.jpeg"、*.jpg"、\*.svg</span><span class="sxs-lookup"><span data-stu-id="56d3d-250">The following image file types are supported: \*.png", \*.gif", \*.jpeg", \*.jpg", \*.svg</span></span>

<!-- External URLs -->
[platyPS]: https://github.com/PowerShell/platyPS
[markdig]: https://github.com/lunet-io/markdig
[CommonMark]: https://spec.commonmark.org/
[atx]: https://github.github.com/gfm/#atx-headings
[pascal-case]: https://en.wikipedia.org/wiki/PascalCase
[reflow]: https://marketplace.visualstudio.com/items?itemName=marvhen.reflow-markdown
