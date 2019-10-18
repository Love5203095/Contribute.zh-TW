---
title: PowerShell 文件存放庫的貢獻流程
description: 本文提供參與 PowerShell 文件存放庫的簡介。 您將了解所使用的存放庫、組織內容的程序，以及管理程式碼範例和其他資產的原則。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/07/2019
ms.openlocfilehash: 9802942dccbfad2cb860739ffba4b30d2b0af0c9
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290188"
---
# <a name="process-for-contributing-to-powershell-docs"></a>參與 PowerShell 文件的流程

感謝社群對文件的參與。下列清單顯示參與 PowerShell 文件時應該注意的一些指導規則：

- **請勿**出其不意地提交大量提取要求。 相反地，請提出一個問題並開始討論，先讓我們就大方向取得共識再投入大量時間。
- **請**遵循這些指示，以及[程式碼](powershell-style-code.md)和[參考](powershell-style-reference.md)的樣式指南。
- **務必**使用[範本](powershell-style-basic-markdown.md)檔案作為您工作的起點。
- **務必**先在您的分支上建立個別分支，再參與文章。
- **務必**遵循 [GitHub 流程的工作流程](../how-to-write-workflows-major.md)。
- **務必**經常針對您的參與撰寫部落格文章和推文 (或透過其他方式)！

遵循這些方針有助於確保您我都有更佳的體驗。

## <a name="make-a-contribution-to-powershell-docs"></a>參與 PowerShell 文件

您可以選擇現有的[問題](https://github.com/MicrosoftDocs/PowerShell-Docs/issues/new/choose)。
根據您的興趣和參與程度，您可以投入下列類別：

- **小型變更** 若變更不大，請參閱參與者指南[首頁](../index.md#quick-edits-to-existing-documents)上有關在 GitHub 中編輯的指示。 小型變更包括：

  - 修正錯字和拼寫錯誤
  - 改善文法或格式
  - 次要技術或實際編輯

- **維護**。 此類別包含相當簡單的參與，例如修正中斷或不正確的連結、新增缺少的程式碼範例，或解決限制的內容問題。 在某些情況下，這些問題可能涉及大量檔案。 在此情況下，您應該讓我們知道您想要參與的內容，再開始進行。 在問題上新增註解，告訴我們您正在參與。

- **內容更新**。 由於文件集很龐大，因此內容很容易就會變得過期而需要修訂。 此外，基於各種不同的原因，某些內容已重複或甚至再三出現。 更新內容時需要確定個別主題是最新的，或修訂功能範圍中的內容，以排除重複出現的情況，並確保以更小的文件集來保留所有唯一內容。

- **撰寫新內容**。 如果您對撰寫自己的主題感興趣，則這些問題會列出我們確定要新增至文件集的主題。 不過在您開始撰寫某個主題之前，請讓我們知道。 如果您對撰寫這裡未列出的主題感興趣，請開啟一個問題。

一旦您選擇了要參與的工作，請遵循[入門](../get-started-setup-github.md)指南以建立 GitHub 帳戶並設定您的環境。

### <a name="making-large-changes"></a>進行大量變更

**步驟 1：** 如果您對撰寫新內容或全面修訂現有內容感興趣，請開啟描述您要執行作業的問題。

**步驟 2：** 派生 `MicrosoftDocs/PowerShell-Docs` 存放庫，並為您的變更建立工作分支。

**步驟 3：** 在此新分支上進行變更。

若這是新主題，請使用[樣式指南](powershell-style-basic-markdown.md)中的範本作為起點。 樣式指南包含撰寫方針，並會說明每篇文章所需的中繼資料。

請巡覽至步驟 1 中針對您文章所決定 TOC 位置的相對應資料夾。
該資料夾包含該區段中所有文章的 Markdown 檔案。 如有需要，請建立新的資料夾來放置您的內容檔案。 該區段的主要文章名為 *index.md*。
針對影像和其他靜態資源，請在包含您文章的資料夾中建立名為 **media** 的子資料夾 (如果尚未存在)。 在 **media** 資料夾中，建立具有文章名稱的子資料夾 (索引檔除外)。

請務必遵循適當的 Markdown 語法。 如需詳細的指示和範例，請參閱[樣式指南](powershell-style-basic-markdown.md)。

**範例結構**

```
reference
  /docs-conceptual
    /learn
      /remoting
        managing-remote-sessions.md
        /images
          /managing-remote-sessions
            sesssion-list.png
```

**步驟 4：** 從您的工作分支提交提取要求 (PR) 至 *staging* 分支。

一般而言，PR 應一次解決一個問題。 PR 可修改一或多個檔案。 如果您要解決不同檔案的多個修正，最好使用個別 PR。

如果您的 PR 會修正現有問題，請將 `Fixes #Issue_Number` 關鍵字新增至認可訊息或 PR 描述。 如此一來，當 PR 合併之後，就會自動關閉問題。 如需詳細資訊，請參閱 [Closing issues via commit messages](https://help.github.com/articles/closing-issues-via-commit-messages/) (透過認可訊息關閉問題)。

PowerShell 小組會檢閱您的 PR，並讓您知道是否需要任何其他變更以通過核准。

**步驟 5：** 根據與小組的討論結果，對您的分支進行任何必要的更新。

PR 獲得核准之後，維護人員會將您的 PR 合併到 *staging* 分支。 我們會定期將 *staging* 分支中的所有提交推送到 *live* 分支。 當您的貢獻上線後，您便可以在 [PowerShell 文件網站](https://docs.microsoft.com/PowerShell/)看見它。 通常，我們會在工作週的期間內發佈二到三次。

## <a name="contributor-license-agreement"></a>參與者授權合約

您必須簽署[貢獻授權合約 (CLA)](https://cla.opensource.microsoft.com/MicrosoftDocs/PowerShell-Docs) 才能合併 PR。 這是對文件進行貢獻時所要進行的一次性需求。

您不需要事先簽署合約。 您可以如往常般複製、派生及提交 PR。
當您的 PR 建立之後，會由 CLA Bot 進行分類。 如果變更不大 (例如修正錯字)，則 PR 會標記為 `cla-not-required`。 否則，它會分類為 `cla-required`。 一旦您簽署了 CLA，目前和所有未來提取要求都會標記為 `cla-signed`。
