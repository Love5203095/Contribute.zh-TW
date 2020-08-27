---
title: 參與 .NET 文件存放庫
description: 本文會描述在存放庫中參與文章和程式碼的流程範例，其組成 .NET 文件。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 05/14/2020
ms.openlocfilehash: 810a1335bf3c93b79952c701c44470d3e72fb124
ms.sourcegitcommit: 940c84d6bc23a8fbec780244563af188d2620ed1
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "88668635"
---
# <a name="learn-how-to-contribute-to-the-net-docs-repositories"></a><span data-ttu-id="7d9e4-103">了解如何參與 .NET 文件存放庫</span><span class="sxs-lookup"><span data-stu-id="7d9e4-103">Learn how to contribute to the .NET docs repositories</span></span>

<span data-ttu-id="7d9e4-104">感謝您對於參與 .NET 文件感到興趣！</span><span class="sxs-lookup"><span data-stu-id="7d9e4-104">Thank you for your interest in contributing to the .NET documentation!</span></span>

<span data-ttu-id="7d9e4-105">本文件涵蓋參與 [.NET 文件網站](https://docs.microsoft.com/dotnet)上所裝載文章和程式碼範例的程序。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-105">This document covers the process for contributing to the articles and code samples that are hosted on the [.NET documentation site](https://docs.microsoft.com/dotnet).</span></span> <span data-ttu-id="7d9e4-106">這些參與可以是簡單的錯字校正，也可以是複雜的新文章。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-106">Contributions may be as simple as typo corrections or as complex as new articles.</span></span>

<span data-ttu-id="7d9e4-107">.NET 文件網站是從多個存放庫建置而來：</span><span class="sxs-lookup"><span data-stu-id="7d9e4-107">The .NET documentation site is built from multiple repositories:</span></span>

- [<span data-ttu-id="7d9e4-108">.NET 概念文章和程式碼片段</span><span class="sxs-lookup"><span data-stu-id="7d9e4-108">.NET conceptual articles and code snippets</span></span>](https://github.com/dotnet/docs)
- [<span data-ttu-id="7d9e4-109">程式碼範例和程式碼片段</span><span class="sxs-lookup"><span data-stu-id="7d9e4-109">Code samples and snippets</span></span>](https://github.com/dotnet/samples)
- [<span data-ttu-id="7d9e4-110">.NET Standard、.NET Core、.NET Framework API 參考</span><span class="sxs-lookup"><span data-stu-id="7d9e4-110">.NET Standard, .NET Core, .NET Framework API reference</span></span>](https://github.com/dotnet/dotnet-api-docs)
- [<span data-ttu-id="7d9e4-111">.NET Compiler Platform SDK 參考</span><span class="sxs-lookup"><span data-stu-id="7d9e4-111">.NET Compiler Platform SDK reference</span></span>](https://github.com/dotnet/roslyn-api-docs)
- [<span data-ttu-id="7d9e4-112">ML.NET API 參考</span><span class="sxs-lookup"><span data-stu-id="7d9e4-112">ML.NET API reference</span></span>](https://github.com/dotnet/ml-api-docs)

<span data-ttu-id="7d9e4-113">這些存放庫的問題都已在 [dotnet/docs](https://github.com/dotnet/docs/issues) 存放庫中進行追蹤。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-113">Issues for all these repositories are tracked in the [dotnet/docs](https://github.com/dotnet/docs/issues) repository.</span></span>

## <a name="guidelines-for-contributions"></a><span data-ttu-id="7d9e4-114">參與方針</span><span class="sxs-lookup"><span data-stu-id="7d9e4-114">Guidelines for contributions</span></span>

<span data-ttu-id="7d9e4-115">感謝社群對文件的參與。下列清單顯示參與 .NET 文件時應注意的一些指導規則：</span><span class="sxs-lookup"><span data-stu-id="7d9e4-115">We appreciate community contributions to docs. The following list shows some guiding rules to keep in mind when you're contributing to the .NET documentation:</span></span>

- <span data-ttu-id="7d9e4-116">**請勿**出其不意地提交大量提取要求。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-116">**DON'T** surprise us with large pull requests.</span></span> <span data-ttu-id="7d9e4-117">相反地，請提出一個問題並開始討論，先讓我們就大方向取得共識再投入大量時間。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-117">Instead, file an issue and start a discussion so we can agree on a direction before you invest a large amount of time.</span></span>
- <span data-ttu-id="7d9e4-118">**務必**遵循這些指示，以及[語態和語調](dotnet-voice-tone.md)方針。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-118">**DO** follow these instructions and [voice and tone](dotnet-voice-tone.md) guidelines.</span></span>
- <span data-ttu-id="7d9e4-119">**務必**使用[範本](dotnet-style-guide.md)檔案作為您工作的起點。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-119">**DO** use the [template](dotnet-style-guide.md) file as the starting point of your work.</span></span>
- <span data-ttu-id="7d9e4-120">**務必**先在您的分支上建立個別分支，再參與文章。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-120">**DO** create a separate branch on your fork before working on the articles.</span></span>
- <span data-ttu-id="7d9e4-121">**務必**遵循 [GitHub flow](https://guides.github.com/introduction/flow/)(GitHub 流程)。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-121">**DO** follow the [GitHub flow](https://guides.github.com/introduction/flow/).</span></span>
- <span data-ttu-id="7d9e4-122">若想要的話，請**務必**針對參與來撰寫部落格文章和推文 (或透過其他方式)！</span><span class="sxs-lookup"><span data-stu-id="7d9e4-122">**DO** blog and tweet (or whatever) about your contributions if you like!</span></span>

<span data-ttu-id="7d9e4-123">遵循這些方針將有助於確保您與我們都有更佳的體驗。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-123">Following these guidelines will ensure a better experience for you and for us.</span></span>

## <a name="make-a-contribution-to-net-docs"></a><span data-ttu-id="7d9e4-124">參與 .NET 文件</span><span class="sxs-lookup"><span data-stu-id="7d9e4-124">Make a contribution to .NET docs</span></span>

<span data-ttu-id="7d9e4-125">**步驟 1：** 如果您對撰寫新內容或全面回顧現有內容感興趣，請開啟描述您要執行之作業的[問題](https://github.com/dotnet/docs/issues)。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-125">**Step 1:** If you're interested in writing new content or in thoroughly revising existing content, open an [issue](https://github.com/dotnet/docs/issues) describing what you want to do.</span></span> <span data-ttu-id="7d9e4-126">**文件**資料夾的內容會組織成章節並反映在目錄 (TOC) 中。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-126">The content inside the **docs** folder is organized into sections that are reflected in the Table of Contents (TOC).</span></span> <span data-ttu-id="7d9e4-127">請定義主題在 TOC 中的位置。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-127">Define where the topic will be located in the TOC.</span></span> <span data-ttu-id="7d9e4-128">然後取得此提案的意見反應。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-128">Get feedback on your proposal.</span></span>

<span data-ttu-id="7d9e4-129">-或-</span><span class="sxs-lookup"><span data-stu-id="7d9e4-129">-or-</span></span>

<span data-ttu-id="7d9e4-130">選擇現有問題並加以解決。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-130">Choose an existing issue and address it.</span></span> <span data-ttu-id="7d9e4-131">您可查看 [open issues](https://github.com/dotnet/docs/issues) (開啟的問題) 清單，並自願參與任何感興趣的問題：</span><span class="sxs-lookup"><span data-stu-id="7d9e4-131">You can look at our [open issues](https://github.com/dotnet/docs/issues) list and volunteer to work on the ones you're interested in:</span></span>

- <span data-ttu-id="7d9e4-132">依照 [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) 標籤進行篩選，以取得良好或優先處理的問題。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-132">Filter by the [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) label for, well, good first issues.</span></span>
- <span data-ttu-id="7d9e4-133">依照 [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) 標籤進行篩選，以取得適合由社群進行貢獻的問題。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-133">Filter by the [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) label for issues appropriate for community contribution.</span></span> <span data-ttu-id="7d9e4-134">這些問題通常僅需要最少的內容。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-134">These issues usually require minimal context.</span></span>
- <span data-ttu-id="7d9e4-135">具備經驗的參與者可處理任何其感興趣的問題。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-135">Experienced contributors can tackle any issues of interest.</span></span>

<span data-ttu-id="7d9e4-136">當找到要處理的問題時，請新增註解來詢問該問題是否處於開啟狀態。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-136">When you find an issue to work on, add a comment to ask if it's open.</span></span>

<span data-ttu-id="7d9e4-137">一旦選擇了要參與的工作，請遵循[入門](../get-started-setup-github.md)指南以建立 GitHub 帳戶並設定環境。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-137">Once you've picked a task to work on, follow the [get started](../get-started-setup-github.md) guide to create a GitHub account and set up your environment.</span></span>

<span data-ttu-id="7d9e4-138">**步驟 2：** 視需要派生 `/dotnet/docs`、`dotnet/samples`、`dotnet/dotnet-api-docs`、`dotnet/roslyn-api-docs` 或 `dotnet/ml-api-docs` 存放庫，並為您的變更建立分支。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-138">**Step 2:** Fork the `/dotnet/docs`, `dotnet/samples`, `dotnet/dotnet-api-docs`, `dotnet/roslyn-api-docs`, or `dotnet/ml-api-docs` repos as needed and create a branch for your changes.</span></span>

<span data-ttu-id="7d9e4-139">若變更不大，請參閱參與者指南[首頁](../index.md#quick-edits-to-existing-documents)上有關在 GitHub 中編輯的指示。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-139">For small changes, see the instructions on editing in GitHub on the [home page](../index.md#quick-edits-to-existing-documents) of the contributor guide.</span></span>

<span data-ttu-id="7d9e4-140">**步驟 3：** 在此新分支上進行變更。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-140">**Step 3:** Make the changes on this new branch.</span></span>

<span data-ttu-id="7d9e4-141">如果這是新主題，您可以使用此[範本檔案](dotnet-style-guide.md)作為起點。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-141">If it's a new topic, you can use this [template file](dotnet-style-guide.md) as your starting point.</span></span> <span data-ttu-id="7d9e4-142">其中包含撰寫方針，並同時說明每篇文章所需的中繼資料，例如作者資訊。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-142">It contains the writing guidelines and also explains the metadata required for each article, such as author information.</span></span> <span data-ttu-id="7d9e4-143">如需 docs.microsoft.com 網站中所使用 Markdown 語法的詳細資訊，請參閱 [Markdown 參考](../markdown-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-143">For more information on the Markdown syntax used in the docs.microsoft.com site, see [Markdown reference](../markdown-reference.md).</span></span>

<span data-ttu-id="7d9e4-144">請巡覽至步驟 1 中針對您文章所決定 TOC 位置的相對應資料夾。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-144">Navigate to the folder that corresponds to the TOC location determined for your article in step 1.</span></span> <span data-ttu-id="7d9e4-145">該資料夾包含該區段中所有文章的 Markdown 檔案。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-145">That folder contains the Markdown files for all articles in that section.</span></span> <span data-ttu-id="7d9e4-146">如有需要，請建立新的資料夾來放置您的內容檔案。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-146">If necessary, create a new folder to place the files for your content.</span></span> <span data-ttu-id="7d9e4-147">該區段的主要文章名為 *index.md*。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-147">The main article for that section is called *index.md*.</span></span>

<span data-ttu-id="7d9e4-148">針對影像和其他靜態資源，請在包含您文章的資料夾中建立名為 **media** 的子資料夾 (如果尚未存在)。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-148">For images and other static resources, create a subfolder called **media** inside the folder that contains your article, if it doesn't already exist.</span></span> <span data-ttu-id="7d9e4-149">在 **media** 資料夾中，建立具有文章名稱的子資料夾 (索引檔除外)。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-149">Inside the **media** folder, create a subfolder with the article name (except for the index file).</span></span>

<span data-ttu-id="7d9e4-150">針對**程式碼片段**，請在包含您文章的資料夾中建立名為 **snippets** 的子資料夾 (如果尚未存在)。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-150">For **code snippets**, create a subfolder called **snippets** inside the folder that contains your article, if it doesn't already exist.</span></span> <span data-ttu-id="7d9e4-151">在 [snippets] 資料夾內，使用文章名稱建立子資料夾。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-151">Inside the **snippets** folder, create a subfolder with the article name.</span></span> <span data-ttu-id="7d9e4-152">在大部分情況下，您會有三種主要 .NET 語言的程式碼片段：C#、F# 與 Visual Basic。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-152">In most cases, you'll have code snippets for all three of the main .NET languages, C#, F#, and Visual Basic.</span></span> <span data-ttu-id="7d9e4-153">在該情況下，請分別建立名為 **chsarp**、**fsharp** 和 **vb** 的子資料夾，其分別適用於三種專案。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-153">In that case, create subfolders named **csharp**, **fsharp**, and **vb** for each of the three projects.</span></span> <span data-ttu-id="7d9e4-154">若正在為位於 [docs/csharp](https://github.com/dotnet/docs/tree/master/docs/csharp)、[docs/fsharp](https://github.com/dotnet/docs/tree/master/docs/fsharp) 或 [docs/visual-basic](https://github.com/dotnet/docs/tree/master/docs/visual-basic) 資料夾下的文章建立程式碼片段，由於程式碼片段只會以一種語言呈現，因此可忽略語言子資料夾。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-154">If you're creating a snippet for an article under the [docs/csharp](https://github.com/dotnet/docs/tree/master/docs/csharp), [docs/fsharp](https://github.com/dotnet/docs/tree/master/docs/fsharp), or [docs/visual-basic](https://github.com/dotnet/docs/tree/master/docs/visual-basic) folders, the snippet will only be in one language so you can omit the language subfolder.</span></span>

<span data-ttu-id="7d9e4-155">程式碼片段為一種小篇幅、重點式的程式碼範例，用以示範文章中提及的概念。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-155">Code snippets are small, focused examples of code that demonstrate the concepts covered in an article.</span></span> <span data-ttu-id="7d9e4-156">大型程式 (供使用者下載與探索) 應該放在 [dotnet/samples](https://github.com/dotnet/samples) 存放庫中。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-156">Larger programs intended for download and exploration should be located in the [dotnet/samples](https://github.com/dotnet/samples) repository.</span></span> <span data-ttu-id="7d9e4-157">完整範例涵蓋在[參與範例](#contribute-to-samples)一節中。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-157">Full samples are covered in the section on [Contributing to samples](#contribute-to-samples).</span></span>

## <a name="example-folder-structure"></a><span data-ttu-id="7d9e4-158">範例資料夾結構</span><span class="sxs-lookup"><span data-stu-id="7d9e4-158">Example folder structure</span></span>

```
docs
  /about
  /core
    /porting
      porting-overview.md
      /media
        /porting-overview
          portability_report.png
      /snippets
        /porting-overview
          /csharp
            porting.csproj
            porting-overview.cs
            Program.cs
          /fsharp
            porting.fsproj
            porting-overview.fs
            Program.fs
          /vb
            porting.vbproj
            porting-overview.vb
            Program.vb
```

> [!NOTE]
> <span data-ttu-id="7d9e4-159">假設只有一個語言，語言指南區域中的程式碼片段底下不需要語言資料夾。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-159">The language folders under snippets are not needed in the language guide area, where only one language is assumed.</span></span>

<span data-ttu-id="7d9e4-160">如上所示的結構包含一個影像 *portability_report.png*，以及三個程式碼專案，專案中含有 *porting-overview.md* 文章中的**程式碼片段**。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-160">The structure shown above includes one image, *portability_report.png*, and three code projects that include **code snippets** that are included in the *porting-overview.md* article.</span></span> <span data-ttu-id="7d9e4-161">可接受的替代結構是為每種語言各建立一個專案，並將所有文章的所有程式碼片段放在該資料夾中。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-161">An accepted alternative structure contains one project per language that contains all snippets for all articles in that folder.</span></span> <span data-ttu-id="7d9e4-162">因為僅使用篇幅非常小的程式碼片段示範語言語法，所以語言參考區域中才會使用此替代結構。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-162">This alternative has been used in the language reference areas because of very small snippets to demonstrate language syntax.</span></span> <span data-ttu-id="7d9e4-163">但不建議在其他區域中使用。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-163">It is discouraged in other areas.</span></span>

<span data-ttu-id="7d9e4-164">為了留下歷程記錄，許多包含的程式碼片段會儲存在 *dotnet/docs* 存放庫中的 */samples* 資料夾底下。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-164">For historical reasons, many of the included snippets are stored under the */samples* folder in the *dotnet/docs* repository.</span></span> <span data-ttu-id="7d9e4-165">如果要大幅變更文章內容，則這些程式碼片段應移至新的結構。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-165">If you're making major changes to an article, those snippets should be moved to the new structure.</span></span> <span data-ttu-id="7d9e4-166">如果只是要微調，請勿移動程式碼片段。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-166">Do not move snippets for small changes.</span></span>

<span data-ttu-id="7d9e4-167">**步驟 4：** 從您的分支提交提取要求 (PR) 至主分支。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-167">**Step 4:** Submit a Pull Request (PR) from your branch to the master branch.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7d9e4-168">目前無法在任何 .NET 文件存放庫上使用[註解自動化](../how-to-write-workflows-major.md#review-and-sign-off)功能。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-168">The [comment automation](../how-to-write-workflows-major.md#review-and-sign-off) functionality is not available on any of the .NET docs repositories at this time.</span></span> <span data-ttu-id="7d9e4-169">.NET 文件小組成員將會審查並合併您的 PR。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-169">Members of the .NET docs team will review and merge your PR.</span></span>

<span data-ttu-id="7d9e4-170">每個 PR 通常一次只能解決一個問題。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-170">Each PR should usually address one issue at a time.</span></span> <span data-ttu-id="7d9e4-171">PR 可修改一或多個檔案。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-171">The PR can modify one or multiple files.</span></span> <span data-ttu-id="7d9e4-172">如果您要解決不同檔案的多個修正，最好使用個別 PR。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-172">If you're addressing multiple fixes on different files, separate PRs are preferred.</span></span> <span data-ttu-id="7d9e4-173">如果要建立範例並更新 Markdown，則需要為範例建立個別 PR。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-173">If you're creating samples as well as updating markdown, you'll need to create a separate PR for samples.</span></span>

<span data-ttu-id="7d9e4-174">如果您的 PR 會修正現有問題，請將 `Fixes #Issue_Number` 關鍵字新增至認可訊息或 PR 描述。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-174">If your PR fixes an existing issue, add the `Fixes #Issue_Number` keyword to the commit message or PR description.</span></span> <span data-ttu-id="7d9e4-175">如此一來，當 PR 合併之後，就會自動關閉問題。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-175">That way, the issue is automatically closed when the PR is merged.</span></span> <span data-ttu-id="7d9e4-176">如需詳細資訊，請參閱 [Closing issues via commit messages](https://help.github.com/articles/closing-issues-via-commit-messages/) (透過認可訊息關閉問題)。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-176">For more information, see [Closing issues via commit messages](https://help.github.com/articles/closing-issues-via-commit-messages/).</span></span>

<span data-ttu-id="7d9e4-177">.NET 小組將會審查您的 PR，並讓您知道是否需要任何其他更新/變更以通過核准。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-177">The .NET team will review your PR and let you know if there are any other updates/changes necessary in order to approve it.</span></span>

<span data-ttu-id="7d9e4-178">**步驟 5：** 根據與小組的討論結果，對您的分支進行任何必要的更新。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-178">**Step 5:** Make any necessary updates to your branch as discussed with the team.</span></span>

<span data-ttu-id="7d9e4-179">一旦套用意見反應並核准您的變更，維護人員就會將您的 PR 合併到主分支。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-179">The maintainers will merge your PR into the master branch once feedback has been applied and your change is approved.</span></span>

<span data-ttu-id="7d9e4-180">我們會定期從主分支將所有認可推送至即時分支，之後您將能夠在 https://docs.microsoft.com/dotnet/ 上看到您的即時參與。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-180">We regularly push all commits from master branch into the live branch and then you'll be able to see your contribution live at https://docs.microsoft.com/dotnet/.</span></span> <span data-ttu-id="7d9e4-181">我們一般會在工作週期間每天發佈。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-181">We typically publish daily during the work week.</span></span>

## <a name="contribute-to-samples"></a><span data-ttu-id="7d9e4-182">參與範例</span><span class="sxs-lookup"><span data-stu-id="7d9e4-182">Contribute to samples</span></span>

<span data-ttu-id="7d9e4-183">我們對程式碼進行了下列區別，以支援我們的內容：</span><span class="sxs-lookup"><span data-stu-id="7d9e4-183">We make the following distinction for code that supports our content:</span></span>

- <span data-ttu-id="7d9e4-184">範例：讀者可以下載並執行範例。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-184">Samples: readers can download and run the samples.</span></span> <span data-ttu-id="7d9e4-185">所有範例都應該是完整的應用程式或程式庫。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-185">All samples should be complete applications or libraries.</span></span> <span data-ttu-id="7d9e4-186">使用範例建立程式庫時，應該包含單元測試或應用程式，讓讀者執行程式碼。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-186">Where the sample creates a library, it should include unit tests or an application that lets readers run the code.</span></span> <span data-ttu-id="7d9e4-187">這些範例通常會使用多項技術、功能或工具組。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-187">They often use more than one technology, feature, or toolkit.</span></span> <span data-ttu-id="7d9e4-188">每個範例的 readme.md 檔案會參考一篇文章，您可以閱讀以深入了解每個範例所包含的概念。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-188">The readme.md file for each sample will refer to the article so that you can read more about the concepts covered in each sample.</span></span>
- <span data-ttu-id="7d9e4-189">程式碼片段：說明較小的概念或工作。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-189">Snippets: illustrate a smaller concept or task.</span></span> <span data-ttu-id="7d9e4-190">它們可供編譯但並非用作完整的應用程式。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-190">They compile but they are not intended to be complete applications.</span></span> <span data-ttu-id="7d9e4-191">它們應該會正確執行，但不是典型案例的範例應用程式。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-191">They should run correctly, but aren't an example application for a typical scenario.</span></span> <span data-ttu-id="7d9e4-192">相反地，它們設計成盡可能小到足以說明單一概念或功能。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-192">Instead, they are designed to be as small as possible to illustrate a single concept or feature.</span></span> <span data-ttu-id="7d9e4-193">這些程式碼片段不應該超過一個螢幕的程式碼。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-193">These should be no more than a single screen of code.</span></span>

<span data-ttu-id="7d9e4-194">範例儲存在 [dotnet/samples](https://github.com/dotnet/samples) 存放庫中。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-194">Samples are stored in the [dotnet/samples](https://github.com/dotnet/samples) repository.</span></span> <span data-ttu-id="7d9e4-195">我們將致力於建立 samples 資料夾結構符合文件資料夾結構的模型。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-195">We are working toward a model where our samples folder structure matches our docs folder structure.</span></span> <span data-ttu-id="7d9e4-196">我們遵循下列標準：</span><span class="sxs-lookup"><span data-stu-id="7d9e4-196">Standards that we follow are:</span></span>

- <span data-ttu-id="7d9e4-197">最上層資料夾會對應到 *docs* 存放庫中的最上層資料夾。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-197">Top-level folders match the top level folders in the *docs* repository.</span></span> <span data-ttu-id="7d9e4-198">例如，文件存放庫具有 *machine-learning/tutorials* 資料夾，而機器學習服務教學課程的範例會位於 *samples/machine-learning/tutorials* 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-198">For example, the docs repository has a *machine-learning/tutorials* folder, and the samples for machine learning tutorials are in the *samples/machine-learning/tutorials* folder.</span></span>

<span data-ttu-id="7d9e4-199">此外，*core* 和 *standard* 資料夾下所有範例都應該在 .NET Core 支援的所有平台上建置和執行。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-199">In addition, all samples under the *core* and *standard* folders should build and run on all platforms supported by .NET Core.</span></span> <span data-ttu-id="7d9e4-200">我們的 CI 建置系統將會強制執行該項作業。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-200">Our CI build system will enforce that.</span></span> <span data-ttu-id="7d9e4-201">最上層 *framework* 資料夾包含只能在 Windows 上建置和驗證的範例。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-201">The top level *framework* folder contains samples that are only built and validated on Windows.</span></span>

<span data-ttu-id="7d9e4-202">請盡可能在適用於指定範例的一組最廣泛平台上建置和執行範例專案。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-202">Sample projects should build and run on the widest set of platforms possible for the given sample.</span></span> <span data-ttu-id="7d9e4-203">實際上，這表示盡可能建置以 .NET Core 為基礎的主控台應用程式。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-203">In practice, that means building .NET Core-based console applications where possible.</span></span> <span data-ttu-id="7d9e4-204">Web 或 UI 架構特定的範例應該視需要新增這些工具。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-204">Samples that are specific to the web or a UI framework should add those tools as needed.</span></span> <span data-ttu-id="7d9e4-205">範例包括 Web 應用程式、行動應用程式、WPF 或 WinForms 應用程式等。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-205">Examples include web applications, mobile apps, WPF or WinForms apps, and so on.</span></span>

<span data-ttu-id="7d9e4-206">我們將致力於開發適用於所有程式碼的 CI 系統。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-206">We are working toward having a CI system in place for all code.</span></span> <span data-ttu-id="7d9e4-207">當您對範例進行任何更新時，請確定每項更新都是可建置專案的一部分。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-207">When you make any updates to samples, make sure each update is part of a buildable project.</span></span> <span data-ttu-id="7d9e4-208">在理想情況下，也可針對範例的正確性新增測試。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-208">Ideally, add tests for correctness on samples as well.</span></span>

<span data-ttu-id="7d9e4-209">您所建立的每個完整範例都應該包含一個 *readme.md* 檔案。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-209">Each complete sample that you create should contain a *readme.md* file.</span></span> <span data-ttu-id="7d9e4-210">此檔案應該包含範例的簡短描述 (一或兩個段落)。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-210">This file should contain a short description of the sample (one or two paragraphs).</span></span> <span data-ttu-id="7d9e4-211">您的 *readme.md* 應該告訴讀者探索此範例將會學到的內容。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-211">Your *readme.md* should tell readers what they will learn by exploring this sample.</span></span> <span data-ttu-id="7d9e4-212">*readme.md* 檔案也應該包含 [.NET 文件網站](https://docs.microsoft.com/dotnet/welcome)上即時文件的連結。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-212">The *readme.md* file should also contain a link to the live document on the [.NET documentation site](https://docs.microsoft.com/dotnet/welcome).</span></span> <span data-ttu-id="7d9e4-213">若要判斷存放庫中指定檔案對應至該網站的位置，請將存放庫路徑中的 `/docs` 取代為 `https://docs.microsoft.com/dotnet`。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-213">To determine where a given file in the repository maps to that site, replace `/docs` in the repository path with `https://docs.microsoft.com/dotnet`.</span></span>

<span data-ttu-id="7d9e4-214">您的主題也會包含範例連結。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-214">Your topic will also contain links to the sample.</span></span> <span data-ttu-id="7d9e4-215">這會直接連結至 GitHub 上的範例資料夾。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-215">Link directly to the sample's folder on GitHub.</span></span>

### <a name="write-a-new-sample"></a><span data-ttu-id="7d9e4-216">撰寫新的範例</span><span class="sxs-lookup"><span data-stu-id="7d9e4-216">Write a new sample</span></span>

<span data-ttu-id="7d9e4-217">範例為可供下載的完整程式與程式庫。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-217">Samples are full programs and libraries meant for download.</span></span> <span data-ttu-id="7d9e4-218">範例的範圍可能很小，但會以可讓使用者自行探索與實驗的方式來示範概念。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-218">They may be small in scope, but they demonstrate concepts in a manner that enables people to explore and experiment on their own.</span></span> <span data-ttu-id="7d9e4-219">範例的指導方針確保讀者可下載與探索。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-219">The guidelines for samples ensure readers can download and explore.</span></span> <span data-ttu-id="7d9e4-220">檢查 [Parallel LINQ (PLINQ)](https://github.com/dotnet/samples/tree/master/csharp/parallel/PLINQ) 範例，以作為每個指導方針的範例。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-220">Examine the [Parallel LINQ (PLINQ)](https://github.com/dotnet/samples/tree/master/csharp/parallel/PLINQ) samples as an example of each of the guidelines.</span></span>

1. <span data-ttu-id="7d9e4-221">範例**必須是可建置專案的一部分**。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-221">Your sample **must be part of a buildable project**.</span></span> <span data-ttu-id="7d9e4-222">請盡可能在 .NET Core 支援的所有平台上建置專案。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-222">Where possible, the projects should build on all platforms supported by .NET Core.</span></span> <span data-ttu-id="7d9e4-223">但示範平台特定功能或平台特定工具的範例則除外。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-223">Exceptions to this are samples that demonstrate a platform specific feature or platform specific tool.</span></span>

2. <span data-ttu-id="7d9e4-224">您的範例應該遵守 [C# Coding Style](https://github.com/dotnet/corefx/blob/master/Documentation/coding-guidelines/coding-style.md) (CoreFX 編碼樣式) 以確保一致性。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-224">Your sample should conform to the [corefx coding style](https://github.com/dotnet/corefx/blob/master/Documentation/coding-guidelines/coding-style.md) to maintain consistency.</span></span>

   <span data-ttu-id="7d9e4-225">此外，當示範不需要具現化新物件的內容時，我們偏好使用 `static` 方法，而不是執行個體方法。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-225">Additionally, we prefer the use of `static` methods rather than instance methods when demonstrating something that doesn't require instantiating a new object.</span></span>

3. <span data-ttu-id="7d9e4-226">您的範例應該包含**適當的例外狀況處理**。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-226">Your sample should include **appropriate exception handling**.</span></span> <span data-ttu-id="7d9e4-227">它應該處理範例內容中可能擲回的所有例外狀況。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-227">It should handle all exceptions that are likely to be thrown in the context of the sample.</span></span> <span data-ttu-id="7d9e4-228">例如，呼叫 [Console.ReadLine](https://docs.microsoft.com/dotnet/api/system.console.readline) 方法以擷取使用者輸入的範例應該在輸入字串作為引數傳遞至方法時，使用適當的例外狀況處理。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-228">For example, a sample that calls the [Console.ReadLine](https://docs.microsoft.com/dotnet/api/system.console.readline) method to retrieve user input should use appropriate exception handling when the input string is passed as an argument to a method.</span></span> <span data-ttu-id="7d9e4-229">同樣地，如果您的範例預期方法呼叫失敗，則必須處理產生的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-229">Similarly, if your sample expects a method call to fail, the resulting exception must be handled.</span></span> <span data-ttu-id="7d9e4-230">請務必處理方法所擲回的特定例外狀況，而不是 [Exception](https://docs.microsoft.com/dotnet/api/system.exception) 或 [SystemException](https://docs.microsoft.com/dotnet/api/system.systemexception) 等基底類別例外狀況。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-230">Always handle the specific exceptions thrown by the method, rather than base class exceptions such as [Exception](https://docs.microsoft.com/dotnet/api/system.exception) or [SystemException](https://docs.microsoft.com/dotnet/api/system.systemexception).</span></span>

<span data-ttu-id="7d9e4-231">若要建立範例：</span><span class="sxs-lookup"><span data-stu-id="7d9e4-231">To create a sample:</span></span>

1. <span data-ttu-id="7d9e4-232">提出[問題](https://github.com/dotnet/docs/issues)，或對您目前參與的現有問題新增註解。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-232">File an [issue](https://github.com/dotnet/docs/issues) or add a comment to an existing one that you are working on it.</span></span>
2. <span data-ttu-id="7d9e4-233">撰寫主題，以說明您範例中所示範的概念 (例如：`docs/standard/linq/where-clause.md`)。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-233">Write the topic that explains the concepts demonstrated in your sample (example: `docs/standard/linq/where-clause.md`).</span></span>
3. <span data-ttu-id="7d9e4-234">撰寫您的範例 (例如：`WhereClause-Sample1.cs`)。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-234">Write your sample (example: `WhereClause-Sample1.cs`).</span></span>
4. <span data-ttu-id="7d9e4-235">建立 Program.cs，其中包含呼叫您範例的主要進入點。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-235">Create a Program.cs with a Main entry point that calls your samples.</span></span> <span data-ttu-id="7d9e4-236">如果已有此檔案，請將呼叫新增至您的範例：</span><span class="sxs-lookup"><span data-stu-id="7d9e4-236">If there is already one there, add the call to your sample:</span></span>

    ```csharp
    public class Program
    {
        public void Main(string[] args)
        {
            WhereClause1.QuerySyntaxExample();

            // Add the method syntax as an example.
            WhereClause1.MethodSyntaxExample();
        }
    }
    ```

<span data-ttu-id="7d9e4-237">請使用可透過 [.NET Core SDK](https://www.microsoft.com/net/download) 安裝的 .NET Core CLI，來建置任何 .NET Core 程式碼片段或範例。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-237">You build any .NET Core snippet or sample using the .NET Core CLI, which can be installed with [the .NET Core SDK](https://www.microsoft.com/net/download).</span></span> <span data-ttu-id="7d9e4-238">若要建置並執行您的範例：</span><span class="sxs-lookup"><span data-stu-id="7d9e4-238">To build and run your sample:</span></span>

1. <span data-ttu-id="7d9e4-239">移至範例資料夾和組建以檢查是否有錯誤：</span><span class="sxs-lookup"><span data-stu-id="7d9e4-239">Go to the sample folder and build to check for errors:</span></span>

    ```dotnetcli
    dotnet build
    ```

2. <span data-ttu-id="7d9e4-240">執行您的範例：</span><span class="sxs-lookup"><span data-stu-id="7d9e4-240">Run your sample:</span></span>

    ```dotnetcli
    dotnet run
    ```

3. <span data-ttu-id="7d9e4-241">將 readme.md 新增至您範例的根目錄。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-241">Add a readme.md to the root directory of your sample.</span></span>

   <span data-ttu-id="7d9e4-242">這應該包含程式碼的簡短描述，並指示使用者前往參考該範例的文章。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-242">This should include a brief description of the code, and refer people to the article that references the sample.</span></span> <span data-ttu-id="7d9e4-243">*readme.md* 的最上層，必須具有[範例瀏覽器](https://docs.microsoft.com/samples)所需的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-243">The top of the *readme.md* must have the metadata required for the [samples browser](https://docs.microsoft.com/samples).</span></span> <span data-ttu-id="7d9e4-244">標頭區塊應包含下欄欄位：</span><span class="sxs-lookup"><span data-stu-id="7d9e4-244">The header block should contain the following fields:</span></span>

   ```yml
   ---
   name: "really cool sample"
   description: "Learn everything about this really cool sample."
   page_type: sample
   languages:
     - csharp
     - fsharp
     - vbnet
   products:
     - dotnet-core
     - dotnet
     - dotnet-standard
     - aspnet
     - aspnet-core
     - ef-core
   ---
   ```

   - <span data-ttu-id="7d9e4-245">`languages` 集合應包含僅適用於您範例的語言。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-245">The `languages` collection should include only those languages available for your sample.</span></span>
   - <span data-ttu-id="7d9e4-246">`products` 集合應包含僅與您範例相關的產品。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-246">The `products` collection should include only those products relevant to your sample.</span></span>

<span data-ttu-id="7d9e4-247">除非另有註明，否則所有範例都是在 .NET Core 支援的任何平台上透過命令列所建置。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-247">Except where noted, all samples build from the command line on any platform supported by .NET Core.</span></span> <span data-ttu-id="7d9e4-248">有些 Visual Studio 特定的範例需要 Visual Studio 2017 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-248">There are a few samples that are specific to Visual Studio and require Visual Studio 2017 or later.</span></span> <span data-ttu-id="7d9e4-249">此外，有些顯示平台特定功能的範例需要特定平台。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-249">In addition, some samples show platform specific features and will require a specific platform.</span></span> <span data-ttu-id="7d9e4-250">其他範例和程式碼片段需要 .NET Framework 並將在 Windows 平台上執行，而且需要適用於目標 Framework 版本的開發人員套件。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-250">Other samples and snippets require the .NET Framework and will run on Windows platforms, and will need the Developer Pack for the target Framework version.</span></span>

## <a name="the-c-interactive-experience"></a><span data-ttu-id="7d9e4-251">C# 互動式體驗</span><span class="sxs-lookup"><span data-stu-id="7d9e4-251">The C# interactive experience</span></span>

<span data-ttu-id="7d9e4-252">文章中包含的所有範例都會使用[語言標記](../code-in-docs.md)來指出來源語言。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-252">All samples included in an article use a [language tag](../code-in-docs.md) to indicate the source language.</span></span> <span data-ttu-id="7d9e4-253">C# 中的簡短程式碼範例可以使用 `csharp-interactive` 語言標記來指定要在瀏覽器中執行的 C# 範例</span><span class="sxs-lookup"><span data-stu-id="7d9e4-253">Short code samples in C# can use the `csharp-interactive` language tag to specify a C# sample that runs in the browser.</span></span> <span data-ttu-id="7d9e4-254">(內嵌程式碼範例使用 `csharp-interactive` 標記，若要包含來自原始程式碼的程式碼片段，請使用 `code-csharp-interactive` 標記)。這些程式碼範例會在文章中顯示程式碼視窗或輸出視窗。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-254">(Inline code samples use the `csharp-interactive` tag, for snippets included from source, use the `code-csharp-interactive` tag.) These code samples display a code window and an output window in the article.</span></span> <span data-ttu-id="7d9e4-255">輸出視窗會顯示使用者執行範例之後執行互動式程式碼的任何輸出。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-255">The output window displays any output from executing the interactive code once the user has run the sample.</span></span>

<span data-ttu-id="7d9e4-256">C# 互動式體驗改變了我們使用範例的方式。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-256">The C# interactive experience changes how we work with samples.</span></span> <span data-ttu-id="7d9e4-257">訪客可以執行範例來查看結果。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-257">Visitors can run the sample to see the results.</span></span> <span data-ttu-id="7d9e4-258">一些因素有助於判斷範例或對應文字是否應該包含輸出的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-258">A number of factors help determine if the sample or corresponding text should include information about the output.</span></span>

### <a name="when-to-display-the-expected-output-without-running-the-sample"></a><span data-ttu-id="7d9e4-259">何時顯示預期的輸出而不需要執行範例</span><span class="sxs-lookup"><span data-stu-id="7d9e4-259">When to display the expected output without running the sample</span></span>

- <span data-ttu-id="7d9e4-260">適用於初學者的文章應該提供輸出，讓讀者可以比較其工作輸出與預期的回應。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-260">Articles intended for beginners should provide output so that readers can compare the output of their work with the expected answer.</span></span>
- <span data-ttu-id="7d9e4-261">輸出是主題不可或缺一部分的範例應該顯示該輸出。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-261">Samples where the output is integral to the topic should display that output.</span></span> <span data-ttu-id="7d9e4-262">例如，格式化文字的相關文章應該顯示文字格式，而不需要執行範例。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-262">For example, articles on formatted text should show the text format without running the sample.</span></span>
- <span data-ttu-id="7d9e4-263">若範例和預期的輸出很短，請考慮顯示輸出。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-263">When both the sample and the expected output is short, consider showing the output.</span></span> <span data-ttu-id="7d9e4-264">這會省下一些時間。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-264">It saves a bit of time.</span></span>
- <span data-ttu-id="7d9e4-265">說明目前或不因文化特性而異的文化特性 (Culture) 如何影響輸出的文章，應該說明預期的輸出。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-265">Articles explaining how current culture or invariant culture affect output should explain the expected output.</span></span> <span data-ttu-id="7d9e4-266">互動式 REPL (「讀取、求值、輸出」迴圈) 會在 Linux 主機上執行。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-266">The interactive REPL (Read Evaluate Print Loop) runs on a Linux-based host.</span></span> <span data-ttu-id="7d9e4-267">預設及不因文化特性而異的文化特性 (Culture) 會在不同作業系統和電腦上產生不同輸出。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-267">The default culture, and the invariant culture produce different output on different operating systems and machines.</span></span> <span data-ttu-id="7d9e4-268">該文應該說明 Windows、Linux 和 Mac 系統中的輸出。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-268">The article should explain the output in Windows, Linux, and Mac systems.</span></span>

### <a name="when-to-exclude-expected-output-from-the-sample"></a><span data-ttu-id="7d9e4-269">何時從範例中排除預期的輸出</span><span class="sxs-lookup"><span data-stu-id="7d9e4-269">When to exclude expected output from the sample</span></span>

- <span data-ttu-id="7d9e4-270">若文章中的範例會產生較大型輸出，則不應該在註解中包含該輸出。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-270">Articles where the sample generates a larger output should not include that in comments.</span></span> <span data-ttu-id="7d9e4-271">這會在執行範例之後使程式碼難以閱讀。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-271">It obscures the code once the sample has been run.</span></span>
- <span data-ttu-id="7d9e4-272">若文章中的範例示範一個主題，但輸出並非了解該主題的必要項目。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-272">Articles where the sample demonstrates a topic, but the output isn't integral to understanding it.</span></span> <span data-ttu-id="7d9e4-273">例如，若程式碼會執行 LINQ 查詢來說明查詢語法，然後顯示輸出集合中的每個項目。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-273">For example, code that runs a LINQ query to explain query syntax and then display every item in the output collection.</span></span>

> [!NOTE]
> <span data-ttu-id="7d9e4-274">您可能會注意到某些主題目前未遵循這裡所指定的方針。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-274">You might notice that some of the topics are not currently following all the guidelines specified here.</span></span> <span data-ttu-id="7d9e4-275">我們將致力於達成整個網站的一致性。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-275">We're working towards achieving consistency throughout the site.</span></span> <span data-ttu-id="7d9e4-276">請查看我們目前針對該特定目標所追蹤的[開啟問題](https://github.com/dotnet/docs/issues?q=is%3Aopen+is%3Aissue+label%3A%22%3Abookmark_tabs%3A+Information+Architecture%22)清單。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-276">Check the list of [open issues](https://github.com/dotnet/docs/issues?q=is%3Aopen+is%3Aissue+label%3A%22%3Abookmark_tabs%3A+Information+Architecture%22) we're currently tracking for that specific goal.</span></span>

### <a name="contributing-to-international-content"></a><span data-ttu-id="7d9e4-277">參與國際內容</span><span class="sxs-lookup"><span data-stu-id="7d9e4-277">Contributing to International content</span></span>

<span data-ttu-id="7d9e4-278">目前不接受機器翻譯 (MT) 的內容。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-278">Contributions for Machine Translated (MT) content are currently not accepted.</span></span> <span data-ttu-id="7d9e4-279">為了改善 MT 內容的品質，我們已轉換成神經 MT 引擎。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-279">In an effort to improve the quality of MT content, we've transitioned to a Neural MT engine.</span></span> <span data-ttu-id="7d9e4-280">我們接受並鼓勵人工翻譯 (HT) 內容的貢獻，這可用於訓練神經 MT 引擎。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-280">We accept and encourage contributions for Human Translated (HT) content, which is used to train the Neural MT engine.</span></span> <span data-ttu-id="7d9e4-281">經過一段時間，HT 內容的貢獻將可同時改善 HT 與 MT 的品質。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-281">So over time, contributions to HT content will improve the quality of both HT and MT.</span></span> <span data-ttu-id="7d9e4-282">MT 主題將有免責聲明，表示部分主題可能是 MT，而當編輯功能停用時，不會顯示 [編輯] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-282">MT topics will have a disclaimer stating that part of the topic may be MT, and the **Edit** button won't be displayed, as editing is disabled.</span></span>

## <a name="contributor-license-agreement"></a><span data-ttu-id="7d9e4-283">參與者授權合約</span><span class="sxs-lookup"><span data-stu-id="7d9e4-283">Contributor license agreement</span></span>

<span data-ttu-id="7d9e4-284">您必須簽署 [.NET Foundation 貢獻授權合約 (CLA)](https://cla.dotnetfoundation.org)才能合併 PR。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-284">You must sign the [.NET Foundation Contribution License Agreement (CLA)](https://cla.dotnetfoundation.org) before your PR is merged.</span></span> <span data-ttu-id="7d9e4-285">這是 .NET Foundation 中專案的一次性要求。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-285">This is a one-time requirement for projects in the .NET Foundation.</span></span> <span data-ttu-id="7d9e4-286">您可以在 Wikipedia 上深入了解[貢獻授權合約 (CLA)](http://en.wikipedia.org/wiki/Contributor_License_Agreement)。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-286">You can read more about [Contribution License Agreements (CLA)](http://en.wikipedia.org/wiki/Contributor_License_Agreement) on Wikipedia.</span></span>

<span data-ttu-id="7d9e4-287">合約：[net-foundation-contribution-license-agreement.pdf](https://github.com/dotnet/home/blob/master/guidance/net-foundation-contribution-license-agreement.pdf)</span><span class="sxs-lookup"><span data-stu-id="7d9e4-287">The agreement: [net-foundation-contribution-license-agreement.pdf](https://github.com/dotnet/home/blob/master/guidance/net-foundation-contribution-license-agreement.pdf)</span></span>

<span data-ttu-id="7d9e4-288">您不需要事先簽署合約。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-288">You don't have to sign the agreement up-front.</span></span> <span data-ttu-id="7d9e4-289">您可以如往常般複製、派生及提交 PR。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-289">You can clone, fork, and submit your PR as usual.</span></span> <span data-ttu-id="7d9e4-290">當您的 PR 建立之後，會由 CLA Bot 進行分類。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-290">When your PR is created, it is classified by a CLA bot.</span></span> <span data-ttu-id="7d9e4-291">如果變更不大 (例如修正錯字)，則 PR 會標記為 `cla-not-required`。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-291">If the change is small (for example, you fixed a typo), then the PR is labeled with `cla-not-required`.</span></span> <span data-ttu-id="7d9e4-292">否則，它會分類為 `cla-required`。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-292">Otherwise, it's classified as `cla-required`.</span></span> <span data-ttu-id="7d9e4-293">一旦您簽署了 CLA，目前和所有未來提取要求都會標記為 `cla-signed`。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-293">Once you signed the CLA, the current and all future pull requests are labeled as `cla-signed`.</span></span>
