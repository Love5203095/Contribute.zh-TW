---
title: 開發語言完成 - Docs 編寫套件
description: 瞭解開發語言完成如何協助 Docs 編寫套件 (Visual Studio Code 延伸模組) 的參與者。
author: scottaddie
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: scaddie
ms.openlocfilehash: f81dc2315dc09256639c98ed72484517ff2c6ff3
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336788"
---
# <a name="dev-lang-completion"></a>開發語言完成

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>摘要

參與者需要協助，來判斷 Markdown 檔案中跟在三個倒引號 (程式碼柵欄的開頭) 之後的有效語言識別碼 (dev lang)。 可惜的是，開發語言的組建階段驗證並不存在。 結果是相同概念文件集中的同一語言卻有不同的表示法。

以 C# 為例。 參與者已使用 `c#`、`C#`、`cs`、`csharp` 和其他字眼做為該語言的開發語言表示法。 這些表示法中哪一個正確？

「開發語言完成」  功能會顯示已知的開發語言清單來消除混淆。 從 IntelliSense 中選取開發語言名稱時：

* 程式碼隔離已結尾。
* 插入點位於程式碼隔離中。

## <a name="preferences"></a>喜好設定

無法停用此功能。 可用的設定如下：

* [顯示常用的開發語言](#display-commonly-used-dev-langs)
* [顯示所有已知的開發語言](#display-all-known-dev-langs)

### <a name="display-commonly-used-dev-langs"></a>顯示常用的開發語言

只有有效開發語言的子集會用於單一文件集中。 若要提升使用者體驗：

1. 在 Visual Studio Code 中，開啟文件集根目錄。
1. 選取 [檔案]   >  [喜好設定]   >  [設定]  ，然後依 *Docs Markdown Extension* 篩選。
1. 按一下 [在 settings.json 中編輯]  連結 (位於 [Markdown:  文件集語言] 區段中)。
1. 在 settings.json  檔案中加入以下 `markdown.docsetLanguages` 屬性：

    ```json
    {
        "markdown.docsetLanguages": [

        ]
    }
    ```

1. 將插入點放在屬性的空白陣列中，然後啟動 IntelliSense (透過 <kbd>Ctrl</kbd> + <kbd>Space</kbd>)。 已知的開發語言名稱清單隨即出現。
1. 將開發語言名稱新增至陣列，直到您滿意清單為止。 例如，下列清單會在使用者輸入三個倒引號之後，對使用者顯示四個開發語言名稱：

    ```json
    {
        "markdown.docsetLanguages": [
            ".NET Core CLI",
            "C#",
            "Markdown",
            "YAML"
        ]
    }
    ```

1. 將您的變更儲存到 settings.json  檔案。

> [!WARNING]
> 空的 `markdown.docsetLanguages` 陣列會使所有已知的開發語言都顯示出來。

### <a name="display-all-known-dev-langs"></a>顯示所有已知的開發語言

根據預設，所有已知的開發語言名稱都會顯示在 IntelliSense 中。 此設定會覆寫 [顯示常用的開發語言](#display-commonly-used-dev-langs)中所述的 `markdown.docsetLanguages` 屬性。

變更此設定：

1. 選取 [檔案]   >  [喜好設定]   >  [設定]  ，然後依 *Docs Markdown Extension* 篩選。
1. 開啟或關閉 [Markdown:  所有可用的語言] 區段中的設定。

## <a name="in-action"></a>操作實況

以下是這項功能的簡短示範：

[![開發語言完成](media/dev-lang-completion.gif)](media/dev-lang-completion.gif#lightbox)
