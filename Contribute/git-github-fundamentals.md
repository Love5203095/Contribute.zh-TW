---
title: 適用於文件的 Git 和 GitHub 基本資訊
description: 本文說明 Git、GitHub 存放庫和內容的組識方式，以及用於 docs.microsoft.com 之命名慣例的概觀。
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 06/30/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 5f7f90b69953e23833906202c739d2168b139d7e
ms.sourcegitcommit: 782b689882cce3ce07f5613763322989f2d0d63f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/05/2018
ms.locfileid: "34469478"
---
# <a name="git-and-github-essentials-for-docs"></a><span data-ttu-id="d01c6-103">適用於 Docs 的 Git 和 GitHub 基本資訊</span><span class="sxs-lookup"><span data-stu-id="d01c6-103">Git and GitHub essentials for Docs</span></span>

## <a name="overview"></a><span data-ttu-id="d01c6-104">概觀</span><span class="sxs-lookup"><span data-stu-id="d01c6-104">Overview</span></span>

<span data-ttu-id="d01c6-105">身為 Docs 內容的貢獻者，您將與多種工具和程序互動。</span><span class="sxs-lookup"><span data-stu-id="d01c6-105">As a contributor to Docs content, you will interact with multiple tools and processes.</span></span> <span data-ttu-id="d01c6-106">您會同時與其他貢獻者在相同專案上共同作業，而且甚至可能同時處理相同內容。</span><span class="sxs-lookup"><span data-stu-id="d01c6-106">You'll work in parallel with other contributors on the same project, potentially the exact same content, even at the same time.</span></span> <span data-ttu-id="d01c6-107">這一切都是透過 Git 和 GitHub 軟體來達成。</span><span class="sxs-lookup"><span data-stu-id="d01c6-107">This is all enabled through Git and GitHub software.</span></span>

<span data-ttu-id="d01c6-108">Git 是開放原始碼版本控制系統。</span><span class="sxs-lookup"><span data-stu-id="d01c6-108">Git is an open-source version control system.</span></span> <span data-ttu-id="d01c6-109">它透過「存放庫」中之檔案的「分散式版本控制」來促成此類型的專案共同作業。</span><span class="sxs-lookup"><span data-stu-id="d01c6-109">It facilitates this type of project collaboration through *distributed version control* of files that live in *repositories*.</span></span> <span data-ttu-id="d01c6-110">本質上來說，Git 可整合由多個參與者在不同時間，針對指定的存放庫所完成的工作流。</span><span class="sxs-lookup"><span data-stu-id="d01c6-110">In essence, Git makes it possible to integrate streams of work done by multiple contributors over time, for a given repository.</span></span>

<span data-ttu-id="d01c6-111">GitHub 是 Git 存放庫 (例如用來存放 [docs.microsoft.com](https://docs.microsoft.com) 內容的存放庫) 的 Web 型主機服務。</span><span class="sxs-lookup"><span data-stu-id="d01c6-111">GitHub is a web-based hosting service for Git repositories, such as those used to store [docs.microsoft.com](https://docs.microsoft.com) content.</span></span> <span data-ttu-id="d01c6-112">針對任何專案，GitHub 都裝載主要存放庫，供貢獻者針對其自己的工作建立複本</span><span class="sxs-lookup"><span data-stu-id="d01c6-112">For any project, GitHub hosts the main repository, from which contributors can make copies for their own work.</span></span>

## <a name="git"></a><span data-ttu-id="d01c6-113">Git</span><span class="sxs-lookup"><span data-stu-id="d01c6-113">Git</span></span>

<span data-ttu-id="d01c6-114">若您熟悉集中式版本控制系統 (例如 Team Foundation Server、SharePoint 或 Visual SourceSafe)，您將注意到 Git 擁有可支援其分散式模型的唯一貢獻工作流程與術語。</span><span class="sxs-lookup"><span data-stu-id="d01c6-114">If you're familiar with centralized version control systems (such as Team Foundation Server, SharePoint, or Visual SourceSafe), you will notice that Git has a unique contribution workflow and terminology to support its distributed model.</span></span> <span data-ttu-id="d01c6-115">例如，它並沒有通常會與簽出/簽入作業一起出現的檔案鎖定功能。</span><span class="sxs-lookup"><span data-stu-id="d01c6-115">For instance, there is no file locking that is normally associated with check-out/check-in operations.</span></span> <span data-ttu-id="d01c6-116">事實上，Git 所關心的是更精細層級中的變更，因此會進行逐位元組檔案比較。</span><span class="sxs-lookup"><span data-stu-id="d01c6-116">As a matter of fact, Git is concerned about changes at an even finer level, comparing files byte by byte.</span></span>

<span data-ttu-id="d01c6-117">Git 也使用分層結構來儲存及管理專案內容：</span><span class="sxs-lookup"><span data-stu-id="d01c6-117">Git also uses a tiered structure to store and manage content for a project:</span></span>

- <span data-ttu-id="d01c6-118">*存放庫*：亦稱為 *repo*，這是最高的儲存單位。</span><span class="sxs-lookup"><span data-stu-id="d01c6-118">*Repository*: Also known as a *repo*, this is the highest unit of storage.</span></span> <span data-ttu-id="d01c6-119">存放庫包含一或多個分支。</span><span class="sxs-lookup"><span data-stu-id="d01c6-119">A repository contains one or more branches.</span></span>
- <span data-ttu-id="d01c6-120">*分支*：包含組成專案內容集合之檔案與資料夾的儲存單位。</span><span class="sxs-lookup"><span data-stu-id="d01c6-120">*Branch*: A unit of storage that contains the files and  folders that make up a project's content set.</span></span> <span data-ttu-id="d01c6-121">分支會分隔工作串流 (通常稱為版本)。</span><span class="sxs-lookup"><span data-stu-id="d01c6-121">Branches separate streams of work (typically referred to as versions).</span></span> <span data-ttu-id="d01c6-122">貢獻一律是在特定分支的範圍所進行。</span><span class="sxs-lookup"><span data-stu-id="d01c6-122">Contributions are always made and scoped to a specific branch.</span></span> <span data-ttu-id="d01c6-123">所有存放庫都包含預設分支 (通常命名為 "master") 以及一或多個目的是合併回主分支的分支。</span><span class="sxs-lookup"><span data-stu-id="d01c6-123">All repositories contain a default branch (typically named "master") and one or more branches that are destined to be merged back into the master branch.</span></span> <span data-ttu-id="d01c6-124">主分支是做為最新版本使用，而且是專案的「單一信任來源」。</span><span class="sxs-lookup"><span data-stu-id="d01c6-124">The master branch serves as the current version and "single source of truth" for the project.</span></span> <span data-ttu-id="d01c6-125">它是存放庫中所有其他分支的建立來源。</span><span class="sxs-lookup"><span data-stu-id="d01c6-125">It's the parent from which all other branches in the repository are created.</span></span>

<span data-ttu-id="d01c6-126">參與者會與 Git 互動，以在本機和 GitHub 層級對存放庫進行更新和操作：</span><span class="sxs-lookup"><span data-stu-id="d01c6-126">Contributors interact with Git to update and manipulate repositories at both the local and GitHub levels:</span></span>

- <span data-ttu-id="d01c6-127">於本機透過如 Git Bash 主控台等工具。Git Bash 主控台支援用來管理本機存放庫和與 GitHub 存放庫通訊的 Git 命令</span><span class="sxs-lookup"><span data-stu-id="d01c6-127">Locally through tools such as the Git Bash console, which supports Git commands for managing local repositories and communicating with GitHub repositories</span></span>
- <span data-ttu-id="d01c6-128">透過 [www.github.com](https://www.github.com)。該網站整合了 Git，以管理協調流回主要存放庫的參與</span><span class="sxs-lookup"><span data-stu-id="d01c6-128">Via [www.github.com](https://www.github.com), which integrates Git to manage the reconciliation of contributions that flow back into the main repository</span></span>

## <a name="github"></a><span data-ttu-id="d01c6-129">GitHub</span><span class="sxs-lookup"><span data-stu-id="d01c6-129">GitHub</span></span>

> [!NOTE]
> <span data-ttu-id="d01c6-130">雖然 Docs 指導方針是以使用 GitHub 為基礎，某些小組會使用 Visual Studio Team Service 來裝載 Git 存放庫。</span><span class="sxs-lookup"><span data-stu-id="d01c6-130">Although Docs guidance is based on using GitHub, some teams use Visual Studio Team Services to host Git repositories.</span></span> <span data-ttu-id="d01c6-131">Visual Studio Team Explorer 用戶端提供用來與 Team Services 存放庫互動的 GUI，做為透過命令列使用 Git 命令之外的替代方法。</span><span class="sxs-lookup"><span data-stu-id="d01c6-131">The Visual Studio Team Explorer client provides a GUI for interacting with Team Services repositories, as an alternative to using Git commands through a command line.</span></span>
> </br>
> <span data-ttu-id="d01c6-132">此外，下列許多指導方針都是透過多年來在 GitHub 中裝載 Azure 服務內容的經驗發展而來的最佳做法。</span><span class="sxs-lookup"><span data-stu-id="d01c6-132">Also, many of the following guidelines were developed as best practices from years of experience in hosting Azure service content in GitHub.</span></span> <span data-ttu-id="d01c6-133">它們某些 Docs 存放庫中可能為必要做法。</span><span class="sxs-lookup"><span data-stu-id="d01c6-133">They might be required in some Docs repositories.</span></span>

<span data-ttu-id="d01c6-134">所有的工作流程都是在 GitHub 層級開始與結束，這也是任何 Doc 專案主要存放庫的儲存位置。</span><span class="sxs-lookup"><span data-stu-id="d01c6-134">All workflows begin and end at the GitHub level, where the main repository for any Docs project is stored.</span></span> <span data-ttu-id="d01c6-135">參與者為自己的使用目的而建立的複本會跨多部電腦散佈。</span><span class="sxs-lookup"><span data-stu-id="d01c6-135">The copies that contributors create for their own use are distributed across multiple computers.</span></span> <span data-ttu-id="d01c6-136">這些複本最終會協調回專案的主要 GitHub 存放庫。</span><span class="sxs-lookup"><span data-stu-id="d01c6-136">These copies are eventually reconciled back into the project's main GitHub repository.</span></span>

### <a name="directory-organization"></a><span data-ttu-id="d01c6-137">目錄組織方式</span><span class="sxs-lookup"><span data-stu-id="d01c6-137">Directory organization</span></span>

<span data-ttu-id="d01c6-138">如同先前所提到的，專案的預設/主分支會作為專案內容的最新版本。</span><span class="sxs-lookup"><span data-stu-id="d01c6-138">As mentioned earlier, a project's default/master branch serves as the current version of content for the project.</span></span> <span data-ttu-id="d01c6-139">主分支中的內容 (以及從它建立的分支) 會約略符合對應 Docs 頁面上文章的組織方式。</span><span class="sxs-lookup"><span data-stu-id="d01c6-139">The content in the master branch--and branches created from it--is loosely aligned with the organization of the articles on the corresponding Docs pages.</span></span> <span data-ttu-id="d01c6-140">系統會使用子目錄來區隔內容 (例如服務)、媒體內容 (例如影像檔案)，以及可讓內容重複使用的 "include" 檔案。</span><span class="sxs-lookup"><span data-stu-id="d01c6-140">Subdirectories are used for separation of like content (such as services), media content (such as image files), and "include" files (which enable reuse of content).</span></span>

<span data-ttu-id="d01c6-141">您通常可以在存放庫的根目錄找到主要 `articles` 目錄。</span><span class="sxs-lookup"><span data-stu-id="d01c6-141">You can typically find a main `articles` directory off the root of the repository.</span></span> <span data-ttu-id="d01c6-142">articles 目錄包含一組子目錄。</span><span class="sxs-lookup"><span data-stu-id="d01c6-142">The articles directory contains a set of subdirectories.</span></span> <span data-ttu-id="d01c6-143">子目錄中的文章格式為 Markdown 檔案，其副檔名為 *.md*。</span><span class="sxs-lookup"><span data-stu-id="d01c6-143">Articles in the subdirectories are formatted as Markdown files that use an *.md* extension.</span></span> <span data-ttu-id="d01c6-144">某些支援多個服務的存放庫會使用一般的 `/articles` 子目錄，例如 [https://github.com/microsoft/Azure-Docs](https://github.com/microsoft/Azure-Docs) 存放庫。</span><span class="sxs-lookup"><span data-stu-id="d01c6-144">Some repositories that support multiple services use a generic `/articles` subdirectory, such as the [https://github.com/microsoft/Azure-Docs](https://github.com/microsoft/Azure-Docs) repository.</span></span> <span data-ttu-id="d01c6-145">其他存放庫可能會使用服務特定的名稱，例如 [https://github.com/microsoft/IntuneDocs](https://github.com/microsoft/IntuneDocs) 存放庫是使用 `/IntuneDocs`。</span><span class="sxs-lookup"><span data-stu-id="d01c6-145">Others might use a service-specific name, such as the [https://github.com/microsoft/IntuneDocs](https://github.com/microsoft/IntuneDocs) repository, which uses `/IntuneDocs`.</span></span>

<span data-ttu-id="d01c6-146">在此目錄的根內，您可以找到有關整體服務或產品的一般文章。</span><span class="sxs-lookup"><span data-stu-id="d01c6-146">Within the root of this directory, you can find general articles that relate to the overall service or product.</span></span> <span data-ttu-id="d01c6-147">您通常也可以接著找到另一系列的子目錄，這些子目錄會符合功能/服務或常見案例。</span><span class="sxs-lookup"><span data-stu-id="d01c6-147">And typically, you can then find another series of subdirectories that match the features/services or common scenarios.</span></span> <span data-ttu-id="d01c6-148">例如，Azure "virtual machine" (虛擬機器) 文章是位於 `/virtual-machines` 子目錄，而 Intune "understand and explore" (了解與探索) 文章則位於 `/understand-explore` 子目錄。</span><span class="sxs-lookup"><span data-stu-id="d01c6-148">For instance, Azure "virtual machine" articles are in the `/virtual-machines` subdirectory, and Intune "understand and explore" articles are in the `/understand-explore` subdirectory.</span></span>

### <a name="media-subdirectory"></a><span data-ttu-id="d01c6-149">Media 子目錄</span><span class="sxs-lookup"><span data-stu-id="d01c6-149">Media subdirectory</span></span>

<span data-ttu-id="d01c6-150">每個 article 目錄都包含對應之媒體檔案的 `/media` 子目錄。</span><span class="sxs-lookup"><span data-stu-id="d01c6-150">Each article directory contains a `/media` subdirectory for corresponding media files.</span></span> <span data-ttu-id="d01c6-151">媒體檔案包含具有影像參考之文章所使用的影像。</span><span class="sxs-lookup"><span data-stu-id="d01c6-151">Media files contain images used by articles that have image references.</span></span>

### <a name="includes-subdirectory"></a><span data-ttu-id="d01c6-152">Includes 子目錄</span><span class="sxs-lookup"><span data-stu-id="d01c6-152">Includes subdirectory</span></span>

<span data-ttu-id="d01c6-153">只要有兩篇或多篇文章共用的可重複使用內容，系統就會將它放置在主要 `articles` 目錄的 `/includes` 子目錄中。</span><span class="sxs-lookup"><span data-stu-id="d01c6-153">Whenever we have reusable content that is shared across two or more articles, it is placed in an `/includes` subdirectory off the main `articles` directory.</span></span> <span data-ttu-id="d01c6-154">在使用 include 檔案的 Markdown 檔案中，系統會將對應的 "include" Markdown 擴充功能放置在需要參考 include 檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="d01c6-154">In a Markdown file that uses the include file, a corresponding "include" Markdown extension is placed in the location where the include file needs to be referenced.</span></span>

<span data-ttu-id="d01c6-155">如需額外的指導方針，請參閱[如何使用 Markdown： Include](how-to-write-use-markdown.md#includes)。</span><span class="sxs-lookup"><span data-stu-id="d01c6-155">See [How to use Markdown: Includes](how-to-write-use-markdown.md#includes) for additional guidance.</span></span>

### <a name="markdown-file-template"></a><span data-ttu-id="d01c6-156">Markdown 檔案範本</span><span class="sxs-lookup"><span data-stu-id="d01c6-156">Markdown file template</span></span>

<span data-ttu-id="d01c6-157">為了方便起見，每個存放庫的根目錄通常包含一個名為 `template.md` 的 Markdown 檔案。</span><span class="sxs-lookup"><span data-stu-id="d01c6-157">For convenience, the root directory of each repository typically contains a Markdown template file named `template.md`.</span></span> <span data-ttu-id="d01c6-158">若需要建立新文章以提交到存放庫，您可以將此範本檔案做為「開始檔案」使用。</span><span class="sxs-lookup"><span data-stu-id="d01c6-158">You can use this template file as a "starter file" if you need to create a new article for submission to the repository.</span></span> <span data-ttu-id="d01c6-159">該檔案包含︰</span><span class="sxs-lookup"><span data-stu-id="d01c6-159">The file contains:</span></span>

- <span data-ttu-id="d01c6-160">檔案頂端的**中繼資料標頭**其中包含兩個具有 3 個破折號的行。</span><span class="sxs-lookup"><span data-stu-id="d01c6-160">A **metadata header** at the top of the file, delineated by two, 3-hyphen lines.</span></span> <span data-ttu-id="d01c6-161">它包含用於與文章相關之追蹤資訊的多種標記。</span><span class="sxs-lookup"><span data-stu-id="d01c6-161">It contains the various tags used for tracking information related to the article.</span></span> <span data-ttu-id="d01c6-162">文章中繼資料可啟用特定功能，例如作者姓名標示、參與者姓名標示、階層連結與文章描述。</span><span class="sxs-lookup"><span data-stu-id="d01c6-162">Article metadata enables certain functionality, such as author attribution, contributor attribution, breadcrumbs, and article descriptions.</span></span> <span data-ttu-id="d01c6-163">它也包括 SEO 最佳化與報告程序，Microsoft 使用它們來評估內容的成效。</span><span class="sxs-lookup"><span data-stu-id="d01c6-163">It also includes SEO optimizations and reporting processes that Microsoft uses to evaluate the performance of the content.</span></span> <span data-ttu-id="d01c6-164">因此，中繼資料非常重要！</span><span class="sxs-lookup"><span data-stu-id="d01c6-164">So the metadata is important!</span></span>
- <span data-ttu-id="d01c6-165">能描述各種中繼資料標記和值的**中繼資料**區段。</span><span class="sxs-lookup"><span data-stu-id="d01c6-165">A **metadata section** that describes the various metadata tags and values.</span></span> <span data-ttu-id="d01c6-166">如果您不確定在中繼資料區段中應使用的值，則可以留白，或在前面加上雜湊標記 (#) 使其成為註解，讓存放庫的提取要求檢閱者來檢閱/完成它們。</span><span class="sxs-lookup"><span data-stu-id="d01c6-166">If you're unsure of the values to use for the metadata section, you can leave them blank or comment them with a leading hashtag (#), and they will be reviewed/completed by the pull request reviewer for the repository.</span></span>
- <span data-ttu-id="d01c6-167">各種使用「Markdown 來格式化文章元素的範例」。</span><span class="sxs-lookup"><span data-stu-id="d01c6-167">Various **examples of using Markdown** to format the elements of an article.</span></span>
- <span data-ttu-id="d01c6-168">一般的**Markdown 擴充功能使用指示**，可用於各種類型的警示。</span><span class="sxs-lookup"><span data-stu-id="d01c6-168">General **instructions on the use of Markdown extensions**, which you can use for various types of alerts.</span></span>
- <span data-ttu-id="d01c6-169">使用 iframe **內嵌視訊**的範例。</span><span class="sxs-lookup"><span data-stu-id="d01c6-169">Examples of **embedding video** by using an iframe.</span></span>
- <span data-ttu-id="d01c6-170">一般**docs.microsoft.com 擴充功能使用指示**，您可以將其用於特殊控制項，例如按鈕與選取器。</span><span class="sxs-lookup"><span data-stu-id="d01c6-170">General **instructions on the use of docs.microsoft.com extensions**, which you can use for special controls such as buttons and selectors.</span></span>

## <a name="pull-requests"></a><span data-ttu-id="d01c6-171">提取要求</span><span class="sxs-lookup"><span data-stu-id="d01c6-171">Pull requests</span></span>

<span data-ttu-id="d01c6-172">「提取要求」為讓參與者建議要套用至預設分支之一系列變更的便利方式。</span><span class="sxs-lookup"><span data-stu-id="d01c6-172">A *pull request* provides a convenient way for a contributor to propose a set of changes that will be applied to the default branch.</span></span> <span data-ttu-id="d01c6-173">變更 (亦稱為「認可」) 會儲存在參與者的分支中，讓 GitHub 可先模擬將它們「合併」至預設分支後所會帶來的影響。</span><span class="sxs-lookup"><span data-stu-id="d01c6-173">The changes (also known as *commits*) are stored in a contributor's branch, so GitHub can first model the impact of *merging* them into the default branch.</span></span> <span data-ttu-id="d01c6-174">提取要求也可作為提供參與者來自建置/驗證流程、提取要求檢閱者之意見反應的機制，以在變更合併至預設分支之前解決可能發生的問題。</span><span class="sxs-lookup"><span data-stu-id="d01c6-174">A pull request also serves as a mechanism to provide the contributor with feedback from a build/validation process, the pull request reviewer, to resolve potential issues or questions before the changes are merged into the default branch.</span></span>

<span data-ttu-id="d01c6-175">有兩種方式可透過提取要求來做出貢獻，這取決於您要建議之變更的大小。</span><span class="sxs-lookup"><span data-stu-id="d01c6-175">There are two ways to contribute by pull request, depending on the size of changes that you want to propose.</span></span> <span data-ttu-id="d01c6-176">我們稍後會在本指南的 [GitHub 工作流程](how-to-write-workflows-major.md)小節中詳細說明這一部分。</span><span class="sxs-lookup"><span data-stu-id="d01c6-176">We will cover this in detail later, in the [GitHub workflow](how-to-write-workflows-major.md) section of this guide.</span></span>

<!---- Reference links for Docs landing pages, associated GitHub repositories, and related Forums matrix. ------------------>
<!---- PLEASE INSERT URLS IN ASCENDING SORT ORDER, AND REMOVE LOCALE SEGMENT FROM URLS (that is, en-us) FOR LOCALIZED FORUMS! -->
<!---- NOTE: these links are saved for future use in another/new article; no longer used above in this article --->
[Visual-Studio-Page]:(https://docs.microsoft.com/en-us/visualstudio/index)
[Visual-Studio-Repo-Internal]:(https://github.com/Microsoft/vsdocs)
[Visual-Studio-Repo-External]:(https://github.com/Microsoft/visualstudio-docs)
[Visual-Studio-SO]: (https://stackoverflow.com/search?q=Visual+Studio+2017)
[Dotnet-Page]: https://docs.microsoft.com/dotnet
[Dotnet-Core-Page]: https://docs.microsoft.com/dotnet/articles/welcome
[Dotnet-Core-Repo]: https://github.com/dotnet/docs
[EM-ATA-Land]: https://docs.microsoft.com/advanced-threat-analytics/
[EM-ATA-Repo]: https://github.com/Microsoft/ATADocs
[EM-AzureAD-Land]: https://docs.microsoft.com/active-directory/
[EM-AzureAD-Repo]: https://github.com/Azure/azure-content/tree/master/articles/active-directory/
[EM-AzureRMS-Land]: https://docs.microsoft.com/rights-management/
[EM-AzureRMS-Repo]: https://github.com/Microsoft/Azure-RMSDocs
[EM-Intune-Land]: https://docs.microsoft.com/intune/
[EM-Intune-Repo]: https://github.com/microsoft/intuneDocs
[EM-Land-Page]: https://docs.microsoft.com/enterprise-mobility/
[EM-Land-Repo]: https://github.com/Microsoft/EMDocs/
[EM-MFA-Land]: https://docs.microsoft.com/multi-factor-authentication/
[EM-MFA-Repo]: https://github.com/Azure/azure-content/tree/master/articles/multi-factor-authentication
[EM-MIM-Land]: https://docs.microsoft.com/microsoft-identity-manager/
[EM-MIM-Repo]: https://github.com/Microsoft/MIMDocs
[EM-RemoteApp-Land]: https://docs.microsoft.com/en-us/remoteapp/
[EM-RemoteApp-Repo]: https://github.com/Azure/azure-content/tree/master/articles/remoteapp
[Forum-MSDN-ATA]: https://social.technet.microsoft.com/Forums/en-US/home?forum=mata
[Forum-MSDN-AzureAD]: https://social.msdn.microsoft.com/Forums/en-US/home?forum=WindowsAzureAD
[Forum-MSDN-AzureRMS]: https://social.technet.microsoft.com/Forums/en-US/home?forum=rmsapps%2Crmscloud&filter=alltypes&sort=lastpostdesc
[Forum-MSDN-EM]: https://social.technet.microsoft.com/Forums/en-US/home?sort=relevancedesc&brandIgnore=True&searchTerm=Enterprise+Mobility
[Forum-MSDN-Intune]: https://social.technet.microsoft.com/Forums/en-us/home?category=microsoftintune
[Forum-MSDN-Main]: https://social.msdn.microsoft.com/Forums/home
[Forum-MSDN-MFA]: https://social.msdn.microsoft.com/Forums/en-US/home?forum=windowsazureactiveauthentication
[Forum-MSDN-MIM]: https://social.technet.microsoft.com/Forums/en-US/home?category=identitymanagement
[Forum-MSDN-RemoteApp]: https://social.technet.microsoft.com/Forums/en-US/home?filter=alltypes&brandIgnore=True&sort=relevancedesc&searchTerm=Azure+Remote+or+RemoteApp
[Forum-SO-AzureAD]: https://stackoverflow.com/questions/tagged/azure-active-directory
[Forum-SO-AzureRMS]: https://stackoverflow.com/questions/tagged/rights-management
[Forum-SO-Dotnet]: https://stackoverflow.com/questions/tagged/.net
[Forum-SO-Dotnet-Core]: https://stackoverflow.com/questions/tagged/.net-core
[Forum-SO-Main]: https://stackoverflow.com/tags
[Forum-SO-Intune]: https://stackoverflow.com/questions/tagged/intune
[Forum-SO-MFA]: https://stackoverflow.com/search?q=%5Bazure%5D+multi-factor
[Forum-SO-MIM]: https://stackoverflow.com/search?q=Microsoft+Identity+Manager
[Forum-SO-RemoteApp]: https://stackoverflow.com/questions/tagged/remoteapp
[Forum-TechNet-Main]: https://social.technet.microsoft.com/Forums/home
[Forum-Yammer-AzureRMS]: https://www.yammer.com/AskIPTeam
[Forum-Yammer-Main]: https://www.yammer.com/
