---
title: docs.microsoft.com 的 Markdown 參考
description: 了解 Microsoft Docs 平台中所使用的 Markdown 功能和語法。
author: meganbradley
ms.author: mbradley
ms.date: 05/18/2018
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.openlocfilehash: 452cbf97db748532ae2b0e09b4bb558c8f757a61
ms.sourcegitcommit: a812d716b31084926b886b93923f9b84c9b23429
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/18/2019
ms.locfileid: "75188264"
---
# <a name="markdown-reference"></a><span data-ttu-id="b754d-103">Markdown 參考</span><span class="sxs-lookup"><span data-stu-id="b754d-103">Markdown Reference</span></span>

<span data-ttu-id="b754d-104">Markdown 是採用純文字格式語法的輕量型標記語言。</span><span class="sxs-lookup"><span data-stu-id="b754d-104">Markdown is a lightweight markup language with plain text formatting syntax.</span></span> <span data-ttu-id="b754d-105">Docs 平台 可支援 Markdown 的 CommonMark 標準，以及為提供 docs.microsoft.com 更豐富內容所設計的一些自訂 Markdown 延伸模組。</span><span class="sxs-lookup"><span data-stu-id="b754d-105">The Docs platform supports the CommonMark standard for Markdown, plus some custom Markdown extensions designed to provide richer content on docs.microsoft.com.</span></span> <span data-ttu-id="b754d-106">本文提供針對 docs.microsoft.com 使用 Markdown 的參考，按字母順序排列。</span><span class="sxs-lookup"><span data-stu-id="b754d-106">This article provides an alphabetical reference for using Markdown for docs.microsoft.com.</span></span>

<span data-ttu-id="b754d-107">您可以使用任何文字編輯器來撰寫 Markdown。</span><span class="sxs-lookup"><span data-stu-id="b754d-107">You can use any text editor to author Markdown.</span></span> <span data-ttu-id="b754d-108">為了讓編輯器可以協助插入標準 Markdown 語法和自訂 Docs 延伸模組，建議您安裝 [VS Code](https://code.visualstudio.com/) 和 [Docs 編寫套件](https://aka.ms/DocsAuthoringPack)。</span><span class="sxs-lookup"><span data-stu-id="b754d-108">For an editor that facilitates inserting both standard Markdown syntax and custom Docs extensions, we recommend [VS Code](https://code.visualstudio.com/) with the [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) installed.</span></span>

<span data-ttu-id="b754d-109">Dos 使用 Markdig Markdown 引擎。</span><span class="sxs-lookup"><span data-stu-id="b754d-109">Docs uses the Markdig Markdown engine.</span></span> <span data-ttu-id="b754d-110">您可以在 [https://babelmark.github.io/](https://babelmark.github.io/) 中測試 Markdig 和其他引擎的 Markdown 呈現。</span><span class="sxs-lookup"><span data-stu-id="b754d-110">You can test the rendering of Markdown in Markdig vs. other engines at [https://babelmark.github.io/](https://babelmark.github.io/).</span></span>

## <a name="alerts-note-tip-important-caution-warning"></a><span data-ttu-id="b754d-111">警示 (附註、提示、重要、注意、警告)</span><span class="sxs-lookup"><span data-stu-id="b754d-111">Alerts (Note, Tip, Important, Caution, Warning)</span></span>

<span data-ttu-id="b754d-112">警示是用來建立區塊引述的 Docs Markdown 延伸模組，該區塊引述會在 docs.microsoft.com 中呈現可指出內容重要性的色彩和圖示。</span><span class="sxs-lookup"><span data-stu-id="b754d-112">Alerts are a Docs Markdown extension to create block quotes that render on docs.microsoft.com with colors and icons that indicate the significance of the content.</span></span> <span data-ttu-id="b754d-113">支援的警示類型如下：</span><span class="sxs-lookup"><span data-stu-id="b754d-113">The following alert types are supported:</span></span>

```md
> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.
```

<span data-ttu-id="b754d-114">這些警示在 docs.microsoft.com 中看起來像這樣：</span><span class="sxs-lookup"><span data-stu-id="b754d-114">These alerts look like this on docs.microsoft.com:</span></span>

![顯示上一個範例中的警示在發佈的 Docs 頁面如何呈現出不同的圖示與色彩](media/alerts-rendering.png)

## <a name="code-snippets"></a><span data-ttu-id="b754d-116">程式碼片段</span><span class="sxs-lookup"><span data-stu-id="b754d-116">Code snippets</span></span>

<span data-ttu-id="b754d-117">您可以在 Markdown 檔案中內嵌程式碼片段：</span><span class="sxs-lookup"><span data-stu-id="b754d-117">You can embed code snippets in your Markdown files:</span></span>

```md
[!code-<language>[<name>](<codepath><queryoption><queryoptionvalue> "<title>")]
```

## <a name="headings"></a><span data-ttu-id="b754d-118">標題</span><span class="sxs-lookup"><span data-stu-id="b754d-118">Headings</span></span>

<span data-ttu-id="b754d-119">Docs 支援六種層級的 Markdown 標題：</span><span class="sxs-lookup"><span data-stu-id="b754d-119">Docs supports six levels of Markdown headings:</span></span>

```md
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- <span data-ttu-id="b754d-120">最後一個 `#` 和標題文字之間必須有一個空格。</span><span class="sxs-lookup"><span data-stu-id="b754d-120">There must be a space between the last `#` and heading text.</span></span>
- <span data-ttu-id="b754d-121">每個 Markdown 檔案都必須且只能有一個 H1。</span><span class="sxs-lookup"><span data-stu-id="b754d-121">Each Markdown file must have one and only one H1.</span></span>
- <span data-ttu-id="b754d-122">H1 必須是檔案中 YML 中繼資料區塊後的第一個內容。</span><span class="sxs-lookup"><span data-stu-id="b754d-122">The H1 must be the first content in the file after the YML metadata block.</span></span>
- <span data-ttu-id="b754d-123">H2 會自動顯示在已發佈檔案的瀏覽功能表右側。</span><span class="sxs-lookup"><span data-stu-id="b754d-123">H2s automatically appear in the right-hand navigating menu of the published file.</span></span> <span data-ttu-id="b754d-124">較低層級的標題則不會，因此請策略性地使用 H2 以協助讀者瀏覽您的內容。</span><span class="sxs-lookup"><span data-stu-id="b754d-124">Lower-level headings do not, so use H2s strategically to help readers navigate your content.</span></span>
- <span data-ttu-id="b754d-125">HTML 標題 (例如 `<h1>`) 在有些情況下會造成建置警告，因此不建議使用。</span><span class="sxs-lookup"><span data-stu-id="b754d-125">HTML headings, such as `<h1>`, are not recommended and in some cases will cause build warnings.</span></span>
- <span data-ttu-id="b754d-126">您可以透過[書籤](#bookmark-links)連結至檔案中的個別標題。</span><span class="sxs-lookup"><span data-stu-id="b754d-126">You can link to individual headings in a file via [bookmarks](#bookmark-links).</span></span>

## <a name="html"></a><span data-ttu-id="b754d-127">HTML</span><span class="sxs-lookup"><span data-stu-id="b754d-127">HTML</span></span>

<span data-ttu-id="b754d-128">雖然 Markdown 支援內嵌 HTML，但仍不建議使用 HTML 來發佈至 Docs，因為除了有限的值清單以外，都會造成建置錯誤或警告。</span><span class="sxs-lookup"><span data-stu-id="b754d-128">Although Markdown supports inline HTML, HTML is not recommended for publishing to Docs, and except for a limited list of values will cause build errors or warnings.</span></span>

## <a name="images"></a><span data-ttu-id="b754d-129">影像</span><span class="sxs-lookup"><span data-stu-id="b754d-129">Images</span></span>

<span data-ttu-id="b754d-130">包含影像的語法如下：</span><span class="sxs-lookup"><span data-stu-id="b754d-130">The syntax to include an image is:</span></span>

```md
![[alt text]](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

<span data-ttu-id="b754d-131">其中，`alt text` 是影像的簡短描述，而 `<folder path>` 是影像的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="b754d-131">Where `alt text` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="b754d-132">適用於視障者的螢幕助讀程式需要使用替代文字。</span><span class="sxs-lookup"><span data-stu-id="b754d-132">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="b754d-133">若發生影像無法呈現的網站錯誤時，替代文字也很實用。</span><span class="sxs-lookup"><span data-stu-id="b754d-133">It is also useful if there is a site bug where the image cannot render.</span></span>

<span data-ttu-id="b754d-134">影像應儲存在您文件集內的 `/media` 資料夾。</span><span class="sxs-lookup"><span data-stu-id="b754d-134">Images should be stored in a `/media` folder within your doc set.</span></span> <span data-ttu-id="b754d-135">以下是預設支援的影像檔案類型：</span><span class="sxs-lookup"><span data-stu-id="b754d-135">The following file types are supported by default for images:</span></span>

- <span data-ttu-id="b754d-136">.jpg</span><span class="sxs-lookup"><span data-stu-id="b754d-136">.jpg</span></span>
- <span data-ttu-id="b754d-137">.png</span><span class="sxs-lookup"><span data-stu-id="b754d-137">.png</span></span>

<span data-ttu-id="b754d-138">您可以將其他影像類型當作資源新增到文件集的 docfx.json 檔案，</span><span class="sxs-lookup"><span data-stu-id="b754d-138">You can add support for other image types by adding them as resources to the docfx.json file</span></span><!--add link to reference when available--> <span data-ttu-id="b754d-139">以新增這些類型的支援。</span><span class="sxs-lookup"><span data-stu-id="b754d-139">for your doc set.</span></span>

## <a name="links"></a><span data-ttu-id="b754d-140">連結</span><span class="sxs-lookup"><span data-stu-id="b754d-140">Links</span></span>

<span data-ttu-id="b754d-141">在大部分情況下，Docs 都會使用標準 Markdown 連結至其他檔案和頁面。</span><span class="sxs-lookup"><span data-stu-id="b754d-141">In most cases, Docs uses standard Markdown links to other files and pages.</span></span> <span data-ttu-id="b754d-142">以下小節說明連結的類型。</span><span class="sxs-lookup"><span data-stu-id="b754d-142">The types of links are described in subsections below.</span></span>

> [!TIP]
> <span data-ttu-id="b754d-143">適用於 VS Code 的 Docs 編寫套件有助於正確插入相對連結和書籤，而不需與冗長的路徑奮戰！</span><span class="sxs-lookup"><span data-stu-id="b754d-143">The Docs Authoring Pack for VS Code can help insert relative links and bookmarks correctly without the tedium of figuring out the paths!</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b754d-144">請不要在您的 Microsoft 網站連結中包含地區設定代碼，例如 en-us。</span><span class="sxs-lookup"><span data-stu-id="b754d-144">Do not include locale codes, such as en-us, in your links to Microsoft sites.</span></span> <span data-ttu-id="b754d-145">硬式編碼的地區設定代碼會妨礙當地語系化內容的轉譯，而這會造成其他地區設定使用者的客戶體驗不佳，並產生高昂的當地語系化成本。</span><span class="sxs-lookup"><span data-stu-id="b754d-145">Hard-coded locale codes prevent localized content from rendering, which is a bad customer experience for users in other locales and incurs significant localization costs.</span></span> <span data-ttu-id="b754d-146">當您從瀏覽器複製 URL 時，預設會包含地區設定代碼，因此您必須在建立連結時手動將它刪除。</span><span class="sxs-lookup"><span data-stu-id="b754d-146">When you copy a URL from a browser, the locale code is included by default, so you need to manually delete it when you create your link.</span></span> <span data-ttu-id="b754d-147">例如，使用：</span><span class="sxs-lookup"><span data-stu-id="b754d-147">For example, use:</span></span>
>
> `[Microsoft](https://www.microsoft.com)`
>
> <span data-ttu-id="b754d-148">而非：</span><span class="sxs-lookup"><span data-stu-id="b754d-148">Not:</span></span>
>
> `[Microsoft](https://www.microsoft.com/en-us/)`

### <a name="relative-links-to-files-in-the-same-doc-set"></a><span data-ttu-id="b754d-149">相同文件集中檔案的相對連結</span><span class="sxs-lookup"><span data-stu-id="b754d-149">Relative links to files in the same doc set</span></span>

<span data-ttu-id="b754d-150">相對路徑是相對於目前檔案的目標檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="b754d-150">A relative path is the path to the target file relative to the current file.</span></span> <span data-ttu-id="b754d-151">在 Docs 中，您可以使用相對路徑連結至相同文件集內的其他檔案。</span><span class="sxs-lookup"><span data-stu-id="b754d-151">In Docs, you can use a relative path to link to another file within the same doc set.</span></span> <span data-ttu-id="b754d-152">相對路徑的語法如下：</span><span class="sxs-lookup"><span data-stu-id="b754d-152">The syntax for a relative path is as follows:</span></span>

```md
[link text](../../folder/filename.md)
```

<span data-ttu-id="b754d-153">其中，`../` 表示階層中的上一個層級。</span><span class="sxs-lookup"><span data-stu-id="b754d-153">Where `../` indicates one level above in the hierarchy.</span></span>

- <span data-ttu-id="b754d-154">相對路徑會在建置期間解析，包括移除 .md 副檔名。</span><span class="sxs-lookup"><span data-stu-id="b754d-154">The relative path will be resolved during the build, including removal of the .md extension.</span></span>
- <span data-ttu-id="b754d-155">您可以使用 "../" 連結至父資料夾中的檔案，但該檔案必須位於相同的文件集中。</span><span class="sxs-lookup"><span data-stu-id="b754d-155">You can use "../" to link to a file in the parent folder, but that file has to be in the same doc set.</span></span> <span data-ttu-id="b754d-156">您無法使用 "../" 連結至另一個文件集資料夾中的檔案。</span><span class="sxs-lookup"><span data-stu-id="b754d-156">You cannot use "../" to link to a file in another doc set folder.</span></span>
- <span data-ttu-id="b754d-157">Docs 也支援開頭為 "~" 的特殊格式相對路徑 (例如 ~/foo/bar.md)。</span><span class="sxs-lookup"><span data-stu-id="b754d-157">Docs also supports a special form of relative path that starts with "~" (for example, ~/foo/bar.md).</span></span> <span data-ttu-id="b754d-158">此語法表示檔案是相對於文件集的根資料夾。</span><span class="sxs-lookup"><span data-stu-id="b754d-158">This syntax indicates a file relative to the root folder of a doc set.</span></span> <span data-ttu-id="b754d-159">這種路徑也會在建置期間進行驗證及解析。</span><span class="sxs-lookup"><span data-stu-id="b754d-159">This kind of path is also validated and resolved during the build.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b754d-160">在相對路徑中包含副檔名。</span><span class="sxs-lookup"><span data-stu-id="b754d-160">Include the file extension in the relative path.</span></span> <span data-ttu-id="b754d-161">組建可驗證該相對路徑的目標檔案是否存在。</span><span class="sxs-lookup"><span data-stu-id="b754d-161">Build validates the existence of the target file of that relative path.</span></span> <span data-ttu-id="b754d-162">如果相對路徑未包含副檔名，組建就可能會回報連結中斷的警告。</span><span class="sxs-lookup"><span data-stu-id="b754d-162">If relative path does not include file extension, it is likely build will report a warning of broken link.</span></span> <span data-ttu-id="b754d-163">例如，使用：</span><span class="sxs-lookup"><span data-stu-id="b754d-163">For example, use:</span></span>
>
> `[link text](../../folder/filename.md)`
>
> <span data-ttu-id="b754d-164">而非：</span><span class="sxs-lookup"><span data-stu-id="b754d-164">Not:</span></span>
>
> `[link text](../../folder/filename)`

### <a name="site-relative-links-to-other-files-on-docs"></a><span data-ttu-id="b754d-165">Docs 上其他檔案的站台相關連結</span><span class="sxs-lookup"><span data-stu-id="b754d-165">Site relative links to other files on Docs</span></span>

```md
[Azure and Linux](/articles/virtual-machines/linux/overview)
```

<span data-ttu-id="b754d-166">請不要包含副檔名 (.md)。</span><span class="sxs-lookup"><span data-stu-id="b754d-166">Do not include the file extension (.md).</span></span> <span data-ttu-id="b754d-167">此為來自外部 Azure「文章」文件集的 Linux 概觀檔連結。</span><span class="sxs-lookup"><span data-stu-id="b754d-167">This links to the Linux overview file from outside the Azure "articles" doc set.</span></span>

### <a name="links-to-external-sites"></a><span data-ttu-id="b754d-168">外部網站的連結</span><span class="sxs-lookup"><span data-stu-id="b754d-168">Links to external sites</span></span>

```md
[Microsoft](https://www.microsoft.com)
```

<span data-ttu-id="b754d-169">其他網頁的 URL 連結 (必須包含 https://)。</span><span class="sxs-lookup"><span data-stu-id="b754d-169">URL-based link to another web page (must include https://).</span></span>

### <a name="bookmark-links"></a><span data-ttu-id="b754d-170">書籤連結</span><span class="sxs-lookup"><span data-stu-id="b754d-170">Bookmark links</span></span>

<span data-ttu-id="b754d-171">相同存放庫中其他檔案的標題書籤連結。</span><span class="sxs-lookup"><span data-stu-id="b754d-171">Bookmark link to a heading in another file in the same repo.</span></span> <span data-ttu-id="b754d-172">例如：</span><span class="sxs-lookup"><span data-stu-id="b754d-172">For example:</span></span>

```md
[Managed Disks](../../linux/overview.md#managed-disks)
```

<span data-ttu-id="b754d-173">目前檔案中的標題書籤連結：</span><span class="sxs-lookup"><span data-stu-id="b754d-173">Bookmark link to a heading in the current file:</span></span>

```md
[Managed Disks](#managed-disks)
```

<span data-ttu-id="b754d-174">使用井字號 `#` 加上標題文字。</span><span class="sxs-lookup"><span data-stu-id="b754d-174">Use a hash mark `#` followed by the words of the heading.</span></span> <span data-ttu-id="b754d-175">若要將標題文字變更為連結文字：</span><span class="sxs-lookup"><span data-stu-id="b754d-175">To change the heading text into link text:</span></span>
- <span data-ttu-id="b754d-176">全部使用小寫字元</span><span class="sxs-lookup"><span data-stu-id="b754d-176">Use all lowercase characters</span></span>
- <span data-ttu-id="b754d-177">移除標點符號</span><span class="sxs-lookup"><span data-stu-id="b754d-177">Remove punctuation</span></span>
- <span data-ttu-id="b754d-178">以虛線取代空格</span><span class="sxs-lookup"><span data-stu-id="b754d-178">Replace spaces with dashes</span></span>

<span data-ttu-id="b754d-179">舉例來說，如果標題名稱為 "2.2 Security concerns"，書籤連結文字就會是 "#22-security-concerns"。</span><span class="sxs-lookup"><span data-stu-id="b754d-179">For example, if the heading name is "2.2 Security concerns", then the bookmark link text will be "#22-security-concerns".</span></span>

### <a name="explicit-anchor-links"></a><span data-ttu-id="b754d-180">明確錨點連結</span><span class="sxs-lookup"><span data-stu-id="b754d-180">Explicit anchor links</span></span>

<span data-ttu-id="b754d-181">除非在中樞和登陸頁面中，否則**沒有必要也不建議使用**含 `<a>` HTML 標籤的明確錨點連結。</span><span class="sxs-lookup"><span data-stu-id="b754d-181">Explicit anchor links using the `<a>` HTML tag are **not required or recommended** except in hub and landing pages.</span></span> <span data-ttu-id="b754d-182">請如上所述在一般 Markdown 檔案中使用書籤。</span><span class="sxs-lookup"><span data-stu-id="b754d-182">Use bookmarks as described above in general Markdown files.</span></span> <span data-ttu-id="b754d-183">針對中樞和登陸頁面，請如下所示使用錨點：</span><span class="sxs-lookup"><span data-stu-id="b754d-183">For hub and landing pages, use anchors as follows:</span></span>

<span data-ttu-id="b754d-184">`## <a id="AnchorText"> </a>Header text` 或 `## <a name="AnchorText"> </a>Header text`</span><span class="sxs-lookup"><span data-stu-id="b754d-184">`## <a id="AnchorText"> </a>Header text` or `## <a name="AnchorText"> </a>Header text`</span></span>

<span data-ttu-id="b754d-185">若要連結至明確錨點，請使用下列語法：</span><span class="sxs-lookup"><span data-stu-id="b754d-185">To link to explicit anchors, use the following syntax:</span></span>

```md
To go to a section on the same page:
[text](#AnchorText)

To go to a section on another page.
[text](FileName.md#AnchorText)
```

### <a name="xref-cross-reference-links"></a><span data-ttu-id="b754d-186">XREF (交互參照) 連結</span><span class="sxs-lookup"><span data-stu-id="b754d-186">XREF (cross reference) links</span></span>

<span data-ttu-id="b754d-187">若要連結至目前文件集或其他文件集中自動產生的 API 參照頁面，請使用 XREF 連結與唯一識別碼 (UID)。</span><span class="sxs-lookup"><span data-stu-id="b754d-187">To link to auto-generated API references pages in the current doc set or other doc sets, use XREF links with the unique ID (UID).</span></span>

> [!NOTE]
> <span data-ttu-id="b754d-188">若要參考其他文件集中的 API 參考頁面，您必須在 `docfx.json` 檔案中新增 `xrefService` 設定。</span><span class="sxs-lookup"><span data-stu-id="b754d-188">To reference API reference pages in other doc sets, you need to add `xrefService` configuration in `docfx.json` file.</span></span>
> ```
> "build": {
>   ...
>   "xrefService": [ "https://xref.docs.microsoft.com/query?uid={uid}" ]
> }
> ```

<span data-ttu-id="b754d-189">UID 等同於完整的類別和成員名稱。</span><span class="sxs-lookup"><span data-stu-id="b754d-189">The UID equates to the fully qualified class and member name.</span></span> <span data-ttu-id="b754d-190">如果您在 UID 之後加上 \*，則連結代表多載頁面，而不是特定的 API。</span><span class="sxs-lookup"><span data-stu-id="b754d-190">If you add a \* after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="b754d-191">例如，使用 `List<T>.BinarySearch*` 連結至 BinarySearch 方法頁面，而不是連結至特定多載，例如 `List<T>.BinarySearch(T, IComparer<T>)`。</span><span class="sxs-lookup"><span data-stu-id="b754d-191">For example, use `List<T>.BinarySearch*` to link to the BinarySearch Method page instead of linking to a specific overload such as `List<T>.BinarySearch(T, IComparer<T>)`.</span></span>

<span data-ttu-id="b754d-192">您可以使用下列其中一個語法：</span><span class="sxs-lookup"><span data-stu-id="b754d-192">You can use one of the following syntaxes:</span></span>

- <span data-ttu-id="b754d-193">自動連結：`<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="b754d-193">Auto-link: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span></span>

  <span data-ttu-id="b754d-194">選用的 `displayProperty` 查詢參數會產生完整的連結文字。</span><span class="sxs-lookup"><span data-stu-id="b754d-194">The optional `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="b754d-195">根據預設，連結文字只會顯示成員或型別名稱。</span><span class="sxs-lookup"><span data-stu-id="b754d-195">By default, link text shows only the member or type name.</span></span>

- <span data-ttu-id="b754d-196">Markdown 連結：`[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="b754d-196">Markdown link: `[link text](xref:UID)`</span></span>
  
  <span data-ttu-id="b754d-197">用於您要自訂顯示的連結文字時。</span><span class="sxs-lookup"><span data-stu-id="b754d-197">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="b754d-198">範例：</span><span class="sxs-lookup"><span data-stu-id="b754d-198">Examples:</span></span>

- <span data-ttu-id="b754d-199">`<xref:System.String>` 會轉譯為 "String"。</span><span class="sxs-lookup"><span data-stu-id="b754d-199">`<xref:System.String>` renders as "String".</span></span>
- <span data-ttu-id="b754d-200">`<xref:System.String?displayProperty=nameWithType>` 會轉譯為 "System.String"。</span><span class="sxs-lookup"><span data-stu-id="b754d-200">`<xref:System.String?displayProperty=nameWithType>` renders as "System.String".</span></span>
- <span data-ttu-id="b754d-201">`[String class](xref:System.String)` 會轉譯為 "String class"。</span><span class="sxs-lookup"><span data-stu-id="b754d-201">`[String class](xref:System.String)` renders as "String class".</span></span>

<span data-ttu-id="b754d-202">目前還沒有較輕鬆的方式可用來尋找 UID。</span><span class="sxs-lookup"><span data-stu-id="b754d-202">Right now, there is no easy way to find the UIDs.</span></span> <!-- ? --><span data-ttu-id="b754d-203">若要尋找 API 的 UID，最佳方法就是檢視所要連結 API 頁面的來源，然後尋找 ms.assetid 值。</span><span class="sxs-lookup"><span data-stu-id="b754d-203">The best way to find the UID for an API is to view the source for the API page you want to link to and find the ms.assetid value.</span></span> <span data-ttu-id="b754d-204">個別的多載值不會顯示在來源中。</span><span class="sxs-lookup"><span data-stu-id="b754d-204">Individual overload values are not shown in the source.</span></span> <span data-ttu-id="b754d-205">我們正努力讓系統在未來會更好。</span><span class="sxs-lookup"><span data-stu-id="b754d-205">We're working on having a better system in the future.</span></span>

<span data-ttu-id="b754d-206">當 UID 包含特殊字元 \`、\# 或 \* 時，UID 值必須分別以 HTML 編碼為 `%60`、`%23` 和 `%2A`。</span><span class="sxs-lookup"><span data-stu-id="b754d-206">When the UID contains the special characters \`, \#, or \*, the UID value needs to be HTML encoded as `%60`, `%23`, and `%2A`, respectively.</span></span> <span data-ttu-id="b754d-207">有時候您會看到括號也會被編碼，但這並非必要。</span><span class="sxs-lookup"><span data-stu-id="b754d-207">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="b754d-208">範例：</span><span class="sxs-lookup"><span data-stu-id="b754d-208">Examples:</span></span>

- <span data-ttu-id="b754d-209">System.Threading.Tasks.Task\`1 變成 `System.Threading.Tasks.Task%601`</span><span class="sxs-lookup"><span data-stu-id="b754d-209">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="b754d-210">System.Exception.\#ctor 變成 `System.Exception.%23ctor`</span><span class="sxs-lookup"><span data-stu-id="b754d-210">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="b754d-211">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) 變成 `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span><span class="sxs-lookup"><span data-stu-id="b754d-211">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<!-- leave out of Contributor Guide for now
Using XREF may require some configuration. For more information, see XREF Service.
-->

## <a name="lists-numbered-bulleted-checklist"></a><span data-ttu-id="b754d-212">清單 (編號、分項、檢查清單)</span><span class="sxs-lookup"><span data-stu-id="b754d-212">Lists (Numbered, Bulleted, Checklist)</span></span>

### <a name="numbered-list"></a><span data-ttu-id="b754d-213">編號清單</span><span class="sxs-lookup"><span data-stu-id="b754d-213">Numbered list</span></span>

<span data-ttu-id="b754d-214">若要建立編號清單，您可以全部都使用 1，系統即會在發佈時將其轉譯為連續清單。</span><span class="sxs-lookup"><span data-stu-id="b754d-214">To create a numbered list, you can use all 1s, which are rendered as a sequential list when published.</span></span> <span data-ttu-id="b754d-215">為了讓來源更方便閱讀，您可以遞增清單。</span><span class="sxs-lookup"><span data-stu-id="b754d-215">For increased source readability, you can increment your lists.</span></span>

<span data-ttu-id="b754d-216">請不要在清單中使用字母，包括巢狀清單。</span><span class="sxs-lookup"><span data-stu-id="b754d-216">Do not use letters in lists, including nested lists.</span></span> <span data-ttu-id="b754d-217">透過 Docs 發佈時，字母無法正確轉譯。如果是使用數字的巢狀清單，系統在發佈時會轉譯為小寫字母。</span><span class="sxs-lookup"><span data-stu-id="b754d-217">They do not render correctly when published to Docs. Nested lists using numbers will render as lowercase letters when published.</span></span> <span data-ttu-id="b754d-218">例如：</span><span class="sxs-lookup"><span data-stu-id="b754d-218">For example:</span></span>

```md
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

<span data-ttu-id="b754d-219">這會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="b754d-219">This renders as follows:</span></span>

1. <span data-ttu-id="b754d-220">This is</span><span class="sxs-lookup"><span data-stu-id="b754d-220">This is</span></span>
1. <span data-ttu-id="b754d-221">a parent numbered list</span><span class="sxs-lookup"><span data-stu-id="b754d-221">a parent numbered list</span></span>
   1. <span data-ttu-id="b754d-222">and this is</span><span class="sxs-lookup"><span data-stu-id="b754d-222">and this is</span></span>
   1. <span data-ttu-id="b754d-223">a nested numbered list</span><span class="sxs-lookup"><span data-stu-id="b754d-223">a nested numbered list</span></span>
1. <span data-ttu-id="b754d-224">(fin)</span><span class="sxs-lookup"><span data-stu-id="b754d-224">(fin)</span></span>

### <a name="bulleted-list"></a><span data-ttu-id="b754d-225">項目符號清單</span><span class="sxs-lookup"><span data-stu-id="b754d-225">Bulleted list</span></span>

<span data-ttu-id="b754d-226">若要建立項目符號清單，請在每行開頭使用 `-` 後接空格：</span><span class="sxs-lookup"><span data-stu-id="b754d-226">To create a bulleted list, use `-` followed by a space at the beginning of each line:</span></span>

```md
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

<span data-ttu-id="b754d-227">這會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="b754d-227">This renders as follows:</span></span>

- <span data-ttu-id="b754d-228">This is</span><span class="sxs-lookup"><span data-stu-id="b754d-228">This is</span></span>
- <span data-ttu-id="b754d-229">a parent bulleted list</span><span class="sxs-lookup"><span data-stu-id="b754d-229">a parent bulleted list</span></span>
  - <span data-ttu-id="b754d-230">and this is</span><span class="sxs-lookup"><span data-stu-id="b754d-230">and this is</span></span>
  - <span data-ttu-id="b754d-231">a nested bulleted list</span><span class="sxs-lookup"><span data-stu-id="b754d-231">a nested bulleted list</span></span>
- <span data-ttu-id="b754d-232">All done!</span><span class="sxs-lookup"><span data-stu-id="b754d-232">All done!</span></span>

### <a name="checklist"></a><span data-ttu-id="b754d-233">檢查清單</span><span class="sxs-lookup"><span data-stu-id="b754d-233">Checklist</span></span>

<span data-ttu-id="b754d-234">您可透過自訂 Markdown 延伸模組，在 docs.microsoft.com (僅限於此) 上使用檢查清單：</span><span class="sxs-lookup"><span data-stu-id="b754d-234">Checklists are available for use on docs.microsoft.com (only) via a custom Markdown extension:</span></span>

```md
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

<span data-ttu-id="b754d-235">此範例在 docs.microsoft.com 上的轉譯如下：</span><span class="sxs-lookup"><span data-stu-id="b754d-235">This example renders on docs.microsoft.com like this:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="b754d-236">List item 1</span><span class="sxs-lookup"><span data-stu-id="b754d-236">List item 1</span></span>
> * <span data-ttu-id="b754d-237">List item 2</span><span class="sxs-lookup"><span data-stu-id="b754d-237">List item 2</span></span>
> * <span data-ttu-id="b754d-238">List item 3</span><span class="sxs-lookup"><span data-stu-id="b754d-238">List item 3</span></span>

<span data-ttu-id="b754d-239">您可在文章的開頭或結尾使用檢查清單，來摘要「您將學到什麼」或「您已學到的內容」。</span><span class="sxs-lookup"><span data-stu-id="b754d-239">Use checklists at the beginning or end of an article to summarize "What will you learn" or "What have you learned" content.</span></span> <span data-ttu-id="b754d-240">請不要在整篇文章中新增隨機檢查清單。</span><span class="sxs-lookup"><span data-stu-id="b754d-240">Do not add random checklists throughout your articles.</span></span>
<!-- is this guidance still accurate? -->

## <a name="next-step-action"></a><span data-ttu-id="b754d-241">下一步動作</span><span class="sxs-lookup"><span data-stu-id="b754d-241">Next step action</span></span>

<span data-ttu-id="b754d-242">您可使用自訂延伸模組，將下一步動作按鈕新增至 docs.microsoft.com (僅限於此) 上的頁面。</span><span class="sxs-lookup"><span data-stu-id="b754d-242">You can use a custom extension to add a next step action button to pages on docs.microsoft.com (only).</span></span>

<span data-ttu-id="b754d-243">語法如下：</span><span class="sxs-lookup"><span data-stu-id="b754d-243">The syntax is as follows:</span></span>

```md
> [!div class="nextstepaction"]
> [button text](link to topic)
```

<span data-ttu-id="b754d-244">例如：</span><span class="sxs-lookup"><span data-stu-id="b754d-244">For example:</span></span>

```md
> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)
```

<span data-ttu-id="b754d-245">這會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="b754d-245">This renders as follows:</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="b754d-246">Learn about basic style</span><span class="sxs-lookup"><span data-stu-id="b754d-246">Learn about basic style</span></span>](style-quick-start.md)

<span data-ttu-id="b754d-247">您可以在下一步動作中使用任何支援的連結，包括其他網頁的 Markdown 連結。</span><span class="sxs-lookup"><span data-stu-id="b754d-247">You can use any supported link in a next step action, including a Markdown link to another web page.</span></span> <span data-ttu-id="b754d-248">在大部分情況下，下一步動作連結都是相同文件集中其他檔案的相對連結。</span><span class="sxs-lookup"><span data-stu-id="b754d-248">In most cases, the next action link will be a relative link to another file in the same doc set.</span></span>

## <a name="section-definition"></a><span data-ttu-id="b754d-249">區段定義</span><span class="sxs-lookup"><span data-stu-id="b754d-249">Section definition</span></span>

<!-- more info about this would be helpful! -->
<span data-ttu-id="b754d-250">您可能需要定義區段。</span><span class="sxs-lookup"><span data-stu-id="b754d-250">You might need to define a section.</span></span> <span data-ttu-id="b754d-251">此語法最常用於程式碼表格。</span><span class="sxs-lookup"><span data-stu-id="b754d-251">This syntax is mostly used for code tables.</span></span>
<span data-ttu-id="b754d-252">請參閱下列範例：</span><span class="sxs-lookup"><span data-stu-id="b754d-252">See the following example:</span></span>

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

<span data-ttu-id="b754d-253">上述區塊引述 Markdown 文字會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="b754d-253">The preceding blockquote Markdown text will be rendered as:</span></span>
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```

## <a name="selectors"></a><span data-ttu-id="b754d-254">選取器</span><span class="sxs-lookup"><span data-stu-id="b754d-254">Selectors</span></span>

<!-- could be more clear! -->
<span data-ttu-id="b754d-255">當您想要連到同一篇文章的不同頁面時，可以使用選取器。</span><span class="sxs-lookup"><span data-stu-id="b754d-255">You can use a selector when you want to connect different pages for the same article.</span></span> <span data-ttu-id="b754d-256">讀者即可在這些頁面間切換。</span><span class="sxs-lookup"><span data-stu-id="b754d-256">Readers can then switch between those pages.</span></span>

> [!NOTE]
> <span data-ttu-id="b754d-257">此延伸在 docs.microsoft.com 和 MSDN 的運作方式不同。</span><span class="sxs-lookup"><span data-stu-id="b754d-257">This extension works differently between docs.microsoft.com and MSDN.</span></span> <!-- should we keep info about MSDN? If so say how they differ?-->

### <a name="single-selector"></a><span data-ttu-id="b754d-258">單一選取器</span><span class="sxs-lookup"><span data-stu-id="b754d-258">Single selector</span></span>

```
> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)
```

<span data-ttu-id="b754d-259">... 轉譯結果如下：</span><span class="sxs-lookup"><span data-stu-id="b754d-259">... will be rendered like this:</span></span>

> [!div class="op_single_selector"]
> - [通用 Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)

### <a name="multi-selector"></a><span data-ttu-id="b754d-268">多重選取器</span><span class="sxs-lookup"><span data-stu-id="b754d-268">Multi-selector</span></span>

```
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows universal C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows universal C# | Javascript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | Javascript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | Javascript)](how-to-write-workflows-major.md)
```

<span data-ttu-id="b754d-269">... 轉譯結果如下：</span><span class="sxs-lookup"><span data-stu-id="b754d-269">... will be rendered like this:</span></span>

> [!div class="op_multi_selector" title1="平台" title2="後端"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows 通用 C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows 通用 C# | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | JavaScript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | JavaScript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | JavaScript)](how-to-write-workflows-major.md)

## <a name="tables"></a><span data-ttu-id="b754d-282">表格</span><span class="sxs-lookup"><span data-stu-id="b754d-282">Tables</span></span>

<span data-ttu-id="b754d-283">在 Markdown 中建立表格的最簡單做法是使用直立線符號及線條。</span><span class="sxs-lookup"><span data-stu-id="b754d-283">The simplest way to create a table in Markdown is to use pipes and lines.</span></span> <span data-ttu-id="b754d-284">若要建立含標題的標準表格，請沿著第一個線段與虛線：</span><span class="sxs-lookup"><span data-stu-id="b754d-284">To create a standard table with a header, follow the first line with dashed line:</span></span>

```md
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

<span data-ttu-id="b754d-285">這會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="b754d-285">This renders as follows:</span></span>

|<span data-ttu-id="b754d-286">This is</span><span class="sxs-lookup"><span data-stu-id="b754d-286">This is</span></span>   |<span data-ttu-id="b754d-287">a simple</span><span class="sxs-lookup"><span data-stu-id="b754d-287">a simple</span></span>   |<span data-ttu-id="b754d-288">table header</span><span class="sxs-lookup"><span data-stu-id="b754d-288">table header</span></span>|
|----------|-----------|------------|
|<span data-ttu-id="b754d-289">table</span><span class="sxs-lookup"><span data-stu-id="b754d-289">table</span></span>     |<span data-ttu-id="b754d-290">data</span><span class="sxs-lookup"><span data-stu-id="b754d-290">data</span></span>       |<span data-ttu-id="b754d-291">here</span><span class="sxs-lookup"><span data-stu-id="b754d-291">here</span></span>        |
|<span data-ttu-id="b754d-292">it doesn't</span><span class="sxs-lookup"><span data-stu-id="b754d-292">it doesn't</span></span>|<span data-ttu-id="b754d-293">actually</span><span class="sxs-lookup"><span data-stu-id="b754d-293">actually</span></span>   |<span data-ttu-id="b754d-294">have to line up nicely!</span><span class="sxs-lookup"><span data-stu-id="b754d-294">have to line up nicely!</span></span>||

<span data-ttu-id="b754d-295">您也可以建立不含標題的表格。</span><span class="sxs-lookup"><span data-stu-id="b754d-295">You can also create a table without a header.</span></span> <span data-ttu-id="b754d-296">例如，若要建立多重資料行清單：</span><span class="sxs-lookup"><span data-stu-id="b754d-296">For example, to create a multiple-column list:</span></span>

```md
|   |   |
| - | - |
| This | table |
| has no | header |
```

<span data-ttu-id="b754d-297">這會轉譯如下：</span><span class="sxs-lookup"><span data-stu-id="b754d-297">This renders like this:</span></span>

|   |   |
| - | - |
| <span data-ttu-id="b754d-298">This</span><span class="sxs-lookup"><span data-stu-id="b754d-298">This</span></span> | <span data-ttu-id="b754d-299">table</span><span class="sxs-lookup"><span data-stu-id="b754d-299">table</span></span> |
| <span data-ttu-id="b754d-300">has no</span><span class="sxs-lookup"><span data-stu-id="b754d-300">has no</span></span> | <span data-ttu-id="b754d-301">header</span><span class="sxs-lookup"><span data-stu-id="b754d-301">header</span></span> |

<span data-ttu-id="b754d-302">您可以使用冒號對齊資料行：</span><span class="sxs-lookup"><span data-stu-id="b754d-302">You can align the columns by using colons:</span></span>

```md
|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|
```

<span data-ttu-id="b754d-303">轉譯如下：</span><span class="sxs-lookup"><span data-stu-id="b754d-303">Renders as follows:</span></span>

|                  |
|------------------|
|    <span data-ttu-id="b754d-304">right aligned:</span><span class="sxs-lookup"><span data-stu-id="b754d-304">right aligned:</span></span>|
|<span data-ttu-id="b754d-305">:left aligned</span><span class="sxs-lookup"><span data-stu-id="b754d-305">:left aligned</span></span>     |
|<span data-ttu-id="b754d-306">:centered        :</span><span class="sxs-lookup"><span data-stu-id="b754d-306">:centered        :</span></span>|

> [!TIP]
> <span data-ttu-id="b754d-307">適用於 VS Code 的 Docs 編寫延伸模組可讓您輕鬆新增基本 Markdown 表格！</span><span class="sxs-lookup"><span data-stu-id="b754d-307">The Docs Authoring Extension for VS Code makes it easy to add basic Markdown tables!</span></span>
>
> <span data-ttu-id="b754d-308">您也可以使用[線上表格產生器](http://www.tablesgenerator.com/markdown_tables)。</span><span class="sxs-lookup"><span data-stu-id="b754d-308">You can also use an [online table generator](http://www.tablesgenerator.com/markdown_tables).</span></span>

### <a name="mx-tdbreakall"></a><span data-ttu-id="b754d-309">mx-tdBreakAll</span><span class="sxs-lookup"><span data-stu-id="b754d-309">mx-tdBreakAll</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b754d-310">此功能僅適用於 docs.microsoft.com 網站。</span><span class="sxs-lookup"><span data-stu-id="b754d-310">This only works on the docs.microsoft.com site.</span></span>

<span data-ttu-id="b754d-311">如果您使用 Markdown 建立表格，該表格可能會擴展到右側導覽，變得難以閱讀。</span><span class="sxs-lookup"><span data-stu-id="b754d-311">If you create a table in Markdown, the table might expand to the right navigation and become unreadable.</span></span> <span data-ttu-id="b754d-312">您可以藉由允許 Docs 轉譯視需要切割表格，來解決此問題。</span><span class="sxs-lookup"><span data-stu-id="b754d-312">You can solve that by allowing Docs rendering to break the table when needed.</span></span> <span data-ttu-id="b754d-313">您只要使用自訂類別 `[!div class="mx-tdBreakAll"]` 加在表格前後即可。</span><span class="sxs-lookup"><span data-stu-id="b754d-313">Just wrap up the table with the custom class `[!div class="mx-tdBreakAll"]`.</span></span>

<span data-ttu-id="b754d-314">以下是具有三列的表格 Markdown 範例，會以類別名稱為 `mx-tdBreakAll` 的 `div` 加在表格前後。</span><span class="sxs-lookup"><span data-stu-id="b754d-314">Here is a Markdown sample of a table with three rows that will be wrapped by a `div` with the class name `mx-tdBreakAll`.</span></span>

```md
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

<span data-ttu-id="b754d-315">轉譯結果如下：</span><span class="sxs-lookup"><span data-stu-id="b754d-315">It will be rendered like this:</span></span>

> [!div class="mx-tdBreakAll"]
> |<span data-ttu-id="b754d-316">Name</span><span class="sxs-lookup"><span data-stu-id="b754d-316">Name</span></span>|<span data-ttu-id="b754d-317">Syntax</span><span class="sxs-lookup"><span data-stu-id="b754d-317">Syntax</span></span>|<span data-ttu-id="b754d-318">Mandatory for silent installation?</span><span class="sxs-lookup"><span data-stu-id="b754d-318">Mandatory for silent installation?</span></span>|<span data-ttu-id="b754d-319">Description</span><span class="sxs-lookup"><span data-stu-id="b754d-319">Description</span></span>|
> |-------------|----------|---------|---------|
> |<span data-ttu-id="b754d-320">Quiet</span><span class="sxs-lookup"><span data-stu-id="b754d-320">Quiet</span></span>|<span data-ttu-id="b754d-321">/quiet</span><span class="sxs-lookup"><span data-stu-id="b754d-321">/quiet</span></span>|<span data-ttu-id="b754d-322">Yes</span><span class="sxs-lookup"><span data-stu-id="b754d-322">Yes</span></span>|<span data-ttu-id="b754d-323">Runs the installer, displaying no UI and no prompts.</span><span class="sxs-lookup"><span data-stu-id="b754d-323">Runs the installer, displaying no UI and no prompts.</span></span>|
> |<span data-ttu-id="b754d-324">NoRestart</span><span class="sxs-lookup"><span data-stu-id="b754d-324">NoRestart</span></span>|<span data-ttu-id="b754d-325">/norestart</span><span class="sxs-lookup"><span data-stu-id="b754d-325">/norestart</span></span>|<span data-ttu-id="b754d-326">No</span><span class="sxs-lookup"><span data-stu-id="b754d-326">No</span></span>|<span data-ttu-id="b754d-327">Suppresses any attempts to restart.</span><span class="sxs-lookup"><span data-stu-id="b754d-327">Suppresses any attempts to restart.</span></span> <span data-ttu-id="b754d-328">By default, the UI will prompt before restart.</span><span class="sxs-lookup"><span data-stu-id="b754d-328">By default, the UI will prompt before restart.</span></span>|
> |<span data-ttu-id="b754d-329">Help</span><span class="sxs-lookup"><span data-stu-id="b754d-329">Help</span></span>|<span data-ttu-id="b754d-330">/help</span><span class="sxs-lookup"><span data-stu-id="b754d-330">/help</span></span>|<span data-ttu-id="b754d-331">No</span><span class="sxs-lookup"><span data-stu-id="b754d-331">No</span></span>|<span data-ttu-id="b754d-332">Provides help and quick reference.</span><span class="sxs-lookup"><span data-stu-id="b754d-332">Provides help and quick reference.</span></span> <span data-ttu-id="b754d-333">Displays the correct use of the setup command, including a list of all options and behaviors.</span><span class="sxs-lookup"><span data-stu-id="b754d-333">Displays the correct use of the setup command, including a list of all options and behaviors.</span></span>|

### <a name="mx-tdcol2breakall"></a><span data-ttu-id="b754d-334">mx-tdCol2BreakAll</span><span class="sxs-lookup"><span data-stu-id="b754d-334">mx-tdCol2BreakAll</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b754d-335">此功能僅適用於 docs.microsoft.com 網站。</span><span class="sxs-lookup"><span data-stu-id="b754d-335">This only works on the docs.microsoft.com site.</span></span>

<span data-ttu-id="b754d-336">有時候，在您表格中第二欄的字詞可能會很長。</span><span class="sxs-lookup"><span data-stu-id="b754d-336">From time to time, you might have very long words in the second column of a table.</span></span> <span data-ttu-id="b754d-337">為了讓它們妥善分隔，您可以使用先前所示的 `div` 包裝函式語法來套用類別 `mx-tdCol2BreakAll`。</span><span class="sxs-lookup"><span data-stu-id="b754d-337">To ensure they are broken apart nicely, you can apply the class `mx-tdCol2BreakAll` by using the `div` wrapper syntax as shown earlier.</span></span>

### <a name="html-tables"></a><span data-ttu-id="b754d-338">HTML 表格</span><span class="sxs-lookup"><span data-stu-id="b754d-338">HTML Tables</span></span>

<span data-ttu-id="b754d-339">HTML 表格不建議用於 docs.microsoft.com。</span><span class="sxs-lookup"><span data-stu-id="b754d-339">HTML tables are not recommended for docs.microsoft.com.</span></span> <span data-ttu-id="b754d-340">這類表格不是使用者可看懂的來源，而這與 Markdown 主要準則抵觸。</span><span class="sxs-lookup"><span data-stu-id="b754d-340">They are not human readable in the source - which is a key principle of Markdown.</span></span>

<!--If you use HTML tables and your Markdown is not being rendered between the two tables, you need to add a closing `br` tag after the closing `table` tag.

![break HTML tables](media/break-tables.png)
-->

## <a name="videos"></a><span data-ttu-id="b754d-341">影片</span><span class="sxs-lookup"><span data-stu-id="b754d-341">Videos</span></span>

### <a name="embedding-videos-into-a-markdown-page"></a><span data-ttu-id="b754d-342">將影片內嵌在 Markdown 頁面中</span><span class="sxs-lookup"><span data-stu-id="b754d-342">Embedding videos into a Markdown page</span></span>

<span data-ttu-id="b754d-343">目前，Docs 可支援將影片發佈至下列三個位置之一：</span><span class="sxs-lookup"><span data-stu-id="b754d-343">Currently, Docs can support videos published to one of three locations:</span></span>

- <span data-ttu-id="b754d-344">YouTube</span><span class="sxs-lookup"><span data-stu-id="b754d-344">YouTube</span></span>
- <span data-ttu-id="b754d-345">Channel 9</span><span class="sxs-lookup"><span data-stu-id="b754d-345">Channel 9</span></span>
- <span data-ttu-id="b754d-346">Microsoft 專屬的 'One Player' 系統</span><span class="sxs-lookup"><span data-stu-id="b754d-346">Microsoft's own 'One Player' system</span></span>

<span data-ttu-id="b754d-347">您可以使用下列語法內嵌影片，而 Docs 會加以轉譯。</span><span class="sxs-lookup"><span data-stu-id="b754d-347">You can embed a video with the following syntax, and Docs will render it.</span></span>

```md
> [!VIDEO <embedded_video_link>]
```

<span data-ttu-id="b754d-348">範例：</span><span class="sxs-lookup"><span data-stu-id="b754d-348">Example:</span></span>

```md
> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
```

<span data-ttu-id="b754d-349">... 將會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="b754d-349">... will be rendered as:</span></span>

```html
<iframe src="https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>

<iframe src="https://www.youtube-nocookie.com/embed/iAtwVM-Z7rY" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
<iframe src="https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
```

<span data-ttu-id="b754d-350">並在發佈頁面上顯示如下：</span><span class="sxs-lookup"><span data-stu-id="b754d-350">And it will be displayed like this on published pages:</span></span>

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

> [!IMPORTANT]
> <span data-ttu-id="b754d-351">CH9 影片 URL 應該以 `https` 開頭並以 `/player` 結尾。</span><span class="sxs-lookup"><span data-stu-id="b754d-351">The CH9 video URL should start with `https` and end with `/player`.</span></span> <span data-ttu-id="b754d-352">否則，它會內嵌整頁而不只是影片。</span><span class="sxs-lookup"><span data-stu-id="b754d-352">Otherwise, it will embed the whole page instead of the video only.</span></span>

### <a name="uploading-new-videos"></a><span data-ttu-id="b754d-353">上傳新影片</span><span class="sxs-lookup"><span data-stu-id="b754d-353">Uploading new videos</span></span>

<span data-ttu-id="b754d-354">您應該使用下列程序上傳任何新影片：</span><span class="sxs-lookup"><span data-stu-id="b754d-354">Any new videos should be uploaded using the following process:</span></span>

1. <span data-ttu-id="b754d-355">加入 IDWEB 上的 **docs_video_users** 群組。</span><span class="sxs-lookup"><span data-stu-id="b754d-355">Join the **docs_video_users** group on IDWEB.</span></span>
1. <span data-ttu-id="b754d-356">前往 https://aka.ms/VideoUploadRequest 並填妥影片的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b754d-356">Go to https://aka.ms/VideoUploadRequest and fill in the details for your video.</span></span> <span data-ttu-id="b754d-357">需要的項目 (請注意，這些項目都不會公開顯示)：</span><span class="sxs-lookup"><span data-stu-id="b754d-357">You will need (note that none of these items will be visible to the public):</span></span>
    1. <span data-ttu-id="b754d-358">影片標題。</span><span class="sxs-lookup"><span data-stu-id="b754d-358">A title for your video.</span></span>
    1. <span data-ttu-id="b754d-359">影片相關的產品/服務清單。</span><span class="sxs-lookup"><span data-stu-id="b754d-359">A list of products/services that your video is related to.</span></span>
    1. <span data-ttu-id="b754d-360">裝載影片的目標頁面或文件集 (如果您還沒有頁面的話)。</span><span class="sxs-lookup"><span data-stu-id="b754d-360">The target page or (if you don’t have the page yet) doc set that your video will be hosted on.</span></span>
    1. <span data-ttu-id="b754d-361">影片的 MP4 檔案連結 (如果您沒有位置存放檔案，可先暫時存放此處：`\\scratch2\scratch\apex`)。</span><span class="sxs-lookup"><span data-stu-id="b754d-361">A link to the MP4 file for your video (if you don’t have a location to put the file, you can put it here temporarily:   `\\scratch2\scratch\apex`).</span></span> <span data-ttu-id="b754d-362">MP4 檔案應該為 720p 或更高品質。</span><span class="sxs-lookup"><span data-stu-id="b754d-362">MP4 files should be 720p or higher.</span></span>
    1. <span data-ttu-id="b754d-363">影片的描述。</span><span class="sxs-lookup"><span data-stu-id="b754d-363">A description of the video.</span></span>
1. <span data-ttu-id="b754d-364">提交 (儲存) 該項目。</span><span class="sxs-lookup"><span data-stu-id="b754d-364">Submit (save) that item.</span></span>
1. <span data-ttu-id="b754d-365">在兩個工作天內，影片即可上傳。</span><span class="sxs-lookup"><span data-stu-id="b754d-365">Within two business days, the video will get uploaded.</span></span> <span data-ttu-id="b754d-366">您需要的內嵌連結會放在工作項目中，並解析後*回傳給您*。</span><span class="sxs-lookup"><span data-stu-id="b754d-366">The link you need for embedding will be placed into the work item, and it will be resolved *back to you*.</span></span>
1. <span data-ttu-id="b754d-367">取得影片連結後，請關閉工作項目。</span><span class="sxs-lookup"><span data-stu-id="b754d-367">Once you have grabbed the video link, close the work item.</span></span>
1. <span data-ttu-id="b754d-368">接著，您即可使用下列語法，將影片連結新增至貼文：</span><span class="sxs-lookup"><span data-stu-id="b754d-368">The video link can then be added to your post, using this syntax:</span></span>

   ```md
   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
   ```
