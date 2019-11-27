---
title: h1-in-moniker
description: Docs 組建問題 h1-in-moniker 的說明和解決方式。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: f22ce2c9e2a014e4d8bf0ae9b61fa48b11d8c9a1
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528814"
---
# <a name="h1-in-moniker"></a>h1-in-moniker

## <a name="warning"></a>警告

`H1s are not allowed in moniker sections. Each article should have one and only one H1.`

H1 指的是 Markdown 檔案中的第一個標題。 當發佈到 docs.microsoft.com 時，H1 會以大型字體顯示在頁面頂端。 H1 的建立方式為以單一井字 (#) 開始一行文字，其後跟隨一個空格，接著為標題文字。 您在每個檔案中只能有一個 H1。 Moniker 區段中不允許 H1，因為取決於版本設定的設定方式，Moniker 中的 H1 容易造成重複或遺漏項目。

若 Moniker 區段包含一行組成雙底線的等號 (`=======`)，您可能也會收到此訊息。 這是 H1 的替代 Markdown 語法。 在合併衝突中也經常會看到它：

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

## <a name="resolution"></a>解決方式

若要修正此問題，請從所有 Moniker 區段移除 H1，並確保文章頂端的 H1 對所有 Moniker 區段均為適當。 請注意，不允許略過標題層級，例如在 H1 後面接著 H3。

若 Moniker 區段中的 H1 實際上是雙底線 (`=======`)，請移除它或適當地將它替換成主題標籤標頭 (例如 `##`)。 若雙底線是合併衝突的一部分，請務必也移除合併衝突的開頭和結尾標記，以及已淘汰的文字。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
