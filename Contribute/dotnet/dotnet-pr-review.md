---
title: .NET 文件提取要求檢閱程序
description: .NET 文件沒有啟用 PR Merger Webhook。 本文說明這些存放庫的 PR 程序
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 01/04/2019
ms.openlocfilehash: 80877a93dc410454c939bcd5be5588861682ed11
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/04/2020
ms.locfileid: "80625112"
---
# <a name="pull-request-review-process-for-the-net-docs-repositories"></a><span data-ttu-id="14f11-104">.NET 文件存放庫的提取要求檢閱程序</span><span class="sxs-lookup"><span data-stu-id="14f11-104">Pull request review process for the .NET docs repositories</span></span>

<span data-ttu-id="14f11-105">許多存放庫都沒有啟用 PR Merger Webhook，此 Webhook 會自動合併次要的 PR。</span><span class="sxs-lookup"><span data-stu-id="14f11-105">Many repositories don't have PR Merger webhooks enabled, which automatically merges minor PRs.</span></span> <span data-ttu-id="14f11-106">本文說明針對那些存放庫的 PR 檢閱程序。</span><span class="sxs-lookup"><span data-stu-id="14f11-106">This article describes the PR review process for those repositories.</span></span> <span data-ttu-id="14f11-107">PR 檢閱程序是基於這些目標而設計：</span><span class="sxs-lookup"><span data-stu-id="14f11-107">The PR review process was designed with these goals:</span></span>

1. <span data-ttu-id="14f11-108">發佈來自我們小組、產品小組成員及社群成員的高品質內容。</span><span class="sxs-lookup"><span data-stu-id="14f11-108">Publish high-quality content from our team, product team members, and community members.</span></span>
1. <span data-ttu-id="14f11-109">以一致的方式為作者提供可採取動作的即時意見反應。</span><span class="sxs-lookup"><span data-stu-id="14f11-109">Provide timely, actionable feedback to authors in a consistent manner.</span></span>
1. <span data-ttu-id="14f11-110">促進作者及檢閱者之間的討論。</span><span class="sxs-lookup"><span data-stu-id="14f11-110">Facilitate discussion between authors and reviewers.</span></span>

<span data-ttu-id="14f11-111">隨著小組持續創新且平台持續成熟，這些程序將會繼續進化。</span><span class="sxs-lookup"><span data-stu-id="14f11-111">The processes continue to evolve as teams innovate, and as the platform matures.</span></span>

## <a name="reviewers"></a><span data-ttu-id="14f11-112">檢閱者</span><span class="sxs-lookup"><span data-stu-id="14f11-112">Reviewers</span></span>

<span data-ttu-id="14f11-113">其中一個內容小組成員會檢閱每一個 PR。</span><span class="sxs-lookup"><span data-stu-id="14f11-113">One of the content team members reviews every PR.</span></span> <span data-ttu-id="14f11-114">內容小組成員可以要求特定產品小組成員進行檢閱，以確認技術上的正確性。</span><span class="sxs-lookup"><span data-stu-id="14f11-114">Content team members may request a review from the specific product team members to verify technical accuracy.</span></span> <span data-ttu-id="14f11-115">內容小組會使用 GitHub 的程式碼擁有權功能來自動要求內容小組成員進行檢閱。</span><span class="sxs-lookup"><span data-stu-id="14f11-115">The content team uses GitHub's Code Ownership feature to automatically request reviews from content team members.</span></span> <span data-ttu-id="14f11-116">作為此程序的一部分，檢閱者可以標記其他小組成員以檢閱內部 PR。</span><span class="sxs-lookup"><span data-stu-id="14f11-116">As part of this process, a reviewer may tag other team members to review internal PRs.</span></span> <span data-ttu-id="14f11-117">小組成員會在相同的佇列中看見來自小組成員和社群成員的所要求檢閱。</span><span class="sxs-lookup"><span data-stu-id="14f11-117">Team members see requested reviews from team members and community members in the same queue.</span></span>

<span data-ttu-id="14f11-118">社群成員也可以檢閱 PR 並提供意見反應。</span><span class="sxs-lookup"><span data-stu-id="14f11-118">Community members can review PRs and provide feedback as well.</span></span> <span data-ttu-id="14f11-119">不過，在該 PR 被合併之前，必須至少由一個核心內容小組的成員進行核准。</span><span class="sxs-lookup"><span data-stu-id="14f11-119">However, at least one member of the core content team must approve any PR before it is merged.</span></span>

## <a name="review-process"></a><span data-ttu-id="14f11-120">檢閱程序</span><span class="sxs-lookup"><span data-stu-id="14f11-120">Review process</span></span>

<span data-ttu-id="14f11-121">會根據 PR 檢閱下列三個路徑中的其中一個：</span><span class="sxs-lookup"><span data-stu-id="14f11-121">Reviews follow one of the three paths based on the PR:</span></span>

- <span data-ttu-id="14f11-122">**小型 PR**：小型 PR 為單一錯誤修正：錯字、無效連結、小型程式碼變更或類似的變更。</span><span class="sxs-lookup"><span data-stu-id="14f11-122">**Small PRs** - Small PRs are single bug fix: typos, broken links, small code changes, or similar changes.</span></span>
- <span data-ttu-id="14f11-123">**主要貢獻**：主要貢獻為針對現有文章或新文章的大量編輯，或是針對許多文章進行編輯。</span><span class="sxs-lookup"><span data-stu-id="14f11-123">**Major contributions** - Major contributions are significant edits to an existing article, new articles, or edits to a number of articles.</span></span>
- <span data-ttu-id="14f11-124">**進行中的工作**：作者可以透過在標題中加上 "[WIP]" 標記來開啟 PR，以要求進行期間的檢閱。</span><span class="sxs-lookup"><span data-stu-id="14f11-124">**Work in progress** - Authors can request an in-progress review by opening a PR with the "[WIP]" tag in the title.</span></span> <span data-ttu-id="14f11-125">"WIP" 標記代表「進行中的工作 (Work in Progress)」。</span><span class="sxs-lookup"><span data-stu-id="14f11-125">The "WIP" tag stands for "Work in Progress."</span></span> 

<span data-ttu-id="14f11-126">「參與者授權合約」(CLA) 機器人所使用的處理方式是一個可區別「小型」與「大型」貢獻的良好指導方針。</span><span class="sxs-lookup"><span data-stu-id="14f11-126">The processing used by the Contributor License Agreement (CLA) bot is a good guideline for the distinction between "small" and "large" contributions.</span></span> <span data-ttu-id="14f11-127">不需要簽署 CLA 的 PR，通常是「小型」的。</span><span class="sxs-lookup"><span data-stu-id="14f11-127">PRs that do not require the CLA to be signed are likely "small."</span></span> <span data-ttu-id="14f11-128">需要 CLA 的 PR 則通常是「大型」的。</span><span class="sxs-lookup"><span data-stu-id="14f11-128">PRs that do require the CLA are likely "large."</span></span>

### <a name="small-prs"></a><span data-ttu-id="14f11-129">小型 PR</span><span class="sxs-lookup"><span data-stu-id="14f11-129">Small PRs</span></span>

<span data-ttu-id="14f11-130">小型 PR 中的變更會針對正確性進行檢閱，並使用檢閱站台上的組建進行檢查。</span><span class="sxs-lookup"><span data-stu-id="14f11-130">The changes in small PRs are reviewed for accuracy, and checked using the build on the review site.</span></span> <span data-ttu-id="14f11-131">由於這些 PR 較小，它們並不會觸發針對整篇文章的檢閱。</span><span class="sxs-lookup"><span data-stu-id="14f11-131">Because they are small, these PRs do not trigger a review of the entire article.</span></span> 

<span data-ttu-id="14f11-132">檢閱者可能會注意到其他能改善文章的小型變更。</span><span class="sxs-lookup"><span data-stu-id="14f11-132">Reviewers may notice other small changes that would improve an article.</span></span> <span data-ttu-id="14f11-133">若那些變更的幅度也相當小，請以檢閱註解的方式建議它們。</span><span class="sxs-lookup"><span data-stu-id="14f11-133">If those changes are also small, suggest them as review comments.</span></span> <span data-ttu-id="14f11-134">若建議的變更會觸發較大規模的檢閱，請提出問題並於未來解決它們。</span><span class="sxs-lookup"><span data-stu-id="14f11-134">If the suggested changes would trigger a larger review, open an issue and address those later.</span></span> 

### <a name="larger-changes"></a><span data-ttu-id="14f11-135">大型變更</span><span class="sxs-lookup"><span data-stu-id="14f11-135">Larger changes</span></span>

<span data-ttu-id="14f11-136">大型 PR 需要進行更徹底的檢閱。</span><span class="sxs-lookup"><span data-stu-id="14f11-136">Larger PRs undergo a more thorough review.</span></span> <span data-ttu-id="14f11-137">會檢查下列所有項目：</span><span class="sxs-lookup"><span data-stu-id="14f11-137">The following are all checked:</span></span>

- <span data-ttu-id="14f11-138">範例程式碼必須包含在 PR、來源，以及可下載的 zip 檔案中。</span><span class="sxs-lookup"><span data-stu-id="14f11-138">Sample code must be included in the PR, in source and as a downloadable zip file.</span></span>
- <span data-ttu-id="14f11-139">範例程式碼必須編譯並正常運作。</span><span class="sxs-lookup"><span data-stu-id="14f11-139">Sample code compiles and runs correctly.</span></span>
- <span data-ttu-id="14f11-140">文章必須清楚地為讀者描述目標，並達成那些目標。</span><span class="sxs-lookup"><span data-stu-id="14f11-140">The article clearly describes the goals for the reader, and those goals are met.</span></span>
- <span data-ttu-id="14f11-141">文章符合[樣式和文法指導方針](dotnet-style-guide.md)，並且依循我們的[語態和語調原則](dotnet-voice-tone.md)。</span><span class="sxs-lookup"><span data-stu-id="14f11-141">The article meets [style and grammar guidelines](dotnet-style-guide.md) and follows our [voice and tone principles](dotnet-voice-tone.md).</span></span>
- <span data-ttu-id="14f11-142">所有連結都必須能正確解析。</span><span class="sxs-lookup"><span data-stu-id="14f11-142">All links should resolve correctly.</span></span>

<span data-ttu-id="14f11-143">內容小組成員將會檢閱 PR，並搭配註解提交檢閱。</span><span class="sxs-lookup"><span data-stu-id="14f11-143">Content team members will review the PR, and submit the review with comments.</span></span> <span data-ttu-id="14f11-144">若僅要求次要變更，小組成員可以透過意見反應「核准」該 PR。</span><span class="sxs-lookup"><span data-stu-id="14f11-144">If only minor changes are requested, team members may "approve" the PR with the feedback.</span></span> <span data-ttu-id="14f11-145">作者可以接著處理意見反應內容並合併 PR。</span><span class="sxs-lookup"><span data-stu-id="14f11-145">The author can then address the feedback and merge the PR.</span></span> <span data-ttu-id="14f11-146">大部分的檢閱都會要求變更，而當那些變更都被執行之後，檢閱者便會再次檢閱。</span><span class="sxs-lookup"><span data-stu-id="14f11-146">Most reviews will request changes and when those changes are made, the reviewer will review again.</span></span>

<span data-ttu-id="14f11-147">若編輯需要技術性檢閱，內容小組檢閱者將會要求適當的產品小組成員進行檢閱。</span><span class="sxs-lookup"><span data-stu-id="14f11-147">If the edits require a technical review, the content team reviewer will request a review from the appropriate product team member.</span></span>

### <a name="review-wip-pull-requests"></a><span data-ttu-id="14f11-148">檢閱 "WIP" 提取要求</span><span class="sxs-lookup"><span data-stu-id="14f11-148">Review "WIP" pull requests</span></span>

<span data-ttu-id="14f11-149">新作者可能會想在程序初期便取得意見反應。</span><span class="sxs-lookup"><span data-stu-id="14f11-149">New authors may want feedback earlier in the process.</span></span> <span data-ttu-id="14f11-150">他們可以開啟 PR 並在標題中加入 "[WIP]" 標籤。</span><span class="sxs-lookup"><span data-stu-id="14f11-150">They can open a PR adding the "[WIP]" label to the title.</span></span> <span data-ttu-id="14f11-151">在註解中，他們可以要求早期檢閱。</span><span class="sxs-lookup"><span data-stu-id="14f11-151">In a comment, they can request an early review.</span></span>

<span data-ttu-id="14f11-152">這些早期檢閱不會像完整 PR 檢閱那麼徹底。</span><span class="sxs-lookup"><span data-stu-id="14f11-152">These early reviews are not as thorough as a full PR review.</span></span> <span data-ttu-id="14f11-153">內容小組將會提供註解，但將不會使用 GitHub 的檢閱功能進行「核准」或「要求變更」。</span><span class="sxs-lookup"><span data-stu-id="14f11-153">The content team will comment, but will not "approve" or "request changes" using GitHub's review feature.</span></span> <span data-ttu-id="14f11-154">這些早期檢閱的重點在於文章的結構：大綱、整體內容及範例。</span><span class="sxs-lookup"><span data-stu-id="14f11-154">These early reviews focus on the structure of the article: the outline, the overall content, and the samples.</span></span> <span data-ttu-id="14f11-155">這些檢閱並不會針對文法或連結進行徹底的檢查。</span><span class="sxs-lookup"><span data-stu-id="14f11-155">These reviews do not include a thorough check for grammar and correct links.</span></span>

## <a name="respond-to-reviews"></a><span data-ttu-id="14f11-156">回應檢閱</span><span class="sxs-lookup"><span data-stu-id="14f11-156">Respond to reviews</span></span>

<span data-ttu-id="14f11-157">作者會更新 PR 以回應註解，並在每個已處理的註解上標記 "+1" 反應，以指出該註解已處理完畢。</span><span class="sxs-lookup"><span data-stu-id="14f11-157">The author updates the PR to respond to comments marking each addressed comment with the "+1" reaction to indicate it was addressed.</span></span> <span data-ttu-id="14f11-158">若作者不同意註解，或是以不同的方式處理該註解，他會加上註解以解釋其變更。</span><span class="sxs-lookup"><span data-stu-id="14f11-158">If the author disagrees with the comment, or addresses the comment in a different, the author adds a comment explaining their change.</span></span>

<span data-ttu-id="14f11-159">作者會在註解中對原始檢閱者進行 @-mentions 以要求新的檢閱。</span><span class="sxs-lookup"><span data-stu-id="14f11-159">The author @-mentions the original reviewer in a comment to request a new review.</span></span> 

## <a name="response-time-expectations"></a><span data-ttu-id="14f11-160">預期回應時間</span><span class="sxs-lookup"><span data-stu-id="14f11-160">Response time expectations</span></span>

<span data-ttu-id="14f11-161">內容小組成員通常會在兩個工作日以內對新的 PR 進行檢閱。</span><span class="sxs-lookup"><span data-stu-id="14f11-161">Content team members will typically review new PRs in under two business days.</span></span> <span data-ttu-id="14f11-162">若檢閱時間較長，其中一個小組成員將會加入註解以確認該 PR 並設立預期時程。</span><span class="sxs-lookup"><span data-stu-id="14f11-162">If it takes longer to review, one of the team members will add a comment to acknowledge the PR and set expectations.</span></span>

<span data-ttu-id="14f11-163">在檢閱者提交檢閱之後，作者應該嘗試在一週以內對註解做出回應。</span><span class="sxs-lookup"><span data-stu-id="14f11-163">Once a review has been submitted, authors should try to respond to comments in a week or less.</span></span> <span data-ttu-id="14f11-164">志工可能會因為自己工作或生活上的其他承諾，而無法達成這些預期的時程。</span><span class="sxs-lookup"><span data-stu-id="14f11-164">Volunteers may not be able to meet these expectations because of other commitments.</span></span> <span data-ttu-id="14f11-165">在那些情況下，小組成員會詢問社群作者是否能更新該 PR。</span><span class="sxs-lookup"><span data-stu-id="14f11-165">In those cases, team members ask if the community author will update the PR.</span></span> <span data-ttu-id="14f11-166">若不行，小組成員將會代替他們更新並合併該 PR。</span><span class="sxs-lookup"><span data-stu-id="14f11-166">If not, the team member updates and merges the PR for them.</span></span>
