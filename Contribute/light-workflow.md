---
title: 適用於次要或不頻繁變更的 GitHub 參與工作流程
description: 本文示範如何使用「次要」參與者工作流程為 docs.microsoft.com 文章做出貢獻。
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 10/06/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 8bde44d502e1942b0870df9dd546a97705c2bb4f
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2018
---
# <a name="github-contribution-workflow-for-minor-or-infrequent-changes"></a><span data-ttu-id="fe1cf-103">適用於次要或不頻繁變更的 GitHub 參與工作流程</span><span class="sxs-lookup"><span data-stu-id="fe1cf-103">GitHub contribution workflow for minor or infrequent changes</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fe1cf-104">所有發佈至 docs.microsoft.com 的存放庫皆採用 [Microsoft 開放原始碼管理辦法](https://opensource.microsoft.com/codeofconduct/) \(英文\) 或 [.NET Foundation 管理辦法](https://dotnetfoundation.org/code-of-conduct) \(英文\)。</span><span class="sxs-lookup"><span data-stu-id="fe1cf-104">All repositories that publish to docs.microsoft.com have adopted either the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/) or the [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct).</span></span> <span data-ttu-id="fe1cf-105">如需詳細資訊，請參閱[管理辦法常見問題集](https://opensource.microsoft.com/codeofconduct/faq/) \(英文\)。</span><span class="sxs-lookup"><span data-stu-id="fe1cf-105">For more information, see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/).</span></span> <span data-ttu-id="fe1cf-106">若有任何問題或意見，也可以連絡 [opencode@microsoft.com](mailto:opencode@microsoft.com) 或 [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org)。</span><span class="sxs-lookup"><span data-stu-id="fe1cf-106">Or contact [opencode@microsoft.com](mailto:opencode@microsoft.com), or [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org) with any questions or comments.</span></span><br>
>
> <span data-ttu-id="fe1cf-107">您在公用存放庫中針對文件和程式碼範例所提交的次要修正或釐清，將受到 [docs.microsoft.com 使用條款](https://docs.microsoft.com/legal/termsofuse)的約束。</span><span class="sxs-lookup"><span data-stu-id="fe1cf-107">Minor corrections or clarifications to documentation and code examples in public repositories are covered by the [docs.microsoft.com Terms of Use](https://docs.microsoft.com/legal/termsofuse).</span></span> <span data-ttu-id="fe1cf-108">如果您不是 Microsoft 的員工，在做出全新或重要的變更時，系統將會在提取要求中產生意見，要求您提交線上版的貢獻授權合約 (CLA)。</span><span class="sxs-lookup"><span data-stu-id="fe1cf-108">New or significant changes will generate a comment in the pull request, asking you to submit an online Contribution License Agreement (CLA) if you are not an employee of Microsoft.</span></span> <span data-ttu-id="fe1cf-109">您必須先完成填寫線上表單，我們才會接受您的提取要求。</span><span class="sxs-lookup"><span data-stu-id="fe1cf-109">We need you to complete the online form before we can accept your pull request.</span></span>

## <a name="overview"></a><span data-ttu-id="fe1cf-110">概觀</span><span class="sxs-lookup"><span data-stu-id="fe1cf-110">Overview</span></span>

<span data-ttu-id="fe1cf-111">此工作流程會使用 GitHub 的網頁型 Markdown 編輯器，以進行次要或不頻繁的變更。</span><span class="sxs-lookup"><span data-stu-id="fe1cf-111">This workflow is suitable for making minor or infrequent changes, by using GitHub's web-based Markdown editor.</span></span> <span data-ttu-id="fe1cf-112">GitHub 編輯器所提供的功能有限，因為其 UI 並不支援所有 Git 作業及撰寫案例。</span><span class="sxs-lookup"><span data-stu-id="fe1cf-112">The GitHub editor is limited in terms of what you can do, because the UI does not support all Git operations and authoring scenarios.</span></span> <span data-ttu-id="fe1cf-113">如果您需要做出較大幅度的參與，或是需要進階 Git 功能 (例如分支管理或進階的合併衝突解決方式) 的支援，請參閱[主要或長期變更工作流程](full-workflow.md)。</span><span class="sxs-lookup"><span data-stu-id="fe1cf-113">If you need to make large contributions, or you need support for advanced Git features (such as branch management or advanced merge conflict resolution), refer to the [major or long-running changes workflow](full-workflow.md).</span></span>

## <a name="procedure-for-using-the-github-editor-to-propose-your-changes"></a><span data-ttu-id="fe1cf-114">使用 GitHub 編輯器來建議變更的程序</span><span class="sxs-lookup"><span data-stu-id="fe1cf-114">Procedure for using the GitHub editor to propose your changes</span></span>

1. <span data-ttu-id="fe1cf-115">瀏覽至文章相對應的 GitHub 存放庫和 Markdown 檔案。</span><span class="sxs-lookup"><span data-stu-id="fe1cf-115">Browse to the article's corresponding GitHub repository and Markdown file.</span></span> <span data-ttu-id="fe1cf-116">您可以使用下列其中一種方法：</span><span class="sxs-lookup"><span data-stu-id="fe1cf-116">You can use either of the following methods:</span></span>

   - <span data-ttu-id="fe1cf-117">透過在相關的 GitHub 存放庫中瀏覽 Markdown 檔案以找出該篇文章。</span><span class="sxs-lookup"><span data-stu-id="fe1cf-117">Find the article by browsing through the Markdown files in the related GitHub repository.</span></span>
   - <span data-ttu-id="fe1cf-118">於 [docs.microsoft.com](https://docs.microsoft.com/) 上移至該篇文章，然後選取頁面右上角的 [編輯] 連結。</span><span class="sxs-lookup"><span data-stu-id="fe1cf-118">Go to the article on [docs.microsoft.com](https://docs.microsoft.com/) and select the **Edit** link in the upper-right corner of the page.</span></span>

     ![[編輯] 連結的位置](./media/light-workflow/contributetogit.png)

2. <span data-ttu-id="fe1cf-120">選取 [編輯此檔案] 鉛筆圖示來進入編輯模式︰</span><span class="sxs-lookup"><span data-stu-id="fe1cf-120">Select the **Edit this file** pencil icon to go into edit mode:</span></span>

    ![鉛筆圖示的位置](./media/light-workflow/editicon.png)

3. <span data-ttu-id="fe1cf-122">透過在 [編輯檔案] 索引標籤上使用 Markdown 來做出變更，並在 [預覽變更] 索引標籤上預覽您的變更。編輯器的使用方法相當直覺，但如果需要協助，請參閱下列指南：</span><span class="sxs-lookup"><span data-stu-id="fe1cf-122">Make changes by using Markdown on the **Edit file** tab, and preview your changes on the **Preview changes** tab. Using the editor is fairly straightforward, but if you need assistance, see the following guides:</span></span>

   - [<span data-ttu-id="fe1cf-123">如何使用 Markdown</span><span class="sxs-lookup"><span data-stu-id="fe1cf-123">How to use Markdown</span></span>](how-to-write-use-markdown.md)
   - <span data-ttu-id="fe1cf-124">[在 GitHub 上建立檔案](https://github.com/blog/1327-creating-files-on-github) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="fe1cf-124">[Creating files on GitHub](https://github.com/blog/1327-creating-files-on-github)</span></span>
   - <span data-ttu-id="fe1cf-125">[將檔案上傳至您的存放庫](https://github.com/blog/2105-upload-files-to-your-repositories) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="fe1cf-125">[Upload files to your repositories](https://github.com/blog/2105-upload-files-to-your-repositories)</span></span>

4. <span data-ttu-id="fe1cf-126">捲動至頁面底部，您將會看見下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="fe1cf-126">Scroll to the bottom of the page, where you see one of the following:</span></span>

   - <span data-ttu-id="fe1cf-127">**建議檔案變更**：會在您針對存放庫具有唯讀存取權時顯示，例如當您在[編輯另一個使用者的存放庫檔案時](https://help.github.com/articles/editing-files-in-another-user-s-repository/) \(英文\)。</span><span class="sxs-lookup"><span data-stu-id="fe1cf-127">**Propose file change**: Appears when you have read-only access to the repository, such as [editing files in another user's repository](https://help.github.com/articles/editing-files-in-another-user-s-repository/).</span></span> <span data-ttu-id="fe1cf-128">在此情況下，GitHub 會在您的存放庫分叉中建立「修補」分支 (如果分叉不存在，系統將會自動建立)。</span><span class="sxs-lookup"><span data-stu-id="fe1cf-128">In this case, GitHub will create a "patch" branch in your fork of the repository (and automatically create a fork if it doesn't exist).</span></span> <span data-ttu-id="fe1cf-129">當您選取 [建議檔案變更] 之後，[比較變更] 頁面便會出現，以供您確認自己的變更。</span><span class="sxs-lookup"><span data-stu-id="fe1cf-129">After you select **Propose file change**, a **Comparing changes** page appears so you can verify your changes.</span></span> <span data-ttu-id="fe1cf-130">接著，請選取 [建立提取要求] 按鈕以將變更提交至提取要求佇列，並繼續移至[下一節](#pull-request-processing)。</span><span class="sxs-lookup"><span data-stu-id="fe1cf-130">Then select the **Create pull request** button to submit your changes to the pull request queue, and proceed to the [next section](#pull-request-processing).</span></span>

   - <span data-ttu-id="fe1cf-131">**認可變更**：會在您針對存放庫具有寫入權限時顯示，例如當您在[編輯自己的存放庫檔案時](https://help.github.com/articles/editing-files-in-your-repository/) \(英文\)。</span><span class="sxs-lookup"><span data-stu-id="fe1cf-131">**Commit changes**: Appears when you have write permissions to a repository, such as [editing files in your own repository](https://help.github.com/articles/editing-files-in-your-repository/).</span></span> <span data-ttu-id="fe1cf-132">在此情況下，GitHub 會給您兩個儲存變更的選項：</span><span class="sxs-lookup"><span data-stu-id="fe1cf-132">In this case, GitHub gives you two options for saving your changes:</span></span>

     - <span data-ttu-id="fe1cf-133">**直接認可至 `<branch-name>` 分支**：其中 `<branch-name>` 是您選取 [編輯] 按鈕時所處於的分支名稱。</span><span class="sxs-lookup"><span data-stu-id="fe1cf-133">**Commit directly to the `<branch-name>` branch**, where `<branch-name>` is the name of the branch that you were on when you selected the **Edit** button.</span></span> <span data-ttu-id="fe1cf-134">這會將您的變更直接套用至分支，而不會使用提取要求。</span><span class="sxs-lookup"><span data-stu-id="fe1cf-134">This applies your changes directly to the branch instead of using a pull request.</span></span> <span data-ttu-id="fe1cf-135">到這裡您就已經完成了！</span><span class="sxs-lookup"><span data-stu-id="fe1cf-135">At this point, you're finished!</span></span>

     - <span data-ttu-id="fe1cf-136">**針對此認可建立新分支並啟動提取要求**：這會向您顯示預設名稱以建立新的分支。</span><span class="sxs-lookup"><span data-stu-id="fe1cf-136">**Create a new branch for this commit and start a pull request**, which prompts you with a default name to create a new branch.</span></span> <span data-ttu-id="fe1cf-137">當您選取 [建議檔案變更] 之後，[比較變更] 頁面便會出現，以供您確認自己的變更。</span><span class="sxs-lookup"><span data-stu-id="fe1cf-137">After you select **Propose file change**, a **Comparing changes** page appears so you can verify your changes.</span></span> <span data-ttu-id="fe1cf-138">接著，請選取 [建立提取要求] 按鈕以將變更提交至提取要求佇列，並繼續移至[下一節](#pull-request-processing)。</span><span class="sxs-lookup"><span data-stu-id="fe1cf-138">Then select the **Create pull request** button to submit your changes to the pull request queue, and proceed to the [next section](#pull-request-processing).</span></span>

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## <a name="next-steps"></a><span data-ttu-id="fe1cf-139">後續步驟</span><span class="sxs-lookup"><span data-stu-id="fe1cf-139">Next steps</span></span>

- <span data-ttu-id="fe1cf-140">請繼續移至＜有關撰寫的基本資訊＞文章，以深入了解 Markdown 和 Markdown 擴充功能語法等內容。</span><span class="sxs-lookup"><span data-stu-id="fe1cf-140">Continue to the "Writing essentials" articles to learn more about Markdown, Markdown extensions syntax, and more.</span></span>
