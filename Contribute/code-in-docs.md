---
title: 如何在文件中包含程式碼
description: 了解如何將程式碼元素和程式碼片段包含在文章中，以在 docs.microsoft.com 上發行。
author: tdykstra
ms.author: tdykstra
ms.date: 03/03/2020
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 4aa34196f59a69651dd19add35a0351dd9b5d59b
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336479"
---
# <a name="how-to-include-code-in-docs"></a>如何在文件中包含程式碼

有數種方法可以將程式碼包含在於 docs.microsoft.com 上發行的文章之中：

* 位於文字內的個別元素 (單字)。

  以下是 `code` 樣式的範例。

  當涉及文字裡附近程式碼區塊中的具名參數和變數時，請使用程式碼格式。 程式碼格式也可以用於屬性、方法、類別、語言關鍵字。 如需詳細資訊，請參閱本文稍後的[程式碼項目](#code-elements)。

* 位於文章 Markdown 檔案中的程式碼區塊。

  ```markdown
      ```csharp
      public static void Log(string message)
      {
          _logger.LogInformation(message);
      }
      ```
  ```

  當藉由參考程式碼檔案來顯示程式碼的做法不可行時，請使用內嵌程式碼區塊。 如需詳細資訊，請參閱本文稍後的[程式碼區塊](#inline-code-blocks)。

* 參考本機存放庫中程式碼檔案的程式碼區塊。

  ```markdown
  :::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
  ```

  如需詳細資訊，請參閱本文稍後的[存放庫內的程式碼片段參考](#in-repo-snippet-references)。

* 參考位於另一個存放庫中程式碼檔案的程式碼區塊。

  ```markdown
  :::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
  ```
  
  如需詳細資訊，請參閱本文稍後的[存放庫外的程式碼片段參考](#out-of-repo-snippet-references)。
  
* 讓使用者在瀏覽器中執行程式碼的程式碼區塊。

   ```markdown
  :::code source="PowerShell.ps1" interactive="cloudshell-powershell":::
  ```

  如需詳細資訊，請參閱本文稍後的[互動式程式碼片段](#interactive-code-snippets)。

除了解釋上述包含程式碼方式的 Markdown 之外，文章也會提供一些[針對所有程式碼區塊的一般指引](#code-blocks)。

## <a name="code-elements"></a>程式碼元素

「程式碼元素」為程式設計語言關鍵字、類別名稱、屬性名稱等等。 要界定什麼是程式碼，本身並不是一件簡單明瞭的事。 例如，NuGet 套件名稱應該要視為程式碼進行處理。 若有疑慮，請參閱[文字格式設定指導方針](text-formatting-guidelines.md)。

### <a name="inline-code-style"></a>內嵌程式碼樣式

若要將程式碼元素包含在文章文字中，請以倒引號 (\`) 環繞它以指出程式碼樣式。
內嵌程式碼樣式不應使用三個倒引號格式。

|Markdown |已轉譯 |
|---------|---------|
|根據預設，Entity Framework 會將名為 \`Id\` 或 \`ClassnameID\` 的屬性解譯為主索引鍵。|根據預設，Entity Framework 會將名為 `Id` 或 `ClassnameID` 的屬性解譯為主索引鍵。|

對文章進行當地語系化 (翻譯成其他語言) 之後，樣式被設定為程式碼的文字將不會被翻譯。 如果您想要在不使用程式碼樣式的情況下防止當地語系化，請參閱[不可當地語系化的字串](markdown-reference.md#non-localized-strings)。

### <a name="bold-style"></a>粗體樣式

某些較舊的樣式指南會針對內嵌程式碼指定粗體。 在程式碼樣式非常突兀並會影響可讀性時，便可以使用粗體。 例如，如果 Markdown 資料表中多為程式碼元素，滿滿的程式碼樣式看起來會很擁擠。 如果您選擇使用粗體樣式，請使用 [不可當地語系化的字串語法](markdown-reference.md#non-localized-strings)，確保不會將程式碼當地語系化。

### <a name="links"></a>連結

在某些內容中，指向參考文件的連結可能比程式碼格式更有用。 如果您使用連結，請勿將程式碼格式套用至連結文字。 將連結的樣式設為程式碼，可能會無法明確表示該文字實際上為連結。

如果您使用連結，並於相同內容的稍後又參考相同的元素，請在之後的例項使用程式碼格式 (而不是連結)。

### <a name="placeholders"></a>預留位置

如果您想要讓使用者以自己的值取代顯示的程式碼區段，請使用預留位置文字 (以角括弧或大括弧標示)。 例如：`az group delete -n <ResourceGroupName>`。 說明在替代成實際值時，必須移除角括弧或大括弧。

## <a name="code-blocks"></a>程式碼區塊

在文件中包含程式碼的語法，會視程式碼所在的位置而有所不同：

* [位於文章 Markdown 檔案中](#inline-code-blocks)
* [位於相同存放庫中的程式碼檔案中](#in-repo-snippet-references)
* [位於不同存放庫中的程式碼檔案中](#out-of-repo-snippet-references)

下列指導方針適用於全部三種類型的程式碼區塊：

* [自動化程式碼驗證。](#code-validation)
* [反白顯示關鍵程式碼行。](#highlighting)
* [避免水平捲軸。](#horizontal-scroll-bars)

### <a name="screenshots"></a>螢幕擷取畫面

上一節所列的所有方法都會產生可使用的程式碼區塊：

* 您可以複製並貼上這些區塊。
* 這些區塊均由搜尋引擎編制索引。
* 螢幕助讀程式可以存取這些區塊。

這些只是不建議使用 IDE 螢幕擷取畫面在文章中包含程式碼的其中幾個原因。 只有當您要顯示與 IDE 本身相關的內容時 (例如 IntelliSense)，才使用 IDE 螢幕擷取畫面。 單只為了秀出顏色標示和反白顯示，請勿使用螢幕擷取畫面。

### <a name="code-validation"></a>程式碼驗證

某些存放庫會實作能自動編譯所有範例程式碼以檢查錯誤的處理程序。 .NET 存放庫就做得到。 如需詳細資訊，請參閱 .NET 存放庫中的[參與貢獻](https://github.com/dotnet/docs/blob/master/CONTRIBUTING.md) \(英文\)。

如果您要包含另一個存放庫中的程式碼區塊，對於這些程式碼的維護策略請與其擁有者合作，讓您包含的程式碼不會因為程式碼所使用的程式庫有了新版本而中斷或過期。

### <a name="highlighting"></a>反白顯示

程式碼片段通常會包含比必要程式碼還要多的程式碼，以提供背景內容。 在此情況下，若能將程式碼片段中的關鍵程式碼反白顯示，便能協助提升可讀性，如此範例所示：

![顯示反白顯示程式碼的範例](media/code-in-docs/highlighted-code.png)

當您將程式碼包含在文章 Markdown 檔案中時，將無法反白顯示它。 此功能僅適用於參考程式碼檔案的程式碼片段。

### <a name="horizontal-scroll-bars"></a>水平捲軸

請將較長的行分段，以避免水平捲軸。 程式碼片段上的捲軸會使程式碼較難閱讀。 水平捲軸對較長程式碼區塊的影響更為明顯，因為讀者可能會無法同時看見捲軸和想要閱讀的程式碼行。

想讓程式碼區塊的水平捲軸盡可能最小，其中一個好的做法是將超過 85 個字元的程式碼行分段。 但請記住，捲軸的存在與否不是可讀性的唯一準則。 如果在 85 個字元前中斷一行會影響可讀性或複製貼上的便利性，超過 85 個也無妨。

## <a name="inline-code-blocks"></a>內嵌程式碼區塊

只有當藉由參考程式碼檔案來顯示程式碼的做法不可行時，才使用內嵌程式碼區塊。 相較於完整專案中的程式碼檔案，內嵌程式碼通常比較不容易測試和保持最新狀態。  且內嵌程式碼可能會省略可協助開發人員瞭解及使用程式碼的內容。 這些考量主要適用於程式設計語言。 內嵌程式碼區塊也可以用於輸出和輸入 (例如 JSON)、查詢語言 (例如 SQL)、指令碼語言 (例如 PowerShell)。
  
有兩種方式可以將文章檔案中的某個文字區塊指定為程式碼區塊：將它*隔離*在三個倒引號 (\`\`\`) 之內，或是對它進行縮排。 建議使用隔離的方式，因為它能讓您指定語言。 請避免使用縮排，因為太容易出錯，而且當其他作者需要編輯您的文章時，可能很難瞭解您的意圖。

語言指標是放置在開頭的三個倒引號之後，如下列範例所示：

Markdown：

```markdown
    ```json
    {
        "aggregator": {
            "batchSize": 1000,
            "flushTimeout": "00:00:30"
        }
    }
    ```
```

已轉譯：

```json
{
    "aggregator": {
        "batchSize": 1000,
        "flushTimeout": "00:00:30"
    }
}
```

對於可作為語言指標使用的值，如需相關資訊，請參閱[語言名稱和別名](http://highlightjs.readthedocs.io/en/latest/css-classes-reference.html#language-names-and-aliases) \(英文\)。

如果您放在三個倒引號 (\`\`\`) 後的語言或環境字組不被支援，該字組會出現在轉譯頁面的程式碼區塊標題列中。 盡可能在內嵌程式碼區塊中使用語言或環境指標。

> [!NOTE]
> 如果您從 Word 文件複製並貼上程式碼，請確定其中沒有任何「曲引號」(例如，`“` 和 `’`)，這些在程式碼中無效。 如果有，請將它們變更成一般引號 (`'` 和 `"`)。 或者，依賴 Docs 編寫套件的[智慧引號取代功能](docs-authoring/smart-quote-replacement.md)。

## <a name="in-repo-snippet-references"></a>存放庫內的程式碼片段參考

想要在文件中包含程式設計語言的程式碼片段，建議透過參考程式碼檔案的方式。 這個方法讓您能夠反白顯示一至數行的程式碼，並讓 GitHub 上提供的程式碼片段範圍更廣，以利開發人員使用。 您可以手動方式使用三個冒號格式 (：\:\:)，或在 Visual Studio Code 中借助 [docs.microsoft.com 編寫套件](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)，來包含程式碼。

1. 在 Visual Studio Code 中，按一下 <kbd>Alt + M</kbd> 或 <kbd>選項 + M</kbd>，然後選取 [程式碼片段]。
2. 選取 [程式碼片段] 後，系統會提示您選取 [全文檢索搜尋]、[Scoped Search] \(限定範圍搜尋\) 或 [Cross-Repository Reference] \(跨存放庫參考\)。 若要在本機搜尋，選取 [全文檢索搜尋]。
3. 輸入搜尋字詞以尋找檔案。 找到檔案之後，請選取檔案。
4. 接下來，選取一個選項以決定應在程式碼片段中包含哪些程式碼。 這些選項包括：[識別碼]  、[範圍]  和 [無]  。
5. 根據您在步驟 4 中的選擇，視需要提供值。

顯示完整程式碼檔案：

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs":::
```

透過指定行號來顯示部分程式碼檔案：

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

透過指定程式碼片段名稱來顯示部分程式碼檔案：

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

下列各節將說明這些範例：

* [使用程式碼檔案的相對路徑](#path-to-code-file)
* [僅包含選取的行號](#selected-line-numbers)
* [參考具名的程式碼片段](#named-snippet)
* [反白顯示選取的行](#highlighting-selected-lines)

如需詳細資訊，請參閱本文稍後的[程式碼片段語法參考](#snippet-syntax-reference)。

### <a name="path-to-code-file"></a>程式碼檔案的路徑

範例：

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

此範例是來自 ASP.NET 文件存放庫中的 [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md) \(英文\) 文章檔案。 程式碼檔案的參考方式，是透過針對相同存放庫中 [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) 的相對路徑。

### <a name="selected-line-numbers"></a>選取的行號

範例：

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

這個範例只顯示 *StudentController.cs* 程式碼檔案中的第 2-24 行和第 26 行。

相較於硬式編碼的行號，請盡量使用具名程式碼片段，原因會於下一節中說明。

### <a name="named-snippet"></a>具名的程式碼片段

範例：

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

名稱只能使用字母和底線。

此範例會顯示程式碼檔案的 `snippet_Create` 區段。 這個範例的程式碼檔案會在 C# 的程式碼註解中放上程式碼片段標記：

```cs
// code excluded from the snippet
// <snippet_Create>
// code included in the snippet
// </snippet_Create>
// code excluded from the snippet
```

請盡可能參考具名的區段，而非指定行號。 行號參考較容易出錯，因為程式碼檔案終究會變更，進而使行號產生變更。
而您不一定會收到這些變更的通知。 您的文章最後會開始顯示錯誤的程式碼行，且您將不會意識到這項變更。

### <a name="highlighting-selected-lines"></a>反白顯示選取的行

範例：

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26" highlight="2,5":::
```

此範例會反白顯示行 2 和 5，這是從顯示的程式碼片段開頭開始計算。 要反白顯示的行號並不是從程式碼檔案的開頭開始計算。 換句話說，系統會醒目提示程式碼檔案的第 3 行和第 6 行。

## <a name="out-of-repo-snippet-references"></a>存放庫外的程式碼片段參考

若您想要參考的程式碼檔案位於另一個存放庫，請將該程式碼存放庫設定為「相依存放庫」  。 這麼做時，便需要為它指定名稱。 接著，基於程式碼參考的目的，該名稱會被作為資料夾名稱使用。

例如，文件存放庫為 *Azure/azure-docs*，且程式碼存放庫為 *Azure/azure-functions-durable-extension*。

在 *azure-docs* 的根資料夾中，新增 *.openpublishing.publish.config.json* 中的下列區段：

```json
    {
      "path_to_root": "samples-durable-functions",
      "url": "https://github.com/Azure/azure-functions-durable-extension",
      "branch": "master",
      "branch_mapping": {}
    },
```

現在，當您以 azure-docs  中資料夾的形式參考 sample-durable-functions  時，實際上是在參考 azure-functions-durable-extension  存放庫中的根資料夾。

您可以手動方式使用三個冒號格式 (：\:\:)，或在 Visual Studio Code 中借助 [docs.microsoft.com 編寫套件](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)，來包含程式碼。

1. 在 Visual Studio Code 中，按一下 <kbd>Alt + M</kbd> 或 <kbd>選項 + M</kbd>，然後選取 [程式碼片段]。
2. 選取 [程式碼片段] 後，系統會提示您選取 [全文檢索搜尋]、[Scoped Search] \(限定範圍搜尋\) 或 [Cross-Repository Reference] \(跨存放庫參考\)。 若要搜尋不同的存放庫，請選取 [Cross-Repository Reference] \(跨存放庫參考\)。
3. *.openpublishing.publish.config.json* 會提供您存放庫選項。 選取存放庫。
4. 輸入搜尋字詞以尋找檔案。 找到檔案之後，請選取檔案。
5. 接下來，選取一個選項以決定應在程式碼片段中包含哪些程式碼。 這些選項包括：[識別碼]  、[範圍]  和 [無]  。
6. 根據您在步驟 5 中的選擇提供值。

您的程式碼片段參考看起來如下：

```markdown
:::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
```

在 *azure-functions-durable-extension* 存放庫中，該程式碼檔案是位於 *samples/csx/shared* 資料夾中。 如[先前所述](#highlighting-selected-lines)，反白顯示行的行號是相對於程式碼片段開頭，而不是檔案的開頭。

> [!NOTE]
> 您指派給相依存放庫的名稱是相對於主要存放庫的根目錄，但波狀符號 (~) 則是指文件集的根目錄。 文件集根目錄是由 .openpublishing.publish.config.json  中的 `build_source_folder` 決定。 在上述範例中，程式碼片段的路徑適用於 azure-docs 檔存放庫，因為 `build_source_folder` 是指存放庫根目錄 (`.`)。 如果 `build_source_folder` 是 `articles`，路徑的開頭會是 `~/../samples-durable-functions`，而不是 `~/samples-durable-functions`。

## <a name="interactive-code-snippets"></a>互動式程式碼片段

### <a name="inline-interactive-code-blocks"></a>內嵌互動式程式碼區塊

針對下列語言，可以使程式碼片段能在瀏覽器視窗中執行：

* Azure Cloud Shell
* Azure PowerShell Cloud Shell
* C# REPL

在啟用互動模式的情況下，所呈現的程式碼方塊會顯示 [試試看]  或 [執行]  按鈕。 例如：

```markdown
    ```azurepowershell-interactive
    New-AzResourceGroup -Name myResourceGroup -Location westeurope
    ```
```

會轉譯為：

```azurepowershell-interactive
New-AzResourceGroup -Name myResourceGroup -Location westeurope
```

若要針對特定程式碼區塊開啟此功能，請使用特殊的語言識別項。 可用的選項包括：

* `azurepowershell-interactive` - 啟用 Azure PowerShell Cloud Shell，如上述範例所示
* `azurecli-interactive` - 啟用 Azure Cloud Shell
* `csharp-interactive` - 啟用 C# REPL

針對 Azure Cloud Shell 和 PowerShell Cloud Shell，使用者可以僅針對其 Azure 帳戶執行命令。

### <a name="code-snippets-included-by-reference"></a>以參考方式包含程式碼片段

您可以針對依參考所包含的程式碼片段啟用互動模式。 以下為範例：

```markdown
:::code source="PowerShell.ps1" interactive="cloudshell-powershell":::
```

```markdown
:::code source="Bash.sh" interactive="cloudshell-bash":::
```

若要針對特定程式碼區塊開啟此功能，請使用 `interactive` 屬性。 可用的屬性值如下：

* `cloudshell-powershell` - 啟用 Azure PowerShell Cloud Shell，如上述範例所示
* `cloudshell-bash` - 啟用 Azure Cloud Shell
* `try-dotnet` - 啟用 Try .NET
* `try-dotnet-class` - 以類別 Scaffolding 啟用 Try .NET
* `try-dotnet-method` - 以方法 Scaffolding 啟用 Try .NET

針對 Azure Cloud Shell 和 PowerShell Cloud Shell，使用者可以僅針對其 Azure 帳戶執行命令。

## <a name="snippet-syntax-reference"></a>程式碼片段語法參考

語法：

```md
:::code language="<language>" source="<path>" <attribute>="<attribute-value>":::
```

> [!IMPORTANT]
> 此語法是區塊 Markdown 延伸。 必須用於本身的行。

* `<language>` (選擇性  )
  * 程式碼片段的語言。 如需詳細資訊，請參閱本文稍後的[＜支援的語言＞](#supported-languages)一節。

* `<path>` (強制  )
  * 檔案系統中的相對路徑，表示要參考的程式碼片段檔案。

* `<attribute>` 與 `<attribute-value>` (選擇性  )
  * 同時使用以指定從檔案擷取程式碼的方式以及如何顯示程式碼：
    * `range`：`1,3-5`行的範圍。 此範例包含第 1、3、4 及 5 行。
    * `id`：`snippet_Create` 需要從程式碼檔案插入的程式碼片段識別碼。 這個值與範圍不能並存。
    * `highlight`：`2-4,6` 需要在產生的程式碼片段中醒目提示的範圍及/或行數。 編號是相對於顯示的行 (如範圍或識別碼所指定)，而不是檔案。
    * `interactive`：`cloudshell-powershell`、`cloudshell-bash`、`try-dotnet`、`try-dotnet-class`、`try-dotnet-method` 字串值決定啟用的互動功能類型。
    * 如需程式碼片段原始程式檔中依語言分類的標籤名稱表示法詳細資料，請參閱 [DocFX 指南](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file)。

## <a name="supported-languages"></a>支援的語言

[Docs 編寫套件](how-to-write-docs-auth-pack.md) 有一項功能，可提供陳述式完成和驗證程式碼隔離區塊的可用語言識別碼。

### <a name="fenced-code-blocks"></a>隔離的程式碼區塊

| Name                           | 有效的別名                                                                  |
|--------------------------------|--------------------------------------------------------------------------------|
| .NET Core CLI                  | `dotnetcli`                                                                    |
| 1C                             | `1c`                                                                           |
| ABNF                           | `abnf`                                                                         |
| Access 記錄                    | `accesslog`                                                                    |
| Ada                            | `ada`                                                                          |
| XML 組譯工具                  | `armasm`, `arm`                                                                |
| AVR 組譯工具                  | `avrasm`                                                                       |
| ActionScript                   | `actionscript`, `as`                                                           |
| Alan                           | `alan`, `i`                                                                    |
| AngelScript                    | `angelscript`, `asc`                                                           |
| ANTLR                          | `antlr`                                                                        |
| Apache                         | `apache`, `apacheconf`                                                         |
| AppleScript                    | `applescript`, `osascript`                                                     |
| Arcade                         | `arcade`                                                                       |
| AsciiDoc                       | `asciidoc`, `adoc`                                                             |
| AspectJ                        | `aspectj`                                                                      |
| ASPX                           | `aspx`                                                                         |
| ASP.NET (C#)                   | `aspx-csharp`                                                                  |
| ASP.NET (VB)                   | `aspx-vb`                                                                      |
| AutoHotkey                     | `autohotkey`                                                                   |
| AutoIt                         | `autoit`                                                                       |
| Awk                            | `awk`, `mawk`, `nawk`, `gawk`                                                  |
| Axapta                         | `axapta`                                                                       |
| AzCopy                         | `azcopy`                                                                       |
| Azure CLI                      | `azurecli`                                                                     |
| Azure CLI (互動式)        | `azurecli-interactive`                                                         |
| Azure Powershell               | `azurepowershell`                                                              |
| Azure Powershell (互動式) | `azurepowershell-interactive`                                                  |
| Bash                           | `bash`, `sh`, `zsh`                                                            |
| Basic                          | `basic`                                                                        |
| BNF                            | `bnf`                                                                          |
| C                              | `c`                                                                            |
| C#                             | `csharp`, `cs`                                                                 |
| C# (互動式)               | `csharp-interactive`                                                           |
| C++                            | `cpp`, `c`, `cc`, `h`, `c++`, `h++`, `hpp`                                     |
| C++/CX                         | `cppcx`                                                                        |
| C++/WinRT                      | `cppwinrt`                                                                     |
| C/AL                           | `cal`                                                                          |
| Cache Object Script            | `cos`, `cls`                                                                   |
| CMake                          | `cmake`, `cmake.in`                                                            |
| Coq                            | `coq`                                                                          |
| CSP                            | `csp`                                                                          |
| CSS                            | `css`                                                                          |
| Cap'n Proto                    | `capnproto`, `capnp`                                                           |
| Clojure                        | `clojure`, `clj`                                                               |
| CoffeeScript                   | `coffeescript`, `coffee`, `cson`, `iced`                                       |
| Crmsh                          | `crmsh`, `crm`, `pcmk`                                                         |
| Crystal                        | `crystal`, `cr`                                                                |
| Cypher (Neo4j)                 | `cypher`                                                                       |
| D                              | `d`                                                                            |
| DAX Power BI                   | `dax`                                                                          |
| DNS Zone 檔案                  | `dns`, `zone`, `bind`                                                          |
| DOS                            | `dos`, `bat`, `cmd`                                                            |
| Dart                           | `dart`                                                                         |
| Delphi                         | `delphi`, `dpr`, `dfm`, `pas`, `pascal`, `freepascal`, `lazarus`, `lpr`, `lfm` |
| Diff                           | `diff`, `patch`                                                                |
| Django                         | `django`, `jinja`                                                              |
| Dockerfile                     | `dockerfile`, `docker`                                                         |
| dsconfig                       | `dsconfig`                                                                     |
| DTS (裝置樹狀目錄)              | `dts`                                                                          |
| Dust                           | `dust`, `dst`                                                                  |
| Dylan                          | `dylan`                                                                        |
| EBNF                           | `ebnf`                                                                         |
| Elixir                         | `elixir`                                                                       |
| Elm                            | `elm`                                                                          |
| Erlang                         | `erlang`, `erl`                                                                |
| Excel                          | `excel`, `xls`, `xlsx`                                                         |
| Extempore                      | `extempore`, `xtlang`, `xtm`                                                   |
| F#                             | `fsharp`, `fs`                                                                 |
| FIX                            | `fix`                                                                          |
| Fortran                        | `fortran`, `f90`, `f95`                                                        |
| G-Code                         | `gcode`, `nc`                                                                  |
| Gams                           | `gams`, `gms`                                                                  |
| GAUSS                          | `gauss`, `gss`                                                                 |
| GDScript                       | `godot`, `gdscript`                                                            |
| Gherkin                        | `gherkin`                                                                      |
| GN for Ninja                   | `gn`, `gni`                                                                    |
| Go                             | `go`, `golang`                                                                 |
| Golo                           | `golo`, `gololang`                                                             |
| Gradle                         | `gradle`                                                                       |
| Groovy                         | `groovy`                                                                       |
| HTML                           | `html`, `xhtml`                                                                |
| HTTP                           | `http`, `https`                                                                |
| Haml                           | `haml`                                                                         |
| Handlebars                     | `handlebars`, `hbs`, `html.hbs`, `html.handlebars`                             |
| Haskell                        | `haskell`, `hs`                                                                |
| Haxe                           | `haxe`, `hx`                                                                   |
| Hy                             | `hy`, `hylang`                                                                 |
| Ini                            | `ini`                                                                          |
| Inform7                        | `inform7`, `i7`                                                                |
| IRPF90                         | `irpf90`                                                                       |
| JSON                           | `json`                                                                         |
| Java                           | `java`, `jsp`                                                                  |
| JavaScript                     | `javascript`, `js`, `jsx`                                                      |
| Kotlin                         | `kotlin`, `kt`                                                                 |
| Kusto                          | `kusto`                                                                        |
| Leaf                           | `leaf`                                                                         |
| Lasso                          | `lasso`, `ls`, `lassoscript`                                                   |
| Less                           | `less`                                                                         |
| LDIF                           | `ldif`                                                                         |
| Lisp                           | `lisp`                                                                         |
| LiveCode Server                | `livecodeserver`                                                               |
| LiveScript                     | `livescript`, `ls`                                                             |
| Lua                            | `lua`                                                                          |
| Makefile                       | `makefile`, `mk`, `mak`                                                        |
| Markdown                       | `markdown`, `md`, `mkdown`, `mkd`                                              |
| Mathematica                    | `mathematica`, `mma`, `wl`                                                     |
| Matlab                         | `matlab`                                                                       |
| Maxima                         | `maxima`                                                                       |
| Maya 內嵌語言         | `mel`                                                                          |
| Mercury                        | `mercury`                                                                      |
| mIRC 指令碼語言        | `mirc`, `mrc`                                                                  |
| Mizar                          | `mizar`                                                                        |
| 受控物件格式          | `mof`                                                                          |
| Mojolicious                    | `mojolicious`                                                                  |
| Monkey                         | `monkey`                                                                       |
| Moonscript                     | `moonscript`, `moon`                                                           |
| MS Graph (互動式)         | `msgraph-interactive`                                                          |
| N1QL                           | `n1ql`                                                                         |
| NSIS                           | `nsis`                                                                         |
| Nginx                          | `nginx`, `nginxconf`                                                           |
| Nimrod                         | `nimrod`, `nim`                                                                |
| Nix                            | `nix`                                                                          |
| OCaml                          | `ocaml`, `ml`                                                                  |
| Objective C                    | `objectivec`, `mm`, `objc`, `obj-c`                                            |
| OpenGL Shading Language        | `glsl`                                                                         |
| OpenSCAD                       | `openscad`, `scad`                                                             |
| Oracle 規則語言          | `ruleslanguage`                                                                |
| Oxygene                        | `oxygene`                                                                      |
| PF                             | `pf`, `pf.conf`                                                                |
| PHP                            | `php`, `php3`, `php4`, `php5`, `php6`                                          |
| Parser3                        | `parser3`                                                                      |
| Perl                           | `perl`, `pl`, `pm`                                                             |
| 純文字無反白         | `plaintext`                                                                    |
| Pony                           | `pony`                                                                         |
| PostgreSQL & PL/pgSQL          | `pgsql`, `postgres`, `postgresql`                                              |
| PowerShell                     | `powershell`, `ps`                                                             |
| PowerShell (互動式)       | `powershell-interactive`                                                       |
| Processing                     | `processing`                                                                   |
| Prolog                         | `prolog`                                                                       |
| 屬性                     | `properties`                                                                   |
| 通訊協定緩衝區               | `protobuf`                                                                     |
| Puppet                         | `puppet`, `pp`                                                                 |
| Python                         | `python`, `py`, `gyp`                                                          |
| Python 分析工具結果        | `profile`                                                                      |
| Q#                             | `qsharp`                                                                       |
| Q                              | `k`, `kdb`                                                                     |
| QML                            | `qml`                                                                          |
| R                              | `r`                                                                            |
| Razor CSHTML                   | `cshtml`, `razor`, `razor-cshtml`                                              |
| ReasonML                       | `reasonml`, `re`                                                               |
| RenderMan RIB                  | `rib`                                                                          |
| RenderMan RSL                  | `rsl`                                                                          |
| Roboconf                       | `graph`, `instances`                                                           |
| Robot Framework                | `robot`, `rf`                                                                  |
| RPM 規格檔案                 | `rpm-specfile`, `rpm`, `spec`, `rpm-spec`, `specfile`                          |
| Ruby                           | `ruby`, `rb`, `gemspec`, `podspec`, `thor`, `irb`                              |
| Rust                           | `rust`, `rs`                                                                   |
| SAS                            | `SAS`, `sas`                                                                   |
| SCSS                           | `scss`                                                                         |
| SQL                            | `sql`                                                                          |
| STEP Part 21                   | `p21`, `step`, `stp`                                                           |
| Scala                          | `scala`                                                                        |
| Scheme                         | `scheme`                                                                       |
| Scilab                         | `scilab`, `sci`                                                                |
| Shape Expressions              | `shexc`                                                                        |
| 殼層                          | `shell`, `console`                                                             |
| Smali                          | `smali`                                                                        |
| Smalltalk                      | `smalltalk`, `st`                                                              |
| Solidity                       | `solidity`, `sol`                                                              |
| Stan                           | `stan`                                                                         |
| Stata                          | `stata`                                                                        |
| 結構化文字                | `iecst`, `scl`, `stl`, `structured-text`                                       |
| Stylus                         | `stylus`, `styl`                                                               |
| SubUnit                        | `subunit`                                                                      |
| Supercollider                  | `supercollider`, `sc`                                                          |
| Swift                          | `swift`                                                                        |
| Tcl                            | `tcl`, `tk`                                                                    |
| Terraform (HCL)                | `terraform`, `tf`, `hcl`                                                       |
| 測試任何通訊協定         | `tap`                                                                          |
| TeX                            | `tex`                                                                          |
| Thrift                         | `thrift`                                                                       |
| TOML                           | `toml`                                                                         |
| TP                             | `tp`                                                                           |
| Twig                           | `twig`, `craftcms`                                                             |
| TypeScript                     | `typescript`, `ts`                                                             |
| VB.NET                         | `vbnet`, `vb`                                                                  |
| VBScript                       | `vbscript`, `vbs`                                                              |
| VHDL                           | `vhdl`                                                                         |
| Vala                           | `vala`                                                                         |
| Verilog                        | `verilog`, `v`                                                                 |
| Vim Script                     | `vim`                                                                          |
| X++                            | `xpp`                                                                          |
| x86 Assembly                   | `x86asm`                                                                       |
| XL                             | `xl`, `tao`                                                                    |
| XQuery                         | `xquery`, `xpath`, `xq`                                                        |
| XAML                           | `xaml`                                                                         |
| XML                            | `xml`, `xhtml`, `rss`, `atom`, `xjb`, `xsd`, `xsl`, `plist`                    |
| YAML                           | `yml`, `yaml`                                                                  |
| Zephir                         | `zephir`, `zep`                                                                |

> [!TIP]
> Docs 編寫套件[開發語言完成功能](docs-authoring/dev-lang-completion.md)在有多個別名可用時，會使用第一個有效的別名。

## <a name="next-steps"></a>下一步

如需程式碼以外內容類型的文字格式設定資訊，請參閱[文字格式設定指導方針](text-formatting-guidelines.md)。
