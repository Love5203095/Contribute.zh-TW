---
title: 如何使用 Markdown 來撰寫 Docs
description: 本文提供用於撰寫 docs.microsoft.com 文章之 Markdown 語言的基本概念和參考資訊。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 03/26/2019
ms.openlocfilehash: 086972acaef9647709fbe43f07c07abde71c7d9f
ms.sourcegitcommit: fd92198ec2d0ce2d6687b6f1521a82b3fefc60e0
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/16/2020
ms.locfileid: "76111059"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="f55fb-103">如何使用 Markdown 來撰寫 Docs</span><span class="sxs-lookup"><span data-stu-id="f55fb-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="f55fb-104">[Docs.microsoft.com](https://docs.microsoft.com) 文章是以稱為 [Markdown](https://daringfireball.net/projects/markdown/) 的輕量型標記語言撰寫，此標記語言容易閱讀及學習。</span><span class="sxs-lookup"><span data-stu-id="f55fb-104">[Docs.microsoft.com](https://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="f55fb-105">基於這個原因，它很快地就成為業界標準。</span><span class="sxs-lookup"><span data-stu-id="f55fb-105">Because of this, it has quickly become an industry standard.</span></span> <span data-ttu-id="f55fb-106">文件網站使用 Markdown 的 [Markdig 變體](#markdown-flavor)。</span><span class="sxs-lookup"><span data-stu-id="f55fb-106">The docs site uses the [Markdig flavor](#markdown-flavor) of Markdown.</span></span>


## <a name="markdown-basics"></a><span data-ttu-id="f55fb-107">Markdown 基本概念</span><span class="sxs-lookup"><span data-stu-id="f55fb-107">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="f55fb-108">標題</span><span class="sxs-lookup"><span data-stu-id="f55fb-108">Headings</span></span>

<span data-ttu-id="f55fb-109">若要建立標題，您可以使用井字號，如下所示：</span><span class="sxs-lookup"><span data-stu-id="f55fb-109">To create a heading, you use a hash mark (#), as follows:</span></span>

```md
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="f55fb-110">標題應該使用 ATX 樣式來完成，也就是在行的開頭使用 1-6 個井字號 (#) 來指出標題，對應到 H1 到 H6 的 HTML標題層級。</span><span class="sxs-lookup"><span data-stu-id="f55fb-110">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="f55fb-111">上面的範例使用第一級到第四級標題。</span><span class="sxs-lookup"><span data-stu-id="f55fb-111">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="f55fb-112">在您的主題中，**必須**只能有一個第一級標題 (H1)，顯示為其頁面上的標題。</span><span class="sxs-lookup"><span data-stu-id="f55fb-112">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="f55fb-113">如果您的標題以 `#` 字元作為結尾，則需要在結尾新增額外的 `#` 字元，以便正確呈現標題。</span><span class="sxs-lookup"><span data-stu-id="f55fb-113">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="f55fb-114">例如，`# Async Programming in F# #`。</span><span class="sxs-lookup"><span data-stu-id="f55fb-114">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="f55fb-115">第二級標題將產生頁面上的 TOC，顯示在頁面標題下方的「本文中」區段中。</span><span class="sxs-lookup"><span data-stu-id="f55fb-115">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="f55fb-116">粗體與斜體文字</span><span class="sxs-lookup"><span data-stu-id="f55fb-116">Bold and italic text</span></span>

<span data-ttu-id="f55fb-117">若要將文字格式設定為**粗體**，請使用兩個星號將它括住：</span><span class="sxs-lookup"><span data-stu-id="f55fb-117">To format text as **bold**, you enclose it in two asterisks:</span></span>

```md
This text is **bold**.
```

<span data-ttu-id="f55fb-118">若要將文字格式設定為*斜體*，請使用單一星號將它括住：</span><span class="sxs-lookup"><span data-stu-id="f55fb-118">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```md
This text is *italic*.
```

<span data-ttu-id="f55fb-119">若要將文字格式設定為***粗體且斜體***，請使用三個星號將它括住：</span><span class="sxs-lookup"><span data-stu-id="f55fb-119">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```md
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="f55fb-120">區塊引述</span><span class="sxs-lookup"><span data-stu-id="f55fb-120">Blockquotes</span></span>

<span data-ttu-id="f55fb-121">區塊引述使用 `>` 字元建立：</span><span class="sxs-lookup"><span data-stu-id="f55fb-121">Blockquotes are created using the `>` character:</span></span>

```md
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="f55fb-122">前述範例會如下呈現：</span><span class="sxs-lookup"><span data-stu-id="f55fb-122">The preceding example renders as follows:</span></span>

> <span data-ttu-id="f55fb-123">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span><span class="sxs-lookup"><span data-stu-id="f55fb-123">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="f55fb-124">此處，在赤道上，在有朝一日稱為非洲的大陸上，生存之戰已來到激烈的最高潮，而勝利者尚未現身。</span><span class="sxs-lookup"><span data-stu-id="f55fb-124">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="f55fb-125">在這片荒蕪乾燥的土地上，只有小型、迅速或兇猛的物體，才能繁榮昌盛，抑或抱有生存下去的希望。</span><span class="sxs-lookup"><span data-stu-id="f55fb-125">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="f55fb-126">清單</span><span class="sxs-lookup"><span data-stu-id="f55fb-126">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="f55fb-127">未排序清單</span><span class="sxs-lookup"><span data-stu-id="f55fb-127">Unordered list</span></span>

<span data-ttu-id="f55fb-128">若要設定不排序/項目符號清單的格式，請使用星號或短破折號。</span><span class="sxs-lookup"><span data-stu-id="f55fb-128">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="f55fb-129">例如，下列 Markdown：</span><span class="sxs-lookup"><span data-stu-id="f55fb-129">For example, the following Markdown:</span></span>

```md
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="f55fb-130">將會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="f55fb-130">will be rendered as:</span></span>

- <span data-ttu-id="f55fb-131">List item 1</span><span class="sxs-lookup"><span data-stu-id="f55fb-131">List item 1</span></span>
- <span data-ttu-id="f55fb-132">List item 2</span><span class="sxs-lookup"><span data-stu-id="f55fb-132">List item 2</span></span>
- <span data-ttu-id="f55fb-133">List item 3</span><span class="sxs-lookup"><span data-stu-id="f55fb-133">List item 3</span></span>

<span data-ttu-id="f55fb-134">若要建立包含在另一個清單中的巢狀清單，請將子清單項目縮排。</span><span class="sxs-lookup"><span data-stu-id="f55fb-134">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="f55fb-135">例如，下列 Markdown：</span><span class="sxs-lookup"><span data-stu-id="f55fb-135">For example, the following Markdown:</span></span>

```md
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="f55fb-136">將會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="f55fb-136">will be rendered as:</span></span>

- <span data-ttu-id="f55fb-137">List item 1</span><span class="sxs-lookup"><span data-stu-id="f55fb-137">List item 1</span></span>
  - <span data-ttu-id="f55fb-138">List item A</span><span class="sxs-lookup"><span data-stu-id="f55fb-138">List item A</span></span>
  - <span data-ttu-id="f55fb-139">List item B</span><span class="sxs-lookup"><span data-stu-id="f55fb-139">List item B</span></span>
- <span data-ttu-id="f55fb-140">List item 2</span><span class="sxs-lookup"><span data-stu-id="f55fb-140">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="f55fb-141">已排序清單</span><span class="sxs-lookup"><span data-stu-id="f55fb-141">Ordered list</span></span>

<span data-ttu-id="f55fb-142">若要設定已排序/逐步清單的格式，請使用對應的數字。</span><span class="sxs-lookup"><span data-stu-id="f55fb-142">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="f55fb-143">例如，下列 Markdown：</span><span class="sxs-lookup"><span data-stu-id="f55fb-143">For example, the following Markdown:</span></span>

```md
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="f55fb-144">將會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="f55fb-144">will be rendered as:</span></span>

1. <span data-ttu-id="f55fb-145">First instruction</span><span class="sxs-lookup"><span data-stu-id="f55fb-145">First instruction</span></span>
2. <span data-ttu-id="f55fb-146">Second instruction</span><span class="sxs-lookup"><span data-stu-id="f55fb-146">Second instruction</span></span>
3. <span data-ttu-id="f55fb-147">Third instruction</span><span class="sxs-lookup"><span data-stu-id="f55fb-147">Third instruction</span></span>

<span data-ttu-id="f55fb-148">若要建立包含在另一個清單中的巢狀清單，請將子清單項目縮排。</span><span class="sxs-lookup"><span data-stu-id="f55fb-148">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="f55fb-149">例如，下列 Markdown：</span><span class="sxs-lookup"><span data-stu-id="f55fb-149">For example, the following Markdown:</span></span>

```md
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="f55fb-150">將會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="f55fb-150">will be rendered as:</span></span>

1. <span data-ttu-id="f55fb-151">First instruction</span><span class="sxs-lookup"><span data-stu-id="f55fb-151">First instruction</span></span>
   1. <span data-ttu-id="f55fb-152">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="f55fb-152">Sub-instruction</span></span>
   2. <span data-ttu-id="f55fb-153">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="f55fb-153">Sub-instruction</span></span>
2. <span data-ttu-id="f55fb-154">Second instruction</span><span class="sxs-lookup"><span data-stu-id="f55fb-154">Second instruction</span></span>

<span data-ttu-id="f55fb-155">請注意，針對所有項目我們</span><span class="sxs-lookup"><span data-stu-id="f55fb-155">Note that we use '1.'</span></span> <span data-ttu-id="f55fb-156">均使用 '1'。</span><span class="sxs-lookup"><span data-stu-id="f55fb-156">for all entries.</span></span> <span data-ttu-id="f55fb-157">這樣，當未來的更新包含新步驟或刪除現有步驟時，就能更輕鬆的檢閱差異。</span><span class="sxs-lookup"><span data-stu-id="f55fb-157">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="f55fb-158">Tables</span><span class="sxs-lookup"><span data-stu-id="f55fb-158">Tables</span></span>

<span data-ttu-id="f55fb-159">表格不是核心 Markdown 規格的一部分，但是 GFM 支援表格。</span><span class="sxs-lookup"><span data-stu-id="f55fb-159">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="f55fb-160">您可以使用管線 (|) 和連字號 (-) 字元來建立表格。</span><span class="sxs-lookup"><span data-stu-id="f55fb-160">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="f55fb-161">連字號是用來建立每一欄的標頭，而管線是用來分隔每一欄。</span><span class="sxs-lookup"><span data-stu-id="f55fb-161">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="f55fb-162">請在您的表格之前包含一個空白行，這樣才能正確轉譯。</span><span class="sxs-lookup"><span data-stu-id="f55fb-162">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="f55fb-163">例如，下列 Markdown：</span><span class="sxs-lookup"><span data-stu-id="f55fb-163">For example, the following Markdown:</span></span>

```md
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="f55fb-164">將會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="f55fb-164">Will be rendered as:</span></span>

| <span data-ttu-id="f55fb-165">Fun</span><span class="sxs-lookup"><span data-stu-id="f55fb-165">Fun</span></span>                  | <span data-ttu-id="f55fb-166">With</span><span class="sxs-lookup"><span data-stu-id="f55fb-166">With</span></span>                 | <span data-ttu-id="f55fb-167">Tables</span><span class="sxs-lookup"><span data-stu-id="f55fb-167">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="f55fb-168">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="f55fb-168">left-aligned column</span></span>  | <span data-ttu-id="f55fb-169">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="f55fb-169">right-aligned column</span></span> | <span data-ttu-id="f55fb-170">centered column</span><span class="sxs-lookup"><span data-stu-id="f55fb-170">centered column</span></span> |
| <span data-ttu-id="f55fb-171">$100</span><span class="sxs-lookup"><span data-stu-id="f55fb-171">$100</span></span>                 | <span data-ttu-id="f55fb-172">$100</span><span class="sxs-lookup"><span data-stu-id="f55fb-172">$100</span></span>                 | <span data-ttu-id="f55fb-173">$100</span><span class="sxs-lookup"><span data-stu-id="f55fb-173">$100</span></span>            |
| <span data-ttu-id="f55fb-174">$10</span><span class="sxs-lookup"><span data-stu-id="f55fb-174">$10</span></span>                  | <span data-ttu-id="f55fb-175">$10</span><span class="sxs-lookup"><span data-stu-id="f55fb-175">$10</span></span>                  | <span data-ttu-id="f55fb-176">$10</span><span class="sxs-lookup"><span data-stu-id="f55fb-176">$10</span></span>             |
| <span data-ttu-id="f55fb-177">$1</span><span class="sxs-lookup"><span data-stu-id="f55fb-177">$1</span></span>                   | <span data-ttu-id="f55fb-178">$1</span><span class="sxs-lookup"><span data-stu-id="f55fb-178">$1</span></span>                   | <span data-ttu-id="f55fb-179">$1</span><span class="sxs-lookup"><span data-stu-id="f55fb-179">$1</span></span>              |

<span data-ttu-id="f55fb-180">如需有關如何建立表格的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="f55fb-180">For more information on creating tables, see:</span></span>

- <span data-ttu-id="f55fb-181">GitHub 的 [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/) (使用表格組織資訊)。</span><span class="sxs-lookup"><span data-stu-id="f55fb-181">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="f55fb-182">[Markdown 表格產生器](https://www.tablesgenerator.com/markdown_tables) Web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="f55fb-182">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="f55fb-183">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables) (Adam Pritchard 的 Markdown 速查表)。</span><span class="sxs-lookup"><span data-stu-id="f55fb-183">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="f55fb-184">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table) (Michel Fortin 的 Markdown Extra)。</span><span class="sxs-lookup"><span data-stu-id="f55fb-184">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="f55fb-185">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/) (將 HTML 表格轉換為 Markdown)。</span><span class="sxs-lookup"><span data-stu-id="f55fb-185">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="f55fb-186">連結</span><span class="sxs-lookup"><span data-stu-id="f55fb-186">Links</span></span>

<span data-ttu-id="f55fb-187">內嵌連結的 Markdown 語法是由超連結文字 `[link text]` 部分，以及緊接在後面的連結 URL 或檔案名稱 `(file-name.md)` 部分所組成：</span><span class="sxs-lookup"><span data-stu-id="f55fb-187">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="f55fb-188">如需連結的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="f55fb-188">For more information on linking, see:</span></span>

- <span data-ttu-id="f55fb-189">[Markdown 語法指南](https://daringfireball.net/projects/markdown/syntax#link) 的 Markdown 基礎連結支援。</span><span class="sxs-lookup"><span data-stu-id="f55fb-189">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="f55fb-190">本指南的[連結](how-to-write-links.md)一節，有 Markdig 提供的額外連結語法詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f55fb-190">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="f55fb-191">程式碼片段</span><span class="sxs-lookup"><span data-stu-id="f55fb-191">Code snippets</span></span>

<span data-ttu-id="f55fb-192">Markdown 支援將程式碼片段內嵌在句子中，或是在句子之間形成個別圍住的區塊。</span><span class="sxs-lookup"><span data-stu-id="f55fb-192">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="f55fb-193">如需詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="f55fb-193">For details, see:</span></span>

- <span data-ttu-id="f55fb-194">[Markdown 的程式碼區塊原生支援](https://daringfireball.net/projects/markdown/syntax#precode) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="f55fb-194">[Markdown's native support for code blocks](https://daringfireball.net/projects/markdown/syntax#precode)</span></span>
- <span data-ttu-id="f55fb-195">[GFM 對程式碼包圍和語法醒目提示的支援](https://help.github.com/articles/creating-and-highlighting-code-blocks/) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="f55fb-195">[GFM support for code fencing and syntax highlighting](https://help.github.com/articles/creating-and-highlighting-code-blocks/)</span></span>

<span data-ttu-id="f55fb-196">圍住的程式碼區塊是對程式碼片段支援語法醒目提示的簡單方式。</span><span class="sxs-lookup"><span data-stu-id="f55fb-196">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="f55fb-197">圍住的程式碼區塊的一般格式為：</span><span class="sxs-lookup"><span data-stu-id="f55fb-197">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="f55fb-198">前三個倒引號 (\`) 字元之後的別名定義所要使用語法醒目提示。</span><span class="sxs-lookup"><span data-stu-id="f55fb-198">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="f55fb-199">下列清單是 Docs 內容中常用的程式設計語言與對應的標籤：</span><span class="sxs-lookup"><span data-stu-id="f55fb-199">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="f55fb-200">這些語言包含易記名稱支援，且大部分都具有語言反白顯示。</span><span class="sxs-lookup"><span data-stu-id="f55fb-200">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="f55fb-201">Name</span><span class="sxs-lookup"><span data-stu-id="f55fb-201">Name</span></span>|<span data-ttu-id="f55fb-202">Markdown 標籤</span><span class="sxs-lookup"><span data-stu-id="f55fb-202">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="f55fb-203">.NET 主控台</span><span class="sxs-lookup"><span data-stu-id="f55fb-203">.NET Console</span></span>|<span data-ttu-id="f55fb-204">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="f55fb-204">dotnetcli</span></span>|
|<span data-ttu-id="f55fb-205">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="f55fb-205">ASP.NET (C#)</span></span>|<span data-ttu-id="f55fb-206">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="f55fb-206">aspx-csharp</span></span>|
|<span data-ttu-id="f55fb-207">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="f55fb-207">ASP.NET (VB)</span></span>|<span data-ttu-id="f55fb-208">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="f55fb-208">aspx-vb</span></span>|
|<span data-ttu-id="f55fb-209">AzCopy</span><span class="sxs-lookup"><span data-stu-id="f55fb-209">AzCopy</span></span>|<span data-ttu-id="f55fb-210">azcopy</span><span class="sxs-lookup"><span data-stu-id="f55fb-210">azcopy</span></span>|
|<span data-ttu-id="f55fb-211">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="f55fb-211">Azure CLI</span></span>|<span data-ttu-id="f55fb-212">azurecli</span><span class="sxs-lookup"><span data-stu-id="f55fb-212">azurecli</span></span>|
|<span data-ttu-id="f55fb-213">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f55fb-213">Azure PowerShell</span></span>|<span data-ttu-id="f55fb-214">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="f55fb-214">azurepowershell</span></span>|
|<span data-ttu-id="f55fb-215">Bash</span><span class="sxs-lookup"><span data-stu-id="f55fb-215">Bash</span></span>|<span data-ttu-id="f55fb-216">bash</span><span class="sxs-lookup"><span data-stu-id="f55fb-216">bash</span></span>|
|<span data-ttu-id="f55fb-217">C++</span><span class="sxs-lookup"><span data-stu-id="f55fb-217">C++</span></span>|<span data-ttu-id="f55fb-218">cpp</span><span class="sxs-lookup"><span data-stu-id="f55fb-218">cpp</span></span>|
|<span data-ttu-id="f55fb-219">C++/CX</span><span class="sxs-lookup"><span data-stu-id="f55fb-219">C++/CX</span></span>|<span data-ttu-id="f55fb-220">cppcx</span><span class="sxs-lookup"><span data-stu-id="f55fb-220">cppcx</span></span>|
|<span data-ttu-id="f55fb-221">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="f55fb-221">C++/WinRT</span></span>|<span data-ttu-id="f55fb-222">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="f55fb-222">cppwinrt</span></span>|
|<span data-ttu-id="f55fb-223">C#</span><span class="sxs-lookup"><span data-stu-id="f55fb-223">C#</span></span>|<span data-ttu-id="f55fb-224">csharp</span><span class="sxs-lookup"><span data-stu-id="f55fb-224">csharp</span></span>|
|<span data-ttu-id="f55fb-225">網頁瀏覽器中的 C#</span><span class="sxs-lookup"><span data-stu-id="f55fb-225">C# in browser</span></span>|<span data-ttu-id="f55fb-226">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="f55fb-226">csharp-interactive</span></span>|
|<span data-ttu-id="f55fb-227">主控台</span><span class="sxs-lookup"><span data-stu-id="f55fb-227">Console</span></span>|<span data-ttu-id="f55fb-228">主控台</span><span class="sxs-lookup"><span data-stu-id="f55fb-228">console</span></span>|
|<span data-ttu-id="f55fb-229">CSHTML</span><span class="sxs-lookup"><span data-stu-id="f55fb-229">CSHTML</span></span>|<span data-ttu-id="f55fb-230">cshtml</span><span class="sxs-lookup"><span data-stu-id="f55fb-230">cshtml</span></span>|
|<span data-ttu-id="f55fb-231">DAX</span><span class="sxs-lookup"><span data-stu-id="f55fb-231">DAX</span></span>|<span data-ttu-id="f55fb-232">dax</span><span class="sxs-lookup"><span data-stu-id="f55fb-232">dax</span></span>|
|<span data-ttu-id="f55fb-233">Docker</span><span class="sxs-lookup"><span data-stu-id="f55fb-233">Docker</span></span>|<span data-ttu-id="f55fb-234">dockerfile</span><span class="sxs-lookup"><span data-stu-id="f55fb-234">dockerfile</span></span>|
|<span data-ttu-id="f55fb-235">F#</span><span class="sxs-lookup"><span data-stu-id="f55fb-235">F#</span></span>|<span data-ttu-id="f55fb-236">fsharp</span><span class="sxs-lookup"><span data-stu-id="f55fb-236">fsharp</span></span>|
|<span data-ttu-id="f55fb-237">Go</span><span class="sxs-lookup"><span data-stu-id="f55fb-237">Go</span></span>|<span data-ttu-id="f55fb-238">go</span><span class="sxs-lookup"><span data-stu-id="f55fb-238">go</span></span>|
|<span data-ttu-id="f55fb-239">HTML</span><span class="sxs-lookup"><span data-stu-id="f55fb-239">HTML</span></span>|<span data-ttu-id="f55fb-240">html</span><span class="sxs-lookup"><span data-stu-id="f55fb-240">html</span></span>|
|<span data-ttu-id="f55fb-241">HTTP</span><span class="sxs-lookup"><span data-stu-id="f55fb-241">HTTP</span></span>|<span data-ttu-id="f55fb-242">http</span><span class="sxs-lookup"><span data-stu-id="f55fb-242">http</span></span>|
|<span data-ttu-id="f55fb-243">Java</span><span class="sxs-lookup"><span data-stu-id="f55fb-243">Java</span></span>|<span data-ttu-id="f55fb-244">java</span><span class="sxs-lookup"><span data-stu-id="f55fb-244">java</span></span>|
|<span data-ttu-id="f55fb-245">JavaScript</span><span class="sxs-lookup"><span data-stu-id="f55fb-245">JavaScript</span></span>|<span data-ttu-id="f55fb-246">javascript</span><span class="sxs-lookup"><span data-stu-id="f55fb-246">javascript</span></span>|
|<span data-ttu-id="f55fb-247">JSON</span><span class="sxs-lookup"><span data-stu-id="f55fb-247">JSON</span></span>|<span data-ttu-id="f55fb-248">json</span><span class="sxs-lookup"><span data-stu-id="f55fb-248">json</span></span>|
|<span data-ttu-id="f55fb-249">Kusto 查詢語言</span><span class="sxs-lookup"><span data-stu-id="f55fb-249">Kusto Query Language</span></span>|<span data-ttu-id="f55fb-250">kusto</span><span class="sxs-lookup"><span data-stu-id="f55fb-250">kusto</span></span>|
|<span data-ttu-id="f55fb-251">Markdown</span><span class="sxs-lookup"><span data-stu-id="f55fb-251">Markdown</span></span>|<span data-ttu-id="f55fb-252">md</span><span class="sxs-lookup"><span data-stu-id="f55fb-252">md</span></span>|
|<span data-ttu-id="f55fb-253">Objective-C</span><span class="sxs-lookup"><span data-stu-id="f55fb-253">Objective-C</span></span>|<span data-ttu-id="f55fb-254">objc</span><span class="sxs-lookup"><span data-stu-id="f55fb-254">objc</span></span>|
|<span data-ttu-id="f55fb-255">OData</span><span class="sxs-lookup"><span data-stu-id="f55fb-255">OData</span></span>|<span data-ttu-id="f55fb-256">odata</span><span class="sxs-lookup"><span data-stu-id="f55fb-256">odata</span></span>|
|<span data-ttu-id="f55fb-257">PHP</span><span class="sxs-lookup"><span data-stu-id="f55fb-257">PHP</span></span>|<span data-ttu-id="f55fb-258">php</span><span class="sxs-lookup"><span data-stu-id="f55fb-258">php</span></span>|
|<span data-ttu-id="f55fb-259">protobuf</span><span class="sxs-lookup"><span data-stu-id="f55fb-259">protobuf</span></span>|<span data-ttu-id="f55fb-260">protobuf</span><span class="sxs-lookup"><span data-stu-id="f55fb-260">protobuf</span></span>|
|<span data-ttu-id="f55fb-261">PowerApps (小數點小數分隔符號)</span><span class="sxs-lookup"><span data-stu-id="f55fb-261">PowerApps (dot decimal separator)</span></span>|<span data-ttu-id="f55fb-262">powerapps-dot</span><span class="sxs-lookup"><span data-stu-id="f55fb-262">powerapps-dot</span></span>|
|<span data-ttu-id="f55fb-263">PowerApps (逗點小數分隔符號)</span><span class="sxs-lookup"><span data-stu-id="f55fb-263">PowerApps (comma decimal separator)</span></span>|<span data-ttu-id="f55fb-264">powerapps-comma</span><span class="sxs-lookup"><span data-stu-id="f55fb-264">powerapps-comma</span></span>|
|<span data-ttu-id="f55fb-265">PowerShell</span><span class="sxs-lookup"><span data-stu-id="f55fb-265">PowerShell</span></span>|<span data-ttu-id="f55fb-266">powershell</span><span class="sxs-lookup"><span data-stu-id="f55fb-266">powershell</span></span>|
|<span data-ttu-id="f55fb-267">Python</span><span class="sxs-lookup"><span data-stu-id="f55fb-267">Python</span></span>|<span data-ttu-id="f55fb-268">python</span><span class="sxs-lookup"><span data-stu-id="f55fb-268">python</span></span>|
|<span data-ttu-id="f55fb-269">Q#</span><span class="sxs-lookup"><span data-stu-id="f55fb-269">Q#</span></span>|<span data-ttu-id="f55fb-270">qsharp</span><span class="sxs-lookup"><span data-stu-id="f55fb-270">qsharp</span></span>|
|<span data-ttu-id="f55fb-271">R</span><span class="sxs-lookup"><span data-stu-id="f55fb-271">R</span></span>|<span data-ttu-id="f55fb-272">r</span><span class="sxs-lookup"><span data-stu-id="f55fb-272">r</span></span>|
|<span data-ttu-id="f55fb-273">Ruby</span><span class="sxs-lookup"><span data-stu-id="f55fb-273">Ruby</span></span>|<span data-ttu-id="f55fb-274">ruby</span><span class="sxs-lookup"><span data-stu-id="f55fb-274">ruby</span></span>|
|<span data-ttu-id="f55fb-275">SQL</span><span class="sxs-lookup"><span data-stu-id="f55fb-275">SQL</span></span>|<span data-ttu-id="f55fb-276">sql</span><span class="sxs-lookup"><span data-stu-id="f55fb-276">sql</span></span>|
|<span data-ttu-id="f55fb-277">Swift</span><span class="sxs-lookup"><span data-stu-id="f55fb-277">Swift</span></span>|<span data-ttu-id="f55fb-278">swift</span><span class="sxs-lookup"><span data-stu-id="f55fb-278">swift</span></span>|
|<span data-ttu-id="f55fb-279">TypeScript</span><span class="sxs-lookup"><span data-stu-id="f55fb-279">TypeScript</span></span>|<span data-ttu-id="f55fb-280">typescript</span><span class="sxs-lookup"><span data-stu-id="f55fb-280">typescript</span></span>|
|<span data-ttu-id="f55fb-281">VB</span><span class="sxs-lookup"><span data-stu-id="f55fb-281">VB</span></span>|<span data-ttu-id="f55fb-282">vb</span><span class="sxs-lookup"><span data-stu-id="f55fb-282">vb</span></span>|
|<span data-ttu-id="f55fb-283">XAML</span><span class="sxs-lookup"><span data-stu-id="f55fb-283">XAML</span></span>|<span data-ttu-id="f55fb-284">xaml</span><span class="sxs-lookup"><span data-stu-id="f55fb-284">xaml</span></span>|
|<span data-ttu-id="f55fb-285">XML</span><span class="sxs-lookup"><span data-stu-id="f55fb-285">XML</span></span>|<span data-ttu-id="f55fb-286">xml</span><span class="sxs-lookup"><span data-stu-id="f55fb-286">xml</span></span>|

<span data-ttu-id="f55fb-287">`csharp-interactive` 名稱會指定 C# 語言，並指定在瀏覽器執行範例的能力。</span><span class="sxs-lookup"><span data-stu-id="f55fb-287">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="f55fb-288">這些程式碼片段會在 Docker 容器中編譯和執行，且程式執行的結果會顯示在使用者的瀏覽器視窗中。</span><span class="sxs-lookup"><span data-stu-id="f55fb-288">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="f55fb-289">範例：C\#</span><span class="sxs-lookup"><span data-stu-id="f55fb-289">Example: C\#</span></span>

<span data-ttu-id="f55fb-290">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="f55fb-290">__Markdown__</span></span>

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

<span data-ttu-id="f55fb-291">__轉譯器__</span><span class="sxs-lookup"><span data-stu-id="f55fb-291">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="f55fb-292">範例：SQL</span><span class="sxs-lookup"><span data-stu-id="f55fb-292">Example: SQL</span></span>

<span data-ttu-id="f55fb-293">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="f55fb-293">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="f55fb-294">__轉譯器__</span><span class="sxs-lookup"><span data-stu-id="f55fb-294">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="docs-custom-markdown-extensions"></a><span data-ttu-id="f55fb-295">Docs 自訂 Markdown 延伸模組</span><span class="sxs-lookup"><span data-stu-id="f55fb-295">Docs custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="f55fb-296">Docs.Microsoft.com (Docs) 會實作用於 Markdown 的 Markdig 剖析器，這與 GitHub 適用的 Markdown (GFM) 高度相容。</span><span class="sxs-lookup"><span data-stu-id="f55fb-296">Docs.Microsoft.com (Docs) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="f55fb-297">Markdig 透過 Markdown 擴充新增了一些功能。</span><span class="sxs-lookup"><span data-stu-id="f55fb-297">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="f55fb-298">就真正的意義來說，從完整《OPS 撰寫指南》選取的文章包含在此指南中供參考</span><span class="sxs-lookup"><span data-stu-id="f55fb-298">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="f55fb-299">(例如，請參閱目錄中的＜Markdig 與 Markdown 擴充＞和＜程式碼片段＞)。</span><span class="sxs-lookup"><span data-stu-id="f55fb-299">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="f55fb-300">Docs 文章使用 GFM 來設定大部分的文章格式 (例如段落、連結、清單與標題)。</span><span class="sxs-lookup"><span data-stu-id="f55fb-300">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="f55fb-301">如需更豐富的格式設定，文章可以使用 Markdig 功能，例如：</span><span class="sxs-lookup"><span data-stu-id="f55fb-301">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="f55fb-302">注意事項區塊</span><span class="sxs-lookup"><span data-stu-id="f55fb-302">Note blocks</span></span>
- <span data-ttu-id="f55fb-303">Include 檔案</span><span class="sxs-lookup"><span data-stu-id="f55fb-303">Include files</span></span>
- <span data-ttu-id="f55fb-304">選取器</span><span class="sxs-lookup"><span data-stu-id="f55fb-304">Selectors</span></span>
- <span data-ttu-id="f55fb-305">內嵌影片</span><span class="sxs-lookup"><span data-stu-id="f55fb-305">Embedded videos</span></span>
- <span data-ttu-id="f55fb-306">程式碼片段/範例</span><span class="sxs-lookup"><span data-stu-id="f55fb-306">Code snippets/samples</span></span>

<span data-ttu-id="f55fb-307">如需完整清單，請參閱目錄中的＜Markdig 與 Markdown 擴充＞和＜程式碼片段＞。</span><span class="sxs-lookup"><span data-stu-id="f55fb-307">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="f55fb-308">注意事項區塊</span><span class="sxs-lookup"><span data-stu-id="f55fb-308">Note blocks</span></span>

<span data-ttu-id="f55fb-309">有四種類型的注意事項區塊可供您選擇用來強調特定內容：</span><span class="sxs-lookup"><span data-stu-id="f55fb-309">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="f55fb-310">注意</span><span class="sxs-lookup"><span data-stu-id="f55fb-310">NOTE</span></span>
- <span data-ttu-id="f55fb-311">警告</span><span class="sxs-lookup"><span data-stu-id="f55fb-311">WARNING</span></span>
- <span data-ttu-id="f55fb-312">祕訣</span><span class="sxs-lookup"><span data-stu-id="f55fb-312">TIP</span></span>
- <span data-ttu-id="f55fb-313">重要</span><span class="sxs-lookup"><span data-stu-id="f55fb-313">IMPORTANT</span></span>

<span data-ttu-id="f55fb-314">在一般情況下，應該謹慎使用注意事項區塊，因為它們可能會造成干擾。</span><span class="sxs-lookup"><span data-stu-id="f55fb-314">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="f55fb-315">雖然注意事項區塊也支援程式碼區塊、影像、清單和連結，但請盡量讓它們保持簡單明瞭。</span><span class="sxs-lookup"><span data-stu-id="f55fb-315">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="f55fb-316">範例：</span><span class="sxs-lookup"><span data-stu-id="f55fb-316">Examples:</span></span>

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

<span data-ttu-id="f55fb-317">這些警示在 docs.microsoft.com 中看起來像這樣：</span><span class="sxs-lookup"><span data-stu-id="f55fb-317">These alerts look like this on docs.microsoft.com:</span></span>

![顯示上一個範例中的警示在發佈的 Docs 頁面如何呈現出不同的圖示與色彩](media/alerts-rendering.png)

### <a name="include-files"></a><span data-ttu-id="f55fb-319">Include 檔案</span><span class="sxs-lookup"><span data-stu-id="f55fb-319">Include files</span></span>

<span data-ttu-id="f55fb-320">當您有可重複使用且需要包含在文章檔案中的文字或影像檔時，可以透過 Markdig 檔案的包含功能，使用「包含」檔案的參考。</span><span class="sxs-lookup"><span data-stu-id="f55fb-320">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="f55fb-321">此功能會指示 OPS 在建置階段將指定的檔案包含到文章檔案中，成為發行文章的一部分。</span><span class="sxs-lookup"><span data-stu-id="f55fb-321">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="f55fb-322">有三種類型的 Include 參考可協助您重複使用內容：</span><span class="sxs-lookup"><span data-stu-id="f55fb-322">Three types of include references are available to help you reuse content:</span></span>

- <span data-ttu-id="f55fb-323">內嵌：在另一個句子中重複使用常用程式碼片段內嵌。</span><span class="sxs-lookup"><span data-stu-id="f55fb-323">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="f55fb-324">區塊：您重複使用整個 Markdown 檔案作為區塊 (巢狀嵌入文章中的小節)。</span><span class="sxs-lookup"><span data-stu-id="f55fb-324">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="f55fb-325">影像：這是 Docs 中實作標準影像包含的方式。</span><span class="sxs-lookup"><span data-stu-id="f55fb-325">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="f55fb-326">內嵌或區塊 Include 檔案都只是簡單的 Markdown (.md) 檔案。</span><span class="sxs-lookup"><span data-stu-id="f55fb-326">An inline or block include file is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="f55fb-327">它可以包含任何有效的 Markdown。</span><span class="sxs-lookup"><span data-stu-id="f55fb-327">It can contain any valid Markdown.</span></span> <span data-ttu-id="f55fb-328">所有的包含 Markdown 檔案都應放在存放庫根目錄中的[一般 `/includes` 子目錄](git-github-fundamentals.md#includes-subdirectory)。</span><span class="sxs-lookup"><span data-stu-id="f55fb-328">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="f55fb-329">當文章發行之後，包含的檔案會直接整合到其中。</span><span class="sxs-lookup"><span data-stu-id="f55fb-329">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="f55fb-330">以下是 Include 檔案的需求與考量：</span><span class="sxs-lookup"><span data-stu-id="f55fb-330">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="f55fb-331">當您需要相同的文字出現在多篇文章中時，就可以使用 Include 檔案。</span><span class="sxs-lookup"><span data-stu-id="f55fb-331">Use an include file whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="f55fb-332">針對大量內容 (例如一兩個段落、共用的程序或共用的節) 使用區塊 Include 參考。</span><span class="sxs-lookup"><span data-stu-id="f55fb-332">Use a block include reference for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="f55fb-333">請勿將它們用在小於一個句子的內容。</span><span class="sxs-lookup"><span data-stu-id="f55fb-333">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="f55fb-334">因為檔案相依於 Markdig 延伸，所以不會在文章的 GitHub 轉譯檢視中轉譯 Include 參考。</span><span class="sxs-lookup"><span data-stu-id="f55fb-334">Include references won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="f55fb-335">它們將會在發行集之後才轉譯。</span><span class="sxs-lookup"><span data-stu-id="f55fb-335">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="f55fb-336">請務必將 Include 檔案中的文字撰寫成完整的句子或片語，且不相依於參考 Include 檔案之文章中的上下文。</span><span class="sxs-lookup"><span data-stu-id="f55fb-336">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include file.</span></span> <span data-ttu-id="f55fb-337">忽略此指導方針會使文章中產生無法翻譯的字串，進而影響本地化體驗。</span><span class="sxs-lookup"><span data-stu-id="f55fb-337">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="f55fb-338">請勿將 Include 參考嵌入其他 Include 檔案中。</span><span class="sxs-lookup"><span data-stu-id="f55fb-338">Don't embed include references within other include files.</span></span> <span data-ttu-id="f55fb-339">不支援此使用方式。</span><span class="sxs-lookup"><span data-stu-id="f55fb-339">They are not supported.</span></span>
- <span data-ttu-id="f55fb-340">將媒體檔案放在包含資料夾的特定 [media] 資料夾中，例如 `<repo>`/includes/media 資料夾。</span><span class="sxs-lookup"><span data-stu-id="f55fb-340">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="f55fb-341">[media] 目錄的根目錄中不應包含任何影像。</span><span class="sxs-lookup"><span data-stu-id="f55fb-341">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="f55fb-342">如果 Include 檔案沒有影像，則不需要對應的媒體目錄。</span><span class="sxs-lookup"><span data-stu-id="f55fb-342">If the include file does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="f55fb-343">對於一般文章，請勿在不同包含檔案之間共用媒體。</span><span class="sxs-lookup"><span data-stu-id="f55fb-343">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="f55fb-344">請針對每個 Include 檔案和文章，使用具有唯一名稱的個別檔案。</span><span class="sxs-lookup"><span data-stu-id="f55fb-344">Use a separate file with a unique name for each include file and article.</span></span> <span data-ttu-id="f55fb-345">將媒體檔案儲存在與該 Include 檔案相關聯的媒體資料夾。</span><span class="sxs-lookup"><span data-stu-id="f55fb-345">Store the media file in the media folder that's associated with the include file.</span></span>
- <span data-ttu-id="f55fb-346">請勿將 Include 檔案用作文章的唯一內容。</span><span class="sxs-lookup"><span data-stu-id="f55fb-346">Don't use an include file as the only content of an article.</span></span>  <span data-ttu-id="f55fb-347">Include 檔案的設計目的是補充文章其他部分中的內容。</span><span class="sxs-lookup"><span data-stu-id="f55fb-347">Include files are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="f55fb-348">範例：</span><span class="sxs-lookup"><span data-stu-id="f55fb-348">Example:</span></span>

```md
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="f55fb-349">選取器</span><span class="sxs-lookup"><span data-stu-id="f55fb-349">Selectors</span></span>

<span data-ttu-id="f55fb-350">當您撰寫同一篇技術文章的不同版本時，可以使用選取器，以滿足跨技術或平台的實作差異。</span><span class="sxs-lookup"><span data-stu-id="f55fb-350">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="f55fb-351">一般而言，此功能非常適合開發人員的行動平台內容。</span><span class="sxs-lookup"><span data-stu-id="f55fb-351">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="f55fb-352">Markdig 中目前有兩種不同類型的選取器：單一選取器和多重選取器。</span><span class="sxs-lookup"><span data-stu-id="f55fb-352">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="f55fb-353">因為相同的選擇器 Markdown 會進入選取範圍的每個文章中，我們建議您將文章的選擇器放在 Include 檔案中。</span><span class="sxs-lookup"><span data-stu-id="f55fb-353">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="f55fb-354">接著，您可以在您使用相同選擇器的所有文章中參考該 Include 檔案。</span><span class="sxs-lookup"><span data-stu-id="f55fb-354">Then you can reference that include file in all your articles that use the same selector.</span></span>

<span data-ttu-id="f55fb-355">下圖顯示範例選取器：</span><span class="sxs-lookup"><span data-stu-id="f55fb-355">The following shows an example selector:</span></span>

```md
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="f55fb-356">您可以在 [Azure 文件](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic)中查看選取器的範例。</span><span class="sxs-lookup"><span data-stu-id="f55fb-356">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-include-references"></a><span data-ttu-id="f55fb-357">程式碼 Include 參考</span><span class="sxs-lookup"><span data-stu-id="f55fb-357">Code include references</span></span>

<span data-ttu-id="f55fb-358">Docs 程式碼片段 Markdown 延伸模組可讓您將程式碼範例內嵌在文章中，並使用語言特定的語法著色來呈現程式碼。</span><span class="sxs-lookup"><span data-stu-id="f55fb-358">The Docs code snippet Markdown extension allows you to embed code samples in your articles and render them with language-specific syntax coloring.</span></span> <span data-ttu-id="f55fb-359">您可以包含來自目前存放庫或其他存放庫的程式碼。</span><span class="sxs-lookup"><span data-stu-id="f55fb-359">You can include code from either the current repository or another repository.</span></span> <span data-ttu-id="f55fb-360">下列指示會提供如何使用功能搭配 [docs.microsoft.com 撰寫套件](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)的總覽。</span><span class="sxs-lookup"><span data-stu-id="f55fb-360">The instructions below provides an overview of how to use the feature with the [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).</span></span> <span data-ttu-id="f55fb-361">在 Visual Studio Code 中，您可以開啟 [預覽]  以預覽程式碼片段。</span><span class="sxs-lookup"><span data-stu-id="f55fb-361">In Visual Studio Code, you can preview the code snippets by opening **Preview**.</span></span> <span data-ttu-id="f55fb-362">預覽不提供醒目提示和互動功能。</span><span class="sxs-lookup"><span data-stu-id="f55fb-362">Highlighting and interactivity are not available in preview.</span></span>

> [!NOTE]
> <span data-ttu-id="f55fb-363">延伸模組不支援在內嵌中包含程式碼內容 – 這必須透過標準的 triple-tick Markdown 代碼標記慣例完成。</span><span class="sxs-lookup"><span data-stu-id="f55fb-363">The extension does not support including code content within it inline – this is to be done through the standard triple-tick Markdown convention.</span></span>

#### <a name="code-from-current-repository"></a><span data-ttu-id="f55fb-364">目前存放庫中的程式碼</span><span class="sxs-lookup"><span data-stu-id="f55fb-364">Code from current repository</span></span>

1. <span data-ttu-id="f55fb-365">在 Visual Studio Code 中，按一下 **Alt + M** 或 **選項 + M**，然後選取 [程式碼片段]。</span><span class="sxs-lookup"><span data-stu-id="f55fb-365">In Visual Studio Code, click **Alt + M** or **Option + M** and select Snippet.</span></span>
2. <span data-ttu-id="f55fb-366">選取 [程式碼片段] 後，系統會提示您選取 [全文檢索搜尋]、[Scoped Search] \(限定範圍搜尋\) 或 [Cross-Repository Reference] \(跨存放庫參考\)。</span><span class="sxs-lookup"><span data-stu-id="f55fb-366">Once Snippet is selected, you will be prompted for Full Search, Scoped Search or Cross-Repository Reference.</span></span> <span data-ttu-id="f55fb-367">若要在本機搜尋，請選取 [Full Local Search] \(本機全文檢索搜尋\)。</span><span class="sxs-lookup"><span data-stu-id="f55fb-367">To search locally, select Full Local Search.</span></span>
3. <span data-ttu-id="f55fb-368">輸入搜尋字詞以尋找檔案。</span><span class="sxs-lookup"><span data-stu-id="f55fb-368">Enter a search term to find the file.</span></span> <span data-ttu-id="f55fb-369">找到檔案之後，請選取檔案。</span><span class="sxs-lookup"><span data-stu-id="f55fb-369">Once you’ve found the file, select the file.</span></span>
4. <span data-ttu-id="f55fb-370">接下來，選取一個選項以決定應在程式碼片段中包含哪些程式碼。</span><span class="sxs-lookup"><span data-stu-id="f55fb-370">Next, select an option to determine which line(s) of code should be included in the snippet.</span></span> <span data-ttu-id="f55fb-371">這些選項包括：[識別碼]  、[範圍]  和 [無]  。</span><span class="sxs-lookup"><span data-stu-id="f55fb-371">The options are: **ID**, **Range** and **None**.</span></span>
5. <span data-ttu-id="f55fb-372">根據您在步驟 4 中的選擇，視需要提供值。</span><span class="sxs-lookup"><span data-stu-id="f55fb-372">Based on your selection from Step 4, provide a value if necessary.</span></span>

<span data-ttu-id="f55fb-373">顯示完整程式碼檔案：</span><span class="sxs-lookup"><span data-stu-id="f55fb-373">Display entire code file:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs":::
```

<span data-ttu-id="f55fb-374">透過指定行號來顯示部分程式碼檔案：</span><span class="sxs-lookup"><span data-stu-id="f55fb-374">Display part of a code file by specifying line numbers:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="f55fb-375">依程式碼片段名稱顯示部分程式碼檔案：</span><span class="sxs-lookup"><span data-stu-id="f55fb-375">Display part of a code file by a snippet name:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

#### <a name="code-from-another-repository"></a><span data-ttu-id="f55fb-376">另一個存放庫中的程式碼</span><span class="sxs-lookup"><span data-stu-id="f55fb-376">Code from another repository</span></span>

1. <span data-ttu-id="f55fb-377">在 Visual Studio Code 中，按一下 **Alt + M** 或 **選項 + M**，然後選取 [程式碼片段]。</span><span class="sxs-lookup"><span data-stu-id="f55fb-377">In Visual Studio Code, click **Alt + M** or **Option + M** and select Snippet.</span></span>
2. <span data-ttu-id="f55fb-378">選取 [程式碼片段] 後，系統會提示您選取 [全文檢索搜尋]、[Scoped Search] \(限定範圍搜尋\) 或 [Cross-Repository Reference] \(跨存放庫參考\)。</span><span class="sxs-lookup"><span data-stu-id="f55fb-378">Once Snippet is selected, you will be prompted for Full Search, Scoped Search or Cross-Repository Reference.</span></span> <span data-ttu-id="f55fb-379">若要搜尋不同的存放庫，請選取 [Cross-Repository Reference] \(跨存放庫參考\)。</span><span class="sxs-lookup"><span data-stu-id="f55fb-379">To search across repositories, select Cross-Repository Reference.</span></span>
3. <span data-ttu-id="f55fb-380">*.openpublishing.publish.config.json* 會提供您存放庫選項。</span><span class="sxs-lookup"><span data-stu-id="f55fb-380">You will be given a selection of repositories that are in *.openpublishing.publish.config.json*.</span></span> <span data-ttu-id="f55fb-381">選取存放庫。</span><span class="sxs-lookup"><span data-stu-id="f55fb-381">Select a repository.</span></span>
3. <span data-ttu-id="f55fb-382">輸入搜尋字詞以尋找檔案。</span><span class="sxs-lookup"><span data-stu-id="f55fb-382">Enter a search term to find the file.</span></span> <span data-ttu-id="f55fb-383">找到檔案之後，請選取檔案。</span><span class="sxs-lookup"><span data-stu-id="f55fb-383">Once you’ve found the file, select the file.</span></span>
4. <span data-ttu-id="f55fb-384">接下來，選取一個選項以決定應在程式碼片段中包含哪些程式碼。</span><span class="sxs-lookup"><span data-stu-id="f55fb-384">Next, select an option to determine which line(s) of code should be included in the snippet.</span></span> <span data-ttu-id="f55fb-385">這些選項包括：[識別碼]  、[範圍]  和 [無]  。</span><span class="sxs-lookup"><span data-stu-id="f55fb-385">The options are: **ID**, **Range** and **None**.</span></span>
5. <span data-ttu-id="f55fb-386">根據您在步驟 5 中的選擇，視需要提供值。</span><span class="sxs-lookup"><span data-stu-id="f55fb-386">Based on your selection from Step 5, provide a value if necessary.</span></span>

<span data-ttu-id="f55fb-387">您的程式碼片段參考看起來如下：</span><span class="sxs-lookup"><span data-stu-id="f55fb-387">Your snippet reference will look like this:</span></span>

```markdown
:::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
```

#### <a name="path-to-code-file"></a><span data-ttu-id="f55fb-388">程式碼檔案的路徑</span><span class="sxs-lookup"><span data-stu-id="f55fb-388">Path to code file</span></span>

<span data-ttu-id="f55fb-389">範例：</span><span class="sxs-lookup"><span data-stu-id="f55fb-389">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="f55fb-390">此範例是來自 ASP.NET 文件存放庫中的 [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md) \(英文\) 文章檔案。</span><span class="sxs-lookup"><span data-stu-id="f55fb-390">The example is from the ASP.NET docs repo, [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md) article file.</span></span> <span data-ttu-id="f55fb-391">程式碼檔案的參考方式，是透過針對相同存放庫中 [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) 的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="f55fb-391">The code file is referenced by a relative path to [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) in the same repository.</span></span>

#### <a name="selected-line-numbers"></a><span data-ttu-id="f55fb-392">選取的行號</span><span class="sxs-lookup"><span data-stu-id="f55fb-392">Selected line numbers</span></span>

<span data-ttu-id="f55fb-393">範例：</span><span class="sxs-lookup"><span data-stu-id="f55fb-393">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="f55fb-394">這個範例只顯示 *StudentController.cs* 程式碼檔案中的第 2-24 行和第 26 行。</span><span class="sxs-lookup"><span data-stu-id="f55fb-394">This example displays only lines 2-24 and 26 of the *StudentController.cs* code file.</span></span>

<span data-ttu-id="f55fb-395">相較於硬式編碼的行號，請盡量使用程式碼片段，原因會於下一節中說明。</span><span class="sxs-lookup"><span data-stu-id="f55fb-395">Prefer snippets over hard-coded line numbers, as explained in the next section.</span></span>

#### <a name="named-snippet"></a><span data-ttu-id="f55fb-396">具名的程式碼片段</span><span class="sxs-lookup"><span data-stu-id="f55fb-396">Named snippet</span></span>

<span data-ttu-id="f55fb-397">範例：</span><span class="sxs-lookup"><span data-stu-id="f55fb-397">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

<span data-ttu-id="f55fb-398">名稱只能使用字母和底線。</span><span class="sxs-lookup"><span data-stu-id="f55fb-398">Use only letters and underscores for the name.</span></span>

<span data-ttu-id="f55fb-399">此範例會顯示程式碼檔案的 `snippet_Create` 區段。</span><span class="sxs-lookup"><span data-stu-id="f55fb-399">The example displays the `snippet_Create` section of the code file.</span></span> <span data-ttu-id="f55fb-400">此範例的程式碼檔案具有名為 `snippet_Create` 的 C# 區域：</span><span class="sxs-lookup"><span data-stu-id="f55fb-400">The code file for this example has a C# region named `snippet_Create`:</span></span>

```cs
// code excluded from the snippet
// <snippet_Create>
// code included in the snippet
// </snippet_Create>
// code excluded from the snippet
```

<span data-ttu-id="f55fb-401">請盡可能參考具名的區段，而非指定行號。</span><span class="sxs-lookup"><span data-stu-id="f55fb-401">Whenever you can, refer to a named section rather than specifying line numbers.</span></span> <span data-ttu-id="f55fb-402">行號參考較容易出錯，因為程式碼檔案終究會變更，進而使行號產生變更。</span><span class="sxs-lookup"><span data-stu-id="f55fb-402">Line number references are brittle because code files inevitably change in ways that make line numbers change.</span></span>
<span data-ttu-id="f55fb-403">而您不一定會收到這些變更的通知。</span><span class="sxs-lookup"><span data-stu-id="f55fb-403">You don't necessarily get notified of such changes.</span></span> <span data-ttu-id="f55fb-404">您的文章最後會開始顯示錯誤的程式碼行，且您將不會意識到這項變更。</span><span class="sxs-lookup"><span data-stu-id="f55fb-404">Your article eventually starts showing the wrong lines and you have no clue anything has changed.</span></span>

#### <a name="highlighting-selected-lines"></a><span data-ttu-id="f55fb-405">反白顯示選取的行</span><span class="sxs-lookup"><span data-stu-id="f55fb-405">Highlighting selected lines</span></span>

<span data-ttu-id="f55fb-406">範例：</span><span class="sxs-lookup"><span data-stu-id="f55fb-406">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26" highlight="2,5":::
```

<span data-ttu-id="f55fb-407">此範例會反白顯示行 2 和 5，這是從顯示的程式碼片段開頭開始計算。</span><span class="sxs-lookup"><span data-stu-id="f55fb-407">The example highlights lines 2 and 5, counting from the start of the displayed snippet.</span></span> <span data-ttu-id="f55fb-408">(要反白顯示的行號並不是從程式碼檔案的開頭開始計算)。換句話說，系統會醒目提示程式碼檔案的第 3 行和第 6 行。</span><span class="sxs-lookup"><span data-stu-id="f55fb-408">(Line numbers to highlight don't count from the start of the code file.) In other words, lines 3 and 6 of the code file are highlighted.</span></span>

#### <a name="interactive-code-snippets"></a><span data-ttu-id="f55fb-409">互動式程式碼片段</span><span class="sxs-lookup"><span data-stu-id="f55fb-409">Interactive code snippets</span></span>

<span data-ttu-id="f55fb-410">您可以針對依參考所包含的程式碼片段啟用互動模式。</span><span class="sxs-lookup"><span data-stu-id="f55fb-410">You can enable interactive mode for code snippets included by reference.</span></span> <span data-ttu-id="f55fb-411">以下為範例：</span><span class="sxs-lookup"><span data-stu-id="f55fb-411">Here are examples:</span></span>

```markdown
:::code language="powershell" source="PowerShell.ps1" interactive="cloudshell-powershell":::
```

```markdown
:::code language="bash" source="Bash.sh" interactive="cloudshell-bash":::
```

<span data-ttu-id="f55fb-412">若要針對特定程式碼區塊開啟此功能，請使用 `interactive` 屬性。</span><span class="sxs-lookup"><span data-stu-id="f55fb-412">To turn on this feature for a particular code block, use the `interactive` attribute.</span></span> <span data-ttu-id="f55fb-413">可用的屬性值如下：</span><span class="sxs-lookup"><span data-stu-id="f55fb-413">The available attribute values are:</span></span>

- <span data-ttu-id="f55fb-414">`cloudshell-powershell` - 啟用 Azure PowerShell Cloud Shell，如上述範例所示</span><span class="sxs-lookup"><span data-stu-id="f55fb-414">`cloudshell-powershell` - Enables the Azure PowerShell Cloud Shell, as in the preceding example</span></span>
- <span data-ttu-id="f55fb-415">`cloudshell-bash` - 啟用 Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="f55fb-415">`cloudshell-bash` - Enables the Azure Cloud Shell</span></span>
- <span data-ttu-id="f55fb-416">`try-dotnet` - 啟用 Try .NET</span><span class="sxs-lookup"><span data-stu-id="f55fb-416">`try-dotnet` - Enables Try .NET</span></span>
- <span data-ttu-id="f55fb-417">`try-dotnet-class` - 以類別 Scaffolding 啟用 Try .NET</span><span class="sxs-lookup"><span data-stu-id="f55fb-417">`try-dotnet-class` - Enables Try .NET with class scaffolding</span></span>
- <span data-ttu-id="f55fb-418">`try-dotnet-method` - 以方法 Scaffolding 啟用 Try .NET</span><span class="sxs-lookup"><span data-stu-id="f55fb-418">`try-dotnet-method` - Enables Try .NET with method scaffolding</span></span>

<span data-ttu-id="f55fb-419">有相容的 `language` 和 `interactive` 配對。</span><span class="sxs-lookup"><span data-stu-id="f55fb-419">There are pairs of `language` and `interactive` that are compatible.</span></span> <span data-ttu-id="f55fb-420">例如，如果 `interactive` 是 `try-dotnet`，則語言必須是 `csharp`。</span><span class="sxs-lookup"><span data-stu-id="f55fb-420">For example, if `interactive` is `try-dotnet`, the language must be `csharp`.</span></span> <span data-ttu-id="f55fb-421">同樣地，`cloudshell-powershell` 只適用於 `powershell`，而 `cloudshell-bash` 為只適用於 `bash` 的語言。</span><span class="sxs-lookup"><span data-stu-id="f55fb-421">Similarly, `cloudshell-powershell` would only work with `powershell` and `cloudshell-bash` would work only with `bash` as the language.</span></span>

<span data-ttu-id="f55fb-422">針對 Azure Cloud Shell 和 PowerShell Cloud Shell，使用者可以僅針對其 Azure 帳戶執行命令。</span><span class="sxs-lookup"><span data-stu-id="f55fb-422">For the Azure Cloud Shell and PowerShell Cloud Shell, users can run commands against only their own Azure account.</span></span>

<span data-ttu-id="f55fb-423">[Try .NET](https://github.com/dotnet/try) 能讓您在瀏覽器中以互動方式執行 .NET 程式碼 (C#)。</span><span class="sxs-lookup"><span data-stu-id="f55fb-423">[Try .NET](https://github.com/dotnet/try) enables interactive execution of .NET code (C#) in the browser.</span></span> <span data-ttu-id="f55fb-424">Try .NET 有三個互動功能選項：`try-dotnet`、`try-dotnet-class` 和 `try-dotnet-method`。</span><span class="sxs-lookup"><span data-stu-id="f55fb-424">For Try .NET, there are three options for interactivity: `try-dotnet`, `try-dotnet-class`, and `try-dotnet-method`.</span></span> <span data-ttu-id="f55fb-425">程式碼片段不需要額外設定，即可使用這些選項。</span><span class="sxs-lookup"><span data-stu-id="f55fb-425">Use of these options require no additional configuration within the code snippet.</span></span> <span data-ttu-id="f55fb-426">根據預設，目前可供使用的命名空間為：</span><span class="sxs-lookup"><span data-stu-id="f55fb-426">The namespaces currently available by default are:</span></span>

- <span data-ttu-id="f55fb-427">System</span><span class="sxs-lookup"><span data-stu-id="f55fb-427">System</span></span>
- <span data-ttu-id="f55fb-428">System.Linq</span><span class="sxs-lookup"><span data-stu-id="f55fb-428">System.Linq</span></span>
- <span data-ttu-id="f55fb-429">System.Collections.Generic</span><span class="sxs-lookup"><span data-stu-id="f55fb-429">System.Collections.Generic</span></span>
- <span data-ttu-id="f55fb-430">System.Text</span><span class="sxs-lookup"><span data-stu-id="f55fb-430">System.Text</span></span>
- <span data-ttu-id="f55fb-431">System.Globalization</span><span class="sxs-lookup"><span data-stu-id="f55fb-431">System.Globalization</span></span>
- <span data-ttu-id="f55fb-432">System.Text.RegularExpressions</span><span class="sxs-lookup"><span data-stu-id="f55fb-432">System.Text.RegularExpressions</span></span>

<span data-ttu-id="f55fb-433">`try-dotnet` 屬性值可讓使用者在瀏覽器中執行 C# 程式碼，不需要將程式碼包裝在任何自訂程式碼中。</span><span class="sxs-lookup"><span data-stu-id="f55fb-433">The `try-dotnet` attribute value enables users to run C# code in the browser without the need to wrap the code in any custom code.</span></span>

<span data-ttu-id="f55fb-434">範例：</span><span class="sxs-lookup"><span data-stu-id="f55fb-434">Example:</span></span>

```md
:::code language="csharp" source="relative/path/source.cs" interactive="try-dotnet":::
```

<span data-ttu-id="f55fb-435">`try-dotnet-class` 值會將類別層級 Scaffolding 套用到傳遞至互動式元件的程式碼。</span><span class="sxs-lookup"><span data-stu-id="f55fb-435">The `try-dotnet-class` value applies class-level scaffolding to the code passed to the interactive component.</span></span>

```md
:::code language="csharp" source="relative/path/source.cs" id="snippet-tag" interactive="try-dotnet-class":::
```

<span data-ttu-id="f55fb-436">範例：</span><span class="sxs-lookup"><span data-stu-id="f55fb-436">Example:</span></span>

<span data-ttu-id="f55fb-437">未套用類別 Scaffolding 的程式碼片段</span><span class="sxs-lookup"><span data-stu-id="f55fb-437">Code Snippet without Class Scaffolding Applied</span></span>

```md
public static void Main()
    {  
        // Specify the data source.  
        int[] scores = new int[] { 97, 92, 81, 60 };        // Define the query expression.

        IEnumerable<int> scoreQuery =
            from score in scores  
            where score > 80  
            select score;

        // Execute the query.  
        foreach (int i in scoreQuery)
        {  
            Console.Write(i + " ");
        }
    }  
}
```

<span data-ttu-id="f55fb-438">套用類別 Scaffolding 的程式碼片段</span><span class="sxs-lookup"><span data-stu-id="f55fb-438">Code Snippet with Class Scaffolding Applied</span></span>

```md
class NameOfClass {

   public static void Main()
    {
        // Specify the data source.
        int[] scores = new int[] { 97, 92, 81, 60 };

        // Define the query expression.
        IEnumerable<int> scoreQuery =
            from score in scores
            where score > 80
            select score;

        // Execute the query.
        foreach (int i in scoreQuery)
        {
            Console.Write(i + " ");
        }
    }  
}
```

<span data-ttu-id="f55fb-439">`try-dotnet-method` 值會將方法層級 Scaffolding 套用到傳遞至互動式元件的程式碼。</span><span class="sxs-lookup"><span data-stu-id="f55fb-439">The `try-dotnet-method` value applies method-level scaffolding to the code passed to the interactive component.</span></span>

```md
:::code language="csharp" source="relative/path/source.cs" id="snippet-tag" interactive="try-dotnet-method":::
```

<span data-ttu-id="f55fb-440">範例：</span><span class="sxs-lookup"><span data-stu-id="f55fb-440">Example:</span></span>

<span data-ttu-id="f55fb-441">未套用方法 Scaffolding 的程式碼片段</span><span class="sxs-lookup"><span data-stu-id="f55fb-441">Code Snippet without Method Scaffolding Applied</span></span>

```md
/*Print some string in C#*/

Console.WriteLine("Hello C#.);
```

<span data-ttu-id="f55fb-442">套用方法 Scaffolding 的程式碼片段</span><span class="sxs-lookup"><span data-stu-id="f55fb-442">Code Snippet with Method Scaffolding Applied</span></span>

```md
public static void Main(string args[]) {

/*Print some string in C#*/

Console.WriteLine("Hello C#.);
}
```

#### <a name="snippet-syntax-reference"></a><span data-ttu-id="f55fb-443">程式碼片段語法參考</span><span class="sxs-lookup"><span data-stu-id="f55fb-443">Snippet syntax reference</span></span>

<span data-ttu-id="f55fb-444">您可以使用指定的程式碼語言，來參考存放庫中所儲存的程式碼片段。</span><span class="sxs-lookup"><span data-stu-id="f55fb-444">You can reference code snippets stored in your repo by using the specified code language.</span></span> <span data-ttu-id="f55fb-445">指定的程式碼路徑內容將會展開並包含在檔案中。</span><span class="sxs-lookup"><span data-stu-id="f55fb-445">The content of the specified code path will be expanded and included in your file.</span></span>

<span data-ttu-id="f55fb-446">程式碼片段的資料夾結構沒有限制。</span><span class="sxs-lookup"><span data-stu-id="f55fb-446">There aren't restrictions on the folder structure of code snippets.</span></span> <span data-ttu-id="f55fb-447">您可以用像是管理一般原始程式碼的方式管理程式碼片段。</span><span class="sxs-lookup"><span data-stu-id="f55fb-447">You can manage the code snippets as normal source code.</span></span>

<span data-ttu-id="f55fb-448">語法：</span><span class="sxs-lookup"><span data-stu-id="f55fb-448">Syntax:</span></span>

```md
:::code language="<language>" source="<path>" <attribute>="<attribute-value>":::
```

> [!IMPORTANT]
> <span data-ttu-id="f55fb-449">此語法是區塊 Markdown 延伸。</span><span class="sxs-lookup"><span data-stu-id="f55fb-449">This syntax is a block Markdown extension.</span></span> <span data-ttu-id="f55fb-450">必須用於本身的行。</span><span class="sxs-lookup"><span data-stu-id="f55fb-450">It must be used on its own line.</span></span>

- <span data-ttu-id="f55fb-451">`<language>` (選擇性  )</span><span class="sxs-lookup"><span data-stu-id="f55fb-451">`<language>` (*optional*)</span></span>
  - <span data-ttu-id="f55fb-452">程式碼片段的語言。</span><span class="sxs-lookup"><span data-stu-id="f55fb-452">Language of the code snippet.</span></span> <span data-ttu-id="f55fb-453">如需詳細資訊，請參閱本文稍後的[＜支援的語言＞](#supported-languages)一節。</span><span class="sxs-lookup"><span data-stu-id="f55fb-453">For more information, see the [Supported languages](#supported-languages) section later in this article.</span></span>

- <span data-ttu-id="f55fb-454">`<path>` (強制  )</span><span class="sxs-lookup"><span data-stu-id="f55fb-454">`<path>` (*mandatory*)</span></span>
  - <span data-ttu-id="f55fb-455">檔案系統中的相對路徑，表示要參考的程式碼片段檔案。</span><span class="sxs-lookup"><span data-stu-id="f55fb-455">Relative path in the file system that indicates the code snippet file to reference.</span></span>

- <span data-ttu-id="f55fb-456">`<attribute>` 與 `<attribute-value>` (選擇性  )</span><span class="sxs-lookup"><span data-stu-id="f55fb-456">`<attribute>` and `<attribute-value>` (*optional*)</span></span>
  - <span data-ttu-id="f55fb-457">同時使用以指定從檔案擷取程式碼的方式：</span><span class="sxs-lookup"><span data-stu-id="f55fb-457">Used together to specify how the code should be retrieved from the file:</span></span>
    - <span data-ttu-id="f55fb-458">`range`：`1,3-5`行的範圍。</span><span class="sxs-lookup"><span data-stu-id="f55fb-458">`range`: `1,3-5` A range of lines.</span></span> <span data-ttu-id="f55fb-459">此範例包含第 1、3、4 及 5 行。</span><span class="sxs-lookup"><span data-stu-id="f55fb-459">This example includes lines 1, 3, 4, and 5.</span></span>
    - <span data-ttu-id="f55fb-460">`id`：`snippet_Create` 需要從程式碼檔案插入的程式碼片段識別碼。</span><span class="sxs-lookup"><span data-stu-id="f55fb-460">`id`: `snippet_Create` The ID of the snippet that needs to be inserted from the code file.</span></span> <span data-ttu-id="f55fb-461">這個值與範圍不能並存。</span><span class="sxs-lookup"><span data-stu-id="f55fb-461">This value cannot co-exist with range.</span></span>
    - <span data-ttu-id="f55fb-462">`highlight`：`2-4,6` 需要在產生的程式碼片段中醒目提示的範圍及/或行數。</span><span class="sxs-lookup"><span data-stu-id="f55fb-462">`highlight`: `2-4,6` Range and/or numbers of lines that need to be highlighted in the generated code snippet.</span></span> <span data-ttu-id="f55fb-463">編號是相對於程式碼片段本身，而不是匯入的範圍。</span><span class="sxs-lookup"><span data-stu-id="f55fb-463">The numbering is relative to the code snippet itself, not the imported range.</span></span>
    - <span data-ttu-id="f55fb-464">`interactive`：`cloudshell-powershell`、`cloudshell-bash`、`try-dotnet`、`try-dotnet-class`、`try-dotnet-method` 字串值決定啟用的互動功能類型。</span><span class="sxs-lookup"><span data-stu-id="f55fb-464">`interactive`: `cloudshell-powershell`, `cloudshell-bash`, `try-dotnet`, `try-dotnet-class`, `try-dotnet-method` String value determines what kinds of interactivity are enabled.</span></span>

#### <a name="supported-languages"></a><span data-ttu-id="f55fb-465">支援的語言</span><span class="sxs-lookup"><span data-stu-id="f55fb-465">Supported languages</span></span>

|<span data-ttu-id="f55fb-466">Name</span><span class="sxs-lookup"><span data-stu-id="f55fb-466">Name</span></span>|<span data-ttu-id="f55fb-467">Markdown 標籤</span><span class="sxs-lookup"><span data-stu-id="f55fb-467">Markdown label</span></span>|
|-----|-------|
|<span data-ttu-id="f55fb-468">.NET Core CLI</span><span class="sxs-lookup"><span data-stu-id="f55fb-468">.NET Core CLI</span></span>|`dotnetcli`|
|<span data-ttu-id="f55fb-469">使用 C# 的 ASP.NET</span><span class="sxs-lookup"><span data-stu-id="f55fb-469">ASP.NET with C#</span></span>|`aspx-csharp`|
|<span data-ttu-id="f55fb-470">使用 VB 的 ASP.NET</span><span class="sxs-lookup"><span data-stu-id="f55fb-470">ASP.NET with VB</span></span>|`aspx-vb`|
|<span data-ttu-id="f55fb-471">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="f55fb-471">Azure CLI</span></span>|`azurecli`|
|<span data-ttu-id="f55fb-472">瀏覽器中的 Azure CLI</span><span class="sxs-lookup"><span data-stu-id="f55fb-472">Azure CLI in browser</span></span>|`azurecli-interactive`|
|<span data-ttu-id="f55fb-473">瀏覽器中的 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f55fb-473">Azure PowerShell in browser</span></span>|`azurepowershell-interactive`|
|<span data-ttu-id="f55fb-474">AzCopy</span><span class="sxs-lookup"><span data-stu-id="f55fb-474">AzCopy</span></span>|`azcopy`|
|<span data-ttu-id="f55fb-475">Bash</span><span class="sxs-lookup"><span data-stu-id="f55fb-475">Bash</span></span>|`bash`|
|<span data-ttu-id="f55fb-476">C++</span><span class="sxs-lookup"><span data-stu-id="f55fb-476">C++</span></span>|`cpp`|
|<span data-ttu-id="f55fb-477">C#</span><span class="sxs-lookup"><span data-stu-id="f55fb-477">C#</span></span>|`csharp`|
|<span data-ttu-id="f55fb-478">網頁瀏覽器中的 C#</span><span class="sxs-lookup"><span data-stu-id="f55fb-478">C# in browser</span></span>|`csharp-interactive`|
|<span data-ttu-id="f55fb-479">主控台</span><span class="sxs-lookup"><span data-stu-id="f55fb-479">Console</span></span>|`console`|
|<span data-ttu-id="f55fb-480">CSHTML</span><span class="sxs-lookup"><span data-stu-id="f55fb-480">CSHTML</span></span>|`cshtml`|
|<span data-ttu-id="f55fb-481">DAX</span><span class="sxs-lookup"><span data-stu-id="f55fb-481">DAX</span></span>|`dax`|
|<span data-ttu-id="f55fb-482">Docker</span><span class="sxs-lookup"><span data-stu-id="f55fb-482">Docker</span></span>|`Dockerfile`|
|<span data-ttu-id="f55fb-483">F#</span><span class="sxs-lookup"><span data-stu-id="f55fb-483">F#</span></span>|`fsharp`|
|<span data-ttu-id="f55fb-484">HTML</span><span class="sxs-lookup"><span data-stu-id="f55fb-484">HTML</span></span>|`html`|
|<span data-ttu-id="f55fb-485">Java</span><span class="sxs-lookup"><span data-stu-id="f55fb-485">Java</span></span>|`java`|
|<span data-ttu-id="f55fb-486">JavaScript</span><span class="sxs-lookup"><span data-stu-id="f55fb-486">JavaScript</span></span>|`javascript`|
|<span data-ttu-id="f55fb-487">JSON</span><span class="sxs-lookup"><span data-stu-id="f55fb-487">JSON</span></span>|`json`|
|<span data-ttu-id="f55fb-488">Kusto 查詢語言</span><span class="sxs-lookup"><span data-stu-id="f55fb-488">Kusto Query Language</span></span>|`kusto`|
|<span data-ttu-id="f55fb-489">Markdown</span><span class="sxs-lookup"><span data-stu-id="f55fb-489">Markdown</span></span>|`md`|
|<span data-ttu-id="f55fb-490">Objective-C</span><span class="sxs-lookup"><span data-stu-id="f55fb-490">Objective-C</span></span>|`objc`|
|<span data-ttu-id="f55fb-491">PHP</span><span class="sxs-lookup"><span data-stu-id="f55fb-491">PHP</span></span>|`php`|
|<span data-ttu-id="f55fb-492">PowerShell</span><span class="sxs-lookup"><span data-stu-id="f55fb-492">PowerShell</span></span>|`powershell`|
|<span data-ttu-id="f55fb-493">Power Query M</span><span class="sxs-lookup"><span data-stu-id="f55fb-493">Power Query M</span></span>|`powerquery-m`|
|<span data-ttu-id="f55fb-494">protobuf</span><span class="sxs-lookup"><span data-stu-id="f55fb-494">protobuf</span></span>|`protobuf`|
|<span data-ttu-id="f55fb-495">Python</span><span class="sxs-lookup"><span data-stu-id="f55fb-495">Python</span></span>|`python`|
|<span data-ttu-id="f55fb-496">Ruby</span><span class="sxs-lookup"><span data-stu-id="f55fb-496">Ruby</span></span>|`ruby`|
|<span data-ttu-id="f55fb-497">SQL</span><span class="sxs-lookup"><span data-stu-id="f55fb-497">SQL</span></span>|`sql`|
|<span data-ttu-id="f55fb-498">Swift</span><span class="sxs-lookup"><span data-stu-id="f55fb-498">Swift</span></span>|`swift`|
|<span data-ttu-id="f55fb-499">VB</span><span class="sxs-lookup"><span data-stu-id="f55fb-499">VB</span></span>|`vb`|
|<span data-ttu-id="f55fb-500">XAML</span><span class="sxs-lookup"><span data-stu-id="f55fb-500">XAML</span></span>|`xaml`|
|<span data-ttu-id="f55fb-501">XML</span><span class="sxs-lookup"><span data-stu-id="f55fb-501">XML</span></span>|`xml`|
|<span data-ttu-id="f55fb-502">YAML</span><span class="sxs-lookup"><span data-stu-id="f55fb-502">YAML</span></span>|`yml`|

#### <a name="code-extensions"></a><span data-ttu-id="f55fb-503">程式碼擴充</span><span class="sxs-lookup"><span data-stu-id="f55fb-503">Code extensions</span></span>

|<span data-ttu-id="f55fb-504">Name</span><span class="sxs-lookup"><span data-stu-id="f55fb-504">Name</span></span>|<span data-ttu-id="f55fb-505">Markdown 標籤</span><span class="sxs-lookup"><span data-stu-id="f55fb-505">Markdown label</span></span>|<span data-ttu-id="f55fb-506">副檔名</span><span class="sxs-lookup"><span data-stu-id="f55fb-506">File extension</span></span>|
|-----|-------|-----|
|<span data-ttu-id="f55fb-507">C#</span><span class="sxs-lookup"><span data-stu-id="f55fb-507">C#</span></span>|<span data-ttu-id="f55fb-508">csharp</span><span class="sxs-lookup"><span data-stu-id="f55fb-508">csharp</span></span>|<span data-ttu-id="f55fb-509">.cs、.csx</span><span class="sxs-lookup"><span data-stu-id="f55fb-509">.cs, .csx</span></span>|
|<span data-ttu-id="f55fb-510">C++</span><span class="sxs-lookup"><span data-stu-id="f55fb-510">C++</span></span>|<span data-ttu-id="f55fb-511">cpp</span><span class="sxs-lookup"><span data-stu-id="f55fb-511">cpp</span></span>|<span data-ttu-id="f55fb-512">.cpp、.h</span><span class="sxs-lookup"><span data-stu-id="f55fb-512">.cpp, .h</span></span>|
|<span data-ttu-id="f55fb-513">F#</span><span class="sxs-lookup"><span data-stu-id="f55fb-513">F#</span></span>|<span data-ttu-id="f55fb-514">fsharp</span><span class="sxs-lookup"><span data-stu-id="f55fb-514">fsharp</span></span>|<span data-ttu-id="f55fb-515">.fs</span><span class="sxs-lookup"><span data-stu-id="f55fb-515">.fs</span></span>|
|<span data-ttu-id="f55fb-516">Java</span><span class="sxs-lookup"><span data-stu-id="f55fb-516">Java</span></span>|<span data-ttu-id="f55fb-517">java</span><span class="sxs-lookup"><span data-stu-id="f55fb-517">java</span></span>|<span data-ttu-id="f55fb-518">.java</span><span class="sxs-lookup"><span data-stu-id="f55fb-518">.java</span></span>|
|<span data-ttu-id="f55fb-519">JavaScript</span><span class="sxs-lookup"><span data-stu-id="f55fb-519">JavaScript</span></span>|<span data-ttu-id="f55fb-520">javascript</span><span class="sxs-lookup"><span data-stu-id="f55fb-520">javascript</span></span>|<span data-ttu-id="f55fb-521">.js</span><span class="sxs-lookup"><span data-stu-id="f55fb-521">.js</span></span>|
|<span data-ttu-id="f55fb-522">Python</span><span class="sxs-lookup"><span data-stu-id="f55fb-522">Python</span></span>|<span data-ttu-id="f55fb-523">python</span><span class="sxs-lookup"><span data-stu-id="f55fb-523">python</span></span>|<span data-ttu-id="f55fb-524">.py</span><span class="sxs-lookup"><span data-stu-id="f55fb-524">.py</span></span>|
|<span data-ttu-id="f55fb-525">SQL</span><span class="sxs-lookup"><span data-stu-id="f55fb-525">SQL</span></span>|<span data-ttu-id="f55fb-526">sql</span><span class="sxs-lookup"><span data-stu-id="f55fb-526">sql</span></span>|<span data-ttu-id="f55fb-527">.sql</span><span class="sxs-lookup"><span data-stu-id="f55fb-527">.sql</span></span>|
|<span data-ttu-id="f55fb-528">VB</span><span class="sxs-lookup"><span data-stu-id="f55fb-528">VB</span></span>|<span data-ttu-id="f55fb-529">vb</span><span class="sxs-lookup"><span data-stu-id="f55fb-529">vb</span></span>|<span data-ttu-id="f55fb-530">.vb</span><span class="sxs-lookup"><span data-stu-id="f55fb-530">.vb</span></span>|
|<span data-ttu-id="f55fb-531">XAML</span><span class="sxs-lookup"><span data-stu-id="f55fb-531">XAML</span></span>|<span data-ttu-id="f55fb-532">xaml</span><span class="sxs-lookup"><span data-stu-id="f55fb-532">xaml</span></span>|<span data-ttu-id="f55fb-533">.xaml</span><span class="sxs-lookup"><span data-stu-id="f55fb-533">.xaml</span></span>|
|<span data-ttu-id="f55fb-534">XML</span><span class="sxs-lookup"><span data-stu-id="f55fb-534">XML</span></span>|<span data-ttu-id="f55fb-535">xml</span><span class="sxs-lookup"><span data-stu-id="f55fb-535">xml</span></span>|<span data-ttu-id="f55fb-536">.xml</span><span class="sxs-lookup"><span data-stu-id="f55fb-536">.xml</span></span>|

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="f55fb-537">偵錯與疑難排解</span><span class="sxs-lookup"><span data-stu-id="f55fb-537">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="f55fb-538">替代文字</span><span class="sxs-lookup"><span data-stu-id="f55fb-538">Alt text</span></span>

<span data-ttu-id="f55fb-539">將無法正確轉譯包含底線的替代文字。</span><span class="sxs-lookup"><span data-stu-id="f55fb-539">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="f55fb-540">例如，不要使用此語法︰</span><span class="sxs-lookup"><span data-stu-id="f55fb-540">For example, instead of using this:</span></span>

```md
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="f55fb-541">將底線逸出，如下所示：</span><span class="sxs-lookup"><span data-stu-id="f55fb-541">Escape the underscores like this:</span></span>

```md
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="f55fb-542">縮寫符號和雙引號</span><span class="sxs-lookup"><span data-stu-id="f55fb-542">Apostrophes and quotation marks</span></span>

<span data-ttu-id="f55fb-543">如果您將內容從 Word 複製到 Markdown 編輯器中，文字可能會包含「智慧」(彎曲) 縮寫符號或雙引號。</span><span class="sxs-lookup"><span data-stu-id="f55fb-543">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="f55fb-544">這些必須編碼或變更為基本縮寫符號或雙引號。</span><span class="sxs-lookup"><span data-stu-id="f55fb-544">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="f55fb-545">否則檔案發佈後可能會產生這樣的內容：Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="f55fb-545">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="f55fb-546">以下是這些標點符號的「智慧」版本編碼：</span><span class="sxs-lookup"><span data-stu-id="f55fb-546">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="f55fb-547">左 (開頭) 雙引號：`&#8220;`</span><span class="sxs-lookup"><span data-stu-id="f55fb-547">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="f55fb-548">右 (結尾) 雙引號：`&#8221;`</span><span class="sxs-lookup"><span data-stu-id="f55fb-548">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="f55fb-549">右 (結尾) 單引號或縮寫符號：`&#8217;`</span><span class="sxs-lookup"><span data-stu-id="f55fb-549">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="f55fb-550">左 (開頭) 單引號 (很少使用)：`&#8216;`</span><span class="sxs-lookup"><span data-stu-id="f55fb-550">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="f55fb-551">角括號</span><span class="sxs-lookup"><span data-stu-id="f55fb-551">Angle brackets</span></span>

<span data-ttu-id="f55fb-552">通常會使用角括弧來表示預留位置。</span><span class="sxs-lookup"><span data-stu-id="f55fb-552">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="f55fb-553">當您使用文字 (非程式碼) 執行此作業時，必須編碼角括弧。</span><span class="sxs-lookup"><span data-stu-id="f55fb-553">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="f55fb-554">否則 Markdown 會將它們視為 HTML 標籤。</span><span class="sxs-lookup"><span data-stu-id="f55fb-554">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="f55fb-555">例如，將 `<script name>` 編碼成 `&lt;script name&gt;`</span><span class="sxs-lookup"><span data-stu-id="f55fb-555">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="markdown-flavor"></a><span data-ttu-id="f55fb-556">Markdown 變體</span><span class="sxs-lookup"><span data-stu-id="f55fb-556">Markdown flavor</span></span>

<span data-ttu-id="f55fb-557">docs.microsoft.com 網站後端支援透過 [Markdig](https://github.com/lunet-io/markdig) 剖析引擎且符合 [CommonMark](https://commonmark.org/) 規範的 Markdown。</span><span class="sxs-lookup"><span data-stu-id="f55fb-557">The docs.microsoft.com site backend supports [CommonMark](https://commonmark.org/) compliant Markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine.</span></span> <span data-ttu-id="f55fb-558">這個 Markdown 變體大多與 [GitHub 變體 Markdown (GFM)](https://help.github.com/categories/writing-on-github/) 相容，因為大多數文件都儲存在 GitHub 中並可在該處編輯。</span><span class="sxs-lookup"><span data-stu-id="f55fb-558">This markdown flavor is mostly compatible with [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="f55fb-559">額外的功能可透過 Markdown 延伸模組新增。</span><span class="sxs-lookup"><span data-stu-id="f55fb-559">Additional functionality is added through Markdown extensions.</span></span>

## <a name="see-also"></a><span data-ttu-id="f55fb-560">另請參閱：</span><span class="sxs-lookup"><span data-stu-id="f55fb-560">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="f55fb-561">Markdown 資源</span><span class="sxs-lookup"><span data-stu-id="f55fb-561">Markdown resources</span></span>

- <span data-ttu-id="f55fb-562">[Markdown 簡介](https://daringfireball.net/projects/markdown/syntax) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="f55fb-562">[Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax)</span></span>
- [<span data-ttu-id="f55fb-563">Docs Markdown 速查表</span><span class="sxs-lookup"><span data-stu-id="f55fb-563">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- <span data-ttu-id="f55fb-564">[GitHub 的 Markdown 基本概念](https://help.github.com/articles/markdown-basics/) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="f55fb-564">[GitHub's Markdown Basics](https://help.github.com/articles/markdown-basics/)</span></span>
- <span data-ttu-id="f55fb-565">[The Markdown Guide](https://www.markdownguide.org/) (Markdown 指南)</span><span class="sxs-lookup"><span data-stu-id="f55fb-565">[The Markdown Guide](https://www.markdownguide.org/)</span></span>
