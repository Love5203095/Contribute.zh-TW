---
title: 安裝內容撰寫工具
description: 本文可協助您下載與安裝使用 Git 與編輯 Markdown 檔案所需的用戶端工具。
author: jasonwhowell
ms.author: jasonh
manager: kfile
ms.date: 04/30/2018
ms.openlocfilehash: 9f22a416810711c076645a9483f022112a3a7642
ms.sourcegitcommit: 886ca76086a302d1d6124967df12a5bcfe4fd4b5
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/10/2018
ms.locfileid: "40251444"
---
# <a name="install-content-authoring-tools"></a><span data-ttu-id="6ef8d-103">安裝內容撰寫工具</span><span class="sxs-lookup"><span data-stu-id="6ef8d-103">Install content authoring tools</span></span>

<span data-ttu-id="6ef8d-104">本文說明以互動方式安裝 Git 用戶端工具和 Visual Studio Code 的步驟。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-104">This article describes the steps to interactively install Git client tools and Visual Studio Code.</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="6ef8d-105">安裝 [Git](https://git-scm.com/)</span><span class="sxs-lookup"><span data-stu-id="6ef8d-105">Install [Git](https://git-scm.com/)</span></span>
> * <span data-ttu-id="6ef8d-106">安裝 [Visual Studio Code](https://code.visualstudio.com/)</span><span class="sxs-lookup"><span data-stu-id="6ef8d-106">Install [Visual Studio Code](https://code.visualstudio.com/)</span></span>
> * <span data-ttu-id="6ef8d-107">安裝 [Docs 編寫套件](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="6ef8d-107">Install [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)</span></span>

>[!IMPORTANT]
> <span data-ttu-id="6ef8d-108">若只是要對文章進行很少量的變更，*不*需要完成此文章中的步驟，而可繼續直接進入[快速變更工作流程](index.md#quick-edits-to-existing-documents)。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-108">If you're making only minor changes to an article, you *do not* need to complete the steps in this article and can continue directly to the [quick changes workflow](index.md#quick-edits-to-existing-documents).</span></span>
>
> <span data-ttu-id="6ef8d-109">我們建議主要參與者完成這些步驟，因為這可讓您使用[主要/長期變更工作流程](how-to-write-workflows-major.md)。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-109">Major contributors are encouraged to complete these steps, which enable you to use the [major/long-running changes workflow](how-to-write-workflows-major.md).</span></span> <span data-ttu-id="6ef8d-110">即使您在主要存放庫中具有寫入權限，仍然*強烈建議您 (且此指南假設您會) 對存放庫進行派生和複製*，這樣您會具有在分支中儲存所建議變更的讀取/寫入權限。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-110">Even if you have write permissions in the main repository, *we highly recommend (and this guide assumes) that you fork and clone the repository*, so that you have read/write permissions to store your proposed changes in your fork.</span></span>

## <a name="install-git-client-tools"></a><span data-ttu-id="6ef8d-111">安裝 Git 用戶端工具</span><span class="sxs-lookup"><span data-stu-id="6ef8d-111">Install Git client tools</span></span> 

 <span data-ttu-id="6ef8d-112">安裝適用於您平台的 [Software Freedom Conservancy 的 Git 用戶端工具](https://git-scm.com/download/)最新版本。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-112">Install the latest version of [Software Freedom Conservancy's Git client tools](https://git-scm.com/download/) for your platform.</span></span> 

* <span data-ttu-id="6ef8d-113">[適用於 Windows 的 Git](https://git-scm.com/download/win)。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-113">[Git for Windows](https://git-scm.com/download/win).</span></span> <span data-ttu-id="6ef8d-114">安裝包含了 Git 版本控制系統和 Git Bash，您可以使用此命令列應用程式來與本機 Git 存放庫互動。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-114">This install includes the Git version control system and Git Bash, the command-line app that you use to interact with your local Git repository.</span></span>
* <span data-ttu-id="6ef8d-115">適用於 Mac 的 Git 是隨著 Xcode 命令列工具提供。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-115">Git for Mac is provided as part of the Xcode Command Line Tools.</span></span> <span data-ttu-id="6ef8d-116">只要從命令列執行 `git`。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-116">Simply run `git` from the command line.</span></span> <span data-ttu-id="6ef8d-117">系統將會提示您視需要安裝該命令列工具。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-117">You will be prompted to install the command line tools if needed.</span></span> <span data-ttu-id="6ef8d-118">您也可以從 Software Freedom Conservancy 下載[適用於 Mac 的 Git](https://git-scm.com/download/mac)。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-118">You can also download [Git for Mac](https://git-scm.com/download/mac) from the Software Freedom Conservancy.</span></span>
* [<span data-ttu-id="6ef8d-119">適用於 Linux 與 Unix 的 Git</span><span class="sxs-lookup"><span data-stu-id="6ef8d-119">Git for Linux and Unix</span></span>](https://git-scm.com/download/linux)

<span data-ttu-id="6ef8d-120">如果您較偏好圖形化使用者介面 (GUI) 而非命令列介面 (CLI)，請參閱 [Software Freedom Conservancy 的可用 GUI 用戶端頁面](https://git-scm.com/downloads/guis) \(英文\)、[GitHub 的 GitHub 電腦版](https://desktop.github.com/)+ \(英文\)，或 [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx) \(英文\) 以取得一些較受歡迎的選項。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-120">If you prefer a graphical user interface (GUI) over a command-line interface (CLI), see [Software Freedom Conservancy's available GUI Clients page](https://git-scm.com/downloads/guis), [GitHub's GitHub Desktop](https://desktop.github.com/), or [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx) for some popular options.</span></span>

<span data-ttu-id="6ef8d-121">請遵循您所選擇用戶端的指示，以進行安裝與設定。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-121">Follow the instructions for your chosen client for installation and configuration.</span></span>

<span data-ttu-id="6ef8d-122">在下一篇文章中，您將[設定本機 Git 存放庫](get-started-setup-local.md)。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-122">In the next article, you will [Set up a local Git repository](get-started-setup-local.md).</span></span>

   <span data-ttu-id="6ef8d-123">其他的 Git 資源可在此處取得：[Git 術語](https://help.github.com/articles/github-glossary) | [Git 基本概念](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [學習 Git 與 GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)</span><span class="sxs-lookup"><span data-stu-id="6ef8d-123">Additional Git resources are available here: [Git terminology](https://help.github.com/articles/github-glossary) | [Git basics](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Learning Git and GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)</span></span>

## <a name="understand-markdown-editors"></a><span data-ttu-id="6ef8d-124">了解 Markdown 編輯器</span><span class="sxs-lookup"><span data-stu-id="6ef8d-124">Understand Markdown editors</span></span>

<span data-ttu-id="6ef8d-125">Markdown 是一種容易閱讀及學習的輕量型標記語言。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-125">Markdown is a lightweight markup language that is both easy to read and easy to learn.</span></span> <span data-ttu-id="6ef8d-126">因此，它快速地成為業界標準。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-126">Therefore, it has rapidly become an industry standard.</span></span> <span data-ttu-id="6ef8d-127">若要以 Markdown 撰寫文章，建議您先下載並安裝 Markdown 編輯器。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-127">To write articles in Markdown, we recommend that you first download and install a Markdown editor.</span></span>  <span data-ttu-id="6ef8d-128">[Visual Studio Code](https://code.visualstudio.com/) 是 Microsoft 用來編輯 Markdown 的偏好工具。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-128">[Visual Studio Code](https://code.visualstudio.com/) is the preferred tool for editing Markdown at Microsoft.</span></span> <span data-ttu-id="6ef8d-129">[Atom](https://atom.io) 是另一個用來編輯 Markdown 的熱門工具。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-129">[Atom](https://atom.io) is another popular tool for editing Markdown.</span></span>

<span data-ttu-id="6ef8d-130">Markdown 文字會儲存到副檔名為 .md 的檔案中。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-130">Markdown text is saved into files with .md extension.</span></span>

<span data-ttu-id="6ef8d-131">關於如何使用 Markdown 撰寫的其他詳細資料，包括 Markdown 基本概念及 OPS 自訂 Markdown 擴充功能所支援的功能，都會在稍後的[如何使用 Markdown](how-to-write-use-markdown.md) 文章中涵蓋。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-131">Additional details on how to write with Markdown, including Markdown basics and the features supported by OPS custom Markdown extensions, are covered later in the [How to use Markdown](how-to-write-use-markdown.md) article.</span></span>

## <a name="visual-studio-code"></a><span data-ttu-id="6ef8d-132">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="6ef8d-132">Visual Studio Code</span></span>

<span data-ttu-id="6ef8d-133">[Visual Studio Code](https://code.visualstudio.com/) 也稱為 VS Code，是一種輕量型編輯器，適用於 Windows、Linux 和 Mac。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-133">[Visual Studio Code](https://code.visualstudio.com/), also known as VS Code, is a lightweight editor that works on Windows, Linux, and Mac.</span></span> <span data-ttu-id="6ef8d-134">它包含 Git 整合，並支援擴充功能。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-134">It includes git integration, and support for extensions.</span></span>

<span data-ttu-id="6ef8d-135">下載並安裝 [VS Code](https://code.visualstudio.com/)。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-135">Download and install [VS Code](https://code.visualstudio.com/).</span></span> <span data-ttu-id="6ef8d-136">VS Code 首頁應該會正確地偵測到您的作業系統。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-136">The VS Code home page should detect your operating system correctly.</span></span>

- [<span data-ttu-id="6ef8d-137">Windows</span><span class="sxs-lookup"><span data-stu-id="6ef8d-137">Windows</span></span>](https://code.visualstudio.com/docs/setup/windows)
- [<span data-ttu-id="6ef8d-138">Mac</span><span class="sxs-lookup"><span data-stu-id="6ef8d-138">Mac</span></span>](https://code.visualstudio.com/docs/setup/mac)
- [<span data-ttu-id="6ef8d-139">Linux</span><span class="sxs-lookup"><span data-stu-id="6ef8d-139">Linux</span></span>](https://code.visualstudio.com/docs/setup/linux)

> [!TIP]
> <span data-ttu-id="6ef8d-140">若要啟動 VS Code 並開啟目前的資料夾，請在命令列或 bash 殼層中執行 `code .` 命令。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-140">To launch VS Code and open the current folder, run the command `code .` in the command line or bash shell.</span></span> <span data-ttu-id="6ef8d-141">如果目前的資料夾為本機 Git 存放庫的一部分，則 Github 整合會自動在 Visual Studio Code 中顯示。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-141">If the current folder is part of a local git repo, the github integration appears in Visual Studio Code automatically.</span></span>

## <a name="docs-authoring-pack"></a><span data-ttu-id="6ef8d-142">Docs 編寫套件</span><span class="sxs-lookup"><span data-stu-id="6ef8d-142">Docs Authoring Pack</span></span>
<span data-ttu-id="6ef8d-143">安裝適用於 Visual Studio Code 的 Docs 編寫套件。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-143">Install the Docs Authoring Pack for Visual Studio Code.</span></span> <span data-ttu-id="6ef8d-144">此延伸模組集包括撰寫 Markdown 時的基本編寫協助，以及可讓您能以 docs.microsoft.com 網站的樣式查看 Markdown 外觀的預覽功能。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-144">This set of extensions includes basic authoring assistance for help when writing Markdown, and a preview feature, so that you can see what the Markdown looks like in the style of the docs.microsoft.com site.</span></span>

   <span data-ttu-id="6ef8d-145">請造訪此[市集頁面](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) \(英文\) 並選取 [Install] \(安裝\)，或在 VS Code 視窗的延伸模組清單中搜尋 `docsmsft.docs-authoring-pack`。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-145">Visit this [marketplace page](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) and select **Install**, or search for `docsmsft.docs-authoring-pack` in your extensions list in the VS Code window.</span></span> 

   <span data-ttu-id="6ef8d-146">Docs 編寫套件可透過在 VS Code 內按 Alt+M 來存取。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-146">The Docs Authoring Pack is accessible by pressing Alt+M inside of VS Code.</span></span> <span data-ttu-id="6ef8d-147">工具列預設會隱藏，但可以顯示它。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-147">The toolbar is hidden by default but can be shown.</span></span> <span data-ttu-id="6ef8d-148">編輯 VS Code 設定 (Control+逗號) 並新增使用者設定 `"markdown.showToolbar": true` 以顯示工具列。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-148">Edit the VS Code settings (Control+comma) and adding user setting `"markdown.showToolbar": true` to show the toolbar.</span></span>

   <span data-ttu-id="6ef8d-149">如需詳細資訊，請參閱 [Docs 編寫套件](how-to-write-docs-auth-pack.md)頁面。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-149">For more information, see the [Docs Authoring Pack](how-to-write-docs-auth-pack.md) page.</span></span>


## <a name="next-steps"></a><span data-ttu-id="6ef8d-150">後續步驟</span><span class="sxs-lookup"><span data-stu-id="6ef8d-150">Next steps</span></span>

<span data-ttu-id="6ef8d-151">現在您已準備好[設定本機 Git 存放庫](get-started-setup-local.md)。</span><span class="sxs-lookup"><span data-stu-id="6ef8d-151">Now you are ready to [Set up a local Git repository](get-started-setup-local.md).</span></span>
