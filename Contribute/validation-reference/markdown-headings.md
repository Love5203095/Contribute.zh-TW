---
title: Markdown 標題
description: 描述 Markdown 標題的需求。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 05/03/2017
ms.openlocfilehash: 18beb815fdf7caad3e8e675e8d79853d8a5688f2
ms.sourcegitcommit: 6f1997864c000a9cd25fb9171a8f8fdb8b5b5ece
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/11/2018
ms.locfileid: "49084428"
---
# <a name="markdown-headings"></a>Markdown 標題

下列驗證需求適用於 OPS Markdown 檔案中的標題。

## <a name="h1"></a>H1

`H1` 指的是 Markdown 檔案中的第一個標題。 當發佈到 docs.microsoft.com 時，H1 會以大型字體顯示在頁面頂端。

H1 的建立方式為以單一井字 (`#`) 開始一行文字，其後跟隨一個空格，接著為標題文字。 例如，本文的 H1 為：

```md
# Markdown headings
```

下列規則適用於 H1 標題：

- 檔案中必須存在 H1。
- 只能有一個 H1。
- H1 必須包含內容。

  ```markdown
  # 
  This is not allowed.
  ```
- `#` 和 H1 內容間必須有一個空格。 不具空格的 H1 將不會在發佈頁面中轉譯為標題。

  ```markdown
  #This looks bad on the site.
  ```
- H1 必須是檔案中 YML 中繼資料標頭後的第一個內容。 YML 標頭的結尾和 H1 間不允許任何內容 (例如文字或影像)。

  ```markdown
  ---
  ... YML would go here
  ---
  ![cheerful image](not-allowed.jpg)
  # This cheer is not allowed
  ```
- 不應使用第一層標題的 HTML 元素 (`<h1>`)。 使用 Markdown 語法 (`# `)。
- H1 的長度不應超過 100 個字元。 此為樣式方針。

## <a name="h2---h6"></a>H2 到 H6

OPS 中允許 H2 (`## `) 到 H6 (`###### `)。 請使用 Markdown 標頭，而非 HTML (`<h2>` - `<h6>`) 來建立標題。
