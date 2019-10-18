---
title: 撰寫 Cmdlet 參考的特定指導
description: 本文提供格式化 PowerShell 程式碼範例的特定規則。 這適用於包含範例的概念文章，以及 Cmdlet 參考。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 793a3c02ae0edf192416ae514585d5161e8c1f98
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290280"
---
# <a name="updating-reference-articles"></a>更新參考文章

Cmdlet 參考文章具有特定結構。 此結構是由 [PlatyPS][] 定義。
PlatyPS 是我們用來產生 PowerShell 模組 Cmdlet 說明的工具。 PlatyPS 會為 Cmdlet 建立基底 Markdown 檔案。 在編輯 Markdown 檔案後，PlatyPS 會用來建立 `Get-Help` Cmdlet 使用的 MAML 說明檔。

PlatyPS 包含寫入程式碼中 Cmdlet 參考的硬式編碼結構描述。 [platyPS.schema.md][] 文件會嘗試描述此結構。 結構描述違規會造成建置錯誤；您必須先修正這些錯誤，我們才可以接受您的貢獻。

## <a name="general-guidelines"></a>一般方針

- 請勿移除任何標頭結構。 PlatyPS 需要一組特定的標頭。
- **輸入類型**和**輸出類型**標頭必須具備類型。 若 Cmdlet 不會接受輸入或是傳回任何值，請使用 "None" 值。
- 只有[範例](#format-for-examples)區段才允許圍住的程式碼區塊。
- 內嵌的程式碼範圍則可用於任何段落。

## <a name="formatting-about_-files"></a>格式化 About_ 檔案

`About_*` 檔案現在會由 [Pandoc][] 處理，而非 PlatyPS。 `About_*` 檔案會針對 PowerShell 所有版本及發行工具的最佳相容性進行格式化。
請不要在沒有和存放庫維護人員進行確認的情況下改變 `about_*` 檔案的格式。

基本格式化指導方針：

- 將行限制在 80 個字元
- 程式碼區塊、區塊引述和表格會限制在 76 個字元，因為 Pandoc 會在轉換時針對這些內容以四個空格進行縮排
- 表格需要容納在 76 個字元內
  - 針對多行的儲存格內容手動進行換行
  - 在每一行使用開頭和結尾的 `|` 字元
  - 請參閱 [about_Comparison_Operators][about-example] 中的運作範例
- 使用 Pandoc 的特殊字元 `\`、`$`、`` ` `` 和 `<`
  - 在標頭內 - 這些字元必須使用前置 `\` 字元進行逸出
  - 在段落內 - 這些字元應放在程式碼範圍內。 例如：

    ~~~markdown
    ### The purpose of the \$foo variable

    The `$foo` variable is used to store ...
    ~~~

## <a name="format-for-examples"></a>範例格式

在 PlatyPS 結構描述中，**EXAMPLES** 標頭為 H2 標頭，且每個範例為 H3 標頭。

在範例中，結構描述不允許使用段落來分隔程式碼區塊。 有效的結構描述為：

```
### Example #X title

0 or more paragraphs
1 or more code blocks
0 or more paragraphs.
```

為每個範例加上編號，並新增簡短標題。

例如：

~~~markdown
### Example 1: Get cmdlets, functions, and aliases

This example gets the PowerShell cmdlets, functions, and aliases that are installed on the
computer.

```powershell
Get-Command
```
~~~


[PlatyPS]: https://github.com/powershell/platyps
[platyPS.schema.md]: https://github.com/PowerShell/platyPS/blob/master/platyPS.schema.md
[issue1806]: https://github.com/PowerShell/PowerShell-Docs/issues/1806
[about-example]: https://github.com/MicrosoftDocs/PowerShell-Docs/blob/staging/reference/6/Microsoft.PowerShell.Core/About/about_Comparison_Operators.md
[Pandoc]: https://pandoc.org