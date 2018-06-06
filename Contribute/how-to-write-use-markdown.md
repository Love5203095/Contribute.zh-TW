---
title: 如何使用 Markdown 來撰寫 Docs
description: 本文提供用於撰寫 docs.microsoft.com 文章之 Markdown 語言的基本概念和參考資訊。
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 07/13/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 041398361aef90c44bdf3a0dad4aaa2d40a38289
ms.sourcegitcommit: 782b689882cce3ce07f5613763322989f2d0d63f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/05/2018
ms.locfileid: "34469938"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="ffe49-103">如何使用 Markdown 來撰寫 Docs</span><span class="sxs-lookup"><span data-stu-id="ffe49-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="ffe49-104">Docs.microsoft.com 文章是以稱為 [Markdown](https://daringfireball.net/projects/markdown/) 的輕量型標記語言撰寫，此標記語言容易閱讀及學習。</span><span class="sxs-lookup"><span data-stu-id="ffe49-104">Docs.microsoft.com articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="ffe49-105">基於這個原因，它很快地就成為業界標準。</span><span class="sxs-lookup"><span data-stu-id="ffe49-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="ffe49-106">因為 Docs 的內容是儲存在 GitHub，所以可以使用稱為 [GitHub 版 Markdown (GFM)](https://help.github.com/categories/writing-on-github/) \(英文\) 的 Markdown 超集合，其中針對常見的格式設定需求提供額外支援。</span><span class="sxs-lookup"><span data-stu-id="ffe49-106">Because Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="ffe49-107">此外，開放式發行服務 (OPS) 會實作 Markdig Markdown 剖析器。</span><span class="sxs-lookup"><span data-stu-id="ffe49-107">Additionally, Open Publishing Services (OPS) implements Markdig Markdown Parser.</span></span> <span data-ttu-id="ffe49-108">Markdig 與 GitHub 適用的 Markdown (GFM) 相容程度很高，並新增了功能，而可使用 Docs 專屬功能。</span><span class="sxs-lookup"><span data-stu-id="ffe49-108">Markdig is highly compatible with GitHub Flavored Markdown (GFM), adding functionality to enable Docs-specific features.</span></span>

* <span data-ttu-id="ffe49-109">Markdig 適用於 .NET，是快速、強大、符合 CommonMark 規範的可延伸 Markdown 處理器。</span><span class="sxs-lookup"><span data-stu-id="ffe49-109">Markdig is a fast, powerful, CommonMark compliant, extensible Markdown processor for .NET.</span></span>
* https://github.com/lunet-io/markdig
* <span data-ttu-id="ffe49-110">更佳的社群支援</span><span class="sxs-lookup"><span data-stu-id="ffe49-110">Better community support</span></span>
* <span data-ttu-id="ffe49-111">更佳的標準支援</span><span class="sxs-lookup"><span data-stu-id="ffe49-111">Better standards support</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="ffe49-112">Markdown 基本概念</span><span class="sxs-lookup"><span data-stu-id="ffe49-112">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="ffe49-113">標題</span><span class="sxs-lookup"><span data-stu-id="ffe49-113">Headings</span></span>

<span data-ttu-id="ffe49-114">若要建立標題，您可以使用雜湊記號，如下所示：</span><span class="sxs-lookup"><span data-stu-id="ffe49-114">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
    # This is heading 1
    ## This is heading 2
    ### This is heading 3
    #### This is heading 4
```

### <a name="bold-and-italic-text"></a><span data-ttu-id="ffe49-115">粗體與斜體文字</span><span class="sxs-lookup"><span data-stu-id="ffe49-115">Bold and italic text</span></span>

<span data-ttu-id="ffe49-116">若要將文字格式設定為**粗體**，請使用兩個星號將它括住：</span><span class="sxs-lookup"><span data-stu-id="ffe49-116">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
    This text is **bold**.
```

<span data-ttu-id="ffe49-117">若要將文字格式設定為*斜體*，請使用單一星號將它括住：</span><span class="sxs-lookup"><span data-stu-id="ffe49-117">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
    This text is *italic*.
```

<span data-ttu-id="ffe49-118">若要將文字格式設定為***粗體且斜體***，請使用三個星號將它括住：</span><span class="sxs-lookup"><span data-stu-id="ffe49-118">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
    This is text is both ***bold and italic***.
```

### <a name="lists"></a><span data-ttu-id="ffe49-119">清單</span><span class="sxs-lookup"><span data-stu-id="ffe49-119">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="ffe49-120">未排序清單</span><span class="sxs-lookup"><span data-stu-id="ffe49-120">Unordered list</span></span>

<span data-ttu-id="ffe49-121">若要設定不排序/項目符號清單的格式，請使用星號或短破折號。</span><span class="sxs-lookup"><span data-stu-id="ffe49-121">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="ffe49-122">例如，下列 Markdown：</span><span class="sxs-lookup"><span data-stu-id="ffe49-122">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="ffe49-123">將會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="ffe49-123">will be rendered as:</span></span>

- <span data-ttu-id="ffe49-124">清單項目 1</span><span class="sxs-lookup"><span data-stu-id="ffe49-124">List item 1</span></span>
- <span data-ttu-id="ffe49-125">清單項目 2</span><span class="sxs-lookup"><span data-stu-id="ffe49-125">List item 2</span></span>
- <span data-ttu-id="ffe49-126">清單項目 3</span><span class="sxs-lookup"><span data-stu-id="ffe49-126">List item 3</span></span>

<span data-ttu-id="ffe49-127">若要建立包含在另一個清單中的巢狀清單，請將子清單項目縮排。</span><span class="sxs-lookup"><span data-stu-id="ffe49-127">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="ffe49-128">例如，下列 Markdown：</span><span class="sxs-lookup"><span data-stu-id="ffe49-128">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="ffe49-129">將會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="ffe49-129">will be rendered as:</span></span>

- <span data-ttu-id="ffe49-130">清單項目 1</span><span class="sxs-lookup"><span data-stu-id="ffe49-130">List item 1</span></span>
  - <span data-ttu-id="ffe49-131">清單項目 A</span><span class="sxs-lookup"><span data-stu-id="ffe49-131">List item A</span></span>
  - <span data-ttu-id="ffe49-132">清單項目 B</span><span class="sxs-lookup"><span data-stu-id="ffe49-132">List item B</span></span>
- <span data-ttu-id="ffe49-133">清單項目 2</span><span class="sxs-lookup"><span data-stu-id="ffe49-133">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="ffe49-134">已排序清單</span><span class="sxs-lookup"><span data-stu-id="ffe49-134">Ordered list</span></span>

<span data-ttu-id="ffe49-135">若要設定已排序/逐步清單的格式，請使用對應的數字。</span><span class="sxs-lookup"><span data-stu-id="ffe49-135">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="ffe49-136">例如，下列 Markdown：</span><span class="sxs-lookup"><span data-stu-id="ffe49-136">For example, the following Markdown:</span></span>

```markdown
1. First instruction
2. Second instruction
3. Third instruction
```

<span data-ttu-id="ffe49-137">將會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="ffe49-137">will be rendered as:</span></span>

1. <span data-ttu-id="ffe49-138">第一個指示</span><span class="sxs-lookup"><span data-stu-id="ffe49-138">First instruction</span></span>
2. <span data-ttu-id="ffe49-139">第二個指示</span><span class="sxs-lookup"><span data-stu-id="ffe49-139">Second instruction</span></span>
3. <span data-ttu-id="ffe49-140">第三個指示</span><span class="sxs-lookup"><span data-stu-id="ffe49-140">Third instruction</span></span>

<span data-ttu-id="ffe49-141">若要建立包含在另一個清單中的巢狀清單，請將子清單項目縮排。</span><span class="sxs-lookup"><span data-stu-id="ffe49-141">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="ffe49-142">例如，下列 Markdown：</span><span class="sxs-lookup"><span data-stu-id="ffe49-142">For example, the following Markdown:</span></span>

```markdown
1. First instruction
    1. Sub-instruction
    2. Sub-instruction
2. Second instruction
```

<span data-ttu-id="ffe49-143">將會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="ffe49-143">will be rendered as:</span></span>

1. <span data-ttu-id="ffe49-144">第一個指示</span><span class="sxs-lookup"><span data-stu-id="ffe49-144">First instruction</span></span>
    1. <span data-ttu-id="ffe49-145">子項目指示</span><span class="sxs-lookup"><span data-stu-id="ffe49-145">Sub-instruction</span></span>
    2. <span data-ttu-id="ffe49-146">子項目指示</span><span class="sxs-lookup"><span data-stu-id="ffe49-146">Sub-instruction</span></span>
2. <span data-ttu-id="ffe49-147">第二個指示</span><span class="sxs-lookup"><span data-stu-id="ffe49-147">Second instruction</span></span>

### <a name="tables"></a><span data-ttu-id="ffe49-148">表格</span><span class="sxs-lookup"><span data-stu-id="ffe49-148">Tables</span></span>

<span data-ttu-id="ffe49-149">表格不是核心 Markdown 規格的一部分，但是 GFM 支援表格。</span><span class="sxs-lookup"><span data-stu-id="ffe49-149">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="ffe49-150">您可以使用管線 (|) 和連字號 (-) 字元來建立表格。</span><span class="sxs-lookup"><span data-stu-id="ffe49-150">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="ffe49-151">連字號是用來建立每一欄的標頭，而管線是用來分隔每一欄。</span><span class="sxs-lookup"><span data-stu-id="ffe49-151">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="ffe49-152">請在您的表格之前包含一個空白行，這樣才能正確轉譯。</span><span class="sxs-lookup"><span data-stu-id="ffe49-152">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="ffe49-153">例如，下列 Markdown：</span><span class="sxs-lookup"><span data-stu-id="ffe49-153">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="ffe49-154">將會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="ffe49-154">will be rendered as:</span></span>

| <span data-ttu-id="ffe49-155">好玩</span><span class="sxs-lookup"><span data-stu-id="ffe49-155">Fun</span></span>                  | <span data-ttu-id="ffe49-156">的</span><span class="sxs-lookup"><span data-stu-id="ffe49-156">With</span></span>                 | <span data-ttu-id="ffe49-157">表格</span><span class="sxs-lookup"><span data-stu-id="ffe49-157">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="ffe49-158">靠左對齊欄</span><span class="sxs-lookup"><span data-stu-id="ffe49-158">left-aligned column</span></span>  | <span data-ttu-id="ffe49-159">靠右對齊欄</span><span class="sxs-lookup"><span data-stu-id="ffe49-159">right-aligned column</span></span> | <span data-ttu-id="ffe49-160">置中欄</span><span class="sxs-lookup"><span data-stu-id="ffe49-160">centered column</span></span> |
| <span data-ttu-id="ffe49-161">$100</span><span class="sxs-lookup"><span data-stu-id="ffe49-161">$100</span></span>                 | <span data-ttu-id="ffe49-162">$100</span><span class="sxs-lookup"><span data-stu-id="ffe49-162">$100</span></span>                 | <span data-ttu-id="ffe49-163">$100</span><span class="sxs-lookup"><span data-stu-id="ffe49-163">$100</span></span>            |
| <span data-ttu-id="ffe49-164">$10</span><span class="sxs-lookup"><span data-stu-id="ffe49-164">$10</span></span>                  | <span data-ttu-id="ffe49-165">$10</span><span class="sxs-lookup"><span data-stu-id="ffe49-165">$10</span></span>                  | <span data-ttu-id="ffe49-166">$10</span><span class="sxs-lookup"><span data-stu-id="ffe49-166">$10</span></span>             |
| <span data-ttu-id="ffe49-167">$1</span><span class="sxs-lookup"><span data-stu-id="ffe49-167">$1</span></span>                   | <span data-ttu-id="ffe49-168">$1</span><span class="sxs-lookup"><span data-stu-id="ffe49-168">$1</span></span>                   | <span data-ttu-id="ffe49-169">$1</span><span class="sxs-lookup"><span data-stu-id="ffe49-169">$1</span></span>              |

<span data-ttu-id="ffe49-170">如需有關如何建立表格的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="ffe49-170">For more information on creating tables, see:</span></span>

- <span data-ttu-id="ffe49-171">Markdig [表格內換行功能](#table-wrapping)可協助設定寬表格的格式</span><span class="sxs-lookup"><span data-stu-id="ffe49-171">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables</span></span>
- <span data-ttu-id="ffe49-172">GitHub 的[使用表格組織資訊](https://help.github.com/articles/organizing-information-with-tables/) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="ffe49-172">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/)</span></span>
- <span data-ttu-id="ffe49-173">[Markdown 表格產生器](https://www.tablesgenerator.com/markdown_tables) Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="ffe49-173">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app</span></span>
- <span data-ttu-id="ffe49-174">[Adam Pritchard 的 Markdown 速查表](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="ffe49-174">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)</span></span>
- <span data-ttu-id="ffe49-175">[Michel Fortin 的 Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="ffe49-175">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table)</span></span>
- [<span data-ttu-id="ffe49-176">將 HTML 表格轉換為 Markdown</span><span class="sxs-lookup"><span data-stu-id="ffe49-176">Convert HTML tables to Markdown</span></span>](https://jmalarcon.github.io/markdowntables/)

### <a name="links"></a><span data-ttu-id="ffe49-177">連結</span><span class="sxs-lookup"><span data-stu-id="ffe49-177">Links</span></span>

<span data-ttu-id="ffe49-178">內嵌連結的 Markdown 語法是由超連結文字 `[link text]` 部分，以及緊接在後面的連結 URL 或檔案名稱 `(file-name.md)` 部分所組成：</span><span class="sxs-lookup"><span data-stu-id="ffe49-178">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="ffe49-179">如需連結的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="ffe49-179">For more information on linking, see:</span></span>

- <span data-ttu-id="ffe49-180">[Markdown 語法指南](https://daringfireball.net/projects/markdown/syntax#link) 的 Markdown 基礎連結支援。</span><span class="sxs-lookup"><span data-stu-id="ffe49-180">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="ffe49-181">本指南的[連結](how-to-write-links.md)章節，了解 Markdig 提供的額外連結語法詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ffe49-181">The [Links](how-to-write-links.md) section of this guide for details on additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="ffe49-182">程式碼片段</span><span class="sxs-lookup"><span data-stu-id="ffe49-182">Code snippets</span></span>

<span data-ttu-id="ffe49-183">Markdown 支援將程式碼片段內嵌在句子中，或是在句子之間形成個別圍住的區塊。</span><span class="sxs-lookup"><span data-stu-id="ffe49-183">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="ffe49-184">如需詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="ffe49-184">For details, see:</span></span>

- <span data-ttu-id="ffe49-185">[Markdown 的程式碼區塊原生支援](https://daringfireball.net/projects/markdown/syntax#precode) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="ffe49-185">[Markdown's native support for code blocks](https://daringfireball.net/projects/markdown/syntax#precode)</span></span>
- <span data-ttu-id="ffe49-186">[GFM 對程式碼包圍和語法醒目提示的支援](https://help.github.com/articles/creating-and-highlighting-code-blocks/) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="ffe49-186">[GFM support for code fencing and syntax highlighting](https://help.github.com/articles/creating-and-highlighting-code-blocks/)</span></span>

<span data-ttu-id="ffe49-187">圍住的程式碼區塊是對程式碼片段支援語法醒目提示的簡單方式。</span><span class="sxs-lookup"><span data-stu-id="ffe49-187">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="ffe49-188">圍住的程式碼區塊的一般格式為：</span><span class="sxs-lookup"><span data-stu-id="ffe49-188">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="ffe49-189">前三個倒引號 ('\`') 字元之後的別名定義要使用的語法醒目提示。</span><span class="sxs-lookup"><span data-stu-id="ffe49-189">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="ffe49-190">下列清單是 Docs 內容中常用的程式設計語言與對應的標籤：</span><span class="sxs-lookup"><span data-stu-id="ffe49-190">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="ffe49-191">這些語言包含易記名稱支援，且大部分都具有語言反白顯示。</span><span class="sxs-lookup"><span data-stu-id="ffe49-191">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="ffe49-192">名稱</span><span class="sxs-lookup"><span data-stu-id="ffe49-192">Name</span></span>|<span data-ttu-id="ffe49-193">Markdown 標籤</span><span class="sxs-lookup"><span data-stu-id="ffe49-193">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="ffe49-194">.NET 主控台</span><span class="sxs-lookup"><span data-stu-id="ffe49-194">.NET Console</span></span>|<span data-ttu-id="ffe49-195">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="ffe49-195">dotnetcli</span></span>|
|<span data-ttu-id="ffe49-196">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="ffe49-196">ASP.NET (C#)</span></span>|<span data-ttu-id="ffe49-197">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="ffe49-197">aspx-csharp</span></span>|
|<span data-ttu-id="ffe49-198">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="ffe49-198">ASP.NET (VB)</span></span>|<span data-ttu-id="ffe49-199">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="ffe49-199">aspx-vb</span></span>|
|<span data-ttu-id="ffe49-200">AzCopy</span><span class="sxs-lookup"><span data-stu-id="ffe49-200">AzCopy</span></span>|<span data-ttu-id="ffe49-201">azcopy</span><span class="sxs-lookup"><span data-stu-id="ffe49-201">azcopy</span></span>|
|<span data-ttu-id="ffe49-202">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="ffe49-202">Azure CLI</span></span>|<span data-ttu-id="ffe49-203">azurecli</span><span class="sxs-lookup"><span data-stu-id="ffe49-203">azurecli</span></span>|
|<span data-ttu-id="ffe49-204">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ffe49-204">Azure PowerShell</span></span>|<span data-ttu-id="ffe49-205">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="ffe49-205">azurepowershell</span></span>|
|<span data-ttu-id="ffe49-206">C++</span><span class="sxs-lookup"><span data-stu-id="ffe49-206">C++</span></span>|<span data-ttu-id="ffe49-207">cpp</span><span class="sxs-lookup"><span data-stu-id="ffe49-207">cpp</span></span>|
|<span data-ttu-id="ffe49-208">C++/CX</span><span class="sxs-lookup"><span data-stu-id="ffe49-208">C++/CX</span></span>|<span data-ttu-id="ffe49-209">cppcx</span><span class="sxs-lookup"><span data-stu-id="ffe49-209">cppcx</span></span>|
|<span data-ttu-id="ffe49-210">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="ffe49-210">C++/WinRT</span></span>|<span data-ttu-id="ffe49-211">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="ffe49-211">cppwinrt</span></span>|
|<span data-ttu-id="ffe49-212">C#</span><span class="sxs-lookup"><span data-stu-id="ffe49-212">C#</span></span>|<span data-ttu-id="ffe49-213">csharp</span><span class="sxs-lookup"><span data-stu-id="ffe49-213">csharp</span></span>|
|<span data-ttu-id="ffe49-214">CSHTML</span><span class="sxs-lookup"><span data-stu-id="ffe49-214">CSHTML</span></span>|<span data-ttu-id="ffe49-215">cshtml</span><span class="sxs-lookup"><span data-stu-id="ffe49-215">cshtml</span></span>|
|<span data-ttu-id="ffe49-216">DAX</span><span class="sxs-lookup"><span data-stu-id="ffe49-216">DAX</span></span>|<span data-ttu-id="ffe49-217">dax</span><span class="sxs-lookup"><span data-stu-id="ffe49-217">dax</span></span>|
|<span data-ttu-id="ffe49-218">F#</span><span class="sxs-lookup"><span data-stu-id="ffe49-218">F#</span></span>|<span data-ttu-id="ffe49-219">fsharp</span><span class="sxs-lookup"><span data-stu-id="ffe49-219">fsharp</span></span>|
|<span data-ttu-id="ffe49-220">Go</span><span class="sxs-lookup"><span data-stu-id="ffe49-220">Go</span></span>|<span data-ttu-id="ffe49-221">go</span><span class="sxs-lookup"><span data-stu-id="ffe49-221">go</span></span>|
|<span data-ttu-id="ffe49-222">HTML</span><span class="sxs-lookup"><span data-stu-id="ffe49-222">HTML</span></span>|<span data-ttu-id="ffe49-223">html</span><span class="sxs-lookup"><span data-stu-id="ffe49-223">html</span></span>|
|<span data-ttu-id="ffe49-224">HTTP</span><span class="sxs-lookup"><span data-stu-id="ffe49-224">HTTP</span></span>|<span data-ttu-id="ffe49-225">http</span><span class="sxs-lookup"><span data-stu-id="ffe49-225">http</span></span>|
|<span data-ttu-id="ffe49-226">Java</span><span class="sxs-lookup"><span data-stu-id="ffe49-226">Java</span></span>|<span data-ttu-id="ffe49-227">java</span><span class="sxs-lookup"><span data-stu-id="ffe49-227">java</span></span>|
|<span data-ttu-id="ffe49-228">JavaScript</span><span class="sxs-lookup"><span data-stu-id="ffe49-228">JavaScript</span></span>|<span data-ttu-id="ffe49-229">javascript</span><span class="sxs-lookup"><span data-stu-id="ffe49-229">javascript</span></span>|
|<span data-ttu-id="ffe49-230">JSON</span><span class="sxs-lookup"><span data-stu-id="ffe49-230">JSON</span></span>|<span data-ttu-id="ffe49-231">json</span><span class="sxs-lookup"><span data-stu-id="ffe49-231">json</span></span>|
|<span data-ttu-id="ffe49-232">Markdown</span><span class="sxs-lookup"><span data-stu-id="ffe49-232">Markdown</span></span>|<span data-ttu-id="ffe49-233">md</span><span class="sxs-lookup"><span data-stu-id="ffe49-233">md</span></span>|
|<span data-ttu-id="ffe49-234">NodeJS</span><span class="sxs-lookup"><span data-stu-id="ffe49-234">NodeJS</span></span>|<span data-ttu-id="ffe49-235">nodejs</span><span class="sxs-lookup"><span data-stu-id="ffe49-235">nodejs</span></span>|
|<span data-ttu-id="ffe49-236">Objective-C</span><span class="sxs-lookup"><span data-stu-id="ffe49-236">Objective-C</span></span>|<span data-ttu-id="ffe49-237">objc</span><span class="sxs-lookup"><span data-stu-id="ffe49-237">objc</span></span>|
|<span data-ttu-id="ffe49-238">OData</span><span class="sxs-lookup"><span data-stu-id="ffe49-238">OData</span></span>|<span data-ttu-id="ffe49-239">odata</span><span class="sxs-lookup"><span data-stu-id="ffe49-239">odata</span></span>|
|<span data-ttu-id="ffe49-240">PHP</span><span class="sxs-lookup"><span data-stu-id="ffe49-240">PHP</span></span>|<span data-ttu-id="ffe49-241">php</span><span class="sxs-lookup"><span data-stu-id="ffe49-241">php</span></span>|
|<span data-ttu-id="ffe49-242">Power Apps 公式</span><span class="sxs-lookup"><span data-stu-id="ffe49-242">Power Apps Formula</span></span>|<span data-ttu-id="ffe49-243">powerappsfl</span><span class="sxs-lookup"><span data-stu-id="ffe49-243">powerappsfl</span></span>|
|<span data-ttu-id="ffe49-244">PowerShell</span><span class="sxs-lookup"><span data-stu-id="ffe49-244">PowerShell</span></span>|<span data-ttu-id="ffe49-245">powershell</span><span class="sxs-lookup"><span data-stu-id="ffe49-245">powershell</span></span>|
|<span data-ttu-id="ffe49-246">Python</span><span class="sxs-lookup"><span data-stu-id="ffe49-246">Python</span></span>|<span data-ttu-id="ffe49-247">python</span><span class="sxs-lookup"><span data-stu-id="ffe49-247">python</span></span>|
|<span data-ttu-id="ffe49-248">Q#</span><span class="sxs-lookup"><span data-stu-id="ffe49-248">Q#</span></span>|<span data-ttu-id="ffe49-249">qsharp</span><span class="sxs-lookup"><span data-stu-id="ffe49-249">qsharp</span></span>|
|<span data-ttu-id="ffe49-250">Ruby</span><span class="sxs-lookup"><span data-stu-id="ffe49-250">Ruby</span></span>|<span data-ttu-id="ffe49-251">ruby</span><span class="sxs-lookup"><span data-stu-id="ffe49-251">ruby</span></span>|
|<span data-ttu-id="ffe49-252">SQL</span><span class="sxs-lookup"><span data-stu-id="ffe49-252">SQL</span></span>|<span data-ttu-id="ffe49-253">sql</span><span class="sxs-lookup"><span data-stu-id="ffe49-253">sql</span></span>|
|<span data-ttu-id="ffe49-254">Swift</span><span class="sxs-lookup"><span data-stu-id="ffe49-254">Swift</span></span>|<span data-ttu-id="ffe49-255">swift</span><span class="sxs-lookup"><span data-stu-id="ffe49-255">swift</span></span>|
|<span data-ttu-id="ffe49-256">TypeScript</span><span class="sxs-lookup"><span data-stu-id="ffe49-256">TypeScript</span></span>|<span data-ttu-id="ffe49-257">typescript</span><span class="sxs-lookup"><span data-stu-id="ffe49-257">typescript</span></span>|
|<span data-ttu-id="ffe49-258">VB</span><span class="sxs-lookup"><span data-stu-id="ffe49-258">VB</span></span>|<span data-ttu-id="ffe49-259">vb</span><span class="sxs-lookup"><span data-stu-id="ffe49-259">vb</span></span>|
|<span data-ttu-id="ffe49-260">VSTS CLI</span><span class="sxs-lookup"><span data-stu-id="ffe49-260">VSTS CLI</span></span>|<span data-ttu-id="ffe49-261">vstscli</span><span class="sxs-lookup"><span data-stu-id="ffe49-261">vstscli</span></span>|
|<span data-ttu-id="ffe49-262">XAML</span><span class="sxs-lookup"><span data-stu-id="ffe49-262">XAML</span></span>|<span data-ttu-id="ffe49-263">xaml</span><span class="sxs-lookup"><span data-stu-id="ffe49-263">xaml</span></span>|
|<span data-ttu-id="ffe49-264">XML</span><span class="sxs-lookup"><span data-stu-id="ffe49-264">XML</span></span>|<span data-ttu-id="ffe49-265">xml</span><span class="sxs-lookup"><span data-stu-id="ffe49-265">xml</span></span>|

#### <a name="example-c"></a><span data-ttu-id="ffe49-266">範例：C\#</span><span class="sxs-lookup"><span data-stu-id="ffe49-266">Example: C\#</span></span>

<span data-ttu-id="ffe49-267">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="ffe49-267">__Markdown__</span></span>

    ```csharp
    // Hello1.cs
    public class Hello1
    {
        public static void Main()
        {
            System.Console.WriteLine("Hello, World!");
        }
    }
    ```

<span data-ttu-id="ffe49-268">__轉譯器__</span><span class="sxs-lookup"><span data-stu-id="ffe49-268">__Render__</span></span>

```csharp
// Hello1.cs
public class Hello1
{
    public static void Main()
    {
        System.Console.WriteLine("Hello, World!");
    }
}
```

#### <a name="example-sql"></a><span data-ttu-id="ffe49-269">範例：SQL</span><span class="sxs-lookup"><span data-stu-id="ffe49-269">Example: SQL</span></span>

<span data-ttu-id="ffe49-270">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="ffe49-270">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="ffe49-271">__轉譯器__</span><span class="sxs-lookup"><span data-stu-id="ffe49-271">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="ffe49-272">OPS 自訂 Markdown 擴充功能</span><span class="sxs-lookup"><span data-stu-id="ffe49-272">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="ffe49-273">開放式發行服務 (OPS) 會實作用於 Markdown 的 Markdig 剖析器，這與 GitHub 適用的 Markdown (GFM) 相容程度很高。</span><span class="sxs-lookup"><span data-stu-id="ffe49-273">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="ffe49-274">Markdig 透過 Markdown 擴充新增了一些功能。</span><span class="sxs-lookup"><span data-stu-id="ffe49-274">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="ffe49-275">就真正的意義來說，從完整《OPS 撰寫指南》選取的文章包含在此指南中供參考</span><span class="sxs-lookup"><span data-stu-id="ffe49-275">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="ffe49-276">(例如，請參閱目錄中的＜Markdig 與 Markdown 擴充＞和＜程式碼片段＞)。</span><span class="sxs-lookup"><span data-stu-id="ffe49-276">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="ffe49-277">Docs 文章使用 GFM 來設定大部分的文章格式 (例如段落、連結、清單與標題)。</span><span class="sxs-lookup"><span data-stu-id="ffe49-277">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="ffe49-278">如需更豐富的格式設定，文章可以使用 Markdig 功能，例如：</span><span class="sxs-lookup"><span data-stu-id="ffe49-278">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="ffe49-279">注意事項區塊</span><span class="sxs-lookup"><span data-stu-id="ffe49-279">Note blocks</span></span>
- <span data-ttu-id="ffe49-280">包含</span><span class="sxs-lookup"><span data-stu-id="ffe49-280">Includes</span></span>
- <span data-ttu-id="ffe49-281">選取器</span><span class="sxs-lookup"><span data-stu-id="ffe49-281">Selectors</span></span>
- <span data-ttu-id="ffe49-282">內嵌影片</span><span class="sxs-lookup"><span data-stu-id="ffe49-282">Embedded videos</span></span>
- <span data-ttu-id="ffe49-283">程式碼片段/範例</span><span class="sxs-lookup"><span data-stu-id="ffe49-283">Code snippets/samples</span></span>

<span data-ttu-id="ffe49-284">如需完整清單，請參閱目錄中的＜Markdig 與 Markdown 擴充＞和＜程式碼片段＞。</span><span class="sxs-lookup"><span data-stu-id="ffe49-284">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="ffe49-285">注意事項區塊</span><span class="sxs-lookup"><span data-stu-id="ffe49-285">Note blocks</span></span>

<span data-ttu-id="ffe49-286">有四種類型的注意事項區塊可供您選擇用來強調特定內容：</span><span class="sxs-lookup"><span data-stu-id="ffe49-286">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="ffe49-287">注意</span><span class="sxs-lookup"><span data-stu-id="ffe49-287">NOTE</span></span>
- <span data-ttu-id="ffe49-288">警告</span><span class="sxs-lookup"><span data-stu-id="ffe49-288">WARNING</span></span>
- <span data-ttu-id="ffe49-289">祕訣</span><span class="sxs-lookup"><span data-stu-id="ffe49-289">TIP</span></span>
- <span data-ttu-id="ffe49-290">重要</span><span class="sxs-lookup"><span data-stu-id="ffe49-290">IMPORTANT</span></span>

<span data-ttu-id="ffe49-291">在一般情況下，應該謹慎使用注意事項區塊，因為它們可能會造成干擾。</span><span class="sxs-lookup"><span data-stu-id="ffe49-291">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="ffe49-292">雖然注意事項區塊也支援程式碼區塊、影像、清單和連結，但請盡量讓它們保持簡單明瞭。</span><span class="sxs-lookup"><span data-stu-id="ffe49-292">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

### <a name="includes"></a><span data-ttu-id="ffe49-293">包含</span><span class="sxs-lookup"><span data-stu-id="ffe49-293">Includes</span></span>

<span data-ttu-id="ffe49-294">當您有可重複使用且需要包含在文章檔案中的文字或影像檔時，可以透過 Markdig 檔案的包含功能，使用「包含」檔案的參考。</span><span class="sxs-lookup"><span data-stu-id="ffe49-294">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="ffe49-295">此功能會指示 OPS 在建置階段將指定的檔案包含到文章檔案中，成為發行文章的一部分。</span><span class="sxs-lookup"><span data-stu-id="ffe49-295">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="ffe49-296">有三 種類型的包含可協助您重複使用內容：</span><span class="sxs-lookup"><span data-stu-id="ffe49-296">Three types of includes are available to help you reuse content:</span></span>

- <span data-ttu-id="ffe49-297">內嵌：您在其他句子中內嵌常用的文字片段。</span><span class="sxs-lookup"><span data-stu-id="ffe49-297">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="ffe49-298">區塊：您重複使用整個 Markdown 檔案作為區塊 (巢狀嵌入文章中的小節)。</span><span class="sxs-lookup"><span data-stu-id="ffe49-298">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="ffe49-299">影像： 這是 Docs 中實作標準影像包含的方式。</span><span class="sxs-lookup"><span data-stu-id="ffe49-299">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="ffe49-300">內嵌或區塊包含只是簡單的 Markdown (.md) 檔案。</span><span class="sxs-lookup"><span data-stu-id="ffe49-300">An inline or block include is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="ffe49-301">它可以包含任何有效的 Markdown。</span><span class="sxs-lookup"><span data-stu-id="ffe49-301">It can contain any valid Markdown.</span></span> <span data-ttu-id="ffe49-302">所有的包含 Markdown 檔案都應放在存放庫根目錄中的[一般 `/includes` 子目錄](git-github-fundamentals.md#includes-subdirectory)。</span><span class="sxs-lookup"><span data-stu-id="ffe49-302">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="ffe49-303">當文章發行之後，包含的檔案會直接整合到其中。</span><span class="sxs-lookup"><span data-stu-id="ffe49-303">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="ffe49-304">以下是包含的需求與考量：</span><span class="sxs-lookup"><span data-stu-id="ffe49-304">Here are requirements and considerations for includes:</span></span>

- <span data-ttu-id="ffe49-305">當您需要相同的文字出現在多篇文章中時，就可以使用包含。</span><span class="sxs-lookup"><span data-stu-id="ffe49-305">Use includes whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="ffe49-306">針對大量內容 (例如一兩個段落、共用的程序或共用的節) 使用區塊包含。</span><span class="sxs-lookup"><span data-stu-id="ffe49-306">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="ffe49-307">請勿將它們用在小於一個句子的內容。</span><span class="sxs-lookup"><span data-stu-id="ffe49-307">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="ffe49-308">包含檔案將不會在文章的 GitHub 轉譯檢視中轉譯，因為檔案相依於 Markdig 擴充。</span><span class="sxs-lookup"><span data-stu-id="ffe49-308">Includes won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="ffe49-309">它們將會在發行集之後才轉譯。</span><span class="sxs-lookup"><span data-stu-id="ffe49-309">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="ffe49-310">請務必將包含檔案中的文字撰寫成完整的句子或片語，且不相依於參考包含檔案之文章中的上下文。</span><span class="sxs-lookup"><span data-stu-id="ffe49-310">Ensure that all the text in an include is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="ffe49-311">忽略此指導方針會使文章中產生無法翻譯的字串，進而影響本地化體驗。</span><span class="sxs-lookup"><span data-stu-id="ffe49-311">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="ffe49-312">請勿將包含檔案嵌入到其他包含檔案中。</span><span class="sxs-lookup"><span data-stu-id="ffe49-312">Don't embed includes within other includes.</span></span> <span data-ttu-id="ffe49-313">不支援此使用方式。</span><span class="sxs-lookup"><span data-stu-id="ffe49-313">They are not supported.</span></span>
- <span data-ttu-id="ffe49-314">將媒體檔案放在包含資料夾的特定 [media] 資料夾中，例如 `<repo>`/includes/media 資料夾。</span><span class="sxs-lookup"><span data-stu-id="ffe49-314">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="ffe49-315">[media] 目錄的根目錄中不應包含任何影像。</span><span class="sxs-lookup"><span data-stu-id="ffe49-315">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="ffe49-316">如果包含檔案沒有影像，則不需要對應的 [media] 目錄。</span><span class="sxs-lookup"><span data-stu-id="ffe49-316">If the include does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="ffe49-317">對於一般文章，請勿在不同包含檔案之間共用媒體。</span><span class="sxs-lookup"><span data-stu-id="ffe49-317">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="ffe49-318">請針對每個包含檔案和文章，使用具有唯一名稱的個別檔案。</span><span class="sxs-lookup"><span data-stu-id="ffe49-318">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="ffe49-319">將媒體檔案儲存在與該包含檔案相關聯的 [media] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="ffe49-319">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="ffe49-320">請勿將包含檔案做為文章的唯一內容。</span><span class="sxs-lookup"><span data-stu-id="ffe49-320">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="ffe49-321">包含檔案是設計成用來補充文章其他部分中的內容。</span><span class="sxs-lookup"><span data-stu-id="ffe49-321">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

### <a name="selectors"></a><span data-ttu-id="ffe49-322">選取器</span><span class="sxs-lookup"><span data-stu-id="ffe49-322">Selectors</span></span>

<span data-ttu-id="ffe49-323">當您撰寫同一篇技術文章的不同版本時，可以使用選取器，以滿足跨技術或平台的實作差異。</span><span class="sxs-lookup"><span data-stu-id="ffe49-323">Use selectors in technical articles when you author multiple flavors of the same article, to address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="ffe49-324">一般而言，此功能非常適合開發人員的行動平台內容。</span><span class="sxs-lookup"><span data-stu-id="ffe49-324">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="ffe49-325">Markdig 中目前有兩種不同類型的選取器：單一選取器和多重選取器。</span><span class="sxs-lookup"><span data-stu-id="ffe49-325">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="ffe49-326">因為相同的選擇器 Markdown 會進入選取範圍的每個文章中，我們建議您將文章的選擇器放在包含檔案中。</span><span class="sxs-lookup"><span data-stu-id="ffe49-326">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include.</span></span> <span data-ttu-id="ffe49-327">接著，您可以在您使用相同選擇器的所有文章中參考該包含檔案。</span><span class="sxs-lookup"><span data-stu-id="ffe49-327">Then you can reference that include in all your articles that use the same selector.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="ffe49-328">程式碼片段</span><span class="sxs-lookup"><span data-stu-id="ffe49-328">Code snippets</span></span>

<span data-ttu-id="ffe49-329">Markdig 透過其程式碼片段擴充，支援在文章中包含程式碼的進階方式。</span><span class="sxs-lookup"><span data-stu-id="ffe49-329">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="ffe49-330">它也提供建置在 GFM 功能上的進階轉譯，例如程式設計語言選擇和語法著色，以及各種實用功能，例如：</span><span class="sxs-lookup"><span data-stu-id="ffe49-330">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="ffe49-331">包含來自外部存放庫的集中程式碼範例/片段。</span><span class="sxs-lookup"><span data-stu-id="ffe49-331">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="ffe49-332">可顯示不同語言版本程式碼範例的標籤化 UI。</span><span class="sxs-lookup"><span data-stu-id="ffe49-332">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="ffe49-333">偵錯與疑難排解</span><span class="sxs-lookup"><span data-stu-id="ffe49-333">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="ffe49-334">替代文字</span><span class="sxs-lookup"><span data-stu-id="ffe49-334">Alt text</span></span>

<span data-ttu-id="ffe49-335">將無法正確轉譯包含底線的替泰文字。</span><span class="sxs-lookup"><span data-stu-id="ffe49-335">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="ffe49-336">例如，不要使用此語法︰</span><span class="sxs-lookup"><span data-stu-id="ffe49-336">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="ffe49-337">將底線逸出，如下所示：</span><span class="sxs-lookup"><span data-stu-id="ffe49-337">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="ffe49-338">縮寫符號和雙引號</span><span class="sxs-lookup"><span data-stu-id="ffe49-338">Apostrophes and quotation marks</span></span>

<span data-ttu-id="ffe49-339">如果您將內容從 Word 複製到 Markdown 編輯器中，文字可能會包含「智慧」(彎曲) 縮寫符號或雙引號。</span><span class="sxs-lookup"><span data-stu-id="ffe49-339">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="ffe49-340">這些必須編碼或變更為基本縮寫符號或雙引號。</span><span class="sxs-lookup"><span data-stu-id="ffe49-340">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="ffe49-341">否則檔案發行之後可能會產生這樣的內容：Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="ffe49-341">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="ffe49-342">以下是這些標點符號的「智慧」版本編碼：</span><span class="sxs-lookup"><span data-stu-id="ffe49-342">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="ffe49-343">左 (開頭) 雙引號：`&#8220;`</span><span class="sxs-lookup"><span data-stu-id="ffe49-343">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="ffe49-344">右 (結尾) 雙引號：`&#8221;`</span><span class="sxs-lookup"><span data-stu-id="ffe49-344">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="ffe49-345">右 (結尾) 單引號或縮寫符號：`&#8217;`</span><span class="sxs-lookup"><span data-stu-id="ffe49-345">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="ffe49-346">左 (開頭) 單引號 (很少使用)：`&#8216;`</span><span class="sxs-lookup"><span data-stu-id="ffe49-346">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="ffe49-347">角括號</span><span class="sxs-lookup"><span data-stu-id="ffe49-347">Angle brackets</span></span>

<span data-ttu-id="ffe49-348">如果您在文字 (非程式碼) 中使用角括號 (例如，用來代表預留位置)，則需要手動將角括號編碼。</span><span class="sxs-lookup"><span data-stu-id="ffe49-348">If you use angle brackets in text (not code) in your file--for example, to denote a placeholder--you need to manually encode the angle brackets.</span></span> <span data-ttu-id="ffe49-349">否則 Markdown 會將它們視為 HTML 標籤。</span><span class="sxs-lookup"><span data-stu-id="ffe49-349">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="ffe49-350">例如，將 `<script name>` 編碼成 `&lt;script name&gt;`</span><span class="sxs-lookup"><span data-stu-id="ffe49-350">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="ffe49-351">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ffe49-351">See also</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="ffe49-352">Markdown 資源</span><span class="sxs-lookup"><span data-stu-id="ffe49-352">Markdown resources</span></span>

- <span data-ttu-id="ffe49-353">[Markdown 簡介](https://daringfireball.net/projects/markdown/syntax) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="ffe49-353">[Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax)</span></span>
- [<span data-ttu-id="ffe49-354">Docs Markdown 速查表</span><span class="sxs-lookup"><span data-stu-id="ffe49-354">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- <span data-ttu-id="ffe49-355">[GitHub 的 Markdown 基本概念](https://help.github.com/articles/markdown-basics/) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="ffe49-355">[GitHub's Markdown Basics](https://help.github.com/articles/markdown-basics/)</span></span>
