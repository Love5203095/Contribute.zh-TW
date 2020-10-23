---
title: 如何在文件中包含程式碼
description: 了解如何將程式碼元素和程式碼片段包含在文章中，以在 docs.microsoft.com 上發行。
author: tdykstra
ms.author: tdykstra
ms.date: 03/03/2020
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: b33333a49df11f0234193ca84fc2c3accdb6894d
ms.sourcegitcommit: f1535713b66ff9b840f1138583746bc2bf182b4f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/12/2020
ms.locfileid: "91953642"
---
# <a name="how-to-include-code-in-docs"></a><span data-ttu-id="3ebf1-103">如何在文件中包含程式碼</span><span class="sxs-lookup"><span data-stu-id="3ebf1-103">How to include code in docs</span></span>

<span data-ttu-id="3ebf1-104">有數種方法可以將程式碼包含在於 docs.microsoft.com 上發行的文章之中：</span><span class="sxs-lookup"><span data-stu-id="3ebf1-104">There are several ways to include code in an article published on docs.microsoft.com:</span></span>

* <span data-ttu-id="3ebf1-105">位於文字內的個別元素 (單字)。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-105">Individual elements (words) within a line.</span></span>

  <span data-ttu-id="3ebf1-106">以下是 `code` 樣式的範例。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-106">Here's an example of `code` style.</span></span>

  <span data-ttu-id="3ebf1-107">當涉及文字裡附近程式碼區塊中的具名參數和變數時，請使用程式碼格式。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-107">Use code format when referring to named parameters and variables in a nearby code block in your text.</span></span> <span data-ttu-id="3ebf1-108">程式碼格式也可以用於屬性、方法、類別、語言關鍵字。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-108">Code format may also be used for properties, methods, classes, and language keywords.</span></span> <span data-ttu-id="3ebf1-109">如需詳細資訊，請參閱本文稍後的[程式碼項目](#code-elements)。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-109">For more information, see [Code elements](#code-elements) later in this article..</span></span>

* <span data-ttu-id="3ebf1-110">位於文章 Markdown 檔案中的程式碼區塊。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-110">Code blocks in the article Markdown file.</span></span>

  ```markdown
      ```csharp
      public static void Log(string message)
      {
          _logger.LogInformation(message);
      }
      ```
  ```

  <span data-ttu-id="3ebf1-111">當藉由參考程式碼檔案來顯示程式碼的做法不可行時，請使用內嵌程式碼區塊。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-111">Use inline code blocks when it's impractical to display code by reference to a code file.</span></span> <span data-ttu-id="3ebf1-112">如需詳細資訊，請參閱本文稍後的[程式碼區塊](#inline-code-blocks)。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-112">For more information, see [Code blocks](#inline-code-blocks) later in this article.</span></span>

* <span data-ttu-id="3ebf1-113">參考本機存放庫中程式碼檔案的程式碼區塊。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-113">Code blocks by reference to a code file in the local repository.</span></span>

  ```markdown
  :::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
  ```

  <span data-ttu-id="3ebf1-114">如需詳細資訊，請參閱本文稍後的[存放庫內的程式碼片段參考](#in-repo-snippet-references)。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-114">For more information, see [In-repo snippet references](#in-repo-snippet-references) later in this article.</span></span>

* <span data-ttu-id="3ebf1-115">參考位於另一個存放庫中程式碼檔案的程式碼區塊。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-115">Code blocks by reference to a code file in another repository.</span></span>

  ```markdown
  :::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
  ```
  
  <span data-ttu-id="3ebf1-116">如需詳細資訊，請參閱本文稍後的[存放庫外的程式碼片段參考](#out-of-repo-snippet-references)。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-116">For more information, see [Out-of-repo snippet references](#out-of-repo-snippet-references) later in this article.</span></span>
  
* <span data-ttu-id="3ebf1-117">讓使用者在瀏覽器中執行程式碼的程式碼區塊。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-117">Code blocks that let the user execute code in the browser.</span></span>

   ```markdown
  :::code source="PowerShell.ps1" interactive="cloudshell-powershell":::
  ```

  <span data-ttu-id="3ebf1-118">如需詳細資訊，請參閱本文稍後的[互動式程式碼片段](#interactive-code-snippets)。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-118">For more information, see [Interactive code snippets](#interactive-code-snippets) later in this article.</span></span>

<span data-ttu-id="3ebf1-119">除了解釋上述包含程式碼方式的 Markdown 之外，文章也會提供一些[針對所有程式碼區塊的一般指引](#code-blocks)。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-119">Besides explaining the Markdown for each of these ways to include code, the article provides some [general guidance for all code blocks](#code-blocks).</span></span>

## <a name="code-elements"></a><span data-ttu-id="3ebf1-120">程式碼元素</span><span class="sxs-lookup"><span data-stu-id="3ebf1-120">Code elements</span></span>

<span data-ttu-id="3ebf1-121">「程式碼元素」為程式設計語言關鍵字、類別名稱、屬性名稱等等。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-121">A "code element" is a programming language keyword, class name, property name, and so forth.</span></span> <span data-ttu-id="3ebf1-122">要界定什麼是程式碼，本身並不是一件簡單明瞭的事。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-122">It's not always obvious what qualifies as code.</span></span> <span data-ttu-id="3ebf1-123">例如，NuGet 套件名稱應該要視為程式碼進行處理。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-123">For example, NuGet package names should be treated as code.</span></span> <span data-ttu-id="3ebf1-124">若有疑慮，請參閱[文字格式設定指導方針](text-formatting-guidelines.md)。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-124">When in doubt, see [Text formatting guidelines](text-formatting-guidelines.md).</span></span>

### <a name="inline-code-style"></a><span data-ttu-id="3ebf1-125">內嵌程式碼樣式</span><span class="sxs-lookup"><span data-stu-id="3ebf1-125">Inline code style</span></span>

<span data-ttu-id="3ebf1-126">若要將程式碼元素包含在文章文字中，請以倒引號 (\`) 環繞它以指出程式碼樣式。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-126">To include a code element in article text, surround it with backticks (\`) to indicate code style.</span></span>
<span data-ttu-id="3ebf1-127">內嵌程式碼樣式不應使用三個倒引號格式。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-127">Inline code style shouldn't use the triple-backtick format.</span></span>

|<span data-ttu-id="3ebf1-128">Markdown</span><span class="sxs-lookup"><span data-stu-id="3ebf1-128">Markdown</span></span> |<span data-ttu-id="3ebf1-129">已轉譯</span><span class="sxs-lookup"><span data-stu-id="3ebf1-129">Rendered</span></span> |
|---------|---------|
|<span data-ttu-id="3ebf1-130">根據預設，Entity Framework 會將名為 \`Id\` 或 \`ClassnameID\` 的屬性解譯為主索引鍵。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-130">By default, the Entity Framework interprets a property that's named \`Id\` or \`ClassnameID\` as the primary key.</span></span>|<span data-ttu-id="3ebf1-131">根據預設，Entity Framework 會將名為 `Id` 或 `ClassnameID` 的屬性解譯為主索引鍵。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-131">By default, the Entity Framework interprets a property that's named `Id` or `ClassnameID` as the primary key.</span></span>|

<span data-ttu-id="3ebf1-132">對文章進行當地語系化 (翻譯成其他語言) 之後，樣式被設定為程式碼的文字將不會被翻譯。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-132">When an article is localized (translated into other languages), text styled as code is left untranslated.</span></span> <span data-ttu-id="3ebf1-133">如果您想要在不使用程式碼樣式的情況下防止當地語系化，請參閱[不可當地語系化的字串](markdown-reference.md#non-localized-strings)。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-133">If you want to prevent localization without using code style, see [Non-localized strings](markdown-reference.md#non-localized-strings).</span></span>

### <a name="bold-style"></a><span data-ttu-id="3ebf1-134">粗體樣式</span><span class="sxs-lookup"><span data-stu-id="3ebf1-134">Bold style</span></span>

<span data-ttu-id="3ebf1-135">某些較舊的樣式指南會針對內嵌程式碼指定粗體。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-135">Some older style guides specify bold for inline code.</span></span> <span data-ttu-id="3ebf1-136">在程式碼樣式非常突兀並會影響可讀性時，便可以使用粗體。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-136">Bold is an option when code style is so obtrusive as to compromise readability.</span></span> <span data-ttu-id="3ebf1-137">例如，如果 Markdown 資料表中多為程式碼元素，滿滿的程式碼樣式看起來會很擁擠。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-137">For example, a Markdown table with mostly code elements might look too busy with code styling everywhere.</span></span> <span data-ttu-id="3ebf1-138">如果您選擇使用粗體樣式，請使用 [不可當地語系化的字串語法](markdown-reference.md#non-localized-strings)，確保不會將程式碼當地語系化。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-138">If you choose to use bold style, use [non-localized strings syntax](markdown-reference.md#non-localized-strings) to make sure that code is not localized.</span></span>

### <a name="links"></a><span data-ttu-id="3ebf1-139">連結</span><span class="sxs-lookup"><span data-stu-id="3ebf1-139">Links</span></span>

<span data-ttu-id="3ebf1-140">在某些內容中，指向參考文件的連結可能比程式碼格式更有用。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-140">A link to reference documentation may be more helpful than code format in some contexts.</span></span> <span data-ttu-id="3ebf1-141">如果您使用連結，請勿將程式碼格式套用至連結文字。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-141">If you use a link, don't apply code format to the link text.</span></span> <span data-ttu-id="3ebf1-142">將連結的樣式設為程式碼，可能會無法明確表示該文字實際上為連結。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-142">Styling a link as code can obscure the fact that the text is a link.</span></span>

<span data-ttu-id="3ebf1-143">如果您使用連結，並於相同內容的稍後又參考相同的元素，請在之後的例項使用程式碼格式 (而不是連結)。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-143">If you use a link and refer to the same element later in the same context, make the subsequent instances code format rather than links.</span></span>

### <a name="placeholders"></a><span data-ttu-id="3ebf1-144">預留位置</span><span class="sxs-lookup"><span data-stu-id="3ebf1-144">Placeholders</span></span>

<span data-ttu-id="3ebf1-145">如果您想要讓使用者以自己的值取代顯示的程式碼區段，請使用預留位置文字 (以角括弧或大括弧標示)。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-145">If you want the user to replace a section of displayed code with their own values, use placeholder text marked off by angle brackets or curly braces.</span></span> <span data-ttu-id="3ebf1-146">例如：`az group delete -n <ResourceGroupName>`。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-146">For example: `az group delete -n <ResourceGroupName>`.</span></span> <span data-ttu-id="3ebf1-147">說明在替代成實際值時，必須移除角括弧或大括弧。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-147">Explain that the brackets or braces must be removed when substituting real values.</span></span>

## <a name="code-blocks"></a><span data-ttu-id="3ebf1-148">程式碼區塊</span><span class="sxs-lookup"><span data-stu-id="3ebf1-148">Code blocks</span></span>

<span data-ttu-id="3ebf1-149">在文件中包含程式碼的語法，會視程式碼所在的位置而有所不同：</span><span class="sxs-lookup"><span data-stu-id="3ebf1-149">The syntax for including code in a doc depends on where the code is located:</span></span>

* [<span data-ttu-id="3ebf1-150">位於文章 Markdown 檔案中</span><span class="sxs-lookup"><span data-stu-id="3ebf1-150">In the article Markdown file</span></span>](#inline-code-blocks)
* [<span data-ttu-id="3ebf1-151">位於相同存放庫中的程式碼檔案中</span><span class="sxs-lookup"><span data-stu-id="3ebf1-151">In a code file in the same repository</span></span>](#in-repo-snippet-references)
* [<span data-ttu-id="3ebf1-152">位於不同存放庫中的程式碼檔案中</span><span class="sxs-lookup"><span data-stu-id="3ebf1-152">In a code file in a different repository</span></span>](#out-of-repo-snippet-references)

<span data-ttu-id="3ebf1-153">下列指導方針適用於全部三種類型的程式碼區塊：</span><span class="sxs-lookup"><span data-stu-id="3ebf1-153">Following are guidelines that apply to all three types of code blocks:</span></span>

* [<span data-ttu-id="3ebf1-154">自動化程式碼驗證。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-154">Automate code validation.</span></span>](#code-validation)
* [<span data-ttu-id="3ebf1-155">反白顯示關鍵程式碼行。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-155">Highlight key lines of code.</span></span>](#highlighting)
* [<span data-ttu-id="3ebf1-156">避免水平捲軸。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-156">Avoid horizontal scroll bars.</span></span>](#horizontal-scroll-bars)

### <a name="screenshots"></a><span data-ttu-id="3ebf1-157">螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="3ebf1-157">Screenshots</span></span>

<span data-ttu-id="3ebf1-158">上一節所列的所有方法都會產生可使用的程式碼區塊：</span><span class="sxs-lookup"><span data-stu-id="3ebf1-158">All of the methods listed in the preceding section result in usable code blocks:</span></span>

* <span data-ttu-id="3ebf1-159">您可以複製並貼上這些區塊。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-159">You can copy and paste from them.</span></span>
* <span data-ttu-id="3ebf1-160">這些區塊均由搜尋引擎編制索引。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-160">They're indexed by search engines.</span></span>
* <span data-ttu-id="3ebf1-161">螢幕助讀程式可以存取這些區塊。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-161">They're accessible to screen readers.</span></span>

<span data-ttu-id="3ebf1-162">這些只是不建議使用 IDE 螢幕擷取畫面在文章中包含程式碼的其中幾個原因。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-162">These are just a few of the reasons why IDE screenshots aren't recommended as a method of including code in an article.</span></span> <span data-ttu-id="3ebf1-163">只有當您要顯示與 IDE 本身相關的內容時 (例如 IntelliSense)，才使用 IDE 螢幕擷取畫面。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-163">Use IDE screenshots for code only if you're showing something about the IDE itself, like IntelliSense.</span></span> <span data-ttu-id="3ebf1-164">單只為了秀出顏色標示和反白顯示，請勿使用螢幕擷取畫面。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-164">Don't use screenshots just to show colorization and highlighting.</span></span>

### <a name="code-validation"></a><span data-ttu-id="3ebf1-165">程式碼驗證</span><span class="sxs-lookup"><span data-stu-id="3ebf1-165">Code validation</span></span>

<span data-ttu-id="3ebf1-166">某些存放庫會實作能自動編譯所有範例程式碼以檢查錯誤的處理程序。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-166">Some repositories have implemented processes that automatically compile all sample code to check for errors.</span></span> <span data-ttu-id="3ebf1-167">.NET 存放庫就做得到。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-167">The .NET repository does this.</span></span> <span data-ttu-id="3ebf1-168">如需詳細資訊，請參閱 .NET 存放庫中的[參與貢獻](https://github.com/dotnet/docs/blob/master/CONTRIBUTING.md) \(英文\)。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-168">For more information, see [Contributing](https://github.com/dotnet/docs/blob/master/CONTRIBUTING.md) in the .NET repository.</span></span>

<span data-ttu-id="3ebf1-169">如果您要包含另一個存放庫中的程式碼區塊，對於這些程式碼的維護策略請與其擁有者合作，讓您包含的程式碼不會因為程式碼所使用的程式庫有了新版本而中斷或過期。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-169">If you are including code blocks from another repository, work with the owners on a maintenance strategy for the code so that your included code does not break or go out of date as new versions of the libraries the code uses are shipped.</span></span>

### <a name="highlighting"></a><span data-ttu-id="3ebf1-170">反白顯示</span><span class="sxs-lookup"><span data-stu-id="3ebf1-170">Highlighting</span></span>

<span data-ttu-id="3ebf1-171">程式碼片段通常會包含比必要程式碼還要多的程式碼，以提供背景內容。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-171">Snippets typically include more code than necessary in order to provide context.</span></span> <span data-ttu-id="3ebf1-172">在此情況下，若能將程式碼片段中的關鍵程式碼反白顯示，便能協助提升可讀性，如此範例所示：</span><span class="sxs-lookup"><span data-stu-id="3ebf1-172">It helps readability when you highlight the key lines that you're focusing on in the snippet, as in this example:</span></span>

![顯示反白顯示程式碼的範例](media/code-in-docs/highlighted-code.png)

<span data-ttu-id="3ebf1-174">當您將程式碼包含在文章 Markdown 檔案中時，將無法反白顯示它。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-174">You can't highlight code when you include it in the article Markdown file.</span></span> <span data-ttu-id="3ebf1-175">此功能僅適用於參考程式碼檔案的程式碼片段。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-175">It works only for code snippets included by reference to a code file.</span></span>

### <a name="horizontal-scroll-bars"></a><span data-ttu-id="3ebf1-176">水平捲軸</span><span class="sxs-lookup"><span data-stu-id="3ebf1-176">Horizontal scroll bars</span></span>

<span data-ttu-id="3ebf1-177">請將較長的行分段，以避免水平捲軸。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-177">Break up long lines to avoid horizontal scroll bars.</span></span> <span data-ttu-id="3ebf1-178">程式碼片段上的捲軸會使程式碼較難閱讀。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-178">Scroll bars on code blocks make code hard to read.</span></span> <span data-ttu-id="3ebf1-179">水平捲軸對較長程式碼區塊的影響更為明顯，因為讀者可能會無法同時看見捲軸和想要閱讀的程式碼行。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-179">They're especially problematic on longer code blocks, where it may be impossible to see the scroll bar and the line you want to read at the same time.</span></span>

<span data-ttu-id="3ebf1-180">想讓程式碼區塊的水平捲軸盡可能最小，其中一個好的做法是將超過 85 個字元的程式碼行分段。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-180">A good practice for minimizing horizontal scroll bars on code blocks is to break up code lines longer than 85 characters.</span></span> <span data-ttu-id="3ebf1-181">但請記住，捲軸的存在與否不是可讀性的唯一準則。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-181">But keep in mind that the presence or absence of a scroll bar isn't the only criterion of readability.</span></span> <span data-ttu-id="3ebf1-182">如果在 85 個字元前中斷一行會影響可讀性或複製貼上的便利性，超過 85 個也無妨。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-182">If breaking a line before 85 hurts readability or copy-paste convenience, feel free to go over 85.</span></span>

## <a name="inline-code-blocks"></a><span data-ttu-id="3ebf1-183">內嵌程式碼區塊</span><span class="sxs-lookup"><span data-stu-id="3ebf1-183">Inline code blocks</span></span>

<span data-ttu-id="3ebf1-184">只有當藉由參考程式碼檔案來顯示程式碼的做法不可行時，才使用內嵌程式碼區塊。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-184">Use inline code blocks only when it's impractical to display code by reference to a code file.</span></span> <span data-ttu-id="3ebf1-185">相較於完整專案中的程式碼檔案，內嵌程式碼通常比較不容易測試和保持最新狀態。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-185">Inline code is generally more difficult to test and keep up to date compared to a code file that is part of a complete project.</span></span>  <span data-ttu-id="3ebf1-186">且內嵌程式碼可能會省略可協助開發人員瞭解及使用程式碼的內容。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-186">And inline code may omit context that could help the developer to understand and use the code.</span></span> <span data-ttu-id="3ebf1-187">這些考量主要適用於程式設計語言。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-187">These considerations apply mainly to programming languages.</span></span> <span data-ttu-id="3ebf1-188">內嵌程式碼區塊也可以用於輸出和輸入 (例如 JSON)、查詢語言 (例如 SQL)、指令碼語言 (例如 PowerShell)。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-188">Inline code blocks can also be used for outputs and inputs (such as JSON), query languages (such as SQL), and scripting languages (such as PowerShell).</span></span>
  
<span data-ttu-id="3ebf1-189">有兩種方式可以將文章檔案中的某個文字區塊指定為程式碼區塊：將它*隔離*在三個倒引號 (\`\`\`) 之內，或是對它進行縮排。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-189">There are two ways to indicate a section of text in an article file is a code block: by *fencing* it in triple-backticks (\`\`\`) or by indenting it.</span></span> <span data-ttu-id="3ebf1-190">建議使用隔離的方式，因為它能讓您指定語言。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-190">Fencing is preferred because it lets you specify the language.</span></span> <span data-ttu-id="3ebf1-191">請避免使用縮排，因為太容易出錯，而且當其他作者需要編輯您的文章時，可能很難瞭解您的意圖。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-191">Avoid using indentation because it's too easy to get wrong and it may be hard for another writer to understand your intent when they need to edit your article.</span></span>

<span data-ttu-id="3ebf1-192">語言指標是放置在開頭的三個倒引號之後，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="3ebf1-192">Language indicators are placed immediately after the opening triple-backticks, as in the following example:</span></span>

<span data-ttu-id="3ebf1-193">Markdown：</span><span class="sxs-lookup"><span data-stu-id="3ebf1-193">Markdown:</span></span>

```markdown
    ```json
    {
        "aggregator": {
            "batchSize": 1000,
            "flushTimeout": "00:00:30"
        }
    }
    ```
```

<span data-ttu-id="3ebf1-194">已轉譯：</span><span class="sxs-lookup"><span data-stu-id="3ebf1-194">Rendered:</span></span>

```json
{
    "aggregator": {
        "batchSize": 1000,
        "flushTimeout": "00:00:30"
    }
}
```

<span data-ttu-id="3ebf1-195">對於可作為語言指標使用的值，如需相關資訊，請參閱[語言名稱和別名](http://highlightjs.readthedocs.io/en/latest/css-classes-reference.html#language-names-and-aliases) \(英文\)。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-195">For information about the values you can use as language indicators, see [Language names and aliases](http://highlightjs.readthedocs.io/en/latest/css-classes-reference.html#language-names-and-aliases).</span></span>

<span data-ttu-id="3ebf1-196">如果您放在三個倒引號 (\`\`\`) 後的語言或環境字組不被支援，該字組會出現在轉譯頁面的程式碼區塊標題列中。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-196">If you use a language or environment word after the triple-backticks (\`\`\`) that isn't supported, that word appears in the code section title bar on the rendered page.</span></span> <span data-ttu-id="3ebf1-197">盡可能在內嵌程式碼區塊中使用語言或環境指標。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-197">Whenever possible, use a language or environment indicator in your inline code blocks.</span></span>

> [!NOTE]
> <span data-ttu-id="3ebf1-198">如果您從 Word 文件複製並貼上程式碼，請確定其中沒有任何「曲引號」(例如，`“` 和 `’`)，這些在程式碼中無效。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-198">If you copy and paste code from a Word document, make sure it has no "curly quotes," which aren't valid in code (for example, `“` and `’`).</span></span> <span data-ttu-id="3ebf1-199">如果有，請將它們變更成一般引號 (`'` 和 `"`)。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-199">If it does, change them back to normal quotes (`'` and `"`).</span></span> <span data-ttu-id="3ebf1-200">或者，依賴 Docs 編寫套件的[智慧引號取代功能](docs-authoring/smart-quote-replacement.md)。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-200">Alternatively, rely on the Docs Authoring Pack, [smart quotes replacement feature](docs-authoring/smart-quote-replacement.md).</span></span>

## <a name="in-repo-snippet-references"></a><span data-ttu-id="3ebf1-201">存放庫內的程式碼片段參考</span><span class="sxs-lookup"><span data-stu-id="3ebf1-201">In-repo snippet references</span></span>

<span data-ttu-id="3ebf1-202">想要在文件中包含程式設計語言的程式碼片段，建議透過參考程式碼檔案的方式。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-202">The preferred way to include code snippets for programming languages in docs is by reference to a code file.</span></span> <span data-ttu-id="3ebf1-203">這個方法讓您能夠反白顯示一至數行的程式碼，並讓 GitHub 上提供的程式碼片段範圍更廣，以利開發人員使用。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-203">This method gives you the ability to highlight lines of code and makes the wider context of the snippet available on GitHub for developers to use.</span></span> <span data-ttu-id="3ebf1-204">您可以手動方式使用三個冒號格式 (：\:\:)，或在 Visual Studio Code 中借助 [docs.microsoft.com 編寫套件](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)，來包含程式碼。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-204">You can include code by using the triple colon format (:\:\:) either manually or in Visual Studio Code with the help of the [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).</span></span>

1. <span data-ttu-id="3ebf1-205">在 Visual Studio Code 中，按一下 <kbd>Alt + M</kbd> 或 <kbd>選項 + M</kbd>，然後選取 [程式碼片段]。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-205">In Visual Studio Code, click <kbd>Alt + M</kbd> or <kbd>Option + M</kbd> and select Snippet.</span></span>
2. <span data-ttu-id="3ebf1-206">選取 [程式碼片段] 後，系統會提示您選取 [全文檢索搜尋]、[Scoped Search] \(限定範圍搜尋\) 或 [Cross-Repository Reference] \(跨存放庫參考\)。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-206">Once Snippet is selected, you will be prompted for Full Search, Scoped Search or Cross-Repository Reference.</span></span> <span data-ttu-id="3ebf1-207">若要在本機搜尋，選取 [全文檢索搜尋]。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-207">To search locally, select Full Search.</span></span>
3. <span data-ttu-id="3ebf1-208">輸入搜尋字詞以尋找檔案。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-208">Enter a search term to find the file.</span></span> <span data-ttu-id="3ebf1-209">找到檔案之後，請選取檔案。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-209">Once you've found the file, select the file.</span></span>
4. <span data-ttu-id="3ebf1-210">接下來，選取一個選項以決定應在程式碼片段中包含哪些程式碼。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-210">Next, select an option to determine which line(s) of code should be included in the snippet.</span></span> <span data-ttu-id="3ebf1-211">這些選項包括：[識別碼]  、[範圍]  和 [無]  。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-211">The options are: **ID**, **Range** and **None**.</span></span>
5. <span data-ttu-id="3ebf1-212">根據您在步驟 4 中的選擇，視需要提供值。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-212">Based on your selection from Step 4, provide a value if necessary.</span></span>

<span data-ttu-id="3ebf1-213">顯示完整程式碼檔案：</span><span class="sxs-lookup"><span data-stu-id="3ebf1-213">Display entire code file:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs":::
```

<span data-ttu-id="3ebf1-214">透過指定行號來顯示部分程式碼檔案：</span><span class="sxs-lookup"><span data-stu-id="3ebf1-214">Display part of a code file by specifying line numbers:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="3ebf1-215">透過指定程式碼片段名稱來顯示部分程式碼檔案：</span><span class="sxs-lookup"><span data-stu-id="3ebf1-215">Display part of a code file by specifying a snippet name:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

<span data-ttu-id="3ebf1-216">下列各節將說明這些範例：</span><span class="sxs-lookup"><span data-stu-id="3ebf1-216">The following sections explain these examples:</span></span>

* [<span data-ttu-id="3ebf1-217">使用程式碼檔案的相對路徑</span><span class="sxs-lookup"><span data-stu-id="3ebf1-217">Use a relative path to the code file</span></span>](#path-to-code-file)
* [<span data-ttu-id="3ebf1-218">僅包含選取的行號</span><span class="sxs-lookup"><span data-stu-id="3ebf1-218">Include only selected line numbers</span></span>](#selected-line-numbers)
* [<span data-ttu-id="3ebf1-219">參考具名的程式碼片段</span><span class="sxs-lookup"><span data-stu-id="3ebf1-219">Refer to a named snippet</span></span>](#named-snippet)
* [<span data-ttu-id="3ebf1-220">反白顯示選取的行</span><span class="sxs-lookup"><span data-stu-id="3ebf1-220">Highlight selected lines</span></span>](#highlighting-selected-lines)

<span data-ttu-id="3ebf1-221">如需詳細資訊，請參閱本文稍後的[程式碼片段語法參考](#snippet-syntax-reference)。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-221">For more information, see [Snippet syntax reference](#snippet-syntax-reference) later in this article.</span></span>

### <a name="path-to-code-file"></a><span data-ttu-id="3ebf1-222">程式碼檔案的路徑</span><span class="sxs-lookup"><span data-stu-id="3ebf1-222">Path to code file</span></span>

<span data-ttu-id="3ebf1-223">範例：</span><span class="sxs-lookup"><span data-stu-id="3ebf1-223">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="3ebf1-224">此範例是來自 ASP.NET 文件存放庫中的 [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md) \(英文\) 文章檔案。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-224">The example is from the ASP.NET docs repo, [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md) article file.</span></span> <span data-ttu-id="3ebf1-225">程式碼檔案的參考方式，是透過針對相同存放庫中 [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) 的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-225">The code file is referenced by a relative path to [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) in the same repository.</span></span>

### <a name="selected-line-numbers"></a><span data-ttu-id="3ebf1-226">選取的行號</span><span class="sxs-lookup"><span data-stu-id="3ebf1-226">Selected line numbers</span></span>

<span data-ttu-id="3ebf1-227">範例：</span><span class="sxs-lookup"><span data-stu-id="3ebf1-227">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="3ebf1-228">這個範例只顯示 *StudentController.cs* 程式碼檔案中的第 2-24 行和第 26 行。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-228">This example displays only lines 2-24 and 26 of the *StudentController.cs* code file.</span></span>

<span data-ttu-id="3ebf1-229">相較於硬式編碼的行號，請盡量使用具名程式碼片段，原因會於下一節中說明。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-229">Prefer named snippets over hard-coded line numbers, as explained in the next section.</span></span>

### <a name="named-snippet"></a><span data-ttu-id="3ebf1-230">具名的程式碼片段</span><span class="sxs-lookup"><span data-stu-id="3ebf1-230">Named snippet</span></span>

<span data-ttu-id="3ebf1-231">範例：</span><span class="sxs-lookup"><span data-stu-id="3ebf1-231">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

<span data-ttu-id="3ebf1-232">名稱只能使用字母和底線。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-232">Use only letters and underscores for the name.</span></span>

<span data-ttu-id="3ebf1-233">此範例會顯示程式碼檔案的 `snippet_Create` 區段。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-233">The example displays the `snippet_Create` section of the code file.</span></span> <span data-ttu-id="3ebf1-234">這個範例的程式碼檔案會在 C# 的程式碼註解中放上程式碼片段標記：</span><span class="sxs-lookup"><span data-stu-id="3ebf1-234">The code file for this example has snippet tags in comments in the C# code:</span></span>

```cs
// code excluded from the snippet
// <snippet_Create>
// code included in the snippet
// </snippet_Create>
// code excluded from the snippet
```

<span data-ttu-id="3ebf1-235">請盡可能參考具名的區段，而非指定行號。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-235">Whenever you can, refer to a named section rather than specifying line numbers.</span></span> <span data-ttu-id="3ebf1-236">行號參考較容易出錯，因為程式碼檔案終究會變更，進而使行號產生變更。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-236">Line number references are brittle because code files inevitably change in ways that make line numbers change.</span></span>
<span data-ttu-id="3ebf1-237">而您不一定會收到這些變更的通知。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-237">You don't necessarily get notified of such changes.</span></span> <span data-ttu-id="3ebf1-238">您的文章最後會開始顯示錯誤的程式碼行，且您將不會意識到這項變更。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-238">Your article eventually starts showing the wrong lines and you have no clue anything has changed.</span></span>

### <a name="highlighting-selected-lines"></a><span data-ttu-id="3ebf1-239">反白顯示選取的行</span><span class="sxs-lookup"><span data-stu-id="3ebf1-239">Highlighting selected lines</span></span>

<span data-ttu-id="3ebf1-240">範例：</span><span class="sxs-lookup"><span data-stu-id="3ebf1-240">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26" highlight="2,5":::
```

<span data-ttu-id="3ebf1-241">此範例會反白顯示行 2 和 5，這是從顯示的程式碼片段開頭開始計算。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-241">The example highlights lines 2 and 5, counting from the start of the displayed snippet.</span></span> <span data-ttu-id="3ebf1-242">要反白顯示的行號並不是從程式碼檔案的開頭開始計算。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-242">Line numbers to highlight don't count from the start of the code file.</span></span> <span data-ttu-id="3ebf1-243">換句話說，系統會醒目提示程式碼檔案的第 3 行和第 6 行。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-243">In other words, lines 3 and 6 of the code file are highlighted.</span></span>

## <a name="out-of-repo-snippet-references"></a><span data-ttu-id="3ebf1-244">存放庫外的程式碼片段參考</span><span class="sxs-lookup"><span data-stu-id="3ebf1-244">Out-of-repo snippet references</span></span>

<span data-ttu-id="3ebf1-245">若您想要參考的程式碼檔案位於另一個存放庫，請將該程式碼存放庫設定為「相依存放庫」  。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-245">If the code file you want to reference is in a different repository, set up the code repository as a *dependent repository*.</span></span> <span data-ttu-id="3ebf1-246">這麼做時，便需要為它指定名稱。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-246">When you do that, you specify a name for it.</span></span> <span data-ttu-id="3ebf1-247">接著，基於程式碼參考的目的，該名稱會被作為資料夾名稱使用。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-247">That name then acts like a folder name for purposes of code references.</span></span>

<span data-ttu-id="3ebf1-248">例如，文件存放庫為 *Azure/azure-docs*，且程式碼存放庫為 *Azure/azure-functions-durable-extension*。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-248">For example, the docs repository is *Azure/azure-docs*, and the code repository is *Azure/azure-functions-durable-extension*.</span></span>

<span data-ttu-id="3ebf1-249">在 *azure-docs* 的根資料夾中，新增 *.openpublishing.publish.config.json* 中的下列區段：</span><span class="sxs-lookup"><span data-stu-id="3ebf1-249">In the root folder of *azure-docs*, add the following section in *.openpublishing.publish.config.json*:</span></span>

```json
    {
      "path_to_root": "samples-durable-functions",
      "url": "https://github.com/Azure/azure-functions-durable-extension",
      "branch": "master",
      "branch_mapping": {}
    },
```

<span data-ttu-id="3ebf1-250">現在，當您以 azure-docs  中資料夾的形式參考 sample-durable-functions  時，實際上是在參考 azure-functions-durable-extension  存放庫中的根資料夾。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-250">Now when you refer to *samples-durable-functions* as if it were a folder in *azure-docs*, you're actually referring to the root folder in the *azure-functions-durable-extension* repository.</span></span>

<span data-ttu-id="3ebf1-251">您可以手動方式使用三個冒號格式 (：\:\:)，或在 Visual Studio Code 中借助 [docs.microsoft.com 編寫套件](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)，來包含程式碼。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-251">You can include code by using the triple colon format (:\:\:) either manually or in Visual Studio Code with the help of the [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).</span></span>

1. <span data-ttu-id="3ebf1-252">在 Visual Studio Code 中，按一下 <kbd>Alt + M</kbd> 或 <kbd>選項 + M</kbd>，然後選取 [程式碼片段]。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-252">In Visual Studio Code, click <kbd>Alt + M</kbd> or <kbd>Option + M</kbd> and select Snippet.</span></span>
2. <span data-ttu-id="3ebf1-253">選取 [程式碼片段] 後，系統會提示您選取 [全文檢索搜尋]、[Scoped Search] \(限定範圍搜尋\) 或 [Cross-Repository Reference] \(跨存放庫參考\)。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-253">Once Snippet is selected, you will be prompted for Full Search, Scoped Search or Cross-Repository Reference.</span></span> <span data-ttu-id="3ebf1-254">若要搜尋不同的存放庫，請選取 [Cross-Repository Reference] \(跨存放庫參考\)。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-254">To search across repositories, select Cross-Repository Reference.</span></span>
3. <span data-ttu-id="3ebf1-255">*.openpublishing.publish.config.json* 會提供您存放庫選項。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-255">You will be given a selection of repositories that are in *.openpublishing.publish.config.json*.</span></span> <span data-ttu-id="3ebf1-256">選取存放庫。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-256">Select a repository.</span></span>
4. <span data-ttu-id="3ebf1-257">輸入搜尋字詞以尋找檔案。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-257">Enter a search term to find the file.</span></span> <span data-ttu-id="3ebf1-258">找到檔案之後，請選取檔案。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-258">Once you've found the file, select the file.</span></span>
5. <span data-ttu-id="3ebf1-259">接下來，選取一個選項以決定應在程式碼片段中包含哪些程式碼。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-259">Next, select an option to determine which line(s) of code should be included in the snippet.</span></span> <span data-ttu-id="3ebf1-260">這些選項包括：[識別碼]  、[範圍]  和 [無]  。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-260">The options are: **ID**, **Range** and **None**.</span></span>
6. <span data-ttu-id="3ebf1-261">根據您在步驟 5 中的選擇提供值。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-261">Based on your selection from Step 5, provide a value.</span></span>

<span data-ttu-id="3ebf1-262">您的程式碼片段參考看起來如下：</span><span class="sxs-lookup"><span data-stu-id="3ebf1-262">Your snippet reference will look like this:</span></span>

```markdown
:::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
```

<span data-ttu-id="3ebf1-263">在 *azure-functions-durable-extension* 存放庫中，該程式碼檔案是位於 *samples/csx/shared* 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-263">In the *azure-functions-durable-extension* repository, that code file is in the *samples/csx/shared* folder.</span></span> <span data-ttu-id="3ebf1-264">如[先前所述](#highlighting-selected-lines)，反白顯示行的行號是相對於程式碼片段開頭，而不是檔案的開頭。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-264">As noted [earlier](#highlighting-selected-lines), line numbers for highlighting are relative to the start of the snippet rather than the start of the file.</span></span>

> [!NOTE]
> <span data-ttu-id="3ebf1-265">您指派給相依存放庫的名稱是相對於主要存放庫的根目錄，但波狀符號 (~) 則是指文件集的根目錄。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-265">The name you assign to the dependent repository is relative to the root of the main repository, but the tilde (~) refers to the root of the doc set.</span></span> <span data-ttu-id="3ebf1-266">文件集根目錄是由 .openpublishing.publish.config.json  中的 `build_source_folder` 決定。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-266">The doc set root is determined by `build_source_folder` in *.openpublishing.publish.config.json*.</span></span> <span data-ttu-id="3ebf1-267">在上述範例中，程式碼片段的路徑適用於 azure-docs 檔存放庫，因為 `build_source_folder` 是指存放庫根目錄 (`.`)。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-267">The path to the snippet in the preceding example works in the azure-docs repo because `build_source_folder` refers to the repo root (`.`).</span></span> <span data-ttu-id="3ebf1-268">如果 `build_source_folder` 是 `articles`，路徑的開頭會是 `~/../samples-durable-functions`，而不是 `~/samples-durable-functions`。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-268">If `build_source_folder` were `articles`, the path would start with `~/../samples-durable-functions` instead of `~/samples-durable-functions`.</span></span>

## <a name="interactive-code-snippets"></a><span data-ttu-id="3ebf1-269">互動式程式碼片段</span><span class="sxs-lookup"><span data-stu-id="3ebf1-269">Interactive code snippets</span></span>

### <a name="inline-interactive-code-blocks"></a><span data-ttu-id="3ebf1-270">內嵌互動式程式碼區塊</span><span class="sxs-lookup"><span data-stu-id="3ebf1-270">Inline interactive code blocks</span></span>

<span data-ttu-id="3ebf1-271">針對下列語言，可以使程式碼片段能在瀏覽器視窗中執行：</span><span class="sxs-lookup"><span data-stu-id="3ebf1-271">For the following languages, code snippets can be made executable in the browser window:</span></span>

* <span data-ttu-id="3ebf1-272">Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="3ebf1-272">Azure Cloud Shell</span></span>
* <span data-ttu-id="3ebf1-273">Azure PowerShell Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="3ebf1-273">Azure PowerShell Cloud Shell</span></span>
* <span data-ttu-id="3ebf1-274">C# REPL</span><span class="sxs-lookup"><span data-stu-id="3ebf1-274">C# REPL</span></span>

<span data-ttu-id="3ebf1-275">在啟用互動模式的情況下，所呈現的程式碼方塊會顯示 [試試看]  或 [執行]  按鈕。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-275">When interactive mode is enabled, the rendered code boxes have a **Try It** or **Run** button.</span></span> <span data-ttu-id="3ebf1-276">例如：</span><span class="sxs-lookup"><span data-stu-id="3ebf1-276">For example:</span></span>

```markdown
    ```azurepowershell-interactive
    New-AzResourceGroup -Name myResourceGroup -Location westeurope
    ```
```

<span data-ttu-id="3ebf1-277">會轉譯為：</span><span class="sxs-lookup"><span data-stu-id="3ebf1-277">renders as follows:</span></span>

```azurepowershell-interactive
New-AzResourceGroup -Name myResourceGroup -Location westeurope
```

<span data-ttu-id="3ebf1-278">若要針對特定程式碼區塊開啟此功能，請使用特殊的語言識別項。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-278">To turn on this feature for a particular code block, use a special language identifier.</span></span> <span data-ttu-id="3ebf1-279">可用的選項包括：</span><span class="sxs-lookup"><span data-stu-id="3ebf1-279">The available options are:</span></span>

* <span data-ttu-id="3ebf1-280">`azurepowershell-interactive` - 啟用 Azure PowerShell Cloud Shell，如上述範例所示</span><span class="sxs-lookup"><span data-stu-id="3ebf1-280">`azurepowershell-interactive` - Enables the Azure PowerShell Cloud Shell, as in the preceding example</span></span>
* <span data-ttu-id="3ebf1-281">`azurecli-interactive` - 啟用 Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="3ebf1-281">`azurecli-interactive` - Enables the Azure Cloud Shell</span></span>
* <span data-ttu-id="3ebf1-282">`csharp-interactive` - 啟用 C# REPL</span><span class="sxs-lookup"><span data-stu-id="3ebf1-282">`csharp-interactive` - Enables the C# REPL</span></span>

<span data-ttu-id="3ebf1-283">針對 Azure Cloud Shell 和 PowerShell Cloud Shell，使用者可以僅針對其 Azure 帳戶執行命令。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-283">For the Azure Cloud Shell and PowerShell Cloud Shell, users can run commands against only their own Azure account.</span></span>

### <a name="code-snippets-included-by-reference"></a><span data-ttu-id="3ebf1-284">以參考方式包含程式碼片段</span><span class="sxs-lookup"><span data-stu-id="3ebf1-284">Code snippets included by reference</span></span>

<span data-ttu-id="3ebf1-285">您可以針對依參考所包含的程式碼片段啟用互動模式。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-285">You can enable interactive mode for code snippets included by reference.</span></span> <span data-ttu-id="3ebf1-286">以下為範例：</span><span class="sxs-lookup"><span data-stu-id="3ebf1-286">Here are examples:</span></span>

```markdown
:::code source="PowerShell.ps1" interactive="cloudshell-powershell":::
```

```markdown
:::code source="Bash.sh" interactive="cloudshell-bash":::
```

<span data-ttu-id="3ebf1-287">若要針對特定程式碼區塊開啟此功能，請使用 `interactive` 屬性。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-287">To turn on this feature for a particular code block, use the `interactive` attribute.</span></span> <span data-ttu-id="3ebf1-288">可用的屬性值如下：</span><span class="sxs-lookup"><span data-stu-id="3ebf1-288">The available attribute values are:</span></span>

* <span data-ttu-id="3ebf1-289">`cloudshell-powershell` - 啟用 Azure PowerShell Cloud Shell，如上述範例所示</span><span class="sxs-lookup"><span data-stu-id="3ebf1-289">`cloudshell-powershell` - Enables the Azure PowerShell Cloud Shell, as in the preceding example</span></span>
* <span data-ttu-id="3ebf1-290">`cloudshell-bash` - 啟用 Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="3ebf1-290">`cloudshell-bash` - Enables the Azure Cloud Shell</span></span>
* <span data-ttu-id="3ebf1-291">`try-dotnet` - 啟用 .NET Interactive</span><span class="sxs-lookup"><span data-stu-id="3ebf1-291">`try-dotnet` - Enables .NET Interactive</span></span>
* <span data-ttu-id="3ebf1-292">`try-dotnet-class` - 啟用具有類別 Scaffolding 的 .NET Interactive</span><span class="sxs-lookup"><span data-stu-id="3ebf1-292">`try-dotnet-class` - Enables .NET Interactive with class scaffolding</span></span>
* <span data-ttu-id="3ebf1-293">`try-dotnet-method` - 啟用具有方法 Scaffolding 的 .NET Interactive</span><span class="sxs-lookup"><span data-stu-id="3ebf1-293">`try-dotnet-method` - Enables .NET Interactive with method scaffolding</span></span>

<span data-ttu-id="3ebf1-294">針對 Azure Cloud Shell 和 PowerShell Cloud Shell，使用者可以僅針對其 Azure 帳戶執行命令。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-294">For the Azure Cloud Shell and PowerShell Cloud Shell, users can only run commands against their own Azure account.</span></span>

<span data-ttu-id="3ebf1-295">針對 .NET Interactive 體驗，您程式碼區塊的內容取決於您選擇三個 Scaffolding 體驗的其中一個：</span><span class="sxs-lookup"><span data-stu-id="3ebf1-295">For the .NET Interactive experience, the contents of your code block depends on which of the three scaffolding experiences you choose:</span></span>

* <span data-ttu-id="3ebf1-296">*無 scaffolding* (`try-dotnet`)：程式碼區塊應該代表完整程式文字。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-296">*No scaffolding* (`try-dotnet`): The code block should represent a full program text.</span></span> <span data-ttu-id="3ebf1-297">例如，由 `dotnet new console` 產生的*Program.cs* 檔案將會有效。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-297">For example, the *Program.cs* file generated by `dotnet new console` would be valid.</span></span> <span data-ttu-id="3ebf1-298">這些最適合用來顯示整個小程式，包括所需的 `using` 指示詞。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-298">These are most useful to show an entire small program, including the `using` directives needed.</span></span> <span data-ttu-id="3ebf1-299">目前不支援頂層陳述式。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-299">Top level statements are not supported at this time.</span></span>
* <span data-ttu-id="3ebf1-300">*方法 Scaffolding* (`try-dotnet-method`)：程式碼區塊應該代表主控台應用程式中 `Main` 方法的內容。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-300">*Method scaffolding* (`try-dotnet-method`): The code block should represent the content of a `Main` method in a console application.</span></span> <span data-ttu-id="3ebf1-301">您可以假設 `using` 指示詞由 `dotnet new console` 範本新增。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-301">You can assume the `using` directives added by the `dotnet new console` template.</span></span> <span data-ttu-id="3ebf1-302">此設定最適合用於示範單一功能的簡短程式碼片段。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-302">This setting is most useful for short snippets that demonstrate one feature.</span></span>
* <span data-ttu-id="3ebf1-303">*類別 Scaffolding* (`try-dotnet-class`)：程式碼區塊應該代表具有作為程式進入點之 `Main` 方法的類別。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-303">*Class scaffolding* (`try-dotnet-class`): The code block should represent a class with a `Main` method as the program entry point.</span></span> <span data-ttu-id="3ebf1-304">這些可用來顯示類別成員的互動方式。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-304">These can be used to show how members of a class interact.</span></span>

## <a name="snippet-syntax-reference"></a><span data-ttu-id="3ebf1-305">程式碼片段語法參考</span><span class="sxs-lookup"><span data-stu-id="3ebf1-305">Snippet syntax reference</span></span>

<span data-ttu-id="3ebf1-306">語法：</span><span class="sxs-lookup"><span data-stu-id="3ebf1-306">Syntax:</span></span>

```md
:::code language="<language>" source="<path>" <attribute>="<attribute-value>":::
```

> [!IMPORTANT]
> <span data-ttu-id="3ebf1-307">此語法是區塊 Markdown 延伸。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-307">This syntax is a block Markdown extension.</span></span> <span data-ttu-id="3ebf1-308">必須用於本身的行。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-308">It must be used on its own line.</span></span>

* <span data-ttu-id="3ebf1-309">`<language>` (選擇性)</span><span class="sxs-lookup"><span data-stu-id="3ebf1-309">`<language>` (*optional*)</span></span>
  * <span data-ttu-id="3ebf1-310">程式碼片段的語言。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-310">Language of the code snippet.</span></span> <span data-ttu-id="3ebf1-311">如需詳細資訊，請參閱本文稍後的＜支援的語言＞[](#supported-languages)一節。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-311">For more information, see the [Supported languages](#supported-languages) section later in this article.</span></span>

* <span data-ttu-id="3ebf1-312">`<path>` (強制)</span><span class="sxs-lookup"><span data-stu-id="3ebf1-312">`<path>` (*mandatory*)</span></span>
  * <span data-ttu-id="3ebf1-313">檔案系統中的相對路徑，表示要參考的程式碼片段檔案。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-313">Relative path in the file system that indicates the code snippet file to reference.</span></span>

* <span data-ttu-id="3ebf1-314">`<attribute>` 和 `<attribute-value>` (選擇性\*\*)</span><span class="sxs-lookup"><span data-stu-id="3ebf1-314">`<attribute>` and `<attribute-value>` (*optional*)</span></span>

  <span data-ttu-id="3ebf1-315">同時使用以指定從檔案擷取程式碼的方式以及如何顯示程式碼：</span><span class="sxs-lookup"><span data-stu-id="3ebf1-315">Used together to specify how the code should be retrieved from the file and how it should be displayed:</span></span>

  * <span data-ttu-id="3ebf1-316">`range`：`1,3-5`行的範圍。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-316">`range`: `1,3-5` A range of lines.</span></span> <span data-ttu-id="3ebf1-317">此範例包含第 1、3、4 及 5 行。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-317">This example includes lines 1, 3, 4, and 5.</span></span>
  * <span data-ttu-id="3ebf1-318">`id`：`snippet_Create` 需要從程式碼檔案插入的程式碼片段識別碼。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-318">`id`: `snippet_Create` The ID of the snippet that needs to be inserted from the code file.</span></span> <span data-ttu-id="3ebf1-319">這個值與範圍不能並存。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-319">This value cannot co-exist with range.</span></span>
  * <span data-ttu-id="3ebf1-320">`highlight`：`2-4,6` 需要在產生的程式碼片段中醒目提示的範圍及/或行數。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-320">`highlight`: `2-4,6` Range and/or numbers of lines that need to be highlighted in the generated code snippet.</span></span> <span data-ttu-id="3ebf1-321">編號是相對於顯示的行 (如範圍或識別碼所指定)，而不是檔案。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-321">The numbering is relative to the lines displayed (as specified by range or id), not the file.</span></span>
  * <span data-ttu-id="3ebf1-322">`interactive`：`cloudshell-powershell`、`cloudshell-bash`、`try-dotnet`、`try-dotnet-class`、`try-dotnet-method` 字串值決定啟用的互動功能類型。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-322">`interactive`: `cloudshell-powershell`, `cloudshell-bash`, `try-dotnet`, `try-dotnet-class`, `try-dotnet-method` String value determines what kinds of interactivity are enabled.</span></span>
  * <span data-ttu-id="3ebf1-323">如需程式碼片段原始程式檔中依語言分類的標籤名稱表示法詳細資料，請參閱 [DocFX 指南](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file)。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-323">For details about tag name representation in code snippet source files by language, see the [DocFX guidelines](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file).</span></span>

## <a name="supported-languages"></a><span data-ttu-id="3ebf1-324">支援的語言</span><span class="sxs-lookup"><span data-stu-id="3ebf1-324">Supported languages</span></span>

<span data-ttu-id="3ebf1-325">[Docs 編寫套件](how-to-write-docs-auth-pack.md) 有一項功能，可提供陳述式完成和驗證程式碼隔離區塊的可用語言識別碼。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-325">The [Docs Authoring Pack](how-to-write-docs-auth-pack.md) includes a feature to provide statement completion and validation of the available language identifiers for code fence blocks.</span></span>

### <a name="fenced-code-blocks"></a><span data-ttu-id="3ebf1-326">隔離的程式碼區塊</span><span class="sxs-lookup"><span data-stu-id="3ebf1-326">Fenced code blocks</span></span>

| <span data-ttu-id="3ebf1-327">名稱</span><span class="sxs-lookup"><span data-stu-id="3ebf1-327">Name</span></span>                           | <span data-ttu-id="3ebf1-328">有效的別名</span><span class="sxs-lookup"><span data-stu-id="3ebf1-328">Valid aliases</span></span>                                                                  |
|--------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="3ebf1-329">.NET Core CLI</span><span class="sxs-lookup"><span data-stu-id="3ebf1-329">.NET Core CLI</span></span>                  | `dotnetcli`                                                                    |
| <span data-ttu-id="3ebf1-330">1C</span><span class="sxs-lookup"><span data-stu-id="3ebf1-330">1C</span></span>                             | `1c`                                                                           |
| <span data-ttu-id="3ebf1-331">ABNF</span><span class="sxs-lookup"><span data-stu-id="3ebf1-331">ABNF</span></span>                           | `abnf`                                                                         |
| <span data-ttu-id="3ebf1-332">存取記錄</span><span class="sxs-lookup"><span data-stu-id="3ebf1-332">Access logs</span></span>                    | `accesslog`                                                                    |
| <span data-ttu-id="3ebf1-333">Ada</span><span class="sxs-lookup"><span data-stu-id="3ebf1-333">Ada</span></span>                            | `ada`                                                                          |
| <span data-ttu-id="3ebf1-334">XML 組譯工具</span><span class="sxs-lookup"><span data-stu-id="3ebf1-334">ARM assembler</span></span>                  | <span data-ttu-id="3ebf1-335">`armasm`, `arm`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-335">`armasm`, `arm`</span></span>                                                                |
| <span data-ttu-id="3ebf1-336">AVR 組譯工具</span><span class="sxs-lookup"><span data-stu-id="3ebf1-336">AVR assembler</span></span>                  | `avrasm`                                                                       |
| <span data-ttu-id="3ebf1-337">ActionScript</span><span class="sxs-lookup"><span data-stu-id="3ebf1-337">ActionScript</span></span>                   | <span data-ttu-id="3ebf1-338">`actionscript`, `as`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-338">`actionscript`, `as`</span></span>                                                           |
| <span data-ttu-id="3ebf1-339">Alan</span><span class="sxs-lookup"><span data-stu-id="3ebf1-339">Alan</span></span>                           | <span data-ttu-id="3ebf1-340">`alan`, `i`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-340">`alan`, `i`</span></span>                                                                    |
| <span data-ttu-id="3ebf1-341">AngelScript</span><span class="sxs-lookup"><span data-stu-id="3ebf1-341">AngelScript</span></span>                    | <span data-ttu-id="3ebf1-342">`angelscript`, `asc`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-342">`angelscript`, `asc`</span></span>                                                           |
| <span data-ttu-id="3ebf1-343">ANTLR</span><span class="sxs-lookup"><span data-stu-id="3ebf1-343">ANTLR</span></span>                          | `antlr`                                                                        |
| <span data-ttu-id="3ebf1-344">Apache</span><span class="sxs-lookup"><span data-stu-id="3ebf1-344">Apache</span></span>                         | <span data-ttu-id="3ebf1-345">`apache`, `apacheconf`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-345">`apache`, `apacheconf`</span></span>                                                         |
| <span data-ttu-id="3ebf1-346">AppleScript</span><span class="sxs-lookup"><span data-stu-id="3ebf1-346">AppleScript</span></span>                    | <span data-ttu-id="3ebf1-347">`applescript`, `osascript`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-347">`applescript`, `osascript`</span></span>                                                     |
| <span data-ttu-id="3ebf1-348">大型電玩</span><span class="sxs-lookup"><span data-stu-id="3ebf1-348">Arcade</span></span>                         | `arcade`                                                                       |
| <span data-ttu-id="3ebf1-349">AsciiDoc</span><span class="sxs-lookup"><span data-stu-id="3ebf1-349">AsciiDoc</span></span>                       | <span data-ttu-id="3ebf1-350">`asciidoc`, `adoc`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-350">`asciidoc`, `adoc`</span></span>                                                             |
| <span data-ttu-id="3ebf1-351">AspectJ</span><span class="sxs-lookup"><span data-stu-id="3ebf1-351">AspectJ</span></span>                        | `aspectj`                                                                      |
| <span data-ttu-id="3ebf1-352">ASPX</span><span class="sxs-lookup"><span data-stu-id="3ebf1-352">ASPX</span></span>                           | `aspx`                                                                         |
| <span data-ttu-id="3ebf1-353">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="3ebf1-353">ASP.NET (C#)</span></span>                   | `aspx-csharp`                                                                  |
| <span data-ttu-id="3ebf1-354">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="3ebf1-354">ASP.NET (VB)</span></span>                   | `aspx-vb`                                                                      |
| <span data-ttu-id="3ebf1-355">AutoHotkey</span><span class="sxs-lookup"><span data-stu-id="3ebf1-355">AutoHotkey</span></span>                     | `autohotkey`                                                                   |
| <span data-ttu-id="3ebf1-356">AutoIt</span><span class="sxs-lookup"><span data-stu-id="3ebf1-356">AutoIt</span></span>                         | `autoit`                                                                       |
| <span data-ttu-id="3ebf1-357">Awk</span><span class="sxs-lookup"><span data-stu-id="3ebf1-357">Awk</span></span>                            | <span data-ttu-id="3ebf1-358">`awk`, `mawk`, `nawk`, `gawk`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-358">`awk`, `mawk`, `nawk`, `gawk`</span></span>                                                  |
| <span data-ttu-id="3ebf1-359">Axapta</span><span class="sxs-lookup"><span data-stu-id="3ebf1-359">Axapta</span></span>                         | `axapta`                                                                       |
| <span data-ttu-id="3ebf1-360">AzCopy</span><span class="sxs-lookup"><span data-stu-id="3ebf1-360">AzCopy</span></span>                         | `azcopy`                                                                       |
| <span data-ttu-id="3ebf1-361">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="3ebf1-361">Azure CLI</span></span>                      | `azurecli`                                                                     |
| <span data-ttu-id="3ebf1-362">Azure CLI (互動式)</span><span class="sxs-lookup"><span data-stu-id="3ebf1-362">Azure CLI (Interactive)</span></span>        | `azurecli-interactive`                                                         |
| <span data-ttu-id="3ebf1-363">Azure Powershell</span><span class="sxs-lookup"><span data-stu-id="3ebf1-363">Azure Powershell</span></span>               | `azurepowershell`                                                              |
| <span data-ttu-id="3ebf1-364">Azure Powershell (互動式)</span><span class="sxs-lookup"><span data-stu-id="3ebf1-364">Azure Powershell (Interactive)</span></span> | `azurepowershell-interactive`                                                  |
| <span data-ttu-id="3ebf1-365">Bash</span><span class="sxs-lookup"><span data-stu-id="3ebf1-365">Bash</span></span>                           | <span data-ttu-id="3ebf1-366">`bash`, `sh`, `zsh`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-366">`bash`, `sh`, `zsh`</span></span>                                                            |
| <span data-ttu-id="3ebf1-367">基本</span><span class="sxs-lookup"><span data-stu-id="3ebf1-367">Basic</span></span>                          | `basic`                                                                        |
| <span data-ttu-id="3ebf1-368">BNF</span><span class="sxs-lookup"><span data-stu-id="3ebf1-368">BNF</span></span>                            | `bnf`                                                                          |
| <span data-ttu-id="3ebf1-369">C</span><span class="sxs-lookup"><span data-stu-id="3ebf1-369">C</span></span>                              | `c`                                                                            |
| <span data-ttu-id="3ebf1-370">C#</span><span class="sxs-lookup"><span data-stu-id="3ebf1-370">C#</span></span>                             | <span data-ttu-id="3ebf1-371">`csharp`, `cs`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-371">`csharp`, `cs`</span></span>                                                                 |
| <span data-ttu-id="3ebf1-372">C# (互動式)</span><span class="sxs-lookup"><span data-stu-id="3ebf1-372">C# (Interactive)</span></span>               | `csharp-interactive`                                                           |
| <span data-ttu-id="3ebf1-373">C++</span><span class="sxs-lookup"><span data-stu-id="3ebf1-373">C++</span></span>                            | <span data-ttu-id="3ebf1-374">`cpp`, `c`, `cc`, `h`, `c++`, `h++`, `hpp`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-374">`cpp`, `c`, `cc`, `h`, `c++`, `h++`, `hpp`</span></span>                                     |
| <span data-ttu-id="3ebf1-375">C++/CX</span><span class="sxs-lookup"><span data-stu-id="3ebf1-375">C++/CX</span></span>                         | `cppcx`                                                                        |
| <span data-ttu-id="3ebf1-376">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="3ebf1-376">C++/WinRT</span></span>                      | `cppwinrt`                                                                     |
| <span data-ttu-id="3ebf1-377">C/AL</span><span class="sxs-lookup"><span data-stu-id="3ebf1-377">C/AL</span></span>                           | `cal`                                                                          |
| <span data-ttu-id="3ebf1-378">Cache Object Script</span><span class="sxs-lookup"><span data-stu-id="3ebf1-378">Cache Object Script</span></span>            | <span data-ttu-id="3ebf1-379">`cos`, `cls`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-379">`cos`, `cls`</span></span>                                                                   |
| <span data-ttu-id="3ebf1-380">CMake</span><span class="sxs-lookup"><span data-stu-id="3ebf1-380">CMake</span></span>                          | <span data-ttu-id="3ebf1-381">`cmake`, `cmake.in`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-381">`cmake`, `cmake.in`</span></span>                                                            |
| <span data-ttu-id="3ebf1-382">Coq</span><span class="sxs-lookup"><span data-stu-id="3ebf1-382">Coq</span></span>                            | `coq`                                                                          |
| <span data-ttu-id="3ebf1-383">CSP</span><span class="sxs-lookup"><span data-stu-id="3ebf1-383">CSP</span></span>                            | `csp`                                                                          |
| <span data-ttu-id="3ebf1-384">CSS</span><span class="sxs-lookup"><span data-stu-id="3ebf1-384">CSS</span></span>                            | `css`                                                                          |
| <span data-ttu-id="3ebf1-385">Cap'n Proto</span><span class="sxs-lookup"><span data-stu-id="3ebf1-385">Cap'n Proto</span></span>                    | <span data-ttu-id="3ebf1-386">`capnproto`, `capnp`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-386">`capnproto`, `capnp`</span></span>                                                           |
| <span data-ttu-id="3ebf1-387">Clojure</span><span class="sxs-lookup"><span data-stu-id="3ebf1-387">Clojure</span></span>                        | <span data-ttu-id="3ebf1-388">`clojure`, `clj`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-388">`clojure`, `clj`</span></span>                                                               |
| <span data-ttu-id="3ebf1-389">CoffeeScript</span><span class="sxs-lookup"><span data-stu-id="3ebf1-389">CoffeeScript</span></span>                   | <span data-ttu-id="3ebf1-390">`coffeescript`, `coffee`, `cson`, `iced`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-390">`coffeescript`, `coffee`, `cson`, `iced`</span></span>                                       |
| <span data-ttu-id="3ebf1-391">Crmsh</span><span class="sxs-lookup"><span data-stu-id="3ebf1-391">Crmsh</span></span>                          | <span data-ttu-id="3ebf1-392">`crmsh`, `crm`, `pcmk`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-392">`crmsh`, `crm`, `pcmk`</span></span>                                                         |
| <span data-ttu-id="3ebf1-393">Crystal</span><span class="sxs-lookup"><span data-stu-id="3ebf1-393">Crystal</span></span>                        | <span data-ttu-id="3ebf1-394">`crystal`, `cr`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-394">`crystal`, `cr`</span></span>                                                                |
| <span data-ttu-id="3ebf1-395">Cypher (Neo4j)</span><span class="sxs-lookup"><span data-stu-id="3ebf1-395">Cypher (Neo4j)</span></span>                 | `cypher`                                                                       |
| <span data-ttu-id="3ebf1-396">D</span><span class="sxs-lookup"><span data-stu-id="3ebf1-396">D</span></span>                              | `d`                                                                            |
| <span data-ttu-id="3ebf1-397">DAX Power BI</span><span class="sxs-lookup"><span data-stu-id="3ebf1-397">DAX Power BI</span></span>                   | `dax`                                                                          |
| <span data-ttu-id="3ebf1-398">DNS Zone 檔案</span><span class="sxs-lookup"><span data-stu-id="3ebf1-398">DNS Zone file</span></span>                  | <span data-ttu-id="3ebf1-399">`dns`, `zone`, `bind`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-399">`dns`, `zone`, `bind`</span></span>                                                          |
| <span data-ttu-id="3ebf1-400">DOS</span><span class="sxs-lookup"><span data-stu-id="3ebf1-400">DOS</span></span>                            | <span data-ttu-id="3ebf1-401">`dos`, `bat`, `cmd`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-401">`dos`, `bat`, `cmd`</span></span>                                                            |
| <span data-ttu-id="3ebf1-402">Dart</span><span class="sxs-lookup"><span data-stu-id="3ebf1-402">Dart</span></span>                           | `dart`                                                                         |
| <span data-ttu-id="3ebf1-403">Delphi</span><span class="sxs-lookup"><span data-stu-id="3ebf1-403">Delphi</span></span>                         | <span data-ttu-id="3ebf1-404">`delphi`, `dpr`, `dfm`, `pas`, `pascal`, `freepascal`, `lazarus`, `lpr`, `lfm`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-404">`delphi`, `dpr`, `dfm`, `pas`, `pascal`, `freepascal`, `lazarus`, `lpr`, `lfm`</span></span> |
| <span data-ttu-id="3ebf1-405">Diff</span><span class="sxs-lookup"><span data-stu-id="3ebf1-405">Diff</span></span>                           | <span data-ttu-id="3ebf1-406">`diff`, `patch`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-406">`diff`, `patch`</span></span>                                                                |
| <span data-ttu-id="3ebf1-407">Django</span><span class="sxs-lookup"><span data-stu-id="3ebf1-407">Django</span></span>                         | <span data-ttu-id="3ebf1-408">`django`, `jinja`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-408">`django`, `jinja`</span></span>                                                              |
| <span data-ttu-id="3ebf1-409">Dockerfile</span><span class="sxs-lookup"><span data-stu-id="3ebf1-409">Dockerfile</span></span>                     | <span data-ttu-id="3ebf1-410">`dockerfile`, `docker`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-410">`dockerfile`, `docker`</span></span>                                                         |
| <span data-ttu-id="3ebf1-411">dsconfig</span><span class="sxs-lookup"><span data-stu-id="3ebf1-411">dsconfig</span></span>                       | `dsconfig`                                                                     |
| <span data-ttu-id="3ebf1-412">DTS (裝置樹狀目錄)</span><span class="sxs-lookup"><span data-stu-id="3ebf1-412">DTS (Device Tree)</span></span>              | `dts`                                                                          |
| <span data-ttu-id="3ebf1-413">Dust</span><span class="sxs-lookup"><span data-stu-id="3ebf1-413">Dust</span></span>                           | <span data-ttu-id="3ebf1-414">`dust`, `dst`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-414">`dust`, `dst`</span></span>                                                                  |
| <span data-ttu-id="3ebf1-415">Dylan</span><span class="sxs-lookup"><span data-stu-id="3ebf1-415">Dylan</span></span>                          | `dylan`                                                                        |
| <span data-ttu-id="3ebf1-416">EBNF</span><span class="sxs-lookup"><span data-stu-id="3ebf1-416">EBNF</span></span>                           | `ebnf`                                                                         |
| <span data-ttu-id="3ebf1-417">Elixir</span><span class="sxs-lookup"><span data-stu-id="3ebf1-417">Elixir</span></span>                         | `elixir`                                                                       |
| <span data-ttu-id="3ebf1-418">Elm</span><span class="sxs-lookup"><span data-stu-id="3ebf1-418">Elm</span></span>                            | `elm`                                                                          |
| <span data-ttu-id="3ebf1-419">Erlang</span><span class="sxs-lookup"><span data-stu-id="3ebf1-419">Erlang</span></span>                         | <span data-ttu-id="3ebf1-420">`erlang`, `erl`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-420">`erlang`, `erl`</span></span>                                                                |
| <span data-ttu-id="3ebf1-421">Excel</span><span class="sxs-lookup"><span data-stu-id="3ebf1-421">Excel</span></span>                          | <span data-ttu-id="3ebf1-422">`excel`, `xls`, `xlsx`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-422">`excel`, `xls`, `xlsx`</span></span>                                                         |
| <span data-ttu-id="3ebf1-423">Extempore</span><span class="sxs-lookup"><span data-stu-id="3ebf1-423">Extempore</span></span>                      | <span data-ttu-id="3ebf1-424">`extempore`, `xtlang`, `xtm`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-424">`extempore`, `xtlang`, `xtm`</span></span>                                                   |
| <span data-ttu-id="3ebf1-425">F#</span><span class="sxs-lookup"><span data-stu-id="3ebf1-425">F#</span></span>                             | <span data-ttu-id="3ebf1-426">`fsharp`, `fs`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-426">`fsharp`, `fs`</span></span>                                                                 |
| <span data-ttu-id="3ebf1-427">FIX</span><span class="sxs-lookup"><span data-stu-id="3ebf1-427">FIX</span></span>                            | `fix`                                                                          |
| <span data-ttu-id="3ebf1-428">Fortran</span><span class="sxs-lookup"><span data-stu-id="3ebf1-428">Fortran</span></span>                        | <span data-ttu-id="3ebf1-429">`fortran`, `f90`, `f95`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-429">`fortran`, `f90`, `f95`</span></span>                                                        |
| <span data-ttu-id="3ebf1-430">G-Code</span><span class="sxs-lookup"><span data-stu-id="3ebf1-430">G-Code</span></span>                         | <span data-ttu-id="3ebf1-431">`gcode`, `nc`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-431">`gcode`, `nc`</span></span>                                                                  |
| <span data-ttu-id="3ebf1-432">Gams</span><span class="sxs-lookup"><span data-stu-id="3ebf1-432">Gams</span></span>                           | <span data-ttu-id="3ebf1-433">`gams`, `gms`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-433">`gams`, `gms`</span></span>                                                                  |
| <span data-ttu-id="3ebf1-434">GAUSS</span><span class="sxs-lookup"><span data-stu-id="3ebf1-434">GAUSS</span></span>                          | <span data-ttu-id="3ebf1-435">`gauss`, `gss`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-435">`gauss`, `gss`</span></span>                                                                 |
| <span data-ttu-id="3ebf1-436">GDScript</span><span class="sxs-lookup"><span data-stu-id="3ebf1-436">GDScript</span></span>                       | <span data-ttu-id="3ebf1-437">`godot`, `gdscript`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-437">`godot`, `gdscript`</span></span>                                                            |
| <span data-ttu-id="3ebf1-438">Gherkin</span><span class="sxs-lookup"><span data-stu-id="3ebf1-438">Gherkin</span></span>                        | `gherkin`                                                                      |
| <span data-ttu-id="3ebf1-439">GN for Ninja</span><span class="sxs-lookup"><span data-stu-id="3ebf1-439">GN for Ninja</span></span>                   | <span data-ttu-id="3ebf1-440">`gn`, `gni`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-440">`gn`, `gni`</span></span>                                                                    |
| <span data-ttu-id="3ebf1-441">Go</span><span class="sxs-lookup"><span data-stu-id="3ebf1-441">Go</span></span>                             | <span data-ttu-id="3ebf1-442">`go`, `golang`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-442">`go`, `golang`</span></span>                                                                 |
| <span data-ttu-id="3ebf1-443">Golo</span><span class="sxs-lookup"><span data-stu-id="3ebf1-443">Golo</span></span>                           | <span data-ttu-id="3ebf1-444">`golo`, `gololang`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-444">`golo`, `gololang`</span></span>                                                             |
| <span data-ttu-id="3ebf1-445">Gradle</span><span class="sxs-lookup"><span data-stu-id="3ebf1-445">Gradle</span></span>                         | `gradle`                                                                       |
| <span data-ttu-id="3ebf1-446">Groovy</span><span class="sxs-lookup"><span data-stu-id="3ebf1-446">Groovy</span></span>                         | `groovy`                                                                       |
| <span data-ttu-id="3ebf1-447">HTML</span><span class="sxs-lookup"><span data-stu-id="3ebf1-447">HTML</span></span>                           | <span data-ttu-id="3ebf1-448">`html`, `xhtml`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-448">`html`, `xhtml`</span></span>                                                                |
| <span data-ttu-id="3ebf1-449">HTTP</span><span class="sxs-lookup"><span data-stu-id="3ebf1-449">HTTP</span></span>                           | <span data-ttu-id="3ebf1-450">`http`, `https`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-450">`http`, `https`</span></span>                                                                |
| <span data-ttu-id="3ebf1-451">Haml</span><span class="sxs-lookup"><span data-stu-id="3ebf1-451">Haml</span></span>                           | `haml`                                                                         |
| <span data-ttu-id="3ebf1-452">把手</span><span class="sxs-lookup"><span data-stu-id="3ebf1-452">Handlebars</span></span>                     | <span data-ttu-id="3ebf1-453">`handlebars`, `hbs`, `html.hbs`, `html.handlebars`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-453">`handlebars`, `hbs`, `html.hbs`, `html.handlebars`</span></span>                             |
| <span data-ttu-id="3ebf1-454">Haskell</span><span class="sxs-lookup"><span data-stu-id="3ebf1-454">Haskell</span></span>                        | <span data-ttu-id="3ebf1-455">`haskell`, `hs`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-455">`haskell`, `hs`</span></span>                                                                |
| <span data-ttu-id="3ebf1-456">Haxe</span><span class="sxs-lookup"><span data-stu-id="3ebf1-456">Haxe</span></span>                           | <span data-ttu-id="3ebf1-457">`haxe`, `hx`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-457">`haxe`, `hx`</span></span>                                                                   |
| <span data-ttu-id="3ebf1-458">Hy</span><span class="sxs-lookup"><span data-stu-id="3ebf1-458">Hy</span></span>                             | <span data-ttu-id="3ebf1-459">`hy`, `hylang`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-459">`hy`, `hylang`</span></span>                                                                 |
| <span data-ttu-id="3ebf1-460">Ini</span><span class="sxs-lookup"><span data-stu-id="3ebf1-460">Ini</span></span>                            | `ini`                                                                          |
| <span data-ttu-id="3ebf1-461">Inform7</span><span class="sxs-lookup"><span data-stu-id="3ebf1-461">Inform7</span></span>                        | <span data-ttu-id="3ebf1-462">`inform7`, `i7`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-462">`inform7`, `i7`</span></span>                                                                |
| <span data-ttu-id="3ebf1-463">IRPF90</span><span class="sxs-lookup"><span data-stu-id="3ebf1-463">IRPF90</span></span>                         | `irpf90`                                                                       |
| <span data-ttu-id="3ebf1-464">JSON</span><span class="sxs-lookup"><span data-stu-id="3ebf1-464">JSON</span></span>                           | `json`                                                                         |
| <span data-ttu-id="3ebf1-465">Java</span><span class="sxs-lookup"><span data-stu-id="3ebf1-465">Java</span></span>                           | <span data-ttu-id="3ebf1-466">`java`, `jsp`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-466">`java`, `jsp`</span></span>                                                                  |
| <span data-ttu-id="3ebf1-467">JavaScript</span><span class="sxs-lookup"><span data-stu-id="3ebf1-467">JavaScript</span></span>                     | <span data-ttu-id="3ebf1-468">`javascript`, `js`, `jsx`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-468">`javascript`, `js`, `jsx`</span></span>                                                      |
| <span data-ttu-id="3ebf1-469">Kotlin</span><span class="sxs-lookup"><span data-stu-id="3ebf1-469">Kotlin</span></span>                         | <span data-ttu-id="3ebf1-470">`kotlin`, `kt`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-470">`kotlin`, `kt`</span></span>                                                                 |
| <span data-ttu-id="3ebf1-471">Kusto</span><span class="sxs-lookup"><span data-stu-id="3ebf1-471">Kusto</span></span>                          | `kusto`                                                                        |
| <span data-ttu-id="3ebf1-472">Leaf</span><span class="sxs-lookup"><span data-stu-id="3ebf1-472">Leaf</span></span>                           | `leaf`                                                                         |
| <span data-ttu-id="3ebf1-473">Lasso</span><span class="sxs-lookup"><span data-stu-id="3ebf1-473">Lasso</span></span>                          | <span data-ttu-id="3ebf1-474">`lasso`, `ls`, `lassoscript`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-474">`lasso`, `ls`, `lassoscript`</span></span>                                                   |
| <span data-ttu-id="3ebf1-475">小於</span><span class="sxs-lookup"><span data-stu-id="3ebf1-475">Less</span></span>                           | `less`                                                                         |
| <span data-ttu-id="3ebf1-476">LDIF</span><span class="sxs-lookup"><span data-stu-id="3ebf1-476">LDIF</span></span>                           | `ldif`                                                                         |
| <span data-ttu-id="3ebf1-477">Lisp</span><span class="sxs-lookup"><span data-stu-id="3ebf1-477">Lisp</span></span>                           | `lisp`                                                                         |
| <span data-ttu-id="3ebf1-478">LiveCode Server</span><span class="sxs-lookup"><span data-stu-id="3ebf1-478">LiveCode Server</span></span>                | `livecodeserver`                                                               |
| <span data-ttu-id="3ebf1-479">LiveScript</span><span class="sxs-lookup"><span data-stu-id="3ebf1-479">LiveScript</span></span>                     | <span data-ttu-id="3ebf1-480">`livescript`, `ls`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-480">`livescript`, `ls`</span></span>                                                             |
| <span data-ttu-id="3ebf1-481">Lua</span><span class="sxs-lookup"><span data-stu-id="3ebf1-481">Lua</span></span>                            | `lua`                                                                          |
| <span data-ttu-id="3ebf1-482">Makefile</span><span class="sxs-lookup"><span data-stu-id="3ebf1-482">Makefile</span></span>                       | <span data-ttu-id="3ebf1-483">`makefile`, `mk`, `mak`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-483">`makefile`, `mk`, `mak`</span></span>                                                        |
| <span data-ttu-id="3ebf1-484">Markdown</span><span class="sxs-lookup"><span data-stu-id="3ebf1-484">Markdown</span></span>                       | <span data-ttu-id="3ebf1-485">`markdown`, `md`, `mkdown`, `mkd`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-485">`markdown`, `md`, `mkdown`, `mkd`</span></span>                                              |
| <span data-ttu-id="3ebf1-486">Mathematica</span><span class="sxs-lookup"><span data-stu-id="3ebf1-486">Mathematica</span></span>                    | <span data-ttu-id="3ebf1-487">`mathematica`, `mma`, `wl`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-487">`mathematica`, `mma`, `wl`</span></span>                                                     |
| <span data-ttu-id="3ebf1-488">Matlab</span><span class="sxs-lookup"><span data-stu-id="3ebf1-488">Matlab</span></span>                         | `matlab`                                                                       |
| <span data-ttu-id="3ebf1-489">Maxima</span><span class="sxs-lookup"><span data-stu-id="3ebf1-489">Maxima</span></span>                         | `maxima`                                                                       |
| <span data-ttu-id="3ebf1-490">Maya 內嵌語言</span><span class="sxs-lookup"><span data-stu-id="3ebf1-490">Maya Embedded Language</span></span>         | `mel`                                                                          |
| <span data-ttu-id="3ebf1-491">Mercury</span><span class="sxs-lookup"><span data-stu-id="3ebf1-491">Mercury</span></span>                        | `mercury`                                                                      |
| <span data-ttu-id="3ebf1-492">mIRC 指令碼語言</span><span class="sxs-lookup"><span data-stu-id="3ebf1-492">mIRC Scripting Language</span></span>        | <span data-ttu-id="3ebf1-493">`mirc`, `mrc`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-493">`mirc`, `mrc`</span></span>                                                                  |
| <span data-ttu-id="3ebf1-494">Mizar</span><span class="sxs-lookup"><span data-stu-id="3ebf1-494">Mizar</span></span>                          | `mizar`                                                                        |
| <span data-ttu-id="3ebf1-495">受控物件格式</span><span class="sxs-lookup"><span data-stu-id="3ebf1-495">Managed Object Format</span></span>          | `mof`                                                                          |
| <span data-ttu-id="3ebf1-496">Mojolicious</span><span class="sxs-lookup"><span data-stu-id="3ebf1-496">Mojolicious</span></span>                    | `mojolicious`                                                                  |
| <span data-ttu-id="3ebf1-497">Monkey</span><span class="sxs-lookup"><span data-stu-id="3ebf1-497">Monkey</span></span>                         | `monkey`                                                                       |
| <span data-ttu-id="3ebf1-498">Moonscript</span><span class="sxs-lookup"><span data-stu-id="3ebf1-498">Moonscript</span></span>                     | <span data-ttu-id="3ebf1-499">`moonscript`, `moon`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-499">`moonscript`, `moon`</span></span>                                                           |
| <span data-ttu-id="3ebf1-500">MS Graph (互動式)</span><span class="sxs-lookup"><span data-stu-id="3ebf1-500">MS Graph (Interactive)</span></span>         | `msgraph-interactive`                                                          |
| <span data-ttu-id="3ebf1-501">N1QL</span><span class="sxs-lookup"><span data-stu-id="3ebf1-501">N1QL</span></span>                           | `n1ql`                                                                         |
| <span data-ttu-id="3ebf1-502">NSIS</span><span class="sxs-lookup"><span data-stu-id="3ebf1-502">NSIS</span></span>                           | `nsis`                                                                         |
| <span data-ttu-id="3ebf1-503">Nginx</span><span class="sxs-lookup"><span data-stu-id="3ebf1-503">Nginx</span></span>                          | <span data-ttu-id="3ebf1-504">`nginx`, `nginxconf`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-504">`nginx`, `nginxconf`</span></span>                                                           |
| <span data-ttu-id="3ebf1-505">Nimrod</span><span class="sxs-lookup"><span data-stu-id="3ebf1-505">Nimrod</span></span>                         | <span data-ttu-id="3ebf1-506">`nimrod`, `nim`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-506">`nimrod`, `nim`</span></span>                                                                |
| <span data-ttu-id="3ebf1-507">Nix</span><span class="sxs-lookup"><span data-stu-id="3ebf1-507">Nix</span></span>                            | `nix`                                                                          |
| <span data-ttu-id="3ebf1-508">OCaml</span><span class="sxs-lookup"><span data-stu-id="3ebf1-508">OCaml</span></span>                          | <span data-ttu-id="3ebf1-509">`ocaml`, `ml`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-509">`ocaml`, `ml`</span></span>                                                                  |
| <span data-ttu-id="3ebf1-510">Objective C</span><span class="sxs-lookup"><span data-stu-id="3ebf1-510">Objective C</span></span>                    | <span data-ttu-id="3ebf1-511">`objectivec`, `mm`, `objc`, `obj-c`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-511">`objectivec`, `mm`, `objc`, `obj-c`</span></span>                                            |
| <span data-ttu-id="3ebf1-512">OpenGL Shading Language</span><span class="sxs-lookup"><span data-stu-id="3ebf1-512">OpenGL Shading Language</span></span>        | `glsl`                                                                         |
| <span data-ttu-id="3ebf1-513">OpenSCAD</span><span class="sxs-lookup"><span data-stu-id="3ebf1-513">OpenSCAD</span></span>                       | <span data-ttu-id="3ebf1-514">`openscad`, `scad`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-514">`openscad`, `scad`</span></span>                                                             |
| <span data-ttu-id="3ebf1-515">Oracle 規則語言</span><span class="sxs-lookup"><span data-stu-id="3ebf1-515">Oracle Rules Language</span></span>          | `ruleslanguage`                                                                |
| <span data-ttu-id="3ebf1-516">Oxygene</span><span class="sxs-lookup"><span data-stu-id="3ebf1-516">Oxygene</span></span>                        | `oxygene`                                                                      |
| <span data-ttu-id="3ebf1-517">PF</span><span class="sxs-lookup"><span data-stu-id="3ebf1-517">PF</span></span>                             | <span data-ttu-id="3ebf1-518">`pf`, `pf.conf`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-518">`pf`, `pf.conf`</span></span>                                                                |
| <span data-ttu-id="3ebf1-519">PHP</span><span class="sxs-lookup"><span data-stu-id="3ebf1-519">PHP</span></span>                            | <span data-ttu-id="3ebf1-520">`php`, `php3`, `php4`, `php5`, `php6`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-520">`php`, `php3`, `php4`, `php5`, `php6`</span></span>                                          |
| <span data-ttu-id="3ebf1-521">Parser3</span><span class="sxs-lookup"><span data-stu-id="3ebf1-521">Parser3</span></span>                        | `parser3`                                                                      |
| <span data-ttu-id="3ebf1-522">Perl</span><span class="sxs-lookup"><span data-stu-id="3ebf1-522">Perl</span></span>                           | <span data-ttu-id="3ebf1-523">`perl`, `pl`, `pm`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-523">`perl`, `pl`, `pm`</span></span>                                                             |
| <span data-ttu-id="3ebf1-524">純文字無反白</span><span class="sxs-lookup"><span data-stu-id="3ebf1-524">Plaintext no highlight</span></span>         | `plaintext`                                                                    |
| <span data-ttu-id="3ebf1-525">Pony</span><span class="sxs-lookup"><span data-stu-id="3ebf1-525">Pony</span></span>                           | `pony`                                                                         |
| <span data-ttu-id="3ebf1-526">PostgreSQL & PL/pgSQL</span><span class="sxs-lookup"><span data-stu-id="3ebf1-526">PostgreSQL & PL/pgSQL</span></span>          | <span data-ttu-id="3ebf1-527">`pgsql`, `postgres`, `postgresql`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-527">`pgsql`, `postgres`, `postgresql`</span></span>                                              |
| <span data-ttu-id="3ebf1-528">PowerShell</span><span class="sxs-lookup"><span data-stu-id="3ebf1-528">PowerShell</span></span>                     | <span data-ttu-id="3ebf1-529">`powershell`, `ps`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-529">`powershell`, `ps`</span></span>                                                             |
| <span data-ttu-id="3ebf1-530">PowerShell (互動式)</span><span class="sxs-lookup"><span data-stu-id="3ebf1-530">PowerShell (Interactive)</span></span>       | `powershell-interactive`                                                       |
| <span data-ttu-id="3ebf1-531">Processing</span><span class="sxs-lookup"><span data-stu-id="3ebf1-531">Processing</span></span>                     | `processing`                                                                   |
| <span data-ttu-id="3ebf1-532">Prolog</span><span class="sxs-lookup"><span data-stu-id="3ebf1-532">Prolog</span></span>                         | `prolog`                                                                       |
| <span data-ttu-id="3ebf1-533">屬性</span><span class="sxs-lookup"><span data-stu-id="3ebf1-533">Properties</span></span>                     | `properties`                                                                   |
| <span data-ttu-id="3ebf1-534">通訊協定緩衝區</span><span class="sxs-lookup"><span data-stu-id="3ebf1-534">Protocol Buffers</span></span>               | `protobuf`                                                                     |
| <span data-ttu-id="3ebf1-535">Puppet</span><span class="sxs-lookup"><span data-stu-id="3ebf1-535">Puppet</span></span>                         | <span data-ttu-id="3ebf1-536">`puppet`, `pp`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-536">`puppet`, `pp`</span></span>                                                                 |
| <span data-ttu-id="3ebf1-537">Python</span><span class="sxs-lookup"><span data-stu-id="3ebf1-537">Python</span></span>                         | <span data-ttu-id="3ebf1-538">`python`, `py`, `gyp`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-538">`python`, `py`, `gyp`</span></span>                                                          |
| <span data-ttu-id="3ebf1-539">Python 分析工具結果</span><span class="sxs-lookup"><span data-stu-id="3ebf1-539">Python profiler results</span></span>        | `profile`                                                                      |
| <span data-ttu-id="3ebf1-540">Q#</span><span class="sxs-lookup"><span data-stu-id="3ebf1-540">Q#</span></span>                             | `qsharp`                                                                       |
| <span data-ttu-id="3ebf1-541">Q</span><span class="sxs-lookup"><span data-stu-id="3ebf1-541">Q</span></span>                              | <span data-ttu-id="3ebf1-542">`k`, `kdb`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-542">`k`, `kdb`</span></span>                                                                     |
| <span data-ttu-id="3ebf1-543">QML</span><span class="sxs-lookup"><span data-stu-id="3ebf1-543">QML</span></span>                            | `qml`                                                                          |
| <span data-ttu-id="3ebf1-544">R</span><span class="sxs-lookup"><span data-stu-id="3ebf1-544">R</span></span>                              | `r`                                                                            |
| <span data-ttu-id="3ebf1-545">Razor CSHTML</span><span class="sxs-lookup"><span data-stu-id="3ebf1-545">Razor CSHTML</span></span>                   | <span data-ttu-id="3ebf1-546">`cshtml`, `razor`, `razor-cshtml`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-546">`cshtml`, `razor`, `razor-cshtml`</span></span>                                              |
| <span data-ttu-id="3ebf1-547">ReasonML</span><span class="sxs-lookup"><span data-stu-id="3ebf1-547">ReasonML</span></span>                       | <span data-ttu-id="3ebf1-548">`reasonml`, `re`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-548">`reasonml`, `re`</span></span>                                                               |
| <span data-ttu-id="3ebf1-549">RenderMan RIB</span><span class="sxs-lookup"><span data-stu-id="3ebf1-549">RenderMan RIB</span></span>                  | `rib`                                                                          |
| <span data-ttu-id="3ebf1-550">RenderMan RSL</span><span class="sxs-lookup"><span data-stu-id="3ebf1-550">RenderMan RSL</span></span>                  | `rsl`                                                                          |
| <span data-ttu-id="3ebf1-551">Roboconf</span><span class="sxs-lookup"><span data-stu-id="3ebf1-551">Roboconf</span></span>                       | <span data-ttu-id="3ebf1-552">`graph`, `instances`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-552">`graph`, `instances`</span></span>                                                           |
| <span data-ttu-id="3ebf1-553">Robot Framework</span><span class="sxs-lookup"><span data-stu-id="3ebf1-553">Robot Framework</span></span>                | <span data-ttu-id="3ebf1-554">`robot`, `rf`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-554">`robot`, `rf`</span></span>                                                                  |
| <span data-ttu-id="3ebf1-555">RPM 規格檔案</span><span class="sxs-lookup"><span data-stu-id="3ebf1-555">RPM spec files</span></span>                 | <span data-ttu-id="3ebf1-556">`rpm-specfile`, `rpm`, `spec`, `rpm-spec`, `specfile`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-556">`rpm-specfile`, `rpm`, `spec`, `rpm-spec`, `specfile`</span></span>                          |
| <span data-ttu-id="3ebf1-557">Ruby</span><span class="sxs-lookup"><span data-stu-id="3ebf1-557">Ruby</span></span>                           | <span data-ttu-id="3ebf1-558">`ruby`, `rb`, `gemspec`, `podspec`, `thor`, `irb`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-558">`ruby`, `rb`, `gemspec`, `podspec`, `thor`, `irb`</span></span>                              |
| <span data-ttu-id="3ebf1-559">Rust</span><span class="sxs-lookup"><span data-stu-id="3ebf1-559">Rust</span></span>                           | <span data-ttu-id="3ebf1-560">`rust`, `rs`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-560">`rust`, `rs`</span></span>                                                                   |
| <span data-ttu-id="3ebf1-561">SAS</span><span class="sxs-lookup"><span data-stu-id="3ebf1-561">SAS</span></span>                            | <span data-ttu-id="3ebf1-562">`SAS`, `sas`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-562">`SAS`, `sas`</span></span>                                                                   |
| <span data-ttu-id="3ebf1-563">SCSS</span><span class="sxs-lookup"><span data-stu-id="3ebf1-563">SCSS</span></span>                           | `scss`                                                                         |
| <span data-ttu-id="3ebf1-564">SQL</span><span class="sxs-lookup"><span data-stu-id="3ebf1-564">SQL</span></span>                            | `sql`                                                                          |
| <span data-ttu-id="3ebf1-565">STEP Part 21</span><span class="sxs-lookup"><span data-stu-id="3ebf1-565">STEP Part 21</span></span>                   | <span data-ttu-id="3ebf1-566">`p21`, `step`, `stp`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-566">`p21`, `step`, `stp`</span></span>                                                           |
| <span data-ttu-id="3ebf1-567">Scala</span><span class="sxs-lookup"><span data-stu-id="3ebf1-567">Scala</span></span>                          | `scala`                                                                        |
| <span data-ttu-id="3ebf1-568">配置</span><span class="sxs-lookup"><span data-stu-id="3ebf1-568">Scheme</span></span>                         | `scheme`                                                                       |
| <span data-ttu-id="3ebf1-569">Scilab</span><span class="sxs-lookup"><span data-stu-id="3ebf1-569">Scilab</span></span>                         | <span data-ttu-id="3ebf1-570">`scilab`, `sci`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-570">`scilab`, `sci`</span></span>                                                                |
| <span data-ttu-id="3ebf1-571">Shape Expressions</span><span class="sxs-lookup"><span data-stu-id="3ebf1-571">Shape Expressions</span></span>              | `shexc`                                                                        |
| <span data-ttu-id="3ebf1-572">殼層</span><span class="sxs-lookup"><span data-stu-id="3ebf1-572">Shell</span></span>                          | <span data-ttu-id="3ebf1-573">`shell`, `console`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-573">`shell`, `console`</span></span>                                                             |
| <span data-ttu-id="3ebf1-574">Smali</span><span class="sxs-lookup"><span data-stu-id="3ebf1-574">Smali</span></span>                          | `smali`                                                                        |
| <span data-ttu-id="3ebf1-575">Smalltalk</span><span class="sxs-lookup"><span data-stu-id="3ebf1-575">Smalltalk</span></span>                      | <span data-ttu-id="3ebf1-576">`smalltalk`, `st`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-576">`smalltalk`, `st`</span></span>                                                              |
| <span data-ttu-id="3ebf1-577">Solidity</span><span class="sxs-lookup"><span data-stu-id="3ebf1-577">Solidity</span></span>                       | <span data-ttu-id="3ebf1-578">`solidity`, `sol`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-578">`solidity`, `sol`</span></span>                                                              |
| <span data-ttu-id="3ebf1-579">Stan</span><span class="sxs-lookup"><span data-stu-id="3ebf1-579">Stan</span></span>                           | `stan`                                                                         |
| <span data-ttu-id="3ebf1-580">Stata</span><span class="sxs-lookup"><span data-stu-id="3ebf1-580">Stata</span></span>                          | `stata`                                                                        |
| <span data-ttu-id="3ebf1-581">結構化文字</span><span class="sxs-lookup"><span data-stu-id="3ebf1-581">Structured Text</span></span>                | <span data-ttu-id="3ebf1-582">`iecst`, `scl`, `stl`, `structured-text`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-582">`iecst`, `scl`, `stl`, `structured-text`</span></span>                                       |
| <span data-ttu-id="3ebf1-583">手寫筆</span><span class="sxs-lookup"><span data-stu-id="3ebf1-583">Stylus</span></span>                         | <span data-ttu-id="3ebf1-584">`stylus`, `styl`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-584">`stylus`, `styl`</span></span>                                                               |
| <span data-ttu-id="3ebf1-585">SubUnit</span><span class="sxs-lookup"><span data-stu-id="3ebf1-585">SubUnit</span></span>                        | `subunit`                                                                      |
| <span data-ttu-id="3ebf1-586">Supercollider</span><span class="sxs-lookup"><span data-stu-id="3ebf1-586">Supercollider</span></span>                  | <span data-ttu-id="3ebf1-587">`supercollider`, `sc`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-587">`supercollider`, `sc`</span></span>                                                          |
| <span data-ttu-id="3ebf1-588">Swift</span><span class="sxs-lookup"><span data-stu-id="3ebf1-588">Swift</span></span>                          | `swift`                                                                        |
| <span data-ttu-id="3ebf1-589">Tcl</span><span class="sxs-lookup"><span data-stu-id="3ebf1-589">Tcl</span></span>                            | <span data-ttu-id="3ebf1-590">`tcl`, `tk`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-590">`tcl`, `tk`</span></span>                                                                    |
| <span data-ttu-id="3ebf1-591">Terraform (HCL)</span><span class="sxs-lookup"><span data-stu-id="3ebf1-591">Terraform (HCL)</span></span>                | <span data-ttu-id="3ebf1-592">`terraform`, `tf`, `hcl`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-592">`terraform`, `tf`, `hcl`</span></span>                                                       |
| <span data-ttu-id="3ebf1-593">測試任何通訊協定</span><span class="sxs-lookup"><span data-stu-id="3ebf1-593">Test Anything Protocol</span></span>         | `tap`                                                                          |
| <span data-ttu-id="3ebf1-594">TeX</span><span class="sxs-lookup"><span data-stu-id="3ebf1-594">TeX</span></span>                            | `tex`                                                                          |
| <span data-ttu-id="3ebf1-595">Thrift</span><span class="sxs-lookup"><span data-stu-id="3ebf1-595">Thrift</span></span>                         | `thrift`                                                                       |
| <span data-ttu-id="3ebf1-596">TOML</span><span class="sxs-lookup"><span data-stu-id="3ebf1-596">TOML</span></span>                           | `toml`                                                                         |
| <span data-ttu-id="3ebf1-597">TP</span><span class="sxs-lookup"><span data-stu-id="3ebf1-597">TP</span></span>                             | `tp`                                                                           |
| <span data-ttu-id="3ebf1-598">Twig</span><span class="sxs-lookup"><span data-stu-id="3ebf1-598">Twig</span></span>                           | <span data-ttu-id="3ebf1-599">`twig`, `craftcms`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-599">`twig`, `craftcms`</span></span>                                                             |
| <span data-ttu-id="3ebf1-600">TypeScript</span><span class="sxs-lookup"><span data-stu-id="3ebf1-600">TypeScript</span></span>                     | <span data-ttu-id="3ebf1-601">`typescript`, `ts`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-601">`typescript`, `ts`</span></span>                                                             |
| <span data-ttu-id="3ebf1-602">VB.NET</span><span class="sxs-lookup"><span data-stu-id="3ebf1-602">VB.NET</span></span>                         | <span data-ttu-id="3ebf1-603">`vbnet`, `vb`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-603">`vbnet`, `vb`</span></span>                                                                  |
| <span data-ttu-id="3ebf1-604">VBScript</span><span class="sxs-lookup"><span data-stu-id="3ebf1-604">VBScript</span></span>                       | <span data-ttu-id="3ebf1-605">`vbscript`, `vbs`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-605">`vbscript`, `vbs`</span></span>                                                              |
| <span data-ttu-id="3ebf1-606">VHDL</span><span class="sxs-lookup"><span data-stu-id="3ebf1-606">VHDL</span></span>                           | `vhdl`                                                                         |
| <span data-ttu-id="3ebf1-607">Vala</span><span class="sxs-lookup"><span data-stu-id="3ebf1-607">Vala</span></span>                           | `vala`                                                                         |
| <span data-ttu-id="3ebf1-608">Verilog</span><span class="sxs-lookup"><span data-stu-id="3ebf1-608">Verilog</span></span>                        | <span data-ttu-id="3ebf1-609">`verilog`, `v`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-609">`verilog`, `v`</span></span>                                                                 |
| <span data-ttu-id="3ebf1-610">Vim Script</span><span class="sxs-lookup"><span data-stu-id="3ebf1-610">Vim Script</span></span>                     | `vim`                                                                          |
| <span data-ttu-id="3ebf1-611">X++</span><span class="sxs-lookup"><span data-stu-id="3ebf1-611">X++</span></span>                            | `xpp`                                                                          |
| <span data-ttu-id="3ebf1-612">x86 Assembly</span><span class="sxs-lookup"><span data-stu-id="3ebf1-612">x86 Assembly</span></span>                   | `x86asm`                                                                       |
| <span data-ttu-id="3ebf1-613">XL</span><span class="sxs-lookup"><span data-stu-id="3ebf1-613">XL</span></span>                             | <span data-ttu-id="3ebf1-614">`xl`, `tao`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-614">`xl`, `tao`</span></span>                                                                    |
| <span data-ttu-id="3ebf1-615">XQuery</span><span class="sxs-lookup"><span data-stu-id="3ebf1-615">XQuery</span></span>                         | <span data-ttu-id="3ebf1-616">`xquery`, `xpath`, `xq`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-616">`xquery`, `xpath`, `xq`</span></span>                                                        |
| <span data-ttu-id="3ebf1-617">XAML</span><span class="sxs-lookup"><span data-stu-id="3ebf1-617">XAML</span></span>                           | `xaml`                                                                         |
| <span data-ttu-id="3ebf1-618">XML</span><span class="sxs-lookup"><span data-stu-id="3ebf1-618">XML</span></span>                            | <span data-ttu-id="3ebf1-619">`xml`, `xhtml`, `rss`, `atom`, `xjb`, `xsd`, `xsl`, `plist`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-619">`xml`, `xhtml`, `rss`, `atom`, `xjb`, `xsd`, `xsl`, `plist`</span></span>                    |
| <span data-ttu-id="3ebf1-620">YAML</span><span class="sxs-lookup"><span data-stu-id="3ebf1-620">YAML</span></span>                           | <span data-ttu-id="3ebf1-621">`yml`, `yaml`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-621">`yml`, `yaml`</span></span>                                                                  |
| <span data-ttu-id="3ebf1-622">Zephir</span><span class="sxs-lookup"><span data-stu-id="3ebf1-622">Zephir</span></span>                         | <span data-ttu-id="3ebf1-623">`zephir`, `zep`</span><span class="sxs-lookup"><span data-stu-id="3ebf1-623">`zephir`, `zep`</span></span>                                                                |

> [!TIP]
> <span data-ttu-id="3ebf1-624">Docs 編寫套件[開發語言完成功能](docs-authoring/dev-lang-completion.md)在有多個別名可用時，會使用第一個有效的別名。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-624">The Docs Authoring Pack, [Dev Lang Completion feature](docs-authoring/dev-lang-completion.md) uses the first valid alias when multiple aliases are available.</span></span>

## <a name="next-steps"></a><span data-ttu-id="3ebf1-625">後續步驟</span><span class="sxs-lookup"><span data-stu-id="3ebf1-625">Next steps</span></span>

<span data-ttu-id="3ebf1-626">如需程式碼以外內容類型的文字格式設定資訊，請參閱[文字格式設定指導方針](text-formatting-guidelines.md)。</span><span class="sxs-lookup"><span data-stu-id="3ebf1-626">For information on text formatting for content types other than code, see [Text formatting guidelines](text-formatting-guidelines.md).</span></span>
