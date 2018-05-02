---
title: 安裝內容撰寫工具
description: 本文可協助您下載與安裝使用 Git 與編輯 Markdown 檔案所需的用戶端工具。
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 01/04/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 0ca942e557640db1ba36d3f5b1064656ed3dea8d
ms.sourcegitcommit: 3ec397fab57ea582edb03a59609f62d886410ee8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2018
---
# <a name="install-content-authoring-tools"></a><span data-ttu-id="11e68-103">安裝內容撰寫工具</span><span class="sxs-lookup"><span data-stu-id="11e68-103">Install content authoring tools</span></span>

<span data-ttu-id="11e68-104">本文說明以互動方式安裝 Git 用戶端工具和 Visual Studio Code 的步驟。</span><span class="sxs-lookup"><span data-stu-id="11e68-104">This article describes the steps to interactively install Git client tools and Visual Studio Code.</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="11e68-105">安裝 [Git for Windows](https://git-scm.com/download/win)</span><span class="sxs-lookup"><span data-stu-id="11e68-105">Install [Git for Windows](https://git-scm.com/download/win)</span></span>
> * <span data-ttu-id="11e68-106">安裝 [Visual Studio Code](https://code.visualstudio.com/)</span><span class="sxs-lookup"><span data-stu-id="11e68-106">Install [Visual Studio Code](https://code.visualstudio.com/)</span></span>

>[!IMPORTANT]
> <span data-ttu-id="11e68-107">若只是要對文章進行很少量的變更，*不*需要完成此文章中的步驟，而可繼續直接進入[快速變更工作流程](index.md#quick-edits-to-existing-documents)。</span><span class="sxs-lookup"><span data-stu-id="11e68-107">If you're making only minor changes to an article, you *do not* need to complete the steps in this article and can continue directly to the [quick changes workflow](index.md#quick-edits-to-existing-documents).</span></span>
>
> <span data-ttu-id="11e68-108">我們建議主要參與者完成這些步驟，因為這可讓您使用[主要/長期變更工作流程](how-to-write-workflows-major.md)。</span><span class="sxs-lookup"><span data-stu-id="11e68-108">Major contributors are encouraged to complete these steps, which enable you to use the [major/long-running changes workflow](how-to-write-workflows-major.md).</span></span> <span data-ttu-id="11e68-109">即使您在主要存放庫中具有寫入權限，仍然*強烈建議您 (且此指南假設您會) 對存放庫進行派生和複製*，這樣您會具有在分支中儲存所建議變更的讀取/寫入權限。</span><span class="sxs-lookup"><span data-stu-id="11e68-109">Even if you have write permissions in the main repository, *we highly recommend (and this guide assumes) that you fork and clone the repository*, so that you have read/write permissions to store your proposed changes in your fork.</span></span>

## <a name="install-git-client-tools-on-windows"></a><span data-ttu-id="11e68-110">在 Windows 上安裝 Git 用戶端工具</span><span class="sxs-lookup"><span data-stu-id="11e68-110">Install Git client tools on Windows</span></span>

 <span data-ttu-id="11e68-111">安裝 [Software Freedom Conservancy 的 Git 用戶端工具](https://git-scm.com/download/) \(英文\) 最新版本。</span><span class="sxs-lookup"><span data-stu-id="11e68-111">Install the latest version of [Software Freedom Conservancy's Git client tools](https://git-scm.com/download/).</span></span> <span data-ttu-id="11e68-112">安裝包含了 Git 版本控制系統和 Git Bash，您可以使用此命令列應用程式來與本機 Git 存放庫互動。</span><span class="sxs-lookup"><span data-stu-id="11e68-112">The install includes the Git version control system and Git Bash, the command-line app that you use to interact with your local Git repository.</span></span>

<span data-ttu-id="11e68-113">如果您較偏好圖形化使用者介面 (GUI) 而非命令列介面 (CLI)，請參閱 [Software Freedom Conservancy 的可用 GUI 用戶端頁面](https://git-scm.com/downloads/guis) \(英文\)、[GitHub 的 GitHub 電腦版](https://desktop.github.com/)+ \(英文\)，或 [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx) \(英文\) 以取得一些較受歡迎的選項。</span><span class="sxs-lookup"><span data-stu-id="11e68-113">If you prefer a graphical user interface (GUI) over a command-line interface (CLI), see [Software Freedom Conservancy's available GUI Clients page](https://git-scm.com/downloads/guis), [GitHub's GitHub Desktop](https://desktop.github.com/), or [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx) for some popular options.</span></span>

<span data-ttu-id="11e68-114">請遵循您所選擇用戶端的指示，以進行安裝與設定。</span><span class="sxs-lookup"><span data-stu-id="11e68-114">Follow the instructions for your chosen client for installation and configuration.</span></span>

<span data-ttu-id="11e68-115">在下一篇文章中，您將[設定本機 Git 存放庫](get-started-setup-local.md)。</span><span class="sxs-lookup"><span data-stu-id="11e68-115">In the next article, you will [Set up a local Git repository](get-started-setup-local.md).</span></span>

   <span data-ttu-id="11e68-116">其他的 Git 資源可在此處取得：[Git 術語](https://help.github.com/articles/github-glossary) | [Git 基本概念](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [學習 Git 與 GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)</span><span class="sxs-lookup"><span data-stu-id="11e68-116">Additional Git resources are available here: [Git terminology](https://help.github.com/articles/github-glossary) | [Git basics](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Learning Git and GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)</span></span>

## <a name="understand-markdown-editors"></a><span data-ttu-id="11e68-117">了解 Markdown 編輯器</span><span class="sxs-lookup"><span data-stu-id="11e68-117">Understand Markdown editors</span></span>

<span data-ttu-id="11e68-118">Markdown 是一種容易閱讀及學習的輕量型標記語言。</span><span class="sxs-lookup"><span data-stu-id="11e68-118">Markdown is a lightweight markup language that is both easy to read and easy to learn.</span></span> <span data-ttu-id="11e68-119">因此，它快速地成為業界標準。</span><span class="sxs-lookup"><span data-stu-id="11e68-119">Therefore, it has rapidly become an industry standard.</span></span> <span data-ttu-id="11e68-120">若要以 Markdown 撰寫文章，建議您先下載並安裝 Markdown 編輯器。</span><span class="sxs-lookup"><span data-stu-id="11e68-120">To write articles in Markdown, we recommend that you first download and install a Markdown editor.</span></span>  <span data-ttu-id="11e68-121">[Visual Studio Code](https://code.visualstudio.com/) 是 Microsoft 用來編輯 Markdown 的偏好工具。</span><span class="sxs-lookup"><span data-stu-id="11e68-121">[Visual Studio Code](https://code.visualstudio.com/) is the preferred tool for editing Markdown at Microsoft.</span></span> <span data-ttu-id="11e68-122">[Atom](https://atom.io) 是另一個用來編輯 Markdown 的熱門工具。</span><span class="sxs-lookup"><span data-stu-id="11e68-122">[Atom](https://atom.io) is another popular tool for editing Markdown.</span></span>

<span data-ttu-id="11e68-123">Markdown 文字會儲存到副檔名為 .md 的檔案中。</span><span class="sxs-lookup"><span data-stu-id="11e68-123">Markdown text is saved into files with .md extension.</span></span>

<span data-ttu-id="11e68-124">關於如何使用 Markdown 撰寫的其他詳細資料，包括 Markdown 基本概念及 OPS 自訂 Markdown 擴充功能所支援的功能，都會在稍後的[如何使用 Markdown](how-to-write-use-markdown.md) 文章中涵蓋。</span><span class="sxs-lookup"><span data-stu-id="11e68-124">Additional details on how to write with Markdown, including Markdown basics and the features supported by OPS custom Markdown extensions, are covered later in the [How to use Markdown](how-to-write-use-markdown.md) article.</span></span>

## <a name="visual-studio-code"></a><span data-ttu-id="11e68-125">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="11e68-125">Visual Studio Code</span></span>

<span data-ttu-id="11e68-126">[Visual Studio Code](https://code.visualstudio.com/) 也稱為 VS Code，是一種輕量型編輯器，適用於 Windows、Linux 和 Mac。</span><span class="sxs-lookup"><span data-stu-id="11e68-126">[Visual Studio Code](https://code.visualstudio.com/), also known as VS Code, is a lightweight editor that works on Windows, Linux, and Mac.</span></span> <span data-ttu-id="11e68-127">它包含 Git 整合，並支援擴充功能。</span><span class="sxs-lookup"><span data-stu-id="11e68-127">It includes git integration, and support for extensions.</span></span>

<span data-ttu-id="11e68-128">下載並安裝 [VS Code](https://code.visualstudio.com/)。</span><span class="sxs-lookup"><span data-stu-id="11e68-128">Download and install [VS Code](https://code.visualstudio.com/).</span></span> <span data-ttu-id="11e68-129">VS Code 首頁應該會正確地偵測到您的作業系統。</span><span class="sxs-lookup"><span data-stu-id="11e68-129">The VS Code home page should detect your operating system correctly.</span></span>

- [<span data-ttu-id="11e68-130">Windows</span><span class="sxs-lookup"><span data-stu-id="11e68-130">Windows</span></span>](https://code.visualstudio.com/docs/setup/windows)
- [<span data-ttu-id="11e68-131">Mac</span><span class="sxs-lookup"><span data-stu-id="11e68-131">Mac</span></span>](https://code.visualstudio.com/docs/setup/mac)
- [<span data-ttu-id="11e68-132">Linux</span><span class="sxs-lookup"><span data-stu-id="11e68-132">Linux</span></span>](https://code.visualstudio.com/docs/setup/linux)

> [!TIP]
> <span data-ttu-id="11e68-133">若要啟動 VS Code 並開啟目前的資料夾，請在命令列或 bash 殼層中執行 `code .` 命令。</span><span class="sxs-lookup"><span data-stu-id="11e68-133">To launch VS Code and open the current folder, run the command `code .` in the command line or bash shell.</span></span> <span data-ttu-id="11e68-134">如果目前的資料夾為本機 Git 存放庫的一部分，則 Github 整合會自動在 Visual Studio Code 中顯示。</span><span class="sxs-lookup"><span data-stu-id="11e68-134">If the current folder is part of a local git repo, the github integration appears in Visual Studio Code automatically.</span></span>

## <a name="next-steps"></a><span data-ttu-id="11e68-135">後續步驟</span><span class="sxs-lookup"><span data-stu-id="11e68-135">Next steps</span></span>

<span data-ttu-id="11e68-136">現在您已準備好[設定本機 Git 存放庫](get-started-setup-local.md)。</span><span class="sxs-lookup"><span data-stu-id="11e68-136">Now you are ready to [Set up a local Git repository](get-started-setup-local.md).</span></span>
