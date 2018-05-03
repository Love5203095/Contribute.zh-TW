---
title: 適用於次要或不頻繁變更的 GitHub 參與工作流程
description: 本文示範如何使用「次要」參與者工作流程為 docs.microsoft.com 文章做出貢獻。
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 10/06/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 8bde44d502e1942b0870df9dd546a97705c2bb4f
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2018
---
# <a name="github-contribution-workflow-for-minor-or-infrequent-changes"></a>適用於次要或不頻繁變更的 GitHub 參與工作流程

> [!IMPORTANT]
> 所有發佈至 docs.microsoft.com 的存放庫皆採用 [Microsoft 開放原始碼管理辦法](https://opensource.microsoft.com/codeofconduct/) \(英文\) 或 [.NET Foundation 管理辦法](https://dotnetfoundation.org/code-of-conduct) \(英文\)。 如需詳細資訊，請參閱[管理辦法常見問題集](https://opensource.microsoft.com/codeofconduct/faq/) \(英文\)。 若有任何問題或意見，也可以連絡 [opencode@microsoft.com](mailto:opencode@microsoft.com) 或 [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org)。<br>
>
> 您在公用存放庫中針對文件和程式碼範例所提交的次要修正或釐清，將受到 [docs.microsoft.com 使用條款](https://docs.microsoft.com/legal/termsofuse)的約束。 如果您不是 Microsoft 的員工，在做出全新或重要的變更時，系統將會在提取要求中產生意見，要求您提交線上版的貢獻授權合約 (CLA)。 您必須先完成填寫線上表單，我們才會接受您的提取要求。

## <a name="overview"></a>概觀

此工作流程會使用 GitHub 的網頁型 Markdown 編輯器，以進行次要或不頻繁的變更。 GitHub 編輯器所提供的功能有限，因為其 UI 並不支援所有 Git 作業及撰寫案例。 如果您需要做出較大幅度的參與，或是需要進階 Git 功能 (例如分支管理或進階的合併衝突解決方式) 的支援，請參閱[主要或長期變更工作流程](full-workflow.md)。

## <a name="procedure-for-using-the-github-editor-to-propose-your-changes"></a>使用 GitHub 編輯器來建議變更的程序

1. 瀏覽至文章相對應的 GitHub 存放庫和 Markdown 檔案。 您可以使用下列其中一種方法：

   - 透過在相關的 GitHub 存放庫中瀏覽 Markdown 檔案以找出該篇文章。
   - 於 [docs.microsoft.com](https://docs.microsoft.com/) 上移至該篇文章，然後選取頁面右上角的 [編輯] 連結。

     ![[編輯] 連結的位置](./media/light-workflow/contributetogit.png)

2. 選取 [編輯此檔案] 鉛筆圖示來進入編輯模式︰

    ![鉛筆圖示的位置](./media/light-workflow/editicon.png)

3. 透過在 [編輯檔案] 索引標籤上使用 Markdown 來做出變更，並在 [預覽變更] 索引標籤上預覽您的變更。編輯器的使用方法相當直覺，但如果需要協助，請參閱下列指南：

   - [如何使用 Markdown](how-to-write-use-markdown.md)
   - [在 GitHub 上建立檔案](https://github.com/blog/1327-creating-files-on-github) \(英文\)
   - [將檔案上傳至您的存放庫](https://github.com/blog/2105-upload-files-to-your-repositories) \(英文\)

4. 捲動至頁面底部，您將會看見下列其中一項：

   - **建議檔案變更**：會在您針對存放庫具有唯讀存取權時顯示，例如當您在[編輯另一個使用者的存放庫檔案時](https://help.github.com/articles/editing-files-in-another-user-s-repository/) \(英文\)。 在此情況下，GitHub 會在您的存放庫分叉中建立「修補」分支 (如果分叉不存在，系統將會自動建立)。 當您選取 [建議檔案變更] 之後，[比較變更] 頁面便會出現，以供您確認自己的變更。 接著，請選取 [建立提取要求] 按鈕以將變更提交至提取要求佇列，並繼續移至[下一節](#pull-request-processing)。

   - **認可變更**：會在您針對存放庫具有寫入權限時顯示，例如當您在[編輯自己的存放庫檔案時](https://help.github.com/articles/editing-files-in-your-repository/) \(英文\)。 在此情況下，GitHub 會給您兩個儲存變更的選項：

     - **直接認可至 `<branch-name>` 分支**：其中 `<branch-name>` 是您選取 [編輯] 按鈕時所處於的分支名稱。 這會將您的變更直接套用至分支，而不會使用提取要求。 到這裡您就已經完成了！

     - **針對此認可建立新分支並啟動提取要求**：這會向您顯示預設名稱以建立新的分支。 當您選取 [建議檔案變更] 之後，[比較變更] 頁面便會出現，以供您確認自己的變更。 接著，請選取 [建立提取要求] 按鈕以將變更提交至提取要求佇列，並繼續移至[下一節](#pull-request-processing)。

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## <a name="next-steps"></a>後續步驟

- 請繼續移至＜有關撰寫的基本資訊＞文章，以深入了解 Markdown 和 Markdown 擴充功能語法等內容。
