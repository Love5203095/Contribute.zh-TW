---
title: 在本機設定 Git 存放庫
description: 本文提供建立本機 Git 存放庫並為文件進行貢獻的指引，包括建立分支和複製程序。
author: jasonwhowell
ms.author: jasonh
ms.date: 01/18/2018
ms.openlocfilehash: 895c0fb0d64708e8e3d0f632c10a060791d15b65
ms.sourcegitcommit: d3c7b49dc854dae8da9cd49da8ac4035789a5010
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/23/2018
ms.locfileid: "49805669"
---
# <a name="set-up-git-repository-locally-for-documentation"></a><span data-ttu-id="a01f3-103">在本機針對文件設定 Git 存放庫</span><span class="sxs-lookup"><span data-stu-id="a01f3-103">Set up Git repository locally for documentation</span></span>

<span data-ttu-id="a01f3-104">本文說明在本機電腦上設定 Git 存放庫以針對 Microsoft 文件進行貢獻的步驟。</span><span class="sxs-lookup"><span data-stu-id="a01f3-104">This article describes the steps to set up a git repository on your local machine, with the intent to contribute to Microsoft documentation.</span></span> <span data-ttu-id="a01f3-105">參與者可能會使用本機複製的存放庫來加入新的文章、在現有的文章上進行主要編輯，或變更圖檔。</span><span class="sxs-lookup"><span data-stu-id="a01f3-105">Contributors may use a locally cloned repository to add new articles, do major edits on existing articles, or change artwork.</span></span>

<span data-ttu-id="a01f3-106">您會執行單次設定活動來開始參與：</span><span class="sxs-lookup"><span data-stu-id="a01f3-106">You run these one-time setup activities to get started contributing:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="a01f3-107">決定適當的存放庫</span><span class="sxs-lookup"><span data-stu-id="a01f3-107">Determine the appropriate repository</span></span>
> * <span data-ttu-id="a01f3-108">將存放庫派生至您的 GitHub 帳戶</span><span class="sxs-lookup"><span data-stu-id="a01f3-108">Fork the repository to your GitHub account</span></span>
> * <span data-ttu-id="a01f3-109">選擇複製檔案的本機資料夾</span><span class="sxs-lookup"><span data-stu-id="a01f3-109">Choose a local folder for the cloned files</span></span>
> * <span data-ttu-id="a01f3-110">將存放庫複製到本機電腦</span><span class="sxs-lookup"><span data-stu-id="a01f3-110">Clone the repository to your local machine</span></span>
> * <span data-ttu-id="a01f3-111">設定上游遠端值</span><span class="sxs-lookup"><span data-stu-id="a01f3-111">Configure the upstream remote value</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a01f3-112">如果只是對文章進行次要變更，則不需要完成本文中的步驟。</span><span class="sxs-lookup"><span data-stu-id="a01f3-112">If you're making only minor changes to an article, you *do not* need to complete the steps in this article.</span></span> <span data-ttu-id="a01f3-113">您可以直接跳到[快速變更工作流程](index.md#quick-edits-to-existing-documents)。</span><span class="sxs-lookup"><span data-stu-id="a01f3-113">You can continue directly to the [quick changes workflow](index.md#quick-edits-to-existing-documents).</span></span>
>

## <a name="overview"></a><span data-ttu-id="a01f3-114">概觀</span><span class="sxs-lookup"><span data-stu-id="a01f3-114">Overview</span></span>

<span data-ttu-id="a01f3-115">若要參與 Microsoft 的文件網站，您可以複製對應的文件存放庫，以便在本機製作和編輯 Markdown 檔案。</span><span class="sxs-lookup"><span data-stu-id="a01f3-115">To contribute to Microsoft's documentation site, you can make and edit Markdown files locally by cloning the corresponding documentation repository.</span></span> <span data-ttu-id="a01f3-116">Microsoft 需要您將適當的存放庫派生至您本身的 GitHub 帳戶，這樣您就有儲存建議變更的讀取/寫入權限。</span><span class="sxs-lookup"><span data-stu-id="a01f3-116">Microsoft requires you to fork the appropriate repository into your own GitHub account, so that you have read/write permissions there to store your proposed changes.</span></span> <span data-ttu-id="a01f3-117">然後，您就可以使用提取要求，將變更合併到唯獨中央共用存放庫中。</span><span class="sxs-lookup"><span data-stu-id="a01f3-117">Then you use pull requests to merge changes into the read-only central shared repository.</span></span>

![GitHub Triangle](./media/git-and-github-initial-setup.png)

<span data-ttu-id="a01f3-119">如果您還不熟悉 GitHub，請觀賞以下影片以了解分叉和複製程序的概念性概觀：</span><span class="sxs-lookup"><span data-stu-id="a01f3-119">If you're new to GitHub, watch the following video for a conceptual overview of the forking and cloning process:</span></span>

>[!VIDEO https://channel9.msdn.com/Blogs/CoolMoose/Git-Repository-Setup/player]

## <a name="determine-the-repository"></a><span data-ttu-id="a01f3-120">決定存放庫</span><span class="sxs-lookup"><span data-stu-id="a01f3-120">Determine the repository</span></span>

<span data-ttu-id="a01f3-121">裝載於 [docs.microsoft.com](https://docs.microsoft.com) 的文件位於 [github.com](https://www.github.com) 上數個不同的存放庫。</span><span class="sxs-lookup"><span data-stu-id="a01f3-121">Documentation hosted at [docs.microsoft.com](https://docs.microsoft.com) resides in several different repositories at [github.com](https://www.github.com).</span></span>

1. <span data-ttu-id="a01f3-122">如果您不確定要使用哪個存放庫，則請使用您的網頁瀏覽器參閱 docs.microsoft.com 上的文件。</span><span class="sxs-lookup"><span data-stu-id="a01f3-122">If you are unsure of which repository to use, then visit the article on docs.microsoft.com using your web browser.</span></span> <span data-ttu-id="a01f3-123">選取文章右上角的 [編輯] 連結 (鉛筆圖示)。</span><span class="sxs-lookup"><span data-stu-id="a01f3-123">Select the **Edit** link (pencil icon) on the upper right of the article.</span></span>

   ![按一下 [編輯] 來決定存放庫和檔案位置。](media/index/edit-article.png)

2. <span data-ttu-id="a01f3-125">該連結會帶您前往適當存放庫中所對應 Markdown 檔案的 github.com 位置。</span><span class="sxs-lookup"><span data-stu-id="a01f3-125">That link takes you to github.com location for the corresponding Markdown file in the appropriate repository.</span></span> <span data-ttu-id="a01f3-126">請記下檢視存放庫名稱的 URL。</span><span class="sxs-lookup"><span data-stu-id="a01f3-126">Note the URL to view the repository name.</span></span>

   ![請注意決定存放庫位置的 URL。](media/public-repo.png)

   <span data-ttu-id="a01f3-128">例如，這些受歡迎的存放庫可供公開參與使用：</span><span class="sxs-lookup"><span data-stu-id="a01f3-128">For example, these popular repositories are available for public contributions:</span></span>
   - <span data-ttu-id="a01f3-129">Azure 文件 [https://github.com/MicrosoftDocs/azure-docs](https://github.com/MicrosoftDocs/azure-docs)</span><span class="sxs-lookup"><span data-stu-id="a01f3-129">Azure documentation [https://github.com/MicrosoftDocs/azure-docs](https://github.com/MicrosoftDocs/azure-docs)</span></span>
   - <span data-ttu-id="a01f3-130">SQL Server 文件 [https://github.com/MicrosoftDocs/sql-docs](https://github.com/MicrosoftDocs/sql-docs)</span><span class="sxs-lookup"><span data-stu-id="a01f3-130">SQL Server documentation [https://github.com/MicrosoftDocs/sql-docs](https://github.com/MicrosoftDocs/sql-docs)</span></span>
   - <span data-ttu-id="a01f3-131">Visual Studio 文件 [https://github.com/MicrosoftDocs/visualstudio-docs](https://github.com/MicrosoftDocs/visualstudio-docs)</span><span class="sxs-lookup"><span data-stu-id="a01f3-131">Visual Studio documentation [https://github.com/MicrosoftDocs/visualstudio-docs](https://github.com/MicrosoftDocs/visualstudio-docs)</span></span>
   - <span data-ttu-id="a01f3-132">.NET 文件 [https://github.com/dotnet/docs](https://github.com/dotnet/docs)</span><span class="sxs-lookup"><span data-stu-id="a01f3-132">.NET Documentation [https://github.com/dotnet/docs](https://github.com/dotnet/docs)</span></span>
   - <span data-ttu-id="a01f3-133">Azure .Net SDK 文件 [https://github.com/azure/azure-docs-sdk-dotnet](https://github.com/azure/azure-docs-sdk-dotnet)</span><span class="sxs-lookup"><span data-stu-id="a01f3-133">Azure .Net SDK documentation [https://github.com/azure/azure-docs-sdk-dotnet](https://github.com/azure/azure-docs-sdk-dotnet)</span></span>

## <a name="fork-the-repository"></a><span data-ttu-id="a01f3-134">派生存放庫</span><span class="sxs-lookup"><span data-stu-id="a01f3-134">Fork the repository</span></span>
<span data-ttu-id="a01f3-135">透過 GitHub 網站使用適當的存放庫，建立該存放庫到您自己 GitHub 帳戶的分支。</span><span class="sxs-lookup"><span data-stu-id="a01f3-135">Using the appropriate repository, create a fork of the repository into your own GitHub account by using the GitHub website.</span></span>

<span data-ttu-id="a01f3-136">因為所有主要文件存放庫都提供唯讀存取權，所以需要個人分支。</span><span class="sxs-lookup"><span data-stu-id="a01f3-136">A personal fork is required since all main documentation repositories provide read-only access.</span></span> <span data-ttu-id="a01f3-137">若要進行變更，您必須從主要存放庫的分支提交[提取要求](git-github-fundamentals.md#pull-requests)。</span><span class="sxs-lookup"><span data-stu-id="a01f3-137">To make changes, you must submit a [pull request](git-github-fundamentals.md#pull-requests) from your fork into the main repository.</span></span> <span data-ttu-id="a01f3-138">為了加快此程序，您首先需要有自己的存放庫複本，而您在其中具有寫入權限。</span><span class="sxs-lookup"><span data-stu-id="a01f3-138">To facilitate this process, you first need your own copy of the repository, in which you have write access.</span></span> <span data-ttu-id="a01f3-139">GitHub 分叉即符合此用途。</span><span class="sxs-lookup"><span data-stu-id="a01f3-139">A GitHub *fork* serves that purpose.</span></span>

1. <span data-ttu-id="a01f3-140">移至主要存放庫的 GitHub 頁面，然後按一下右上角的 [Fork] \(分叉\) 按鈕。</span><span class="sxs-lookup"><span data-stu-id="a01f3-140">Go to the main repository's GitHub page and click the **Fork** button on the upper right.</span></span>

   ![GitHub 設定檔範例](./media/contribute-get-started-setup-local/fork.png)

2. <span data-ttu-id="a01f3-142">出現提示時，請選取您的 GitHub 帳戶磚作為應建立分支的目的地。</span><span class="sxs-lookup"><span data-stu-id="a01f3-142">If you are prompted, select your GitHub account tile as the destination where the fork should be created.</span></span> <span data-ttu-id="a01f3-143">這個提示會在您的 GitHub 帳戶中建立該存放庫的複本 (稱為分支)。</span><span class="sxs-lookup"><span data-stu-id="a01f3-143">This prompt creates a copy of the repository within your GitHub account, known as a fork.</span></span>

## <a name="choose-a-local-folder"></a><span data-ttu-id="a01f3-144">撰擇本機資料夾</span><span class="sxs-lookup"><span data-stu-id="a01f3-144">Choose a local folder</span></span>
<span data-ttu-id="a01f3-145">請建立一個本機資料夾，以便在本機保留存放庫的複本。</span><span class="sxs-lookup"><span data-stu-id="a01f3-145">Make a local folder to hold a copy of the repository locally.</span></span> <span data-ttu-id="a01f3-146">某些存放庫可能很大；例如，對於 azure-docs，最高可達 5 GB。</span><span class="sxs-lookup"><span data-stu-id="a01f3-146">Some of the repositories can be large; up to 5 GB for azure-docs for example.</span></span> <span data-ttu-id="a01f3-147">請選擇具有可用磁碟空間的位置。</span><span class="sxs-lookup"><span data-stu-id="a01f3-147">Choose a location with available disk space.</span></span>

1. <span data-ttu-id="a01f3-148">選擇應該容易記住和鍵入的名稱。</span><span class="sxs-lookup"><span data-stu-id="a01f3-148">Choose a folder name should be easy for you to remember and type.</span></span> <span data-ttu-id="a01f3-149">例如，考慮使用根資料夾 `C:\docs\`，或者在您的使用者設定檔目錄 `~/Documents/docs/` 中建立一個資料夾</span><span class="sxs-lookup"><span data-stu-id="a01f3-149">For example, consider a root folder `C:\docs\` or make a folder in your user profile directory `~/Documents/docs/`</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="a01f3-150">請避免選擇以巢狀方式內嵌於另一個 Git 存放庫資料夾位置的本機資料夾路徑。</span><span class="sxs-lookup"><span data-stu-id="a01f3-150">Avoid choosing a local folder path that is nested inside of another git repository folder location.</span></span> <span data-ttu-id="a01f3-151">雖然接受以彼此相隣的方式儲存 Git 複製的資料夾，但以巢狀方式將 Git 資料夾內嵌於另一個資料夾會導致檔案追蹤發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="a01f3-151">While it is acceptable to store the git cloned folders adjacent to each other, nesting git folders inside one another causes errors for the file tracking.</span></span>

2. <span data-ttu-id="a01f3-152">啟動 Git Bash</span><span class="sxs-lookup"><span data-stu-id="a01f3-152">Launch Git Bash</span></span>

   ![啟動 Git Bash](./media/contribute-get-started-setup-local/gitbash-start.png)

   <span data-ttu-id="a01f3-154">Git Bash 的預設啟動位置通常是 Windows 作業系統上的主目錄 (~) 或 `/c/users/<Windows-user-account>/`。</span><span class="sxs-lookup"><span data-stu-id="a01f3-154">The default location that Git Bash starts in is typically the home directory (~) or `/c/users/<Windows-user-account>/` on Windows OS.</span></span>

   <span data-ttu-id="a01f3-155">若要判定目前的目錄，請在 $ 提示下鍵入 `pwd`。</span><span class="sxs-lookup"><span data-stu-id="a01f3-155">To determine the current directory, type `pwd` at the $ prompt.</span></span> 

3. <span data-ttu-id="a01f3-156">將目錄切換 (cd) 到您為了在本機裝載存放庫而建立的資料夾。</span><span class="sxs-lookup"><span data-stu-id="a01f3-156">Change directory (cd) into the folder that you created for hosting the repository locally.</span></span> <span data-ttu-id="a01f3-157">請注意，Git Bash 會針對資料夾路徑使用 Linux 正斜線慣例，而不是反斜線。</span><span class="sxs-lookup"><span data-stu-id="a01f3-157">Note that Git Bash uses the Linux convention of forward-slashes instead of back-slashes for folder paths.</span></span>

   <span data-ttu-id="a01f3-158">例如，`cd /c/docs/ ` 或 `cd ~/Documents/docs/`</span><span class="sxs-lookup"><span data-stu-id="a01f3-158">For example, `cd /c/docs/ ` or `cd ~/Documents/docs/`</span></span>

## <a name="create-a-local-clone"></a><span data-ttu-id="a01f3-159">建立本機複製品</span><span class="sxs-lookup"><span data-stu-id="a01f3-159">Create a local clone</span></span>

<span data-ttu-id="a01f3-160">使用 Git Bash，準備執行 **clone** 命令，以將存放庫的複本 (您的分支) 下拉至裝置的目前目錄中。</span><span class="sxs-lookup"><span data-stu-id="a01f3-160">Using Git Bash, prepare to run the **clone** command to pull a copy of a repository (your fork) down to your device on the current directory.</span></span> 

### <a name="authenticate-by-using-git-credential-manager"></a><span data-ttu-id="a01f3-161">使用 Git 認證管理員進行驗證</span><span class="sxs-lookup"><span data-stu-id="a01f3-161">Authenticate by using Git Credential Manager</span></span>
<span data-ttu-id="a01f3-162">如果您已安裝最新版本的 Git for Windows 並已接受預設安裝，Git 認證管理員預設便會啟用。</span><span class="sxs-lookup"><span data-stu-id="a01f3-162">If you installed the latest version of Git for Windows and accepted the default installation, Git Credential Manager is enabled by default.</span></span> <span data-ttu-id="a01f3-163">Git 認證管理員能使驗證變得更加輕鬆，因為您不需要在重新建立與 GitHub 的驗證連線/遠端時，重新叫用自己的個人存取權杖。</span><span class="sxs-lookup"><span data-stu-id="a01f3-163">Git Credential Manager makes authentication much easier, because you don't need to recall your personal access token when re-establishing authenticated connections and remotes with GitHub.</span></span>

1. <span data-ttu-id="a01f3-164">執行 **clone** 命令，並提供存放庫名稱。</span><span class="sxs-lookup"><span data-stu-id="a01f3-164">Run the **clone** command, by providing the repository name.</span></span> <span data-ttu-id="a01f3-165">複製作業會將分支存放庫下載 (複製) 到本機電腦上。</span><span class="sxs-lookup"><span data-stu-id="a01f3-165">Cloning downloads (clone) the forked repository on your local computer.</span></span> 

    > [!Tip]
    > <span data-ttu-id="a01f3-166">從 GitHub UI 中的 [Clone or download] \(複製或下載\) 按鈕，可以取得複製命令的分叉 GitHub URL：</span><span class="sxs-lookup"><span data-stu-id="a01f3-166">You can get your fork's GitHub URL for the clone command from the **Clone or download** button in the GitHub UI:</span></span>
    >
    > ![複製或下載](./media/contribute-get-started-setup-local/clone-or-download.png)

    <span data-ttu-id="a01f3-168">請務必於複製程序期間指定「您的分叉」的路徑，而非用於建立分叉的主要存放庫。</span><span class="sxs-lookup"><span data-stu-id="a01f3-168">Be sure to specify the path to *your fork* during the cloning process, not the main repository from which you created the fork.</span></span> <span data-ttu-id="a01f3-169">否則，您無法參與變更。</span><span class="sxs-lookup"><span data-stu-id="a01f3-169">Otherwise, you cannot contribute changes.</span></span> <span data-ttu-id="a01f3-170">個人 GitHub 使用者帳戶可用來參考分支，例如：`github.com/<github-username>/<repo>`。</span><span class="sxs-lookup"><span data-stu-id="a01f3-170">Your fork is referenced through your personal GitHub user account, such as `github.com/<github-username>/<repo>`.</span></span>

    ```bash
    git clone https://github.com/<github-username>/<repo>.git
    ```

    <span data-ttu-id="a01f3-171">您的 clone 命令應該類似此範例：</span><span class="sxs-lookup"><span data-stu-id="a01f3-171">Your clone command should look similar to this example:</span></span>

    ```bash
    git clone https://github.com/smithj/azure-docs.git
    ```

2. <span data-ttu-id="a01f3-172">出現提示時，請輸入您的 GitHub 認證。</span><span class="sxs-lookup"><span data-stu-id="a01f3-172">When you're prompted, enter your GitHub credentials.</span></span>

    ![GitHub 登入](./media/contribute-get-started-setup-local/github-login.png)

3. <span data-ttu-id="a01f3-174">出現提示時，請輸入您的雙因素驗證碼。</span><span class="sxs-lookup"><span data-stu-id="a01f3-174">When you're prompted, enter your two-factor authentication code.</span></span>

    ![GitHub 雙因素驗證](./media/contribute-get-started-setup-local/github-2fa.png)

    > [!Note]
    > <span data-ttu-id="a01f3-176">您的認證將會被儲存，並用於驗證日後的 GitHub 要求。</span><span class="sxs-lookup"><span data-stu-id="a01f3-176">Your credentials will be saved and used to authenticate future GitHub requests.</span></span> <span data-ttu-id="a01f3-177">您在每部電腦上只需執行此驗證一次。</span><span class="sxs-lookup"><span data-stu-id="a01f3-177">You only need to do this authentication once per computer.</span></span> 

4. <span data-ttu-id="a01f3-178">clone 命令即會執行，並將分支中的存放庫檔案複本下載到本機磁碟。</span><span class="sxs-lookup"><span data-stu-id="a01f3-178">The clone command runs and downloads a copy of the repository files from your fork into a new folder on the local disk.</span></span> <span data-ttu-id="a01f3-179">將會在目前的資料夾中建立新的資料夾。</span><span class="sxs-lookup"><span data-stu-id="a01f3-179">A new folder is made within the current folder.</span></span> <span data-ttu-id="a01f3-180">根據存放庫大小而定，這可能需要幾分鐘的時間。</span><span class="sxs-lookup"><span data-stu-id="a01f3-180">It may take a few minutes, depending on the repository size.</span></span> <span data-ttu-id="a01f3-181">您可以在此作業完成後，瀏覽資料夾以查看結構。</span><span class="sxs-lookup"><span data-stu-id="a01f3-181">You can explore the folder to see the structure once it is finished.</span></span>

## <a name="configure-remote-upstream"></a><span data-ttu-id="a01f3-182">設定遠端上游</span><span class="sxs-lookup"><span data-stu-id="a01f3-182">Configure remote upstream</span></span>
<span data-ttu-id="a01f3-183">複製存放庫之後，請設定與主要存放庫 (名為**上游**) 的唯讀遠端連線。</span><span class="sxs-lookup"><span data-stu-id="a01f3-183">After cloning the repository, set up a read-only remote connection to the main repository named **upstream**.</span></span> <span data-ttu-id="a01f3-184">您將使用此上游 URL，讓本機存放庫與其他人所進行的最新變更保持同步。</span><span class="sxs-lookup"><span data-stu-id="a01f3-184">You use the upstream URL to keep your local repository in sync with the latest changes made by others.</span></span> <span data-ttu-id="a01f3-185">**git remote** 命令可用來設定設定值。</span><span class="sxs-lookup"><span data-stu-id="a01f3-185">The **git remote** command is used to set the configuration value.</span></span> <span data-ttu-id="a01f3-186">您將會使用 **fetch** 命令從上游存放庫重新整理分支資訊。</span><span class="sxs-lookup"><span data-stu-id="a01f3-186">You use the **fetch** command to refresh the branch info from the upstream repository.</span></span>

1. <span data-ttu-id="a01f3-187">如果您使用 **Git 認證管理員**，請使用下列命令。</span><span class="sxs-lookup"><span data-stu-id="a01f3-187">If you're using **Git Credential Manager**, use the following commands.</span></span> <span data-ttu-id="a01f3-188">請取代 \<存放庫\> 和 \<組織\> 預留位置。</span><span class="sxs-lookup"><span data-stu-id="a01f3-188">Replace the \<repo\> and \<organization\> placeholders.</span></span>
   ```bash
   cd <repo>
   git remote add upstream https://github.com/<organization>/<repo>.git
   git fetch upstream
   ```

2. <span data-ttu-id="a01f3-189">檢視設定的值，並確認 URL 都正確。</span><span class="sxs-lookup"><span data-stu-id="a01f3-189">View the configured values and confirm the URLs are correct.</span></span> <span data-ttu-id="a01f3-190">請確定**原始** URL 指向您的個人分支。</span><span class="sxs-lookup"><span data-stu-id="a01f3-190">Ensure the **origin** URLs point to your personal fork.</span></span> <span data-ttu-id="a01f3-191">請確定**上游** URL 指向主要存放庫，例如 MicrosoftDocs 或 Azure。</span><span class="sxs-lookup"><span data-stu-id="a01f3-191">Ensure the **upstream** URLs point to the main repository, such as MicrosoftDocs or Azure.</span></span> 
   ```bash
   git remote -v 
   ```

   <span data-ttu-id="a01f3-192">隨即顯示遠端輸出範例。</span><span class="sxs-lookup"><span data-stu-id="a01f3-192">Example remote output is shown.</span></span> <span data-ttu-id="a01f3-193">名為 MyGitAccount 的虛構 Git 帳戶設有用來存取存放庫 azure-docs 的個人存取權杖：</span><span class="sxs-lookup"><span data-stu-id="a01f3-193">A fictitious git account named MyGitAccount is configured with a personal access token to access the repo azure-docs:</span></span>
   ```output
   origin  https://github.com/MyGitAccount/azure-docs.git (fetch)
   origin  https://github.com/MyGitAccount/azure-docs.git(push)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (fetch)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (push)
   ```

3. <span data-ttu-id="a01f3-194">如果犯了一個錯誤，您可以移除遠端值。</span><span class="sxs-lookup"><span data-stu-id="a01f3-194">If you made a mistake, you can remove the remote value.</span></span> <span data-ttu-id="a01f3-195">若要移除上游值，請執行 `git remote remove upstream`。</span><span class="sxs-lookup"><span data-stu-id="a01f3-195">To remove the upstream value, run the command `git remote remove upstream`.</span></span>

## <a name="next-steps"></a><span data-ttu-id="a01f3-196">後續步驟</span><span class="sxs-lookup"><span data-stu-id="a01f3-196">Next steps</span></span>
- <span data-ttu-id="a01f3-197">若要深入了解新增和更新內容，請繼續移至 [GitHub 參與工作流程](how-to-write-workflows-major.md)頁面。</span><span class="sxs-lookup"><span data-stu-id="a01f3-197">To learn more about adding and updating content, continue to the [GitHub contribution workflow](how-to-write-workflows-major.md).</span></span>
