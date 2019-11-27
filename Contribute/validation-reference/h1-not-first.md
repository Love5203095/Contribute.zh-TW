---
title: h1-not-first
description: Docs 組建問題 h1-not-first 的說明與解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: 09b91577f4c87125a92c0c116bc07bc7206c6833
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528923"
---
# <a name="h1-not-first"></a>h1-not-first

## <a name="warning"></a>警告

`Markdown content is not allowed before H1.`

只有 YAML 中繼資料標頭可以位於 Markdown 檔案的 H1 之前。 例如，若希望在文章一開頭加入備註或影像，其必須位於 H1 之後。 不允許下列情況：

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
> [!NOTE]
> You can't do this.

# This is the H1
```

請改為執行：

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
# This is the H1

> [!NOTE]
> This is OK.
```

此問題的另一個常見原因是，在 YAML 標頭之前出現[位元組順序標記 (BOM)](http://www.websina.com/bugzero/kb/unicode-bom.html)。 將內容認可至存放庫時，編碼問題有時候會引入這些情況。 因為如此會導致 GitHub 中轉譯不正確，因此應予以移除。

## <a name="resolution"></a>解決方式

移除 H1 之前 YAML 中繼資料標頭以外的所有內容。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
