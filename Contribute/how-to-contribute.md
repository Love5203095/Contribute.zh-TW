---
title: 如何參與 docs.microsoft.com
description: 本文描述參與 docs.microsoft.com 內容的不同方式。
author: billwagner
ms.author: wiwagn
manager: wpickett
ms.date: 01/17/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: bc6f9c314eda5f0d950da049374a7a157f16782a
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2018
---
# <a name="how-to-contribute-to-docsmicrosoftcom"></a><span data-ttu-id="8f8fb-103">如何參與 docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="8f8fb-103">How to contribute to docs.microsoft.com</span></span>

<span data-ttu-id="8f8fb-104">有數種可以參與改善組成 [docs.microsoft.com](https://docs.microsoft.com) 之內容的方式：</span><span class="sxs-lookup"><span data-stu-id="8f8fb-104">There are several ways to participate in improving the content that makes up [docs.microsoft.com](https://docs.microsoft.com):</span></span>

- <span data-ttu-id="8f8fb-105">您可以[建立問題](#create-issues)，以建議新文章或改善現有的文章。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-105">You can [create issues](#create-issues) to recommend new articles, or improve existing articles.</span></span>
- <span data-ttu-id="8f8fb-106">您可以在 GitHub 線上編輯器中[快速編輯](#quick-edits)文章以進行小變更。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-106">You can [quickly edit](#quick-edits) articles to make small changes in the GitHub online editor.</span></span>
- <span data-ttu-id="8f8fb-107">您可以[校閱新文章的草稿](#review-new-articles)，以確保品質和技術正確性。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-107">You can [review drafts of new articles](#review-new-articles) to ensure quality and technical accuracy.</span></span>
- <span data-ttu-id="8f8fb-108">您可以為主題[建立新文章](#create-new-articles)，以協助發展內容的敘述。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-108">You can [create new articles](#create-new-articles) for topics when you want to help drive the content story.</span></span>
- <span data-ttu-id="8f8fb-109">您可以[更新](#update-samples)或[建立](#create-samples)範例，以改善輔助重要概念的程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-109">You can [update](#update-samples) or [create](#create-samples) samples to improve the code samples that reinforce important concepts.</span></span>

<span data-ttu-id="8f8fb-110">在本文中，您將學習參與的不同方式、查看如何完成每一個工作，並尋找每個工作之相關詳細資訊的指標。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-110">In this article, you'll learn the different ways to contribute, see how to accomplish each of those tasks, and find pointers to more information about each of those tasks.</span></span>

<span data-ttu-id="8f8fb-111">我們的公用存放庫裝載於 [GitHub](https://wwww.GitHub.com)。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-111">Our public repositories are hosted on [GitHub](https://wwww.GitHub.com).</span></span>  <span data-ttu-id="8f8fb-112">您必須在 GitHub 上建立帳戶，以參與我們的文件存放庫。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-112">You will need to create an account on GitHub to participate in our documentation repositories.</span></span>

<span data-ttu-id="8f8fb-113">您也需要文字編輯器來更新文件。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-113">You'll also need a text editor to update the documents.</span></span> <span data-ttu-id="8f8fb-114">建議您使用 [Visual Studio Code](https://www.visualstudio.com/code)。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-114">We recommend [Visual Studio Code](https://www.visualstudio.com/code).</span></span> <span data-ttu-id="8f8fb-115">您對於 [Markdown](https://daringfireball.net/projects/markdown/syntax) 語法應該要有基本的了解。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-115">You should have a basic understanding of [Markdown](https://daringfireball.net/projects/markdown/syntax) syntax.</span></span>

<span data-ttu-id="8f8fb-116">如果您要加入或修改範例，您將需要一個開發環境。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-116">If you are adding or modifying samples, you'll need a development environment.</span></span> <span data-ttu-id="8f8fb-117">建議您使用 [Visual Studio](https://www.visualstudio.com) (PC 和 Mac) 或是 [Visual Studio Code](https://www.visualstudio.com/code) (所有平台)。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-117">We recommend [Visual Studio](https://www.visualstudio.com) on PC and Mac, or [Visual Studio Code](https://www.visualstudio.com/code) on all platforms.</span></span>

## <a name="create-issues"></a><span data-ttu-id="8f8fb-118">建立問題</span><span class="sxs-lookup"><span data-stu-id="8f8fb-118">Create issues</span></span>

<span data-ttu-id="8f8fb-119">如果您發現文章中有遺漏或是不正確，請針對該文章建立問題。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-119">If you find omissions or inaccuracies in a article, create an issue against that article.</span></span> <span data-ttu-id="8f8fb-120">尋找正確位置最簡單的方式，就是按一下您瀏覽器中的 [編輯] 按鈕，這將會帶您到正確的公用 GitHub 存放庫中的文章來源。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-120">The easiest way to find the right location is to click the "Edit" button in your browser, which will take you to the article source in the correct public GitHub repository.</span></span> <span data-ttu-id="8f8fb-121">您可以從該處擷取網址列中該文章的來源 URL。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-121">From there, you can retrieve the URL for the source of the article from your address bar.</span></span> <span data-ttu-id="8f8fb-122">按一下 [建立問題] 以建立有關該文章的新問題。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-122">Click "Create Issue" to make a new issue on the article.</span></span>

> [!NOTE]
> <span data-ttu-id="8f8fb-123">如果您發現稍微修改就能修正問題 (例如輸入錯誤或文法問題)，您可以使用瀏覽器，透過[提交修正](#quick-edits)來編輯來源，節省您的時間和我們的時間。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-123">If you find issues you can fix with small edits, such as typing mistakes or grammar issues, you can save yourself and us time by [submitting the fix](#quick-edits) using the browser to edit the source.</span></span>

<span data-ttu-id="8f8fb-124">我們大部分的公用存放庫包含了新問題的範本，可引導您提供修正問題所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-124">Most of our public repos contain templates for new issues that will guide you to provide the information needed to fix the issue.</span></span>

<span data-ttu-id="8f8fb-125">您也可以提供您無法找到所需資訊的新問題。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-125">You can also contribute new issues where you can't find the information you need.</span></span> <span data-ttu-id="8f8fb-126">程序是相同的：在其中一個公用文件存放庫上建立新問題。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-126">The process is the same: create a new issue on one of the public docs repositories.</span></span> <span data-ttu-id="8f8fb-127">告訴我們您正在搜尋的項目、您想要執行的動作，以及為何您找到的文章無法以您預期的方式協助您。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-127">Tell us what you were searching for, what you wanted to do, and why the articles you found did not help the way you expected.</span></span>

## <a name="review-new-articles"></a><span data-ttu-id="8f8fb-128">檢閱新文章</span><span class="sxs-lookup"><span data-stu-id="8f8fb-128">Review new articles</span></span>

<span data-ttu-id="8f8fb-129">如果您正在使用新的軟體 (可能是 CTP 或搶鮮版 (Beta))，在您探索技術的同時，我們可能正在建置文件。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-129">If you are working on new, possibly CTP or beta, software, we are likely building the docs as you are exploring the technology.</span></span> <span data-ttu-id="8f8fb-130">您可以在我們的公用存放庫中尋找處理中文件。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-130">You can find the in-process docs in our public repositories.</span></span> <span data-ttu-id="8f8fb-131">如果您有意見，您可以在文件發行之前，協助我們改進它們。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-131">If you have comments, you can help us make them better before they are released.</span></span>

<span data-ttu-id="8f8fb-132">新文章會使用 [GitHub 流程](https://guides.github.com/introduction/flow/)程序公開檢閱。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-132">New articles are reviewed in public, using the [GitHub flow](https://guides.github.com/introduction/flow/) process.</span></span> <span data-ttu-id="8f8fb-133">查看我們的任何文件存放庫，並查看未處理的提取要求 (PR)。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-133">Look at any of our docs repositories, and check the open pull requests (PRs).</span></span> <span data-ttu-id="8f8fb-134">我們歡迎有關任何未處理的提取要求的意見和評論。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-134">We welcome comments and reviews on any open pull requests.</span></span> <span data-ttu-id="8f8fb-135">這可以協助我們在初次發行時發佈更好的內容，而不是在上線之後等待意見反應。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-135">That helps us publish better content on our first release, rather than waiting for feedback after going live.</span></span>

<span data-ttu-id="8f8fb-136">我們正在尋找方法來改進技術的正確性、描述的精確度和文法的正確性。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-136">We are looking for ways to improve technical accuracy, clarity of the descriptions, and grammatical accuracy.</span></span>

## <a name="quick-edits"></a><span data-ttu-id="8f8fb-137">快速編輯</span><span class="sxs-lookup"><span data-stu-id="8f8fb-137">Quick edits</span></span>

<span data-ttu-id="8f8fb-138">快速編輯是使用瀏覽器型編輯器進行小修正的方法。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-138">Quick edits are a way to make small fixes using the browser based editor.</span></span> <span data-ttu-id="8f8fb-139">如果您找到小的拼字或文法錯誤，或是命名錯誤的 API，您可以透過編輯和提交 PR 來略過建立問題。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-139">If you find small spelling or grammar errors, or mis-named APIs, you can skip creating an issue by making the edit and submitting a PR.</span></span>

<span data-ttu-id="8f8fb-140">在任何文章上，按一下 [編輯] 按鈕 (通常是頁面右上方)、進行編輯，然後按一下頁面底部的 [提交 PR]。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-140">On any article, click the "Edit" button (usually toward the top right-hand side of the page), make your edits, and click "Submit PR" at the bottom of the page.</span></span> <span data-ttu-id="8f8fb-141">我們將檢閱 PR，並在我們進行每日 PR 檢閱時合併它。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-141">We'll review the PR, and merge it as we do our daily PR review.</span></span>

## <a name="create-new-articles"></a><span data-ttu-id="8f8fb-142">建立新文章</span><span class="sxs-lookup"><span data-stu-id="8f8fb-142">Create new articles</span></span>

<span data-ttu-id="8f8fb-143">如果有您熱衷的概念，且希望向其他人說明，您可以建立文章並提交 PR。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-143">If there are concepts you are passionate about, and want to explain to others, you can create the articles and submit a PR.</span></span>

<span data-ttu-id="8f8fb-144">建立新文章非常耗時，而我們非常重視您寶貴的時間與貢獻。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-144">Creating new articles is time-consuming, and we value your time and contributions.</span></span> <span data-ttu-id="8f8fb-145">我們希望能及早參與過程，以確保您從一開始就能遵循我們的指導方針與樣式。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-145">We want to be involved early in the process to ensure you're following our guidelines and style from the beginning.</span></span> <span data-ttu-id="8f8fb-146">我們建議您採取下列步驟：</span><span class="sxs-lookup"><span data-stu-id="8f8fb-146">We recommend the following steps:</span></span>

1. <span data-ttu-id="8f8fb-147">[建立問題](#create-issues)：說明缺失部分，以及您的處理方式。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-147">[Create an issue](#create-issues) describing what's missing and how you'd address it.</span></span>
1. <span data-ttu-id="8f8fb-148">對問題進行註解、告訴我們您希望處理該問題，並建議該文章的大綱與摘要。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-148">Comment on the issue, telling us you'd like to work on it, and suggesting an outline and abstract for the article.</span></span>
1. <span data-ttu-id="8f8fb-149">我們會透過建議來回應。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-149">We'll respond with suggestions.</span></span> <span data-ttu-id="8f8fb-150">這些可能包含相關文章的連結、範例的建議，或是組織文件的方式。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-150">These may include links to related articles, suggestions for samples, or how the article will be organized.</span></span>
1. <span data-ttu-id="8f8fb-151">一旦我們同意大綱，即會建立存放庫的分叉，您就可以開始進行。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-151">Once we agree on the outline, fork the repository, and start working.</span></span>
1. <span data-ttu-id="8f8fb-152">在流程初期，開啟 PR，並在標題開頭包含 "[WIP]"。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-152">Early in the process, open a PR, with "[WIP]" at the beginning of the title.</span></span>
1. <span data-ttu-id="8f8fb-153">其中一個核心參與者將提供您初始的意見反應。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-153">One of the core contributors will give you initial feedback.</span></span>
1. <span data-ttu-id="8f8fb-154">持續撰寫，當您準備好收到更多意見反應時，使用 @-mention 標註檢閱您初稿的人員。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-154">Keep writing, @-mention the person who reviewed the first draft when you're ready for more feedback.</span></span>
1. <span data-ttu-id="8f8fb-155">當您準備好進行最終檢閱，請移除 "[WIP]"。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-155">Remove the "[WIP]" when you're ready for final review.</span></span>
1. <span data-ttu-id="8f8fb-156">回應意見反應</span><span class="sxs-lookup"><span data-stu-id="8f8fb-156">Respond to the feedback</span></span>
1. <span data-ttu-id="8f8fb-157">核心參與者將會合併您的 PR。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-157">The core contributors will merge your PR.</span></span>

<span data-ttu-id="8f8fb-158">清單中有幾點值得擴充。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-158">There are a couple points worth expanding on from that list.</span></span> <span data-ttu-id="8f8fb-159">一般來說，我們會遵循 [GitHub 流程](https://guides.github.com/introduction/flow/)程序來盡早檢閱內容。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-159">In general, we're following the [GitHub flow](https://guides.github.com/introduction/flow/) process to review content as early as possible.</span></span> <span data-ttu-id="8f8fb-160">這樣一來，我們能同意文章應該在目錄中的哪個位置、讀者能從新文章得到哪些好處，還有您將建立之任何範例的範圍。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-160">That way, we agree on where an article should go in the table of contents, what benefit the reader will get from the new article, and the scope of any samples you'll create.</span></span> <span data-ttu-id="8f8fb-161">在您已投入大量時間撰寫之前，我們可以提早進行任何必要的課程修正。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-161">We can make any necessary course corrections early, before you've invested significant time writing.</span></span>

## <a name="update-samples"></a><span data-ttu-id="8f8fb-162">更新範例</span><span class="sxs-lookup"><span data-stu-id="8f8fb-162">Update samples</span></span>

<span data-ttu-id="8f8fb-163">某些範例可能原本在數個版本前就已經撰寫，其中使用不再建議的做法。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-163">Some samples may have originally been written several releases ago, using practices no long recommended.</span></span> <span data-ttu-id="8f8fb-164">您可能會希望協助我們更新那些範例。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-164">You may want to help us update those samples.</span></span> <span data-ttu-id="8f8fb-165">或者，您可能發現一個簡單的變數名稱變更，會增加說明的精確度。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-165">Or, you may find that a simple variable name change could increase the clarity of an explanation.</span></span>

<span data-ttu-id="8f8fb-166">每個文章中所顯示的範例程式碼，都屬於所建置的程式一部分，且經常在我們的 CI 系統下進行測試。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-166">The sample code displayed with each article are part of programs that are built and often tested under our CI system.</span></span>

<span data-ttu-id="8f8fb-167">若要進行小更新，您可以在適當的存放庫中尋找來源、在瀏覽器中進行程式碼變更並提交 PR。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-167">To make small updates, you find the source in the appropriate repository, make the code change in the browser and submit a PR.</span></span> <span data-ttu-id="8f8fb-168">我們的 CI 系統將建置這些變更，而我們會在它完成時合併 PR。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-168">Our CI system will build the changes, and we'll merge the PR when it finishes.</span></span>

<span data-ttu-id="8f8fb-169">針對較大的變更，請建立存放庫的分岔，並在您偏好的開發環境中進行變更。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-169">For larger scale changes fork the repository and make the changes in your favorite development environment.</span></span> <span data-ttu-id="8f8fb-170">請確定您已加入一些測試，以確保您的變更會如您預期般運作。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-170">Make sure you add some tests to ensure that your changes work as you intended.</span></span> <span data-ttu-id="8f8fb-171">提交 PR，我們將會加以檢閱。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-171">Submit a PR, and we'll review it.</span></span>

<span data-ttu-id="8f8fb-172">針對所有的程式碼變更，請遵循您正在修改之範例程式碼的現有程式碼慣例。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-172">With all code changes, follow the existing code conventions for the sample code you are modifying.</span></span> <span data-ttu-id="8f8fb-173">我們的範例存放庫程式碼撰寫標準將鏡映對應之產品小組的那些程式碼撰寫標準。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-173">Our samples repositories coding standards will mirror those of the corresponding product teams.</span></span> <span data-ttu-id="8f8fb-174">請查看每個存放庫以了解特定指導方針。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-174">Check each repository for specific guidance.</span></span>

> [!NOTE]
> <span data-ttu-id="8f8fb-175">我們本身也遵循此指導方針來進行處理。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-175">We're working toward following this guidance ourselves.</span></span> <span data-ttu-id="8f8fb-176">部分範例比我們目前的標準還要早，且尚未更新。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-176">Some of the samples predate our current standards ane have not been updated yet.</span></span> <span data-ttu-id="8f8fb-177">我們正朝著所有執行中的範例程式碼可顯示處理中、已測試、範例的目標努力。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-177">We are working toward a goal of all running sample code being displayed from working, tested, samples.</span></span>

## <a name="create-samples"></a><span data-ttu-id="8f8fb-178">建立範例</span><span class="sxs-lookup"><span data-stu-id="8f8fb-178">Create samples</span></span>

<span data-ttu-id="8f8fb-179">您也可以建立新的範例來示範概念或案例。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-179">You can also create new samples that demonstrate concepts or scenarios.</span></span> <span data-ttu-id="8f8fb-180">任何範例都必須伴隨一篇文章，以說明範例中的關鍵資訊。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-180">Any samples must be accompanied by a article that explains the key information from the sample.</span></span>

<span data-ttu-id="8f8fb-181">如果您的新範例可補充現有的文章，請在該文章中新增範例的參考。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-181">If your new sample complements an existing article, add a reference to the sample in that article.</span></span> <span data-ttu-id="8f8fb-182">如果沒有，請與我們合作[撰寫伴隨範例的文章](#create-new-articles)。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-182">If not, work with us to [write the article](#create-new-articles) that accompanies the sample.</span></span>

<span data-ttu-id="8f8fb-183">在所有情況下，我們的程式碼都遵循相關產品小組所使用的程式碼慣例。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-183">In all cases, our sample code follows the coding conventions used by the related product teams.</span></span> <span data-ttu-id="8f8fb-184">唯一例外的是，當那些宣告包含在文章中時，為了清楚起見，我們更可能會使用明確型別的變數，而非隱含型別的變數 (使用 `var` 宣告)。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-184">One exception is that we are more likely to use explicitly typed varables over implicitly typed (declared with `var`) for clarity when those declarations are included in the article.</span></span>

<span data-ttu-id="8f8fb-185">請遵循[新文章](#create-new-articles)中前一節所述的範例程序，這樣我們才能在開發程序中及早檢閱程式碼。</span><span class="sxs-lookup"><span data-stu-id="8f8fb-185">Follow the sample process outlined in the earlier section for [new articles](#create-new-articles) so that we can review the code early in the development process.</span></span>
