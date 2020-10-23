---
title: 參與 .NET 文件存放庫中的 .NET 程式碼分析規則文件編審
description: 此文章描述在 .NET 文件存放庫中參與 .NET 程式碼分析規則相關文章與程式法範例編審的程序。
author: mavasani
ms.author: mavasani
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 10/09/2020
ms.openlocfilehash: 27ae1a31c55c41aa1c97bf1f88dbf28bec35a80a
ms.sourcegitcommit: f1535713b66ff9b840f1138583746bc2bf182b4f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/12/2020
ms.locfileid: "91957040"
---
# <a name="contribute-docs-for-net-code-analysis-rules-to-the-net-docs-repository"></a>參與 .NET 文件存放庫中的 .NET 程式碼分析規則文件編審

.NET 編譯器平台 (Roslyn) 分析器會檢查 C# 或 Visual Basic 程式碼以找出程式碼品質與程式碼樣式問題。 從 .NET 5.0 開始，這些分析器即[隨附於 .NET SDK](/dotnet/fundamentals/code-analysis/overview)。

- [程式碼品質分析 ("CAxxxx" 規則)](/dotnet/fundamentals/code-analysis/overview#code-quality-analysis):
  - 已在 `dotnet/roslyn-analyzers` 存放庫中於[這裡](https://github.com/dotnet/roslyn-analyzers/tree/master/src/NetAnalyzers)實作。
  - 已在 `dotnet/docs` 存放庫中記載在[這裡](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/quality-rules)。 請參閱[參與 'CAxxxx' 規則相關文件的編審](#contribute-docs-for-caxxxx-rules)。
- [程式碼樣式分析 ("IDExxxx" 規則)](/dotnet/fundamentals/code-analysis/overview#code-style-analysis)：
  - 已在 `dotnet/roslyn` 存放庫中於[這裡](https://github.com/dotnet/roslyn/tree/master/src/Analyzers)實作。
  - 已在 `dotnet/docs` 存放庫中記載在[這裡](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/style-rules)。 請參閱[參與 'IDExxxx' 規則相關文件的編審](#contribute-docs-for-idexxxx-rules)。

## <a name="contribute-docs-for-caxxxx-rules"></a>參與 'CAxxxx' 規則相關文件的編審

請依照下列步驟在 [dotnet/docs](https://github.com/dotnet/docs) 存放庫中參與程式碼品質分析規則相關文件的編審：

1. 判斷 `Rule ID` 與 `Category`：確定您知道要記載之規則的 'CAxxxx' 規則識別碼與類別。 這表示您的 CA 分析器已合併到 [dotnet/roslyn-analyzers](https://github.com/dotnet/roslyn-analyzers) 存放庫，或您有未決的 PR 且該 PR 具有指派到該規則的已核准識別碼與類別。
2. 新增規則文件：
   1. 在 [root](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/quality-rules) 資料夾下複製現有的 CA 規則檔案，假設其為 `ca1000.md`，並將其重新命名。
   2. 適當地更新該檔案的內容。
3. 將規則的項目新增到下列資料表：
   - 在規則類別清單下的[目錄](https://github.com/dotnet/docs/blob/master/docs/fundamentals/toc.yml)檔案中。 例如，針對具有 `Performance` 類別的 CA 規則，請在檔案中搜尋字詞 `- name: Performance rules` 並新增項目到清單中。 若沒有任何類別清單在，請在 `- name: Code quality rules` 下建立新的類別清單。
   - 在[頂層規則索引](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/quality-rules/index.md)檔案中。
   - 在 `category` 型規則索引檔案中：
     1. 在 [root](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/quality-rules) 資料夾下識別類別型索引檔案。 例如，針對具有 `Performance` 類別的 CA 規則，此檔案的名稱為 `performance-warnings.md`。 若沒有任何類別型索引檔案存在，請透過複製現有檔案來建立新檔案。
     2. 在此檔案中新增規則識別碼的項目。

> [!TIP]
> 在 `dotnet/docs` 存放庫中執行存放庫搜尋以尋找已知的現有 CA 規則識別碼，以識別可能需要更新的潛在位置。 如需範例，請參閱 <https://github.com/dotnet/docs/search?q=CA2000>。

## <a name="contribute-docs-for-idexxxx-rules"></a>參與 'IDExxxx' 規則相關文件的編審

請依照下列步驟在 [dotnet/docs](https://github.com/dotnet/docs) 存放庫中參與程式碼樣式分析規則相關文件的編審：

1. 判斷 `Rule ID` 與程式碼樣式選項 (如果有的話)：確定您知道要記載之規則的 'IDExxxx' 規則識別碼與程式碼樣式選項。 這表示 IDE 分析器已合併到 [dotnet/roslyn](https://github.com/dotnet/roslyn) 存放庫，或您有未決的 PR 且該 PR 具有指派到該規則的已核准識別碼與程式碼樣式選項。
2. 判斷規則 `subcategory`：IDE 規則具有類別 `Style`。 透過完整閱讀[程式碼樣式規則](/dotnet/fundamentals/code-analysis/style-rules/index)的簡介小節，來識別規則子類別。 大部分的 IDE 程式碼樣式規則都位於 `Language` 子類別下。
3. 判斷規則 `preference group`：透過在[這裡](/dotnet/fundamentals/code-analysis/style-rules/language-rules#net-style-rules)閱讀喜好設定標頭，來識別規則的 `preference group`。
   - 若規則具有已知、關聯的程式碼樣式選項，則喜好設定群組將會符合程式碼樣式選項宣告中指定的 `OptionGroup`。
   - 否則，判斷規則是否屬於現有的喜好設定群組或需要新增喜好設定群組。
4. 新增規則文件：
   1. 在 [root](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/style-rules) 資料夾下複製現有的 IDE 規則檔案，假設其為 `ide0011.md`，並將其重新命名。
   2. 適當地更新該檔案的內容。
5. 新增 IDE 規則的項目和/或程式碼樣式選項到下列資料表：
   - 在規則子類別與喜好設定清單下的[目錄](https://github.com/dotnet/docs/blob/master/docs/fundamentals/toc.yml)檔案中。 例如，針對具有 `Language` 子類別與 `Modifier preferences` 群組的IDE 程式碼樣式規則，在檔案中搜尋字詞 `- name: Language rules` 與子節點 `- name: Modifier preferences` 並新增項目到清單中。 若子類別下的子類別清單或喜好設定清單不存在，請在 `- name: Code style rules` 下建立新項目。
   - 在[程式碼樣式選項型索引](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/style-rules/language-rules.md)檔案中。
   - 在[規則識別碼型索引](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/style-rules/index.md)檔案中。
   - 在 `preferences group` 型規則索引檔案中：
     1. 在 [root](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/style-rules) 資料夾下識別喜好設定群組型索引檔案。 例如，針對 `Modifier preferences` 的 IDE 規則，此檔案的名稱為 `modifier-preferences.md`。 若沒有任何喜好設定群組型索引檔案存在，請透過複製現有檔案來建立新檔案。
     2. 在此檔案中新增規則識別碼的項目。

> [!TIP]
> 在 `dotnet/docs` 存放庫中執行存放庫搜尋以尋找已知的現有 IDE 規則和/或程式碼樣式選項，以識別可能需要更新的潛在位置。 如需範例，請參閱 <https://github.com/dotnet/docs/search?q=IDE0011> 與 <https://github.com/dotnet/docs/search?q=csharp_prefer_braces>。

## <a name="see-also"></a>另請參閱

- [參與 .NET 文件存放庫](dotnet-contribute.md)
