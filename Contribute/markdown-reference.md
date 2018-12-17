---
title: docs.microsoft.com 的 Markdown 參考
description: Markdown 的 Docs 平台指南。
author: meganbradley
ms.author: mbradley
manager: jemash
ms.date: 05/18/2018
ms.topic: contributor-guide
ms.prod: non-product-specific
audience: internal,external
ms.openlocfilehash: 1023f3036e5c1facd0bcd4c31069e6faf3c95483
ms.sourcegitcommit: 21c9ac71e1abff946466cddf17a1ee97bc349ec5
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/11/2018
ms.locfileid: "53245864"
---
# <a name="markdown-reference"></a><span data-ttu-id="cc242-103">Markdown 參考</span><span class="sxs-lookup"><span data-stu-id="cc242-103">Markdown Reference</span></span>

<span data-ttu-id="cc242-104">Markdown 是採用純文字格式語法的輕量型標記語言。</span><span class="sxs-lookup"><span data-stu-id="cc242-104">Markdown is a lightweight markup language with plain text formatting syntax.</span></span> <span data-ttu-id="cc242-105">Docs 平台 可支援 Markdown 的 CommonMark 標準，以及為提供 docs.microsoft.com 更豐富內容所設計的一些自訂 Markdown 延伸模組。</span><span class="sxs-lookup"><span data-stu-id="cc242-105">The Docs platform supports the CommonMark standard for Markdown, plus some custom Markdown extensions designed to provide richer content on docs.microsoft.com.</span></span> <span data-ttu-id="cc242-106">本文提供針對 docs.microsoft.com 使用 Markdown 的參考，按字母順序排列。</span><span class="sxs-lookup"><span data-stu-id="cc242-106">This article provides an alphabetical reference for using Markdown for docs.microsoft.com.</span></span>

<span data-ttu-id="cc242-107">您可以使用任何文字編輯器來撰寫 Markdown。</span><span class="sxs-lookup"><span data-stu-id="cc242-107">You can use any text editor to author Markdown.</span></span> <span data-ttu-id="cc242-108">為了讓編輯器可以協助插入標準 Markdown 語法和自訂 Docs 延伸模組，建議您安裝 [VS Code](https://code.visualstudio.com/) 和 [Docs 編寫套件](https://aka.ms/DocsAuthoringPack)。</span><span class="sxs-lookup"><span data-stu-id="cc242-108">For an editor that facilitates inserting both standard Markdown syntax and custom Docs extensions, we recommend [VS Code](https://code.visualstudio.com/) with the [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) installed.</span></span>

<span data-ttu-id="cc242-109">Dos 使用 Markdig Markdown 引擎。</span><span class="sxs-lookup"><span data-stu-id="cc242-109">Docs uses the Markdig Markdown engine.</span></span> <span data-ttu-id="cc242-110">您可以在 [https://babelmark.github.io/](https://babelmark.github.io/) 中測試 Markdig 和其他引擎的 Markdown 呈現。</span><span class="sxs-lookup"><span data-stu-id="cc242-110">You can test the rendering of Markdown in Markdig vs. other engines at [https://babelmark.github.io/](https://babelmark.github.io/).</span></span>

## <a name="alerts-note-tip-important-caution-warning"></a><span data-ttu-id="cc242-111">警示 (附註、提示、重要、注意、警告)</span><span class="sxs-lookup"><span data-stu-id="cc242-111">Alerts (Note, Tip, Important, Caution, Warning)</span></span>

<span data-ttu-id="cc242-112">警示是用來建立區塊引述的 Docs Markdown 延伸模組，該區塊引述會在 docs.microsoft.com 中呈現可指出內容重要性的色彩和圖示。</span><span class="sxs-lookup"><span data-stu-id="cc242-112">Alerts are a Docs Markdown extension to create block quotes that render on docs.microsoft.com with colors and icons that indicate the significance of the content.</span></span> <span data-ttu-id="cc242-113">支援的警示類型如下：</span><span class="sxs-lookup"><span data-stu-id="cc242-113">The following alert types are supported:</span></span>

```markdown
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

<span data-ttu-id="cc242-114">這些警示在 docs.microsoft.com 中看起來像這樣：</span><span class="sxs-lookup"><span data-stu-id="cc242-114">These alerts look like this on docs.microsoft.com:</span></span>

> [!NOTE]
> <span data-ttu-id="cc242-115">即使一眼看過去，使用者也應該注意到的資訊。</span><span class="sxs-lookup"><span data-stu-id="cc242-115">Information the user should notice even if skimming.</span></span>

> [!TIP]
> <span data-ttu-id="cc242-116">可協助使用者更成功的選用資訊。</span><span class="sxs-lookup"><span data-stu-id="cc242-116">Optional information to help a user be more successful.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cc242-117">使用者要成功的必要資訊。</span><span class="sxs-lookup"><span data-stu-id="cc242-117">Essential information required for user success.</span></span>

> [!CAUTION]
> <span data-ttu-id="cc242-118">動作可能會導致負面的結果。</span><span class="sxs-lookup"><span data-stu-id="cc242-118">Negative potential consequences of an action.</span></span>

> [!WARNING]
> <span data-ttu-id="cc242-119">動作可能會導致危險的結果。</span><span class="sxs-lookup"><span data-stu-id="cc242-119">Dangerous certain consequences of an action.</span></span>

## <a name="code-snippets"></a><span data-ttu-id="cc242-120">程式碼片段</span><span class="sxs-lookup"><span data-stu-id="cc242-120">Code snippets</span></span>

<span data-ttu-id="cc242-121">您可以在 Markdown 檔案中內嵌程式碼片段：</span><span class="sxs-lookup"><span data-stu-id="cc242-121">You can embed code snippets in your Markdown files:</span></span>

```markdown
[!code-<language>[<name>](<codepath><queryoption><queryoptionvalue> "<title>")]
```

## <a name="headings"></a><span data-ttu-id="cc242-122">標題</span><span class="sxs-lookup"><span data-stu-id="cc242-122">Headings</span></span>

<span data-ttu-id="cc242-123">Docs 支援六種層級的 Markdown 標題：</span><span class="sxs-lookup"><span data-stu-id="cc242-123">Docs supports six levels of Markdown headings:</span></span>

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- <span data-ttu-id="cc242-124">最後一個 `#` 和標題文字之間必須有一個空格。</span><span class="sxs-lookup"><span data-stu-id="cc242-124">There must be a space between the last `#` and heading text.</span></span>
- <span data-ttu-id="cc242-125">每個 Markdown 檔案都必須且只能有一個 H1。</span><span class="sxs-lookup"><span data-stu-id="cc242-125">Each Markdown file must have one and only one H1.</span></span>
- <span data-ttu-id="cc242-126">H1 必須是檔案中 YML 中繼資料區塊後的第一個內容。</span><span class="sxs-lookup"><span data-stu-id="cc242-126">The H1 must be the first content in the file after the YML metadata block.</span></span>
- <span data-ttu-id="cc242-127">H2 會自動顯示在已發佈檔案的瀏覽功能表右側。</span><span class="sxs-lookup"><span data-stu-id="cc242-127">H2s automatically appear in the right-hand navigating menu of the published file.</span></span> <span data-ttu-id="cc242-128">較低層級的標題則不會，因此請策略性地使用 H2 以協助讀者瀏覽您的內容。</span><span class="sxs-lookup"><span data-stu-id="cc242-128">Lower-level headings do not, so use H2s strategically to help readers navigate your content.</span></span>
- <span data-ttu-id="cc242-129">HMTL 標題 (例如 `<h1>`) 在有些情況下會造成建置警告，因此不建議您使用。</span><span class="sxs-lookup"><span data-stu-id="cc242-129">HMTL headings, such as `<h1>`, are not recommended and in some cases will cause build warnings.</span></span>
- <span data-ttu-id="cc242-130">您可以透過[書籤](#bookmark-links)連結至檔案中的個別標題。</span><span class="sxs-lookup"><span data-stu-id="cc242-130">You can link to individual headings in a file via [bookmarks](#bookmark-links).</span></span>

## <a name="html"></a><span data-ttu-id="cc242-131">HTML</span><span class="sxs-lookup"><span data-stu-id="cc242-131">HTML</span></span>

<span data-ttu-id="cc242-132">雖然 Markdown 支援內嵌 HTML，但仍不建議使用 HTML 來發佈至 Docs，因為除了有限的值清單以外，都會造成建置錯誤或警告。</span><span class="sxs-lookup"><span data-stu-id="cc242-132">Although Markdown supports inline HTML, HTML is not recommended for publishing to Docs, and except for a limited list of values will cause build errors or warnings.</span></span> <!--For more information, see HTML Whitelist. // do we want to add the whitelist? -->

## <a name="images"></a><span data-ttu-id="cc242-133">影像</span><span class="sxs-lookup"><span data-stu-id="cc242-133">Images</span></span>

<span data-ttu-id="cc242-134">包含影像的語法如下：</span><span class="sxs-lookup"><span data-stu-id="cc242-134">The syntax to include an image is:</span></span>

```markdown
![[alt text]](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

<span data-ttu-id="cc242-135">其中，`alt text` 是影像的簡短描述，而 `<folder path>` 是影像的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="cc242-135">Where `alt text` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="cc242-136">適用於視障者的螢幕助讀程式需要使用替代文字。</span><span class="sxs-lookup"><span data-stu-id="cc242-136">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="cc242-137">若發生影像無法呈現的網站錯誤時，替代文字也很實用。</span><span class="sxs-lookup"><span data-stu-id="cc242-137">It is also useful if there is a site bug where the image cannot render.</span></span>

<span data-ttu-id="cc242-138">影像應儲存在您文件集內的 `/media` 資料夾。</span><span class="sxs-lookup"><span data-stu-id="cc242-138">Images should be stored in a `/media` folder within your doc set.</span></span> <span data-ttu-id="cc242-139">以下是預設支援的影像檔案類型：</span><span class="sxs-lookup"><span data-stu-id="cc242-139">The following file types are supported by default for images:</span></span>

- <span data-ttu-id="cc242-140">.jpg</span><span class="sxs-lookup"><span data-stu-id="cc242-140">.jpg</span></span>
- <span data-ttu-id="cc242-141">.png</span><span class="sxs-lookup"><span data-stu-id="cc242-141">.png</span></span>

<span data-ttu-id="cc242-142">您可以將其他影像類型新增為文件集 docfx.json 檔<!--add link to reference when available-->的資源，以新增支援這些類型。</span><span class="sxs-lookup"><span data-stu-id="cc242-142">You can add support for other image types by adding them as resources to the docfx.json file<!--add link to reference when available--> for your doc set.</span></span>

## <a name="links"></a><span data-ttu-id="cc242-143">連結</span><span class="sxs-lookup"><span data-stu-id="cc242-143">Links</span></span>

<span data-ttu-id="cc242-144">在大部分情況下，Docs 都會使用標準 Markdown 連結至其他檔案和頁面。</span><span class="sxs-lookup"><span data-stu-id="cc242-144">In most cases, Docs uses standard Markdown links to other files and pages.</span></span> <span data-ttu-id="cc242-145">以下小節說明連結的類型。</span><span class="sxs-lookup"><span data-stu-id="cc242-145">The types of links are described in subsections below.</span></span>

> [!TIP]
> <span data-ttu-id="cc242-146">適用於 VS Code 的 Docs 編寫套件有助於正確插入相對連結和書籤，而不需與冗長的路徑奮戰！</span><span class="sxs-lookup"><span data-stu-id="cc242-146">The Docs Authoring Pack for VS Code can help insert relative links and bookmarks correctly without the tedium of figuring out the paths!</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cc242-147">請不要在您的 Microsoft 網站連結中包含地區設定代碼，例如 en-us。</span><span class="sxs-lookup"><span data-stu-id="cc242-147">Do not include locale codes, such as en-us, in your links to Microsoft sites.</span></span> <span data-ttu-id="cc242-148">硬式編碼的地區設定代碼會妨礙當地語系化內容的轉譯，而這會造成其他地區設定使用者的客戶體驗不佳，並產生高昂的當地語系化成本。</span><span class="sxs-lookup"><span data-stu-id="cc242-148">Hard-coded locale codes prevent localized content from rendering, which is a bad customer experience for users in other locales and incurs significant localization costs.</span></span> <span data-ttu-id="cc242-149">當您從瀏覽器複製 URL 時，預設會包含地區設定代碼，因此您必須在建立連結時手動將它刪除。</span><span class="sxs-lookup"><span data-stu-id="cc242-149">When you copy a URL from a browser, the locale code is included by default, so you need to manually delete it when you create your link.</span></span> <span data-ttu-id="cc242-150">例如，使用：</span><span class="sxs-lookup"><span data-stu-id="cc242-150">For example, use:</span></span>
>
> `[Microsoft](https://www.microsoft.com)`
>
> <span data-ttu-id="cc242-151">而非：</span><span class="sxs-lookup"><span data-stu-id="cc242-151">Not:</span></span>
>
> `[Microsoft](https://www.microsoft.com/en-us/)`

### <a name="relative-links-to-files-in-the-same-doc-set"></a><span data-ttu-id="cc242-152">相同文件集中檔案的相對連結</span><span class="sxs-lookup"><span data-stu-id="cc242-152">Relative links to files in the same doc set</span></span>

<span data-ttu-id="cc242-153">相對路徑是相對於目前檔案的目標檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="cc242-153">A relative path is the path to the target file relative to the current file.</span></span> <span data-ttu-id="cc242-154">在 Docs 中，您可以使用相對路徑連結至相同文件集內的其他檔案。</span><span class="sxs-lookup"><span data-stu-id="cc242-154">In Docs, you can use a relative path to link to another file within the same doc set.</span></span> <span data-ttu-id="cc242-155">相對路徑的語法如下：</span><span class="sxs-lookup"><span data-stu-id="cc242-155">The syntax for a relative path is as follows:</span></span>

```markdown
[link text](../../folder/filename.md)
```

<span data-ttu-id="cc242-156">其中，`../` 表示階層中的上一個層級。</span><span class="sxs-lookup"><span data-stu-id="cc242-156">Where `../` indicates one level above in the hierarchy.</span></span>

- <span data-ttu-id="cc242-157">相對路徑會在建置期間解析，包括移除 .md 副檔名。</span><span class="sxs-lookup"><span data-stu-id="cc242-157">The relative path will be resolved during the build, including removal of the .md extension.</span></span>
- <span data-ttu-id="cc242-158">您可以使用 "../" 連結至父資料夾中的檔案，但該檔案必須位於相同的文件集中。</span><span class="sxs-lookup"><span data-stu-id="cc242-158">You can use "../" to link to a file in the parent folder, but that file has to be in the same doc set.</span></span> <span data-ttu-id="cc242-159">您無法使用 "../" 連結至另一個文件集資料夾中的檔案。</span><span class="sxs-lookup"><span data-stu-id="cc242-159">You cannot use "../" to link to a file in another doc set folder.</span></span>
- <span data-ttu-id="cc242-160">Docs 也支援開頭為 "~" 的特殊格式相對路徑 (例如 ~/foo/bar.md)。</span><span class="sxs-lookup"><span data-stu-id="cc242-160">Docs also supports a special form of relative path that starts with "~" (for example, ~/foo/bar.md).</span></span> <span data-ttu-id="cc242-161">此語法表示檔案是相對於文件集的根資料夾。</span><span class="sxs-lookup"><span data-stu-id="cc242-161">This syntax indicates a file relative to the root folder of a doc set.</span></span> <span data-ttu-id="cc242-162">這種路徑也會在建置期間進行驗證及解析。</span><span class="sxs-lookup"><span data-stu-id="cc242-162">This kind of path is also validated and resolved during the build.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cc242-163">在相對路徑中包含副檔名。</span><span class="sxs-lookup"><span data-stu-id="cc242-163">Include the file extension in the relative path.</span></span> <span data-ttu-id="cc242-164">組建可驗證該相對路徑的目標檔案是否存在。</span><span class="sxs-lookup"><span data-stu-id="cc242-164">Build validates the existence of the target file of that relative path.</span></span> <span data-ttu-id="cc242-165">如果相對路徑未包含副檔名，組建就可能會回報連結中斷的警告。</span><span class="sxs-lookup"><span data-stu-id="cc242-165">If relative path does not include file extension, it is likely build will report a warning of broken link.</span></span> <span data-ttu-id="cc242-166">例如，使用：</span><span class="sxs-lookup"><span data-stu-id="cc242-166">For example, use:</span></span>
>
> `[link text](../../folder/filename.md)`
>
> <span data-ttu-id="cc242-167">而非：</span><span class="sxs-lookup"><span data-stu-id="cc242-167">Not:</span></span>
>
> `[link text](../../folder/filename)`

### <a name="site-relative-links-to-other-files-on-docs"></a><span data-ttu-id="cc242-168">Docs 上其他檔案的站台相關連結</span><span class="sxs-lookup"><span data-stu-id="cc242-168">Site relative links to other files on Docs</span></span>

```markdown
[Azure and Linux](/articles/virtual-machines/linux/overview)
```

<span data-ttu-id="cc242-169">請不要包含副檔名 (.md)。</span><span class="sxs-lookup"><span data-stu-id="cc242-169">Do not include the file extension (.md).</span></span> <span data-ttu-id="cc242-170">此為來自外部 Azure「文章」文件集的 Linux 概觀檔連結。</span><span class="sxs-lookup"><span data-stu-id="cc242-170">This links to the Linux overview file from outside the Azure "articles" doc set.</span></span>

### <a name="links-to-external-sites"></a><span data-ttu-id="cc242-171">外部網站的連結</span><span class="sxs-lookup"><span data-stu-id="cc242-171">Links to external sites</span></span>

```markdown
[Microsoft](https://www.microsoft.com)
```

<span data-ttu-id="cc242-172">其他網頁的 URL 連結 (必須包含 https://)。</span><span class="sxs-lookup"><span data-stu-id="cc242-172">URL-based link to another web page (must include https://).</span></span>

### <a name="bookmark-links"></a><span data-ttu-id="cc242-173">書籤連結</span><span class="sxs-lookup"><span data-stu-id="cc242-173">Bookmark links</span></span>

<span data-ttu-id="cc242-174">相同存放庫中其他檔案的標題書籤連結：</span><span class="sxs-lookup"><span data-stu-id="cc242-174">Bookmark link to a heading in another file in the same repo:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<span data-ttu-id="cc242-175">目前檔案中的標題書籤連結：</span><span class="sxs-lookup"><span data-stu-id="cc242-175">Bookmark link to a heading in the current file:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<span data-ttu-id="cc242-176">使用主題標籤後接標題文字，移除標點符號並將空格取代為虛線。</span><span class="sxs-lookup"><span data-stu-id="cc242-176">Use a hash tag followed by the words of the heading with punctuation removed and spaces replaced with dashes.</span></span>

### <a name="explicit-anchor-links"></a><span data-ttu-id="cc242-177">明確錨點連結</span><span class="sxs-lookup"><span data-stu-id="cc242-177">Explicit anchor links</span></span>

<span data-ttu-id="cc242-178">除非在中樞和登陸頁面中，否則**沒有必要也不建議使用**含 `<a>` HTML 標籤的明確錨點連結。</span><span class="sxs-lookup"><span data-stu-id="cc242-178">Explicit anchor links using the `<a>` HTML tag are **not required or recommended** except in hub and landing pages.</span></span> <span data-ttu-id="cc242-179">請如上所述在一般 Markdown 檔案中使用書籤。</span><span class="sxs-lookup"><span data-stu-id="cc242-179">Use bookmarks as described above in general Markdown files.</span></span> <span data-ttu-id="cc242-180">針對中樞和登陸頁面，請如下所示使用錨點：</span><span class="sxs-lookup"><span data-stu-id="cc242-180">For hub and landing pages, use anchors as follows:</span></span>

<span data-ttu-id="cc242-181">`## <a id="AnchorText"> </a>Header text` 或 `## <a name="AnchorText"> </a>Header text`</span><span class="sxs-lookup"><span data-stu-id="cc242-181">`## <a id="AnchorText"> </a>Header text` or `## <a name="AnchorText"> </a>Header text`</span></span>

<span data-ttu-id="cc242-182">若要連結至明確錨點，請使用下列語法：</span><span class="sxs-lookup"><span data-stu-id="cc242-182">To link to explicit anchors, use the following syntax:</span></span>

```markdown
To go to a section on the same page:
[text](#AnchorText)

To go to a section on another page.
[text](FileName.md#AnchorText)
```

### <a name="xref-cross-reference-links"></a><span data-ttu-id="cc242-183">XREF (交互參照) 連結</span><span class="sxs-lookup"><span data-stu-id="cc242-183">XREF (cross reference) links</span></span>

<span data-ttu-id="cc242-184">若要連結至目前文件集或其他文件集中自動產生的 API 參照頁面，請使用 XREF 連結與唯一識別碼 (UID)。</span><span class="sxs-lookup"><span data-stu-id="cc242-184">To link to auto-generated API references pages in the current doc set or other doc sets, use XREF links with the unique ID (UID).</span></span>

> [!NOTE]
> <span data-ttu-id="cc242-185">若要參考其他文件集中的 API 參考頁面，您必須在 `docfx.json` 檔案中新增 `xrefService` 設定。</span><span class="sxs-lookup"><span data-stu-id="cc242-185">To reference API reference pages in other doc sets, you need to add `xrefService` configuration in `docfx.json` file.</span></span>
> ```
> "build": {
>   ...
>   "xrefService": [ "https://xref.docs.microsoft.com/query?uid={uid}" ]
> }
> ```

<span data-ttu-id="cc242-186">UID 等同於完整的類別和成員名稱。</span><span class="sxs-lookup"><span data-stu-id="cc242-186">The UID equates to the fully qualified class and member name.</span></span> <span data-ttu-id="cc242-187">如果您在 UID 之後加上 \*，則連結代表多載頁面，而不是特定的 API。</span><span class="sxs-lookup"><span data-stu-id="cc242-187">If you add a \* after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="cc242-188">例如，使用 `List<T>.BinarySearch*` 連結至 BinarySearch 方法頁面，而不是連結至特定多載，例如 `List<T>.BinarySearch(T, IComparer<T>)`。</span><span class="sxs-lookup"><span data-stu-id="cc242-188">For example, use `List<T>.BinarySearch*` to link to the BinarySearch Method page instead of linking to a specific overload such as `List<T>.BinarySearch(T, IComparer<T>)`.</span></span>

<span data-ttu-id="cc242-189">您可以使用下列其中一個語法：</span><span class="sxs-lookup"><span data-stu-id="cc242-189">You can use one of the following syntaxes:</span></span>

- <span data-ttu-id="cc242-190">自動連結：`<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="cc242-190">Auto-link: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span></span>

  <span data-ttu-id="cc242-191">選用的 `displayProperty` 查詢參數會產生完整的連結文字。</span><span class="sxs-lookup"><span data-stu-id="cc242-191">The optional `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="cc242-192">根據預設，連結文字只會顯示成員或型別名稱。</span><span class="sxs-lookup"><span data-stu-id="cc242-192">By default, link text shows only the member or type name.</span></span>

- <span data-ttu-id="cc242-193">Markdown 連結：`[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="cc242-193">Markdown link: `[link text](xref:UID)`</span></span>
  
  <span data-ttu-id="cc242-194">用於您要自訂顯示的連結文字時。</span><span class="sxs-lookup"><span data-stu-id="cc242-194">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="cc242-195">範例：</span><span class="sxs-lookup"><span data-stu-id="cc242-195">Examples:</span></span>

- <span data-ttu-id="cc242-196">`<xref:System.String>` 會轉譯為 "String"。</span><span class="sxs-lookup"><span data-stu-id="cc242-196">`<xref:System.String>` renders as "String".</span></span>
- <span data-ttu-id="cc242-197">`<xref:System.String?displayProperty=nameWithType>` 會轉譯為 "System.String"。</span><span class="sxs-lookup"><span data-stu-id="cc242-197">`<xref:System.String?displayProperty=nameWithType>` renders as "System.String".</span></span>
- <span data-ttu-id="cc242-198">`[String class](xref:System.String)` 會轉譯為 "String class"。</span><span class="sxs-lookup"><span data-stu-id="cc242-198">`[String class](xref:System.String)` renders as "String class".</span></span>

<span data-ttu-id="cc242-199">目前還沒有較輕鬆的方式可用來尋找 UID。</span><span class="sxs-lookup"><span data-stu-id="cc242-199">Right now, there is no easy way to find the UIDs.</span></span> <span data-ttu-id="cc242-200"><!-- ? -->若要尋找 API 的 UID，最佳方法就是檢視所要連結 API 頁面的來源，然後尋找 ms.assetid 值。</span><span class="sxs-lookup"><span data-stu-id="cc242-200"><!-- ? -->The best way to find the UID for an API is to view the source for the API page you want to link to and find the ms.assetid value.</span></span> <span data-ttu-id="cc242-201">個別的多載值不會顯示在來源中。</span><span class="sxs-lookup"><span data-stu-id="cc242-201">Individual overload values are not shown in the source.</span></span> <span data-ttu-id="cc242-202">我們正努力讓系統在未來會更好。</span><span class="sxs-lookup"><span data-stu-id="cc242-202">We're working on having a better system in the future.</span></span>

<span data-ttu-id="cc242-203">當 UID 包含特殊字元 \`、\# 或 \* 時，UID 值必須分別以 HTML 編碼為 `%60`、`%23` 和 `%2A`。</span><span class="sxs-lookup"><span data-stu-id="cc242-203">When the UID contains the special characters \`, \#, or \*, the UID value needs to be HTML encoded as `%60`, `%23`, and `%2A`, respectively.</span></span> <span data-ttu-id="cc242-204">有時候您會看到括號也會被編碼，但這並非必要。</span><span class="sxs-lookup"><span data-stu-id="cc242-204">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="cc242-205">範例：</span><span class="sxs-lookup"><span data-stu-id="cc242-205">Examples:</span></span>

- <span data-ttu-id="cc242-206">System.Threading.Tasks.Task\`1 變成 `System.Threading.Tasks.Task%601`</span><span class="sxs-lookup"><span data-stu-id="cc242-206">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="cc242-207">System.Exception.\#ctor 變成 `System.Exception.%23ctor`</span><span class="sxs-lookup"><span data-stu-id="cc242-207">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="cc242-208">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) 變成 `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span><span class="sxs-lookup"><span data-stu-id="cc242-208">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<!-- leave out of Contributor Guide for now
Using XREF may require some configuration. For more information, see XREF Service.
-->

## <a name="lists-numbered-bulleted-checklist"></a><span data-ttu-id="cc242-209">清單 (編號、分項、檢查清單)</span><span class="sxs-lookup"><span data-stu-id="cc242-209">Lists (Numbered, Bulleted, Checklist)</span></span>

### <a name="numbered-list"></a><span data-ttu-id="cc242-210">編號清單</span><span class="sxs-lookup"><span data-stu-id="cc242-210">Numbered list</span></span>

<span data-ttu-id="cc242-211">若要建立編號清單，您可以全部都使用 1，系統即會在發佈時將其轉譯為連續清單。</span><span class="sxs-lookup"><span data-stu-id="cc242-211">To create a numbered list, you can use all 1s, which are rendered as a sequential list when published.</span></span> <span data-ttu-id="cc242-212">為了讓來源更方便閱讀，您可以遞增清單。</span><span class="sxs-lookup"><span data-stu-id="cc242-212">For increased source readability, you can increment your lists.</span></span>

<span data-ttu-id="cc242-213">請不要在清單中使用字母，包括巢狀清單。</span><span class="sxs-lookup"><span data-stu-id="cc242-213">Do not use letters in lists, including nested lists.</span></span> <span data-ttu-id="cc242-214">透過 Docs 發佈時，字母無法正確轉譯。如果是使用數字的巢狀清單，系統在發佈時會轉譯為小寫字母。</span><span class="sxs-lookup"><span data-stu-id="cc242-214">They do not render correctly when published to Docs. Nested lists using numbers will render as lowercase letters when published.</span></span> <span data-ttu-id="cc242-215">例如：</span><span class="sxs-lookup"><span data-stu-id="cc242-215">For example:</span></span>

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

<span data-ttu-id="cc242-216">這會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="cc242-216">This renders as follows:</span></span>

1. <span data-ttu-id="cc242-217">這是</span><span class="sxs-lookup"><span data-stu-id="cc242-217">This is</span></span>
1. <span data-ttu-id="cc242-218">父代編號清單</span><span class="sxs-lookup"><span data-stu-id="cc242-218">a parent numbered list</span></span>
   1. <span data-ttu-id="cc242-219">而這是</span><span class="sxs-lookup"><span data-stu-id="cc242-219">and this is</span></span>
   1. <span data-ttu-id="cc242-220">巢狀編號清單</span><span class="sxs-lookup"><span data-stu-id="cc242-220">a nested numbered list</span></span>
1. <span data-ttu-id="cc242-221">(fin)</span><span class="sxs-lookup"><span data-stu-id="cc242-221">(fin)</span></span>

### <a name="bulleted-list"></a><span data-ttu-id="cc242-222">項目符號清單</span><span class="sxs-lookup"><span data-stu-id="cc242-222">Bulleted list</span></span>

<span data-ttu-id="cc242-223">若要建立項目符號清單，請在每行開頭使用 `-` 後接空格：</span><span class="sxs-lookup"><span data-stu-id="cc242-223">To create a bulleted list, use `-` followed by a space at the beginning of each line:</span></span>

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

<span data-ttu-id="cc242-224">這會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="cc242-224">This renders as follows:</span></span>

- <span data-ttu-id="cc242-225">這是</span><span class="sxs-lookup"><span data-stu-id="cc242-225">This is</span></span>
- <span data-ttu-id="cc242-226">父代項目符號清單</span><span class="sxs-lookup"><span data-stu-id="cc242-226">a parent bulleted list</span></span>
  - <span data-ttu-id="cc242-227">而這是</span><span class="sxs-lookup"><span data-stu-id="cc242-227">and this is</span></span>
  - <span data-ttu-id="cc242-228">巢狀項目符號清單</span><span class="sxs-lookup"><span data-stu-id="cc242-228">a nested bulleted list</span></span>
- <span data-ttu-id="cc242-229">完成！</span><span class="sxs-lookup"><span data-stu-id="cc242-229">All done!</span></span>

### <a name="checklist"></a><span data-ttu-id="cc242-230">檢查清單</span><span class="sxs-lookup"><span data-stu-id="cc242-230">Checklist</span></span>

<span data-ttu-id="cc242-231">您可透過自訂 Markdown 延伸模組，在 docs.microsoft.com (僅限於此) 上使用檢查清單：</span><span class="sxs-lookup"><span data-stu-id="cc242-231">Checklists are available for use on docs.microsoft.com (only) via a custom Markdown extension:</span></span>

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

<span data-ttu-id="cc242-232">此範例在 docs.microsoft.com 上的轉譯如下：</span><span class="sxs-lookup"><span data-stu-id="cc242-232">This example renders on docs.microsoft.com like this:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="cc242-233">清單項目 1</span><span class="sxs-lookup"><span data-stu-id="cc242-233">List item 1</span></span>
> * <span data-ttu-id="cc242-234">清單項目 2</span><span class="sxs-lookup"><span data-stu-id="cc242-234">List item 2</span></span>
> * <span data-ttu-id="cc242-235">清單項目 3</span><span class="sxs-lookup"><span data-stu-id="cc242-235">List item 3</span></span>

<span data-ttu-id="cc242-236">您可在文章的開頭或結尾使用檢查清單，來摘要「您將學到什麼」或「您已學到的內容」。</span><span class="sxs-lookup"><span data-stu-id="cc242-236">Use checklists at the beginning or end of an article to summarize "What will you learn" or "What have you learned" content.</span></span> <span data-ttu-id="cc242-237">請不要在整篇文章中新增隨機檢查清單。</span><span class="sxs-lookup"><span data-stu-id="cc242-237">Do not add random checklists throughout your articles.</span></span>
<!-- is this guidance still accurate? -->

## <a name="next-step-action"></a><span data-ttu-id="cc242-238">下一步動作</span><span class="sxs-lookup"><span data-stu-id="cc242-238">Next step action</span></span>

<span data-ttu-id="cc242-239">您可使用自訂延伸模組，將下一步動作按鈕新增至 docs.microsoft.com (僅限於此) 上的頁面。</span><span class="sxs-lookup"><span data-stu-id="cc242-239">You can use a custom extension to add a next step action button to pages on docs.microsoft.com (only).</span></span>

<span data-ttu-id="cc242-240">語法如下：</span><span class="sxs-lookup"><span data-stu-id="cc242-240">The syntax is as follows:</span></span>

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

<span data-ttu-id="cc242-241">例如：</span><span class="sxs-lookup"><span data-stu-id="cc242-241">For example:</span></span>

```markdown
> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)
```

<span data-ttu-id="cc242-242">這會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="cc242-242">This renders as follows:</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="cc242-243">了解基本樣式</span><span class="sxs-lookup"><span data-stu-id="cc242-243">Learn about basic style</span></span>](style-quick-start.md)

<span data-ttu-id="cc242-244">您可以在下一步動作中使用任何支援的連結，包括其他網頁的 Markdown 連結。</span><span class="sxs-lookup"><span data-stu-id="cc242-244">You can use any supported link in a next step action, including a Markdown link to another web page.</span></span> <span data-ttu-id="cc242-245">在大部分情況下，下一步動作連結都是相同文件集中其他檔案的相對連結。</span><span class="sxs-lookup"><span data-stu-id="cc242-245">In most cases, the next action link will be a relative link to another file in the same doc set.</span></span>

## <a name="section-definition"></a><span data-ttu-id="cc242-246">區段定義</span><span class="sxs-lookup"><span data-stu-id="cc242-246">Section definition</span></span>

<span data-ttu-id="cc242-247"><!-- more info about this would be helpful! --> 您可能需要定義區段。</span><span class="sxs-lookup"><span data-stu-id="cc242-247"><!-- more info about this would be helpful! --> You might need to define a section.</span></span> <span data-ttu-id="cc242-248">此語法最常用於程式碼表格。</span><span class="sxs-lookup"><span data-stu-id="cc242-248">This syntax is mostly used for code tables.</span></span>
<span data-ttu-id="cc242-249">請參閱下列範例：</span><span class="sxs-lookup"><span data-stu-id="cc242-249">See the following example:</span></span>

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

<span data-ttu-id="cc242-250">上述區塊引述 Markdown 文字會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="cc242-250">The preceding blockquote Markdown text will be rendered as:</span></span>
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```

## <a name="selectors"></a><span data-ttu-id="cc242-251">選取器</span><span class="sxs-lookup"><span data-stu-id="cc242-251">Selectors</span></span>

<span data-ttu-id="cc242-252"><!-- could be more clear! --> 當您想要連線到同一篇文章的不同頁面，可以使用選取器。</span><span class="sxs-lookup"><span data-stu-id="cc242-252"><!-- could be more clear! --> You can use a selector when you want to connect different pages for the same article.</span></span> <span data-ttu-id="cc242-253">讀者即可在這些頁面間切換。</span><span class="sxs-lookup"><span data-stu-id="cc242-253">Readers can then switch between those pages.</span></span>

> [!NOTE]
> <span data-ttu-id="cc242-254">此延伸在 docs.microsoft.com 和 MSDN 的運作方式不同。</span><span class="sxs-lookup"><span data-stu-id="cc242-254">This extension works differently between docs.microsoft.com and MSDN.</span></span> <!-- should we keep info about MSDN? If so say how they differ?-->

### <a name="single-selector"></a><span data-ttu-id="cc242-255">單一選取器</span><span class="sxs-lookup"><span data-stu-id="cc242-255">Single selector</span></span>

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

<span data-ttu-id="cc242-256">... 轉譯結果如下：</span><span class="sxs-lookup"><span data-stu-id="cc242-256">... will be rendered like this:</span></span>

> [!div class="op_single_selector"]
> - [通用 Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)

### <a name="multi-selector"></a><span data-ttu-id="cc242-265">多重選取器</span><span class="sxs-lookup"><span data-stu-id="cc242-265">Multi-selector</span></span>

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

<span data-ttu-id="cc242-266">... 轉譯結果如下：</span><span class="sxs-lookup"><span data-stu-id="cc242-266">... will be rendered like this:</span></span>

> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
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

## <a name="tables"></a><span data-ttu-id="cc242-277">表格</span><span class="sxs-lookup"><span data-stu-id="cc242-277">Tables</span></span>

<span data-ttu-id="cc242-278">在 Markdown 中建立表格的最簡單做法是使用直立線符號及線條。</span><span class="sxs-lookup"><span data-stu-id="cc242-278">The simplest way to create a table in Markdown is to use pipes and lines.</span></span> <span data-ttu-id="cc242-279">若要建立含標題的標準表格，請沿著第一個線段與虛線：</span><span class="sxs-lookup"><span data-stu-id="cc242-279">To create a standard table with a header, follow the first line with dashed line:</span></span>

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

<span data-ttu-id="cc242-280">這會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="cc242-280">This renders as follows:</span></span>

|<span data-ttu-id="cc242-281">這是</span><span class="sxs-lookup"><span data-stu-id="cc242-281">This is</span></span>   |<span data-ttu-id="cc242-282">簡單的</span><span class="sxs-lookup"><span data-stu-id="cc242-282">a simple</span></span>   |<span data-ttu-id="cc242-283">表格標題</span><span class="sxs-lookup"><span data-stu-id="cc242-283">table header</span></span>|
|----------|-----------|------------|
|<span data-ttu-id="cc242-284">表格</span><span class="sxs-lookup"><span data-stu-id="cc242-284">table</span></span>     |<span data-ttu-id="cc242-285">資料</span><span class="sxs-lookup"><span data-stu-id="cc242-285">data</span></span>       |<span data-ttu-id="cc242-286">這裡</span><span class="sxs-lookup"><span data-stu-id="cc242-286">here</span></span>        |
|<span data-ttu-id="cc242-287">其實</span><span class="sxs-lookup"><span data-stu-id="cc242-287">it doesn't</span></span>|<span data-ttu-id="cc242-288">並不</span><span class="sxs-lookup"><span data-stu-id="cc242-288">actually</span></span>   |<span data-ttu-id="cc242-289">需要完全對齊！</span><span class="sxs-lookup"><span data-stu-id="cc242-289">have to line up nicely!</span></span>||

<span data-ttu-id="cc242-290">您也可以建立不含標題的表格。</span><span class="sxs-lookup"><span data-stu-id="cc242-290">You can also create a table without a header.</span></span> <span data-ttu-id="cc242-291">例如，若要建立多重資料行清單：</span><span class="sxs-lookup"><span data-stu-id="cc242-291">For example, to create a multiple-column list:</span></span>

```markdown
|   |   |
| - | - |
| This | table |
| has no | header |
```

<span data-ttu-id="cc242-292">這會轉譯如下：</span><span class="sxs-lookup"><span data-stu-id="cc242-292">This renders like this:</span></span>

|   |   |
| - | - |
| <span data-ttu-id="cc242-293">此</span><span class="sxs-lookup"><span data-stu-id="cc242-293">This</span></span> | <span data-ttu-id="cc242-294">表格</span><span class="sxs-lookup"><span data-stu-id="cc242-294">table</span></span> |
| <span data-ttu-id="cc242-295">不含任何</span><span class="sxs-lookup"><span data-stu-id="cc242-295">has no</span></span> | <span data-ttu-id="cc242-296">標題</span><span class="sxs-lookup"><span data-stu-id="cc242-296">header</span></span> |

<span data-ttu-id="cc242-297">您可以使用冒號對齊資料行：</span><span class="sxs-lookup"><span data-stu-id="cc242-297">You can align the columns by using colons:</span></span>

```markdown
|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|
```

<span data-ttu-id="cc242-298">轉譯如下：</span><span class="sxs-lookup"><span data-stu-id="cc242-298">Renders as follows:</span></span>

|                  |
|------------------|
|    <span data-ttu-id="cc242-299">靠右對齊：</span><span class="sxs-lookup"><span data-stu-id="cc242-299">right aligned:</span></span>|
|<span data-ttu-id="cc242-300">：靠左對齊</span><span class="sxs-lookup"><span data-stu-id="cc242-300">:left aligned</span></span>     |
|<span data-ttu-id="cc242-301">：置中對齊        :</span><span class="sxs-lookup"><span data-stu-id="cc242-301">:centered        :</span></span>|

> [!TIP]
> 適用於 VS Code 的 Docs 編寫延伸模組可讓您輕鬆新增基本 Markdown 表格！
>
> 您也可以使用[線上表格產生器](http://www.tablesgenerator.com/markdown_tables)。

### <a name="mx-tdbreakall"></a><span data-ttu-id="cc242-304">mx-tdBreakAll</span><span class="sxs-lookup"><span data-stu-id="cc242-304">mx-tdBreakAll</span></span>

> [!IMPORTANT]
> 此功能僅適用於 docs.microsoft.com 網站。

<span data-ttu-id="cc242-306">如果您使用 Markdown 建立表格，該表格可能會擴展到右側導覽，變得難以閱讀。</span><span class="sxs-lookup"><span data-stu-id="cc242-306">If you create a table in Markdown, the table might expand to the right navigation and become unreadable.</span></span> <span data-ttu-id="cc242-307">您可以藉由允許 Docs 轉譯視需要切割表格，來解決此問題。</span><span class="sxs-lookup"><span data-stu-id="cc242-307">You can solve that by allowing Docs rendering to break the table when needed.</span></span> <span data-ttu-id="cc242-308">您只要使用自訂類別 `[!div class="mx-tdBreakAll"]` 加在表格前後即可。</span><span class="sxs-lookup"><span data-stu-id="cc242-308">Just wrap up the table with the custom class `[!div class="mx-tdBreakAll"]`.</span></span>

<span data-ttu-id="cc242-309">以下是具有三列的表格 Markdown 範例，會以類別名稱為 `mx-tdBreakAll` 的 `div` 加在表格前後。</span><span class="sxs-lookup"><span data-stu-id="cc242-309">Here is a Markdown sample of a table with three rows that will be wrapped by a `div` with the class name `mx-tdBreakAll`.</span></span>

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

<span data-ttu-id="cc242-310">轉譯結果如下：</span><span class="sxs-lookup"><span data-stu-id="cc242-310">It will be rendered like this:</span></span>

> [!div class="mx-tdBreakAll"]
> |<span data-ttu-id="cc242-311">名稱</span><span class="sxs-lookup"><span data-stu-id="cc242-311">Name</span></span>|<span data-ttu-id="cc242-312">語法</span><span class="sxs-lookup"><span data-stu-id="cc242-312">Syntax</span></span>|<span data-ttu-id="cc242-313">對無訊息安裝為必要？</span><span class="sxs-lookup"><span data-stu-id="cc242-313">Mandatory for silent installation?</span></span>|<span data-ttu-id="cc242-314">描述</span><span class="sxs-lookup"><span data-stu-id="cc242-314">Description</span></span>|
> |-------------|----------|---------|---------|
> |<span data-ttu-id="cc242-315">Quiet</span><span class="sxs-lookup"><span data-stu-id="cc242-315">Quiet</span></span>|<span data-ttu-id="cc242-316">/quiet</span><span class="sxs-lookup"><span data-stu-id="cc242-316">/quiet</span></span>|<span data-ttu-id="cc242-317">是</span><span class="sxs-lookup"><span data-stu-id="cc242-317">Yes</span></span>|<span data-ttu-id="cc242-318">執行安裝程式，而不顯示 UI 和提示。</span><span class="sxs-lookup"><span data-stu-id="cc242-318">Runs the installer, displaying no UI and no prompts.</span></span>|
> |<span data-ttu-id="cc242-319">NoRestart</span><span class="sxs-lookup"><span data-stu-id="cc242-319">NoRestart</span></span>|<span data-ttu-id="cc242-320">/norestart</span><span class="sxs-lookup"><span data-stu-id="cc242-320">/norestart</span></span>|<span data-ttu-id="cc242-321">否</span><span class="sxs-lookup"><span data-stu-id="cc242-321">No</span></span>|<span data-ttu-id="cc242-322">隱藏重新啟動的任何嘗試。</span><span class="sxs-lookup"><span data-stu-id="cc242-322">Suppresses any attempts to restart.</span></span> <span data-ttu-id="cc242-323">根據預設，UI 會在重新啟動前出現提示。</span><span class="sxs-lookup"><span data-stu-id="cc242-323">By default, the UI will prompt before restart.</span></span>|
> |<span data-ttu-id="cc242-324">Help</span><span class="sxs-lookup"><span data-stu-id="cc242-324">Help</span></span>|<span data-ttu-id="cc242-325">/help</span><span class="sxs-lookup"><span data-stu-id="cc242-325">/help</span></span>|<span data-ttu-id="cc242-326">否</span><span class="sxs-lookup"><span data-stu-id="cc242-326">No</span></span>|<span data-ttu-id="cc242-327">提供說明和快速參考。</span><span class="sxs-lookup"><span data-stu-id="cc242-327">Provides help and quick reference.</span></span> <span data-ttu-id="cc242-328">顯示安裝命令的正確用法，包括所有選項和行為的清單。</span><span class="sxs-lookup"><span data-stu-id="cc242-328">Displays the correct use of the setup command, including a list of all options and behaviors.</span></span>|

### <a name="mx-tdcol2breakall"></a><span data-ttu-id="cc242-329">mx-tdCol2BreakAll</span><span class="sxs-lookup"><span data-stu-id="cc242-329">mx-tdCol2BreakAll</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cc242-330">此功能僅適用於 docs.microsoft.com 網站。</span><span class="sxs-lookup"><span data-stu-id="cc242-330">This only works on the docs.microsoft.com site.</span></span>

<span data-ttu-id="cc242-331">有時候，在您表格中第二欄的字詞可能會很長。</span><span class="sxs-lookup"><span data-stu-id="cc242-331">From time to time, you might have very long words in the second column of a table.</span></span> <span data-ttu-id="cc242-332">為了讓它們妥善分隔，您可以使用先前所示的 `div` 包裝函式語法來套用類別 `mx-tdCol2BreakAll`。</span><span class="sxs-lookup"><span data-stu-id="cc242-332">To ensure they are broken apart nicely, you can apply the class `mx-tdCol2BreakAll` by using the `div` wrapper syntax as shown earlier.</span></span>

### <a name="html-tables"></a><span data-ttu-id="cc242-333">HTML 表格</span><span class="sxs-lookup"><span data-stu-id="cc242-333">HTML Tables</span></span>

<span data-ttu-id="cc242-334">HTML 表格不建議用於 docs.microsoft.com。</span><span class="sxs-lookup"><span data-stu-id="cc242-334">HTML tables are not recommended for docs.microsoft.com.</span></span> <span data-ttu-id="cc242-335">這類表格不是使用者可看懂的來源，而這與 Markdown 主要準則抵觸。</span><span class="sxs-lookup"><span data-stu-id="cc242-335">They are not human readable in the source - which is a key principle of Markdown.</span></span>

<!--If you use HTML tables and your Markdown is not being rendered between the two tables, you need to add a closing `br` tag after the closing `table` tag.

![break HTML tables](media/break-tables.png)
-->

## <a name="videos"></a><span data-ttu-id="cc242-336">影片</span><span class="sxs-lookup"><span data-stu-id="cc242-336">Videos</span></span>

### <a name="embedding-videos-into-a-markdown-page"></a><span data-ttu-id="cc242-337">將影片內嵌在 Markdown 頁面中</span><span class="sxs-lookup"><span data-stu-id="cc242-337">Embedding videos into a Markdown page</span></span>

<span data-ttu-id="cc242-338">目前，Docs 可支援將影片發佈至下列三個位置之一：</span><span class="sxs-lookup"><span data-stu-id="cc242-338">Currently, Docs can support videos published to one of three locations:</span></span>

- <span data-ttu-id="cc242-339">YouTube</span><span class="sxs-lookup"><span data-stu-id="cc242-339">YouTube</span></span>
- <span data-ttu-id="cc242-340">Channel 9</span><span class="sxs-lookup"><span data-stu-id="cc242-340">Channel 9</span></span>
- <span data-ttu-id="cc242-341">Microsoft 專屬的 'One Player' 系統</span><span class="sxs-lookup"><span data-stu-id="cc242-341">Microsoft's own 'One Player' system</span></span>

<span data-ttu-id="cc242-342">您可以使用下列語法內嵌影片，而 Docs 會加以轉譯。</span><span class="sxs-lookup"><span data-stu-id="cc242-342">You can embed a video with the following syntax, and Docs will render it.</span></span>

```markdown
> [!VIDEO <embedded_video_link>]
```

<span data-ttu-id="cc242-343">範例：</span><span class="sxs-lookup"><span data-stu-id="cc242-343">Example:</span></span>

```markdown
> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
```

<span data-ttu-id="cc242-344">... 將會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="cc242-344">... will be rendered as:</span></span>

```html
<iframe src="https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>

<iframe src="https://www.youtube-nocookie.com/embed/iAtwVM-Z7rY" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
<iframe src="https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
```

<span data-ttu-id="cc242-345">並在發佈頁面上顯示如下：</span><span class="sxs-lookup"><span data-stu-id="cc242-345">And it will be displayed like this on published pages:</span></span>

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

> [!IMPORTANT]
> <span data-ttu-id="cc242-346">CH9 影片 URL 應該以 `https` 開頭並以 `/player` 結尾。</span><span class="sxs-lookup"><span data-stu-id="cc242-346">The CH9 video URL should start with `https` and end with `/player`.</span></span> <span data-ttu-id="cc242-347">否則，它會內嵌整頁而不只是影片。</span><span class="sxs-lookup"><span data-stu-id="cc242-347">Otherwise, it will embed the whole page instead of the video only.</span></span>

### <a name="uploading-new-videos"></a><span data-ttu-id="cc242-348">上傳新影片</span><span class="sxs-lookup"><span data-stu-id="cc242-348">Uploading new videos</span></span>

<span data-ttu-id="cc242-349">您應該使用下列程序上傳任何新影片：</span><span class="sxs-lookup"><span data-stu-id="cc242-349">Any new videos should be uploaded using the following process:</span></span>

1. <span data-ttu-id="cc242-350">加入 IDWEB 上的 **docs_video_users** 群組。</span><span class="sxs-lookup"><span data-stu-id="cc242-350">Join the **docs_video_users** group on IDWEB.</span></span>
1. <span data-ttu-id="cc242-351">前往 https://aka.ms/VideoUploadRequest 並填妥影片的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="cc242-351">Go to https://aka.ms/VideoUploadRequest and fill in the details for your video.</span></span> <span data-ttu-id="cc242-352">需要的項目 (請注意，這些項目都不會公開顯示)：</span><span class="sxs-lookup"><span data-stu-id="cc242-352">You will need (note that none of these items will be visible to the public):</span></span>
    1. <span data-ttu-id="cc242-353">影片標題。</span><span class="sxs-lookup"><span data-stu-id="cc242-353">A title for your video.</span></span>
    1. <span data-ttu-id="cc242-354">影片相關的產品/服務清單。</span><span class="sxs-lookup"><span data-stu-id="cc242-354">A list of products/services that your video is related to.</span></span>
    1. <span data-ttu-id="cc242-355">裝載影片的目標頁面或文件集 (如果您還沒有頁面的話)。</span><span class="sxs-lookup"><span data-stu-id="cc242-355">The target page or (if you don’t have the page yet) doc set that your video will be hosted on.</span></span>
    1. <span data-ttu-id="cc242-356">影片的 MP4 檔案連結 (如果您沒有位置存放檔案，可先暫時存放此處：`\\scratch2\scratch\apex`)。</span><span class="sxs-lookup"><span data-stu-id="cc242-356">A link to the MP4 file for your video (if you don’t have a location to put the file, you can put it here temporarily:   `\\scratch2\scratch\apex`).</span></span> <span data-ttu-id="cc242-357">MP4 檔案應該為 720p 或更高品質。</span><span class="sxs-lookup"><span data-stu-id="cc242-357">MP4 files should be 720p or higher.</span></span>
    1. <span data-ttu-id="cc242-358">影片的描述。</span><span class="sxs-lookup"><span data-stu-id="cc242-358">A description of the video.</span></span>
1. <span data-ttu-id="cc242-359">提交 (儲存) 該項目。</span><span class="sxs-lookup"><span data-stu-id="cc242-359">Submit (save) that item.</span></span>
1. <span data-ttu-id="cc242-360">在兩個工作天內，影片即可上傳。</span><span class="sxs-lookup"><span data-stu-id="cc242-360">Within two business days, the video will get uploaded.</span></span> <span data-ttu-id="cc242-361">您需要的內嵌連結會放在工作項目中，並解析後*回傳給您*。</span><span class="sxs-lookup"><span data-stu-id="cc242-361">The link you need for embedding will be placed into the work item, and it will be resolved *back to you*.</span></span>
1. <span data-ttu-id="cc242-362">取得影片連結後，請關閉工作項目。</span><span class="sxs-lookup"><span data-stu-id="cc242-362">Once you have grabbed the video link, close the work item.</span></span>
1. <span data-ttu-id="cc242-363">接著，您即可使用下列語法，將影片連結新增至貼文：</span><span class="sxs-lookup"><span data-stu-id="cc242-363">The video link can then be added to your post, using this syntax:</span></span>

   ```markdown
   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
   ```
