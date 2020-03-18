---
title: 適用於主要或長期變更的 GitHub 參與工作流程
description: 本文示範如何使用「主要」參與者工作流程為 docs.microsoft.com 文章做出貢獻。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 08/30/2017
ms.openlocfilehash: 5231b68f04caa94d3ff2ff26afc38e3218ca06b8
ms.sourcegitcommit: 804a99b89785e5c8f056a9da3f0fbde9f0a56a51
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2020
ms.locfileid: "78331898"
---
# <a name="github-contribution-workflow-for-major-or-long-running-changes"></a>適用於主要或長期變更的 GitHub 參與工作流程

> [!IMPORTANT]
> 所有發佈至 docs.microsoft.com 的存放庫皆採用 [Microsoft 開放原始碼管理辦法](https://opensource.microsoft.com/codeofconduct/) \(英文\) 或 [.NET Foundation 管理辦法](https://dotnetfoundation.org/code-of-conduct) \(英文\)。 如需詳細資訊，請參閱[管理辦法常見問題集](https://opensource.microsoft.com/codeofconduct/faq/) \(英文\)。 若有任何問題或意見，也可以連絡 [opencode@microsoft.com](mailto:opencode@microsoft.com) 或 [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org)。<br>
>
> 您在公用存放庫中針對文件和程式碼範例所提交的次要修正或釐清，將受到 [docs.microsoft.com 使用條款](https://docs.microsoft.com/legal/termsofuse)的約束。 如果您不是 Microsoft 的員工，在做出全新或重要的變更時，系統將會在提取要求中產生意見，要求您提交線上版的貢獻授權合約 (CLA)。 您必須先完成線上表單，您的提取要求才會被合併。

## <a name="overview"></a>概觀

此工作流程適用於需要對某個存放庫進行主要變更，或會成為該存放庫頻繁參與者的參與者。 頻繁的參與者通常會有進行中 (長期) 的變更，這些變更在提取要求完成簽核並合併之前，都需要經歷多個建置/驗證/暫存循環或是花費許多天才能完成。

這些參與類型的範例包括：

[!INCLUDE[contribute-major-changes-change-definition](includes/contribute-how-to-write-workflows-major-change-definition.md)]

### <a name="terminology"></a>術語

在您開始之前，讓我們先檢閱一些用於此工作流程的 Git/GitHub 詞彙及代號。 您暫時還不需要了解它們。 您只需要知道自己將會學習它們，並可以在需要確認定義時回來參考本節。

| Name | 描述 |
|-----------|-------------|
|分叉|通常是作為名詞使用，用來描述主要 GitHub 存放庫的複本。 實際上，分叉只是另一個存放庫。 但它的特殊之處在於 GitHub 會維護與主要/父存放庫之間的關係。 它有時會作為動詞使用，例如「您必須先針對存放庫進行分叉」。|
|遠端 (Remote)|針對遠端存放庫的具名關係，例如「原始」或「上游」遠端。 Git 會將此稱為遠端，因為它是用來參考裝載於另一部電腦上的存放庫。 在此工作流程中，「遠端」一律會是 GitHub 存放庫。|
|原始 (Origin)|指派給本機存放庫和複製該存放庫之原始存放庫之間關係的名稱。 在此工作流程中，「原始」代表針對您分叉的關係。 它有時候會作為原始存放庫本身的代號，例如「記得將您的變更推送到原始」。|
|上游 (Upstream)|上游和原始遠端相同，是針對另一個存放庫的具名關係。 在此工作流程中，「上游」代表您的本機存放庫及主要存放庫 (也就是從之建立分叉的存放庫) 之間的關係。 它有時候會作為上游存放庫本身的代號，例如「記得從上游提取變更」。|

## <a name="workflow"></a>工作流程

>[!IMPORTANT]
> 如果您尚未完成[設定](get-started-setup-github.md)一節中的步驟，請務必完成它們。 本節會引導您設定 GitHub 帳戶、安裝 Git Bash 和 Markdown 編輯器、建立分叉，以及設定本機存放庫。 如果您不熟悉 Git 和 GitHub 概念 (例如存放庫或分支等)，請先檢閱 [Git 和 GitHub 基本概念](git-github-fundamentals.md)。

在此工作流程中，變更流程會是重複性的循環。 變更會從裝置的本機存放庫開始，回流至 GitHub 分叉，接著傳送至主要 GitHub 存放庫，然後隨著您納入來自其他參與者的變更再次返回本機。

### <a name="use-github-flow"></a>使用 GitHub 流程

在 [Git 和 GitHub 基本概念](git-github-fundamentals.md#git)中，有提到 Git 存放庫會包含一個主要分支，以及任何其他尚未整合至「主要」的處理中分支。 每當您要導入一系列邏輯相關的變更時，最佳做法為建立「工作分支」  來透過工作流程管理這些變更。 我們在此之所以將它稱為工作分支，是因為它是將變更整合至主要分支之前，對變更進行逐一查看/改進的工作空間。

將相關聯的變更隔離限制於特定分支中，可讓您獨立地控制及導入變更，並將其目標設定為發佈週期中的特定發行時間。 在現實中，根據所進行工作的不同，您的存放庫中很容易就會出現數個工作分支。 同時處理多個分支 (每個分支都代表不同的專案) 的情況，其實相當常見。

>[!TIP]
>直接在主要分支中做出變更並不是  良好的做法。 假設您使用主要分支，以針對預定時程的功能發行導入一系列變更。 您完成變更，並正在等待發行這些變更。 在此期間，您收到修正某個項目的緊急要求，因此您對主要分支中的某個檔案做出變更並將它發佈。 在此範例中，您會在無意中使該修正「連同」  先前正在為特定發行日期保留的變更一起發佈。

現在，讓我們在本機存放庫中建立新的工作分支，以擷取您所建議的變更。 如果您已設定 Git Bash (請參閱[安裝內容撰寫工具](get-started-setup-tools.md))，您可以建立新的分支，並使用下列複製存放庫中的命令將該分支「簽出」：

````
git checkout -b "branchname"
````

每個 Git 用戶端都不同，因此請參閱適您慣用用戶端的說明。 在 [GitHub 流程](https://guides.github.com/introduction/flow/)上的 GitHub 指南中有程序的概觀。

## <a name="making-your-changes"></a>進行變更

您已經有 Microsoft 存放庫的複本 (「複製的存放庫」)，且已經建立分支，現在您可以隨意使用任何文字或 Markdown 編輯器 (如[安裝內容撰寫工具](get-started-setup-tools.md)頁面上所述)，進行您認為對社群有所幫助的任何變更。  您可以在本機儲存變更，在完成變更之前都無需將其提交至 Microsoft。

## <a name="saving-changes-to-your-repository"></a>儲存變更至您的存放庫

將變更傳送給作者之前，您必須先將其儲存至 Github 存放庫。  同樣地，雖然所有工具都不相同，但如果您使用 Git Bash 命令列，只需要幾個簡單的步驟就可以完成這項作業。

首先，您需要在存放庫中「暫存」  所有要認可的變更。  您可以執行下列命令來完成此動作：

````
git add --all
````

接下來，您需要將已儲存的變更認可至本機存放庫。  您可以執行下列命令以在 Git Bash 中完成此動作：

````
git commit -m "Short Description of Changes Made"
````

最後，由於您是在本機電腦上建立此分支，因此需要為 GitHub.com 帳戶中的分支同步更新資訊。  如果您使用 Git Bash，則可執行下列命令來完成此動作：

````
git push --set-upstream origin <branchname>
````

大功告成！  您的程式碼現在已經在 GitHub 存放庫中，並可供建立提取要求。  

>[!TIP]
> 雖然您的變更會在推送時顯示於您個人 GitHub 帳戶中，但您並不需要立即提交提取要求。  如果您想要暫停並稍後再回來進行其他調整也沒關係！

需要修正您已經提交的東西嗎？  沒問題！  只要在相同分支中進行變更，然後再次認可並推送即可 (不需要在相同分支的後續推送上設定上游伺服器)。

還需要進行更多其他項目的變更嗎？  切換回主分支，並簽出另一個全新的分支，使用 Git Bash 輕鬆完成此動作：

````
git checkout master
git checkout -b "branchname"
````

現在已經回到新的分支，您又朝成為主要參與者邁進了一大步。

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## <a name="next-steps"></a>下一步

大功告成！ 您已對 docs.microsoft.com 內容做出貢獻！

- 若要深入了解 Markdown 和 Markdown 延伸模組語法等主題，請繼續閱讀 [Markdown 參考](markdown-reference.md)一文。
