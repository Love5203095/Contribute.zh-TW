---
title: .NET 文件提取要求檢閱程序
description: .NET 文件沒有啟用 PR Merger Webhook。 本文說明這些存放庫的 PR 程序
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 06/24/2020
ms.openlocfilehash: b2c0cbb0ed72948ba49a7456e16df5659057f5e6
ms.sourcegitcommit: 56505b3f7e670f6387d2c919f0326e9f4c571c8a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/31/2020
ms.locfileid: "89201119"
---
# <a name="pull-request-review-process-for-the-net-docs-repositories"></a><span data-ttu-id="cbdde-104">.NET 文件存放庫的提取要求檢閱程序</span><span class="sxs-lookup"><span data-stu-id="cbdde-104">Pull request review process for the .NET docs repositories</span></span>

<span data-ttu-id="cbdde-105">某些存放庫 (包括 .NET 存放庫) 啟用「PR 合併」Webhook，這種 Webhook 會自動合併較小的 PR。</span><span class="sxs-lookup"><span data-stu-id="cbdde-105">Some repositories, including the .NET repositories, don't have the "PR Merger" web hook enabled, which automatically merges minor PRs.</span></span> <span data-ttu-id="cbdde-106">本文說明針對那些存放庫的 PR 檢閱程序。</span><span class="sxs-lookup"><span data-stu-id="cbdde-106">This article describes the PR review process for those repositories.</span></span> <span data-ttu-id="cbdde-107">PR 檢閱程序是基於這些目標而設計：</span><span class="sxs-lookup"><span data-stu-id="cbdde-107">The PR review process was designed with these goals:</span></span>

- <span data-ttu-id="cbdde-108">發佈來自我們小組、產品小組成員及社群成員的高品質內容。</span><span class="sxs-lookup"><span data-stu-id="cbdde-108">Publish high-quality content from our team, product team members, and community members.</span></span>
- <span data-ttu-id="cbdde-109">以一致的方式為作者提供可採取動作的即時意見反應。</span><span class="sxs-lookup"><span data-stu-id="cbdde-109">Provide timely, actionable feedback to authors in a consistent manner.</span></span>
- <span data-ttu-id="cbdde-110">促進作者及檢閱者之間的討論。</span><span class="sxs-lookup"><span data-stu-id="cbdde-110">Facilitate discussion between authors and reviewers.</span></span>

<span data-ttu-id="cbdde-111">隨著小組持續創新且平台持續成熟，這些程序將會繼續進化。</span><span class="sxs-lookup"><span data-stu-id="cbdde-111">The processes continue to evolve as teams innovate and as the platform matures.</span></span>

## <a name="reviewers"></a><span data-ttu-id="cbdde-112">檢閱者</span><span class="sxs-lookup"><span data-stu-id="cbdde-112">Reviewers</span></span>

<span data-ttu-id="cbdde-113">其中一個內容小組成員會檢閱每一個 PR。</span><span class="sxs-lookup"><span data-stu-id="cbdde-113">One of the content team members reviews every PR.</span></span> <span data-ttu-id="cbdde-114">內容小組成員可以要求特定產品小組成員進行檢閱，以確認技術上的正確性。</span><span class="sxs-lookup"><span data-stu-id="cbdde-114">Content team members may request a review from the specific product team members to verify technical accuracy.</span></span> <span data-ttu-id="cbdde-115">內容小組會使用 GitHub 的程式碼擁有權功能來自動要求內容小組成員進行檢閱。</span><span class="sxs-lookup"><span data-stu-id="cbdde-115">The content team uses GitHub's Code Ownership feature to automatically request reviews from content team members.</span></span> <span data-ttu-id="cbdde-116">作為此程序的一部分，檢閱者可以標記其他小組成員以檢閱內部 PR。</span><span class="sxs-lookup"><span data-stu-id="cbdde-116">As part of this process, a reviewer may tag other team members to review internal PRs.</span></span> <span data-ttu-id="cbdde-117">小組成員會在相同的佇列中看見來自小組成員和社群成員的所要求檢閱。</span><span class="sxs-lookup"><span data-stu-id="cbdde-117">Team members see requested reviews from team members and community members in the same queue.</span></span>

<span data-ttu-id="cbdde-118">社群成員也可以檢閱 PR 並提供意見反應。</span><span class="sxs-lookup"><span data-stu-id="cbdde-118">Community members can review PRs and provide feedback as well.</span></span> <span data-ttu-id="cbdde-119">不過，在該 PR 被合併之前，必須至少由一個核心內容小組的成員進行核准。</span><span class="sxs-lookup"><span data-stu-id="cbdde-119">However, at least one member of the core content team must approve any PR before it is merged.</span></span>

## <a name="review-process"></a><span data-ttu-id="cbdde-120">檢閱程序</span><span class="sxs-lookup"><span data-stu-id="cbdde-120">Review process</span></span>

<span data-ttu-id="cbdde-121">會根據 PR 檢閱下列三個路徑中的其中一個：</span><span class="sxs-lookup"><span data-stu-id="cbdde-121">Reviews follow one of the three paths based on the PR:</span></span>

- <span data-ttu-id="cbdde-122">**小型 PR**：小型 PR 為單一錯誤修正：錯字、無效連結、小型程式碼變更或類似的變更。</span><span class="sxs-lookup"><span data-stu-id="cbdde-122">**Small PRs** - Small PRs are single bug fix: typos, broken links, small code changes, or similar changes.</span></span>
- <span data-ttu-id="cbdde-123">**主要貢獻**：主要貢獻為針對現有文章或新文章的大量編輯，或是針對許多文章進行編輯。</span><span class="sxs-lookup"><span data-stu-id="cbdde-123">**Major contributions** - Major contributions are significant edits to an existing article, new articles, or edits to a number of articles.</span></span>
- <span data-ttu-id="cbdde-124">**正在進行的工作** - 作者可透過開啟「草稿」提取要求，以建立標記為尚未準備好進行檢閱的 PR。</span><span class="sxs-lookup"><span data-stu-id="cbdde-124">**Work in progress** - Authors can can create a PR that is marked as not ready for review yet by opening a *draft* pull request.</span></span>

<span data-ttu-id="cbdde-125">「參與者授權合約」(CLA) 機器人所使用的處理方式是一個可區別「小型」與「大型」貢獻的良好指導方針。</span><span class="sxs-lookup"><span data-stu-id="cbdde-125">The processing used by the Contributor License Agreement (CLA) bot is a good guideline for the distinction between "small" and "large" contributions.</span></span> <span data-ttu-id="cbdde-126">不需要簽署 CLA 的 PR，通常是「小型」的。</span><span class="sxs-lookup"><span data-stu-id="cbdde-126">PRs that do not require the CLA to be signed are likely "small."</span></span> <span data-ttu-id="cbdde-127">需要 CLA 的 PR 則通常是「大型」的。</span><span class="sxs-lookup"><span data-stu-id="cbdde-127">PRs that do require the CLA are likely "large."</span></span>

### <a name="small-prs"></a><span data-ttu-id="cbdde-128">小型 PR</span><span class="sxs-lookup"><span data-stu-id="cbdde-128">Small PRs</span></span>

<span data-ttu-id="cbdde-129">小型 PR 中的變更會針對正確性進行檢閱，並使用檢閱網站上的組建進行檢查。</span><span class="sxs-lookup"><span data-stu-id="cbdde-129">The changes in small PRs are reviewed for accuracy and checked using the build on the review site.</span></span> <span data-ttu-id="cbdde-130">由於這些 PR 較小，它們並不會觸發針對整篇文章的檢閱。</span><span class="sxs-lookup"><span data-stu-id="cbdde-130">Because they are small, these PRs do not trigger a review of the entire article.</span></span> 

<span data-ttu-id="cbdde-131">檢閱者可能會注意到其他能改善文章的小型變更。</span><span class="sxs-lookup"><span data-stu-id="cbdde-131">Reviewers may notice other small changes that would improve an article.</span></span> <span data-ttu-id="cbdde-132">若那些變更的幅度也相當小，請以檢閱註解的方式建議它們。</span><span class="sxs-lookup"><span data-stu-id="cbdde-132">If those changes are also small, suggest them as review comments.</span></span> <span data-ttu-id="cbdde-133">若建議的變更會觸發較大規模的檢閱，請提出問題並於未來解決它們。</span><span class="sxs-lookup"><span data-stu-id="cbdde-133">If the suggested changes would trigger a larger review, open an issue and address those later.</span></span> 

### <a name="larger-changes"></a><span data-ttu-id="cbdde-134">大型變更</span><span class="sxs-lookup"><span data-stu-id="cbdde-134">Larger changes</span></span>

<span data-ttu-id="cbdde-135">大型 PR 需要進行更徹底的檢閱。</span><span class="sxs-lookup"><span data-stu-id="cbdde-135">Larger PRs undergo a more thorough review.</span></span> <span data-ttu-id="cbdde-136">會檢查下列所有項目：</span><span class="sxs-lookup"><span data-stu-id="cbdde-136">The following are all checked:</span></span>

- <span data-ttu-id="cbdde-137">範例程式碼必須包含在 PR、來源，以及可下載的 zip 檔案中。</span><span class="sxs-lookup"><span data-stu-id="cbdde-137">Sample code must be included in the PR, in source and as a downloadable zip file.</span></span>
- <span data-ttu-id="cbdde-138">範例程式碼必須編譯並正常運作。</span><span class="sxs-lookup"><span data-stu-id="cbdde-138">Sample code compiles and runs correctly.</span></span>
- <span data-ttu-id="cbdde-139">文章必須清楚地為讀者描述目標，並達成那些目標。</span><span class="sxs-lookup"><span data-stu-id="cbdde-139">The article clearly describes the goals for the reader, and those goals are met.</span></span>
- <span data-ttu-id="cbdde-140">文章符合[樣式和文法指導方針](dotnet-style-guide.md)，並且依循我們的[語態和語調原則](dotnet-voice-tone.md)。</span><span class="sxs-lookup"><span data-stu-id="cbdde-140">The article meets [style and grammar guidelines](dotnet-style-guide.md) and follows our [voice and tone principles](dotnet-voice-tone.md).</span></span>
- <span data-ttu-id="cbdde-141">所有連結都必須能正確解析。</span><span class="sxs-lookup"><span data-stu-id="cbdde-141">All links should resolve correctly.</span></span>

<span data-ttu-id="cbdde-142">內容小組成員將會檢閱 PR，並搭配註解提交檢閱。</span><span class="sxs-lookup"><span data-stu-id="cbdde-142">Content team members will review the PR and submit the review with comments.</span></span> <span data-ttu-id="cbdde-143">若僅要求次要變更，小組成員可以透過意見反應「核准」該 PR。</span><span class="sxs-lookup"><span data-stu-id="cbdde-143">If only minor changes are requested, team members may "approve" the PR with the feedback.</span></span> <span data-ttu-id="cbdde-144">作者可以接著處理意見反應內容並合併 PR。</span><span class="sxs-lookup"><span data-stu-id="cbdde-144">The author can then address the feedback and merge the PR.</span></span> <span data-ttu-id="cbdde-145">大部分的檢閱都會要求變更，而當那些變更都被執行之後，檢閱者便會再次檢閱。</span><span class="sxs-lookup"><span data-stu-id="cbdde-145">Most reviews will request changes and when those changes are made, the reviewer will review again.</span></span>

<span data-ttu-id="cbdde-146">若編輯需要技術性檢閱，內容小組檢閱者將會要求適當的產品小組成員進行檢閱。</span><span class="sxs-lookup"><span data-stu-id="cbdde-146">If the edits require a technical review, the content team reviewer will request a review from the appropriate product team member.</span></span>

### <a name="review-draft-pull-requests"></a><span data-ttu-id="cbdde-147">檢閱草稿提取要求</span><span class="sxs-lookup"><span data-stu-id="cbdde-147">Review draft pull requests</span></span>

<span data-ttu-id="cbdde-148">您可以會想要在流程初期便取得意見反應。</span><span class="sxs-lookup"><span data-stu-id="cbdde-148">You may want feedback earlier in the process.</span></span> <span data-ttu-id="cbdde-149">開啟草稿 PR，並新增要求早期檢閱的註解。</span><span class="sxs-lookup"><span data-stu-id="cbdde-149">Open a draft PR and add a comment that requests an early review.</span></span> <span data-ttu-id="cbdde-150">這些早期檢閱的重點在於文章的結構：大綱、整體內容及範例。</span><span class="sxs-lookup"><span data-stu-id="cbdde-150">These early reviews focus on the structure of the article: the outline, the overall content, and the samples.</span></span> <span data-ttu-id="cbdde-151">這些檢閱並不會針對文法或連結進行徹底的檢查。</span><span class="sxs-lookup"><span data-stu-id="cbdde-151">These reviews do not include a thorough check for grammar and correct links.</span></span>

## <a name="explain-suggestions"></a><span data-ttu-id="cbdde-152">說明建議</span><span class="sxs-lookup"><span data-stu-id="cbdde-152">Explain suggestions</span></span>

<span data-ttu-id="cbdde-153">GitHub 可讓您在類型為 `suggestion` 的三接續符號區塊中輸入註解，這些會顯示為差異並可透過按一下按鈕來合併。</span><span class="sxs-lookup"><span data-stu-id="cbdde-153">GitHub lets you enter comments in triple-back-tick blocks of type `suggestion` that are displayed as a diff and can be merged by clicking a button.</span></span> <span data-ttu-id="cbdde-154">在較短的行上，GitHub 能有效地反白顯示變更。</span><span class="sxs-lookup"><span data-stu-id="cbdde-154">On short lines, GitHub does a good job of highlighting the changes.</span></span> <span data-ttu-id="cbdde-155">在較長的行 (例如一行文字中的長段落) 上，GitHub 不會反白顯示變更。</span><span class="sxs-lookup"><span data-stu-id="cbdde-155">On longer lines, such as a long paragraph in one line of text, GitHub doesn't highlight the changes.</span></span> <span data-ttu-id="cbdde-156">針對較長的行輸入建議時，請注意您的變更是否清楚地反白顯示。</span><span class="sxs-lookup"><span data-stu-id="cbdde-156">When entering a suggestion for a long line, notice whether your changes are clearly highlighted.</span></span> <span data-ttu-id="cbdde-157">若變更未反白顯示，請納入建議區塊外的註解並說明變更為何。</span><span class="sxs-lookup"><span data-stu-id="cbdde-157">If the changes aren't highlighted, include comments outside the suggestion block explaining what you changed.</span></span> <span data-ttu-id="cbdde-158">如果沒有說明，後續的檢閱者或 PR 作者通常會花很多時間來找出變更的內容。</span><span class="sxs-lookup"><span data-stu-id="cbdde-158">Without an explanation it's often time-consuming for subsequent reviewers or the PR author to figure out what the changes are.</span></span>

## <a name="respond-to-reviews"></a><span data-ttu-id="cbdde-159">回應檢閱</span><span class="sxs-lookup"><span data-stu-id="cbdde-159">Respond to reviews</span></span>

<span data-ttu-id="cbdde-160">作者可以更新 PR 以回應註解，並在每個已處理的註解上標記 "+1" 反應，以指出該註解已處理完畢。</span><span class="sxs-lookup"><span data-stu-id="cbdde-160">The author updates the PR to respond to comments and marks each addressed comment with the "+1" reaction to indicate it was addressed.</span></span> <span data-ttu-id="cbdde-161">若作者不同意註解，或是以不同的方式處理該註解，作者便會新增註解以解釋其變更。</span><span class="sxs-lookup"><span data-stu-id="cbdde-161">If the author disagrees with the comment, or addresses the comment in a different PR, the author adds a comment explaining their change.</span></span>

<span data-ttu-id="cbdde-162">作者會在註解中對原始檢閱者進行 @-mentions 以要求新的檢閱。</span><span class="sxs-lookup"><span data-stu-id="cbdde-162">The author @-mentions the original reviewer in a comment to request a new review.</span></span> 

## <a name="response-time-expectations"></a><span data-ttu-id="cbdde-163">預期回應時間</span><span class="sxs-lookup"><span data-stu-id="cbdde-163">Response time expectations</span></span>

<span data-ttu-id="cbdde-164">內容小組成員通常會在兩個工作日以內對新的 PR 進行檢閱。</span><span class="sxs-lookup"><span data-stu-id="cbdde-164">Content team members will typically review new PRs in under two business days.</span></span> <span data-ttu-id="cbdde-165">若檢閱時間較長，其中一個小組成員將會加入註解以確認該 PR 並設立預期時程。</span><span class="sxs-lookup"><span data-stu-id="cbdde-165">If it takes longer to review, one of the team members will add a comment to acknowledge the PR and set expectations.</span></span>

<span data-ttu-id="cbdde-166">在檢閱者提交檢閱之後，作者應該嘗試在一週以內對註解做出回應。</span><span class="sxs-lookup"><span data-stu-id="cbdde-166">Once a review has been submitted, authors should try to respond to comments in a week or less.</span></span> <span data-ttu-id="cbdde-167">志工可能會因為自己工作或生活上的其他承諾，而無法達成這些預期的時程。</span><span class="sxs-lookup"><span data-stu-id="cbdde-167">Volunteers may not be able to meet these expectations because of other commitments.</span></span> <span data-ttu-id="cbdde-168">在那些情況下，小組成員會詢問社群作者是否能更新該 PR。</span><span class="sxs-lookup"><span data-stu-id="cbdde-168">In those cases, team members ask if the community author will update the PR.</span></span> <span data-ttu-id="cbdde-169">若不行，小組成員將會代替他們更新並合併該 PR。</span><span class="sxs-lookup"><span data-stu-id="cbdde-169">If not, the team member updates and merges the PR for them.</span></span>
