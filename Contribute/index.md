---
title: Microsoft Docs 參與者指南的概觀
description: 本指南描述您如何為 Microsoft 文件網站 docs.microsoft.com 做出貢獻。
author: billwagner
ms.author: wiwagn
ms.date: 02/19/2019
ms.openlocfilehash: 9b091f864f5191c9f7a00900ec11a4a1cffdb698
ms.sourcegitcommit: af37d44eb67daa2841959817cd205ec95db18cec
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/29/2019
ms.locfileid: "58653497"
---
# <a name="microsoft-docs-contributor-guide-overview"></a>Microsoft Docs 參與者指南的概觀

歡迎使用 [docs.microsoft.com](https://docs.microsoft.com) (Docs) 參與者指南！

我們有幾個開放原始碼的 Microsoft 文件集，由 GitHub 代管。 並非所有文件集都是完全開放原始碼的，但許多都有公開的存放庫，可讓您透過提取要求來建議變更。 這種開放原始碼的方法可簡化並改善產品工程師、內容小組與客戶之間的通訊，而且還有其他優點：

- 開放原始碼存放庫「公開規畫」  以取得意見反應，了解最迫切需要的文件有哪些。
- 開放原始碼存放庫「公開檢閱」  ，以在我們初次發行時發佈最實用的內容。
- 開放原始碼存放庫「公開更新」  ，讓持續改善內容變得更容易。

[docs.microsoft.com](https://docs.microsoft.com) 上的使用者體驗會直接整合 [GitHub](https://github.com) \(英文\) 工作流程，使其變得更加容易。 請從[編輯您正在檢閱的文件](#quick-edits-to-existing-documents)開始。 或者，透過[檢閱新主題](#review-open-prs)或[建立品質問題](#create-quality-issues)來提供協助。

> [!IMPORTANT]
> 所有發佈至 docs.microsoft.com 的存放庫皆採用 [Microsoft 開放原始碼管理辦法](https://opensource.microsoft.com/codeofconduct/) \(英文\) 或 [.NET Foundation 管理辦法](https://dotnetfoundation.org/code-of-conduct) \(英文\)。 如需詳細資訊，請參閱[管理辦法常見問題集](https://opensource.microsoft.com/codeofconduct/faq/) \(英文\)。 若有任何問題或意見，也可以連絡 [opencode@microsoft.com](mailto:opencode@microsoft.com) 或 [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org)。<br>
>
> 您在公用存放庫中針對文件和程式碼範例所提交的次要修正或釐清，將受到 [docs.microsoft.com 使用條款](https://docs.microsoft.com/legal/termsofuse)的約束。 如果您不是 Microsoft 的員工，在做出全新或大規模的變更時，系統會在提取要求中產生意見，要求您提交線上版的貢獻授權合約 (CLA)。 您必須先完成填寫線上表單，我們才會檢閱或接受您的提取要求。

## <a name="quick-edits-to-existing-documents"></a>快速編輯現有文件

快速編輯可簡化回報並修正文件中小錯誤和遺漏的流程。 即便我們非常努力，發佈的文件中仍不免  存在少許文法和拼字錯誤。 儘管您可以建立問題來回報錯誤，建立提取要求 (PR) 來解決問題會更加快速且輕鬆 (當該選項可用時)。

1. 某些文件頁面允許您直接在瀏覽器中編輯內容。 如果是這樣，您將會看到如下 [編輯]  按鈕。 按一下 [編輯]  (或當地語系化的同等文字) 按鈕，即前往 GitHub 上的原始程式檔。 若沒有看到 [編輯]  按鈕 (不含文字的鉛筆圖示)，表示文件頁面無法變更。

   ![[編輯] 連結的位置](./media/index/edit-article.png)

2. 接著，按一下鉛筆圖示以編輯文章，如下所示。 如果鉛筆圖示顯示為灰色，表示您必須登入您的 GitHub 帳戶或建立新帳戶。 

   ![鉛筆圖示的位置](./media/index/edit-icon.png)


3. 在 Web 編輯器中進行變更。 按一下 [預覽變更]  索引標籤來檢查變更的格式。

4. 完成變更後，請向下捲動到頁面底部。 為變更的內容輸入標題與說明，然後按一下 [建議檔案變更]  ，如下圖所示：

   ![建議檔案變更](./media/index/submit-pull-request.png)

5. 現在您已提出變更建議，您必須要求存放庫的擁有者將您的變更「提取」到其存放庫中。 使用「提取要求」即可完成此動作。 按一下上圖中的 [Propose file change]  \(建議檔案變更\) 後，應該就會前往如下圖所示的新網面：

   ![建立提取要求](media/index/create-pull-request.png)

   按一下 [建立提取要求]  並輸入提取要求的標題 (也可以選擇輸入描述)，然後再按一下 [建立提取要求]  。 (如果您沒有使用過 GitHub，請參閱 [About Pull Requests](https://help.github.com/en/articles/about-pull-requests) (關於提取要求) 以取得詳細資訊。)

6. 大功告成！ 內容小組成員將檢閱並合併您的 PR。 如果您做出較大規模的變更，則可能會收到一些要求變更的意見反應。

GitHub 編輯 UI 會回應您對存放庫的權限。 上述影像適用於不具有目標存放庫寫入權限的參與者。 GitHub 會自動在您的帳戶中建立目標存放庫的分叉。 如果您有目標存放庫的寫入權限，GitHub 會在目標存放庫中建立一個新的分支。 分支名稱的格式為 **\<GitHubId\>-patch-n**，並使用您的 GitHub 識別碼，以及針對修補分支的數值識別碼。

我們會使用提取要求來進行所有變更，即使對擁有寫入權限的參與者也是如此。 大多數存放庫都會保護其 `master` 分支，因此必須將更新提交為提取要求。

瀏覽器內編輯體驗，最適合用於小規模或非常態的變更。 如果您做出較大規模的貢獻，或是使用進階 Git 功能 (例如分支管理或進階的合併衝突解決)，則需要[派生存放庫並在本機處理](how-to-write-workflows-major.md)。

> [!NOTE]
> 若已啟用，您能以**任何語言**編輯文章，而且根據編輯類型，將會發生下列情況：
> 1. 已核准的任何語言變更將也能協助我們改進機器翻譯引擎
> 2. 任何大幅修改文章內容的編輯都會交由內部處理，以對同一篇文章的英文版提交變更，使其在核准後可以當地語系化成所有語言。
> 您建議的改進不僅能對您自己的語言產生正面影響，對所有語言也是。

## <a name="review-open-prs"></a>檢閱未處理的 PR

您可以透過查看目前未處理的 PR，來在新主題發佈之前閱讀它們。 檢閱需遵循 [GitHub 流程](https://guides.github.com/introduction/flow/) \(英文\) 的程序。 您可以查看公開存放庫中的建議更新或新文章。 請檢閱它們並新增您的意見。 查看我們的文件存放庫，並針對您感興趣的領域查看未處理的提取要求 (PR)。 任何針對建議更新的社群意見反應，都能為整個社群提供協助。

## <a name="create-quality-issues"></a>建立品質問題

我們的文件都是持續進行中的工作。 好的問題有助於我們將工作重點放在社群的最高優先事項上。 您可以提供的細節越多，該問題就越有幫助。 請告訴我們您想要的資訊。 請告訴我們您所使用的搜尋字詞。 如果您無法開始使用，請告訴我們您想要如何開始探索不熟悉的技術。

許多 Microsoft 文件頁面底部都有 [意見反應]  區段，在其中按一下即可留下 [產品意見反應]  或 [內容意見反應]  以追蹤該文章的特定問題。

問題能促進所需項目的相關討論。 內容小組將回應這些問題，提供我們可以新增內容的想法，並徵求您的意見。 當我們建立草稿時，我們會要求您[檢閱 PR](#review-open-prs)。

## <a name="get-more-involved"></a>深入參與

其他主題可協助您開始有效率地為 Microsoft Docs 做出貢獻。這些主題會說明如何使用 GitHub 存放庫、Markdown 工具，以及 Microsoft Docs 平台所使用的延伸模組。
