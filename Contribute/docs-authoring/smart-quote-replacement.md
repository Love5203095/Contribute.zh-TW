---
title: 自動智慧引號取代 - Docs 編寫套件
description: 瞭解如何使用 Docs 編寫套件 (Visual Studio Code 延伸模組) 來進行自動智慧引號取代。
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 048f244324d7dde540c78e6631ccb5abbed3e431
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336696"
---
# <a name="smart-quote-replacement"></a>智慧引號取代

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>摘要

內容開發人員負責撰寫現代化技術和情報的一些最先進的功能，然而現今的工具仍偏好在 Markdown 中使用「笨蛋引號」。 就怕「智慧引號」聰明反被聰明誤。 智慧引號常見於完美的字型設計上，但在 Markdown 和轉譯 HTML 上並不常用。

例如，您可能已經注意到，在處理 Microsoft Word 文件時，當您按住 <kbd>Shift</kbd> 並輸入 <kbd>"</kbd> 時，Microsoft Word 會快速地將 `"` 字元取代為相當於 `“` 字元的智慧引號。

| Description        | Unicode  | 智慧引號 | 取代 |
|--------------------|----------|-------------|-------------|
| 左雙引號  | `\u201c` | `“`         | `"`         |
| 右雙引號 | `\u201d` | `”`         | `"`         |
| 左單引號  | `\u2018` | `‘`         | `'`         |
| 右單引號 | `\u2019` | `’`         | `'`         |

在 Markdown (.md *\** ) 檔案中，當您貼上文字或更新內容時，這項功能會主動評估內容，並據此自動取代值。

> [!NOTE]
> 「智慧引號取代」功能也會取代其他字元，例如但不限於 `©, ™, ®, •`、下標和上標字元。 從 Word 文件貼入文字時，這很有用。

## <a name="preferences"></a>喜好設定

這是選擇性功能，但預設為 `true`。 開啟或關閉此功能：

1. 選取 [檔案]   >  [喜好設定]   >  [設定]  ，然後依 *Docs Markdown Extension* 篩選。
1. 開啟或關閉 [Markdown:  取代智慧引號] 區段中的設定。

## <a name="in-action"></a>操作實況

以下是這項功能的簡短示範。

[![取代智慧引號示範](media/replace-smart-quotes.gif)](media/replace-smart-quotes.gif#lightbox)
