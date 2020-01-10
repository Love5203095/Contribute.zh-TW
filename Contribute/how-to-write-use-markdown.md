---
title: 如何使用 Markdown 來撰寫 Docs
description: 本文提供用於撰寫 docs.microsoft.com 文章之 Markdown 語言的基本概念和參考資訊。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 03/26/2019
ms.openlocfilehash: 1f43cecb450c988e4f546aa5ecc5907061521f34
ms.sourcegitcommit: a812d716b31084926b886b93923f9b84c9b23429
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/18/2019
ms.locfileid: "75188297"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="91c53-103">如何使用 Markdown 來撰寫 Docs</span><span class="sxs-lookup"><span data-stu-id="91c53-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="91c53-104">[Docs.microsoft.com](https://docs.microsoft.com) 文章是以稱為 [Markdown](https://daringfireball.net/projects/markdown/) 的輕量型標記語言撰寫，此標記語言容易閱讀及學習。</span><span class="sxs-lookup"><span data-stu-id="91c53-104">[Docs.microsoft.com](https://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="91c53-105">基於這個原因，它很快地就成為業界標準。</span><span class="sxs-lookup"><span data-stu-id="91c53-105">Because of this, it has quickly become an industry standard.</span></span> <span data-ttu-id="91c53-106">文件網站使用 Markdown 的 [Markdig 變體](#markdown-flavor)。</span><span class="sxs-lookup"><span data-stu-id="91c53-106">The docs site uses the [Markdig flavor](#markdown-flavor) of Markdown.</span></span>


## <a name="markdown-basics"></a><span data-ttu-id="91c53-107">Markdown 基本概念</span><span class="sxs-lookup"><span data-stu-id="91c53-107">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="91c53-108">標題</span><span class="sxs-lookup"><span data-stu-id="91c53-108">Headings</span></span>

<span data-ttu-id="91c53-109">若要建立標題，您可以使用井字號，如下所示：</span><span class="sxs-lookup"><span data-stu-id="91c53-109">To create a heading, you use a hash mark (#), as follows:</span></span>

```md
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="91c53-110">標題應該使用 ATX 樣式來完成，也就是在行的開頭使用 1-6 個井字號 (#) 來指出標題，對應到 H1 到 H6 的 HTML標題層級。</span><span class="sxs-lookup"><span data-stu-id="91c53-110">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="91c53-111">上面的範例使用第一級到第四級標題。</span><span class="sxs-lookup"><span data-stu-id="91c53-111">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="91c53-112">在您的主題中，**必須**只能有一個第一級標題 (H1)，顯示為其頁面上的標題。</span><span class="sxs-lookup"><span data-stu-id="91c53-112">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="91c53-113">如果您的標題以 `#` 字元作為結尾，則需要在結尾新增額外的 `#` 字元，以便正確呈現標題。</span><span class="sxs-lookup"><span data-stu-id="91c53-113">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="91c53-114">例如，`# Async Programming in F# #`。</span><span class="sxs-lookup"><span data-stu-id="91c53-114">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="91c53-115">第二級標題將產生頁面上的 TOC，顯示在頁面標題下方的「本文中」區段中。</span><span class="sxs-lookup"><span data-stu-id="91c53-115">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="91c53-116">粗體與斜體文字</span><span class="sxs-lookup"><span data-stu-id="91c53-116">Bold and italic text</span></span>

<span data-ttu-id="91c53-117">若要將文字格式設定為**粗體**，請使用兩個星號將它括住：</span><span class="sxs-lookup"><span data-stu-id="91c53-117">To format text as **bold**, you enclose it in two asterisks:</span></span>

```md
This text is **bold**.
```

<span data-ttu-id="91c53-118">若要將文字格式設定為*斜體*，請使用單一星號將它括住：</span><span class="sxs-lookup"><span data-stu-id="91c53-118">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```md
This text is *italic*.
```

<span data-ttu-id="91c53-119">若要將文字格式設定為***粗體且斜體***，請使用三個星號將它括住：</span><span class="sxs-lookup"><span data-stu-id="91c53-119">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```md
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="91c53-120">區塊引述</span><span class="sxs-lookup"><span data-stu-id="91c53-120">Blockquotes</span></span>

<span data-ttu-id="91c53-121">區塊引述使用 `>` 字元建立：</span><span class="sxs-lookup"><span data-stu-id="91c53-121">Blockquotes are created using the `>` character:</span></span>

```md
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="91c53-122">前述範例會如下呈現：</span><span class="sxs-lookup"><span data-stu-id="91c53-122">The preceding example renders as follows:</span></span>

> <span data-ttu-id="91c53-123">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span><span class="sxs-lookup"><span data-stu-id="91c53-123">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="91c53-124">此處，在赤道上，在有朝一日稱為非洲的大陸上，生存之戰已來到激烈的最高潮，而勝利者尚未現身。</span><span class="sxs-lookup"><span data-stu-id="91c53-124">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="91c53-125">在這片荒蕪乾燥的土地上，只有小型、迅速或兇猛的物體，才能繁榮昌盛，抑或抱有生存下去的希望。</span><span class="sxs-lookup"><span data-stu-id="91c53-125">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="91c53-126">清單</span><span class="sxs-lookup"><span data-stu-id="91c53-126">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="91c53-127">未排序清單</span><span class="sxs-lookup"><span data-stu-id="91c53-127">Unordered list</span></span>

<span data-ttu-id="91c53-128">若要設定不排序/項目符號清單的格式，請使用星號或短破折號。</span><span class="sxs-lookup"><span data-stu-id="91c53-128">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="91c53-129">例如，下列 Markdown：</span><span class="sxs-lookup"><span data-stu-id="91c53-129">For example, the following Markdown:</span></span>

```md
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="91c53-130">將會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="91c53-130">will be rendered as:</span></span>

- <span data-ttu-id="91c53-131">List item 1</span><span class="sxs-lookup"><span data-stu-id="91c53-131">List item 1</span></span>
- <span data-ttu-id="91c53-132">List item 2</span><span class="sxs-lookup"><span data-stu-id="91c53-132">List item 2</span></span>
- <span data-ttu-id="91c53-133">List item 3</span><span class="sxs-lookup"><span data-stu-id="91c53-133">List item 3</span></span>

<span data-ttu-id="91c53-134">若要建立包含在另一個清單中的巢狀清單，請將子清單項目縮排。</span><span class="sxs-lookup"><span data-stu-id="91c53-134">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="91c53-135">例如，下列 Markdown：</span><span class="sxs-lookup"><span data-stu-id="91c53-135">For example, the following Markdown:</span></span>

```md
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="91c53-136">將會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="91c53-136">will be rendered as:</span></span>

- <span data-ttu-id="91c53-137">List item 1</span><span class="sxs-lookup"><span data-stu-id="91c53-137">List item 1</span></span>
  - <span data-ttu-id="91c53-138">List item A</span><span class="sxs-lookup"><span data-stu-id="91c53-138">List item A</span></span>
  - <span data-ttu-id="91c53-139">List item B</span><span class="sxs-lookup"><span data-stu-id="91c53-139">List item B</span></span>
- <span data-ttu-id="91c53-140">List item 2</span><span class="sxs-lookup"><span data-stu-id="91c53-140">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="91c53-141">已排序清單</span><span class="sxs-lookup"><span data-stu-id="91c53-141">Ordered list</span></span>

<span data-ttu-id="91c53-142">若要設定已排序/逐步清單的格式，請使用對應的數字。</span><span class="sxs-lookup"><span data-stu-id="91c53-142">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="91c53-143">例如，下列 Markdown：</span><span class="sxs-lookup"><span data-stu-id="91c53-143">For example, the following Markdown:</span></span>

```md
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="91c53-144">將會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="91c53-144">will be rendered as:</span></span>

1. <span data-ttu-id="91c53-145">First instruction</span><span class="sxs-lookup"><span data-stu-id="91c53-145">First instruction</span></span>
2. <span data-ttu-id="91c53-146">Second instruction</span><span class="sxs-lookup"><span data-stu-id="91c53-146">Second instruction</span></span>
3. <span data-ttu-id="91c53-147">Third instruction</span><span class="sxs-lookup"><span data-stu-id="91c53-147">Third instruction</span></span>

<span data-ttu-id="91c53-148">若要建立包含在另一個清單中的巢狀清單，請將子清單項目縮排。</span><span class="sxs-lookup"><span data-stu-id="91c53-148">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="91c53-149">例如，下列 Markdown：</span><span class="sxs-lookup"><span data-stu-id="91c53-149">For example, the following Markdown:</span></span>

```md
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="91c53-150">將會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="91c53-150">will be rendered as:</span></span>

1. <span data-ttu-id="91c53-151">First instruction</span><span class="sxs-lookup"><span data-stu-id="91c53-151">First instruction</span></span>
   1. <span data-ttu-id="91c53-152">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="91c53-152">Sub-instruction</span></span>
   2. <span data-ttu-id="91c53-153">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="91c53-153">Sub-instruction</span></span>
2. <span data-ttu-id="91c53-154">Second instruction</span><span class="sxs-lookup"><span data-stu-id="91c53-154">Second instruction</span></span>

<span data-ttu-id="91c53-155">請注意，針對所有項目我們</span><span class="sxs-lookup"><span data-stu-id="91c53-155">Note that we use '1.'</span></span> <span data-ttu-id="91c53-156">均使用 '1'。</span><span class="sxs-lookup"><span data-stu-id="91c53-156">for all entries.</span></span> <span data-ttu-id="91c53-157">這樣，當未來的更新包含新步驟或刪除現有步驟時，就能更輕鬆的檢閱差異。</span><span class="sxs-lookup"><span data-stu-id="91c53-157">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="91c53-158">Tables</span><span class="sxs-lookup"><span data-stu-id="91c53-158">Tables</span></span>

<span data-ttu-id="91c53-159">表格不是核心 Markdown 規格的一部分，但是 GFM 支援表格。</span><span class="sxs-lookup"><span data-stu-id="91c53-159">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="91c53-160">您可以使用管線 (|) 和連字號 (-) 字元來建立表格。</span><span class="sxs-lookup"><span data-stu-id="91c53-160">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="91c53-161">連字號是用來建立每一欄的標頭，而管線是用來分隔每一欄。</span><span class="sxs-lookup"><span data-stu-id="91c53-161">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="91c53-162">請在您的表格之前包含一個空白行，這樣才能正確轉譯。</span><span class="sxs-lookup"><span data-stu-id="91c53-162">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="91c53-163">例如，下列 Markdown：</span><span class="sxs-lookup"><span data-stu-id="91c53-163">For example, the following Markdown:</span></span>

```md
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="91c53-164">將會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="91c53-164">Will be rendered as:</span></span>

| <span data-ttu-id="91c53-165">Fun</span><span class="sxs-lookup"><span data-stu-id="91c53-165">Fun</span></span>                  | <span data-ttu-id="91c53-166">With</span><span class="sxs-lookup"><span data-stu-id="91c53-166">With</span></span>                 | <span data-ttu-id="91c53-167">Tables</span><span class="sxs-lookup"><span data-stu-id="91c53-167">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="91c53-168">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="91c53-168">left-aligned column</span></span>  | <span data-ttu-id="91c53-169">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="91c53-169">right-aligned column</span></span> | <span data-ttu-id="91c53-170">centered column</span><span class="sxs-lookup"><span data-stu-id="91c53-170">centered column</span></span> |
| <span data-ttu-id="91c53-171">$100</span><span class="sxs-lookup"><span data-stu-id="91c53-171">$100</span></span>                 | <span data-ttu-id="91c53-172">$100</span><span class="sxs-lookup"><span data-stu-id="91c53-172">$100</span></span>                 | <span data-ttu-id="91c53-173">$100</span><span class="sxs-lookup"><span data-stu-id="91c53-173">$100</span></span>            |
| <span data-ttu-id="91c53-174">$10</span><span class="sxs-lookup"><span data-stu-id="91c53-174">$10</span></span>                  | <span data-ttu-id="91c53-175">$10</span><span class="sxs-lookup"><span data-stu-id="91c53-175">$10</span></span>                  | <span data-ttu-id="91c53-176">$10</span><span class="sxs-lookup"><span data-stu-id="91c53-176">$10</span></span>             |
| <span data-ttu-id="91c53-177">$1</span><span class="sxs-lookup"><span data-stu-id="91c53-177">$1</span></span>                   | <span data-ttu-id="91c53-178">$1</span><span class="sxs-lookup"><span data-stu-id="91c53-178">$1</span></span>                   | <span data-ttu-id="91c53-179">$1</span><span class="sxs-lookup"><span data-stu-id="91c53-179">$1</span></span>              |

<span data-ttu-id="91c53-180">如需有關如何建立表格的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="91c53-180">For more information on creating tables, see:</span></span>

- <span data-ttu-id="91c53-181">GitHub 的 [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/) (使用表格組織資訊)。</span><span class="sxs-lookup"><span data-stu-id="91c53-181">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="91c53-182">[Markdown 表格產生器](https://www.tablesgenerator.com/markdown_tables) Web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="91c53-182">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="91c53-183">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables) (Adam Pritchard 的 Markdown 速查表)。</span><span class="sxs-lookup"><span data-stu-id="91c53-183">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="91c53-184">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table) (Michel Fortin 的 Markdown Extra)。</span><span class="sxs-lookup"><span data-stu-id="91c53-184">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="91c53-185">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/) (將 HTML 表格轉換為 Markdown)。</span><span class="sxs-lookup"><span data-stu-id="91c53-185">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="91c53-186">連結</span><span class="sxs-lookup"><span data-stu-id="91c53-186">Links</span></span>

<span data-ttu-id="91c53-187">內嵌連結的 Markdown 語法是由超連結文字 `[link text]` 部分，以及緊接在後面的連結 URL 或檔案名稱 `(file-name.md)` 部分所組成：</span><span class="sxs-lookup"><span data-stu-id="91c53-187">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="91c53-188">如需連結的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="91c53-188">For more information on linking, see:</span></span>

- <span data-ttu-id="91c53-189">[Markdown 語法指南](https://daringfireball.net/projects/markdown/syntax#link) 的 Markdown 基礎連結支援。</span><span class="sxs-lookup"><span data-stu-id="91c53-189">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="91c53-190">本指南的[連結](how-to-write-links.md)一節，有 Markdig 提供的額外連結語法詳細資料。</span><span class="sxs-lookup"><span data-stu-id="91c53-190">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="91c53-191">程式碼片段</span><span class="sxs-lookup"><span data-stu-id="91c53-191">Code snippets</span></span>

<span data-ttu-id="91c53-192">Markdown 支援將程式碼片段內嵌在句子中，或是在句子之間形成個別圍住的區塊。</span><span class="sxs-lookup"><span data-stu-id="91c53-192">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="91c53-193">如需詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="91c53-193">For details, see:</span></span>

- <span data-ttu-id="91c53-194">[Markdown 的程式碼區塊原生支援](https://daringfireball.net/projects/markdown/syntax#precode) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="91c53-194">[Markdown's native support for code blocks](https://daringfireball.net/projects/markdown/syntax#precode)</span></span>
- <span data-ttu-id="91c53-195">[GFM 對程式碼包圍和語法醒目提示的支援](https://help.github.com/articles/creating-and-highlighting-code-blocks/) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="91c53-195">[GFM support for code fencing and syntax highlighting](https://help.github.com/articles/creating-and-highlighting-code-blocks/)</span></span>

<span data-ttu-id="91c53-196">圍住的程式碼區塊是對程式碼片段支援語法醒目提示的簡單方式。</span><span class="sxs-lookup"><span data-stu-id="91c53-196">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="91c53-197">圍住的程式碼區塊的一般格式為：</span><span class="sxs-lookup"><span data-stu-id="91c53-197">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="91c53-198">前三個倒引號 (\`) 字元之後的別名定義所要使用語法醒目提示。</span><span class="sxs-lookup"><span data-stu-id="91c53-198">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="91c53-199">下列清單是 Docs 內容中常用的程式設計語言與對應的標籤：</span><span class="sxs-lookup"><span data-stu-id="91c53-199">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="91c53-200">這些語言包含易記名稱支援，且大部分都具有語言反白顯示。</span><span class="sxs-lookup"><span data-stu-id="91c53-200">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="91c53-201">Name</span><span class="sxs-lookup"><span data-stu-id="91c53-201">Name</span></span>|<span data-ttu-id="91c53-202">Markdown 標籤</span><span class="sxs-lookup"><span data-stu-id="91c53-202">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="91c53-203">.NET 主控台</span><span class="sxs-lookup"><span data-stu-id="91c53-203">.NET Console</span></span>|<span data-ttu-id="91c53-204">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="91c53-204">dotnetcli</span></span>|
|<span data-ttu-id="91c53-205">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="91c53-205">ASP.NET (C#)</span></span>|<span data-ttu-id="91c53-206">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="91c53-206">aspx-csharp</span></span>|
|<span data-ttu-id="91c53-207">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="91c53-207">ASP.NET (VB)</span></span>|<span data-ttu-id="91c53-208">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="91c53-208">aspx-vb</span></span>|
|<span data-ttu-id="91c53-209">AzCopy</span><span class="sxs-lookup"><span data-stu-id="91c53-209">AzCopy</span></span>|<span data-ttu-id="91c53-210">azcopy</span><span class="sxs-lookup"><span data-stu-id="91c53-210">azcopy</span></span>|
|<span data-ttu-id="91c53-211">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="91c53-211">Azure CLI</span></span>|<span data-ttu-id="91c53-212">azurecli</span><span class="sxs-lookup"><span data-stu-id="91c53-212">azurecli</span></span>|
|<span data-ttu-id="91c53-213">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="91c53-213">Azure PowerShell</span></span>|<span data-ttu-id="91c53-214">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="91c53-214">azurepowershell</span></span>|
|<span data-ttu-id="91c53-215">Bash</span><span class="sxs-lookup"><span data-stu-id="91c53-215">Bash</span></span>|<span data-ttu-id="91c53-216">bash</span><span class="sxs-lookup"><span data-stu-id="91c53-216">bash</span></span>|
|<span data-ttu-id="91c53-217">C++</span><span class="sxs-lookup"><span data-stu-id="91c53-217">C++</span></span>|<span data-ttu-id="91c53-218">cpp</span><span class="sxs-lookup"><span data-stu-id="91c53-218">cpp</span></span>|
|<span data-ttu-id="91c53-219">C++/CX</span><span class="sxs-lookup"><span data-stu-id="91c53-219">C++/CX</span></span>|<span data-ttu-id="91c53-220">cppcx</span><span class="sxs-lookup"><span data-stu-id="91c53-220">cppcx</span></span>|
|<span data-ttu-id="91c53-221">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="91c53-221">C++/WinRT</span></span>|<span data-ttu-id="91c53-222">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="91c53-222">cppwinrt</span></span>|
|<span data-ttu-id="91c53-223">C#</span><span class="sxs-lookup"><span data-stu-id="91c53-223">C#</span></span>|<span data-ttu-id="91c53-224">csharp</span><span class="sxs-lookup"><span data-stu-id="91c53-224">csharp</span></span>|
|<span data-ttu-id="91c53-225">網頁瀏覽器中的 C#</span><span class="sxs-lookup"><span data-stu-id="91c53-225">C# in browser</span></span>|<span data-ttu-id="91c53-226">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="91c53-226">csharp-interactive</span></span>|
|<span data-ttu-id="91c53-227">主控台</span><span class="sxs-lookup"><span data-stu-id="91c53-227">Console</span></span>|<span data-ttu-id="91c53-228">主控台</span><span class="sxs-lookup"><span data-stu-id="91c53-228">console</span></span>|
|<span data-ttu-id="91c53-229">CSHTML</span><span class="sxs-lookup"><span data-stu-id="91c53-229">CSHTML</span></span>|<span data-ttu-id="91c53-230">cshtml</span><span class="sxs-lookup"><span data-stu-id="91c53-230">cshtml</span></span>|
|<span data-ttu-id="91c53-231">DAX</span><span class="sxs-lookup"><span data-stu-id="91c53-231">DAX</span></span>|<span data-ttu-id="91c53-232">dax</span><span class="sxs-lookup"><span data-stu-id="91c53-232">dax</span></span>|
|<span data-ttu-id="91c53-233">Docker</span><span class="sxs-lookup"><span data-stu-id="91c53-233">Docker</span></span>|<span data-ttu-id="91c53-234">dockerfile</span><span class="sxs-lookup"><span data-stu-id="91c53-234">dockerfile</span></span>|
|<span data-ttu-id="91c53-235">F#</span><span class="sxs-lookup"><span data-stu-id="91c53-235">F#</span></span>|<span data-ttu-id="91c53-236">fsharp</span><span class="sxs-lookup"><span data-stu-id="91c53-236">fsharp</span></span>|
|<span data-ttu-id="91c53-237">Go</span><span class="sxs-lookup"><span data-stu-id="91c53-237">Go</span></span>|<span data-ttu-id="91c53-238">go</span><span class="sxs-lookup"><span data-stu-id="91c53-238">go</span></span>|
|<span data-ttu-id="91c53-239">HTML</span><span class="sxs-lookup"><span data-stu-id="91c53-239">HTML</span></span>|<span data-ttu-id="91c53-240">html</span><span class="sxs-lookup"><span data-stu-id="91c53-240">html</span></span>|
|<span data-ttu-id="91c53-241">HTTP</span><span class="sxs-lookup"><span data-stu-id="91c53-241">HTTP</span></span>|<span data-ttu-id="91c53-242">http</span><span class="sxs-lookup"><span data-stu-id="91c53-242">http</span></span>|
|<span data-ttu-id="91c53-243">Java</span><span class="sxs-lookup"><span data-stu-id="91c53-243">Java</span></span>|<span data-ttu-id="91c53-244">java</span><span class="sxs-lookup"><span data-stu-id="91c53-244">java</span></span>|
|<span data-ttu-id="91c53-245">JavaScript</span><span class="sxs-lookup"><span data-stu-id="91c53-245">JavaScript</span></span>|<span data-ttu-id="91c53-246">javascript</span><span class="sxs-lookup"><span data-stu-id="91c53-246">javascript</span></span>|
|<span data-ttu-id="91c53-247">JSON</span><span class="sxs-lookup"><span data-stu-id="91c53-247">JSON</span></span>|<span data-ttu-id="91c53-248">json</span><span class="sxs-lookup"><span data-stu-id="91c53-248">json</span></span>|
|<span data-ttu-id="91c53-249">Kusto 查詢語言</span><span class="sxs-lookup"><span data-stu-id="91c53-249">Kusto Query Language</span></span>|<span data-ttu-id="91c53-250">kusto</span><span class="sxs-lookup"><span data-stu-id="91c53-250">kusto</span></span>|
|<span data-ttu-id="91c53-251">Markdown</span><span class="sxs-lookup"><span data-stu-id="91c53-251">Markdown</span></span>|<span data-ttu-id="91c53-252">md</span><span class="sxs-lookup"><span data-stu-id="91c53-252">md</span></span>|
|<span data-ttu-id="91c53-253">Objective-C</span><span class="sxs-lookup"><span data-stu-id="91c53-253">Objective-C</span></span>|<span data-ttu-id="91c53-254">objc</span><span class="sxs-lookup"><span data-stu-id="91c53-254">objc</span></span>|
|<span data-ttu-id="91c53-255">OData</span><span class="sxs-lookup"><span data-stu-id="91c53-255">OData</span></span>|<span data-ttu-id="91c53-256">odata</span><span class="sxs-lookup"><span data-stu-id="91c53-256">odata</span></span>|
|<span data-ttu-id="91c53-257">PHP</span><span class="sxs-lookup"><span data-stu-id="91c53-257">PHP</span></span>|<span data-ttu-id="91c53-258">php</span><span class="sxs-lookup"><span data-stu-id="91c53-258">php</span></span>|
|<span data-ttu-id="91c53-259">protobuf</span><span class="sxs-lookup"><span data-stu-id="91c53-259">protobuf</span></span>|<span data-ttu-id="91c53-260">protobuf</span><span class="sxs-lookup"><span data-stu-id="91c53-260">protobuf</span></span>|
|<span data-ttu-id="91c53-261">PowerApps (小數點小數分隔符號)</span><span class="sxs-lookup"><span data-stu-id="91c53-261">PowerApps (dot decimal separator)</span></span>|<span data-ttu-id="91c53-262">powerapps-dot</span><span class="sxs-lookup"><span data-stu-id="91c53-262">powerapps-dot</span></span>|
|<span data-ttu-id="91c53-263">PowerApps (逗點小數分隔符號)</span><span class="sxs-lookup"><span data-stu-id="91c53-263">PowerApps (comma decimal separator)</span></span>|<span data-ttu-id="91c53-264">powerapps-comma</span><span class="sxs-lookup"><span data-stu-id="91c53-264">powerapps-comma</span></span>|
|<span data-ttu-id="91c53-265">PowerShell</span><span class="sxs-lookup"><span data-stu-id="91c53-265">PowerShell</span></span>|<span data-ttu-id="91c53-266">powershell</span><span class="sxs-lookup"><span data-stu-id="91c53-266">powershell</span></span>|
|<span data-ttu-id="91c53-267">Python</span><span class="sxs-lookup"><span data-stu-id="91c53-267">Python</span></span>|<span data-ttu-id="91c53-268">python</span><span class="sxs-lookup"><span data-stu-id="91c53-268">python</span></span>|
|<span data-ttu-id="91c53-269">Q#</span><span class="sxs-lookup"><span data-stu-id="91c53-269">Q#</span></span>|<span data-ttu-id="91c53-270">qsharp</span><span class="sxs-lookup"><span data-stu-id="91c53-270">qsharp</span></span>|
|<span data-ttu-id="91c53-271">R</span><span class="sxs-lookup"><span data-stu-id="91c53-271">R</span></span>|<span data-ttu-id="91c53-272">r</span><span class="sxs-lookup"><span data-stu-id="91c53-272">r</span></span>|
|<span data-ttu-id="91c53-273">Ruby</span><span class="sxs-lookup"><span data-stu-id="91c53-273">Ruby</span></span>|<span data-ttu-id="91c53-274">ruby</span><span class="sxs-lookup"><span data-stu-id="91c53-274">ruby</span></span>|
|<span data-ttu-id="91c53-275">SQL</span><span class="sxs-lookup"><span data-stu-id="91c53-275">SQL</span></span>|<span data-ttu-id="91c53-276">sql</span><span class="sxs-lookup"><span data-stu-id="91c53-276">sql</span></span>|
|<span data-ttu-id="91c53-277">Swift</span><span class="sxs-lookup"><span data-stu-id="91c53-277">Swift</span></span>|<span data-ttu-id="91c53-278">swift</span><span class="sxs-lookup"><span data-stu-id="91c53-278">swift</span></span>|
|<span data-ttu-id="91c53-279">TypeScript</span><span class="sxs-lookup"><span data-stu-id="91c53-279">TypeScript</span></span>|<span data-ttu-id="91c53-280">typescript</span><span class="sxs-lookup"><span data-stu-id="91c53-280">typescript</span></span>|
|<span data-ttu-id="91c53-281">VB</span><span class="sxs-lookup"><span data-stu-id="91c53-281">VB</span></span>|<span data-ttu-id="91c53-282">vb</span><span class="sxs-lookup"><span data-stu-id="91c53-282">vb</span></span>|
|<span data-ttu-id="91c53-283">XAML</span><span class="sxs-lookup"><span data-stu-id="91c53-283">XAML</span></span>|<span data-ttu-id="91c53-284">xaml</span><span class="sxs-lookup"><span data-stu-id="91c53-284">xaml</span></span>|
|<span data-ttu-id="91c53-285">XML</span><span class="sxs-lookup"><span data-stu-id="91c53-285">XML</span></span>|<span data-ttu-id="91c53-286">xml</span><span class="sxs-lookup"><span data-stu-id="91c53-286">xml</span></span>|

<span data-ttu-id="91c53-287">`csharp-interactive` 名稱會指定 C# 語言，並指定在瀏覽器執行範例的能力。</span><span class="sxs-lookup"><span data-stu-id="91c53-287">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="91c53-288">這些程式碼片段會在 Docker 容器中編譯和執行，且程式執行的結果會顯示在使用者的瀏覽器視窗中。</span><span class="sxs-lookup"><span data-stu-id="91c53-288">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="91c53-289">範例：C\#</span><span class="sxs-lookup"><span data-stu-id="91c53-289">Example: C\#</span></span>

<span data-ttu-id="91c53-290">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="91c53-290">__Markdown__</span></span>

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

<span data-ttu-id="91c53-291">__轉譯器__</span><span class="sxs-lookup"><span data-stu-id="91c53-291">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="91c53-292">範例：SQL</span><span class="sxs-lookup"><span data-stu-id="91c53-292">Example: SQL</span></span>

<span data-ttu-id="91c53-293">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="91c53-293">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="91c53-294">__轉譯器__</span><span class="sxs-lookup"><span data-stu-id="91c53-294">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="docs-custom-markdown-extensions"></a><span data-ttu-id="91c53-295">Docs 自訂 Markdown 延伸模組</span><span class="sxs-lookup"><span data-stu-id="91c53-295">Docs custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="91c53-296">Docs.Microsoft.com (Docs) 會實作用於 Markdown 的 Markdig 剖析器，這與 GitHub 適用的 Markdown (GFM) 高度相容。</span><span class="sxs-lookup"><span data-stu-id="91c53-296">Docs.Microsoft.com (Docs) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="91c53-297">Markdig 透過 Markdown 擴充新增了一些功能。</span><span class="sxs-lookup"><span data-stu-id="91c53-297">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="91c53-298">就真正的意義來說，從完整《OPS 撰寫指南》選取的文章包含在此指南中供參考</span><span class="sxs-lookup"><span data-stu-id="91c53-298">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="91c53-299">(例如，請參閱目錄中的＜Markdig 與 Markdown 擴充＞和＜程式碼片段＞)。</span><span class="sxs-lookup"><span data-stu-id="91c53-299">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="91c53-300">Docs 文章使用 GFM 來設定大部分的文章格式 (例如段落、連結、清單與標題)。</span><span class="sxs-lookup"><span data-stu-id="91c53-300">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="91c53-301">如需更豐富的格式設定，文章可以使用 Markdig 功能，例如：</span><span class="sxs-lookup"><span data-stu-id="91c53-301">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="91c53-302">注意事項區塊</span><span class="sxs-lookup"><span data-stu-id="91c53-302">Note blocks</span></span>
- <span data-ttu-id="91c53-303">Include 檔案</span><span class="sxs-lookup"><span data-stu-id="91c53-303">Include files</span></span>
- <span data-ttu-id="91c53-304">選取器</span><span class="sxs-lookup"><span data-stu-id="91c53-304">Selectors</span></span>
- <span data-ttu-id="91c53-305">內嵌影片</span><span class="sxs-lookup"><span data-stu-id="91c53-305">Embedded videos</span></span>
- <span data-ttu-id="91c53-306">程式碼片段/範例</span><span class="sxs-lookup"><span data-stu-id="91c53-306">Code snippets/samples</span></span>

<span data-ttu-id="91c53-307">如需完整清單，請參閱目錄中的＜Markdig 與 Markdown 擴充＞和＜程式碼片段＞。</span><span class="sxs-lookup"><span data-stu-id="91c53-307">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="91c53-308">注意事項區塊</span><span class="sxs-lookup"><span data-stu-id="91c53-308">Note blocks</span></span>

<span data-ttu-id="91c53-309">有四種類型的注意事項區塊可供您選擇用來強調特定內容：</span><span class="sxs-lookup"><span data-stu-id="91c53-309">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="91c53-310">注意</span><span class="sxs-lookup"><span data-stu-id="91c53-310">NOTE</span></span>
- <span data-ttu-id="91c53-311">警告</span><span class="sxs-lookup"><span data-stu-id="91c53-311">WARNING</span></span>
- <span data-ttu-id="91c53-312">祕訣</span><span class="sxs-lookup"><span data-stu-id="91c53-312">TIP</span></span>
- <span data-ttu-id="91c53-313">重要</span><span class="sxs-lookup"><span data-stu-id="91c53-313">IMPORTANT</span></span>

<span data-ttu-id="91c53-314">在一般情況下，應該謹慎使用注意事項區塊，因為它們可能會造成干擾。</span><span class="sxs-lookup"><span data-stu-id="91c53-314">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="91c53-315">雖然注意事項區塊也支援程式碼區塊、影像、清單和連結，但請盡量讓它們保持簡單明瞭。</span><span class="sxs-lookup"><span data-stu-id="91c53-315">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="91c53-316">範例：</span><span class="sxs-lookup"><span data-stu-id="91c53-316">Examples:</span></span>

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

<span data-ttu-id="91c53-317">這些警示在 docs.microsoft.com 中看起來像這樣：</span><span class="sxs-lookup"><span data-stu-id="91c53-317">These alerts look like this on docs.microsoft.com:</span></span>

![顯示上一個範例中的警示在發佈的 Docs 頁面如何呈現出不同的圖示與色彩](media/alerts-rendering.png)

### <a name="include-files"></a><span data-ttu-id="91c53-319">Include 檔案</span><span class="sxs-lookup"><span data-stu-id="91c53-319">Include files</span></span>

<span data-ttu-id="91c53-320">當您有可重複使用且需要包含在文章檔案中的文字或影像檔時，可以透過 Markdig 檔案的包含功能，使用「包含」檔案的參考。</span><span class="sxs-lookup"><span data-stu-id="91c53-320">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="91c53-321">此功能會指示 OPS 在建置階段將指定的檔案包含到文章檔案中，成為發行文章的一部分。</span><span class="sxs-lookup"><span data-stu-id="91c53-321">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="91c53-322">有三種類型的 Include 參考可協助您重複使用內容：</span><span class="sxs-lookup"><span data-stu-id="91c53-322">Three types of include references are available to help you reuse content:</span></span>

- <span data-ttu-id="91c53-323">內嵌：在另一個句子中重複使用常用程式碼片段內嵌。</span><span class="sxs-lookup"><span data-stu-id="91c53-323">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="91c53-324">區塊：您重複使用整個 Markdown 檔案作為區塊 (巢狀嵌入文章中的小節)。</span><span class="sxs-lookup"><span data-stu-id="91c53-324">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="91c53-325">影像：這是 Docs 中實作標準影像包含的方式。</span><span class="sxs-lookup"><span data-stu-id="91c53-325">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="91c53-326">內嵌或區塊 Include 檔案都只是簡單的 Markdown (.md) 檔案。</span><span class="sxs-lookup"><span data-stu-id="91c53-326">An inline or block include file is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="91c53-327">它可以包含任何有效的 Markdown。</span><span class="sxs-lookup"><span data-stu-id="91c53-327">It can contain any valid Markdown.</span></span> <span data-ttu-id="91c53-328">所有的包含 Markdown 檔案都應放在存放庫根目錄中的[一般 `/includes` 子目錄](git-github-fundamentals.md#includes-subdirectory)。</span><span class="sxs-lookup"><span data-stu-id="91c53-328">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="91c53-329">當文章發行之後，包含的檔案會直接整合到其中。</span><span class="sxs-lookup"><span data-stu-id="91c53-329">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="91c53-330">以下是 Include 檔案的需求與考量：</span><span class="sxs-lookup"><span data-stu-id="91c53-330">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="91c53-331">當您需要相同的文字出現在多篇文章中時，就可以使用 Include 檔案。</span><span class="sxs-lookup"><span data-stu-id="91c53-331">Use an include file whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="91c53-332">針對大量內容 (例如一兩個段落、共用的程序或共用的節) 使用區塊 Include 參考。</span><span class="sxs-lookup"><span data-stu-id="91c53-332">Use a block include reference for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="91c53-333">請勿將它們用在小於一個句子的內容。</span><span class="sxs-lookup"><span data-stu-id="91c53-333">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="91c53-334">因為檔案相依於 Markdig 延伸，所以不會在文章的 GitHub 轉譯檢視中轉譯 Include 參考。</span><span class="sxs-lookup"><span data-stu-id="91c53-334">Include references won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="91c53-335">它們將會在發行集之後才轉譯。</span><span class="sxs-lookup"><span data-stu-id="91c53-335">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="91c53-336">請務必將 Include 檔案中的文字撰寫成完整的句子或片語，且不相依於參考 Include 檔案之文章中的上下文。</span><span class="sxs-lookup"><span data-stu-id="91c53-336">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include file.</span></span> <span data-ttu-id="91c53-337">忽略此指導方針會使文章中產生無法翻譯的字串，進而影響本地化體驗。</span><span class="sxs-lookup"><span data-stu-id="91c53-337">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="91c53-338">請勿將 Include 參考嵌入其他 Include 檔案中。</span><span class="sxs-lookup"><span data-stu-id="91c53-338">Don't embed include references within other include files.</span></span> <span data-ttu-id="91c53-339">不支援此使用方式。</span><span class="sxs-lookup"><span data-stu-id="91c53-339">They are not supported.</span></span>
- <span data-ttu-id="91c53-340">將媒體檔案放在包含資料夾的特定 [media] 資料夾中，例如 `<repo>`/includes/media 資料夾。</span><span class="sxs-lookup"><span data-stu-id="91c53-340">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="91c53-341">[media] 目錄的根目錄中不應包含任何影像。</span><span class="sxs-lookup"><span data-stu-id="91c53-341">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="91c53-342">如果 Include 檔案沒有影像，則不需要對應的媒體目錄。</span><span class="sxs-lookup"><span data-stu-id="91c53-342">If the include file does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="91c53-343">對於一般文章，請勿在不同包含檔案之間共用媒體。</span><span class="sxs-lookup"><span data-stu-id="91c53-343">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="91c53-344">請針對每個 Include 檔案和文章，使用具有唯一名稱的個別檔案。</span><span class="sxs-lookup"><span data-stu-id="91c53-344">Use a separate file with a unique name for each include file and article.</span></span> <span data-ttu-id="91c53-345">將媒體檔案儲存在與該 Include 檔案相關聯的媒體資料夾。</span><span class="sxs-lookup"><span data-stu-id="91c53-345">Store the media file in the media folder that's associated with the include file.</span></span>
- <span data-ttu-id="91c53-346">請勿將 Include 檔案用作文章的唯一內容。</span><span class="sxs-lookup"><span data-stu-id="91c53-346">Don't use an include file as the only content of an article.</span></span>  <span data-ttu-id="91c53-347">Include 檔案的設計目的是補充文章其他部分中的內容。</span><span class="sxs-lookup"><span data-stu-id="91c53-347">Include files are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="91c53-348">範例：</span><span class="sxs-lookup"><span data-stu-id="91c53-348">Example:</span></span>

```md
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="91c53-349">選取器</span><span class="sxs-lookup"><span data-stu-id="91c53-349">Selectors</span></span>

<span data-ttu-id="91c53-350">當您撰寫同一篇技術文章的不同版本時，可以使用選取器，以滿足跨技術或平台的實作差異。</span><span class="sxs-lookup"><span data-stu-id="91c53-350">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="91c53-351">一般而言，此功能非常適合開發人員的行動平台內容。</span><span class="sxs-lookup"><span data-stu-id="91c53-351">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="91c53-352">Markdig 中目前有兩種不同類型的選取器：單一選取器和多重選取器。</span><span class="sxs-lookup"><span data-stu-id="91c53-352">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="91c53-353">因為相同的選擇器 Markdown 會進入選取範圍的每個文章中，我們建議您將文章的選擇器放在 Include 檔案中。</span><span class="sxs-lookup"><span data-stu-id="91c53-353">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="91c53-354">接著，您可以在您使用相同選擇器的所有文章中參考該 Include 檔案。</span><span class="sxs-lookup"><span data-stu-id="91c53-354">Then you can reference that include file in all your articles that use the same selector.</span></span>

<span data-ttu-id="91c53-355">下圖顯示範例選取器：</span><span class="sxs-lookup"><span data-stu-id="91c53-355">The following shows an example selector:</span></span>

```md
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="91c53-356">您可以在 [Azure 文件](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic)中查看選取器的範例。</span><span class="sxs-lookup"><span data-stu-id="91c53-356">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-include-references"></a><span data-ttu-id="91c53-357">程式碼 Include 參考</span><span class="sxs-lookup"><span data-stu-id="91c53-357">Code include references</span></span>

<span data-ttu-id="91c53-358">Markdig 透過其程式碼片段擴充，支援在文章中包含程式碼的進階方式。</span><span class="sxs-lookup"><span data-stu-id="91c53-358">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="91c53-359">它也提供建置在 GFM 功能上的進階轉譯，例如程式設計語言選擇和語法著色，以及各種實用功能，例如：</span><span class="sxs-lookup"><span data-stu-id="91c53-359">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="91c53-360">包含來自外部存放庫的集中程式碼範例/片段。</span><span class="sxs-lookup"><span data-stu-id="91c53-360">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="91c53-361">可顯示不同語言版本程式碼範例的標籤化 UI。</span><span class="sxs-lookup"><span data-stu-id="91c53-361">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="91c53-362">偵錯與疑難排解</span><span class="sxs-lookup"><span data-stu-id="91c53-362">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="91c53-363">替代文字</span><span class="sxs-lookup"><span data-stu-id="91c53-363">Alt text</span></span>

<span data-ttu-id="91c53-364">將無法正確轉譯包含底線的替代文字。</span><span class="sxs-lookup"><span data-stu-id="91c53-364">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="91c53-365">例如，不要使用此語法︰</span><span class="sxs-lookup"><span data-stu-id="91c53-365">For example, instead of using this:</span></span>

```md
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="91c53-366">將底線逸出，如下所示：</span><span class="sxs-lookup"><span data-stu-id="91c53-366">Escape the underscores like this:</span></span>

```md
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="91c53-367">縮寫符號和雙引號</span><span class="sxs-lookup"><span data-stu-id="91c53-367">Apostrophes and quotation marks</span></span>

<span data-ttu-id="91c53-368">如果您將內容從 Word 複製到 Markdown 編輯器中，文字可能會包含「智慧」(彎曲) 縮寫符號或雙引號。</span><span class="sxs-lookup"><span data-stu-id="91c53-368">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="91c53-369">這些必須編碼或變更為基本縮寫符號或雙引號。</span><span class="sxs-lookup"><span data-stu-id="91c53-369">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="91c53-370">否則檔案發佈後可能會產生這樣的內容：Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="91c53-370">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="91c53-371">以下是這些標點符號的「智慧」版本編碼：</span><span class="sxs-lookup"><span data-stu-id="91c53-371">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="91c53-372">左 (開頭) 雙引號：`&#8220;`</span><span class="sxs-lookup"><span data-stu-id="91c53-372">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="91c53-373">右 (結尾) 雙引號：`&#8221;`</span><span class="sxs-lookup"><span data-stu-id="91c53-373">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="91c53-374">右 (結尾) 單引號或縮寫符號：`&#8217;`</span><span class="sxs-lookup"><span data-stu-id="91c53-374">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="91c53-375">左 (開頭) 單引號 (很少使用)：`&#8216;`</span><span class="sxs-lookup"><span data-stu-id="91c53-375">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="91c53-376">角括號</span><span class="sxs-lookup"><span data-stu-id="91c53-376">Angle brackets</span></span>

<span data-ttu-id="91c53-377">通常會使用角括弧來表示預留位置。</span><span class="sxs-lookup"><span data-stu-id="91c53-377">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="91c53-378">當您使用文字 (非程式碼) 執行此作業時，必須編碼角括弧。</span><span class="sxs-lookup"><span data-stu-id="91c53-378">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="91c53-379">否則 Markdown 會將它們視為 HTML 標籤。</span><span class="sxs-lookup"><span data-stu-id="91c53-379">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="91c53-380">例如，將 `<script name>` 編碼成 `&lt;script name&gt;`</span><span class="sxs-lookup"><span data-stu-id="91c53-380">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="markdown-flavor"></a><span data-ttu-id="91c53-381">Markdown 變體</span><span class="sxs-lookup"><span data-stu-id="91c53-381">Markdown flavor</span></span>

<span data-ttu-id="91c53-382">docs.microsoft.com 網站後端支援透過 [Markdig](https://github.com/lunet-io/markdig) 剖析引擎且符合 [CommonMark](https://commonmark.org/) 規範的 Markdown。</span><span class="sxs-lookup"><span data-stu-id="91c53-382">The docs.microsoft.com site backend supports [CommonMark](https://commonmark.org/) compliant Markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine.</span></span> <span data-ttu-id="91c53-383">這個 Markdown 變體大多與 [GitHub 變體 Markdown (GFM)](https://help.github.com/categories/writing-on-github/) 相容，因為大多數文件都儲存在 GitHub 中並可在該處編輯。</span><span class="sxs-lookup"><span data-stu-id="91c53-383">This markdown flavor is mostly compatible with [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="91c53-384">額外的功能可透過 Markdown 延伸模組新增。</span><span class="sxs-lookup"><span data-stu-id="91c53-384">Additional functionality is added through Markdown extensions.</span></span>

## <a name="see-also"></a><span data-ttu-id="91c53-385">另請參閱：</span><span class="sxs-lookup"><span data-stu-id="91c53-385">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="91c53-386">Markdown 資源</span><span class="sxs-lookup"><span data-stu-id="91c53-386">Markdown resources</span></span>

- <span data-ttu-id="91c53-387">[Markdown 簡介](https://daringfireball.net/projects/markdown/syntax) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="91c53-387">[Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax)</span></span>
- [<span data-ttu-id="91c53-388">Docs Markdown 速查表</span><span class="sxs-lookup"><span data-stu-id="91c53-388">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- <span data-ttu-id="91c53-389">[GitHub 的 Markdown 基本概念](https://help.github.com/articles/markdown-basics/) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="91c53-389">[GitHub's Markdown Basics](https://help.github.com/articles/markdown-basics/)</span></span>
- <span data-ttu-id="91c53-390">[The Markdown Guide](https://www.markdownguide.org/) (Markdown 指南)</span><span class="sxs-lookup"><span data-stu-id="91c53-390">[The Markdown Guide](https://www.markdownguide.org/)</span></span>
