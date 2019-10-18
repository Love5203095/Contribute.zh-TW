---
title: PowerShell 文件存放庫的貢獻流程
description: 本文提供參與 PowerShell 文件存放庫的簡介。 您將了解所使用的存放庫、組織內容的程序，以及管理程式碼範例和其他資產的原則。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/07/2019
ms.openlocfilehash: 9802942dccbfad2cb860739ffba4b30d2b0af0c9
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290188"
---
# <a name="process-for-contributing-to-powershell-docs"></a><span data-ttu-id="9f1aa-104">參與 PowerShell 文件的流程</span><span class="sxs-lookup"><span data-stu-id="9f1aa-104">Process for contributing to PowerShell docs</span></span>

<span data-ttu-id="9f1aa-105">感謝社群對文件的參與。下列清單顯示參與 PowerShell 文件時應該注意的一些指導規則：</span><span class="sxs-lookup"><span data-stu-id="9f1aa-105">We appreciate community contributions to docs. The following list shows some guiding rules that you should keep in mind when you're contributing to the PowerShell documentation:</span></span>

- <span data-ttu-id="9f1aa-106">**請勿**出其不意地提交大量提取要求。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-106">**DON'T** surprise us with large pull requests.</span></span> <span data-ttu-id="9f1aa-107">相反地，請提出一個問題並開始討論，先讓我們就大方向取得共識再投入大量時間。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-107">Instead, file an issue and start a discussion so we can agree on a direction before you invest a large amount of time.</span></span>
- <span data-ttu-id="9f1aa-108">**請**遵循這些指示，以及[程式碼](powershell-style-code.md)和[參考](powershell-style-reference.md)的樣式指南。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-108">**DO** follow these instructions and the [code](powershell-style-code.md) and [reference](powershell-style-reference.md) style guides..</span></span>
- <span data-ttu-id="9f1aa-109">**務必**使用[範本](powershell-style-basic-markdown.md)檔案作為您工作的起點。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-109">**DO** use the [template](powershell-style-basic-markdown.md) file as the starting point of your work.</span></span>
- <span data-ttu-id="9f1aa-110">**務必**先在您的分支上建立個別分支，再參與文章。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-110">**DO** create a separate branch on your fork before working on the articles.</span></span>
- <span data-ttu-id="9f1aa-111">**務必**遵循 [GitHub 流程的工作流程](../how-to-write-workflows-major.md)。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-111">**DO** follow the [GitHub Flow workflow](../how-to-write-workflows-major.md).</span></span>
- <span data-ttu-id="9f1aa-112">**務必**經常針對您的參與撰寫部落格文章和推文 (或透過其他方式)！</span><span class="sxs-lookup"><span data-stu-id="9f1aa-112">**DO** blog and tweet (or whatever) about your contributions, frequently!</span></span>

<span data-ttu-id="9f1aa-113">遵循這些方針有助於確保您我都有更佳的體驗。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-113">Following these guidelines ensures a better experience for you and for us.</span></span>

## <a name="make-a-contribution-to-powershell-docs"></a><span data-ttu-id="9f1aa-114">參與 PowerShell 文件</span><span class="sxs-lookup"><span data-stu-id="9f1aa-114">Make a contribution to PowerShell docs</span></span>

<span data-ttu-id="9f1aa-115">您可以選擇現有的[問題](https://github.com/MicrosoftDocs/PowerShell-Docs/issues/new/choose)。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-115">You can choose from existing [issues](https://github.com/MicrosoftDocs/PowerShell-Docs/issues/new/choose).</span></span>
<span data-ttu-id="9f1aa-116">根據您的興趣和參與程度，您可以投入下列類別：</span><span class="sxs-lookup"><span data-stu-id="9f1aa-116">Depending on your interests and level of commitment, the efforts fall into the following categories:</span></span>

- <span data-ttu-id="9f1aa-117">**小型變更**</span><span class="sxs-lookup"><span data-stu-id="9f1aa-117">**Small changes**.</span></span> <span data-ttu-id="9f1aa-118">若變更不大，請參閱參與者指南[首頁](../index.md#quick-edits-to-existing-documents)上有關在 GitHub 中編輯的指示。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-118">For small changes, see the instructions on editing in GitHub on the [home page](../index.md#quick-edits-to-existing-documents) of the contributor guide.</span></span> <span data-ttu-id="9f1aa-119">小型變更包括：</span><span class="sxs-lookup"><span data-stu-id="9f1aa-119">Small changes include:</span></span>

  - <span data-ttu-id="9f1aa-120">修正錯字和拼寫錯誤</span><span class="sxs-lookup"><span data-stu-id="9f1aa-120">Fixing typos and spelling errors</span></span>
  - <span data-ttu-id="9f1aa-121">改善文法或格式</span><span class="sxs-lookup"><span data-stu-id="9f1aa-121">Improving grammar or formatting</span></span>
  - <span data-ttu-id="9f1aa-122">次要技術或實際編輯</span><span class="sxs-lookup"><span data-stu-id="9f1aa-122">Minor technical or factual edits</span></span>

- <span data-ttu-id="9f1aa-123">**維護**。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-123">**Maintenance**.</span></span> <span data-ttu-id="9f1aa-124">此類別包含相當簡單的參與，例如修正中斷或不正確的連結、新增缺少的程式碼範例，或解決限制的內容問題。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-124">This category includes fairly simple contributions, such as fixing broken or incorrect links, adding missing code examples, or addressing limited content issues.</span></span> <span data-ttu-id="9f1aa-125">在某些情況下，這些問題可能涉及大量檔案。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-125">In some cases, these issues may concern large numbers of files.</span></span> <span data-ttu-id="9f1aa-126">在此情況下，您應該讓我們知道您想要參與的內容，再開始進行。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-126">In that case, you should let us know what you'd like to work on before you begin.</span></span> <span data-ttu-id="9f1aa-127">在問題上新增註解，告訴我們您正在參與。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-127">Add a comment on the issue to tell us that you are working on it.</span></span>

- <span data-ttu-id="9f1aa-128">**內容更新**。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-128">**Content updates**.</span></span> <span data-ttu-id="9f1aa-129">由於文件集很龐大，因此內容很容易就會變得過期而需要修訂。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-129">Given the enormity of the doc set, content easily becomes outdated and requires revision.</span></span> <span data-ttu-id="9f1aa-130">此外，基於各種不同的原因，某些內容已重複或甚至再三出現。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-130">In addition, for a variety of reason, some content has been duplicated or even triplicated.</span></span> <span data-ttu-id="9f1aa-131">更新內容時需要確定個別主題是最新的，或修訂功能範圍中的內容，以排除重複出現的情況，並確保以更小的文件集來保留所有唯一內容。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-131">Updating content involves making sure that individual topics are current or revising content in a feature area to eliminate duplication and ensure that all unique content is preserved in the smaller documentation set.</span></span>

- <span data-ttu-id="9f1aa-132">**撰寫新內容**。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-132">**New content authoring**.</span></span> <span data-ttu-id="9f1aa-133">如果您對撰寫自己的主題感興趣，則這些問題會列出我們確定要新增至文件集的主題。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-133">If you're interested in authoring your own topic, these issues list topics that we know we'd like to add to our doc set.</span></span> <span data-ttu-id="9f1aa-134">不過在您開始撰寫某個主題之前，請讓我們知道。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-134">Let us know before you begin working on a topic, though.</span></span> <span data-ttu-id="9f1aa-135">如果您對撰寫這裡未列出的主題感興趣，請開啟一個問題。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-135">If you're interested in writing a topic that isn't listed here, open an issue.</span></span>

<span data-ttu-id="9f1aa-136">一旦您選擇了要參與的工作，請遵循[入門](../get-started-setup-github.md)指南以建立 GitHub 帳戶並設定您的環境。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-136">Once you've picked a task to work on, follow the [get started](../get-started-setup-github.md) guide to create a GitHub account and setup your environment.</span></span>

### <a name="making-large-changes"></a><span data-ttu-id="9f1aa-137">進行大量變更</span><span class="sxs-lookup"><span data-stu-id="9f1aa-137">Making large changes</span></span>

<span data-ttu-id="9f1aa-138">**步驟 1：** 如果您對撰寫新內容或全面修訂現有內容感興趣，請開啟描述您要執行作業的問題。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-138">**Step 1:** If you're interested in writing new content or in thoroughly revising existing content, open an issue describing what you want to do.</span></span>

<span data-ttu-id="9f1aa-139">**步驟 2：** 派生 `MicrosoftDocs/PowerShell-Docs` 存放庫，並為您的變更建立工作分支。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-139">**Step 2:** Fork the `MicrosoftDocs/PowerShell-Docs` repository and create a working branch for your changes.</span></span>

<span data-ttu-id="9f1aa-140">**步驟 3：** 在此新分支上進行變更。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-140">**Step 3:** Make the changes in this new branch.</span></span>

<span data-ttu-id="9f1aa-141">若這是新主題，請使用[樣式指南](powershell-style-basic-markdown.md)中的範本作為起點。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-141">If it's a new topic, use the template in the [style guide](powershell-style-basic-markdown.md) as your starting point.</span></span> <span data-ttu-id="9f1aa-142">樣式指南包含撰寫方針，並會說明每篇文章所需的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-142">The style guide contains the writing guidelines and explains the metadata required for each article.</span></span>

<span data-ttu-id="9f1aa-143">請巡覽至步驟 1 中針對您文章所決定 TOC 位置的相對應資料夾。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-143">Navigate to the folder that corresponds to the TOC location determined for your article in step 1.</span></span>
<span data-ttu-id="9f1aa-144">該資料夾包含該區段中所有文章的 Markdown 檔案。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-144">That folder contains the Markdown files for all articles in that section.</span></span> <span data-ttu-id="9f1aa-145">如有需要，請建立新的資料夾來放置您的內容檔案。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-145">If necessary, create a new folder to place the files for your content.</span></span> <span data-ttu-id="9f1aa-146">該區段的主要文章名為 *index.md*。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-146">The main article for that section is called *index.md*.</span></span>
<span data-ttu-id="9f1aa-147">針對影像和其他靜態資源，請在包含您文章的資料夾中建立名為 **media** 的子資料夾 (如果尚未存在)。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-147">For images and other static resources, create a subfolder called **media** inside the folder that contains your article, if it doesn't already exist.</span></span> <span data-ttu-id="9f1aa-148">在 **media** 資料夾中，建立具有文章名稱的子資料夾 (索引檔除外)。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-148">Inside the **media** folder, create a subfolder with the article name (except for the index file).</span></span>

<span data-ttu-id="9f1aa-149">請務必遵循適當的 Markdown 語法。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-149">Be sure to follow the proper Markdown syntax.</span></span> <span data-ttu-id="9f1aa-150">如需詳細的指示和範例，請參閱[樣式指南](powershell-style-basic-markdown.md)。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-150">Please read the [style guide](powershell-style-basic-markdown.md) for detailed instructions and examples.</span></span>

<span data-ttu-id="9f1aa-151">**範例結構**</span><span class="sxs-lookup"><span data-stu-id="9f1aa-151">**Example structure**</span></span>

```
reference
  /docs-conceptual
    /learn
      /remoting
        managing-remote-sessions.md
        /images
          /managing-remote-sessions
            sesssion-list.png
```

<span data-ttu-id="9f1aa-152">**步驟 4：** 從您的工作分支提交提取要求 (PR) 至 *staging* 分支。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-152">**Step 4:** Submit a Pull Request (PR) from your working branch to the *staging* branch.</span></span>

<span data-ttu-id="9f1aa-153">一般而言，PR 應一次解決一個問題。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-153">Normally, a PR should address one issue at a time.</span></span> <span data-ttu-id="9f1aa-154">PR 可修改一或多個檔案。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-154">The PR can modify one or multiple files.</span></span> <span data-ttu-id="9f1aa-155">如果您要解決不同檔案的多個修正，最好使用個別 PR。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-155">If you're addressing multiple fixes on different files, separate PRs are preferred.</span></span>

<span data-ttu-id="9f1aa-156">如果您的 PR 會修正現有問題，請將 `Fixes #Issue_Number` 關鍵字新增至認可訊息或 PR 描述。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-156">If your PR fixes an existing issue, add the `Fixes #Issue_Number` keyword to the commit message or PR description.</span></span> <span data-ttu-id="9f1aa-157">如此一來，當 PR 合併之後，就會自動關閉問題。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-157">That way, the issue is automatically closed when the PR is merged.</span></span> <span data-ttu-id="9f1aa-158">如需詳細資訊，請參閱 [Closing issues via commit messages](https://help.github.com/articles/closing-issues-via-commit-messages/) (透過認可訊息關閉問題)。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-158">For more information, see [Closing issues via commit messages](https://help.github.com/articles/closing-issues-via-commit-messages/).</span></span>

<span data-ttu-id="9f1aa-159">PowerShell 小組會檢閱您的 PR，並讓您知道是否需要任何其他變更以通過核准。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-159">The PowerShell team reviews your PR and lets you know if there are any other changes necessary in order to approve it.</span></span>

<span data-ttu-id="9f1aa-160">**步驟 5：** 根據與小組的討論結果，對您的分支進行任何必要的更新。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-160">**Step 5:** Make any necessary updates to your branch as discussed with the team.</span></span>

<span data-ttu-id="9f1aa-161">PR 獲得核准之後，維護人員會將您的 PR 合併到 *staging* 分支。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-161">Once the PR is approved, the maintainers merge your PR into the *staging* branch.</span></span> <span data-ttu-id="9f1aa-162">我們會定期將 *staging* 分支中的所有提交推送到 *live* 分支。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-162">We periodically push all commits from *staging* branch into the *live* branch.</span></span> <span data-ttu-id="9f1aa-163">當您的貢獻上線後，您便可以在 [PowerShell 文件網站](https://docs.microsoft.com/PowerShell/)看見它。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-163">Once your contribution is live, you can see it in the [PowerShell docs site](https://docs.microsoft.com/PowerShell/).</span></span> <span data-ttu-id="9f1aa-164">通常，我們會在工作週的期間內發佈二到三次。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-164">Typically, we publish a two to three times during the work week.</span></span>

## <a name="contributor-license-agreement"></a><span data-ttu-id="9f1aa-165">參與者授權合約</span><span class="sxs-lookup"><span data-stu-id="9f1aa-165">Contributor license agreement</span></span>

<span data-ttu-id="9f1aa-166">您必須簽署[貢獻授權合約 (CLA)](https://cla.opensource.microsoft.com/MicrosoftDocs/PowerShell-Docs) 才能合併 PR。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-166">You must sign the [Contribution License Agreement (CLA)](https://cla.opensource.microsoft.com/MicrosoftDocs/PowerShell-Docs) before your PR is merged.</span></span> <span data-ttu-id="9f1aa-167">這是對文件進行貢獻時所要進行的一次性需求。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-167">This is a one-time requirement when contributing to our documentation.</span></span>

<span data-ttu-id="9f1aa-168">您不需要事先簽署合約。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-168">You don't have to sign the agreement up-front.</span></span> <span data-ttu-id="9f1aa-169">您可以如往常般複製、派生及提交 PR。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-169">You can clone, fork, and submit your PR as usual.</span></span>
<span data-ttu-id="9f1aa-170">當您的 PR 建立之後，會由 CLA Bot 進行分類。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-170">When your PR is created, it is classified by a CLA bot.</span></span> <span data-ttu-id="9f1aa-171">如果變更不大 (例如修正錯字)，則 PR 會標記為 `cla-not-required`。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-171">If the change is small (for example, you fixed a typo), then the PR is labeled with `cla-not-required`.</span></span> <span data-ttu-id="9f1aa-172">否則，它會分類為 `cla-required`。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-172">Otherwise, it's classified as `cla-required`.</span></span> <span data-ttu-id="9f1aa-173">一旦您簽署了 CLA，目前和所有未來提取要求都會標記為 `cla-signed`。</span><span class="sxs-lookup"><span data-stu-id="9f1aa-173">Once you signed the CLA, the current and all future pull requests are labeled as `cla-signed`.</span></span>
