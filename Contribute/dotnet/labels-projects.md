---
title: 標籤、專案與里程碑藍圖
description: 此文章說明 dotnet/docs 存放庫中標籤、專案與里程碑的使用方式。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 08/06/2020
ms.openlocfilehash: b8e9f2a33f9b4a8025aa36a890bff1017cf132c6
ms.sourcegitcommit: abcc67cb3ec1f635a6374d7c47a4831e3eee9050
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "89559255"
---
# <a name="labels-projects-and-milestones-roadmap"></a><span data-ttu-id="fd081-103">標籤、專案與里程碑藍圖</span><span class="sxs-lookup"><span data-stu-id="fd081-103">Labels, projects, and milestones roadmap</span></span>

<span data-ttu-id="fd081-104">.NET 文件小組廣泛使用 [GitHub 標籤](https://github.com/dotnet/docs/labels)來管理工作。</span><span class="sxs-lookup"><span data-stu-id="fd081-104">The .NET docs team makes extensive use of [GitHub labels](https://github.com/dotnet/docs/labels) to organize our work.</span></span> <span data-ttu-id="fd081-105">藉由篩選標籤組合，即可快速專注於 [.NET 文件網站](https://docs.microsoft.com/dotnet)上感興趣的章節。</span><span class="sxs-lookup"><span data-stu-id="fd081-105">By filtering on combinations of labels, we can quickly focus on sections of interest on the [.NET docs website](https://docs.microsoft.com/dotnet).</span></span> <span data-ttu-id="fd081-106">例如，我們可以使用對 [is:issue is:open label:":books:Area - .NET 架構指南"](https://github.com/dotnet/docs/issues?q=is%3Aissue+is%3Aopen+label%3A%22%3Abooks%3A+Area+-+.NET+Architecture+Guide%22) \(英文\) 的查詢，來篩選至所有未結的優先順序一 `P1` 問題。</span><span class="sxs-lookup"><span data-stu-id="fd081-106">For example, we could filter to all of the open priority one `P1` issues with a query to [is:issue is:open label:":books: Area - .NET Architecture Guide"](https://github.com/dotnet/docs/issues?q=is%3Aissue+is%3Aopen+label%3A%22%3Abooks%3A+Area+-+.NET+Architecture+Guide%22).</span></span>

<span data-ttu-id="fd081-107">我們會使用 [GitHub 專案](https://github.com/dotnet/docs/projects) \(英文\) 來管理短期衝刺與其他目標導向的 Epic。</span><span class="sxs-lookup"><span data-stu-id="fd081-107">We use [GitHub projects](https://github.com/dotnet/docs/projects) to organize sprints and other goal-oriented epics.</span></span> <span data-ttu-id="fd081-108">我們也會使用 [GitHub 里程碑](https://github.com/dotnet/docs/milestones) \(英文\) 來追蹤工作。</span><span class="sxs-lookup"><span data-stu-id="fd081-108">We also use [GitHub milestones](https://github.com/dotnet/docs/milestones) to track work.</span></span> <span data-ttu-id="fd081-109">最好將專案視為用於規劃 (問題)，並將里程碑視為用於工作 (提取要求)。</span><span class="sxs-lookup"><span data-stu-id="fd081-109">It is best to think of projects for planning (issues), and milestones for work (pull requests).</span></span>

<span data-ttu-id="fd081-110">此藍圖說明如何使用這些管理工具，並包含便利的篩選連結，以便用來尋找感興趣的區域。</span><span class="sxs-lookup"><span data-stu-id="fd081-110">This roadmap explains how we use these organizational tools and has links to handy filters we use to find areas of interest.</span></span>

## <a name="labels"></a><span data-ttu-id="fd081-111">標籤</span><span class="sxs-lookup"><span data-stu-id="fd081-111">Labels</span></span>

<span data-ttu-id="fd081-112">如果這是第一次參與 [dotnet/docs](https://github.com/dotnet/docs)，建議您從 [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) 問題開始。</span><span class="sxs-lookup"><span data-stu-id="fd081-112">If this is your first experience contributing to [dotnet/docs](https://github.com/dotnet/docs), start with the [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) issues.</span></span> <span data-ttu-id="fd081-113">這些是範圍較集中的問題。</span><span class="sxs-lookup"><span data-stu-id="fd081-113">These are issues that have a more focused scope.</span></span> <span data-ttu-id="fd081-114">也是您第一次參與的絕佳方式。</span><span class="sxs-lookup"><span data-stu-id="fd081-114">They are a great way to make your first contribution.</span></span> <span data-ttu-id="fd081-115">從 up-for-grabs 檢視，您可根據區域和優先順序進一步篩選問題。</span><span class="sxs-lookup"><span data-stu-id="fd081-115">From the up-for-grabs view, you can further filter issues based on areas and priority.</span></span> <span data-ttu-id="fd081-116">如果想要在第一次參與時嘗試較不嚴重的問題，我們在 [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) 中列出了適合初學者的不錯問題。</span><span class="sxs-lookup"><span data-stu-id="fd081-116">We've identified good issues for beginners with the [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) if you want to try a smaller first contribution.</span></span>

<span data-ttu-id="fd081-117">我們使用標籤，以許多不同的方式來分類問題：</span><span class="sxs-lookup"><span data-stu-id="fd081-117">We use labels to classify issues in many different ways:</span></span>

- <span data-ttu-id="fd081-118">[.NET 指南](#find-a-single-net-guide)和[指南的章節](#search-one-section-of-a-guide)。</span><span class="sxs-lookup"><span data-stu-id="fd081-118">[.NET Guides](#find-a-single-net-guide) and [sections of a guide](#search-one-section-of-a-guide).</span></span>
- [<span data-ttu-id="fd081-119">目標版本</span><span class="sxs-lookup"><span data-stu-id="fd081-119">Target release</span></span>](#releases)
- [<span data-ttu-id="fd081-120">優先順序</span><span class="sxs-lookup"><span data-stu-id="fd081-120">Priority</span></span>](#priority)

<span data-ttu-id="fd081-121">您可從每個集合 (指南、版本、優先順序) 合併成一個標籤來建立範圍較窄的焦點，以尋找想要解決的問題。</span><span class="sxs-lookup"><span data-stu-id="fd081-121">You can combine a label from each set (guide, release, priority) to create a narrow focus to find issues you want to work on.</span></span>

### <a name="find-a-single-net-guide"></a><span data-ttu-id="fd081-122">尋找單一 .NET 指南</span><span class="sxs-lookup"><span data-stu-id="fd081-122">Find a single .NET guide</span></span>

<span data-ttu-id="fd081-123">我們針對每個架構電子書和每個 .NET 指南使用標籤。</span><span class="sxs-lookup"><span data-stu-id="fd081-123">We use labels for each of the architecture e-books and for each .NET Guide.</span></span>

<span data-ttu-id="fd081-124">![淺綠色背景上的 :book: guide](./media/labels-projects/guide.png "架構指南標籤的前置詞")</span><span class="sxs-lookup"><span data-stu-id="fd081-124">![:book: guide on light green background](./media/labels-projects/guide.png "Prefix for architecture guide labels")</span></span>

<span data-ttu-id="fd081-125">架構電子書會以 `:book: guide` 前置詞來註明，並具有淺綠色背景。</span><span class="sxs-lookup"><span data-stu-id="fd081-125">Architecture e-books are noted with the `:book: guide` prefix and have a light green background.</span></span> <span data-ttu-id="fd081-126">這些是涵蓋建議架構的完整格式區域。</span><span class="sxs-lookup"><span data-stu-id="fd081-126">These are the long-form areas that cover recommended architecture.</span></span> <span data-ttu-id="fd081-127">以下是針對每個 .NET 架構指南篩選的目前問題。</span><span class="sxs-lookup"><span data-stu-id="fd081-127">Here are current issues filtered for each of the .NET architecture guides.</span></span>

- [<span data-ttu-id="fd081-128">ASP.NET Core Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="fd081-128">ASP.NET Core web apps</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20ASP.NET%20Core%20web%20apps)
- [<span data-ttu-id="fd081-129">Blazor</span><span class="sxs-lookup"><span data-stu-id="fd081-129">Blazor</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Blazor)
- [<span data-ttu-id="fd081-130">雲端原生</span><span class="sxs-lookup"><span data-stu-id="fd081-130">Cloud Native</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Cloud%20Native)
- [<span data-ttu-id="fd081-131">Docker 生命週期</span><span class="sxs-lookup"><span data-stu-id="fd081-131">Docker lifecycle</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Docker%20lifecycle)
- [<span data-ttu-id="fd081-132">gRPC</span><span class="sxs-lookup"><span data-stu-id="fd081-132">gRPC</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20gRPC)
- [<span data-ttu-id="fd081-133">使用 Windows 容器進行現代化</span><span class="sxs-lookup"><span data-stu-id="fd081-133">Modernizing w/ Windows containers</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Modernizing%20w%2F%20Windows%20containers)
- [<span data-ttu-id="fd081-134">.NET 微服務</span><span class="sxs-lookup"><span data-stu-id="fd081-134">.NET Microservices</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20.NET%20Microservices)
- [<span data-ttu-id="fd081-135">無伺服器應用程式</span><span class="sxs-lookup"><span data-stu-id="fd081-135">Serverless apps</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Serverless%20apps)

<span data-ttu-id="fd081-136">此標籤樣式也適用於 [Framework 設計方針](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines)。</span><span class="sxs-lookup"><span data-stu-id="fd081-136">This label style is also applied to the [Framework design guidelines](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines).</span></span> <span data-ttu-id="fd081-137">此區域具有相同的標籤設計，但不建議社群公關部門使用。</span><span class="sxs-lookup"><span data-stu-id="fd081-137">This area has the same label design, but community PRs are discouraged.</span></span> <span data-ttu-id="fd081-138">這是需要許可才能轉載的內容，且不可編輯。</span><span class="sxs-lookup"><span data-stu-id="fd081-138">This is material reprinted with permission and should not be edited.</span></span>

<span data-ttu-id="fd081-139">![深藍色背景上的 :books:區域](./media/labels-projects/area.png ".NET 指南區域標籤的前置詞")</span><span class="sxs-lookup"><span data-stu-id="fd081-139">![:books: Area on dark blue background](./media/labels-projects/area.png "Prefix for .NET Guide area labels")</span></span>

<span data-ttu-id="fd081-140">每個 .NET 指南會以 `:books: Area` 前置詞來註明，並具有深藍色背景。</span><span class="sxs-lookup"><span data-stu-id="fd081-140">Each .NET Guide is noted with the `:books: Area` prefix and has a dark blue background.</span></span> <span data-ttu-id="fd081-141">以下是針對每個 .NET 指南篩選的目前問題。</span><span class="sxs-lookup"><span data-stu-id="fd081-141">Here are current issues filtered for each of the .NET guides.</span></span>

- [<span data-ttu-id="fd081-142">API 參考</span><span class="sxs-lookup"><span data-stu-id="fd081-142">API Reference</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20API%20Reference)
- [<span data-ttu-id="fd081-143">Azure .NET SDK</span><span class="sxs-lookup"><span data-stu-id="fd081-143">Azure .NET SDK</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Azure%20.NET%20SDk)
- [<span data-ttu-id="fd081-144">C# 指南</span><span class="sxs-lookup"><span data-stu-id="fd081-144">C# Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20C%23%20Guide)
- [<span data-ttu-id="fd081-145">桌面指南</span><span class="sxs-lookup"><span data-stu-id="fd081-145">Desktop Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Desktop%20Guide)
- [<span data-ttu-id="fd081-146">F# 指南</span><span class="sxs-lookup"><span data-stu-id="fd081-146">F# Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20F%23%20Guide)
- [<span data-ttu-id="fd081-147">ML.NET 指南</span><span class="sxs-lookup"><span data-stu-id="fd081-147">ML.NET Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20ML.NET%20Guide)
- <span data-ttu-id="fd081-148">[.NET 架構指南](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) - 可移除</span><span class="sxs-lookup"><span data-stu-id="fd081-148">[.NET Architecture Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) - Could be removed</span></span>
- [<span data-ttu-id="fd081-149">.NET Core 指南</span><span class="sxs-lookup"><span data-stu-id="fd081-149">.NET Core Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Core%20Guide)
- [<span data-ttu-id="fd081-150">適用於 Apache Spark 的 .NET 指南</span><span class="sxs-lookup"><span data-stu-id="fd081-150">.NET for Apache Spark Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20for%20Apache%20Spark%20Guide)
- [<span data-ttu-id="fd081-151">.NET Framework 指南</span><span class="sxs-lookup"><span data-stu-id="fd081-151">.NET Framework Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Framework%20Guide)
- [<span data-ttu-id="fd081-152">.NET 指南</span><span class="sxs-lookup"><span data-stu-id="fd081-152">.NET Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Guide)
- <span data-ttu-id="fd081-153">[Roslyn API 參照](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) - 可移除。</span><span class="sxs-lookup"><span data-stu-id="fd081-153">[Roslyn API Reference](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) - could be removed.</span></span>
- [<span data-ttu-id="fd081-154">Visual Basic 指南</span><span class="sxs-lookup"><span data-stu-id="fd081-154">Visual Basic Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Visual%20Basic%20Guide)

#### <a name="search-one-section-of-a-guide"></a><span data-ttu-id="fd081-155">搜尋指南的某個章節</span><span class="sxs-lookup"><span data-stu-id="fd081-155">Search one section of a guide</span></span>

<span data-ttu-id="fd081-156">![中藍色背景上的 :card_file_box:區域](./media/labels-projects/technology.png ".NET 指南子區域標籤的前置詞")</span><span class="sxs-lookup"><span data-stu-id="fd081-156">![:card_file_box: Area on medium blue background](./media/labels-projects/technology.png "Prefix for .NET Guide sub-area labels")</span></span>

<span data-ttu-id="fd081-157">.NET 指南很大，因此這些標籤會依指南章節進一步限制範圍。</span><span class="sxs-lookup"><span data-stu-id="fd081-157">The .NET guides are large, so these labels further limit the scope by a section of a guide.</span></span> <span data-ttu-id="fd081-158">每個 .NET 指南子區域會以 `:card_file_box: Technology` 前置詞來註明，並具有中藍色背景。</span><span class="sxs-lookup"><span data-stu-id="fd081-158">Each .NET Guide subarea is noted with the `:card_file_box: Technology` prefix and has a medium blue background.</span></span> <span data-ttu-id="fd081-159">這些標籤中有許多適用於多個指南，而其他標籤則只適用於一個指南。</span><span class="sxs-lookup"><span data-stu-id="fd081-159">Many of these labels apply to multiple guides, while others are in only one guide.</span></span> <span data-ttu-id="fd081-160">依區域篩選之後，請新增下列其中一個標籤，以進一步限制問題的範圍。</span><span class="sxs-lookup"><span data-stu-id="fd081-160">After filtering on an area, add one of these labels to further limit the scope of issues.</span></span>

- <span data-ttu-id="fd081-161">AppCompat</span><span class="sxs-lookup"><span data-stu-id="fd081-161">AppCompat</span></span>
- <span data-ttu-id="fd081-162">非同步工作</span><span class="sxs-lookup"><span data-stu-id="fd081-162">Async Task</span></span>
- <span data-ttu-id="fd081-163">C# 進階概念</span><span class="sxs-lookup"><span data-stu-id="fd081-163">C# Advanced concepts</span></span>
- <span data-ttu-id="fd081-164">C# 編譯器</span><span class="sxs-lookup"><span data-stu-id="fd081-164">C# compiler</span></span>
- <span data-ttu-id="fd081-165">C# 基礎</span><span class="sxs-lookup"><span data-stu-id="fd081-165">C# Fundamentals</span></span>
- <span data-ttu-id="fd081-166">C# 入門</span><span class="sxs-lookup"><span data-stu-id="fd081-166">C# Get Started</span></span>
- <span data-ttu-id="fd081-167">C# 語言參考</span><span class="sxs-lookup"><span data-stu-id="fd081-167">C# Language Reference</span></span>
- <span data-ttu-id="fd081-168">C# Null 安全</span><span class="sxs-lookup"><span data-stu-id="fd081-168">C# Null safety</span></span>
- <span data-ttu-id="fd081-169">C# 的新功能</span><span class="sxs-lookup"><span data-stu-id="fd081-169">C# What's new</span></span>
- <span data-ttu-id="fd081-170">CLI</span><span class="sxs-lookup"><span data-stu-id="fd081-170">CLI</span></span>
- <span data-ttu-id="fd081-171">資料存取</span><span class="sxs-lookup"><span data-stu-id="fd081-171">Data Access</span></span>
- <span data-ttu-id="fd081-172">Docker</span><span class="sxs-lookup"><span data-stu-id="fd081-172">Docker</span></span>
- <span data-ttu-id="fd081-173">安裝程式</span><span class="sxs-lookup"><span data-stu-id="fd081-173">Installers</span></span>
- <span data-ttu-id="fd081-174">LINQ</span><span class="sxs-lookup"><span data-stu-id="fd081-174">LINQ</span></span>
- <span data-ttu-id="fd081-175">NCL</span><span class="sxs-lookup"><span data-stu-id="fd081-175">NCL</span></span>
- <span data-ttu-id="fd081-176">.NET Standard</span><span class="sxs-lookup"><span data-stu-id="fd081-176">.NET Standard</span></span>
- <span data-ttu-id="fd081-177">Roslyn API</span><span class="sxs-lookup"><span data-stu-id="fd081-177">Roslyn APIs</span></span>
- <span data-ttu-id="fd081-178">安全性</span><span class="sxs-lookup"><span data-stu-id="fd081-178">Security</span></span>
- <span data-ttu-id="fd081-179">WCF</span><span class="sxs-lookup"><span data-stu-id="fd081-179">WCF</span></span>
- <span data-ttu-id="fd081-180">WF</span><span class="sxs-lookup"><span data-stu-id="fd081-180">WF</span></span>
- <span data-ttu-id="fd081-181">WIF</span><span class="sxs-lookup"><span data-stu-id="fd081-181">WIF</span></span>
- <span data-ttu-id="fd081-182">WinForms</span><span class="sxs-lookup"><span data-stu-id="fd081-182">WinForms</span></span>
- <span data-ttu-id="fd081-183">WPF</span><span class="sxs-lookup"><span data-stu-id="fd081-183">WPF</span></span>

### <a name="releases"></a><span data-ttu-id="fd081-184">版本</span><span class="sxs-lookup"><span data-stu-id="fd081-184">Releases</span></span>

<span data-ttu-id="fd081-185">![深黃色上的 :checkered_flag:Release:](./media/labels-projects/release.png "版本標籤的前置詞")</span><span class="sxs-lookup"><span data-stu-id="fd081-185">![:checkered_flag: Release: on dark yellow](./media/labels-projects/release.png "Prefix for release labels")</span></span>

<span data-ttu-id="fd081-186">針對特定版本標記的問題會以 `:checkered_flag: Release:` 前置詞來註明，並具有深黃色背景。</span><span class="sxs-lookup"><span data-stu-id="fd081-186">Issues tagged for a specific release are noted with the `:checkered_flag: Release:` prefix and have a dark yellow background.</span></span>

- <span data-ttu-id="fd081-187">.NET Core 2.2</span><span class="sxs-lookup"><span data-stu-id="fd081-187">.NET Core 2.2</span></span>
- <span data-ttu-id="fd081-188">.NET Core 3.0</span><span class="sxs-lookup"><span data-stu-id="fd081-188">.NET Core 3.0</span></span>
- <span data-ttu-id="fd081-189">.NET Framework 4.8</span><span class="sxs-lookup"><span data-stu-id="fd081-189">.NET Framework 4.8</span></span>
- <span data-ttu-id="fd081-190">.NET 5</span><span class="sxs-lookup"><span data-stu-id="fd081-190">.NET 5</span></span>

### <a name="priority"></a><span data-ttu-id="fd081-191">優先順序</span><span class="sxs-lookup"><span data-stu-id="fd081-191">Priority</span></span>

<span data-ttu-id="fd081-192">所有優先順序標籤都是 `P` 後面接著一位數。</span><span class="sxs-lookup"><span data-stu-id="fd081-192">Priority labels are all `P` followed by a single digit.</span></span> <span data-ttu-id="fd081-193">數字越低則表示優先順序越高：</span><span class="sxs-lookup"><span data-stu-id="fd081-193">Lower numbers are higher priority:</span></span>

- <span data-ttu-id="fd081-194">P0 - 指出具有重要優先順序的問題或 PR</span><span class="sxs-lookup"><span data-stu-id="fd081-194">P0 - Indicates issues or PRs that are critical priority</span></span>
- <span data-ttu-id="fd081-195">P1 - 高優先順序</span><span class="sxs-lookup"><span data-stu-id="fd081-195">P1 - High priority</span></span>
- <span data-ttu-id="fd081-196">P2 - 中優先順序</span><span class="sxs-lookup"><span data-stu-id="fd081-196">P2 - Medium priority</span></span>
- <span data-ttu-id="fd081-197">P3 - 低優先順序</span><span class="sxs-lookup"><span data-stu-id="fd081-197">P3 - Low priority</span></span>

### <a name="what-about-the-other-labels"></a><span data-ttu-id="fd081-198">那麼其他標籤呢</span><span class="sxs-lookup"><span data-stu-id="fd081-198">What about the other labels</span></span>

<span data-ttu-id="fd081-199">內容小組使用許多其他標籤來管理不同分類的問題。</span><span class="sxs-lookup"><span data-stu-id="fd081-199">There are many other labels used by the content teams to manage different classifications of issues.</span></span> <span data-ttu-id="fd081-200">如果您不在內容小組上，則可以忽略這些其他標籤。</span><span class="sxs-lookup"><span data-stu-id="fd081-200">If you're not on the content team, you can ignore these other labels.</span></span>

## <a name="projects"></a><span data-ttu-id="fd081-201">專案</span><span class="sxs-lookup"><span data-stu-id="fd081-201">Projects</span></span>

<span data-ttu-id="fd081-202">專案適用於規劃目的，其中具有較高優先順序的工作會透過工作流程看板自動化。</span><span class="sxs-lookup"><span data-stu-id="fd081-202">Projects are intended for planning purposes, where prioritized work is automated through a Kanban board.</span></span> <span data-ttu-id="fd081-203">專案只應該包含 GitHub 問題，而「非」提取要求。</span><span class="sxs-lookup"><span data-stu-id="fd081-203">Projects should only ever contain GitHub issues, _not_ pull requests.</span></span> <span data-ttu-id="fd081-204">專案與里程碑的不同之處，在於里程碑只會包含提取要求。</span><span class="sxs-lookup"><span data-stu-id="fd081-204">Projects differ from milestones, in that milestones only contain pull requests.</span></span>

<span data-ttu-id="fd081-205">我們透過兩種方式來使用專案：</span><span class="sxs-lookup"><span data-stu-id="fd081-205">We use projects in two ways:</span></span>

- <span data-ttu-id="fd081-206">`Month YYYY` 專案類型：這些是每月工作計畫的工作流程看板。</span><span class="sxs-lookup"><span data-stu-id="fd081-206">`Month YYYY` project types: These are Kanban boards for each month's working plan.</span></span>
  - <span data-ttu-id="fd081-207">例如 [2020 年 7 月](https://github.com/dotnet/docs/projects/103) \(英文\)、[2020 年 8 月](https://github.com/dotnet/docs/projects/117) \(英文\) 等等。</span><span class="sxs-lookup"><span data-stu-id="fd081-207">Examples, [July 2020](https://github.com/dotnet/docs/projects/103), [August 2020](https://github.com/dotnet/docs/projects/117), and so on.</span></span>
- <span data-ttu-id="fd081-208">長時間執行的 Epic：這些會在工作持續數個月時，用來管理工作達成目標的進度。</span><span class="sxs-lookup"><span data-stu-id="fd081-208">Long-running epics: These are used to organize tasks toward a goal when the work will occur over several months.</span></span>
  - <span data-ttu-id="fd081-209">範例：[.NET 5 Wave - 重新組織](https://github.com/dotnet/docs/projects/105) \(英文\)、[.NET 語言 (.NET 5 wave) ](https://github.com/dotnet/docs/projects/106) \(英文\) 等等。</span><span class="sxs-lookup"><span data-stu-id="fd081-209">Examples: [.NET 5 Wave - Reorganization](https://github.com/dotnet/docs/projects/105), [.NET Languages (.NET 5 wave) ](https://github.com/dotnet/docs/projects/106), and so on.</span></span>

## <a name="milestones"></a><span data-ttu-id="fd081-210">里程碑</span><span class="sxs-lookup"><span data-stu-id="fd081-210">Milestones</span></span>

<span data-ttu-id="fd081-211">里程碑通常會遵循與專案相同的命名慣例 (`Month YYYY`)，但其與專案不同。</span><span class="sxs-lookup"><span data-stu-id="fd081-211">Milestones typically follow the same naming convention of projects `Month YYYY`, but they're different from projects.</span></span> <span data-ttu-id="fd081-212">我們會使用里程碑來追蹤已完成的工作。</span><span class="sxs-lookup"><span data-stu-id="fd081-212">We use milestones to track completed work.</span></span> <span data-ttu-id="fd081-213">里程碑「不應該」包含問題 (潛在工作)，而只應包含提取要求。</span><span class="sxs-lookup"><span data-stu-id="fd081-213">Milestones should _not_ contain issues (potential work), but rather exclusively contain pull requests.</span></span> <span data-ttu-id="fd081-214">目前的里程碑會自動套用到新的提取要求。</span><span class="sxs-lookup"><span data-stu-id="fd081-214">The current milestone is automatically applied to new pull requests.</span></span>
