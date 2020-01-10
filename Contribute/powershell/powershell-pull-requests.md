---
title: 提交提取要求
description: 本文描述 PR 流程和確保您的貢獻可供合併的最佳做法。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 156b5ec7b77bba5cf0a0ef2756ed8b64c21a8342
ms.sourcegitcommit: a812d716b31084926b886b93923f9b84c9b23429
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/18/2019
ms.locfileid: "75188215"
---
# <a name="best-practices-for-pull-requests"></a>提取要求的最佳做法

若要將變更發行到內容，您必須從您的分叉提交提取要求。 每個提取要求在合併前都必須經過檢閱。

## <a name="target-the-correct-branch"></a>以正確的分支為目標

所有變更都應在 `staging` 分支進行。 變更永遠都不應該以 `live` 分支為目標。 在 `staging` 分支中進行的變更會合併到 `live`，因此任何對 `live` 進行的變更都會遭到覆寫。

若您正在提交對文件進行的變更，且該變更僅適用於尚未發行的 PowerShell 版本，請檢查是否有該版本的發行分支。 任何適用於未來特定版本的變更都應以發行分支為目標。 發行分支具有下列名稱模式：`release-<version>`。

## <a name="make-the-pull-request-queue-work-better-for-everyone"></a>使提取要求佇列更利於每個人處理

提取要求佇列中有兩項基本的事實：

- 小範圍和包含相關變更的提取要求所需檢閱時間較少。
- 大範圍或包含不相關變更的提取要求所需檢閱時間較多。

### <a name="avoid-branches-that-update-large-numbers-of-files"></a>避免會更新大量檔案的分支

分隔現有文章的次要更新與新文章或重大重寫。 在個別的工作分支中處理這些變更。

大量變更會造成具有大量變更檔案的 PR。 請將您的 PR 限制在最多 50 個變更檔案。 大型的 PR 不僅難以檢閱，也可能較會包含錯誤。

### <a name="renaming-or-deleting-files"></a>重新命名或刪除檔案

當您重新命名或刪除檔案時，請避免將這些變更與新增或更新的內容混合。
請在個別的 PR 中處理這些變更，使其合併順序晚於針對相關更新的 PR。 例如，請先更新重新導向檔案，並確認重新導向能正常運作，然後再刪除某篇文章。

您必須更新所有連結到重新命名檔案的檔案。 這包含任何 TOC 檔案。 您也必須在存放庫根的主要重新導向檔案 (`.openpublishing.redirection.json`) 中新增重新導向項目。

## <a name="docs-pr-validation-service"></a>Docs PR 驗證服務

Docs PR 驗證服務是一項 GitHub 應用程式，可在 PR 中於檔案上執行驗證規則。

您會看見下列行為：

1. 您提交 PR。
1. 在指出您 PR 狀態的 GitHub 註解中，您會看到存放庫上已啟用的「檢查」狀態。 請注意，在此範例中，有兩項已啟用的檢查：「認可驗證」和「OpenPublishing.Build」：

   ![有些檢查失敗](media/powershell-pull-requests/validation-failed.png)

   即使認可驗證失敗，建置也可能會通過。

1. 按一下 [詳細資料]  以取得詳細資訊。
1. 在 [詳細資料] 頁面上，您會看到所有失敗的驗證檢查，其中包含如何修正問題的相關資訊。
1. 驗證成功時，會將下列註解新增至 PR：

   ![組建驗證](media/powershell-pull-requests/build-validation.png)

若您是外部 (非 Microsoft) 參與者，您將無法存取詳細的組建報告或預覽連結。

### <a name="build-warnings"></a>組建警告

一般而言，您應修正所有建置錯誤、警告和建議。 但是，您可以忽略部分警告。

您可以忽略下列警告：

- > 找不到 `<version>/<modulepath>/About/About.md` 的服務名稱

- > 包含下列名稱的中繼資料不允許在 YAML 標頭中設定，或是設為 docfx.json 中的檔案層級中繼資料，或是 docfx.json 中的全域中繼資料：`locale`。 它們會由 Docs 平台產生，因此在這 3 處設定的值會遭到忽略。 請從這 3 個位置移除它們以解決警告。
