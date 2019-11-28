---
title: insecure-link
description: Docs 組建問題 issue-insecure-link 的說明和解決方式
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4735d47cdf2029d2c613c9b333a393c7d978c58e
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528854"
---
# <a name="insecure-link"></a>insecure-link

> [!IMPORTANT]
> 此規則一開始以「建議」的形式啟用，讓內容小組有時間可以評估影響，以及發展清理其存放庫的計劃。 **在 2019/12/20，它將會提升為「警告」** 。

## <a name="suggestion"></a>建議

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

此訊息表示您與 `http` 搭配使用了明確的 Markdown 連結，或原始 URL (例如 `www.microsoft.com`)。 原始 URL 會在發佈至 Docs 時轉換成不安全的連結，因此不應使用。

## <a name="resolution"></a>解決方式

將所有 Microsoft 網站的 URL 變更為使用 `https` 而非 `http`。

若您的連結是原始 URL，請將其變更為以 `https` 開頭的明確 Markdown 連結，例如：

```md
`[www.microsoft.com](https://www.microsoft.com)`.
```

> [!TIP]
> VS Code 的 Docs Markdown 延伸模組包含清除指令碼 (適用於 Microsoft 連結)。 指令碼會檢查存放庫中所有 Microsoft 網站的連結，確保它們的開頭都是 `https` 而非 `http`，且未包含地區設定代碼 (例如 `en-us`)。 執行指令碼：
>
> 1. 安裝 VS Code 的 [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) 延伸模組。
> 1. 按一下 alt + M 來開啟 Markdown 功能表。
> 1. 選取 [Cleanup] \(清除\)  ，然後選取 [Microsoft links] \(Microsoft 連結\)  。

在某些情況下，您可能需要記下沒有要建立成可按式連結的網址 (例如完整網域名稱)。 這些網址的樣式應為內嵌程式碼，例如：

```md
`www.microsoft.com:90`
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
