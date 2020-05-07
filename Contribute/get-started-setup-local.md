---
title: 在本機設定 Git 存放庫
description: 本文提供建立本機 Git 存放庫並為文件進行貢獻的指引，包括建立分支和複製程序。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: jasonwhowell
ms.author: jasonh
ms.date: 01/18/2018
ms.openlocfilehash: e73c60c439285f901c5c83e538f8971d795bd6c4
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/04/2020
ms.locfileid: "72288605"
---
# <a name="set-up-git-repository-locally-for-documentation"></a>在本機針對文件設定 Git 存放庫

本文說明在本機電腦上設定 Git 存放庫以針對 Microsoft 文件進行貢獻的步驟。 參與者可能會使用本機複製的存放庫來加入新的文章、在現有的文章上進行主要編輯，或變更圖檔。

您會執行這些一次性安裝活動來開始參與：
> [!div class="checklist"]
> * 決定適當的存放庫
> * 將存放庫派生至您的 GitHub 帳戶
> * 選擇複製檔案的本機資料夾
> * 將存放庫複製到本機電腦
> * 設定上游遠端值

> [!IMPORTANT]
> 如果只是對文章進行次要變更，則不需要  完成本文中的步驟。 您可以直接跳到[快速變更工作流程](index.md#quick-edits-to-existing-documents)。
>

## <a name="overview"></a>概觀

若要參與 Microsoft 的文件網站，您可以複製對應的文件存放庫，以便在本機製作和編輯 Markdown 檔案。 Microsoft 需要您將適當的存放庫派生至您本身的 GitHub 帳戶，這樣您就有儲存建議變更的讀取/寫入權限。 然後，您就可以使用提取要求，將變更合併到唯獨中央共用存放庫中。

![GitHub Triangle](./media/git-and-github-initial-setup.png)

如果您還不熟悉 GitHub，請觀賞以下影片以了解分叉和複製程序的概念性概觀：

>[!VIDEO https://channel9.msdn.com/Blogs/CoolMoose/Git-Repository-Setup/player]

## <a name="determine-the-repository"></a>決定存放庫

裝載於 [docs.microsoft.com](https://docs.microsoft.com) 的文件位於 [github.com](https://www.github.com) 上數個不同的存放庫。

1. 如果您不確定要使用哪個存放庫，請使用您的網頁瀏覽器瀏覽 [docs.microsoft.com](https://docs.microsoft.com) 上的文章。 選取文章右上角的 [編輯]  連結 (鉛筆圖示)。

   ![按一下 [編輯] 來決定存放庫和檔案位置。](media/index/edit-article.png)

2. 該連結會帶您前往適當存放庫中所對應 Markdown 檔案的 github.com 位置。 請記下檢視存放庫名稱的 URL。

   ![請注意決定存放庫位置的 URL。](media/public-repo.png)

   例如，這些受歡迎的存放庫可供公開參與使用：
   - Azure 文件 [https://github.com/MicrosoftDocs/azure-docs](https://github.com/MicrosoftDocs/azure-docs)
   - SQL Server 文件 [https://github.com/MicrosoftDocs/sql-docs](https://github.com/MicrosoftDocs/sql-docs)
   - Visual Studio 文件 [https://github.com/MicrosoftDocs/visualstudio-docs](https://github.com/MicrosoftDocs/visualstudio-docs)
   - .NET 文件 [https://github.com/dotnet/docs](https://github.com/dotnet/docs)
   - Azure .Net SDK 文件 [https://github.com/azure/azure-docs-sdk-dotnet](https://github.com/azure/azure-docs-sdk-dotnet)
   - ConfigMgr 文件 [https://github.com/MicrosoftDocs/SCCMdocs](https://github.com/MicrosoftDocs/SCCMdocs/)

## <a name="fork-the-repository"></a>派生存放庫
透過 GitHub 網站使用適當的存放庫，建立該存放庫到您自己 GitHub 帳戶的分支。

因為所有主要文件存放庫都提供唯讀存取權，所以需要個人分支。 若要進行變更，您必須從主要存放庫的分支提交[提取要求](git-github-fundamentals.md#pull-requests)。 為了加快此程序，您首先需要有自己的存放庫複本，而您在其中具有寫入權限。 GitHub 分叉  即符合此用途。

1. 移至主要存放庫的 GitHub 頁面，然後按一下右上角的 [Fork]  \(分叉\) 按鈕。

   ![GitHub 設定檔範例](./media/contribute-get-started-setup-local/fork.png)

2. 出現提示時，請選取您的 GitHub 帳戶磚作為應建立分支的目的地。 這個提示會在您的 GitHub 帳戶中建立該存放庫的複本 (稱為分支)。

## <a name="choose-a-local-folder"></a>撰擇本機資料夾
請建立一個本機資料夾，以便在本機保留存放庫的複本。 某些存放庫可能很大；例如，對於 azure-docs，最高可達 5 GB。 請選擇具有可用磁碟空間的位置。

1. 選擇應該容易記住和鍵入的名稱。 例如，考慮使用根資料夾 `C:\docs\`，或者在您的使用者設定檔目錄 `~/Documents/docs/` 中建立一個資料夾

   > [!IMPORTANT]
   > 請避免選擇以巢狀方式內嵌於另一個 Git 存放庫資料夾位置的本機資料夾路徑。 雖然接受以彼此相隣的方式儲存 Git 複製的資料夾，但以巢狀方式將 Git 資料夾內嵌於另一個資料夾會導致檔案追蹤發生錯誤。

2. 啟動 Git Bash

   ![啟動 Git Bash](./media/contribute-get-started-setup-local/gitbash-start.png)

   Git Bash 的預設啟動位置通常是 Windows 作業系統上的主目錄 (~) 或 `/c/users/<Windows-user-account>/`。

   若要判定目前的目錄，請在 $ 提示下鍵入 `pwd`。 

3. 將目錄切換 (cd) 到您為了在本機裝載存放庫而建立的資料夾。 請注意，Git Bash 會針對資料夾路徑使用 Linux 正斜線慣例，而不是反斜線。

   例如，`cd /c/docs/ ` 或 `cd ~/Documents/docs/`

## <a name="create-a-local-clone"></a>建立本機複製品

使用 Git Bash，準備執行 **clone** 命令，以將存放庫的複本 (您的分支) 下拉至裝置的目前目錄中。 

### <a name="authenticate-by-using-git-credential-manager"></a>使用 Git 認證管理員進行驗證
如果您已安裝最新版本的 Git for Windows 並已接受預設安裝，Git 認證管理員預設便會啟用。 Git 認證管理員能使驗證變得更加輕鬆，因為您不需要在重新建立與 GitHub 的驗證連線/遠端時，重新叫用自己的個人存取權杖。

1. 執行 **clone** 命令，並提供存放庫名稱。 複製作業會將分支存放庫下載 (複製) 到本機電腦上。 

    > [!Tip]
    > 從 GitHub UI 中的 [Clone or download]  \(複製或下載\) 按鈕，可以取得複製命令的分叉 GitHub URL：
    >
    > ![複製或下載](./media/contribute-get-started-setup-local/clone-or-download.png)

    請務必於複製程序期間指定「您的分叉」  的路徑，而非用於建立分叉的主要存放庫。 否則，您無法參與變更。 個人 GitHub 使用者帳戶可用來參考分支，例如：`github.com/<github-username>/<repo>`。

    ```bash
    git clone https://github.com/<github-username>/<repo>.git
    ```

    您的 clone 命令應該類似此範例：

    ```bash
    git clone https://github.com/smithj/azure-docs.git
    ```

2. 出現提示時，請輸入您的 GitHub 認證。

    ![GitHub 登入](./media/contribute-get-started-setup-local/github-login.png)

3. 出現提示時，請輸入您的雙因素驗證碼。

    ![GitHub 雙因素驗證](./media/contribute-get-started-setup-local/github-2fa.png)

    > [!Note]
    > 您的認證將會被儲存，並用於驗證日後的 GitHub 要求。 您在每部電腦上只需執行此驗證一次。 

4. clone 命令即會執行，並將分支中的存放庫檔案複本下載到本機磁碟。 將會在目前的資料夾中建立新的資料夾。 根據存放庫大小而定，這可能需要幾分鐘的時間。 您可以在此作業完成後，瀏覽資料夾以查看結構。

## <a name="configure-remote-upstream"></a>設定遠端上游
複製存放庫之後，請設定與主要存放庫 (名為**上游**) 的唯讀遠端連線。 您將使用此上游 URL，讓本機存放庫與其他人所進行的最新變更保持同步。 **git remote** 命令可用來設定設定值。 您將會使用 **fetch** 命令從上游存放庫重新整理分支資訊。

1. 如果您使用 **Git 認證管理員**，請使用下列命令。 請取代 \<存放庫\> 和 \<組織\> 預留位置。
   ```bash
   cd <repo>
   git remote add upstream https://github.com/<organization>/<repo>.git
   git fetch upstream
   ```

2. 檢視設定的值，並確認 URL 都正確。 請確定**原始** URL 指向您的個人分支。 請確定**上游** URL 指向主要存放庫，例如 MicrosoftDocs 或 Azure。 
   ```bash
   git remote -v 
   ```

   隨即顯示遠端輸出範例。 名為 MyGitAccount 的虛構 Git 帳戶設有用來存取存放庫 azure-docs 的個人存取權杖：
   ```output
   origin  https://github.com/MyGitAccount/azure-docs.git (fetch)
   origin  https://github.com/MyGitAccount/azure-docs.git(push)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (fetch)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (push)
   ```

3. 如果犯了一個錯誤，您可以移除遠端值。 若要移除上游值，請執行 `git remote remove upstream`。

## <a name="next-steps"></a>後續步驟
- 若要深入了解新增和更新內容，請繼續移至 [GitHub 參與工作流程](how-to-write-workflows-major.md)頁面。
