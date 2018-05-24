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
ms.sourcegitcommit: e046e7aad8ed22bffe5380d63a9d40f0baeecc57
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/22/2018
---
# <a name="git-and-github-essentials-for-docs"></a>適用於 Docs 的 Git 和 GitHub 基本資訊

## <a name="overview"></a>概觀

身為 Docs 內容的貢獻者，您將與多種工具和程序互動。 您會同時與其他貢獻者在相同專案上共同作業，而且甚至可能同時處理相同內容。 這一切都是透過 Git 和 GitHub 軟體來達成。

Git 是開放原始碼版本控制系統。 它透過「存放庫」中之檔案的「分散式版本控制」來促成此類型的專案共同作業。 本質上來說，Git 可整合由多個參與者在不同時間，針對指定的存放庫所完成的工作流。

GitHub 是 Git 存放庫 (例如用來存放 [docs.microsoft.com](https://docs.microsoft.com) 內容的存放庫) 的 Web 型主機服務。 針對任何專案，GitHub 都裝載主要存放庫，供貢獻者針對其自己的工作建立複本

## <a name="git"></a>Git

若您熟悉集中式版本控制系統 (例如 Team Foundation Server、SharePoint 或 Visual SourceSafe)，您將注意到 Git 擁有可支援其分散式模型的唯一貢獻工作流程與術語。 例如，它並沒有通常會與簽出/簽入作業一起出現的檔案鎖定功能。 事實上，Git 所關心的是更精細層級中的變更，因此會進行逐位元組檔案比較。

Git 也使用分層結構來儲存及管理專案內容：

- *存放庫*：亦稱為 *repo*，這是最高的儲存單位。 存放庫包含一或多個分支。
- *分支*：包含組成專案內容集合之檔案與資料夾的儲存單位。 分支會分隔工作串流 (通常稱為版本)。 貢獻一律是在特定分支的範圍所進行。 所有存放庫都包含預設分支 (通常命名為 "master") 以及一或多個目的是合併回主分支的分支。 主分支是做為最新版本使用，而且是專案的「單一信任來源」。 它是存放庫中所有其他分支的建立來源。

參與者會與 Git 互動，以在本機和 GitHub 層級對存放庫進行更新和操作：

- 於本機透過如 Git Bash 主控台等工具。Git Bash 主控台支援用來管理本機存放庫和與 GitHub 存放庫通訊的 Git 命令
- 透過 [www.github.com](https://www.github.com)。該網站整合了 Git，以管理協調流回主要存放庫的參與

## <a name="github"></a>GitHub

> [!NOTE]
> 雖然 Docs 指導方針是以使用 GitHub 為基礎，某些小組會使用 Visual Studio Team Service 來裝載 Git 存放庫。 Visual Studio Team Explorer 用戶端提供用來與 Team Services 存放庫互動的 GUI，做為透過命令列使用 Git 命令之外的替代方法。
> </br>
> 此外，下列許多指導方針都是透過多年來在 GitHub 中裝載 Azure 服務內容的經驗發展而來的最佳做法。 它們某些 Docs 存放庫中可能為必要做法。

所有的工作流程都是在 GitHub 層級開始與結束，這也是任何 Doc 專案主要存放庫的儲存位置。 參與者為自己的使用目的而建立的複本會跨多部電腦散佈。 這些複本最終會協調回專案的主要 GitHub 存放庫。

### <a name="directory-organization"></a>目錄組織方式

如同先前所提到的，專案的預設/主分支會作為專案內容的最新版本。 主分支中的內容 (以及從它建立的分支) 會約略符合對應 Docs 頁面上文章的組織方式。 系統會使用子目錄來區隔內容 (例如服務)、媒體內容 (例如影像檔案)，以及可讓內容重複使用的 "include" 檔案。

您通常可以在存放庫的根目錄找到主要 `articles` 目錄。 articles 目錄包含一組子目錄。 子目錄中的文章格式為 Markdown 檔案，其副檔名為 *.md*。 某些支援多個服務的存放庫會使用一般的 `/articles` 子目錄，例如 [https://github.com/microsoft/Azure-Docs](https://github.com/microsoft/Azure-Docs) 存放庫。 其他存放庫可能會使用服務特定的名稱，例如 [https://github.com/microsoft/IntuneDocs](https://github.com/microsoft/IntuneDocs) 存放庫是使用 `/IntuneDocs`。

在此目錄的根內，您可以找到有關整體服務或產品的一般文章。 您通常也可以接著找到另一系列的子目錄，這些子目錄會符合功能/服務或常見案例。 例如，Azure "virtual machine" (虛擬機器) 文章是位於 `/virtual-machines` 子目錄，而 Intune "understand and explore" (了解與探索) 文章則位於 `/understand-explore` 子目錄。

### <a name="media-subdirectory"></a>Media 子目錄

每個 article 目錄都包含對應之媒體檔案的 `/media` 子目錄。 媒體檔案包含具有影像參考之文章所使用的影像。

### <a name="includes-subdirectory"></a>Includes 子目錄

只要有兩篇或多篇文章共用的可重複使用內容，系統就會將它放置在主要 `articles` 目錄的 `/includes` 子目錄中。 在使用 include 檔案的 Markdown 檔案中，系統會將對應的 "include" Markdown 擴充功能放置在需要參考 include 檔案的位置。

如需額外的指導方針，請參閱[如何使用 Markdown： Include](how-to-write-use-markdown.md#includes)。

### <a name="markdown-file-template"></a>Markdown 檔案範本

為了方便起見，每個存放庫的根目錄通常包含一個名為 `template.md` 的 Markdown 檔案。 若需要建立新文章以提交到存放庫，您可以將此範本檔案做為「開始檔案」使用。 該檔案包含︰

- 檔案頂端的**中繼資料標頭**其中包含兩個具有 3 個破折號的行。 它包含用於與文章相關之追蹤資訊的多種標記。 文章中繼資料可啟用特定功能，例如作者姓名標示、參與者姓名標示、階層連結與文章描述。 它也包括 SEO 最佳化與報告程序，Microsoft 使用它們來評估內容的成效。 因此，中繼資料非常重要！
- 能描述各種中繼資料標記和值的**中繼資料**區段。 如果您不確定在中繼資料區段中應使用的值，則可以留白，或在前面加上雜湊標記 (#) 使其成為註解，讓存放庫的提取要求檢閱者來檢閱/完成它們。
- 各種使用「Markdown 來格式化文章元素的範例」。
- 一般的**Markdown 擴充功能使用指示**，可用於各種類型的警示。
- 使用 iframe **內嵌視訊**的範例。
- 一般**docs.microsoft.com 擴充功能使用指示**，您可以將其用於特殊控制項，例如按鈕與選取器。

## <a name="pull-requests"></a>提取要求

「提取要求」為讓參與者建議要套用至預設分支之一系列變更的便利方式。 變更 (亦稱為「認可」) 會儲存在參與者的分支中，讓 GitHub 可先模擬將它們「合併」至預設分支後所會帶來的影響。 提取要求也可作為提供參與者來自建置/驗證流程、提取要求檢閱者之意見反應的機制，以在變更合併至預設分支之前解決可能發生的問題。

有兩種方式可透過提取要求來做出貢獻，這取決於您要建議之變更的大小。 我們稍後會在本指南的 [GitHub 工作流程](how-to-write-workflows-major.md)小節中詳細說明這一部分。

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
