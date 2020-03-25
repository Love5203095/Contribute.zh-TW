---
title: docs.microsoft.com 的 Markdown 參考
description: 了解 Microsoft Docs 平台中所使用的 Markdown 功能和語法。
author: meganbradley
ms.author: mbradley
ms.date: 01/30/2020
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.openlocfilehash: c1568264c687ebaf26048f5432fdea7d5132c012
ms.sourcegitcommit: 216ef77ca2cd1eeb31c6c89d96778b178fc0d540
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/21/2020
ms.locfileid: "80070090"
---
# <a name="docs-markdown-reference"></a><span data-ttu-id="e171f-103">Docs Markdown 參考</span><span class="sxs-lookup"><span data-stu-id="e171f-103">Docs Markdown reference</span></span>

<span data-ttu-id="e171f-104">本文提供針對 docs.microsoft.com (Docs) 撰寫 Markdown 的參考資訊，按字母順序排列。</span><span class="sxs-lookup"><span data-stu-id="e171f-104">This article provides an alphabetical reference for writing Markdown for docs.microsoft.com (Docs).</span></span>

<span data-ttu-id="e171f-105">[Markdown](https://daringfireball.net/projects/markdown/) 是採用純文字格式語法的輕量型標記語言。</span><span class="sxs-lookup"><span data-stu-id="e171f-105">[Markdown](https://daringfireball.net/projects/markdown/) is a lightweight markup language with plain text formatting syntax.</span></span> <span data-ttu-id="e171f-106">Docs 支援符合 [CommonMark](https://commonmark.org/) 規範且透過 [Markdig](https://github.com/lunet-io/markdig) 剖析引擎剖析的 Markdown。</span><span class="sxs-lookup"><span data-stu-id="e171f-106">Docs supports [CommonMark](https://commonmark.org/) compliant Markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine.</span></span> <span data-ttu-id="e171f-107">Docs 也支援自訂 Markdown 延伸模組，可在 Docs 網站上提供更豐富的內容。</span><span class="sxs-lookup"><span data-stu-id="e171f-107">Docs also supports custom Markdown extensions that provide richer content on the Docs site.</span></span>

<span data-ttu-id="e171f-108">您可以使用任何文字編輯器撰寫 Markdown，但建議您使用 [Visual Studio Code](https://code.visualstudio.com/) 搭配 [Docs 編寫套件](https://aka.ms/DocsAuthoringPack)。</span><span class="sxs-lookup"><span data-stu-id="e171f-108">You can use any text editor to write Markdown, but we recommend [Visual Studio Code](https://code.visualstudio.com/) with the [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack).</span></span> <span data-ttu-id="e171f-109">Docs 編寫套件提供編輯工具和預覽功能，可讓您看到您的文章在 Docs 上轉譯出來的樣子。</span><span class="sxs-lookup"><span data-stu-id="e171f-109">The Docs Authoring Pack provides editing tools and preview functionality that lets you see what your articles will look like when rendered on Docs.</span></span>

## <a name="alerts-note-tip-important-caution-warning"></a><span data-ttu-id="e171f-110">警示 (附註、提示、重要、注意、警告)</span><span class="sxs-lookup"><span data-stu-id="e171f-110">Alerts (Note, Tip, Important, Caution, Warning)</span></span>

<span data-ttu-id="e171f-111">警示是用來建立區塊引述的Markdown 延伸模組，在 docs.microsoft.com 中這些區塊引述會呈現出可表示內容重要性的色彩和圖示。</span><span class="sxs-lookup"><span data-stu-id="e171f-111">Alerts are a Markdown extension to create block quotes that render on docs.microsoft.com with colors and icons that indicate the significance of the content.</span></span> <span data-ttu-id="e171f-112">支援的警示類型如下：</span><span class="sxs-lookup"><span data-stu-id="e171f-112">The following alert types are supported:</span></span>

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

<span data-ttu-id="e171f-113">這些警示在 docs.microsoft.com 中看起來像這樣：</span><span class="sxs-lookup"><span data-stu-id="e171f-113">These alerts look like this on docs.microsoft.com:</span></span>

> [!NOTE]
> <span data-ttu-id="e171f-114">Information the user should notice even if skimming.</span><span class="sxs-lookup"><span data-stu-id="e171f-114">Information the user should notice even if skimming.</span></span>

> [!TIP]
> <span data-ttu-id="e171f-115">Optional information to help a user be more successful.</span><span class="sxs-lookup"><span data-stu-id="e171f-115">Optional information to help a user be more successful.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e171f-116">Essential information required for user success.</span><span class="sxs-lookup"><span data-stu-id="e171f-116">Essential information required for user success.</span></span>

> [!CAUTION]
> <span data-ttu-id="e171f-117">Negative potential consequences of an action.</span><span class="sxs-lookup"><span data-stu-id="e171f-117">Negative potential consequences of an action.</span></span>

> [!WARNING]
> <span data-ttu-id="e171f-118">Dangerous certain consequences of an action.</span><span class="sxs-lookup"><span data-stu-id="e171f-118">Dangerous certain consequences of an action.</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="e171f-119">角括號</span><span class="sxs-lookup"><span data-stu-id="e171f-119">Angle brackets</span></span>

<span data-ttu-id="e171f-120">如果您在文字中使用角括號 (例如，用來代表預留位置)，需要手動將角括號編碼。</span><span class="sxs-lookup"><span data-stu-id="e171f-120">If you use angle brackets in text in your file--for example, to denote a placeholder--you need to manually encode the angle brackets.</span></span> <span data-ttu-id="e171f-121">否則 Markdown 會將它們視為 HTML 標籤。</span><span class="sxs-lookup"><span data-stu-id="e171f-121">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="e171f-122">例如，將 `<script name>` 編碼成 `&lt;script name&gt;` 或 `\<script name>`。</span><span class="sxs-lookup"><span data-stu-id="e171f-122">For example, encode `<script name>` as `&lt;script name&gt;` or `\<script name>`.</span></span>

<span data-ttu-id="e171f-123">在格式化為內嵌程式碼或程式碼區塊的文字中，角括號不需要逸出。</span><span class="sxs-lookup"><span data-stu-id="e171f-123">Angle brackets don't have to be escaped in text formatted as inline code or in code blocks.</span></span>

## <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="e171f-124">縮寫符號和雙引號</span><span class="sxs-lookup"><span data-stu-id="e171f-124">Apostrophes and quotation marks</span></span>

<span data-ttu-id="e171f-125">如果您將內容從 Word 複製到 Markdown 編輯器中，文字可能會包含「智慧」(彎曲) 縮寫符號或雙引號。</span><span class="sxs-lookup"><span data-stu-id="e171f-125">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="e171f-126">這些必須編碼或變更為基本縮寫符號或雙引號。</span><span class="sxs-lookup"><span data-stu-id="e171f-126">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="e171f-127">否則檔案發佈後可能會產生這樣的內容：Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="e171f-127">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="e171f-128">以下是這些標點符號的「智慧」版本編碼：</span><span class="sxs-lookup"><span data-stu-id="e171f-128">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="e171f-129">左 (開頭) 雙引號：`&#8220;`</span><span class="sxs-lookup"><span data-stu-id="e171f-129">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="e171f-130">右 (結尾) 雙引號：`&#8221;`</span><span class="sxs-lookup"><span data-stu-id="e171f-130">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="e171f-131">右 (結尾) 單引號或縮寫符號：`&#8217;`</span><span class="sxs-lookup"><span data-stu-id="e171f-131">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="e171f-132">左 (開頭) 單引號 (很少使用)：`&#8216;`</span><span class="sxs-lookup"><span data-stu-id="e171f-132">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

## <a name="blockquotes"></a><span data-ttu-id="e171f-133">區塊引述</span><span class="sxs-lookup"><span data-stu-id="e171f-133">Blockquotes</span></span>

<span data-ttu-id="e171f-134">區塊引述使用 `>` 字元建立：</span><span class="sxs-lookup"><span data-stu-id="e171f-134">Blockquotes are created using the `>` character:</span></span>

```md
> This is a blockquote. It is usually rendered indented and with a different background color.
```

<span data-ttu-id="e171f-135">前述範例會如下呈現：</span><span class="sxs-lookup"><span data-stu-id="e171f-135">The preceding example renders as follows:</span></span>

> <span data-ttu-id="e171f-136">This is a blockquote.</span><span class="sxs-lookup"><span data-stu-id="e171f-136">This is a blockquote.</span></span> <span data-ttu-id="e171f-137">It is usually rendered indented and with a different background color.</span><span class="sxs-lookup"><span data-stu-id="e171f-137">It is usually rendered indented and with a different background color.</span></span>

## <a name="bold-and-italic-text"></a><span data-ttu-id="e171f-138">粗體與斜體文字</span><span class="sxs-lookup"><span data-stu-id="e171f-138">Bold and italic text</span></span>

<span data-ttu-id="e171f-139">若要將文字格式設定為**粗體**，請使用兩個星號將它括住：</span><span class="sxs-lookup"><span data-stu-id="e171f-139">To format text as **bold**, enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="e171f-140">若要將文字格式設定為*斜體*，請使用單一星號將它括住：</span><span class="sxs-lookup"><span data-stu-id="e171f-140">To format text as *italic*, enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="e171f-141">若要將文字格式設定為***粗體加斜體***，請使用三個星號將它括住：</span><span class="sxs-lookup"><span data-stu-id="e171f-141">To format text as both ***bold and italic***, enclose it in three asterisks:</span></span>

```markdown
This text is both ***bold and italic***.
```

## <a name="code-snippets"></a><span data-ttu-id="e171f-142">程式碼片段</span><span class="sxs-lookup"><span data-stu-id="e171f-142">Code snippets</span></span>

<span data-ttu-id="e171f-143">Docs Markdown 支援將程式碼片段內嵌在句子中，或是將「隔離」的個別區塊放在句子之間。</span><span class="sxs-lookup"><span data-stu-id="e171f-143">Docs Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="e171f-144">如需詳細資訊，請參閱[如何在 Docs 中新增程式碼](code-in-docs.md)。</span><span class="sxs-lookup"><span data-stu-id="e171f-144">For more information, see [How to add code to docs](code-in-docs.md).</span></span>

## <a name="columns"></a><span data-ttu-id="e171f-145">columns</span><span class="sxs-lookup"><span data-stu-id="e171f-145">Columns</span></span>

<span data-ttu-id="e171f-146">**columns** (資料行) Markdown 延伸模組讓 Docs 作者能夠加入以資料行配置的內容，比只適用於真正表格資料的基本 Markdown 資料表更具彈性且功能強大。</span><span class="sxs-lookup"><span data-stu-id="e171f-146">The **columns** Markdown extension gives Docs authors the ability to add column-based content layouts that are more flexible and powerful than basic Markdown tables, which are only suited for true tabular data.</span></span> <span data-ttu-id="e171f-147">您最多可以加入四個資料行，並使用選擇性的 `span` 屬性來合併兩個或更多資料行。</span><span class="sxs-lookup"><span data-stu-id="e171f-147">You can add up to four columns, and use the optional `span` attribute to merge two or more columns.</span></span>

<span data-ttu-id="e171f-148">columns 的語法如下：</span><span class="sxs-lookup"><span data-stu-id="e171f-148">The syntax for columns is as follows:</span></span>

```markdown
:::row:::
   :::column span="":::
      Content...
   :::column-end:::
   :::column span="":::
      More content...
   :::column-end:::
:::row-end:::
```

<span data-ttu-id="e171f-149">資料行只能包含基本 Markdown，包括影像。</span><span class="sxs-lookup"><span data-stu-id="e171f-149">Columns should only contain basic Markdown, including images.</span></span> <span data-ttu-id="e171f-150">不應包含標題、資料表、索引標籤和其他複雜的結構。</span><span class="sxs-lookup"><span data-stu-id="e171f-150">Headings, tables, tabs, and other complex structures shouldn't be included.</span></span> <span data-ttu-id="e171f-151">資料列不能有任何內容落在資料行之外。</span><span class="sxs-lookup"><span data-stu-id="e171f-151">A row can't have any content outside of column.</span></span>

<span data-ttu-id="e171f-152">例如，下列 Markdown 會建立一個橫跨兩資料行寬度的資料行，以及一個標準 (無 `span`) 資料行：</span><span class="sxs-lookup"><span data-stu-id="e171f-152">For example, the following Markdown creates one column that spans two column widths, and one standard (no `span`) column:</span></span>

```markdown
:::row:::
   :::column span="2":::
      **This is a 2-span column with lots of text.**

      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec vestibulum mollis nunc
      ornare commodo. Nullam ac metus imperdiet, rutrum justo vel, vulputate leo. Donec
      rutrum non eros eget consectetur.
   :::column-end:::
   :::column span="":::
      **This is a single-span column with an image in it.**

      ![Doc.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::
```

<span data-ttu-id="e171f-153">這會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="e171f-153">This renders as follows:</span></span>

:::row:::
   :::column span="2":::
      <span data-ttu-id="e171f-154">**This is a 2-span column with lots of text.**</span><span class="sxs-lookup"><span data-stu-id="e171f-154">**This is a 2-span column with lots of text.**</span></span>

      <span data-ttu-id="e171f-155">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</span><span class="sxs-lookup"><span data-stu-id="e171f-155">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</span></span> <span data-ttu-id="e171f-156">Donec vestibulum mollis nunc ornare commodo.</span><span class="sxs-lookup"><span data-stu-id="e171f-156">Donec vestibulum mollis nunc ornare commodo.</span></span> <span data-ttu-id="e171f-157">Nullam ac metus imperdiet, rutrum justo vel, vulputate leo.</span><span class="sxs-lookup"><span data-stu-id="e171f-157">Nullam ac metus imperdiet, rutrum justo vel, vulputate leo.</span></span> <span data-ttu-id="e171f-158">Donec rutrum non eros eget consectetur.</span><span class="sxs-lookup"><span data-stu-id="e171f-158">Donec rutrum non eros eget consectetur.</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="e171f-159">**This is a single-span column with an image in it.**</span><span class="sxs-lookup"><span data-stu-id="e171f-159">**This is a single-span column with an image in it.**</span></span>

      ![Doc.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::

## <a name="headings"></a><span data-ttu-id="e171f-161">標題</span><span class="sxs-lookup"><span data-stu-id="e171f-161">Headings</span></span>

<span data-ttu-id="e171f-162">Docs 支援六種層級的 Markdown 標題：</span><span class="sxs-lookup"><span data-stu-id="e171f-162">Docs supports six levels of Markdown headings:</span></span>

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- <span data-ttu-id="e171f-163">最後一個 `#` 和標題文字之間必須有一個空格。</span><span class="sxs-lookup"><span data-stu-id="e171f-163">There must be a space between the last `#` and heading text.</span></span>
- <span data-ttu-id="e171f-164">每個 Markdown 檔案都必須且只能有一個 H1 標題。</span><span class="sxs-lookup"><span data-stu-id="e171f-164">Each Markdown file must have one and only one H1 heading.</span></span>
- <span data-ttu-id="e171f-165">H1 標題必須是檔案中 YML 中繼資料區塊後的第一個內容。</span><span class="sxs-lookup"><span data-stu-id="e171f-165">The H1 heading must be the first content in the file after the YML metadata block.</span></span>
- <span data-ttu-id="e171f-166">H2 標題會自動顯示在已發佈檔案的瀏覽功能表右側。</span><span class="sxs-lookup"><span data-stu-id="e171f-166">H2 headings automatically appear in the right-hand navigating menu of the published file.</span></span> <span data-ttu-id="e171f-167">較低層級的標題則不會，因此請策略性地使用 H2 以協助讀者瀏覽您的內容。</span><span class="sxs-lookup"><span data-stu-id="e171f-167">Lower-level headings don't appear, so use H2s strategically to help readers navigate your content.</span></span>
- <span data-ttu-id="e171f-168">HTML 標題 (例如 `<h1>`) 在有些情況下會造成建置警告，因此不建議使用。</span><span class="sxs-lookup"><span data-stu-id="e171f-168">HTML headings, such as `<h1>`, aren't recommended, and in some cases will cause build warnings.</span></span>
- <span data-ttu-id="e171f-169">您可以透過[書籤連結](how-to-write-links.md#links-to-anchors)連至檔案中的個別標題。</span><span class="sxs-lookup"><span data-stu-id="e171f-169">You can link to individual headings in a file via [bookmark links](how-to-write-links.md#links-to-anchors).</span></span>

## <a name="html"></a><span data-ttu-id="e171f-170">HTML</span><span class="sxs-lookup"><span data-stu-id="e171f-170">HTML</span></span>

<span data-ttu-id="e171f-171">雖然 Markdown 支援內嵌 HTML，但仍不建議使用 HTML 來發佈至 Docs，因為除了有限的值清單以外，都會造成建置錯誤或警告。</span><span class="sxs-lookup"><span data-stu-id="e171f-171">Although Markdown supports inline HTML, HTML isn't recommended for publishing to Docs, and except for a limited list of values will cause build errors or warnings.</span></span> 

## <a name="images"></a><span data-ttu-id="e171f-172">影像</span><span class="sxs-lookup"><span data-stu-id="e171f-172">Images</span></span>

<span data-ttu-id="e171f-173">以下是預設支援的影像檔案類型：</span><span class="sxs-lookup"><span data-stu-id="e171f-173">The following file types are supported by default for images:</span></span>

- <span data-ttu-id="e171f-174">.jpg</span><span class="sxs-lookup"><span data-stu-id="e171f-174">.jpg</span></span>
- <span data-ttu-id="e171f-175">.png</span><span class="sxs-lookup"><span data-stu-id="e171f-175">.png</span></span>

### <a name="standard-conceptual-images-default-markdown"></a><span data-ttu-id="e171f-176">標準概念影像 (預設 Markdown)</span><span class="sxs-lookup"><span data-stu-id="e171f-176">Standard conceptual images (default Markdown)</span></span>

<span data-ttu-id="e171f-177">用來內嵌影像的基本 Markdown 語法為：</span><span class="sxs-lookup"><span data-stu-id="e171f-177">The basic Markdown syntax to embed an image is:</span></span>

```Markdown
![<alt text>](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

<span data-ttu-id="e171f-178">其中，`<alt text>` 是影像的簡短描述，而 `<folder path>` 是影像的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="e171f-178">Where `<alt text>` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="e171f-179">適用於視障者的螢幕助讀程式需要使用替代文字。</span><span class="sxs-lookup"><span data-stu-id="e171f-179">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="e171f-180">若發生影像無法轉譯的網站錯誤時，替代文字也很實用。</span><span class="sxs-lookup"><span data-stu-id="e171f-180">It's also useful if there's a site bug where the image can't render.</span></span>

<span data-ttu-id="e171f-181">替代文字中的底線不會正確轉譯出來，除非您在前面加上反斜線 (`\_`) 加以逸出。</span><span class="sxs-lookup"><span data-stu-id="e171f-181">Underscores in alt text aren't rendered properly unless you escape them by prefixing them with a backslash (`\_`).</span></span> <span data-ttu-id="e171f-182">不過，請勿複製檔案名稱做為替代文字。</span><span class="sxs-lookup"><span data-stu-id="e171f-182">However, don't copy file names for use as alt text.</span></span> <span data-ttu-id="e171f-183">例如，不應使用：</span><span class="sxs-lookup"><span data-stu-id="e171f-183">For example, instead of this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="e171f-184">而是寫成：</span><span class="sxs-lookup"><span data-stu-id="e171f-184">Write this:</span></span>

```markdown
![Active Directory extension for two-factor authentication, step 4: Configure](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="standard-conceptual-images-docs-markdown"></a><span data-ttu-id="e171f-185">標準概念影像 (Docs Markdown)</span><span class="sxs-lookup"><span data-stu-id="e171f-185">Standard conceptual images (Docs Markdown)</span></span>

<span data-ttu-id="e171f-186">Docs 自訂 `:::image:::` 延伸模組支援標準影像、複雜影像、圖示。</span><span class="sxs-lookup"><span data-stu-id="e171f-186">The Docs custom `:::image:::` extension supports standard images, complex images, and icons.</span></span>

<span data-ttu-id="e171f-187">針對標準影像，較舊的 Markdown 語法仍然可以運作，但建議使用新的延伸模組，因為後者支援更強大的功能，例如指定與父系主題不同的當地語系化範圍。</span><span class="sxs-lookup"><span data-stu-id="e171f-187">For standard images, the older Markdown syntax will still work, but the new extension is recommended because it supports more powerful functionality, such as specifying a localization scope that's different from the parent topic.</span></span> <span data-ttu-id="e171f-188">未來將會提供其他先進的功能，例如從共用影像庫中選取，而不是指定本機影像。</span><span class="sxs-lookup"><span data-stu-id="e171f-188">Other advanced functionality, such as selecting from the shared image gallery instead of specifying a local image, will be available in the future.</span></span> <span data-ttu-id="e171f-189">新語法如下：</span><span class="sxs-lookup"><span data-stu-id="e171f-189">The new syntax is as follows:</span></span>

```Markdown
:::image type="content" source="<folderPath>" alt-text="<alt text>":::
```

<span data-ttu-id="e171f-190">如果 `type="content"` (預設值)，則 `source` 和 `alt-text` 都是必要的。</span><span class="sxs-lookup"><span data-stu-id="e171f-190">If `type="content"` (the default), both `source` and `alt-text` are required.</span></span>

### <a name="complex-images-with-long-descriptions"></a><span data-ttu-id="e171f-191">具有長描述的複雜影像</span><span class="sxs-lookup"><span data-stu-id="e171f-191">Complex images with long descriptions</span></span>

<span data-ttu-id="e171f-192">您也可以使用此延伸模組，新增具有長描述的影像，這種描述會由螢幕助讀程式朗讀，但不會視覺呈現在發佈的頁面上。</span><span class="sxs-lookup"><span data-stu-id="e171f-192">You can also use this extension to add an image with a long description that is read by screen readers but not rendered visually on the published page.</span></span> <span data-ttu-id="e171f-193">長描述是複雜影像 (例如圖形) 所必需的協助。</span><span class="sxs-lookup"><span data-stu-id="e171f-193">Long descriptions are an accessibility requirement for complex images, such as graphs.</span></span> <span data-ttu-id="e171f-194">語法如下：</span><span class="sxs-lookup"><span data-stu-id="e171f-194">The syntax is the following:</span></span>

```Markdown
:::image type="complex" source="<folderPath>" alt-text="<alt text>":::
   <long description here>
:::image-end:::
```

<span data-ttu-id="e171f-195">如果 `type="complex"`，則 `source`、`alt-text`、長描述、`:::image-end:::` 標記都是必要的。</span><span class="sxs-lookup"><span data-stu-id="e171f-195">If `type="complex"`, `source`, `alt-text`, a long description, and the `:::image-end:::` tag are all required.</span></span>

### <a name="specifying-loc-scope"></a><span data-ttu-id="e171f-196">指定 loc-scope</span><span class="sxs-lookup"><span data-stu-id="e171f-196">Specifying loc-scope</span></span>

<span data-ttu-id="e171f-197">有時候，影像的當地語系化範圍 (localization scope) 與包含它的文章或模組不同。</span><span class="sxs-lookup"><span data-stu-id="e171f-197">Sometimes the localization scope for an image is different from that of the article or module that contains it.</span></span> <span data-ttu-id="e171f-198">這可能會導致不良的全球體驗：例如，如果產品的螢幕擷取畫面不小心當地語系化成無法使用產品的語言。</span><span class="sxs-lookup"><span data-stu-id="e171f-198">This can cause a bad global experience: for example, if a screenshot of a product is accidentally localized into a language the product isn't available in.</span></span> <span data-ttu-id="e171f-199">若要避免這種情況，您可以在 `content` 和 `complex` 類型的影像中指定選擇性的 `loc-scope` 屬性。</span><span class="sxs-lookup"><span data-stu-id="e171f-199">To prevent this, you can specify the optional `loc-scope` attribute in images of types `content` and `complex`.</span></span>

### <a name="icons"></a><span data-ttu-id="e171f-200">圖示</span><span class="sxs-lookup"><span data-stu-id="e171f-200">Icons</span></span>

<span data-ttu-id="e171f-201">影像延伸模組支援圖示，圖示是裝飾影像，不應該有替代文字。</span><span class="sxs-lookup"><span data-stu-id="e171f-201">The image extension supports icons, which are decorative images and should not have alt text.</span></span> <span data-ttu-id="e171f-202">圖示的語法為：</span><span class="sxs-lookup"><span data-stu-id="e171f-202">The syntax for icons is:</span></span>

```Markdown
:::image type="icon" source="<folderPath>":::
```

<span data-ttu-id="e171f-203">若 `type="icon"`，則應指定 `source`。</span><span class="sxs-lookup"><span data-stu-id="e171f-203">If `type="icon"`, only `source` should be specified.</span></span>

## <a name="included-markdown-files"></a><span data-ttu-id="e171f-204">include 的 Markdown 檔案</span><span class="sxs-lookup"><span data-stu-id="e171f-204">Included Markdown files</span></span>

<span data-ttu-id="e171f-205">在多篇文章中需要重複 Markdown 檔案的情況，您可以使用 include 檔案。</span><span class="sxs-lookup"><span data-stu-id="e171f-205">Where markdown files need to be repeated in multiple articles, you can use an include file.</span></span> <span data-ttu-id="e171f-206">include 功能會指示 Docs 在組建階段以 include 檔案的內容取代參考。</span><span class="sxs-lookup"><span data-stu-id="e171f-206">The includes feature instructs Docs to replace the reference with the contents of the include file at build time.</span></span> <span data-ttu-id="e171f-207">您可以下列方式使用 include：</span><span class="sxs-lookup"><span data-stu-id="e171f-207">You can use includes in the following ways:</span></span>

- <span data-ttu-id="e171f-208">內嵌：在一個句子中重複使用常用程式碼片段內嵌。</span><span class="sxs-lookup"><span data-stu-id="e171f-208">Inline: Reuse a common text snippet inline with within a sentence.</span></span>
- <span data-ttu-id="e171f-209">區塊：您重複使用整個 Markdown 檔案作為區塊 (巢狀嵌入文章中的小節)。</span><span class="sxs-lookup"><span data-stu-id="e171f-209">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>

<span data-ttu-id="e171f-210">內嵌或區塊 include 檔案是簡單的 Markdown (.md) 檔案。</span><span class="sxs-lookup"><span data-stu-id="e171f-210">An inline or block include file is a Markdown (.md) file.</span></span> <span data-ttu-id="e171f-211">它可以包含任何有效的 Markdown。</span><span class="sxs-lookup"><span data-stu-id="e171f-211">It can contain any valid Markdown.</span></span> <span data-ttu-id="e171f-212">include 檔案通常放在通用的*includes* 子目錄中，此子目錄則位於存放庫的根目錄。</span><span class="sxs-lookup"><span data-stu-id="e171f-212">Include files are typically located in a common *includes* subdirectory, in the root of the repository.</span></span> <span data-ttu-id="e171f-213">當文章發行之後，包含的檔案會直接整合到其中。</span><span class="sxs-lookup"><span data-stu-id="e171f-213">When the article is published, the included file is seamlessly integrated into it.</span></span>

### <a name="includes-syntax"></a><span data-ttu-id="e171f-214">include 語法</span><span class="sxs-lookup"><span data-stu-id="e171f-214">Includes syntax</span></span>

<span data-ttu-id="e171f-215">區塊 include 是自己一行：</span><span class="sxs-lookup"><span data-stu-id="e171f-215">Block include is on its own line:</span></span>

```markdown
[!INCLUDE [<title>](<filepath>)]
```

<span data-ttu-id="e171f-216">內嵌 include 是放在一行之中：</span><span class="sxs-lookup"><span data-stu-id="e171f-216">Inline include is within a line:</span></span>

```markdown
Text before [!INCLUDE [<title>](<filepath>)] and after.
```

<span data-ttu-id="e171f-217">其中 `<title>` 是檔案的名稱，而 `<filepath>` 是檔案的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="e171f-217">Where `<title>` is the name of the file and `<filepath>` is the relative path to the file.</span></span> <span data-ttu-id="e171f-218">`INCLUDE` 必須大寫，而且 `<title>` 前面必須有一個空格。</span><span class="sxs-lookup"><span data-stu-id="e171f-218">`INCLUDE` must be capitalized and there must be a space before the `<title>`.</span></span>

<span data-ttu-id="e171f-219">以下是 Include 檔案的需求與考量：</span><span class="sxs-lookup"><span data-stu-id="e171f-219">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="e171f-220">針對大量內容 (例如一兩個段落、共用的程序或共用的節) 使用區塊包含。</span><span class="sxs-lookup"><span data-stu-id="e171f-220">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="e171f-221">請勿將它們用在小於一個句子的內容。</span><span class="sxs-lookup"><span data-stu-id="e171f-221">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="e171f-222">include 檔案將不會在文章的 GitHub 轉譯檢視中呈現，因為它們依靠 Docs 延伸模組。</span><span class="sxs-lookup"><span data-stu-id="e171f-222">Includes won't be rendered in the GitHub rendered view of your article, because they rely on Docs extensions.</span></span> <span data-ttu-id="e171f-223">它們將會在發行集之後才轉譯。</span><span class="sxs-lookup"><span data-stu-id="e171f-223">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="e171f-224">請務必將 include 檔案中的文字撰寫成完整的句子或片語，且不相依於參考 include 之文章中的上下文。</span><span class="sxs-lookup"><span data-stu-id="e171f-224">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="e171f-225">忽略此指導方針會使文章中產生無法翻譯的字串。</span><span class="sxs-lookup"><span data-stu-id="e171f-225">Ignoring this guidance creates an untranslatable string in the article.</span></span>
- <span data-ttu-id="e171f-226">請勿將 include 檔案嵌入其他 include 檔案中。</span><span class="sxs-lookup"><span data-stu-id="e171f-226">Don't embed include files within other include files.</span></span>
- <span data-ttu-id="e171f-227">將媒體檔案放在包含資料夾的特定 media 資料夾中，例如 */includes/media`<repo>`* 資料夾。</span><span class="sxs-lookup"><span data-stu-id="e171f-227">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`*/includes/media* folder.</span></span> <span data-ttu-id="e171f-228">media  目錄的根目錄中不應包含任何影像。</span><span class="sxs-lookup"><span data-stu-id="e171f-228">The *media* directory should not contain any images in its root.</span></span> <span data-ttu-id="e171f-229">如果 include 沒有影像，則不需要對應的 media  目錄。</span><span class="sxs-lookup"><span data-stu-id="e171f-229">If the include does not have images, a corresponding *media* directory is not required.</span></span>
- <span data-ttu-id="e171f-230">對於一般文章，請勿在不同包含檔案之間共用媒體。</span><span class="sxs-lookup"><span data-stu-id="e171f-230">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="e171f-231">請針對每個包含檔案和文章，使用具有唯一名稱的個別檔案。</span><span class="sxs-lookup"><span data-stu-id="e171f-231">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="e171f-232">將媒體檔案儲存在與該包含檔案相關聯的 [media] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="e171f-232">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="e171f-233">請勿將包含檔案做為文章的唯一內容。</span><span class="sxs-lookup"><span data-stu-id="e171f-233">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="e171f-234">包含檔案是設計成用來補充文章其他部分中的內容。</span><span class="sxs-lookup"><span data-stu-id="e171f-234">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

## <a name="links"></a><span data-ttu-id="e171f-235">連結</span><span class="sxs-lookup"><span data-stu-id="e171f-235">Links</span></span>

<span data-ttu-id="e171f-236">如需此連結的語法詳細資訊，請參閱 [在文件中使用連結](how-to-write-links.md)。</span><span class="sxs-lookup"><span data-stu-id="e171f-236">For information on syntax for links, see [Use links in documentation](how-to-write-links.md).</span></span>

## <a name="lists-numbered-bulleted-checklist"></a><span data-ttu-id="e171f-237">清單 (編號、分項、檢查清單)</span><span class="sxs-lookup"><span data-stu-id="e171f-237">Lists (Numbered, Bulleted, Checklist)</span></span>

### <a name="numbered-list"></a><span data-ttu-id="e171f-238">編號清單</span><span class="sxs-lookup"><span data-stu-id="e171f-238">Numbered list</span></span>

<span data-ttu-id="e171f-239">若要建立編號清單，您可以全部使用 1。</span><span class="sxs-lookup"><span data-stu-id="e171f-239">To create a numbered list, you can use all 1s.</span></span> <span data-ttu-id="e171f-240">發佈時，數字會以遞增順序轉譯為連續清單。</span><span class="sxs-lookup"><span data-stu-id="e171f-240">The numbers are rendered in ascending order as a sequential list when published.</span></span> <span data-ttu-id="e171f-241">為了讓來源更方便閱讀，您可以手動遞增清單。</span><span class="sxs-lookup"><span data-stu-id="e171f-241">For increased source readability, you can increment your lists manually.</span></span>

<span data-ttu-id="e171f-242">請不要在清單中使用字母，包括巢狀清單。</span><span class="sxs-lookup"><span data-stu-id="e171f-242">Don't use letters in lists, including nested lists.</span></span> <span data-ttu-id="e171f-243">發佈至 Docs 時，字母無法正確轉譯。如果是使用數字的巢狀清單，系統在發佈時會轉譯為小寫字母。</span><span class="sxs-lookup"><span data-stu-id="e171f-243">They don't render correctly when published to Docs. Nested lists using numbers will render as lowercase letters when published.</span></span> <span data-ttu-id="e171f-244">例如：</span><span class="sxs-lookup"><span data-stu-id="e171f-244">For example:</span></span>

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

<span data-ttu-id="e171f-245">這會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="e171f-245">This renders as follows:</span></span>

1. <span data-ttu-id="e171f-246">This is</span><span class="sxs-lookup"><span data-stu-id="e171f-246">This is</span></span>
1. <span data-ttu-id="e171f-247">a parent numbered list</span><span class="sxs-lookup"><span data-stu-id="e171f-247">a parent numbered list</span></span>
   1. <span data-ttu-id="e171f-248">and this is</span><span class="sxs-lookup"><span data-stu-id="e171f-248">and this is</span></span>
   1. <span data-ttu-id="e171f-249">a nested numbered list</span><span class="sxs-lookup"><span data-stu-id="e171f-249">a nested numbered list</span></span>
1. <span data-ttu-id="e171f-250">(fin)</span><span class="sxs-lookup"><span data-stu-id="e171f-250">(fin)</span></span>

### <a name="bulleted-list"></a><span data-ttu-id="e171f-251">項目符號清單</span><span class="sxs-lookup"><span data-stu-id="e171f-251">Bulleted list</span></span>

<span data-ttu-id="e171f-252">若要建立項目符號清單，請在每行開頭使用 `-` 或 `*` 後接空格：</span><span class="sxs-lookup"><span data-stu-id="e171f-252">To create a bulleted list, use `-` or `*` followed by a space at the beginning of each line:</span></span>

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

<span data-ttu-id="e171f-253">這會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="e171f-253">This renders as follows:</span></span>

- <span data-ttu-id="e171f-254">This is</span><span class="sxs-lookup"><span data-stu-id="e171f-254">This is</span></span>
- <span data-ttu-id="e171f-255">a parent bulleted list</span><span class="sxs-lookup"><span data-stu-id="e171f-255">a parent bulleted list</span></span>
  - <span data-ttu-id="e171f-256">and this is</span><span class="sxs-lookup"><span data-stu-id="e171f-256">and this is</span></span>
  - <span data-ttu-id="e171f-257">a nested bulleted list</span><span class="sxs-lookup"><span data-stu-id="e171f-257">a nested bulleted list</span></span>
- <span data-ttu-id="e171f-258">All done!</span><span class="sxs-lookup"><span data-stu-id="e171f-258">All done!</span></span>

<span data-ttu-id="e171f-259">無論您使用哪種語法，`-` 或 `*`，請在同一篇文章中一致使用它。</span><span class="sxs-lookup"><span data-stu-id="e171f-259">Whichever syntax you use, `-` or `*`, use it consistently within an article.</span></span>

### <a name="checklist"></a><span data-ttu-id="e171f-260">檢查清單</span><span class="sxs-lookup"><span data-stu-id="e171f-260">Checklist</span></span>

<span data-ttu-id="e171f-261">您可透過自訂 Markdown 延伸模組，在 Docs 上使用檢查清單：</span><span class="sxs-lookup"><span data-stu-id="e171f-261">Checklists are available for use on Docs via a custom Markdown extension:</span></span>

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

<span data-ttu-id="e171f-262">此範例在 Docs 上的轉譯如下：</span><span class="sxs-lookup"><span data-stu-id="e171f-262">This example renders on Docs like this:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="e171f-263">List item 1</span><span class="sxs-lookup"><span data-stu-id="e171f-263">List item 1</span></span>
> * <span data-ttu-id="e171f-264">List item 2</span><span class="sxs-lookup"><span data-stu-id="e171f-264">List item 2</span></span>
> * <span data-ttu-id="e171f-265">List item 3</span><span class="sxs-lookup"><span data-stu-id="e171f-265">List item 3</span></span>

<span data-ttu-id="e171f-266">您可在文章的開頭或結尾使用檢查清單，來摘要「您將學到什麼」或「您已學到的內容」。</span><span class="sxs-lookup"><span data-stu-id="e171f-266">Use checklists at the beginning or end of an article to summarize "What will you learn" or "What have you learned" content.</span></span> <span data-ttu-id="e171f-267">請不要在整篇文章中新增隨機檢查清單。</span><span class="sxs-lookup"><span data-stu-id="e171f-267">Do not add random checklists throughout your articles.</span></span>

## <a name="next-step-action"></a><span data-ttu-id="e171f-268">下一步動作</span><span class="sxs-lookup"><span data-stu-id="e171f-268">Next step action</span></span>

<span data-ttu-id="e171f-269">您可使用自訂延伸模組，將 next step (下一步動作) 按鈕新增至 Docs 頁面。</span><span class="sxs-lookup"><span data-stu-id="e171f-269">You can use a custom extension to add a next step action button to Docs pages.</span></span>

<span data-ttu-id="e171f-270">語法如下：</span><span class="sxs-lookup"><span data-stu-id="e171f-270">The syntax is as follows:</span></span>

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

<span data-ttu-id="e171f-271">例如：</span><span class="sxs-lookup"><span data-stu-id="e171f-271">For example:</span></span>

```markdown
> [!div class="nextstepaction"]
> [Learn about adding code to articles](code-in-docs.md)
```

<span data-ttu-id="e171f-272">這會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="e171f-272">This renders as follows:</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="e171f-273">Learn about adding code to articles</span><span class="sxs-lookup"><span data-stu-id="e171f-273">Learn about adding code to articles</span></span>](code-in-docs.md)

<span data-ttu-id="e171f-274">您可以在下一步動作中使用任何支援的連結，包括其他網頁的 Markdown 連結。</span><span class="sxs-lookup"><span data-stu-id="e171f-274">You can use any supported link in a next step action, including a Markdown link to another web page.</span></span> <span data-ttu-id="e171f-275">在大部分情況下，下一步動作連結都是相同文件集中其他檔案的相對連結。</span><span class="sxs-lookup"><span data-stu-id="e171f-275">In most cases, the next action link will be a relative link to another file in the same docset.</span></span>

## <a name="non-localized-strings"></a><span data-ttu-id="e171f-276">不可當地語系化的字串</span><span class="sxs-lookup"><span data-stu-id="e171f-276">Non-localized strings</span></span>

<span data-ttu-id="e171f-277">您可以使用自訂 `no-loc` (不可當地語系化) Markdown 延伸模組，來識別您想要當地語系化過程忽略的內容字串。</span><span class="sxs-lookup"><span data-stu-id="e171f-277">You can use the custom `no-loc` Markdown extension to identify strings of content that you would like the localization process to ignore.</span></span>

<span data-ttu-id="e171f-278">所有被點名的字串都區分大小寫；也就是說，字串必須完全相同，才會被忽略不進行當地語系化。</span><span class="sxs-lookup"><span data-stu-id="e171f-278">All strings called out will be case-sensitive; that is, the string must match exactly to be ignored for localization.</span></span>

<span data-ttu-id="e171f-279">若要將個別字串標記為不可當地語系化，請使用下列語法：</span><span class="sxs-lookup"><span data-stu-id="e171f-279">To mark an individual string as non-localizable, use this syntax:</span></span>

```markdown
:::no-loc text="String":::
```

<span data-ttu-id="e171f-280">例如，在下列範例中，當地語系化過程只會忽略唯一一個 `Document`：</span><span class="sxs-lookup"><span data-stu-id="e171f-280">For example, in the following, only the single instance of `Document` will be ignored during the localization process:</span></span>

```markdown
# Heading 1 of the Document

Markdown content within the :::no-loc text="Document":::.  The are multiple instances of Document, document, and documents.
```

> [!NOTE]
> <span data-ttu-id="e171f-281">使用 `\` 逸出特殊字元：</span><span class="sxs-lookup"><span data-stu-id="e171f-281">Use `\` to escape special characters:</span></span>
> ```markdown
> Lorem :::no-loc text="Find a \"Quotation\""::: Ipsum.
> ```

<span data-ttu-id="e171f-282">您也可以使用 YAML 標頭中的中繼資料，將目前 Markdown 檔案中的所有字串例項標記為不可當地語系化：</span><span class="sxs-lookup"><span data-stu-id="e171f-282">You can also use metadata in the YAML header to mark all instances of a string within the current Markdown file as non-localizable:</span></span>

```yml
author: cillroy
no-loc: [Global, Strings, to be, Ignored]
```

> [!NOTE]
> <span data-ttu-id="e171f-283">docfx.json  檔案中不支援以 no-loc 中繼資料做為全域中繼資料。</span><span class="sxs-lookup"><span data-stu-id="e171f-283">The no-loc metadata is not supported as global metadata in *docfx.json* file.</span></span> <span data-ttu-id="e171f-284">當地語系化管線不會讀取 docfx.json  檔案，因此必須將 non-loc 中繼資料加入每個個別來源檔案。</span><span class="sxs-lookup"><span data-stu-id="e171f-284">The localization pipeline doesn't read the *docfx.json* file, so the no-loc metadata must be added into each individual source file.</span></span>

<span data-ttu-id="e171f-285">在下列範例中，在中繼資料 `title` 中以及在 Markdown 標頭中的 `Document`，都會在當地語系化過程中被忽略。</span><span class="sxs-lookup"><span data-stu-id="e171f-285">In the following example, both in the metadata `title` and the Markdown header the word `Document` will be ignored during the localization process.</span></span>

<span data-ttu-id="e171f-286">在中繼資料 `description` 和 Markdown 主要內容中的 `document` 都會當地語系化，因為它的開頭不是大寫 `D`。</span><span class="sxs-lookup"><span data-stu-id="e171f-286">In the metadata `description` and the Markdown main content the word `document` is localized, because it does not start with a capital `D`.</span></span>

```markdown
---
title: Title of the Document
author: author-name
description: Description for the document
no-loc: [Title, Document]
---
# Heading 1 of the Document

Markdown content within the document.
```

<!-- commenting out for now because no one knows what this means
## Section definition

You might need to define a section. This syntax is mostly used for code tables.
See the following example:

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

The preceding blockquote Markdown text will be rendered as:
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
-->

## <a name="selectors"></a><span data-ttu-id="e171f-287">選取器</span><span class="sxs-lookup"><span data-stu-id="e171f-287">Selectors</span></span>

<span data-ttu-id="e171f-288">selector (選取器) 是使用者介面元素，可讓使用者在同一篇文章的多個類別之間切換。</span><span class="sxs-lookup"><span data-stu-id="e171f-288">Selectors are UI elements that let the user switch between multiple flavors of the same article.</span></span> <span data-ttu-id="e171f-289">某些文件集會使用選取器來解決跨技術或平台的實作差異。</span><span class="sxs-lookup"><span data-stu-id="e171f-289">They are used in some doc sets to address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="e171f-290">一般而言，選取器非常適合開發人員的行動平台內容。</span><span class="sxs-lookup"><span data-stu-id="e171f-290">Selectors are typically most applicable to our mobile platform content for developers.</span></span>

<span data-ttu-id="e171f-291">因為相同的選取器 Markdown 會進入使用 selector 的每個文章檔案，我們建議您將文章的選取器放在 include 檔案中。</span><span class="sxs-lookup"><span data-stu-id="e171f-291">Because the same selector Markdown goes in each article file that uses the selector, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="e171f-292">接著，您可以在您所有使用相同選取器的文章檔案中參考該 include 檔案。</span><span class="sxs-lookup"><span data-stu-id="e171f-292">Then you can reference that include file in all your article files that use the same selector.</span></span>

<span data-ttu-id="e171f-293">目前有兩種選擇器：single selector (單一選取器) 和 multi-selector (多重選取器)。</span><span class="sxs-lookup"><span data-stu-id="e171f-293">There are two types of selectors: a single selector and a multi-selector.</span></span>

### <a name="single-selector"></a><span data-ttu-id="e171f-294">單一選取器</span><span class="sxs-lookup"><span data-stu-id="e171f-294">Single selector</span></span>

```markdown
> [!div class="op_single_selector"]
> - [Universal Windows](../articles/notification-hubs-windows-store-dotnet-get-started/)
> - [Windows Phone](../articles/notification-hubs-windows-phone-get-started/)
> - [iOS](../articles/notification-hubs-ios-get-started/)
> - [Android](../articles/notification-hubs-android-get-started/)
> - [Kindle](../articles/notification-hubs-kindle-get-started/)
> - [Baidu](../articles/notification-hubs-baidu-get-started/)
> - [Xamarin.iOS](../articles/partner-xamarin-notification-hubs-ios-get-started/)
> - [Xamarin.Android](../articles/partner-xamarin-notification-hubs-android-get-started/)
```

<span data-ttu-id="e171f-295">... 轉譯結果如下：</span><span class="sxs-lookup"><span data-stu-id="e171f-295">... will be rendered like this:</span></span>

> [!div class="op_single_selector"]
> - [通用 Windows](how-to-write-links.md)
> - [Windows Phone](how-to-write-links.md)
> - [iOS](how-to-write-links.md)
> - [Android](how-to-write-links.md)
> - [Kindle](how-to-write-links.md)
> - [Baidu](how-to-write-links.md)
> - [Xamarin.iOS](how-to-write-links.md)
> - [Xamarin.Android](how-to-write-links.md)

### <a name="multi-selector"></a><span data-ttu-id="e171f-304">多重選取器</span><span class="sxs-lookup"><span data-stu-id="e171f-304">Multi-selector</span></span>

```markdown
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](./mobile-services-dotnet-backend-ios-get-started-push.md)
> - [(iOS | JavaScript)](./mobile-services-javascript-backend-ios-get-started-push.md)
> - [(Windows universal C# | .NET)](./mobile-services-dotnet-backend-windows-universal-dotnet-get-started-push.md)
> - [(Windows universal C# | Javascript)](./mobile-services-javascript-backend-windows-universal-dotnet-get-started-push.md)
> - [(Windows Phone | .NET)](./mobile-services-dotnet-backend-windows-phone-get-started-push.md)
> - [(Windows Phone | Javascript)](./mobile-services-javascript-backend-windows-phone-get-started-push.md)
> - [(Android | .NET)](./mobile-services-dotnet-backend-android-get-started-push.md)
> - [(Android | Javascript)](./mobile-services-javascript-backend-android-get-started-push.md)
> - [(Xamarin iOS | Javascript)](./partner-xamarin-mobile-services-ios-get-started-push.md)
> - [(Xamarin Android | Javascript)](./partner-xamarin-mobile-services-android-get-started-push.md)
```

<span data-ttu-id="e171f-305">... 轉譯結果如下：</span><span class="sxs-lookup"><span data-stu-id="e171f-305">... will be rendered like this:</span></span>

> [!div class="op_multi_selector" title1="平台" title2="後端"]
> - [(iOS | .NET)](how-to-write-links.md)
> - [(iOS | JavaScript)](how-to-write-links.md)
> - [(Windows 通用 C# | .NET)](how-to-write-links.md)
> - [(Windows 通用 C# | JavaScript)](how-to-write-links.md)
> - [(Windows Phone | .NET)](how-to-write-links.md)
> - [(Windows Phone | JavaScript)](how-to-write-links.md)
> - [(Android | .NET)](how-to-write-links.md)
> - [(Android | JavaScript)](how-to-write-links.md)
> - [(Xamarin iOS | JavaScript)](how-to-write-links.md)
> - [(Xamarin Android | JavaScript)](how-to-write-links.md)

## <a name="subscript-and-superscript"></a><span data-ttu-id="e171f-318">下標和上標</span><span class="sxs-lookup"><span data-stu-id="e171f-318">Subscript and superscript</span></span>

<span data-ttu-id="e171f-319">您應該只在技術正確必需時才使用下標或上標，例如撰寫數學公式時。</span><span class="sxs-lookup"><span data-stu-id="e171f-319">You should only use subscript or superscript when necessary for technical accuracy, such as when writing about mathematical formulas.</span></span> <span data-ttu-id="e171f-320">請勿將它們用於非標準樣式，例如註腳。</span><span class="sxs-lookup"><span data-stu-id="e171f-320">Don't use them for non-standard styles, such as footnotes.</span></span>

<span data-ttu-id="e171f-321">下標和上標樣式請使用 HTML：</span><span class="sxs-lookup"><span data-stu-id="e171f-321">For both subscript and superscript, use HTML:</span></span>

```html
Hello <sub>This is subscript!</sub>
```

<span data-ttu-id="e171f-322">這會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="e171f-322">This renders as follows:</span></span>

<span data-ttu-id="e171f-323">Hello <sub>This is subscript!</sub></span><span class="sxs-lookup"><span data-stu-id="e171f-323">Hello <sub>This is subscript!</sub></span></span>

```html
Goodbye <sup>This is superscript!</sup>
```

<span data-ttu-id="e171f-324">這會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="e171f-324">This renders as follows:</span></span>

<span data-ttu-id="e171f-325">Goodbye <sup>This is superscript!</sup></span><span class="sxs-lookup"><span data-stu-id="e171f-325">Goodbye <sup>This is superscript!</sup></span></span>

## <a name="tables"></a><span data-ttu-id="e171f-326">Tables</span><span class="sxs-lookup"><span data-stu-id="e171f-326">Tables</span></span>

<span data-ttu-id="e171f-327">在 Markdown 中建立表格的最簡單做法是使用直立線符號及線條。</span><span class="sxs-lookup"><span data-stu-id="e171f-327">The simplest way to create a table in Markdown is to use pipes and lines.</span></span> <span data-ttu-id="e171f-328">若要建立含標題的標準表格，請沿著第一個線段與虛線：</span><span class="sxs-lookup"><span data-stu-id="e171f-328">To create a standard table with a header, follow the first line with dashed line:</span></span>

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

<span data-ttu-id="e171f-329">這會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="e171f-329">This renders as follows:</span></span>

|<span data-ttu-id="e171f-330">This is</span><span class="sxs-lookup"><span data-stu-id="e171f-330">This is</span></span>   |<span data-ttu-id="e171f-331">a simple</span><span class="sxs-lookup"><span data-stu-id="e171f-331">a simple</span></span>   |<span data-ttu-id="e171f-332">table header</span><span class="sxs-lookup"><span data-stu-id="e171f-332">table header</span></span>|
|----------|-----------|------------|
|<span data-ttu-id="e171f-333">table</span><span class="sxs-lookup"><span data-stu-id="e171f-333">table</span></span>     |<span data-ttu-id="e171f-334">data</span><span class="sxs-lookup"><span data-stu-id="e171f-334">data</span></span>       |<span data-ttu-id="e171f-335">here</span><span class="sxs-lookup"><span data-stu-id="e171f-335">here</span></span>        |
|<span data-ttu-id="e171f-336">it doesn't</span><span class="sxs-lookup"><span data-stu-id="e171f-336">it doesn't</span></span>|<span data-ttu-id="e171f-337">actually</span><span class="sxs-lookup"><span data-stu-id="e171f-337">actually</span></span>   |<span data-ttu-id="e171f-338">have to line up nicely!</span><span class="sxs-lookup"><span data-stu-id="e171f-338">have to line up nicely!</span></span>||

<span data-ttu-id="e171f-339">您可以使用冒號對齊資料行：</span><span class="sxs-lookup"><span data-stu-id="e171f-339">You can align the columns by using colons:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="e171f-340">轉譯如下：</span><span class="sxs-lookup"><span data-stu-id="e171f-340">Renders as follows:</span></span>

| <span data-ttu-id="e171f-341">Fun</span><span class="sxs-lookup"><span data-stu-id="e171f-341">Fun</span></span>                  | <span data-ttu-id="e171f-342">With</span><span class="sxs-lookup"><span data-stu-id="e171f-342">With</span></span>                 | <span data-ttu-id="e171f-343">Tables</span><span class="sxs-lookup"><span data-stu-id="e171f-343">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="e171f-344">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="e171f-344">left-aligned column</span></span>  | <span data-ttu-id="e171f-345">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="e171f-345">right-aligned column</span></span> | <span data-ttu-id="e171f-346">centered column</span><span class="sxs-lookup"><span data-stu-id="e171f-346">centered column</span></span> |
| <span data-ttu-id="e171f-347">$100</span><span class="sxs-lookup"><span data-stu-id="e171f-347">$100</span></span>                 | <span data-ttu-id="e171f-348">$100</span><span class="sxs-lookup"><span data-stu-id="e171f-348">$100</span></span>                 | <span data-ttu-id="e171f-349">$100</span><span class="sxs-lookup"><span data-stu-id="e171f-349">$100</span></span>            |
| <span data-ttu-id="e171f-350">$10</span><span class="sxs-lookup"><span data-stu-id="e171f-350">$10</span></span>                  | <span data-ttu-id="e171f-351">$10</span><span class="sxs-lookup"><span data-stu-id="e171f-351">$10</span></span>                  | <span data-ttu-id="e171f-352">$10</span><span class="sxs-lookup"><span data-stu-id="e171f-352">$10</span></span>             |
| <span data-ttu-id="e171f-353">$1</span><span class="sxs-lookup"><span data-stu-id="e171f-353">$1</span></span>                   | <span data-ttu-id="e171f-354">$1</span><span class="sxs-lookup"><span data-stu-id="e171f-354">$1</span></span>                   | <span data-ttu-id="e171f-355">$1</span><span class="sxs-lookup"><span data-stu-id="e171f-355">$1</span></span>              |

> [!TIP]
> <span data-ttu-id="e171f-356">適用於 VS Code 的 Docs 編寫延伸模組可讓您輕鬆新增基本 Markdown 表格！</span><span class="sxs-lookup"><span data-stu-id="e171f-356">The Docs Authoring Extension for VS Code makes it easy to add basic Markdown tables!</span></span>
>
> <span data-ttu-id="e171f-357">您也可以使用[線上表格產生器](http://www.tablesgenerator.com/markdown_tables)。</span><span class="sxs-lookup"><span data-stu-id="e171f-357">You can also use an [online table generator](http://www.tablesgenerator.com/markdown_tables).</span></span>

### <a name="line-breaks-within-words-in-any-table-cell"></a><span data-ttu-id="e171f-358">任何表格儲存格中的單字內換行</span><span class="sxs-lookup"><span data-stu-id="e171f-358">Line breaks within words in any table cell</span></span>

<span data-ttu-id="e171f-359">Markdown 表格中的長單字可能會使表格擴展到右側導覽，變得難以閱讀。</span><span class="sxs-lookup"><span data-stu-id="e171f-359">Long words in a Markdown table might make the table expand to the right navigation and become unreadable.</span></span> <span data-ttu-id="e171f-360">您可以允許 Docs 轉譯視需要在單字中自動插入換行，來解決此問題。</span><span class="sxs-lookup"><span data-stu-id="e171f-360">You can solve that by allowing Docs rendering to automatically insert line breaks within words when needed.</span></span> <span data-ttu-id="e171f-361">您只要使用自訂類別 `[!div class="mx-tdBreakAll"]` 加在表格前後即可。</span><span class="sxs-lookup"><span data-stu-id="e171f-361">Just wrap up the table with the custom class `[!div class="mx-tdBreakAll"]`.</span></span>

<span data-ttu-id="e171f-362">以下是具有三列的表格 Markdown 範例，會以類別名稱為 `mx-tdBreakAll` 的 `div` 加在表格前後。</span><span class="sxs-lookup"><span data-stu-id="e171f-362">Here is a Markdown sample of a table with three rows that will be wrapped by a `div` with the class name `mx-tdBreakAll`.</span></span>

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

<span data-ttu-id="e171f-363">轉譯結果如下：</span><span class="sxs-lookup"><span data-stu-id="e171f-363">It will be rendered like this:</span></span>

> [!div class="mx-tdBreakAll"]
> |<span data-ttu-id="e171f-364">Name</span><span class="sxs-lookup"><span data-stu-id="e171f-364">Name</span></span>|<span data-ttu-id="e171f-365">Syntax</span><span class="sxs-lookup"><span data-stu-id="e171f-365">Syntax</span></span>|<span data-ttu-id="e171f-366">Mandatory for silent installation?</span><span class="sxs-lookup"><span data-stu-id="e171f-366">Mandatory for silent installation?</span></span>|<span data-ttu-id="e171f-367">Description</span><span class="sxs-lookup"><span data-stu-id="e171f-367">Description</span></span>|
> |-------------|----------|---------|---------|
> |<span data-ttu-id="e171f-368">Quiet</span><span class="sxs-lookup"><span data-stu-id="e171f-368">Quiet</span></span>|<span data-ttu-id="e171f-369">/quiet</span><span class="sxs-lookup"><span data-stu-id="e171f-369">/quiet</span></span>|<span data-ttu-id="e171f-370">Yes</span><span class="sxs-lookup"><span data-stu-id="e171f-370">Yes</span></span>|<span data-ttu-id="e171f-371">Runs the installer, displaying no UI and no prompts.</span><span class="sxs-lookup"><span data-stu-id="e171f-371">Runs the installer, displaying no UI and no prompts.</span></span>|
> |<span data-ttu-id="e171f-372">NoRestart</span><span class="sxs-lookup"><span data-stu-id="e171f-372">NoRestart</span></span>|<span data-ttu-id="e171f-373">/norestart</span><span class="sxs-lookup"><span data-stu-id="e171f-373">/norestart</span></span>|<span data-ttu-id="e171f-374">No</span><span class="sxs-lookup"><span data-stu-id="e171f-374">No</span></span>|<span data-ttu-id="e171f-375">Suppresses any attempts to restart.</span><span class="sxs-lookup"><span data-stu-id="e171f-375">Suppresses any attempts to restart.</span></span> <span data-ttu-id="e171f-376">By default, the UI will prompt before restart.</span><span class="sxs-lookup"><span data-stu-id="e171f-376">By default, the UI will prompt before restart.</span></span>|
> |<span data-ttu-id="e171f-377">Help</span><span class="sxs-lookup"><span data-stu-id="e171f-377">Help</span></span>|<span data-ttu-id="e171f-378">/help</span><span class="sxs-lookup"><span data-stu-id="e171f-378">/help</span></span>|<span data-ttu-id="e171f-379">No</span><span class="sxs-lookup"><span data-stu-id="e171f-379">No</span></span>|<span data-ttu-id="e171f-380">Provides help and quick reference.</span><span class="sxs-lookup"><span data-stu-id="e171f-380">Provides help and quick reference.</span></span> <span data-ttu-id="e171f-381">Displays the correct use of the setup command, including a list of all options and behaviors.</span><span class="sxs-lookup"><span data-stu-id="e171f-381">Displays the correct use of the setup command, including a list of all options and behaviors.</span></span>|

### <a name="line-breaks-within-words-in-second-column-table-cells"></a><span data-ttu-id="e171f-382">表格第二資料行儲存格中的單字內換行</span><span class="sxs-lookup"><span data-stu-id="e171f-382">Line breaks within words in second column table cells</span></span>

<span data-ttu-id="e171f-383">您可能只想要將換行自動插入表格的第二資料行中的單字內。</span><span class="sxs-lookup"><span data-stu-id="e171f-383">You might want line breaks to be automatically inserted within words only in the second column of a table.</span></span> <span data-ttu-id="e171f-384">若要將換行限於第二資料行，您可以如先前所述，使用 `div` 包裝函式語法來套用 `mx-tdCol2BreakAll` 類別。</span><span class="sxs-lookup"><span data-stu-id="e171f-384">To limit the breaks to the second column, apply the class `mx-tdCol2BreakAll` by using the `div` wrapper syntax as shown earlier.</span></span>

### <a name="data-matrix-tables"></a><span data-ttu-id="e171f-385">資料矩陣表格</span><span class="sxs-lookup"><span data-stu-id="e171f-385">Data matrix tables</span></span>

<span data-ttu-id="e171f-386">資料矩陣表格同時具有標頭與加權第一欄，並在左上方建立具有空白儲存格的矩陣。</span><span class="sxs-lookup"><span data-stu-id="e171f-386">A data matrix table has both a header and a weighted first column, creating a matrix with an empty cell in the top left.</span></span> <span data-ttu-id="e171f-387">Docs 具有資料矩陣表格的自訂 Markdown：</span><span class="sxs-lookup"><span data-stu-id="e171f-387">Docs has custom Markdown for data matrix tables:</span></span>

```md
|                  |Header 1 |Header 2|
|------------------|---------|--------|
|**First column A**|Cell 1A  |Cell 2A |
|**First column B**|Cell 1B  |Cell 2B |
```

<span data-ttu-id="e171f-388">第一欄中的每個項目都必須將樣式設為粗體 (`**bold**`)；否則，這些表格將無法供螢幕助讀程式存取，或不適用於 Docs。</span><span class="sxs-lookup"><span data-stu-id="e171f-388">Every entry in the first column must be styled as bold (`**bold**`); otherwise the tables won't be accessible for screen readers or valid for Docs.</span></span>

### <a name="html-tables"></a><span data-ttu-id="e171f-389">HTML 表格</span><span class="sxs-lookup"><span data-stu-id="e171f-389">HTML Tables</span></span>

<span data-ttu-id="e171f-390">HTML 表格不建議用於 docs.microsoft.com。</span><span class="sxs-lookup"><span data-stu-id="e171f-390">HTML tables aren't recommended for docs.microsoft.com.</span></span> <span data-ttu-id="e171f-391">這類表格不是使用者可看懂的來源，而這與 Markdown 主要準則抵觸。</span><span class="sxs-lookup"><span data-stu-id="e171f-391">They aren't human readable in the source - which is a key principle of Markdown.</span></span>
