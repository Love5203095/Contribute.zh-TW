---
title: .NET 文章的範本和速查表
description: 本文包含一個方便的範本，您可以使用該範本為 .NET 文件存放庫建立新文章
ms.date: 11/07/2018
ms.openlocfilehash: e342373a09b623dc71aadd63e8d8627d154ec8b6
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2019
ms.locfileid: "55712916"
---
# <a name="metadata-and-markdown-template-for-net-docs"></a><span data-ttu-id="d0989-103">.NET 文件的中繼資料和 Markdown 範本</span><span class="sxs-lookup"><span data-stu-id="d0989-103">Metadata and Markdown template for .NET docs</span></span>

<span data-ttu-id="d0989-104">此 dotnet/docs 範本包含 Markdown 語法的範例，以及設定中繼資料的指導。</span><span class="sxs-lookup"><span data-stu-id="d0989-104">This dotnet/docs template contains examples of Markdown syntax, as well as guidance on setting the metadata.</span></span>

<span data-ttu-id="d0989-105">當建立 Markdown 檔案時，您應將包含的範本複製到新檔案中、依照如下指定來填寫中繼資料，並將以上 H1 標題設為文章標題。</span><span class="sxs-lookup"><span data-stu-id="d0989-105">When creating a Markdown file, you should copy the included template to a new file, fill out the metadata as specified below, and set the H1 heading above to the title of the article.</span></span>

## <a name="metadata"></a><span data-ttu-id="d0989-106">中繼資料</span><span class="sxs-lookup"><span data-stu-id="d0989-106">Metadata</span></span>

<span data-ttu-id="d0989-107">所需的中繼資料區塊位於下列範例中繼資料區塊中：</span><span class="sxs-lookup"><span data-stu-id="d0989-107">The required metadata block is in the following sample metadata block:</span></span>

```markdown
---
title: [ARTICLE TITLE]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
author: [GITHUB USERNAME]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- <span data-ttu-id="d0989-108">冒號 (:) 和中繼資料項目的值之間**必須**有空格。</span><span class="sxs-lookup"><span data-stu-id="d0989-108">You **must** have a space between the colon (:) and the value for a metadata element.</span></span>
- <span data-ttu-id="d0989-109">值中的冒號 (例如標題) 會中斷中繼資料解析器。</span><span class="sxs-lookup"><span data-stu-id="d0989-109">Colons in a value (for example, a title) break the metadata parser.</span></span> <span data-ttu-id="d0989-110">在此情況下，請使用雙引號來括住標題 (例如 `title: "Writing .NET Core console apps: An advanced step-by-step guide"`)。</span><span class="sxs-lookup"><span data-stu-id="d0989-110">In this case, surround the title with double quotes (for example, `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span></span>
- <span data-ttu-id="d0989-111">**標題**：會出現在搜尋引擎結果中。</span><span class="sxs-lookup"><span data-stu-id="d0989-111">**title**: Appears in search engine results.</span></span> <span data-ttu-id="d0989-112">標題不應與 H1 標題中的標題相同，且不應超過 60 個字元。</span><span class="sxs-lookup"><span data-stu-id="d0989-112">The title shouldn't be identical to the title in your H1 heading, and it should contain 60 characters or less.</span></span>
- <span data-ttu-id="d0989-113">**描述**：會摘要文章的內容。</span><span class="sxs-lookup"><span data-stu-id="d0989-113">**description**: Summarizes the content of the article.</span></span> <span data-ttu-id="d0989-114">通常會顯示於搜尋結果頁面，但不會用於搜尋排名。</span><span class="sxs-lookup"><span data-stu-id="d0989-114">It's usually shown in the search results page, but it isn't used for search ranking.</span></span> <span data-ttu-id="d0989-115">長度應為 115-145 個字元，包括空格。</span><span class="sxs-lookup"><span data-stu-id="d0989-115">Its length should be 115-145 characters including spaces.</span></span>
- <span data-ttu-id="d0989-116">**作者**：作者欄位應包含作者的 **GitHub 使用者名稱**。</span><span class="sxs-lookup"><span data-stu-id="d0989-116">**author**: The author field should contain the **GitHub username** of the author.</span></span>
- <span data-ttu-id="d0989-117">**ms.date**：上次重大更新的日期。</span><span class="sxs-lookup"><span data-stu-id="d0989-117">**ms.date**: The date of the last significant update.</span></span> <span data-ttu-id="d0989-118">如果您已檢閱並更新整篇文章，請在現有文章中對此進行更新。</span><span class="sxs-lookup"><span data-stu-id="d0989-118">Update this on existing articles if you reviewed and updated the entire article.</span></span> <span data-ttu-id="d0989-119">錯字或類似內容的小修正，不保證會更新。</span><span class="sxs-lookup"><span data-stu-id="d0989-119">Small fixes, such as typos or similar do not warrant an update.</span></span>

<span data-ttu-id="d0989-120">其他中繼資料會附加至每篇文章，但我們通常會在資料夾層級套用大多數中繼資料值 (在 **docfx.json** 中指定)。</span><span class="sxs-lookup"><span data-stu-id="d0989-120">Other metadata is attached to each article, but we typically apply most metadata values at the folder level, specified in **docfx.json**.</span></span>

## <a name="basic-markdown-gfm-and-special-characters"></a><span data-ttu-id="d0989-121">基本 Markdown、GFM 和特殊字元</span><span class="sxs-lookup"><span data-stu-id="d0989-121">Basic Markdown, GFM, and special characters</span></span>

<span data-ttu-id="d0989-122">您可以在 [Markdown](how-to-write-use-markdown.md) 和 [Markdown 參考](markdown-reference.md)的一般文章中了解 Markdown、GitHub Flavored Markdown (GFM) 和 OPS 特定延伸模組的基本知識。</span><span class="sxs-lookup"><span data-stu-id="d0989-122">You can learn the basics of Markdown, GitHub Flavored Markdown (GFM), and OPS specific extensions in the general articles on [Markdown](how-to-write-use-markdown.md) and [Markdown reference](markdown-reference.md).</span></span>

<span data-ttu-id="d0989-123">Markdown 使用 \*、\` 和 \# 等特殊字元來格式化。</span><span class="sxs-lookup"><span data-stu-id="d0989-123">Markdown uses special characters such as \*, \`, and \# for formatting.</span></span> <span data-ttu-id="d0989-124">如果您希望將其中一個字元包含在內容中，則必須執行以下兩項作業之一：</span><span class="sxs-lookup"><span data-stu-id="d0989-124">If you wish to include one of these characters in your content, you must do one of two things:</span></span>

- <span data-ttu-id="d0989-125">在特殊字元前加上一個反斜線以將其「逸出」 (例如 `\*` 對於 \*)</span><span class="sxs-lookup"><span data-stu-id="d0989-125">Put a backslash before the special character to "escape" it (for example, `\*` for a \*)</span></span>
- <span data-ttu-id="d0989-126">為字元使用 [HTML 實體程式碼](http://www.ascii.cl/htmlcodes.htm) (例如，`&#42;` 對於 &#42;)。</span><span class="sxs-lookup"><span data-stu-id="d0989-126">Use the [HTML entity code](http://www.ascii.cl/htmlcodes.htm) for the character (for example, `&#42;` for a &#42;).</span></span>

## <a name="file-names"></a><span data-ttu-id="d0989-127">檔案名稱</span><span class="sxs-lookup"><span data-stu-id="d0989-127">File names</span></span>

<span data-ttu-id="d0989-128">檔案名稱使用下列規則：</span><span class="sxs-lookup"><span data-stu-id="d0989-128">File names use the following rules:</span></span>

* <span data-ttu-id="d0989-129">只包含小寫字母、數字和連字號。</span><span class="sxs-lookup"><span data-stu-id="d0989-129">Contain only lowercase letters, numbers, and hyphens.</span></span>
* <span data-ttu-id="d0989-130">沒有空格或標點符號字元。</span><span class="sxs-lookup"><span data-stu-id="d0989-130">No spaces or punctuation characters.</span></span> <span data-ttu-id="d0989-131">檔案名稱中使用連字號來分隔文字和數字。</span><span class="sxs-lookup"><span data-stu-id="d0989-131">Use the hyphens to separate words and numbers in the file name.</span></span>
* <span data-ttu-id="d0989-132">使用特定的動作動詞，例如 develop、buy、build、troubleshoot。</span><span class="sxs-lookup"><span data-stu-id="d0989-132">Use action verbs that are specific, such as develop, buy, build, troubleshoot.</span></span> <span data-ttu-id="d0989-133">沒有 -ing 字詞。</span><span class="sxs-lookup"><span data-stu-id="d0989-133">No -ing words.</span></span>
* <span data-ttu-id="d0989-134">不包含 a、and、the、in、or 等短字。</span><span class="sxs-lookup"><span data-stu-id="d0989-134">No small words - don't include a, and, the, in, or, etc.</span></span>
* <span data-ttu-id="d0989-135">必須是 Markdown 格式且使用 .md 副檔名。</span><span class="sxs-lookup"><span data-stu-id="d0989-135">Must be in Markdown and use the .md file extension.</span></span>
* <span data-ttu-id="d0989-136">保持檔案名稱合理簡短。</span><span class="sxs-lookup"><span data-stu-id="d0989-136">Keep file names reasonably short.</span></span> <span data-ttu-id="d0989-137">它們是您文章 URL 的一部分。</span><span class="sxs-lookup"><span data-stu-id="d0989-137">They are part of the URL for your articles.</span></span>

## <a name="headings"></a><span data-ttu-id="d0989-138">標題</span><span class="sxs-lookup"><span data-stu-id="d0989-138">Headings</span></span>

<span data-ttu-id="d0989-139">使用句型大寫。</span><span class="sxs-lookup"><span data-stu-id="d0989-139">Use sentence-style capitalization.</span></span> <span data-ttu-id="d0989-140">標題的第一個單字一律為大寫。</span><span class="sxs-lookup"><span data-stu-id="d0989-140">Always capitalize the first word of a heading.</span></span>

## <a name="text-styling"></a><span data-ttu-id="d0989-141">文字樣式</span><span class="sxs-lookup"><span data-stu-id="d0989-141">Text styling</span></span>

<span data-ttu-id="d0989-142">*斜體*：用於檔案、資料夾、路徑 (對於長項目，則拆分為其自己的行)、新術語。</span><span class="sxs-lookup"><span data-stu-id="d0989-142">*Italics* Use for files, folders, paths (for long items, split onto their own line), new terms.</span></span>

<span data-ttu-id="d0989-143">**粗體**：用於 UI 項目。</span><span class="sxs-lookup"><span data-stu-id="d0989-143">**Bold** Use for UI elements.</span></span>

<span data-ttu-id="d0989-144">`Code`用於內嵌程式碼、語言關鍵字，NuGet 套件名稱、命令列命令、資料庫資料表和資料列名稱，以及您不希望能點選的 URL。</span><span class="sxs-lookup"><span data-stu-id="d0989-144">`Code` Use for inline code, language keywords, NuGet package names, command-line commands, database table and column names, and URLs that you don't want to be clickable.</span></span>

## <a name="links"></a><span data-ttu-id="d0989-145">連結</span><span class="sxs-lookup"><span data-stu-id="d0989-145">Links</span></span>

<span data-ttu-id="d0989-146">如需錨點、內部連結、其他文件的連結、程式碼包含項目和外部連結的資訊，請參閱[連結](how-to-write-links.md)的一般文章。</span><span class="sxs-lookup"><span data-stu-id="d0989-146">See the general article on [Links](how-to-write-links.md) for information about anchors, internal links, links to other documents, code includes, and external links.</span></span>

<span data-ttu-id="d0989-147">.NET 文件小組使用下列慣例：</span><span class="sxs-lookup"><span data-stu-id="d0989-147">The .NET docs team uses the following conventions:</span></span>

- <span data-ttu-id="d0989-148">在大多數情況下，我們使用相對連結且不建議在連結中使用 `~/`，因為相對連結會在 GitHub 上的來源中解析。</span><span class="sxs-lookup"><span data-stu-id="d0989-148">In most cases, we use the relative links and discourage the use of `~/` in links because relative links resolve in the source on GitHub.</span></span> <span data-ttu-id="d0989-149">但是，每當我們連結到相依存放庫中的檔案時，我們將使用 `~/` 字元來提供路徑。</span><span class="sxs-lookup"><span data-stu-id="d0989-149">However, whenever we link to a file in a dependent repo, we'll use the `~/` character to provide the path.</span></span> <span data-ttu-id="d0989-150">由於相依存放庫中的檔案位於 GitHub 中不同位置，因此無論撰寫方式如何，連結都無法使用相對連結來正確解析。</span><span class="sxs-lookup"><span data-stu-id="d0989-150">Because the files in the dependent repo are in a different location in GitHub the links won't resolve correctly with relative links regardless of how they were written.</span></span>
- <span data-ttu-id="d0989-151">C# 語言規格和 Visual Basic 語言規格包含在 .NET 文件中，包含語言存放庫中的來源。</span><span class="sxs-lookup"><span data-stu-id="d0989-151">The C# language specification and the Visual Basic language specification are included in the .NET docs by including the source from the language repositories.</span></span> <span data-ttu-id="d0989-152">Markdown 來源在 [csharplang](https://github.com/dotnet/csharplang) 和 [vblang](https://github.com/dotnet/vblang) 存放庫中管理。</span><span class="sxs-lookup"><span data-stu-id="d0989-152">The markdown sources are managed in the [csharplang](https://github.com/dotnet/csharplang) and [vblang](https://github.com/dotnet/vblang) repositories.</span></span>

<span data-ttu-id="d0989-153">規格的連結，必須指向包含這些規格的來源目錄。</span><span class="sxs-lookup"><span data-stu-id="d0989-153">Links to the spec must point to the source directories where those specs are included.</span></span> <span data-ttu-id="d0989-154">若為 C#，其為 **~/_csharplang/spec**，若為 VB，則為 **~/_vblang/spec**，如下範例所示：</span><span class="sxs-lookup"><span data-stu-id="d0989-154">For C#, it's **~/_csharplang/spec** and for VB, it's **~/_vblang/spec**, as in the following example:</span></span>

```markdown
[C# Query Expressions](~/_csharplang/spec/expressions.md#query-expressions)
```

### <a name="links-to-apis"></a><span data-ttu-id="d0989-155">API 的連結</span><span class="sxs-lookup"><span data-stu-id="d0989-155">Links to APIs</span></span>

<span data-ttu-id="d0989-156">組建系統具有一些延伸模組，可讓我們連結到 .NET API 而無需使用外部連結。</span><span class="sxs-lookup"><span data-stu-id="d0989-156">The build system has some extensions that allow us to link to .NET APIs without having to use external links.</span></span> <span data-ttu-id="d0989-157">請使用下列語法之一：</span><span class="sxs-lookup"><span data-stu-id="d0989-157">You use one of the following syntax:</span></span>

1. <span data-ttu-id="d0989-158">自動連結：`<xref:UID>` 或 `<xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="d0989-158">Auto-link: `<xref:UID>` or `<xref:UID?displayProperty=nameWithType>`</span></span>

   <span data-ttu-id="d0989-159">`displayProperty` 查詢參數會產生完整的連結文字。</span><span class="sxs-lookup"><span data-stu-id="d0989-159">The `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="d0989-160">根據預設，連結文字只會顯示成員或型別名稱。</span><span class="sxs-lookup"><span data-stu-id="d0989-160">By default, link text shows only the member or type name.</span></span>

2. <span data-ttu-id="d0989-161">Markdown 連結：`[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="d0989-161">Markdown link: `[link text](xref:UID)`</span></span>

   <span data-ttu-id="d0989-162">用於您要自訂顯示的連結文字時。</span><span class="sxs-lookup"><span data-stu-id="d0989-162">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="d0989-163">範例：</span><span class="sxs-lookup"><span data-stu-id="d0989-163">Examples:</span></span>

- <span data-ttu-id="d0989-164">`<xref:System.String>` 會轉譯為 [String](https://docs.microsoft.com/dotnet/api/system.string) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="d0989-164">`<xref:System.String>` renders as [String](https://docs.microsoft.com/dotnet/api/system.string)</span></span>
- <span data-ttu-id="d0989-165">`<xref:System.String?displayProperty=nameWithType>` 會轉譯為 [System.String](https://docs.microsoft.com/dotnet/api/system.string) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="d0989-165">`<xref:System.String?displayProperty=nameWithType>` renders as [System.String](https://docs.microsoft.com/dotnet/api/system.string)</span></span>
- <span data-ttu-id="d0989-166">`[String class](xref:System.String)` 會轉譯為 [String 類別](https://docs.microsoft.com/dotnet/api/system.string) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="d0989-166">`[String class](xref:System.String)` renders as [String class](https://docs.microsoft.com/dotnet/api/system.string)</span></span>

<span data-ttu-id="d0989-167">如需如何使用此標記法的詳細資訊，請參閱[使用交叉參考](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference) \(英文\)。</span><span class="sxs-lookup"><span data-stu-id="d0989-167">For more information about using this notation, see [Using cross reference](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference).</span></span>

<span data-ttu-id="d0989-168">UID 包含特殊字元 \`、\# 或 \*，UID 值必須分別以 HTML 編碼為 `%60`、`%23` 和 `%2A`。</span><span class="sxs-lookup"><span data-stu-id="d0989-168">Some UIDs contain the special characters \`, \# or \*, the UID value needs to be HTML encoded as `%60`, `%23` and `%2A` respectively.</span></span> <span data-ttu-id="d0989-169">有時候您會看到括號也會被編碼，但這並非必要。</span><span class="sxs-lookup"><span data-stu-id="d0989-169">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="d0989-170">範例：</span><span class="sxs-lookup"><span data-stu-id="d0989-170">Examples:</span></span>

- <span data-ttu-id="d0989-171">System.Threading.Tasks.Task\`1 變成 `System.Threading.Tasks.Task%601`</span><span class="sxs-lookup"><span data-stu-id="d0989-171">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="d0989-172">System.Exception.\#ctor 變成 `System.Exception.%23ctor`</span><span class="sxs-lookup"><span data-stu-id="d0989-172">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="d0989-173">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) 變成 `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span><span class="sxs-lookup"><span data-stu-id="d0989-173">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<span data-ttu-id="d0989-174">您可以在 `https://xref.docs.microsoft.com/autocomplete` 中找到類型的 UID、成員多載清單或特定多載成員。</span><span class="sxs-lookup"><span data-stu-id="d0989-174">You can find the UIDs of types, a member overload list, or a particular overloaded member from `https://xref.docs.microsoft.com/autocomplete`.</span></span> <span data-ttu-id="d0989-175">查詢字元字串 `?text=*\<type-member-name>*` 可識別出您要查看其 UID 的類型或成員。</span><span class="sxs-lookup"><span data-stu-id="d0989-175">The query string `?text=*\<type-member-name>*` identifies the type or member whose UIDs you'd like to see.</span></span> <span data-ttu-id="d0989-176">例如，`https://xref.docs.microsoft.com/autocomplete?text=string.format` 會擷取 [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format) 多載。</span><span class="sxs-lookup"><span data-stu-id="d0989-176">For example, `https://xref.docs.microsoft.com/autocomplete?text=string.format` retrieves the [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format) overloads.</span></span> <span data-ttu-id="d0989-177">該工具會在 UID 的任何部分中，搜尋所提供的 `text` 查詢參數。</span><span class="sxs-lookup"><span data-stu-id="d0989-177">The tool searches for the provided `text` query parameter in any part of the UID.</span></span> <span data-ttu-id="d0989-178">例如，您可以搜尋成員名稱 (ToString)、部分成員名稱 (ToStri)、類型和成員名稱 (Double.ToString) 等。</span><span class="sxs-lookup"><span data-stu-id="d0989-178">For example, you can search for member name (ToString), partial member name (ToStri), type and member name (Double.ToString), etc.</span></span>

<span data-ttu-id="d0989-179">如果您在 UID 之後新增 \* (或 `%2A`)，則連結代表多載頁面，而不是特定的 API。</span><span class="sxs-lookup"><span data-stu-id="d0989-179">If you add a \* (or `%2A`) after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="d0989-180">例如，當您想要以一般方法連結到 [List\<T>.BinarySearch Method](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) \(英文\) 頁面，而不是如 [List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_) \(英文\) 的特定多載，就可以使用該方式。</span><span class="sxs-lookup"><span data-stu-id="d0989-180">For example, you can use that when you want to link to the [List\<T>.BinarySearch Method](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) page in a generic way instead of a specific overload such as [List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_).</span></span> <span data-ttu-id="d0989-181">當成員未多載時，您也可以使用 \* 連結到成員頁面；這可讓您無需在 UID 中包含參數清單。</span><span class="sxs-lookup"><span data-stu-id="d0989-181">You can also use \* to link to a member page when the member is not overloaded; this saves you from having to include the parameter list in the UID.</span></span>

<span data-ttu-id="d0989-182">要連結到特定方法多載，必須包含每個方法參數的完整類型名稱。</span><span class="sxs-lookup"><span data-stu-id="d0989-182">To link to a specific method overload, you must include the fully qualified type name of each of the method's parameters.</span></span> <span data-ttu-id="d0989-183">例如，\<xref:System.DateTime.ToString> 會連結到無參數 [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString) 方法，而 \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)> 會連結到 [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_) 方法。</span><span class="sxs-lookup"><span data-stu-id="d0989-183">For example, \<xref:System.DateTime.ToString> links to the parameterless [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString) method, while \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)> links to the  [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_) method.</span></span>

<span data-ttu-id="d0989-184">若要連結到泛型型別，例如 [System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1)，則可以使用 \` (`%60`) 字元，後面接著泛型型別參數的數量。</span><span class="sxs-lookup"><span data-stu-id="d0989-184">To link to a generic type, such as [System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1), you use the \` (`%60`) character followed by the number of generic type parameters.</span></span> <span data-ttu-id="d0989-185">例如，`<xref:System.Nullable%601>` 會連結到 [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1) 類型，而 `<xref:System.Func%602>` 會連結到 [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2) 委派。</span><span class="sxs-lookup"><span data-stu-id="d0989-185">For example, `<xref:System.Nullable%601>` links to the [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1) type, while `<xref:System.Func%602>` links to the [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2) delegate.</span></span>

## <a name="code"></a><span data-ttu-id="d0989-186">程式碼</span><span class="sxs-lookup"><span data-stu-id="d0989-186">Code</span></span>

<span data-ttu-id="d0989-187">包含程式碼的最佳方法，是包含工作範例中的程式碼片段。</span><span class="sxs-lookup"><span data-stu-id="d0989-187">The best way to include code is to include snippets from a working sample.</span></span> <span data-ttu-id="d0989-188">遵循[參與 .NET](dotnet-contribute-process.md#contributing-to-samples) 文章中的指令來建立範例。</span><span class="sxs-lookup"><span data-stu-id="d0989-188">Create your sample following the instructions in the [contributing to .NET](dotnet-contribute-process.md#contributing-to-samples) article.</span></span> <span data-ttu-id="d0989-189">包含程式碼的基本規則，位於[程式碼](how-to-write-use-markdown.md#code-snippets)的一般指導中。</span><span class="sxs-lookup"><span data-stu-id="d0989-189">The basic rules for including code are located in the general guidance on [code](how-to-write-use-markdown.md#code-snippets).</span></span>

<span data-ttu-id="d0989-190">您可以使用下列語法來包含程式碼：</span><span class="sxs-lookup"><span data-stu-id="d0989-190">You can include the code using the following syntax:</span></span>

```markdown
[!code-<language>[<name>](<pathToFile><queryoption><queryoptionvalue>)]
```

* <span data-ttu-id="d0989-191">`-<language>` (「選擇性」，但「建議使用」)</span><span class="sxs-lookup"><span data-stu-id="d0989-191">`-<language>` (*optional* but *recommended*)</span></span>
  * <span data-ttu-id="d0989-192">正在參考之程式碼片段的語言。</span><span class="sxs-lookup"><span data-stu-id="d0989-192">Language of the code snippet being referenced.</span></span> <span data-ttu-id="d0989-193">如需支援值的清單，請參閱[支援的語言](#supported-languages)。</span><span class="sxs-lookup"><span data-stu-id="d0989-193">For a list of supported values, see [Supported languages](#supported-languages).</span></span>

* <span data-ttu-id="d0989-194">`<name>` (選擇性)</span><span class="sxs-lookup"><span data-stu-id="d0989-194">`<name>` (*optional*)</span></span>
  * <span data-ttu-id="d0989-195">程式碼片段的名稱。</span><span class="sxs-lookup"><span data-stu-id="d0989-195">Name for the code snippet.</span></span> <span data-ttu-id="d0989-196">這對輸出 HTML 並沒有任何影響，但您可以用來提高 Markdown 原始碼的可讀性。</span><span class="sxs-lookup"><span data-stu-id="d0989-196">It doesn’t have any impact on the output HTML, but you can use it to improve the readability of your Markdown source.</span></span>

* <span data-ttu-id="d0989-197">`<pathToFile>` (強制)</span><span class="sxs-lookup"><span data-stu-id="d0989-197">`<pathToFile>` (*mandatory*)</span></span>
  * <span data-ttu-id="d0989-198">檔案系統中的相對路徑，表示要參考的程式碼片段檔案。</span><span class="sxs-lookup"><span data-stu-id="d0989-198">Relative path in the file system that indicates the code snippet file to reference.</span></span> <span data-ttu-id="d0989-199">構成 .NET 文件集的不同存放庫可能會使這變得複雜。</span><span class="sxs-lookup"><span data-stu-id="d0989-199">This can be complicated by the different repos that make up the .NET doc set.</span></span> <span data-ttu-id="d0989-200">.NET 範例位於 dotnet/samples 存放庫中。</span><span class="sxs-lookup"><span data-stu-id="d0989-200">The .NET samples are in the dotnet/samples repo.</span></span> <span data-ttu-id="d0989-201">所有程式碼片段路徑都以 `~/samples` 開頭，路徑的其餘部分，來自該存放庫根目錄的來源路徑。</span><span class="sxs-lookup"><span data-stu-id="d0989-201">All snippet paths would start with `~/samples`, the rest of the path being the path to the source from the root of that repo.</span></span>

* <span data-ttu-id="d0989-202">`<queryoption>` (選擇性)</span><span class="sxs-lookup"><span data-stu-id="d0989-202">`<queryoption>` (*optional*)</span></span>
  * <span data-ttu-id="d0989-203">用於指定如何從檔案中擷取程式碼：</span><span class="sxs-lookup"><span data-stu-id="d0989-203">Used to specify how the code should be retrieved from the file:</span></span>
    * <span data-ttu-id="d0989-204">`#`：`#{tagname}` (標籤名稱) 「或」 `#L{startlinenumber}-L{endlinenumber}` (行範圍)。</span><span class="sxs-lookup"><span data-stu-id="d0989-204">`#`:  `#{tagname}` (tag name) *or* `#L{startlinenumber}-L{endlinenumber}` (line range).</span></span>
    <span data-ttu-id="d0989-205">我們不鼓勵使用行號，因為較容易出錯。</span><span class="sxs-lookup"><span data-stu-id="d0989-205">We discourage the use of line numbers because they are very brittle.</span></span> <span data-ttu-id="d0989-206">標籤名稱是參考程式碼片段的首選方式。</span><span class="sxs-lookup"><span data-stu-id="d0989-206">Tag name is the preferred way of referencing code snippets.</span></span> <span data-ttu-id="d0989-207">請使用有意義的標籤名稱。</span><span class="sxs-lookup"><span data-stu-id="d0989-207">Use meaningful tag names.</span></span> <span data-ttu-id="d0989-208">(許多程式碼片段都是從先前的平台遷移過來，且標籤的名稱包含 `Snippet1`、`Snippet2` 等。該做法較難維持。)</span><span class="sxs-lookup"><span data-stu-id="d0989-208">(Many snippets were migrated from a previous platform and the tags have names such as `Snippet1`, `Snippet2` etc. That practice is much harder to maintain.)</span></span>
    * <span data-ttu-id="d0989-209">`range`：`?range=1,3-5`行的範圍。</span><span class="sxs-lookup"><span data-stu-id="d0989-209">`range`: `?range=1,3-5` A range of lines.</span></span> <span data-ttu-id="d0989-210">此範例包含第 1、3、4 及 5 行。</span><span class="sxs-lookup"><span data-stu-id="d0989-210">This example includes lines 1, 3, 4, and 5.</span></span>

<span data-ttu-id="d0989-211">我們建議盡可能使用標籤名稱選項。</span><span class="sxs-lookup"><span data-stu-id="d0989-211">We recommend using the tag name option whenever possible.</span></span> <span data-ttu-id="d0989-212">標籤名稱是區域的名稱，或是以 `Snippettagname` 格式出現在原始程式碼中的程式碼註解名稱。</span><span class="sxs-lookup"><span data-stu-id="d0989-212">The tag name is the name of a region or of a code comment in the format of `Snippettagname` present in the source code.</span></span> <span data-ttu-id="d0989-213">下列範例顯示如何參考標記名稱 `BasicThrow`：</span><span class="sxs-lookup"><span data-stu-id="d0989-213">The following example shows how to refer to the tag name `BasicThrow`:</span></span>

```markdown
[!code-csharp[csrefKeyword#1](~/samples/snippets/snippets/csharp/language-reference/operators/ConditionalExamples.csConditionalRef)]
```

<span data-ttu-id="d0989-214">**dotnet/samples** 中來源的相對路徑會遵循 `~/samples` 路徑。</span><span class="sxs-lookup"><span data-stu-id="d0989-214">The relative path to the source in the **dotnet/samples** repo follows the `~/samples` path.</span></span>

<span data-ttu-id="d0989-215">您可以在[來源檔案](https://github.com/dotnet/samples/blob/master/snippets/csharp/language-reference/operators/ConditionalExamples.cs)中查看程式碼片段標籤的結構。</span><span class="sxs-lookup"><span data-stu-id="d0989-215">And you can see how the snippet tags are structured in [this source file](https://github.com/dotnet/samples/blob/master/snippets/csharp/language-reference/operators/ConditionalExamples.cs).</span></span> <span data-ttu-id="d0989-216">如需程式碼片段原始程式檔中依語言分類的標籤名稱表示法詳細資料，請參閱 [DocFX 指南](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file)。</span><span class="sxs-lookup"><span data-stu-id="d0989-216">For details about tag name representation in code snippet source files by language, see the [DocFX guidelines](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file).</span></span>

<span data-ttu-id="d0989-217">下列範例顯示所有三種 .NET 語言中包含的程式碼：</span><span class="sxs-lookup"><span data-stu-id="d0989-217">The following example shows code included in all three .NET languages:</span></span>

```markdown
[!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/pig-latin.fs#L1-L14)]
 [!code-csharp[ADCreateDomain#2](../../../samples/snippets/csharp/VS_Snippets_CLR/ADCreateDomain/CS/source2.cs#2)]
 [!code-vb[ADCreateDomain#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/ADCreateDomain/VB/source2.vb#2)]  
```

<span data-ttu-id="d0989-218">包含完整程式的程式碼片段，可確保所有程式碼都透過我們的持續整合 (CI) 系統執行。</span><span class="sxs-lookup"><span data-stu-id="d0989-218">Including snippets from full programs ensures that all code runs through our Continuous Integration (CI) system.</span></span> <span data-ttu-id="d0989-219">但是，如果需要顯示導致編譯時間或執行階段錯誤的內容，則可以使用內嵌程式碼區塊。</span><span class="sxs-lookup"><span data-stu-id="d0989-219">However, if you need to show something that causes compile time or runtime errors, you can use inline code blocks.</span></span>

## <a name="images"></a><span data-ttu-id="d0989-220">影像</span><span class="sxs-lookup"><span data-stu-id="d0989-220">Images</span></span>

### <a name="static-image-or-animated-gif"></a><span data-ttu-id="d0989-221">靜態影像或動畫 GIF</span><span class="sxs-lookup"><span data-stu-id="d0989-221">Static image or animated GIF</span></span>

```markdown
![this is the alt text](../images/Logo_DotNet.png)
```

### <a name="linked-image"></a><span data-ttu-id="d0989-222">連結的影像</span><span class="sxs-lookup"><span data-stu-id="d0989-222">Linked image</span></span>

```markdown
[![alt text for linked image](../images/Logo_DotNet.png)](https://dot.net)
```

## <a name="videos"></a><span data-ttu-id="d0989-223">影片</span><span class="sxs-lookup"><span data-stu-id="d0989-223">Videos</span></span>

<span data-ttu-id="d0989-224">目前，您可以使用下列語法嵌入 Channel 9 和 YouTube 影片：</span><span class="sxs-lookup"><span data-stu-id="d0989-224">Currently, you can embed both Channel 9 and YouTube videos with the following syntax:</span></span>

### <a name="channel-9"></a><span data-ttu-id="d0989-225">Channel 9</span><span class="sxs-lookup"><span data-stu-id="d0989-225">Channel 9</span></span>

```markdown
> [!VIDEO <channel9_video_link>]
```

<span data-ttu-id="d0989-226">若要取得影片的正確網址，請選取影片框架下方的 [嵌入] 索引標籤，然後從 `<iframe>` 項目中複製網址。</span><span class="sxs-lookup"><span data-stu-id="d0989-226">To get the video's correct URL, select the **Embed** tab below the video frame, and copy the URL from the `<iframe>` element.</span></span> <span data-ttu-id="d0989-227">例如：</span><span class="sxs-lookup"><span data-stu-id="d0989-227">For example:</span></span>

```markdown
> [!VIDEO https://channel9.msdn.com/Blogs/dotnet/NET-Core-20-Released/player]
```

### <a name="youtube"></a><span data-ttu-id="d0989-228">YouTube</span><span class="sxs-lookup"><span data-stu-id="d0989-228">YouTube</span></span>

<span data-ttu-id="d0989-229">若要取得影片的正確網址，請以右鍵按一下影片，選取 [複製內嵌程式碼]，然後從 `<iframe>` 項目複製網址。</span><span class="sxs-lookup"><span data-stu-id="d0989-229">To get the video's correct URL, right-click on the video, select **Copy Embed Code**, and copy the URL from the `<iframe>` element.</span></span>

```markdown
> [!VIDEO <youtube_video_link>]
```

<span data-ttu-id="d0989-230">例如：</span><span class="sxs-lookup"><span data-stu-id="d0989-230">For example:</span></span>

```markdown
> [!VIDEO https://www.youtube.com/embed/Q2mMbjw6cLA]
```

## <a name="docsmicrosoft-extensions"></a><span data-ttu-id="d0989-231">docs.microsoft 延伸模組</span><span class="sxs-lookup"><span data-stu-id="d0989-231">docs.microsoft extensions</span></span>

<span data-ttu-id="d0989-232">docs.microsoft 為 GitHub Flavored Markdown 提供一些額外的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="d0989-232">docs.microsoft provides a few additional extensions to GitHub Flavored Markdown.</span></span>

### <a name="checked-lists"></a><span data-ttu-id="d0989-233">檢查清單</span><span class="sxs-lookup"><span data-stu-id="d0989-233">Checked lists</span></span>

<span data-ttu-id="d0989-234">自訂樣式適用於清單。</span><span class="sxs-lookup"><span data-stu-id="d0989-234">A custom style is available for lists.</span></span> <span data-ttu-id="d0989-235">您可以轉譯具有綠色核取記號的清單。</span><span class="sxs-lookup"><span data-stu-id="d0989-235">You can render lists with green check marks.</span></span>

```markdown
> [!div class="checklist"]
> * How to create a .NET Core app
> * How to add a reference to the Microsoft.XmlSerializer.Generator package
> * How to edit your MyApp.csproj to add dependencies
> * How to add a class and an XmlSerializer
> * How to build and run the application
```

<span data-ttu-id="d0989-236">這會呈現為：</span><span class="sxs-lookup"><span data-stu-id="d0989-236">This renders as:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="d0989-237">如何建立 .NET Core 應用程式</span><span class="sxs-lookup"><span data-stu-id="d0989-237">How to create a .NET Core app</span></span>
> * <span data-ttu-id="d0989-238">如何將參考新增至 Microsoft.XmlSerializer.Generator 套件</span><span class="sxs-lookup"><span data-stu-id="d0989-238">How to add a reference to the Microsoft.XmlSerializer.Generator package</span></span>
> * <span data-ttu-id="d0989-239">如何編輯您的 MyApp.csproj 以新增相依性</span><span class="sxs-lookup"><span data-stu-id="d0989-239">How to edit your MyApp.csproj to add dependencies</span></span>
> * <span data-ttu-id="d0989-240">如何新增類別和 XmlSerializer</span><span class="sxs-lookup"><span data-stu-id="d0989-240">How to add a class and an XmlSerializer</span></span>
> * <span data-ttu-id="d0989-241">如何建置並執行應用程式</span><span class="sxs-lookup"><span data-stu-id="d0989-241">How to build and run the application</span></span>

<span data-ttu-id="d0989-242">您可以在 [.NET Core 文件](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator)中查看檢查清單的範例。</span><span class="sxs-lookup"><span data-stu-id="d0989-242">You can see an example of checked lists in action in the [.NET Core docs](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator).</span></span>

### <a name="buttons"></a><span data-ttu-id="d0989-243">按鈕</span><span class="sxs-lookup"><span data-stu-id="d0989-243">Buttons</span></span>

<span data-ttu-id="d0989-244">按鈕連結：</span><span class="sxs-lookup"><span data-stu-id="d0989-244">Button links:</span></span>

```markdown
> [!div class="button"]
> [button links](dotnet-contribute.md)
```

<span data-ttu-id="d0989-245">這會呈現為：</span><span class="sxs-lookup"><span data-stu-id="d0989-245">This renders as:</span></span>

> [!div class="button"]
> [<span data-ttu-id="d0989-246">按鈕連結</span><span class="sxs-lookup"><span data-stu-id="d0989-246">button links</span></span>](dotnet-contribute.md)

<span data-ttu-id="d0989-247">您可以在 [Visual Studio 文件](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio)中查看按鈕的範例。</span><span class="sxs-lookup"><span data-stu-id="d0989-247">You can see an example of buttons in action in the [Visual Studio docs](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio).</span></span>

### <a name="step-by-steps"></a><span data-ttu-id="d0989-248">逐步</span><span class="sxs-lookup"><span data-stu-id="d0989-248">Step-by-steps</span></span>

```markdown
>[!div class="step-by-step"]
> [Pre](../docs/csharp/expression-trees-interpreting.md)
> [Next](../docs/csharp/expression-trees-translating.md)
```

<span data-ttu-id="d0989-249">您可以在 [C# 指南](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure)中查看動作中的逐步範例。</span><span class="sxs-lookup"><span data-stu-id="d0989-249">You can see an example of step-by-steps in action at the [C# Guide](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure).</span></span>
