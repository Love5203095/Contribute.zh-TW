---
title: .NET 文章的範本和速查表
description: 本文包含一個方便的範本，您可以使用該範本為 .NET 文件存放庫建立新文章
ms.date: 11/07/2018
ms.openlocfilehash: 8980f5e39213d8f2edd1d29e66d900f2c3d04bbc
ms.sourcegitcommit: 44eb4f5ee65c1848d7f36fca107b296eb7687397
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/13/2018
ms.locfileid: "51609731"
---
# <a name="metadata-and-markdown-template-for-net-docs"></a>.NET 文件的中繼資料和 Markdown 範本

此 dotnet/docs 範本包含 Markdown 語法的範例，以及設定中繼資料的指導。

當建立 Markdown 檔案時，您應將包含的範本複製到新檔案中、依照如下指定來填寫中繼資料，並將以上 H1 標題設為文章標題。

## <a name="metadata"></a>中繼資料

所需的中繼資料區塊位於下列範例中繼資料區塊中：

```markdown
---
title: [ARTICLE TITLE]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
author: [GITHUB USERNAME]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- 冒號 (:) 和中繼資料項目的值之間**必須**有空格。
- 值中的冒號 (例如標題) 會中斷中繼資料解析器。 在此情況下，請使用雙引號來括住標題 (例如 `title: "Writing .NET Core console apps: An advanced step-by-step guide"`)。
- **標題**：會出現在搜尋引擎結果中。 標題不應與 H1 標題中的標題相同，且不應超過 60 個字元。
- **描述**：摘要文章的內容。 通常會顯示於搜尋結果頁面，但不會用於搜尋排名。 長度應為 115-145 個字元，包括空格。
- **作者**：作者欄位應包含作者的 **GitHub 使用者名稱**。
- **ms.date**：上次重大更新的日期。 如果您已檢閱並更新整篇文章，請在現有文章中對此進行更新。 錯字或類似內容的小修正，不保證會更新。

其他中繼資料會附加至每篇文章，但我們通常會在資料夾層級套用大多數中繼資料值 (在 **docfx.json** 中指定)。

## <a name="basic-markdown-gfm-and-special-characters"></a>基本 Markdown、GFM 和特殊字元

您可以在 [Markdown](how-to-write-use-markdown.md) 和 [Markdown 參考](markdown-reference.md)的一般文章中了解 Markdown、GitHub Flavored Markdown (GFM) 和 OPS 特定延伸模組的基本知識。

Markdown 使用 \*、\` 和 \# 等特殊字元來格式化。 如果您希望將其中一個字元包含在內容中，則必須執行以下兩項作業之一：

- 在特殊字元前加上一個反斜線以將其「逸出」 (例如 `\*` 對於 \*)
- 為字元使用 [HTML 實體程式碼](http://www.ascii.cl/htmlcodes.htm) (例如，`&#42;` 對於 &#42;)。

## <a name="file-names"></a>檔案名稱

檔案名稱使用下列規則：

* 只包含小寫字母、數字和連字號。
* 沒有空格或標點符號字元。 檔案名稱中使用連字號來分隔文字和數字。
* 使用特定的動作動詞，例如 develop、buy、build、troubleshoot。 沒有 -ing 字詞。
* 不包含 a、and、the、in、or 等短字。
* 必須是 Markdown 格式且使用 .md 副檔名。
* 保持檔案名稱合理簡短。 它們是您文章 URL 的一部分。

## <a name="headings"></a>標題

使用句型大寫。 標題的第一個單字一律為大寫。

## <a name="text-styling"></a>文字樣式

*斜體*：用於檔案、資料夾、路徑 (對於長項目，則拆分為其自己的行)、新術語。

**粗體**：用於 UI 項目。

`Code`用於內嵌程式碼、語言關鍵字，NuGet 套件名稱、命令列命令、資料庫資料表和資料列名稱，以及您不希望能點選的 URL。

## <a name="links"></a>連結

如需錨點、內部連結、其他文件的連結、程式碼包含項目和外部連結的資訊，請參閱[連結](how-to-write-links.md)的一般文章。

.NET 文件小組使用下列慣例：

- 在大多數情況下，我們使用相對連結且不建議在連結中使用 `~/`，因為相對連結會在 GitHub 上的來源中解析。 但是，每當我們連結到相依存放庫中的檔案時，我們將使用 `~/` 字元來提供路徑。 由於相依存放庫中的檔案位於 GitHub 中不同位置，因此無論撰寫方式如何，連結都無法使用相對連結來正確解析。
- C# 語言規格和 Visual Basic 語言規格包含在 .NET 文件中，包含語言存放庫中的來源。 Markdown 來源在 [csharplang](https://github.com/dotnet/csharplang) 和 [vblang](https://github.com/dotnet/vblang) 存放庫中管理。

規格的連結，必須指向包含這些規格的來源目錄。 針對 C#，目錄是 **~/_csharplang/spec**；針對 VB，目錄是 **~/_vblang/spec**。

- 範例：`[C# Query Expressions](~/_csharplang/spec/expressions.md#query-expressions)`

### <a name="links-to-apis"></a>API 的連結

組建系統具有一些延伸模組，可讓我們連結到 .NET API 而無需使用外部連結。 請使用下列語法之一：

1. 自動連結：`<xref:UID>` 或 `<xref:UID?displayProperty=nameWithType>`

   `displayProperty` 查詢參數會產生完整的連結文字。 根據預設，連結文字只會顯示成員或型別名稱。

2. Markdown 連結：`[link text](xref:UID)`

   用於您要自訂顯示的連結文字時。

範例：

- `<xref:System.String>` 會轉譯為 [String](https://docs.microsoft.com/dotnet/api/system.string) \(英文\)
- `<xref:System.String?displayProperty=nameWithType>` 會轉譯為 [System.String](https://docs.microsoft.com/dotnet/api/system.string) \(英文\)
- `[String class](xref:System.String)` 會轉譯為 [String 類別](https://docs.microsoft.com/dotnet/api/system.string) \(英文\)

如需如何使用此標記法的詳細資訊，請參閱[使用交叉參考](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference) \(英文\)。

UID 包含特殊字元 \`、\# 或 \*，UID 值必須分別以 HTML 編碼為 `%60`、`%23` 和 `%2A`。 有時候您會看到括號也會被編碼，但這並非必要。

範例：

- System.Threading.Tasks.Task\`1 變成 `System.Threading.Tasks.Task%601`
- System.Exception.\#ctor 變成 `System.Exception.%23ctor`
- System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) 變成 `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`

您可以在 `https://xref.docs.microsoft.com/autocomplete` 中找到類型的 UID、成員多載清單或特定多載成員。 查詢字元字串 ?text=*\<type-member-name>*" 可識別出您要查看其 UID 的類型或成員。 例如，`https://xref.docs.microsoft.com/autocomplete?text=string.format` 會擷取 [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format) 多載。 該工具會在 UID 的任何部分中，搜尋所提供的 `text` 查詢參數。 例如，您可以搜尋成員名稱 (ToString)、部分成員名稱 (ToStri)、類型和成員名稱 (Double.ToString) 等。

如果您在 UID 之後新增 \* (或 %2A)，則連結代表多載頁面，而不是特定的 API。 例如，當您想要以一般方法連結到 [List\<T>.BinarySearch Method](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) \(英文\) 頁面，而不是如 [List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_) \(英文\) 的特定多載，就可以使用該方式。 當成員未多載時，您也可以使用 \* 連結到成員頁面；這可讓您無需在 UID 中包含參數清單。

要連結到特定方法多載，必須包含每個方法參數的完整類型名稱。 例如，\<xref:System.DateTime.ToString> 會連結到無參數 [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString) 方法，而 \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)> 會連結到 [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_) 方法。

若要連結到泛型型別，例如 [System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1)，則可以使用 \` (%60) 字元，後面接著泛型型別參數的數量。 例如，\<xref:System.Nullable%601> 會連結到 [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1) 類型，而 \<xref:System.Func%602> 會連結到 [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2) 委派。

## <a name="code"></a>程式碼

包含程式碼的最佳方法，是包含工作範例中的程式碼片段。 遵循[參與 .NET](dotnet-contribute-process.md#contributing-to-samples) 文章中的指令來建立範例。 包含程式碼的基本規則，位於[程式碼](how-to-write-use-markdown.md#code-includes)的一般指導中。

您可以使用下列語法來包含程式碼：

```markdown
[!code-<language>[<name>](<pathToFile><queryoption><queryoptionvalue>)]
```

* `-<language>` (「選擇性」，但「建議使用」)
  * 正在參考之程式碼片段的語言。 如需支援值的清單，請參閱[支援的語言](#supported-languages)。

* `<name>` (選擇性)
  * 程式碼片段的名稱。 這對輸出 HTML 並沒有任何影響，但您可以用來提高 Markdown 原始碼的可讀性。

* `<pathToFile>` (強制)
  * 檔案系統中的相對路徑，表示要參考的程式碼片段檔案。 構成 .NET 文件集的不同存放庫可能會使這變得複雜。 .NET 範例位於 dotnet/samples 存放庫中。 所有程式碼片段路徑都以 `~/samples` 開頭，路徑的其餘部分，來自該存放庫根目錄的來源路徑。

* `<queryoption>` (選擇性)
  * 用於指定如何從檔案中擷取程式碼：
    * `#`：`#{tagname}` (標籤名稱) 「或」 `#L{startlinenumber}-L{endlinenumber}` (行範圍)。
    我們不鼓勵使用行號，因為較容易出錯。 標籤名稱是參考程式碼片段的首選方式。 請使用有意義的標籤名稱。 (許多程式碼片段都是從先前的平台遷移過來，且標籤的名稱包含 `Snippet1`、`Snippet2` 等。該做法較難維持。)
    * `range`：`?range=1,3-5` 行的範圍。 此範例包含第 1、3、4 及 5 行。

我們建議盡可能使用標籤名稱選項。 標籤名稱是區域的名稱，或是以 `Snippettagname` 格式出現在原始程式碼中的程式碼註解名稱。 下列範例顯示如何參考標記名稱 `BasicThrow`：

```markdown
[!code-csharp[csrefKeyword#1](~/samples/snippets/snippets/csharp/language-reference/operators/ConditionalExamples.csConditionalRef)]
```

**dotnet/samples** 中來源的相對路徑會遵循 `~/samples` 路徑。

您可以在[來源檔案](https://github.com/dotnet/samples/blob/master/snippets/csharp/language-reference/operators/ConditionalExamples.cs)中查看程式碼片段標籤的結構。 如需程式碼片段原始程式檔中依語言分類的標籤名稱表示法詳細資料，請參閱 [DocFX 指南](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file)。

下列範例顯示所有三種 .NET 語言中包含的程式碼：

```markdown
[!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/pig-latin.fs#L1-L14)]
 [!code-csharp[ADCreateDomain#2](../../../samples/snippets/csharp/VS_Snippets_CLR/ADCreateDomain/CS/source2.cs#2)]
 [!code-vb[ADCreateDomain#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/ADCreateDomain/VB/source2.vb#2)]  
```

包含完整程式的程式碼片段，可確保所有程式碼都透過我們的持續整合 (CI) 系統執行。 但是，如果需要顯示導致編譯時間或執行階段錯誤的內容，則可以使用內嵌程式碼區塊。

## <a name="images"></a>影像

### <a name="static-image-or-animated-gif"></a>靜態影像或動畫 GIF

```markdown
![this is the alt text](../images/Logo_DotNet.png)
```

### <a name="linked-image"></a>連結的影像

```markdown
[![alt text for linked image](../images/Logo_DotNet.png)](https://dot.net)
```

## <a name="videos"></a>影片

目前，您可以使用下列語法嵌入 Channel 9 和 YouTube 影片：

### <a name="channel-9"></a>Channel 9

```markdown
> [!VIDEO <channel9_video_link>]
```

若要取得影片的正確網址，請選取影片框架下方的 [嵌入] 索引標籤，然後從 `<iframe>` 項目中複製網址。 例如：

```markdown
> [!VIDEO https://channel9.msdn.com/Blogs/dotnet/NET-Core-20-Released/player]
```

### <a name="youtube"></a>YouTube

若要取得影片的正確網址，請以右鍵按一下影片，選取 [複製內嵌程式碼]，然後從 `<iframe>` 項目複製網址。

```markdown
> [!VIDEO <youtube_video_link>]
```

例如：

```markdown
> [!VIDEO https://www.youtube.com/embed/Q2mMbjw6cLA]
```

## <a name="docsmicrosoft-extensions"></a>docs.microsoft 延伸模組

docs.microsoft 為 GitHub Flavored Markdown 提供一些額外的延伸模組。

### <a name="checked-lists"></a>檢查清單

自訂樣式適用於清單。 您可以轉譯具有綠色核取記號的清單。

```markdown
> [!div class="checklist"]
> * How to create a .NET Core app
> * How to add a reference to the Microsoft.XmlSerializer.Generator package
> * How to edit your MyApp.csproj to add dependencies
> * How to add a class and an XmlSerializer
> * How to build and run the application
```

這會呈現為：

> [!div class="checklist"]
> * 如何建立 .NET Core 應用程式
> * 如何將參考新增至 Microsoft.XmlSerializer.Generator 套件
> * 如何編輯您的 MyApp.csproj 以新增相依性
> * 如何新增類別和 XmlSerializer
> * 如何建置並執行應用程式

您可以在 [.NET Core 文件](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator)中查看檢查清單的範例。

### <a name="buttons"></a>按鈕

按鈕連結：

```markdown
> [!div class="button"]
[button links](dotnet-contribute.md)
```

這會呈現為：

> [!div class="button"]
[按鈕連結](dotnet-contribute.md)

您可以在 [Visual Studio 文件](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio)中查看按鈕的範例。

### <a name="step-by-steps"></a>逐步

```markdown
>[!div class="step-by-step"]
[Pre](../docs/csharp/expression-trees-interpreting.md)
[Next](../docs/csharp/expression-trees-translating.md)
```

您可以在 [C# 指南](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure)中查看動作中的逐步範例。
