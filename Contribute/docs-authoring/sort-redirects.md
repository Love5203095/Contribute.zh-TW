---
title: 排序重新導向 - Docs 編寫套件
description: 瞭解如何使用 Docs 編寫套件 (Visual Studio Code 延伸模組) 來排序重新導向。
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 4924c631c8720743c283083e53b3a1e9af86b00a
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336673"
---
# <a name="sort-redirects"></a>排序重新導向

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>摘要

隨著 docs.microsoft.com 文件集的演進，部分 Markdown 檔案最後會被刪除。 刪除 Markdown 檔案時，我們必須提供重新導向，透過重新導向正確地處理指向已刪除文章的任何參考連結。 重新導向是在 .openpublishing.redirection.json  檔案中指定。

1. 開啟命令選擇區，按 <kbd>F1</kbd> (或 macOS 上的 <kbd>⇧⌘ P</kbd>)
1. 輸入：**Docs:Sort master redirection file**
1. 選取要執行的命令
1. 觀察 .openpublishing.redirection.json  檔案的變更

## <a name="considerations"></a>考量

.openpublishing.redirection.json  檔案設計之初便有「菊鍊」的概念。 一段時間後，以重新導向新增的檔案終將過時。 刪除檔案 A 需要重新導向至檔案 B，之後刪除檔案 B 再重新導向至檔案 C，就是這種情況。理想情況下，前兩個項目都會指向 C：讓 A 重新導向至 C，而 B 保持導向至 C。 這是小幅的效能提升，我們正積極改善此功能。

## <a name="in-action"></a>操作實況

以下是這項功能的簡短示範。

[![排序重新導向示範](media/sort-redirect.gif)](media/sort-redirect.gif#lightbox)
