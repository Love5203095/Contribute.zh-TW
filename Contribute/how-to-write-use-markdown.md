---
title: 如何使用 Markdown 來撰寫 Docs
description: 本文提供用於撰寫 docs.microsoft.com 文章之 Markdown 語言的基本概念和參考資訊。
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 07/13/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 96d00abc052c3b23ca62201dccdbe590a927e72d
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2018
---
# <a name="how-to-use-markdown-for-writing-docs"></a>如何使用 Markdown 來撰寫 Docs

Docs.microsoft.com 文章是以稱為 [Markdown](https://daringfireball.net/projects/markdown/) 的輕量型標記語言撰寫，此標記語言容易閱讀及學習。 基於這個原因，它很快地就成為業界標準。

因為 Docs 的內容是儲存在 GitHub，所以可以使用稱為 [GitHub 版 Markdown (GFM)](https://help.github.com/categories/writing-on-github/) \(英文\) 的 Markdown 超集合，其中針對常見的格式設定需求提供額外支援。 此外，開放式發行服務 (OPS) 實作 DocFX 版 Markdown (DFM)。 DFM 與 GitHub 版 Markdown (GFM) 高度相容，新增了功能以啟用 Docs 特定功能。

## <a name="markdown-basics"></a>Markdown 基本概念

### <a name="headings"></a>標題

若要建立標題，您可以使用雜湊記號，如下所示：

```markdown
    # This is heading 1
    ## This is heading 2
    ### This is heading 3
    #### This is heading 4
```

### <a name="bold-and-italic-text"></a>粗體與斜體文字

若要將文字格式設定為**粗體**，請使用兩個星號將它括住：

```markdown
    This text is **bold**.
```

若要將文字格式設定為*斜體*，請使用單一星號將它括住：

```markdown
    This text is *italic*.
```

若要將文字格式設定為***粗體且斜體***，請使用三個星號將它括住：

```markdown
    This is text is both ***bold and italic***.
```

### <a name="lists"></a>清單

#### <a name="unordered-list"></a>未排序清單

若要設定不排序/項目符號清單的格式，請使用星號或短破折號。 例如，下列 Markdown：

```markdown
- List item 1
- List item 2
- List item 3
```

將會轉譯為：

- 清單項目 1
- 清單項目 2
- 清單項目 3

若要建立包含在另一個清單中的巢狀清單，請將子清單項目縮排。 例如，下列 Markdown：

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

將會轉譯為：

- 清單項目 1
  - 清單項目 A
  - 清單項目 B
- 清單項目 2

#### <a name="ordered-list"></a>已排序清單

若要設定已排序/逐步清單的格式，請使用對應的數字。 例如，下列 Markdown：

```markdown
1. First instruction
2. Second instruction
3. Third instruction
```

將會轉譯為：

1. 第一個指示
2. 第二個指示
3. 第三個指示

若要建立包含在另一個清單中的巢狀清單，請將子清單項目縮排。 例如，下列 Markdown：

```markdown
1. First instruction
    1. Sub-instruction
    2. Sub-instruction
2. Second instruction
```

將會轉譯為：

1. 第一個指示
    1. 子項目指示
    2. 子項目指示
2. 第二個指示

### <a name="tables"></a>表格

表格不是核心 Markdown 規格的一部分，但是 GFM 支援表格。 您可以使用管線 (|) 和連字號 (-) 字元來建立表格。 連字號是用來建立每一欄的標頭，而管線是用來分隔每一欄。 請在您的表格之前包含一個空白行，這樣才能正確轉譯。

例如，下列 Markdown：

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

將會轉譯為：

| 好玩                  | 的                 | 表格          |
| :------------------- | -------------------: |:---------------:|
| 靠左對齊欄  | 靠右對齊欄 | 置中欄 |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |

如需有關如何建立表格的詳細資訊，請參閱：

- DFM [表格內換行功能](#table-wrapping)，可協助設定寬表格格式
- GitHub 的[使用表格組織資訊](https://help.github.com/articles/organizing-information-with-tables/) \(英文\)
- [Markdown 表格產生器](https://www.tablesgenerator.com/markdown_tables) Web 應用程式
- [Adam Pritchard 的 Markdown 速查表](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables) \(英文\)
- [Michel Fortin 的 Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table) \(英文\)
- [將 HTML 表格轉換為 Markdown](https://jmalarcon.github.io/markdowntables/)

### <a name="links"></a>連結

內嵌連結的 Markdown 語法是由超連結文字 `[link text]` 部分，以及緊接在後面的連結 URL 或檔案名稱 `(file-name.md)` 部分所組成：

 `[link text](file-name.md)`

如需連結的詳細資訊，請參閱：

- [Markdown 語法指南](https://daringfireball.net/projects/markdown/syntax#link) 的 Markdown 基礎連結支援。
- 此指南的[連結](how-to-write-links.md)一節，以取得 DFM 所提供之其他連結語法的詳細資料。

### <a name="code-snippets"></a>程式碼片段

Markdown 支援將程式碼片段內嵌在句子中，或是在句子之間形成個別圍住的區塊。 如需詳細資訊，請參閱：

- [Markdown 的程式碼區塊原生支援](https://daringfireball.net/projects/markdown/syntax#precode) \(英文\)
- [GFM 對程式碼包圍和語法醒目提示的支援](https://help.github.com/articles/creating-and-highlighting-code-blocks/) \(英文\)

圍住的程式碼區塊是對程式碼片段支援語法醒目提示的簡單方式。 圍住的程式碼區塊的一般格式為：

    ```alias
    ...
    your code goes in here
    ...
    ```

前三個倒引號 ('`') 字元之後的別名定義要使用的語法醒目提示。 下列清單是 Docs 內容中常用的程式設計語言與對應的標籤：

這些語言包含易記名稱支援，且大部分都具有語言反白顯示。

|名稱|Markdown 標籤|
|-----|-------|
|.NET 主控台|dotnetcli|
|ASP.NET (C#)|aspx-csharp|
|ASP.NET (VB)|aspx-vb|
|AzCopy|azcopy|
|Azure CLI|azurecli|
|Azure PowerShell|azurepowershell|
|C++|cpp|
|C++/CX|cppcx|
|C++/WinRT|cppwinrt|
|C#|csharp|
|CSHTML|cshtml|
|DAX|dax|
|F#|fsharp|
|Go|go|
|HTML|html|
|HTTP|http|
|Java|java|
|JavaScript|javascript|
|JSON|json|
|Markdown|md|
|NodeJS|nodejs|
|Objective-C|objc|
|OData|odata|
|PHP|php|
|Power Apps 公式|powerappsfl|
|PowerShell|powershell|
|Python|python|
|Q#|qsharp|
|Ruby|ruby|
|SQL|sql|
|Swift|swift|
|TypeScript|typescript|
|VB|vb|
|VSTS CLI|vstscli|
|XAML|xaml|
|XML|xml|

#### <a name="example-c"></a>範例：C\#

__Markdown__

    ```csharp
    // Hello1.cs
    public class Hello1
    {
        public static void Main()
        {
            System.Console.WriteLine("Hello, World!");
        }
    }
    ```

__轉譯器__

```csharp
// Hello1.cs
public class Hello1
{
    public static void Main()
    {
        System.Console.WriteLine("Hello, World!");
    }
}
```

#### <a name="example-sql"></a>範例：SQL

__Markdown__

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

__轉譯器__

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a>OPS 自訂 Markdown 擴充功能

> [!NOTE]
> 開放式發行服務 (OPS) 實作與 GitHub 版 Markdown (GFM) 高度相容的「DocFX 版 Markdown」(DFM)。 DFM 透過 Markdown 擴充功能新增了一些功能。 就真正的意義來說，從完整《OPS 撰寫指南》選取的文章包含在此指南中供參考 (例如，請參閱目錄中的＜DFM 與 Markdown 擴充功能＞和＜程式碼片段＞)。

Docs 文章使用 GFM 來設定大部分的文章格式 (例如段落、連結、清單與標題)。 如需更豐富的格式設定，文章可以使用 DFM 功能，例如：

- 注意事項區塊
- 包含
- 選取器
- 內嵌影片
- 程式碼片段/範例

如需完整清單，請參閱目錄中的＜DFM 與 Markdown 擴充功能＞和＜程式碼片段＞。

### <a name="note-blocks"></a>注意事項區塊

有四種類型的注意事項區塊可供您選擇用來強調特定內容：

- 注意
- 警告
- 祕訣
- 重要

在一般情況下，應該謹慎使用注意事項區塊，因為它們可能會造成干擾。 雖然注意事項區塊也支援程式碼區塊、影像、清單和連結，但請盡量讓它們保持簡單明瞭。

### <a name="includes"></a>包含

當您有可重複使用且需要包含到文章檔案中的文字或影像檔時，可以透過 DFM 檔案的包含功能使用「包含」檔案的參考。 此功能會指示 OPS 在建置階段將指定的檔案包含到文章檔案中，成為發行文章的一部分。 有三 種類型的包含可協助您重複使用內容：

- 內嵌：您在其他句子中內嵌常用的文字片段。
- 區塊：您重複使用整個 Markdown 檔案作為區塊 (巢狀嵌入文章中的小節)。
- 影像： 這是 Docs 中實作標準影像包含的方式。

內嵌或區塊包含只是簡單的 Markdown (.md) 檔案。 它可以包含任何有效的 Markdown。 所有的包含 Markdown 檔案都應放在存放庫根目錄中的[一般 `/includes` 子目錄](git-github-fundamentals.md#includes-subdirectory)。 當文章發行之後，包含的檔案會直接整合到其中。

以下是包含的需求與考量：

- 當您需要相同的文字出現在多篇文章中時，就可以使用包含。
- 針對大量內容 (例如一兩個段落、共用的程序或共用的節) 使用區塊包含。 請勿將它們用在小於一個句子的內容。
- 包含檔案將不會在文章的 GitHub 轉譯檢視中轉譯，因為它們依靠 DFM 擴充功能。 它們將會在發行集之後才轉譯。
- 請務必將包含檔案中的文字撰寫成完整的句子或片語，且不相依於參考包含檔案之文章中的上下文。 忽略此指導方針會使文章中產生無法翻譯的字串，進而影響本地化體驗。
- 請勿將包含檔案嵌入到其他包含檔案中。 不支援此使用方式。
- 將媒體檔案放在包含資料夾的特定 [media] 資料夾中，例如 `<repo>`/includes/media 資料夾。 [media] 目錄的根目錄中不應包含任何影像。 如果包含檔案沒有影像，則不需要對應的 [media] 目錄。
- 對於一般文章，請勿在不同包含檔案之間共用媒體。 請針對每個包含檔案和文章，使用具有唯一名稱的個別檔案。 將媒體檔案儲存在與該包含檔案相關聯的 [media] 資料夾。
- 請勿將包含檔案做為文章的唯一內容。  包含檔案是設計成用來補充文章其他部分中的內容。

### <a name="selectors"></a>選取器

當您撰寫同一篇技術文章的不同版本時，可以使用選取器，以滿足跨技術或平台的實作差異。 一般而言，此功能非常適合開發人員的行動平台內容。 DFM 中目前有兩種不同的選擇器 (單一選擇器和多重選擇器)。

因為相同的選擇器 Markdown 會進入選取範圍的每個文章中，我們建議您將文章的選擇器放在包含檔案中。 接著，您可以在您使用相同選擇器的所有文章中參考該包含檔案。

### <a name="code-snippets"></a>程式碼片段

DFM 透過其程式碼片段擴充功能支援將程式碼包含到文章中的進階方式。 它也提供建置在 GFM 功能上的進階轉譯，例如程式設計語言選擇和語法著色，以及各種實用功能，例如：

- 包含來自外部存放庫的集中程式碼範例/片段。
- 可顯示不同語言版本程式碼範例的標籤化 UI。

## <a name="gotchas-and-troubleshooting"></a>偵錯與疑難排解

### <a name="alt-text"></a>替代文字

將無法正確轉譯包含底線的替泰文字。 例如，不要使用此語法︰

```markdown
![ADextension_2FA_Configure_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

將底線逸出，如下所示：

```markdown
![ADextension\_2FA\_Configure\_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a>縮寫符號和雙引號

如果您將內容從 Word 複製到 Markdown 編輯器中，文字可能會包含「智慧」(彎曲) 縮寫符號或雙引號。 這些必須編碼或變更為基本縮寫符號或雙引號。 否則檔案發行之後可能會產生這樣的內容：Itâ€™s

以下是這些標點符號的「智慧」版本編碼：

- 左 (開頭) 雙引號：`&#8220;`
- 右 (結尾) 雙引號：`&#8221;`
- 右 (結尾) 單引號或縮寫符號：`&#8217;`
- 左 (開頭) 單引號 (很少使用)：`&#8216;`

### <a name="angle-brackets"></a>角括號

如果您在文字 (非程式碼) 中使用角括號 (例如，用來代表預留位置)，則需要手動將角括號編碼。 否則 Markdown 會將它們視為 HTML 標籤。

例如，將 `<script name>` 編碼成 `&lt;script name&gt;`

## <a name="see-also"></a>另請參閱

### <a name="markdown-resources"></a>Markdown 資源

- [Markdown 簡介](https://daringfireball.net/projects/markdown/syntax) \(英文\)
- [Docs Markdown 速查表](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [GitHub 的 Markdown 基本概念](https://help.github.com/articles/markdown-basics/) \(英文\)
