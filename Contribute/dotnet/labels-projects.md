---
title: 標籤和專案藍圖
description: 本文說明 dotnet/docs 存放庫中標籤和專案的使用方式。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 03/24/2020
ms.openlocfilehash: 0dcac28db04378730b186c0f23064c1433d9f80e
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/04/2020
ms.locfileid: "80760368"
---
# <a name="labels-and-projects-roadmap"></a><span data-ttu-id="4ae02-103">標籤和專案藍圖</span><span class="sxs-lookup"><span data-stu-id="4ae02-103">Labels and projects roadmap</span></span>

<span data-ttu-id="4ae02-104">.NET 文件小組廣泛使用 [GitHub 標籤](https://github.com/dotnet/docs/labels)來管理工作。</span><span class="sxs-lookup"><span data-stu-id="4ae02-104">The .NET docs team makes extensive use of [GitHub labels](https://github.com/dotnet/docs/labels) to organize our work.</span></span> <span data-ttu-id="4ae02-105">藉由篩選標籤組合，即可快速專注於 [.NET 文件網站](https://docs.microsoft.com/dotnet)上感興趣的章節。</span><span class="sxs-lookup"><span data-stu-id="4ae02-105">By filtering on combinations of labels, we can quickly focus on sections of interest on the [.NET docs website](https://docs.microsoft.com/dotnet).</span></span>

<span data-ttu-id="4ae02-106">我們也使用 [GitHub 專案](https://github.com/dotnet/docs/projects) 來管理短期衝刺及其他目標導向的 Epic。</span><span class="sxs-lookup"><span data-stu-id="4ae02-106">We also use [GitHub projects](https://github.com/dotnet/docs/projects) to organize sprints and other goal-oriented epics.</span></span>

<span data-ttu-id="4ae02-107">此藍圖說明如何使用這些管理工具，並包含便利的篩選連結，以便用來尋找感興趣的區域。</span><span class="sxs-lookup"><span data-stu-id="4ae02-107">This roadmap explains how we use these organizational tools and has links to handy filters we use to find areas of interest.</span></span>

## <a name="labels"></a><span data-ttu-id="4ae02-108">標籤</span><span class="sxs-lookup"><span data-stu-id="4ae02-108">Labels</span></span>

<span data-ttu-id="4ae02-109">如果這是第一次參與 [dotnet/docs](https://github.com/dotnet/docs)，建議您從 [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) 問題開始。</span><span class="sxs-lookup"><span data-stu-id="4ae02-109">If this is your first experience contributing to [dotnet/docs](https://github.com/dotnet/docs), start with the [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) issues.</span></span> <span data-ttu-id="4ae02-110">這些是範圍較集中的問題。</span><span class="sxs-lookup"><span data-stu-id="4ae02-110">These are issues that have a more focused scope.</span></span> <span data-ttu-id="4ae02-111">也是您第一次參與的絕佳方式。</span><span class="sxs-lookup"><span data-stu-id="4ae02-111">They are a great way to make your first contribution.</span></span> <span data-ttu-id="4ae02-112">從 up-for-grabs 檢視，您可根據區域和優先順序進一步篩選問題。</span><span class="sxs-lookup"><span data-stu-id="4ae02-112">From the up-for-grabs view, you can further filter issues based on areas and priority.</span></span> <span data-ttu-id="4ae02-113">如果想要在第一次參與時嘗試較不嚴重的問題，我們在 [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) 中列出了適合初學者的不錯問題。</span><span class="sxs-lookup"><span data-stu-id="4ae02-113">We've identified good issues for beginners with the [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) if you want to try a smaller first contribution.</span></span>

<span data-ttu-id="4ae02-114">我們使用標籤，以許多不同的方式來分類問題：</span><span class="sxs-lookup"><span data-stu-id="4ae02-114">We use labels to classify issues in many different ways:</span></span>

- <span data-ttu-id="4ae02-115">[.NET 指南](#find-a-single-net-guide)和[指南的章節](#search-one-section-of-a-guide)。</span><span class="sxs-lookup"><span data-stu-id="4ae02-115">[.NET Guides](#find-a-single-net-guide) and [sections of a guide](#search-one-section-of-a-guide).</span></span>
- [<span data-ttu-id="4ae02-116">目標版本</span><span class="sxs-lookup"><span data-stu-id="4ae02-116">Target release</span></span>](#releases)
- [<span data-ttu-id="4ae02-117">優先順序</span><span class="sxs-lookup"><span data-stu-id="4ae02-117">Priority</span></span>](#priority)

<span data-ttu-id="4ae02-118">您可從每個集合 (指南、版本、優先順序) 合併成一個標籤來建立範圍較窄的焦點，以尋找想要解決的問題。</span><span class="sxs-lookup"><span data-stu-id="4ae02-118">You can combine a label from each set (guide, release, priority) to create a narrow focus to find issues you want to work on.</span></span>

### <a name="find-a-single-net-guide"></a><span data-ttu-id="4ae02-119">尋找單一 .NET 指南</span><span class="sxs-lookup"><span data-stu-id="4ae02-119">Find a single .NET guide</span></span>

<span data-ttu-id="4ae02-120">我們針對每個架構電子書和每個 .NET 指南使用標籤。</span><span class="sxs-lookup"><span data-stu-id="4ae02-120">We use labels for each of the architecture e-books and for each .NET Guide.</span></span>

<span data-ttu-id="4ae02-121">![淺綠色背景上的 :book: guide](./media/labels-projects/guide.png "架構指南標籤的前置詞")</span><span class="sxs-lookup"><span data-stu-id="4ae02-121">![:book: guide on light green background](./media/labels-projects/guide.png "Prefix for architecture guide labels")</span></span>

<span data-ttu-id="4ae02-122">架構電子書會以 `:book: guide` 前置詞來註明，並具有淺綠色背景。</span><span class="sxs-lookup"><span data-stu-id="4ae02-122">Architecture e-books are noted with the `:book: guide` prefix and have a light green background.</span></span> <span data-ttu-id="4ae02-123">這些是涵蓋建議架構的完整格式區域。</span><span class="sxs-lookup"><span data-stu-id="4ae02-123">These are the long-form areas that cover recommended architecture.</span></span> <span data-ttu-id="4ae02-124">以下是針對每個 .NET 架構指南篩選的目前問題。</span><span class="sxs-lookup"><span data-stu-id="4ae02-124">Here are current issues filtered for each of the .NET architecture guides.</span></span>

- [<span data-ttu-id="4ae02-125">ASP.NET Core Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="4ae02-125">ASP.NET Core web apps</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20ASP.NET%20Core%20web%20apps)
- [<span data-ttu-id="4ae02-126">Blazor</span><span class="sxs-lookup"><span data-stu-id="4ae02-126">Blazor</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Blazor)
- [<span data-ttu-id="4ae02-127">雲端原生</span><span class="sxs-lookup"><span data-stu-id="4ae02-127">Cloud Native</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Cloud%20Native)
- [<span data-ttu-id="4ae02-128">Docker 生命週期</span><span class="sxs-lookup"><span data-stu-id="4ae02-128">Docker lifecycle</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Docker%20lifecycle)
- [<span data-ttu-id="4ae02-129">gRPC</span><span class="sxs-lookup"><span data-stu-id="4ae02-129">gRPC</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20gRPC)
- [<span data-ttu-id="4ae02-130">使用 Windows 容器進行現代化</span><span class="sxs-lookup"><span data-stu-id="4ae02-130">Modernizing w/ Windows containers</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Modernizing%20w%2F%20Windows%20containers)
- [<span data-ttu-id="4ae02-131">.NET 微服務</span><span class="sxs-lookup"><span data-stu-id="4ae02-131">.NET Microservices</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20.NET%20Microservices)
- [<span data-ttu-id="4ae02-132">無伺服器應用程式</span><span class="sxs-lookup"><span data-stu-id="4ae02-132">Serverless apps</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Serverless%20apps)

<span data-ttu-id="4ae02-133">此標籤樣式也適用於 [Framework 設計方針](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines)。</span><span class="sxs-lookup"><span data-stu-id="4ae02-133">This label style is also applied to the [Framework design guidelines](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines).</span></span> <span data-ttu-id="4ae02-134">此區域具有相同的標籤設計，但不建議社群公關部門使用。</span><span class="sxs-lookup"><span data-stu-id="4ae02-134">This area has the same label design, but community PRs are discouraged.</span></span> <span data-ttu-id="4ae02-135">這是需要許可才能轉載的內容，且不可編輯。</span><span class="sxs-lookup"><span data-stu-id="4ae02-135">This is material reprinted with permission and should not be edited.</span></span>

<span data-ttu-id="4ae02-136">![深藍色背景上的 :books:區域](./media/labels-projects/area.png ".NET 指南區域標籤的前置詞")</span><span class="sxs-lookup"><span data-stu-id="4ae02-136">![:books: Area on dark blue background](./media/labels-projects/area.png "Prefix for .NET Guide area labels")</span></span>

<span data-ttu-id="4ae02-137">每個 .NET 指南會以 `:books: Area` 前置詞來註明，並具有深藍色背景。</span><span class="sxs-lookup"><span data-stu-id="4ae02-137">Each .NET Guide is noted with the `:books: Area` prefix and has a dark blue background.</span></span> <span data-ttu-id="4ae02-138">以下是針對每個 .NET 指南篩選的目前問題。</span><span class="sxs-lookup"><span data-stu-id="4ae02-138">Here are current issues filtered for each of the .NET guides.</span></span>

- [<span data-ttu-id="4ae02-139">API 參照</span><span class="sxs-lookup"><span data-stu-id="4ae02-139">API Reference</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20API%20Reference)
- [<span data-ttu-id="4ae02-140">Azure .NET SDK</span><span class="sxs-lookup"><span data-stu-id="4ae02-140">Azure .NET SDK</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Azure%20.NET%20SDk)
- [<span data-ttu-id="4ae02-141">C# 指南</span><span class="sxs-lookup"><span data-stu-id="4ae02-141">C# Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20C%23%20Guide)
- [<span data-ttu-id="4ae02-142">桌面指南</span><span class="sxs-lookup"><span data-stu-id="4ae02-142">Desktop Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Desktop%20Guide)
- [<span data-ttu-id="4ae02-143">F# 指南</span><span class="sxs-lookup"><span data-stu-id="4ae02-143">F# Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20F%23%20Guide)
- [<span data-ttu-id="4ae02-144">ML.NET 指南</span><span class="sxs-lookup"><span data-stu-id="4ae02-144">ML.NET Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20ML.NET%20Guide)
- <span data-ttu-id="4ae02-145">[.NET 架構指南](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) - 可移除</span><span class="sxs-lookup"><span data-stu-id="4ae02-145">[.NET Architecture Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) - Could be removed</span></span>
- [<span data-ttu-id="4ae02-146">.NET Core 指南</span><span class="sxs-lookup"><span data-stu-id="4ae02-146">.NET Core Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Core%20Guide)
- [<span data-ttu-id="4ae02-147">適用於 Apache Spark 的 .NET 指南</span><span class="sxs-lookup"><span data-stu-id="4ae02-147">.NET for Apache Spark Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20for%20Apache%20Spark%20Guide)
- [<span data-ttu-id="4ae02-148">.NET Framework 指南</span><span class="sxs-lookup"><span data-stu-id="4ae02-148">.NET Framework Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Framework%20Guide)
- [<span data-ttu-id="4ae02-149">.NET 指南</span><span class="sxs-lookup"><span data-stu-id="4ae02-149">.NET Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Guide)
- <span data-ttu-id="4ae02-150">[Roslyn API 參照](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) - 可移除。</span><span class="sxs-lookup"><span data-stu-id="4ae02-150">[Roslyn API Reference](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) - could be removed.</span></span>
- [<span data-ttu-id="4ae02-151">Visual Basic 指南</span><span class="sxs-lookup"><span data-stu-id="4ae02-151">Visual Basic Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Visual%20Basic%20Guide)

#### <a name="search-one-section-of-a-guide"></a><span data-ttu-id="4ae02-152">搜尋指南的某個章節</span><span class="sxs-lookup"><span data-stu-id="4ae02-152">Search one section of a guide</span></span>

<span data-ttu-id="4ae02-153">![中藍色背景上的 :card_file_box:區域](./media/labels-projects/technology.png ".NET 指南子區域標籤的前置詞")</span><span class="sxs-lookup"><span data-stu-id="4ae02-153">![:card_file_box: Area on medium blue background](./media/labels-projects/technology.png "Prefix for .NET Guide sub-area labels")</span></span>

<span data-ttu-id="4ae02-154">.NET 指南很大，因此這些標籤會依指南章節進一步限制範圍。</span><span class="sxs-lookup"><span data-stu-id="4ae02-154">The .NET guides are large, so these labels further limit the scope by a section of a guide.</span></span> <span data-ttu-id="4ae02-155">每個 .NET 指南子區域會以 `:card_file_box: Technology` 前置詞來註明，並具有中藍色背景。</span><span class="sxs-lookup"><span data-stu-id="4ae02-155">Each .NET Guide subarea is noted with the `:card_file_box: Technology` prefix and has a medium blue background.</span></span> <span data-ttu-id="4ae02-156">這些標籤中有許多適用於多個指南，而其他標籤則只適用於一個指南。</span><span class="sxs-lookup"><span data-stu-id="4ae02-156">Many of these labels apply to multiple guides, while others are in only one guide.</span></span> <span data-ttu-id="4ae02-157">依區域篩選之後，請新增下列其中一個標籤，以進一步限制問題的範圍。</span><span class="sxs-lookup"><span data-stu-id="4ae02-157">After filtering on an area, add one of these labels to further limit the scope of issues.</span></span>

- <span data-ttu-id="4ae02-158">AppCompat</span><span class="sxs-lookup"><span data-stu-id="4ae02-158">AppCompat</span></span>
- <span data-ttu-id="4ae02-159">非同步工作</span><span class="sxs-lookup"><span data-stu-id="4ae02-159">Async Task</span></span>
- <span data-ttu-id="4ae02-160">C# 進階概念</span><span class="sxs-lookup"><span data-stu-id="4ae02-160">C# Advanced concepts</span></span>
- <span data-ttu-id="4ae02-161">C# 編譯器</span><span class="sxs-lookup"><span data-stu-id="4ae02-161">C# compiler</span></span>
- <span data-ttu-id="4ae02-162">C# 基礎</span><span class="sxs-lookup"><span data-stu-id="4ae02-162">C# Fundamentals</span></span>
- <span data-ttu-id="4ae02-163">C# 入門</span><span class="sxs-lookup"><span data-stu-id="4ae02-163">C# Get Started</span></span>
- <span data-ttu-id="4ae02-164">C# 語言參考</span><span class="sxs-lookup"><span data-stu-id="4ae02-164">C# Language Reference</span></span>
- <span data-ttu-id="4ae02-165">C# Null 安全</span><span class="sxs-lookup"><span data-stu-id="4ae02-165">C# Null safety</span></span>
- <span data-ttu-id="4ae02-166">C# 的新功能</span><span class="sxs-lookup"><span data-stu-id="4ae02-166">C# What's new</span></span>
- <span data-ttu-id="4ae02-167">CLI</span><span class="sxs-lookup"><span data-stu-id="4ae02-167">CLI</span></span>
- <span data-ttu-id="4ae02-168">資料存取</span><span class="sxs-lookup"><span data-stu-id="4ae02-168">Data Access</span></span>
- <span data-ttu-id="4ae02-169">Docker</span><span class="sxs-lookup"><span data-stu-id="4ae02-169">Docker</span></span>
- <span data-ttu-id="4ae02-170">安裝程式</span><span class="sxs-lookup"><span data-stu-id="4ae02-170">Installers</span></span>
- <span data-ttu-id="4ae02-171">LINQ</span><span class="sxs-lookup"><span data-stu-id="4ae02-171">LINQ</span></span>
- <span data-ttu-id="4ae02-172">NCL</span><span class="sxs-lookup"><span data-stu-id="4ae02-172">NCL</span></span>
- <span data-ttu-id="4ae02-173">.NET Standard</span><span class="sxs-lookup"><span data-stu-id="4ae02-173">.NET Standard</span></span>
- <span data-ttu-id="4ae02-174">Roslyn API</span><span class="sxs-lookup"><span data-stu-id="4ae02-174">Roslyn APIs</span></span>
- <span data-ttu-id="4ae02-175">安全性</span><span class="sxs-lookup"><span data-stu-id="4ae02-175">Security</span></span>
- <span data-ttu-id="4ae02-176">WCF</span><span class="sxs-lookup"><span data-stu-id="4ae02-176">WCF</span></span>
- <span data-ttu-id="4ae02-177">WF</span><span class="sxs-lookup"><span data-stu-id="4ae02-177">WF</span></span>
- <span data-ttu-id="4ae02-178">WIF</span><span class="sxs-lookup"><span data-stu-id="4ae02-178">WIF</span></span>
- <span data-ttu-id="4ae02-179">WinForms</span><span class="sxs-lookup"><span data-stu-id="4ae02-179">WinForms</span></span>
- <span data-ttu-id="4ae02-180">WPF</span><span class="sxs-lookup"><span data-stu-id="4ae02-180">WPF</span></span>

### <a name="releases"></a><span data-ttu-id="4ae02-181">版本</span><span class="sxs-lookup"><span data-stu-id="4ae02-181">Releases</span></span>

<span data-ttu-id="4ae02-182">![深黃色上的 :checkered_flag:Release:](./media/labels-projects/release.png "版本標籤的前置詞")</span><span class="sxs-lookup"><span data-stu-id="4ae02-182">![:checkered_flag: Release: on dark yellow](./media/labels-projects/release.png "Prefix for release labels")</span></span>

<span data-ttu-id="4ae02-183">針對特定版本標記的問題會以 `:checkered_flag: Release:` 前置詞來註明，並具有深黃色背景。</span><span class="sxs-lookup"><span data-stu-id="4ae02-183">Issues tagged for a specific release are noted with the `:checkered_flag: Release:` prefix and have a dark yellow background.</span></span>

- <span data-ttu-id="4ae02-184">.NET Core 2.2</span><span class="sxs-lookup"><span data-stu-id="4ae02-184">.NET Core 2.2</span></span>
- <span data-ttu-id="4ae02-185">.NET Core 3.0</span><span class="sxs-lookup"><span data-stu-id="4ae02-185">.NET Core 3.0</span></span>
- <span data-ttu-id="4ae02-186">.NET Framework 4.8</span><span class="sxs-lookup"><span data-stu-id="4ae02-186">.NET Framework 4.8</span></span>
- <span data-ttu-id="4ae02-187">.NET 5</span><span class="sxs-lookup"><span data-stu-id="4ae02-187">.NET 5</span></span>

### <a name="priority"></a><span data-ttu-id="4ae02-188">優先順序</span><span class="sxs-lookup"><span data-stu-id="4ae02-188">Priority</span></span>

<span data-ttu-id="4ae02-189">所有優先順序標籤都是 `P` 後面接著一位數。</span><span class="sxs-lookup"><span data-stu-id="4ae02-189">Priority labels are all `P` followed by a single digit.</span></span> <span data-ttu-id="4ae02-190">數字越低則表示優先順序越高：</span><span class="sxs-lookup"><span data-stu-id="4ae02-190">Lower numbers are higher priority:</span></span>

- <span data-ttu-id="4ae02-191">P0</span><span class="sxs-lookup"><span data-stu-id="4ae02-191">P0</span></span>
- <span data-ttu-id="4ae02-192">P1</span><span class="sxs-lookup"><span data-stu-id="4ae02-192">P1</span></span>
- <span data-ttu-id="4ae02-193">P2</span><span class="sxs-lookup"><span data-stu-id="4ae02-193">P2</span></span>
- <span data-ttu-id="4ae02-194">P3</span><span class="sxs-lookup"><span data-stu-id="4ae02-194">P3</span></span>

### <a name="what-about-the-other-labels"></a><span data-ttu-id="4ae02-195">其他標籤如何？</span><span class="sxs-lookup"><span data-stu-id="4ae02-195">What about the other labels?</span></span>

<span data-ttu-id="4ae02-196">內容小組使用許多其他標籤來管理不同分類的問題。</span><span class="sxs-lookup"><span data-stu-id="4ae02-196">There are many other labels used by the content teams to manage different classifications of issues.</span></span> <span data-ttu-id="4ae02-197">如果您不在內容小組上，則可以忽略這些其他標籤。</span><span class="sxs-lookup"><span data-stu-id="4ae02-197">If you're not on the content team, you can ignore these other labels.</span></span>

## <a name="projects"></a><span data-ttu-id="4ae02-198">專案</span><span class="sxs-lookup"><span data-stu-id="4ae02-198">Projects</span></span>

<span data-ttu-id="4ae02-199">我們透過兩種方式來使用專案：</span><span class="sxs-lookup"><span data-stu-id="4ae02-199">We use projects in two ways:</span></span>

- <span data-ttu-id="4ae02-200">Month YYYY 專案類型：這些是每月工作計畫的 Scrum 面板。</span><span class="sxs-lookup"><span data-stu-id="4ae02-200">Month YYYY project types: These are scrum boards for each month's working plan.</span></span>
- <span data-ttu-id="4ae02-201">長時間執行的 Epic：這些會在工作持續數個月時，用來管理工作達成目標的進度。</span><span class="sxs-lookup"><span data-stu-id="4ae02-201">Long-running epics: These are used to organize tasks toward a goal when the work will occur over several months.</span></span>
