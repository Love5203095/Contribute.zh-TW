---
title: 文字格式設定指導方針
description: 了解在何種情況下於 docs.microsoft.com 網站發佈的文章中使用粗體、斜體、程式碼和其他文字樣式。
author: tdykstra
ms.author: tdykstra
ms.date: 01/30/2020
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 7b6927918c81fdc41e3c3887f94339b225e2a6e6
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336508"
---
# <a name="text-formatting-guidelines"></a>文字格式設定指導方針

對文字項目一致且適當地使用粗體、斜體和程式碼樣式可提升可讀性並避免誤解。

## <a name="bold"></a>粗體

使用粗體來表示使用者介面元素，例如功能表選取項目、對話方塊名稱、輸入欄位名稱。

### <a name="examples"></a>範例

* **正確**：在**方案總管**中，以滑鼠右鍵按一下專案節點，然後選取 **[新增] > [新項目]** 。
* **不正確**：在方案總管中，以滑鼠右鍵按一下專案節點，然後選取 [新增] > [新項目]。
* **不正確**：在*方案總管*中，以滑鼠右鍵按一下專案節點，然後選取 *[新增] > [新項目]* 。

## <a name="italics"></a>斜體

使用斜體來表示：

* 介紹新的字詞，包含其定義或說明。
* 檔案名稱、資料夾名稱、路徑。
* 使用者輸入。

### <a name="examples"></a>範例

* **正確**：在 App Service 中，應用程式會在 *App Service 方案*中執行。 App Service 方案定義一組計算資源供 Web 應用程式執行。
* **不正確**：在 App Service 中，應用程式會在 "App Service 方案" 中執行。 App Service 方案定義一組計算資源供 Web 應用程式執行。
* **正確**：將 *HttpTriggerCSharp.cs* 中的程式碼取代為下列程式碼。
* **不正確**：將 `HttpTriggerCSharp.cs` 中的程式碼取代為下列程式碼。
* **正確**：**名稱**請輸入 *ContosoUniversity*，然後選取**新增**。
* **不正確**：**名稱**請輸入 "ContosoUniversity"，然後選取**新增**。

## <a name="code-style"></a>程式碼樣式

使用程式碼樣式來表示：

* 程式碼項目，例如方法名稱、屬性名稱和語言關鍵字。
* SQL 命令
* NuGet 套件名稱
* 命令列的命令
* 資料庫資料表和資料行名稱
* 不應當地語系化的資源名稱，例如虛擬機器名稱
* 不想讓人按的 URL

**為什麼？** 較舊的樣式指南會為許多這類文字元素指定粗體。 然而，大部分的文章都已當地語系化，而程式碼樣式能告訴譯者保留該部分的文字不要翻譯。

可將程式碼樣式「內嵌」  (以 \` 括住)，或將跨越數行的程式碼區塊「隔離」  (以 \`\`\` 括住)。 請將較長的程式碼片段和路徑放在括住的程式碼區塊中。

### <a name="examples-using-inline-styles"></a>內嵌樣式的範例

* **正確**：根據預設，Entity Framework 會將名為 `Id` 或 `ClassnameID` 的屬性解譯為主索引鍵。
* **不正確**：根據預設，Entity Framework 會將名為 *Id* 或 *ClassnameID* 的屬性解譯為主索引鍵。
* **正確**：`Microsoft.EntityFrameworkCore` 套件提供 EF Core 的執行階段支援。
* **不正確**：*Microsoft.EntityFrameworkCore* 套件提供 EF Core 的執行階段支援。

### <a name="examples-of-fenced-code-blocks"></a>括住的程式碼區塊範例

* **正確**：只變更 `IQueryable` 的陳述式不會將任何命令傳送至資料庫，如下列程式碼：

  ```markdown
      ```csharp
      var students = context.Students.Where(s => s.LastName == "Davolio")
      ```
  ```

* **不正確**：只變更 **IQueryable** 的陳述式不會將任何命令傳送至資料庫，例如 **var students = context.Students.Where(s => s.LastName == "Davolio")** 。

* **正確**：例如，若要在 `C:\Scripts` 目錄中執行 `Get-ServiceLog.ps1` 指令碼，請輸入：

  ```markdown
      ```powershell
      C:\Scripts\Get-ServiceLog.ps1
      ```
  ```

* **不正確**：例如，若要在 **C:\Scripts** 目錄中執行 **Get-ServiceLog.ps1** 指令碼，請輸入："C:\Scripts\Get-ServiceLog.ps1"。

* **所有**隔離的程式碼區塊都必須有已核准的語言標記。 如需支援的語言標記清單，請參閱[如何在 Docs 中包含程式碼](./code-in-docs.md#supported-languages)。

## <a name="headings-and-link-text"></a>標題和連結文字

請不要將斜體、粗體或程式碼等內嵌樣式套用至標題或超連結文字。

**為什麼？**

大眾會根據標準超連結文字確認文字項目為可按的連結。 假如您將連結的樣式設為程式碼，會無法明確表示該文字實際上為連結。 標題有其專屬樣式，混用其他樣式並不美觀。

### <a name="examples"></a>範例

* **正確**：*function.json* 檔案由 NuGet 套件 [Microsoft.NET.Sdk.Functions](http://www.nuget.org/packages/Microsoft.NET.Sdk.Functions) 產生。
* **不正確**：*function.json* 檔案由 NuGet 套件 [`Microsoft.NET.Sdk.Functions`](http://www.nuget.org/packages/Microsoft.NET.Sdk.Functions) 產生。

* **正確**：

  ```markdown
  ### The Microsoft.NET.Sdk.Functions package
  ```

* **不正確**：

  ```markdown
  ### The `Microsoft.NET.Sdk.Functions` package
  ```

## <a name="keys-and-keyboard-shortcuts"></a>鍵盤和鍵盤快速鍵

用到按鍵或按鍵組合時，請遵循下列慣例：

* 將按鍵名稱的第一個字母大寫。
* 不要套用斜體、粗體或程式碼等內嵌樣式。
* 使用 "+" 來聯結同時選取的按鍵。

### <a name="examples"></a>範例

* **正確**：選取 Alt + Ctrl + S。
* **不正確**：選取 **ALT+CTRL+S**。
* **不正確**：點擊 `ALT+CTRL+S`。

如需詳細資訊，請參閱[描述與 UI 的互動](https://styleguides.azurewebsites.net/StyleGuide/Read?id=2700&topicid=26472)。

## <a name="exceptions"></a>例外狀況

樣式指導方針並不是僵化的規則。 在會危害可讀性的情況下，可採行不同的做法。 例如，如果 HTML 資料表中多為程式碼項目，滿滿的程式碼樣式看起來會很擁擠。 您可以在該內容中選擇粗體樣式。

如果您在通常會呼叫程式碼之處選擇使用替代的文字樣式，請確定該文字可以在當地語系化版本的文章中翻譯。 畢竟，程式碼是唯一可以自動防止翻譯的樣式。 如果您想要在不使用程式碼樣式的情況下防止當地語系化，請參閱 [不可當地語系化的字串](markdown-reference.md#non-localized-strings)。
