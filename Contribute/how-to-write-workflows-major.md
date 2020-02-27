---
title: 適用於主要或長期變更的 GitHub 參與工作流程
description: 本文示範如何使用「主要」參與者工作流程為 docs.microsoft.com 文章做出貢獻。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 08/30/2017
ms.openlocfilehash: 997f313e94e4858f37501736c1ec0be2fa8fd552
ms.sourcegitcommit: a812d716b31084926b886b93923f9b84c9b23429
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/18/2019
ms.locfileid: "75188230"
---
# <a name="github-contribution-workflow-for-major-or-long-running-changes"></a><span data-ttu-id="6f081-103">適用於主要或長期變更的 GitHub 參與工作流程</span><span class="sxs-lookup"><span data-stu-id="6f081-103">GitHub contribution workflow for major or long-running changes</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6f081-104">所有發佈至 docs.microsoft.com 的存放庫皆採用 [Microsoft 開放原始碼管理辦法](https://opensource.microsoft.com/codeofconduct/) \(英文\) 或 [.NET Foundation 管理辦法](https://dotnetfoundation.org/code-of-conduct) \(英文\)。</span><span class="sxs-lookup"><span data-stu-id="6f081-104">All repositories that publish to docs.microsoft.com have adopted either the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/) or the [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct).</span></span> <span data-ttu-id="6f081-105">如需詳細資訊，請參閱[管理辦法常見問題集](https://opensource.microsoft.com/codeofconduct/faq/) \(英文\)。</span><span class="sxs-lookup"><span data-stu-id="6f081-105">For more information, see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/).</span></span> <span data-ttu-id="6f081-106">若有任何問題或意見，也可以連絡 [opencode@microsoft.com](mailto:opencode@microsoft.com) 或 [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org)。</span><span class="sxs-lookup"><span data-stu-id="6f081-106">Or contact [opencode@microsoft.com](mailto:opencode@microsoft.com), or [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org) with any questions or comments.</span></span><br>
>
> <span data-ttu-id="6f081-107">您在公用存放庫中針對文件和程式碼範例所提交的次要修正或釐清，將受到 [docs.microsoft.com 使用條款](https://docs.microsoft.com/legal/termsofuse)的約束。</span><span class="sxs-lookup"><span data-stu-id="6f081-107">Minor corrections or clarifications to documentation and code examples in public repositories are covered by the [docs.microsoft.com Terms of Use](https://docs.microsoft.com/legal/termsofuse).</span></span> <span data-ttu-id="6f081-108">如果您不是 Microsoft 的員工，在做出全新或重要的變更時，系統將會在提取要求中產生意見，要求您提交線上版的貢獻授權合約 (CLA)。</span><span class="sxs-lookup"><span data-stu-id="6f081-108">New or significant changes will generate a comment in the pull request, asking you to submit an online Contribution License Agreement (CLA) if you are not an employee of Microsoft.</span></span> <span data-ttu-id="6f081-109">您必須先完成線上表單，您的提取要求才會被合併。</span><span class="sxs-lookup"><span data-stu-id="6f081-109">You will need to complete the online form before your pull request can be merged.</span></span>

## <a name="overview"></a><span data-ttu-id="6f081-110">概觀</span><span class="sxs-lookup"><span data-stu-id="6f081-110">Overview</span></span>

<span data-ttu-id="6f081-111">此工作流程適用於需要對某個存放庫進行主要變更，或會成為該存放庫頻繁參與者的參與者。</span><span class="sxs-lookup"><span data-stu-id="6f081-111">This workflow is suitable for a contributor who needs to make a major change or will be a frequent contributor to a repository.</span></span> <span data-ttu-id="6f081-112">頻繁的參與者通常會有進行中 (長期) 的變更，這些變更在提取要求完成簽核並合併之前，都需要經歷多個建置/驗證/暫存循環或是花費許多天才能完成。</span><span class="sxs-lookup"><span data-stu-id="6f081-112">Frequent contributors typically have ongoing (long-running) changes, which go through multiple build/validation/staging cycles or span multiple days before pull request sign-off and merge.</span></span>

<span data-ttu-id="6f081-113">這些參與類型的範例包括：</span><span class="sxs-lookup"><span data-stu-id="6f081-113">Examples of these types of contributions include:</span></span>

[!INCLUDE[contribute-major-changes-change-definition](includes/contribute-how-to-write-workflows-major-change-definition.md)]

### <a name="terminology"></a><span data-ttu-id="6f081-114">術語</span><span class="sxs-lookup"><span data-stu-id="6f081-114">Terminology</span></span>

<span data-ttu-id="6f081-115">在您開始之前，讓我們先檢閱一些用於此工作流程的 Git/GitHub 詞彙及代號。</span><span class="sxs-lookup"><span data-stu-id="6f081-115">Before you start, let's review some of the Git/GitHub terms and monikers used in this workflow.</span></span> <span data-ttu-id="6f081-116">您暫時還不需要了解它們。</span><span class="sxs-lookup"><span data-stu-id="6f081-116">Don't worry about understanding them now.</span></span> <span data-ttu-id="6f081-117">您只需要知道自己將會學習它們，並可以在需要確認定義時回來參考本節。</span><span class="sxs-lookup"><span data-stu-id="6f081-117">Just know that you will be learning about them, and you can refer back to this section when you need to verify a definition.</span></span>

| <span data-ttu-id="6f081-118">Name</span><span class="sxs-lookup"><span data-stu-id="6f081-118">Name</span></span> | <span data-ttu-id="6f081-119">描述</span><span class="sxs-lookup"><span data-stu-id="6f081-119">Description</span></span> |
|-----------|-------------|
|<span data-ttu-id="6f081-120">分叉</span><span class="sxs-lookup"><span data-stu-id="6f081-120">fork</span></span>|<span data-ttu-id="6f081-121">通常是作為名詞使用，用來描述主要 GitHub 存放庫的複本。</span><span class="sxs-lookup"><span data-stu-id="6f081-121">Normally used as a noun, when referring to a copy of a main GitHub repository.</span></span> <span data-ttu-id="6f081-122">實際上，分叉只是另一個存放庫。</span><span class="sxs-lookup"><span data-stu-id="6f081-122">In practice, a fork is just another repository.</span></span> <span data-ttu-id="6f081-123">但它的特殊之處在於 GitHub 會維護與主要/父存放庫之間的關係。</span><span class="sxs-lookup"><span data-stu-id="6f081-123">But it's special in the sense that GitHub maintains a connection back to the main/parent repository.</span></span> <span data-ttu-id="6f081-124">它有時會作為動詞使用，例如「您必須先針對存放庫進行分叉」。</span><span class="sxs-lookup"><span data-stu-id="6f081-124">It's sometimes used as a verb, as in "You must fork the repository first."</span></span>|
|<span data-ttu-id="6f081-125">遠端 (Remote)</span><span class="sxs-lookup"><span data-stu-id="6f081-125">remote</span></span>|<span data-ttu-id="6f081-126">針對遠端存放庫的具名關係，例如「原始」或「上游」遠端。</span><span class="sxs-lookup"><span data-stu-id="6f081-126">A named connection to a remote repository, such as the "origin" or "upstream" remote.</span></span> <span data-ttu-id="6f081-127">Git 會將此稱為遠端，因為它是用來參考裝載於另一部電腦上的存放庫。</span><span class="sxs-lookup"><span data-stu-id="6f081-127">Git refers to this as remote because it is used to reference a repository that's hosted on another computer.</span></span> <span data-ttu-id="6f081-128">在此工作流程中，「遠端」一律會是 GitHub 存放庫。</span><span class="sxs-lookup"><span data-stu-id="6f081-128">In this workflow, a remote is always a GitHub repository.</span></span>|
|<span data-ttu-id="6f081-129">原始 (Origin)</span><span class="sxs-lookup"><span data-stu-id="6f081-129">origin</span></span>|<span data-ttu-id="6f081-130">指派給本機存放庫和複製該存放庫之原始存放庫之間關係的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f081-130">The name assigned to the connection between your local repository and the repository from which it was cloned.</span></span> <span data-ttu-id="6f081-131">在此工作流程中，「原始」代表針對您分叉的關係。</span><span class="sxs-lookup"><span data-stu-id="6f081-131">In this workflow, origin represents the connection to your fork.</span></span> <span data-ttu-id="6f081-132">它有時候會作為原始存放庫本身的代號，例如「記得將您的變更推送到原始」。</span><span class="sxs-lookup"><span data-stu-id="6f081-132">It's sometimes used as a moniker for the origin repository itself, as in "Remember to push your changes to origin."</span></span>|
|<span data-ttu-id="6f081-133">上游 (Upstream)</span><span class="sxs-lookup"><span data-stu-id="6f081-133">upstream</span></span>|<span data-ttu-id="6f081-134">上游和原始遠端相同，是針對另一個存放庫的具名關係。</span><span class="sxs-lookup"><span data-stu-id="6f081-134">Like the origin remote, upstream is a named connection to another repository.</span></span> <span data-ttu-id="6f081-135">在此工作流程中，「上游」代表您的本機存放庫及主要存放庫 (也就是從之建立分叉的存放庫) 之間的關係。</span><span class="sxs-lookup"><span data-stu-id="6f081-135">In this workflow, upstream represents the connection between your local repository and the main repository, from which your fork was created.</span></span> <span data-ttu-id="6f081-136">它有時候會作為上游存放庫本身的代號，例如「記得從上游提取變更」。</span><span class="sxs-lookup"><span data-stu-id="6f081-136">It's sometimes used as a moniker for the upstream repository itself, as in "Remember to pull the changes from upstream."</span></span>|

## <a name="workflow"></a><span data-ttu-id="6f081-137">工作流程</span><span class="sxs-lookup"><span data-stu-id="6f081-137">Workflow</span></span>

>[!IMPORTANT]
> <span data-ttu-id="6f081-138">如果您尚未完成[設定](get-started-setup-github.md)一節中的步驟，請務必完成它們。</span><span class="sxs-lookup"><span data-stu-id="6f081-138">If you haven't already, you must complete the steps in the [Setup](get-started-setup-github.md) section.</span></span> <span data-ttu-id="6f081-139">本節會引導您設定 GitHub 帳戶、安裝 Git Bash 和 Markdown 編輯器、建立分叉，以及設定本機存放庫。</span><span class="sxs-lookup"><span data-stu-id="6f081-139">This section walks you through setting up your GitHub account, installing Git Bash and a Markdown editor, creating a fork, and setting up your local repository.</span></span> <span data-ttu-id="6f081-140">如果您不熟悉 Git 和 GitHub 概念 (例如存放庫或分支等)，請先檢閱 [Git 和 GitHub 基本概念](git-github-fundamentals.md)。</span><span class="sxs-lookup"><span data-stu-id="6f081-140">If you are unfamiliar with Git and GitHub concepts such as a repository or branch, please first review [Git and GitHub fundamentals](git-github-fundamentals.md).</span></span>

<span data-ttu-id="6f081-141">在此工作流程中，變更流程會是重複性的循環。</span><span class="sxs-lookup"><span data-stu-id="6f081-141">In this workflow, changes flow in a repetitive cycle.</span></span> <span data-ttu-id="6f081-142">變更會從裝置的本機存放庫開始，回流至 GitHub 分叉，接著傳送至主要 GitHub 存放庫，然後隨著您納入來自其他參與者的變更再次返回本機。</span><span class="sxs-lookup"><span data-stu-id="6f081-142">Starting from your device's local repository, they flow back up to your GitHub fork, into the main GitHub repository, and back down locally again as you incorporate changes from other contributors.</span></span>

### <a name="use-github-flow"></a><span data-ttu-id="6f081-143">使用 GitHub 流程</span><span class="sxs-lookup"><span data-stu-id="6f081-143">Use GitHub flow</span></span>

<span data-ttu-id="6f081-144">在 [Git 和 GitHub 基本概念](git-github-fundamentals.md#git)中，有提到 Git 存放庫會包含一個主要分支，以及任何其他尚未整合至「主要」的處理中分支。</span><span class="sxs-lookup"><span data-stu-id="6f081-144">Recall from [Git and GitHub fundamentals](git-github-fundamentals.md#git) that a Git repository contains a master branch, plus any additional work-in-progress branches that have not been integrated into master.</span></span> <span data-ttu-id="6f081-145">每當您要導入一系列邏輯相關的變更時，最佳做法為建立「工作分支」  來透過工作流程管理這些變更。</span><span class="sxs-lookup"><span data-stu-id="6f081-145">Whenever you introduce a set of logically related changes, it’s a best practice to create a *working branch* to manage your changes through the workflow.</span></span> <span data-ttu-id="6f081-146">我們在此之所以將它稱為工作分支，是因為它是將變更整合至主要分支之前，對變更進行逐一查看/改進的工作空間。</span><span class="sxs-lookup"><span data-stu-id="6f081-146">We refer to it here as a working branch because it's a workspace to iterate/refine changes, until they can be integrated back into the master branch.</span></span>

<span data-ttu-id="6f081-147">將相關聯的變更隔離限制於特定分支中，可讓您獨立地控制及導入變更，並將其目標設定為發佈週期中的特定發行時間。</span><span class="sxs-lookup"><span data-stu-id="6f081-147">Isolating related changes to a specific branch allows you to control and introduce those changes independently, targeting them to a specific release time in the publishing cycle.</span></span> <span data-ttu-id="6f081-148">在現實中，根據所進行工作的不同，您的存放庫中很容易就會出現數個工作分支。</span><span class="sxs-lookup"><span data-stu-id="6f081-148">In reality, depending on the type of work you do, you can easily end up with several working branches in your repository.</span></span> <span data-ttu-id="6f081-149">同時處理多個分支 (每個分支都代表不同的專案) 的情況，其實相當常見。</span><span class="sxs-lookup"><span data-stu-id="6f081-149">It's not uncommon to be working on multiple branches at the same time, each representing a different project.</span></span>

>[!TIP]
><span data-ttu-id="6f081-150">直接在主要分支中做出變更並不是  良好的做法。</span><span class="sxs-lookup"><span data-stu-id="6f081-150">Making your changes in the master branch is *not* a good practice.</span></span> <span data-ttu-id="6f081-151">假設您使用主要分支，以針對預定時程的功能發行導入一系列變更。</span><span class="sxs-lookup"><span data-stu-id="6f081-151">Imagine that you use the master branch to introduce a set of changes for a timed feature release.</span></span> <span data-ttu-id="6f081-152">您完成變更，並正在等待發行這些變更。</span><span class="sxs-lookup"><span data-stu-id="6f081-152">You finish the changes and are waiting to release them.</span></span> <span data-ttu-id="6f081-153">在此期間，您收到修正某個項目的緊急要求，因此您對主要分支中的某個檔案做出變更並將它發佈。</span><span class="sxs-lookup"><span data-stu-id="6f081-153">Then in the interim, you have an urgent request to fix something, so you make the change to a file in the master branch and then publish the change.</span></span> <span data-ttu-id="6f081-154">在此範例中，您會在無意中使該修正「連同」  先前正在為特定發行日期保留的變更一起發佈。</span><span class="sxs-lookup"><span data-stu-id="6f081-154">In this example, you inadvertently publish both the fix *and* the changes that you were holding for release on a specific date.</span></span>

<span data-ttu-id="6f081-155">現在，讓我們在本機存放庫中建立新的工作分支，以擷取您所建議的變更。</span><span class="sxs-lookup"><span data-stu-id="6f081-155">Now let's create a new working branch in your local repository, to capture your proposed changes.</span></span> <span data-ttu-id="6f081-156">如果您已設定 Git Bash (請參閱[安裝內容撰寫工具](get-started-setup-tools.md))，則您可以建立新的分支，並使用下列命令，從您已複製的存放庫內將該分支「簽出」：</span><span class="sxs-lookup"><span data-stu-id="6f081-156">If you've setup Git Bash (see [Install content authoring tools](get-started-setup-tools.md)), you can create a new branch and "checkout" that branch with one command from within your cloned repository:</span></span>

````
git checkout -b "branchname"
````

<span data-ttu-id="6f081-157">每個 Git 用戶端都不同，因此請參閱適您慣用用戶端的說明。</span><span class="sxs-lookup"><span data-stu-id="6f081-157">Each git client is different, so consult the help for your preferred client.</span></span> <span data-ttu-id="6f081-158">在 [GitHub 流程](https://guides.github.com/introduction/flow/)上的 GitHub 指南中有程序的概觀。</span><span class="sxs-lookup"><span data-stu-id="6f081-158">You can see an overview of the process in the GitHub Guide on [GitHub flow](https://guides.github.com/introduction/flow/).</span></span>

## <a name="making-your-changes"></a><span data-ttu-id="6f081-159">進行變更</span><span class="sxs-lookup"><span data-stu-id="6f081-159">Making your changes</span></span>

<span data-ttu-id="6f081-160">您已經有 Microsoft 存放庫的複本 (「複製的存放庫」)，且已經建立分支，現在您可以隨意使用任何文字或 Markdown 編輯器 (如[安裝內容撰寫工具](get-started-setup-tools.md)頁面上所述)，進行您認為對社群有所幫助的任何變更。</span><span class="sxs-lookup"><span data-stu-id="6f081-160">Now that you have a copy ("clone") of the Microsoft repository and you've created a branch, you're now free to make whatever changes you think would benefit the community using any text or Markdown editor, as outlined on the [Install content authoring tools](get-started-setup-tools.md) page.</span></span>  <span data-ttu-id="6f081-161">您可以在本機儲存變更，在完成變更之前都無需將其提交至 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="6f081-161">You can save your changes locally without needing to submit them to Microsoft until you're ready.</span></span>

## <a name="saving-changes-to-your-repository"></a><span data-ttu-id="6f081-162">儲存變更至您的存放庫</span><span class="sxs-lookup"><span data-stu-id="6f081-162">Saving changes to your repository</span></span>

<span data-ttu-id="6f081-163">將變更傳送給作者之前，您必須先將其儲存至 Github 存放庫。</span><span class="sxs-lookup"><span data-stu-id="6f081-163">Before sending your changes to the author, you must first save them to your Github repository.</span></span>  <span data-ttu-id="6f081-164">同樣地，雖然所有工具都不相同，但如果您使用 Git Bash 命令列，只需要幾個簡單的步驟就可以完成這項作業。</span><span class="sxs-lookup"><span data-stu-id="6f081-164">Again, while all tools are different, if you're using the Git Bash command line, this can be done in just a few easy steps.</span></span>

<span data-ttu-id="6f081-165">首先，您需要在存放庫中「暫存」  所有要認可的變更。</span><span class="sxs-lookup"><span data-stu-id="6f081-165">First, from within the repository, you need to _stage_ all of your changes to be commmited.</span></span>  <span data-ttu-id="6f081-166">您可以執行下列命令來完成此動作：</span><span class="sxs-lookup"><span data-stu-id="6f081-166">This can be done by executing:</span></span>

````
git add --all
````

<span data-ttu-id="6f081-167">接下來，您需要將已儲存的變更認可至本機存放庫。</span><span class="sxs-lookup"><span data-stu-id="6f081-167">Next, you need to commit your saved changes to your local repository.</span></span>  <span data-ttu-id="6f081-168">您可以執行下列命令以在 Git Bash 中完成此動作：</span><span class="sxs-lookup"><span data-stu-id="6f081-168">This can be done in Git Bash by running:</span></span>

````
git commit -m "Short Description of Changes Made"
````

<span data-ttu-id="6f081-169">最後，由於您是在本機電腦上建立此分支，因此需要為 GitHub.com 帳戶中的分支同步更新資訊。</span><span class="sxs-lookup"><span data-stu-id="6f081-169">Finally, since you created this branch on your local computer, you need to let the fork in your GitHub.com account know about it.</span></span>  <span data-ttu-id="6f081-170">如果您使用 Git Bash，則可執行下列命令來完成此動作：</span><span class="sxs-lookup"><span data-stu-id="6f081-170">If you're using Git Bash, this can be done by running:</span></span>

````
git push --set-upstream origin <branchname>
````

<span data-ttu-id="6f081-171">大功告成！</span><span class="sxs-lookup"><span data-stu-id="6f081-171">You've done it!</span></span>  <span data-ttu-id="6f081-172">您的程式碼現在已經在 GitHub 存放庫中，並可供建立提取要求。</span><span class="sxs-lookup"><span data-stu-id="6f081-172">Your code is now up in your GitHub repository and ready for you to create a pull request.</span></span>  

>[!TIP]
> <span data-ttu-id="6f081-173">雖然您的變更會在推送時顯示於您個人 GitHub 帳戶中，但您並不需要立即提交提取要求。</span><span class="sxs-lookup"><span data-stu-id="6f081-173">Even though your changes become visible in your personal GitHub account when you push them, there is no rule that you need to submit a pull request immediately.</span></span>  <span data-ttu-id="6f081-174">如果您想要暫停並稍後再回來進行其他調整也沒關係！</span><span class="sxs-lookup"><span data-stu-id="6f081-174">If you want to come stop and return at a later time to make additional tweaks, that's OK!</span></span>

<span data-ttu-id="6f081-175">需要修正您已經提交的東西嗎？</span><span class="sxs-lookup"><span data-stu-id="6f081-175">Need to fix something you submitted?</span></span>  <span data-ttu-id="6f081-176">沒問題！</span><span class="sxs-lookup"><span data-stu-id="6f081-176">No problem!</span></span>  <span data-ttu-id="6f081-177">只要在相同分支中進行變更，然後再次認可並推送即可 (不需要在相同分支的後續推送上設定上游伺服器)。</span><span class="sxs-lookup"><span data-stu-id="6f081-177">Just make your changes in the same branch and then commit and push again (no need to set the upstream server on subsequent pushes of the same branch).</span></span>

<span data-ttu-id="6f081-178">還需要進行更多其他項目的變更嗎？</span><span class="sxs-lookup"><span data-stu-id="6f081-178">Got more changes you need to make unrelated to this one?</span></span>  <span data-ttu-id="6f081-179">切換回主分支，並簽出另一個全新的分支，使用 Git Bash 輕鬆完成此動作：</span><span class="sxs-lookup"><span data-stu-id="6f081-179">Switch back to the master branch and checkout another fresh branch,  Using Git Bash, this is as easy as:</span></span>

````
git checkout master
git checkout -b "branchname"
````

<span data-ttu-id="6f081-180">現在已經回到新的分支，您又朝成為主要參與者邁進了一大步。</span><span class="sxs-lookup"><span data-stu-id="6f081-180">You're now back in a new branch and you're well on your way to being a master contributer.</span></span>

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## <a name="next-steps"></a><span data-ttu-id="6f081-181">後續步驟</span><span class="sxs-lookup"><span data-stu-id="6f081-181">Next steps</span></span>

<span data-ttu-id="6f081-182">大功告成！</span><span class="sxs-lookup"><span data-stu-id="6f081-182">That's it!</span></span> <span data-ttu-id="6f081-183">您已對 docs.microsoft.com 內容做出貢獻！</span><span class="sxs-lookup"><span data-stu-id="6f081-183">You've made a contribution to docs.microsoft.com content!</span></span>

- <span data-ttu-id="6f081-184">若要深入了解 Markdown 和 Markdown 延伸模組語法等主題，請繼續閱讀[撰寫基本資訊](how-to-write-use-markdown.md)一文。</span><span class="sxs-lookup"><span data-stu-id="6f081-184">To learn more about topics such as Markdown and Markdown extensions syntax, continue to the [Writing essentials](how-to-write-use-markdown.md) article.</span></span>
