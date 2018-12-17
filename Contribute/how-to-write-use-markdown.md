---
title: 如何使用 Markdown 來撰寫 Docs
description: 本文提供用於撰寫 docs.microsoft.com 文章之 Markdown 語言的基本概念和參考資訊。
ms.date: 07/13/2017
ms.openlocfilehash: 8613d525afc11caf9ec760c4f15ea44010781634
ms.sourcegitcommit: 21c9ac71e1abff946466cddf17a1ee97bc349ec5
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/11/2018
ms.locfileid: "53245887"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="70cb0-103">如何使用 Markdown 來撰寫 Docs</span><span class="sxs-lookup"><span data-stu-id="70cb0-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="70cb0-104">[Docs.microsoft.com](http://docs.microsoft.com) 文章是以稱為 [Markdown](https://daringfireball.net/projects/markdown/) 的輕量型標記語言撰寫，此標記語言容易閱讀及學習。</span><span class="sxs-lookup"><span data-stu-id="70cb0-104">[Docs.microsoft.com](http://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="70cb0-105">基於這個原因，它很快地就成為業界標準。</span><span class="sxs-lookup"><span data-stu-id="70cb0-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="70cb0-106">因為 Docs 內容儲存在 GitHub，所以可以使用稱為 [GitHub 版 Markdown (GFM)](https://help.github.com/categories/writing-on-github/) 的 Markdown 超集合，其中針對常見的格式設定需求提供額外功能。</span><span class="sxs-lookup"><span data-stu-id="70cb0-106">Since Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="70cb0-107">此外，開放式發行服務 (OPS) 會實作 Markdig Markdown 剖析器。</span><span class="sxs-lookup"><span data-stu-id="70cb0-107">Additionally, Open Publishing Services (OPS) implements Markdig Markdown Parser.</span></span> <span data-ttu-id="70cb0-108">Markdig 與 GFM 相容程度很高，並新增功能，而可使用 Docs 專屬功能。</span><span class="sxs-lookup"><span data-stu-id="70cb0-108">Markdig is highly compatible with GFM, adding functionality to enable Docs-specific features.</span></span>

* <span data-ttu-id="70cb0-109">Markdig 適用於 .NET，是快速、強大、符合 CommonMark 規範的可延伸 Markdown 處理器。</span><span class="sxs-lookup"><span data-stu-id="70cb0-109">Markdig is a fast, powerful, CommonMark compliant, extensible Markdown processor for .NET.</span></span>
* https://github.com/lunet-io/markdig
* <span data-ttu-id="70cb0-110">更佳的社群支援</span><span class="sxs-lookup"><span data-stu-id="70cb0-110">Better community support</span></span>
* <span data-ttu-id="70cb0-111">更佳的標準支援</span><span class="sxs-lookup"><span data-stu-id="70cb0-111">Better standards support</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="70cb0-112">Markdown 基本概念</span><span class="sxs-lookup"><span data-stu-id="70cb0-112">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="70cb0-113">標題</span><span class="sxs-lookup"><span data-stu-id="70cb0-113">Headings</span></span>

<span data-ttu-id="70cb0-114">若要建立標題，您可以使用雜湊記號，如下所示：</span><span class="sxs-lookup"><span data-stu-id="70cb0-114">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="70cb0-115">標題應該使用 ATX 樣式，就是在行的開頭使用 1-6 個雜湊字元 (#) 來指出標題，對應於 H1 到 H6 的 HTML標題層級。</span><span class="sxs-lookup"><span data-stu-id="70cb0-115">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="70cb0-116">上述使用了第一到第四級標題的範例。</span><span class="sxs-lookup"><span data-stu-id="70cb0-116">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="70cb0-117">在您的主題中，**必須**只能有一個第一級標題 (H1)，顯示為其頁面上的標題。</span><span class="sxs-lookup"><span data-stu-id="70cb0-117">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="70cb0-118">如果您的標題以 `#` 字元作為結尾，則需要在結尾新增額外的 `#` 字元，以便正確呈現標題。</span><span class="sxs-lookup"><span data-stu-id="70cb0-118">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="70cb0-119">例如，`# Async Programming in F# #`。</span><span class="sxs-lookup"><span data-stu-id="70cb0-119">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="70cb0-120">第二級標題將產生頁面上的 TOC，顯示在頁面標題下方的「本文中」區段中。</span><span class="sxs-lookup"><span data-stu-id="70cb0-120">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="70cb0-121">粗體與斜體文字</span><span class="sxs-lookup"><span data-stu-id="70cb0-121">Bold and italic text</span></span>

<span data-ttu-id="70cb0-122">若要將文字格式設定為**粗體**，請使用兩個星號將它括住：</span><span class="sxs-lookup"><span data-stu-id="70cb0-122">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="70cb0-123">若要將文字格式設定為*斜體*，請使用單一星號將它括住：</span><span class="sxs-lookup"><span data-stu-id="70cb0-123">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="70cb0-124">若要將文字格式設定為***粗體且斜體***，請使用三個星號將它括住：</span><span class="sxs-lookup"><span data-stu-id="70cb0-124">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="70cb0-125">區塊引述</span><span class="sxs-lookup"><span data-stu-id="70cb0-125">Blockquotes</span></span>

<span data-ttu-id="70cb0-126">區塊引述使用 `>` 字元建立：</span><span class="sxs-lookup"><span data-stu-id="70cb0-126">Blockquotes are created using the `>` character:</span></span>

```markdown
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="70cb0-127">前述範例會如下呈現：</span><span class="sxs-lookup"><span data-stu-id="70cb0-127">The preceding example renders as follows:</span></span>

> <span data-ttu-id="70cb0-128">旱災已持續了一千萬年，可怕蜥蜴的統治時期早已結束。</span><span class="sxs-lookup"><span data-stu-id="70cb0-128">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="70cb0-129">此處，在赤道上，在有朝一日稱為非洲的大陸上，生存之戰已來到激烈的最高潮，而勝利者尚未現身。</span><span class="sxs-lookup"><span data-stu-id="70cb0-129">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="70cb0-130">在這片荒蕪乾燥的土地上，只有小型、迅速或兇猛的物體，才能繁榮昌盛，抑或抱有生存下去的希望。</span><span class="sxs-lookup"><span data-stu-id="70cb0-130">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="70cb0-131">清單</span><span class="sxs-lookup"><span data-stu-id="70cb0-131">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="70cb0-132">未排序清單</span><span class="sxs-lookup"><span data-stu-id="70cb0-132">Unordered list</span></span>

<span data-ttu-id="70cb0-133">若要設定不排序/項目符號清單的格式，請使用星號或短破折號。</span><span class="sxs-lookup"><span data-stu-id="70cb0-133">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="70cb0-134">例如，下列 Markdown：</span><span class="sxs-lookup"><span data-stu-id="70cb0-134">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="70cb0-135">將會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="70cb0-135">will be rendered as:</span></span>

- <span data-ttu-id="70cb0-136">清單項目 1</span><span class="sxs-lookup"><span data-stu-id="70cb0-136">List item 1</span></span>
- <span data-ttu-id="70cb0-137">清單項目 2</span><span class="sxs-lookup"><span data-stu-id="70cb0-137">List item 2</span></span>
- <span data-ttu-id="70cb0-138">清單項目 3</span><span class="sxs-lookup"><span data-stu-id="70cb0-138">List item 3</span></span>

<span data-ttu-id="70cb0-139">若要建立包含在另一個清單中的巢狀清單，請將子清單項目縮排。</span><span class="sxs-lookup"><span data-stu-id="70cb0-139">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="70cb0-140">例如，下列 Markdown：</span><span class="sxs-lookup"><span data-stu-id="70cb0-140">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="70cb0-141">將會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="70cb0-141">will be rendered as:</span></span>

- <span data-ttu-id="70cb0-142">清單項目 1</span><span class="sxs-lookup"><span data-stu-id="70cb0-142">List item 1</span></span>
  - <span data-ttu-id="70cb0-143">清單項目 A</span><span class="sxs-lookup"><span data-stu-id="70cb0-143">List item A</span></span>
  - <span data-ttu-id="70cb0-144">清單項目 B</span><span class="sxs-lookup"><span data-stu-id="70cb0-144">List item B</span></span>
- <span data-ttu-id="70cb0-145">清單項目 2</span><span class="sxs-lookup"><span data-stu-id="70cb0-145">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="70cb0-146">已排序清單</span><span class="sxs-lookup"><span data-stu-id="70cb0-146">Ordered list</span></span>

<span data-ttu-id="70cb0-147">若要設定已排序/逐步清單的格式，請使用對應的數字。</span><span class="sxs-lookup"><span data-stu-id="70cb0-147">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="70cb0-148">例如，下列 Markdown：</span><span class="sxs-lookup"><span data-stu-id="70cb0-148">For example, the following Markdown:</span></span>

```markdown
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="70cb0-149">將會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="70cb0-149">will be rendered as:</span></span>

1. <span data-ttu-id="70cb0-150">第一個指示</span><span class="sxs-lookup"><span data-stu-id="70cb0-150">First instruction</span></span>
2. <span data-ttu-id="70cb0-151">第二個指示</span><span class="sxs-lookup"><span data-stu-id="70cb0-151">Second instruction</span></span>
3. <span data-ttu-id="70cb0-152">第三個指示</span><span class="sxs-lookup"><span data-stu-id="70cb0-152">Third instruction</span></span>

<span data-ttu-id="70cb0-153">若要建立包含在另一個清單中的巢狀清單，請將子清單項目縮排。</span><span class="sxs-lookup"><span data-stu-id="70cb0-153">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="70cb0-154">例如，下列 Markdown：</span><span class="sxs-lookup"><span data-stu-id="70cb0-154">For example, the following Markdown:</span></span>

```markdown
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="70cb0-155">將會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="70cb0-155">will be rendered as:</span></span>

1. <span data-ttu-id="70cb0-156">第一個指示</span><span class="sxs-lookup"><span data-stu-id="70cb0-156">First instruction</span></span>
   1. <span data-ttu-id="70cb0-157">子項目指示</span><span class="sxs-lookup"><span data-stu-id="70cb0-157">Sub-instruction</span></span>
   2. <span data-ttu-id="70cb0-158">子項目指示</span><span class="sxs-lookup"><span data-stu-id="70cb0-158">Sub-instruction</span></span>
2. <span data-ttu-id="70cb0-159">第二個指示</span><span class="sxs-lookup"><span data-stu-id="70cb0-159">Second instruction</span></span>

<span data-ttu-id="70cb0-160">請注意，針對所有項目我們</span><span class="sxs-lookup"><span data-stu-id="70cb0-160">Note that we use '1.'</span></span> <span data-ttu-id="70cb0-161">均使用 '1'。</span><span class="sxs-lookup"><span data-stu-id="70cb0-161">for all entries.</span></span> <span data-ttu-id="70cb0-162">這樣，當未來的更新包含新步驟或刪除現有步驟時，就能更輕鬆的檢閱差異。</span><span class="sxs-lookup"><span data-stu-id="70cb0-162">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="70cb0-163">表格</span><span class="sxs-lookup"><span data-stu-id="70cb0-163">Tables</span></span>

<span data-ttu-id="70cb0-164">表格不是核心 Markdown 規格的一部分，但是 GFM 支援表格。</span><span class="sxs-lookup"><span data-stu-id="70cb0-164">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="70cb0-165">您可以使用管線 (|) 和連字號 (-) 字元來建立表格。</span><span class="sxs-lookup"><span data-stu-id="70cb0-165">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="70cb0-166">連字號是用來建立每一欄的標頭，而管線是用來分隔每一欄。</span><span class="sxs-lookup"><span data-stu-id="70cb0-166">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="70cb0-167">請在您的表格之前包含一個空白行，這樣才能正確轉譯。</span><span class="sxs-lookup"><span data-stu-id="70cb0-167">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="70cb0-168">例如，下列 Markdown：</span><span class="sxs-lookup"><span data-stu-id="70cb0-168">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="70cb0-169">將會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="70cb0-169">will be rendered as:</span></span>

| <span data-ttu-id="70cb0-170">好玩</span><span class="sxs-lookup"><span data-stu-id="70cb0-170">Fun</span></span>                  | <span data-ttu-id="70cb0-171">的</span><span class="sxs-lookup"><span data-stu-id="70cb0-171">With</span></span>                 | <span data-ttu-id="70cb0-172">表格</span><span class="sxs-lookup"><span data-stu-id="70cb0-172">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="70cb0-173">靠左對齊欄</span><span class="sxs-lookup"><span data-stu-id="70cb0-173">left-aligned column</span></span>  | <span data-ttu-id="70cb0-174">靠右對齊欄</span><span class="sxs-lookup"><span data-stu-id="70cb0-174">right-aligned column</span></span> | <span data-ttu-id="70cb0-175">置中欄</span><span class="sxs-lookup"><span data-stu-id="70cb0-175">centered column</span></span> |
| <span data-ttu-id="70cb0-176">$100</span><span class="sxs-lookup"><span data-stu-id="70cb0-176">$100</span></span>                 | <span data-ttu-id="70cb0-177">$100</span><span class="sxs-lookup"><span data-stu-id="70cb0-177">$100</span></span>                 | <span data-ttu-id="70cb0-178">$100</span><span class="sxs-lookup"><span data-stu-id="70cb0-178">$100</span></span>            |
| <span data-ttu-id="70cb0-179">$10</span><span class="sxs-lookup"><span data-stu-id="70cb0-179">$10</span></span>                  | <span data-ttu-id="70cb0-180">$10</span><span class="sxs-lookup"><span data-stu-id="70cb0-180">$10</span></span>                  | <span data-ttu-id="70cb0-181">$10</span><span class="sxs-lookup"><span data-stu-id="70cb0-181">$10</span></span>             |
| <span data-ttu-id="70cb0-182">$1</span><span class="sxs-lookup"><span data-stu-id="70cb0-182">$1</span></span>                   | <span data-ttu-id="70cb0-183">$1</span><span class="sxs-lookup"><span data-stu-id="70cb0-183">$1</span></span>                   | <span data-ttu-id="70cb0-184">$1</span><span class="sxs-lookup"><span data-stu-id="70cb0-184">$1</span></span>              |

<span data-ttu-id="70cb0-185">如需有關如何建立表格的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="70cb0-185">For more information on creating tables, see:</span></span>

- <span data-ttu-id="70cb0-186">Markdig [表格內換行功能](#table-wrapping)，可協助設定寬表格的格式。</span><span class="sxs-lookup"><span data-stu-id="70cb0-186">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables.</span></span>
- <span data-ttu-id="70cb0-187">GitHub 的 [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/) (使用表格組織資訊)。</span><span class="sxs-lookup"><span data-stu-id="70cb0-187">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="70cb0-188">[Markdown 表格產生器](https://www.tablesgenerator.com/markdown_tables) Web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="70cb0-188">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="70cb0-189">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables) (Adam Pritchard 的 Markdown 速查表)。</span><span class="sxs-lookup"><span data-stu-id="70cb0-189">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="70cb0-190">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table) (Michel Fortin 的 Markdown Extra)。</span><span class="sxs-lookup"><span data-stu-id="70cb0-190">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="70cb0-191">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/) (將 HTML 表格轉換為 Markdown)。</span><span class="sxs-lookup"><span data-stu-id="70cb0-191">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="70cb0-192">連結</span><span class="sxs-lookup"><span data-stu-id="70cb0-192">Links</span></span>

<span data-ttu-id="70cb0-193">內嵌連結的 Markdown 語法是由超連結文字 `[link text]` 部分，以及緊接在後面的連結 URL 或檔案名稱 `(file-name.md)` 部分所組成：</span><span class="sxs-lookup"><span data-stu-id="70cb0-193">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="70cb0-194">如需連結的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="70cb0-194">For more information on linking, see:</span></span>

- <span data-ttu-id="70cb0-195">[Markdown 語法指南](https://daringfireball.net/projects/markdown/syntax#link) 的 Markdown 基礎連結支援。</span><span class="sxs-lookup"><span data-stu-id="70cb0-195">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="70cb0-196">本指南的[連結](how-to-write-links.md)一節，有 Markdig 提供的額外連結語法詳細資料。</span><span class="sxs-lookup"><span data-stu-id="70cb0-196">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="70cb0-197">程式碼片段</span><span class="sxs-lookup"><span data-stu-id="70cb0-197">Code snippets</span></span>

<span data-ttu-id="70cb0-198">Markdown 支援將程式碼片段內嵌在句子中，或是在句子之間形成個別圍住的區塊。</span><span class="sxs-lookup"><span data-stu-id="70cb0-198">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="70cb0-199">如需詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="70cb0-199">For details, see:</span></span>

- <span data-ttu-id="70cb0-200">[Markdown 的程式碼區塊原生支援](https://daringfireball.net/projects/markdown/syntax#precode) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="70cb0-200">[Markdown's native support for code blocks](https://daringfireball.net/projects/markdown/syntax#precode)</span></span>
- <span data-ttu-id="70cb0-201">[GFM 對程式碼包圍和語法醒目提示的支援](https://help.github.com/articles/creating-and-highlighting-code-blocks/) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="70cb0-201">[GFM support for code fencing and syntax highlighting](https://help.github.com/articles/creating-and-highlighting-code-blocks/)</span></span>

<span data-ttu-id="70cb0-202">圍住的程式碼區塊是對程式碼片段支援語法醒目提示的簡單方式。</span><span class="sxs-lookup"><span data-stu-id="70cb0-202">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="70cb0-203">圍住的程式碼區塊的一般格式為：</span><span class="sxs-lookup"><span data-stu-id="70cb0-203">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="70cb0-204">前三個倒引號 ('\`') 字元之後的別名定義要使用的語法醒目提示。</span><span class="sxs-lookup"><span data-stu-id="70cb0-204">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="70cb0-205">下列清單是 Docs 內容中常用的程式設計語言與對應的標籤：</span><span class="sxs-lookup"><span data-stu-id="70cb0-205">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="70cb0-206">這些語言包含易記名稱支援，且大部分都具有語言反白顯示。</span><span class="sxs-lookup"><span data-stu-id="70cb0-206">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="70cb0-207">名稱</span><span class="sxs-lookup"><span data-stu-id="70cb0-207">Name</span></span>|<span data-ttu-id="70cb0-208">Markdown 標籤</span><span class="sxs-lookup"><span data-stu-id="70cb0-208">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="70cb0-209">.NET 主控台</span><span class="sxs-lookup"><span data-stu-id="70cb0-209">.NET Console</span></span>|<span data-ttu-id="70cb0-210">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="70cb0-210">dotnetcli</span></span>|
|<span data-ttu-id="70cb0-211">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="70cb0-211">ASP.NET (C#)</span></span>|<span data-ttu-id="70cb0-212">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="70cb0-212">aspx-csharp</span></span>|
|<span data-ttu-id="70cb0-213">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="70cb0-213">ASP.NET (VB)</span></span>|<span data-ttu-id="70cb0-214">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="70cb0-214">aspx-vb</span></span>|
|<span data-ttu-id="70cb0-215">AzCopy</span><span class="sxs-lookup"><span data-stu-id="70cb0-215">AzCopy</span></span>|<span data-ttu-id="70cb0-216">azcopy</span><span class="sxs-lookup"><span data-stu-id="70cb0-216">azcopy</span></span>|
|<span data-ttu-id="70cb0-217">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="70cb0-217">Azure CLI</span></span>|<span data-ttu-id="70cb0-218">azurecli</span><span class="sxs-lookup"><span data-stu-id="70cb0-218">azurecli</span></span>|
|<span data-ttu-id="70cb0-219">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="70cb0-219">Azure PowerShell</span></span>|<span data-ttu-id="70cb0-220">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="70cb0-220">azurepowershell</span></span>|
|<span data-ttu-id="70cb0-221">C++</span><span class="sxs-lookup"><span data-stu-id="70cb0-221">C++</span></span>|<span data-ttu-id="70cb0-222">cpp</span><span class="sxs-lookup"><span data-stu-id="70cb0-222">cpp</span></span>|
|<span data-ttu-id="70cb0-223">C++/CX</span><span class="sxs-lookup"><span data-stu-id="70cb0-223">C++/CX</span></span>|<span data-ttu-id="70cb0-224">cppcx</span><span class="sxs-lookup"><span data-stu-id="70cb0-224">cppcx</span></span>|
|<span data-ttu-id="70cb0-225">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="70cb0-225">C++/WinRT</span></span>|<span data-ttu-id="70cb0-226">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="70cb0-226">cppwinrt</span></span>|
|<span data-ttu-id="70cb0-227">C#</span><span class="sxs-lookup"><span data-stu-id="70cb0-227">C#</span></span>|<span data-ttu-id="70cb0-228">csharp</span><span class="sxs-lookup"><span data-stu-id="70cb0-228">csharp</span></span>|
|<span data-ttu-id="70cb0-229">網頁瀏覽器中的 C#</span><span class="sxs-lookup"><span data-stu-id="70cb0-229">C# in browser</span></span>|<span data-ttu-id="70cb0-230">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="70cb0-230">csharp-interactive</span></span>|
|<span data-ttu-id="70cb0-231">主控台</span><span class="sxs-lookup"><span data-stu-id="70cb0-231">Console</span></span>|<span data-ttu-id="70cb0-232">主控台</span><span class="sxs-lookup"><span data-stu-id="70cb0-232">console</span></span>|
|<span data-ttu-id="70cb0-233">CSHTML</span><span class="sxs-lookup"><span data-stu-id="70cb0-233">CSHTML</span></span>|<span data-ttu-id="70cb0-234">cshtml</span><span class="sxs-lookup"><span data-stu-id="70cb0-234">cshtml</span></span>|
|<span data-ttu-id="70cb0-235">DAX</span><span class="sxs-lookup"><span data-stu-id="70cb0-235">DAX</span></span>|<span data-ttu-id="70cb0-236">dax</span><span class="sxs-lookup"><span data-stu-id="70cb0-236">dax</span></span>|
|<span data-ttu-id="70cb0-237">F#</span><span class="sxs-lookup"><span data-stu-id="70cb0-237">F#</span></span>|<span data-ttu-id="70cb0-238">fsharp</span><span class="sxs-lookup"><span data-stu-id="70cb0-238">fsharp</span></span>|
|<span data-ttu-id="70cb0-239">Go</span><span class="sxs-lookup"><span data-stu-id="70cb0-239">Go</span></span>|<span data-ttu-id="70cb0-240">go</span><span class="sxs-lookup"><span data-stu-id="70cb0-240">go</span></span>|
|<span data-ttu-id="70cb0-241">HTML</span><span class="sxs-lookup"><span data-stu-id="70cb0-241">HTML</span></span>|<span data-ttu-id="70cb0-242">html</span><span class="sxs-lookup"><span data-stu-id="70cb0-242">html</span></span>|
|<span data-ttu-id="70cb0-243">HTTP</span><span class="sxs-lookup"><span data-stu-id="70cb0-243">HTTP</span></span>|<span data-ttu-id="70cb0-244">http</span><span class="sxs-lookup"><span data-stu-id="70cb0-244">http</span></span>|
|<span data-ttu-id="70cb0-245">Java</span><span class="sxs-lookup"><span data-stu-id="70cb0-245">Java</span></span>|<span data-ttu-id="70cb0-246">java</span><span class="sxs-lookup"><span data-stu-id="70cb0-246">java</span></span>|
|<span data-ttu-id="70cb0-247">JavaScript</span><span class="sxs-lookup"><span data-stu-id="70cb0-247">JavaScript</span></span>|<span data-ttu-id="70cb0-248">javascript</span><span class="sxs-lookup"><span data-stu-id="70cb0-248">javascript</span></span>|
|<span data-ttu-id="70cb0-249">JSON</span><span class="sxs-lookup"><span data-stu-id="70cb0-249">JSON</span></span>|<span data-ttu-id="70cb0-250">json</span><span class="sxs-lookup"><span data-stu-id="70cb0-250">json</span></span>|
|<span data-ttu-id="70cb0-251">Markdown</span><span class="sxs-lookup"><span data-stu-id="70cb0-251">Markdown</span></span>|<span data-ttu-id="70cb0-252">md</span><span class="sxs-lookup"><span data-stu-id="70cb0-252">md</span></span>|
|<span data-ttu-id="70cb0-253">NodeJS</span><span class="sxs-lookup"><span data-stu-id="70cb0-253">NodeJS</span></span>|<span data-ttu-id="70cb0-254">nodejs</span><span class="sxs-lookup"><span data-stu-id="70cb0-254">nodejs</span></span>|
|<span data-ttu-id="70cb0-255">Objective-C</span><span class="sxs-lookup"><span data-stu-id="70cb0-255">Objective-C</span></span>|<span data-ttu-id="70cb0-256">objc</span><span class="sxs-lookup"><span data-stu-id="70cb0-256">objc</span></span>|
|<span data-ttu-id="70cb0-257">OData</span><span class="sxs-lookup"><span data-stu-id="70cb0-257">OData</span></span>|<span data-ttu-id="70cb0-258">odata</span><span class="sxs-lookup"><span data-stu-id="70cb0-258">odata</span></span>|
|<span data-ttu-id="70cb0-259">PHP</span><span class="sxs-lookup"><span data-stu-id="70cb0-259">PHP</span></span>|<span data-ttu-id="70cb0-260">php</span><span class="sxs-lookup"><span data-stu-id="70cb0-260">php</span></span>|
|<span data-ttu-id="70cb0-261">Power Apps 公式</span><span class="sxs-lookup"><span data-stu-id="70cb0-261">Power Apps Formula</span></span>|<span data-ttu-id="70cb0-262">powerappsfl</span><span class="sxs-lookup"><span data-stu-id="70cb0-262">powerappsfl</span></span>|
|<span data-ttu-id="70cb0-263">PowerShell</span><span class="sxs-lookup"><span data-stu-id="70cb0-263">PowerShell</span></span>|<span data-ttu-id="70cb0-264">powershell</span><span class="sxs-lookup"><span data-stu-id="70cb0-264">powershell</span></span>|
|<span data-ttu-id="70cb0-265">Python</span><span class="sxs-lookup"><span data-stu-id="70cb0-265">Python</span></span>|<span data-ttu-id="70cb0-266">python</span><span class="sxs-lookup"><span data-stu-id="70cb0-266">python</span></span>|
|<span data-ttu-id="70cb0-267">Q#</span><span class="sxs-lookup"><span data-stu-id="70cb0-267">Q#</span></span>|<span data-ttu-id="70cb0-268">qsharp</span><span class="sxs-lookup"><span data-stu-id="70cb0-268">qsharp</span></span>|
|<span data-ttu-id="70cb0-269">R</span><span class="sxs-lookup"><span data-stu-id="70cb0-269">R</span></span>|<span data-ttu-id="70cb0-270">r</span><span class="sxs-lookup"><span data-stu-id="70cb0-270">r</span></span>|
|<span data-ttu-id="70cb0-271">Ruby</span><span class="sxs-lookup"><span data-stu-id="70cb0-271">Ruby</span></span>|<span data-ttu-id="70cb0-272">ruby</span><span class="sxs-lookup"><span data-stu-id="70cb0-272">ruby</span></span>|
|<span data-ttu-id="70cb0-273">SQL</span><span class="sxs-lookup"><span data-stu-id="70cb0-273">SQL</span></span>|<span data-ttu-id="70cb0-274">sql</span><span class="sxs-lookup"><span data-stu-id="70cb0-274">sql</span></span>|
|<span data-ttu-id="70cb0-275">Swift</span><span class="sxs-lookup"><span data-stu-id="70cb0-275">Swift</span></span>|<span data-ttu-id="70cb0-276">swift</span><span class="sxs-lookup"><span data-stu-id="70cb0-276">swift</span></span>|
|<span data-ttu-id="70cb0-277">TypeScript</span><span class="sxs-lookup"><span data-stu-id="70cb0-277">TypeScript</span></span>|<span data-ttu-id="70cb0-278">typescript</span><span class="sxs-lookup"><span data-stu-id="70cb0-278">typescript</span></span>|
|<span data-ttu-id="70cb0-279">VB</span><span class="sxs-lookup"><span data-stu-id="70cb0-279">VB</span></span>|<span data-ttu-id="70cb0-280">vb</span><span class="sxs-lookup"><span data-stu-id="70cb0-280">vb</span></span>|
|<span data-ttu-id="70cb0-281">VSTS CLI</span><span class="sxs-lookup"><span data-stu-id="70cb0-281">VSTS CLI</span></span>|<span data-ttu-id="70cb0-282">vstscli</span><span class="sxs-lookup"><span data-stu-id="70cb0-282">vstscli</span></span>|
|<span data-ttu-id="70cb0-283">XAML</span><span class="sxs-lookup"><span data-stu-id="70cb0-283">XAML</span></span>|<span data-ttu-id="70cb0-284">xaml</span><span class="sxs-lookup"><span data-stu-id="70cb0-284">xaml</span></span>|
|<span data-ttu-id="70cb0-285">XML</span><span class="sxs-lookup"><span data-stu-id="70cb0-285">XML</span></span>|<span data-ttu-id="70cb0-286">xml</span><span class="sxs-lookup"><span data-stu-id="70cb0-286">xml</span></span>|

<span data-ttu-id="70cb0-287">`csharp-interactive` 名稱會指定 C# 語言，並指定在瀏覽器執行範例的能力。</span><span class="sxs-lookup"><span data-stu-id="70cb0-287">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="70cb0-288">這些程式碼片段會在 Docker 容器中編譯和執行，且程式執行的結果會顯示在使用者的瀏覽器視窗中。</span><span class="sxs-lookup"><span data-stu-id="70cb0-288">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="70cb0-289">範例：C\#</span><span class="sxs-lookup"><span data-stu-id="70cb0-289">Example: C\#</span></span>

<span data-ttu-id="70cb0-290">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="70cb0-290">__Markdown__</span></span>

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

<span data-ttu-id="70cb0-291">__轉譯器__</span><span class="sxs-lookup"><span data-stu-id="70cb0-291">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="70cb0-292">範例：SQL</span><span class="sxs-lookup"><span data-stu-id="70cb0-292">Example: SQL</span></span>

<span data-ttu-id="70cb0-293">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="70cb0-293">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="70cb0-294">__轉譯器__</span><span class="sxs-lookup"><span data-stu-id="70cb0-294">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="70cb0-295">OPS 自訂 Markdown 擴充功能</span><span class="sxs-lookup"><span data-stu-id="70cb0-295">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="70cb0-296">開放式發行服務 (OPS) 會實作用於 Markdown 的 Markdig 剖析器，這與 GitHub 適用的 Markdown (GFM) 相容程度很高。</span><span class="sxs-lookup"><span data-stu-id="70cb0-296">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="70cb0-297">Markdig 透過 Markdown 擴充新增了一些功能。</span><span class="sxs-lookup"><span data-stu-id="70cb0-297">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="70cb0-298">就真正的意義來說，從完整《OPS 撰寫指南》選取的文章包含在此指南中供參考</span><span class="sxs-lookup"><span data-stu-id="70cb0-298">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="70cb0-299">(例如，請參閱目錄中的＜Markdig 與 Markdown 擴充＞和＜程式碼片段＞)。</span><span class="sxs-lookup"><span data-stu-id="70cb0-299">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="70cb0-300">Docs 文章使用 GFM 來設定大部分的文章格式 (例如段落、連結、清單與標題)。</span><span class="sxs-lookup"><span data-stu-id="70cb0-300">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="70cb0-301">如需更豐富的格式設定，文章可以使用 Markdig 功能，例如：</span><span class="sxs-lookup"><span data-stu-id="70cb0-301">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="70cb0-302">注意事項區塊</span><span class="sxs-lookup"><span data-stu-id="70cb0-302">Note blocks</span></span>
- <span data-ttu-id="70cb0-303">Include 檔案</span><span class="sxs-lookup"><span data-stu-id="70cb0-303">Include files</span></span>
- <span data-ttu-id="70cb0-304">選取器</span><span class="sxs-lookup"><span data-stu-id="70cb0-304">Selectors</span></span>
- <span data-ttu-id="70cb0-305">內嵌影片</span><span class="sxs-lookup"><span data-stu-id="70cb0-305">Embedded videos</span></span>
- <span data-ttu-id="70cb0-306">程式碼片段/範例</span><span class="sxs-lookup"><span data-stu-id="70cb0-306">Code snippets/samples</span></span>

<span data-ttu-id="70cb0-307">如需完整清單，請參閱目錄中的＜Markdig 與 Markdown 擴充＞和＜程式碼片段＞。</span><span class="sxs-lookup"><span data-stu-id="70cb0-307">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="70cb0-308">注意事項區塊</span><span class="sxs-lookup"><span data-stu-id="70cb0-308">Note blocks</span></span>

<span data-ttu-id="70cb0-309">有四種類型的注意事項區塊可供您選擇用來強調特定內容：</span><span class="sxs-lookup"><span data-stu-id="70cb0-309">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="70cb0-310">注意</span><span class="sxs-lookup"><span data-stu-id="70cb0-310">NOTE</span></span>
- <span data-ttu-id="70cb0-311">警告</span><span class="sxs-lookup"><span data-stu-id="70cb0-311">WARNING</span></span>
- <span data-ttu-id="70cb0-312">祕訣</span><span class="sxs-lookup"><span data-stu-id="70cb0-312">TIP</span></span>
- <span data-ttu-id="70cb0-313">重要</span><span class="sxs-lookup"><span data-stu-id="70cb0-313">IMPORTANT</span></span>

<span data-ttu-id="70cb0-314">在一般情況下，應該謹慎使用注意事項區塊，因為它們可能會造成干擾。</span><span class="sxs-lookup"><span data-stu-id="70cb0-314">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="70cb0-315">雖然注意事項區塊也支援程式碼區塊、影像、清單和連結，但請盡量讓它們保持簡單明瞭。</span><span class="sxs-lookup"><span data-stu-id="70cb0-315">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="70cb0-316">範例：</span><span class="sxs-lookup"><span data-stu-id="70cb0-316">Examples:</span></span>

```markdown
> [!NOTE]
> This is a NOTE

> [!WARNING]
> This is a WARNING

> [!TIP]
> This is a TIP

> [!IMPORTANT]
> This is IMPORTANT
```

<span data-ttu-id="70cb0-317">這些會如下呈現：</span><span class="sxs-lookup"><span data-stu-id="70cb0-317">These render as follows:</span></span>

> [!NOTE]
> <span data-ttu-id="70cb0-318">這是「附註」</span><span class="sxs-lookup"><span data-stu-id="70cb0-318">This is a NOTE</span></span>

> [!WARNING]
> <span data-ttu-id="70cb0-319">這是「警告」</span><span class="sxs-lookup"><span data-stu-id="70cb0-319">This is a WARNING</span></span>

> [!TIP]
> <span data-ttu-id="70cb0-320">這是「提示」</span><span class="sxs-lookup"><span data-stu-id="70cb0-320">This is a TIP</span></span>

> [!IMPORTANT]
> <span data-ttu-id="70cb0-321">這是「重要」</span><span class="sxs-lookup"><span data-stu-id="70cb0-321">This is IMPORTANT</span></span>

### <a name="include-files"></a><span data-ttu-id="70cb0-322">Include 檔案</span><span class="sxs-lookup"><span data-stu-id="70cb0-322">Include files</span></span>

<span data-ttu-id="70cb0-323">當您有可重複使用且需要包含在文章檔案中的文字或影像檔時，可以透過 Markdig 檔案的包含功能，使用「包含」檔案的參考。</span><span class="sxs-lookup"><span data-stu-id="70cb0-323">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="70cb0-324">此功能會指示 OPS 在建置階段將指定的檔案包含到文章檔案中，成為發行文章的一部分。</span><span class="sxs-lookup"><span data-stu-id="70cb0-324">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="70cb0-325">有三種類型的 Include 參考可協助您重複使用內容：</span><span class="sxs-lookup"><span data-stu-id="70cb0-325">Three types of include references are available to help you reuse content:</span></span>

- <span data-ttu-id="70cb0-326">內嵌：在另一個句子中重複使用常用程式碼片段內嵌。</span><span class="sxs-lookup"><span data-stu-id="70cb0-326">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="70cb0-327">區塊：您重複使用整個 Markdown 檔案作為區塊 (巢狀嵌入文章中的小節)。</span><span class="sxs-lookup"><span data-stu-id="70cb0-327">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="70cb0-328">影像：這是 Docs 中實作標準影像包含的方式。</span><span class="sxs-lookup"><span data-stu-id="70cb0-328">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="70cb0-329">內嵌或區塊 Include 檔案都只是簡單的 Markdown (.md) 檔案。</span><span class="sxs-lookup"><span data-stu-id="70cb0-329">An inline or block include file is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="70cb0-330">它可以包含任何有效的 Markdown。</span><span class="sxs-lookup"><span data-stu-id="70cb0-330">It can contain any valid Markdown.</span></span> <span data-ttu-id="70cb0-331">所有的包含 Markdown 檔案都應放在存放庫根目錄中的[一般 `/includes` 子目錄](git-github-fundamentals.md#includes-subdirectory)。</span><span class="sxs-lookup"><span data-stu-id="70cb0-331">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="70cb0-332">當文章發行之後，包含的檔案會直接整合到其中。</span><span class="sxs-lookup"><span data-stu-id="70cb0-332">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="70cb0-333">以下是 Include 檔案的需求與考量：</span><span class="sxs-lookup"><span data-stu-id="70cb0-333">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="70cb0-334">當您需要相同的文字出現在多篇文章中時，就可以使用 Include 檔案。</span><span class="sxs-lookup"><span data-stu-id="70cb0-334">Use an include file whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="70cb0-335">針對大量內容 (例如一兩個段落、共用的程序或共用的節) 使用區塊 Include 參考。</span><span class="sxs-lookup"><span data-stu-id="70cb0-335">Use a block include reference for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="70cb0-336">請勿將它們用在小於一個句子的內容。</span><span class="sxs-lookup"><span data-stu-id="70cb0-336">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="70cb0-337">因為檔案相依於 Markdig 延伸，所以不會在文章的 GitHub 轉譯檢視中轉譯 Include 參考。</span><span class="sxs-lookup"><span data-stu-id="70cb0-337">Include references won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="70cb0-338">它們將會在發行集之後才轉譯。</span><span class="sxs-lookup"><span data-stu-id="70cb0-338">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="70cb0-339">請務必將 Include 檔案中的文字撰寫成完整的句子或片語，且不相依於參考 Include 檔案之文章中的上下文。</span><span class="sxs-lookup"><span data-stu-id="70cb0-339">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include file.</span></span> <span data-ttu-id="70cb0-340">忽略此指導方針會使文章中產生無法翻譯的字串，進而影響本地化體驗。</span><span class="sxs-lookup"><span data-stu-id="70cb0-340">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="70cb0-341">請勿將 Include 參考嵌入其他 Include 檔案中。</span><span class="sxs-lookup"><span data-stu-id="70cb0-341">Don't embed include references within other include files.</span></span> <span data-ttu-id="70cb0-342">不支援此使用方式。</span><span class="sxs-lookup"><span data-stu-id="70cb0-342">They are not supported.</span></span>
- <span data-ttu-id="70cb0-343">將媒體檔案放在包含資料夾的特定 [media] 資料夾中，例如 `<repo>`/includes/media 資料夾。</span><span class="sxs-lookup"><span data-stu-id="70cb0-343">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="70cb0-344">[media] 目錄的根目錄中不應包含任何影像。</span><span class="sxs-lookup"><span data-stu-id="70cb0-344">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="70cb0-345">如果 Include 檔案沒有影像，則不需要對應的媒體目錄。</span><span class="sxs-lookup"><span data-stu-id="70cb0-345">If the include file does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="70cb0-346">對於一般文章，請勿在不同包含檔案之間共用媒體。</span><span class="sxs-lookup"><span data-stu-id="70cb0-346">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="70cb0-347">請針對每個 Include 檔案和文章，使用具有唯一名稱的個別檔案。</span><span class="sxs-lookup"><span data-stu-id="70cb0-347">Use a separate file with a unique name for each include file and article.</span></span> <span data-ttu-id="70cb0-348">將媒體檔案儲存在與該 Include 檔案相關聯的媒體資料夾。</span><span class="sxs-lookup"><span data-stu-id="70cb0-348">Store the media file in the media folder that's associated with the include file.</span></span>
- <span data-ttu-id="70cb0-349">請勿將 Include 檔案用作文章的唯一內容。</span><span class="sxs-lookup"><span data-stu-id="70cb0-349">Don't use an include file as the only content of an article.</span></span>  <span data-ttu-id="70cb0-350">Include 檔案的設計目的是補充文章其他部分中的內容。</span><span class="sxs-lookup"><span data-stu-id="70cb0-350">Include files are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="70cb0-351">範例：</span><span class="sxs-lookup"><span data-stu-id="70cb0-351">Example:</span></span>

```markdown
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="70cb0-352">選取器</span><span class="sxs-lookup"><span data-stu-id="70cb0-352">Selectors</span></span>

<span data-ttu-id="70cb0-353">當您撰寫同一篇技術文章的不同版本時，可以使用選取器，以滿足跨技術或平台的實作差異。</span><span class="sxs-lookup"><span data-stu-id="70cb0-353">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="70cb0-354">一般而言，此功能非常適合開發人員的行動平台內容。</span><span class="sxs-lookup"><span data-stu-id="70cb0-354">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="70cb0-355">Markdig 中目前有兩種不同類型的選取器：單一選取器和多重選取器。</span><span class="sxs-lookup"><span data-stu-id="70cb0-355">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="70cb0-356">因為相同的選擇器 Markdown 會進入選取範圍的每個文章中，我們建議您將文章的選擇器放在 Include 檔案中。</span><span class="sxs-lookup"><span data-stu-id="70cb0-356">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="70cb0-357">接著，您可以在您使用相同選擇器的所有文章中參考該 Include 檔案。</span><span class="sxs-lookup"><span data-stu-id="70cb0-357">Then you can reference that include file in all your articles that use the same selector.</span></span>

<span data-ttu-id="70cb0-358">下圖顯示範例選取器：</span><span class="sxs-lookup"><span data-stu-id="70cb0-358">The following shows an example selector:</span></span>

```markdown
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="70cb0-359">您可以在 [Azure 文件](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic)中查看選取器的範例。</span><span class="sxs-lookup"><span data-stu-id="70cb0-359">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-include-references"></a><span data-ttu-id="70cb0-360">程式碼 Include 參考</span><span class="sxs-lookup"><span data-stu-id="70cb0-360">Code include references</span></span>

<span data-ttu-id="70cb0-361">Markdig 透過其程式碼片段擴充，支援在文章中包含程式碼的進階方式。</span><span class="sxs-lookup"><span data-stu-id="70cb0-361">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="70cb0-362">它也提供建置在 GFM 功能上的進階轉譯，例如程式設計語言選擇和語法著色，以及各種實用功能，例如：</span><span class="sxs-lookup"><span data-stu-id="70cb0-362">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="70cb0-363">包含來自外部存放庫的集中程式碼範例/片段。</span><span class="sxs-lookup"><span data-stu-id="70cb0-363">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="70cb0-364">可顯示不同語言版本程式碼範例的標籤化 UI。</span><span class="sxs-lookup"><span data-stu-id="70cb0-364">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="70cb0-365">偵錯與疑難排解</span><span class="sxs-lookup"><span data-stu-id="70cb0-365">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="70cb0-366">替代文字</span><span class="sxs-lookup"><span data-stu-id="70cb0-366">Alt text</span></span>

<span data-ttu-id="70cb0-367">將無法正確轉譯包含底線的替泰文字。</span><span class="sxs-lookup"><span data-stu-id="70cb0-367">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="70cb0-368">例如，不要使用此語法︰</span><span class="sxs-lookup"><span data-stu-id="70cb0-368">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="70cb0-369">將底線逸出，如下所示：</span><span class="sxs-lookup"><span data-stu-id="70cb0-369">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="70cb0-370">縮寫符號和雙引號</span><span class="sxs-lookup"><span data-stu-id="70cb0-370">Apostrophes and quotation marks</span></span>

<span data-ttu-id="70cb0-371">如果您將內容從 Word 複製到 Markdown 編輯器中，文字可能會包含「智慧」(彎曲) 縮寫符號或雙引號。</span><span class="sxs-lookup"><span data-stu-id="70cb0-371">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="70cb0-372">這些必須編碼或變更為基本縮寫符號或雙引號。</span><span class="sxs-lookup"><span data-stu-id="70cb0-372">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="70cb0-373">否則檔案發佈後可能會產生這樣的內容：Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="70cb0-373">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="70cb0-374">以下是這些標點符號的「智慧」版本編碼：</span><span class="sxs-lookup"><span data-stu-id="70cb0-374">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="70cb0-375">左 (開頭) 雙引號：`&#8220;`</span><span class="sxs-lookup"><span data-stu-id="70cb0-375">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="70cb0-376">右 (結尾) 雙引號：`&#8221;`</span><span class="sxs-lookup"><span data-stu-id="70cb0-376">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="70cb0-377">右 (結尾) 單引號或縮寫符號：`&#8217;`</span><span class="sxs-lookup"><span data-stu-id="70cb0-377">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="70cb0-378">左 (開頭) 單引號 (很少使用)：`&#8216;`</span><span class="sxs-lookup"><span data-stu-id="70cb0-378">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="70cb0-379">角括號</span><span class="sxs-lookup"><span data-stu-id="70cb0-379">Angle brackets</span></span>

<span data-ttu-id="70cb0-380">通常會使用角括弧來表示預留位置。</span><span class="sxs-lookup"><span data-stu-id="70cb0-380">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="70cb0-381">當您使用文字 (非程式碼) 執行此作業時，必須編碼角括弧。</span><span class="sxs-lookup"><span data-stu-id="70cb0-381">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="70cb0-382">否則 Markdown 會將它們視為 HTML 標籤。</span><span class="sxs-lookup"><span data-stu-id="70cb0-382">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="70cb0-383">例如，將 `<script name>` 編碼成 `&lt;script name&gt;`</span><span class="sxs-lookup"><span data-stu-id="70cb0-383">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="70cb0-384">另請參閱：</span><span class="sxs-lookup"><span data-stu-id="70cb0-384">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="70cb0-385">Markdown 資源</span><span class="sxs-lookup"><span data-stu-id="70cb0-385">Markdown resources</span></span>

- <span data-ttu-id="70cb0-386">[Markdown 簡介](https://daringfireball.net/projects/markdown/syntax) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="70cb0-386">[Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax)</span></span>
- [<span data-ttu-id="70cb0-387">Docs Markdown 速查表</span><span class="sxs-lookup"><span data-stu-id="70cb0-387">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- <span data-ttu-id="70cb0-388">[GitHub 的 Markdown 基本概念](https://help.github.com/articles/markdown-basics/) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="70cb0-388">[GitHub's Markdown Basics](https://help.github.com/articles/markdown-basics/)</span></span>
- <span data-ttu-id="70cb0-389">[The Markdown Guide](https://www.markdownguide.org/) (Markdown 指南)</span><span class="sxs-lookup"><span data-stu-id="70cb0-389">[The Markdown Guide](https://www.markdownguide.org/)</span></span>
