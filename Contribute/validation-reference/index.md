---
author: meganbradley
ms.author: mbradley
ms.openlocfilehash: fa048980afcf3c50f7d990f9c88064df6ee5ebb5
ms.sourcegitcommit: 6f1997864c000a9cd25fb9171a8f8fdb8b5b5ece
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/11/2018
ms.locfileid: "49084438"
---
# <a name="docs-pr-validation-service"></a>Docs PR 驗證服務

Docs PR 驗證服務是一項 GitHub 應用程式，可在 PR 中於檔案上執行驗證規則。

在存放庫上啟用時驗證服務時，您會看到下列行為：

1. 您提交 PR。
1. 在指出您 PR 狀態的 GitHub 註解中，您會看到存放庫上已啟用的「檢查」狀態。 請注意，在此範例中，有兩項已啟用的檢查：「認可驗證」和「OpenPublishing.Build」：

   ![有些檢查失敗](media/validation-failed.png)

   即使認可驗證失敗，建置也可能會通過。

1. 按一下 [詳細資料] 以取得詳細資訊。
1. 在 [詳細資料] 頁面上，您會看到所有失敗的驗證檢查，其中包含如何修正問題的相關資訊：

   ![驗證訊息](media/validation-details.png)

請參閱本文左側的 TOC，以取得目前服務中的驗證清單。