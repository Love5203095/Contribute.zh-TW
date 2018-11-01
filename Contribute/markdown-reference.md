---
title: OPS 和 docs.microsoft.com 的 Markdown 參考
description: Markdown 和 DocFX Flavored Markdown (DFM) 延伸模組的 OPS 平台指南。
author: meganbradley
ms.author: mbradley
manager: jemash
ms.date: 05/18/2018
ms.topic: contributor-guide
ms.prod: non-product-specific
audience: internal,external
ms.openlocfilehash: e248eafb0247b200313ba198f2545eca947f5627
ms.sourcegitcommit: d3c7b49dc854dae8da9cd49da8ac4035789a5010
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/23/2018
ms.locfileid: "49805877"
---
# <a name="markdown-reference-for-ops"></a>OPS 的 Markdown 參考

Markdown 是採用純文字格式語法的輕量型標記語言。 OPS 可支援 Markdown 的 CommonMark 標準，以及為提供 docs.microsoft.com 更豐富內容所設計的一些自訂 Markdown 延伸模組。 本文提供針對 docs.microsoft.com 在 OPS 中使用 Markdown 的參考，按字母順序排列。

您可以使用任何文字編輯器來撰寫 Markdown。 為了讓編輯器可以協助插入標準 Markdown 語法和自訂 OPS 延伸模組，建議您安裝 [VS Code](https://code.visualstudio.com/) 和 [Docs 編寫套件](https://aka.ms/DocsAuthoringPack)。

OPS 已針對 Markdig 上所有新版存放庫進行標準化，而舊版存放庫也陸續移轉至 Markdig。 您可以在 [https://babelmark.github.io/](https://babelmark.github.io/) 中測試 Markdig 和其他引擎的 Markdown 呈現。

## <a name="alerts-note-tip-important-caution-warning"></a>警示 (附註、提示、重要、注意、警告)

通知 OPS 專用的 Markdown 延伸模組以建立區塊引述，該區塊引述會在 docs.microsoft.com 中呈現可指出內容重要性的色彩和圖示。 支援的警示類型如下：

```markdown
> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.
```

這些警示在 docs.microsoft.com 中看起來像這樣：

> [!NOTE]
> 即使一眼看過去，使用者也應該注意到的資訊。

> [!TIP]
> 可協助使用者更成功的選用資訊。

> [!IMPORTANT]
> 使用者要成功的必要資訊。

> [!CAUTION]
> 動作可能會導致負面的結果。

> [!WARNING]
> 動作可能會導致危險的結果。

## <a name="code-snippets"></a>程式碼片段

您可以在 Markdown 檔案中內嵌程式碼片段：

```markdown
[!code-<language>[<name>](<codepath><queryoption><queryoptionvalue> "<title>")]
```

## <a name="headings"></a>標題

OPS 支援六種層級的 Markdown 標題：

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- 最後一個 `#` 和標題文字之間必須有一個空格。
- 每個 Markdown 檔案都必須且只能有一個 H1。
- H1 必須是檔案中 YML 中繼資料區塊後的第一個內容。
- H2 會自動顯示在已發佈檔案的瀏覽功能表右側。 較低層級的標題則不會，因此請策略性地使用 H2 以協助讀者瀏覽您的內容。
- HMTL 標題 (例如 `<h1>`) 在有些情況下會造成建置警告，因此不建議您使用。
- 您可以透過[書籤](#bookmark-links)連結至檔案中的個別標題。

## <a name="html"></a>HTML

雖然 Markdown 支援內嵌 HTML，但仍不建議使用 HTML 來透過 OPS 發佈，因為除了有限的值清單以外，都會造成建置錯誤或警告。 <!--For more information, see HTML Whitelist. // do we want to add the whitelist? -->

## <a name="images"></a>影像

包含影像的語法如下：

```markdown
![[alt text]](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

其中，`alt text` 是影像的簡短描述，而 `<folder path>` 是影像的相對路徑。 適用於視障者的螢幕助讀程式需要使用替代文字。 若發生影像無法呈現的網站錯誤時，替代文字也很實用。

影像應儲存在您文件集內的 `/media` 資料夾。 以下是預設支援的影像檔案類型：

- .jpg
- .png

您可以將其他影像類型新增為文件集 docfx.json 檔<!--add link to reference when available-->的資源，以新增支援這些類型。

## <a name="links"></a>連結

在大部分情況下，OPS 都會使用標準 Markdown 連結至其他檔案和頁面。 以下小節說明連結的類型。

> [!TIP]
> 適用於 VS Code 的 Docs 編寫套件有助於正確插入相對連結和書籤，而不需與冗長的路徑奮戰！

> [!IMPORTANT]
> 請不要在您的 Microsoft 網站連結中包含地區設定代碼，例如 en-us。 硬式編碼的地區設定代碼會妨礙當地語系化內容的轉譯，而這會造成其他地區設定使用者的客戶體驗不佳，並產生高昂的當地語系化成本。 當您從瀏覽器複製 URL 時，預設會包含地區設定代碼，因此您必須在建立連結時手動刪除。 例如，使用：
>
> `[Microsoft](https://www.microsoft.com)`
>
> 而非：
>
> `[Microsoft](https://www.microsoft.com/en-us/)`

### <a name="relative-links-to-files-in-the-same-doc-set"></a>相同文件集中檔案的相對連結

相對路徑是相對於目前檔案的目標檔案路徑。 在 OPS 中，您可以使用相對路徑連結至相同文件集內的其他檔案。 相對路徑的語法如下：

```markdown
[link text](../../folder/filename.md)
```

其中，`../` 表示階層中的上一個層級。

- 相對路徑會在建置期間解析，包括移除 .md 副檔名。
- 您可以使用 "../" 連結至父資料夾中的檔案，但該檔案必須位於相同的文件集中。 您無法使用 "../" 連結至另一個文件集資料夾中的檔案。
- OPS 也支援開頭為 "~" 的特殊格式相對路徑 (例如 ~/foo/bar.md)。 此語法表示檔案是相對於文件集的根資料夾。 這種路徑也會在建置期間進行驗證及解析。

> [!IMPORTANT]
> 在相對路徑中包含副檔名。 組建可驗證該相對路徑的目標檔案是否存在。 如果相對路徑未包含副檔名，組建就可能會回報連結中斷的警告。 例如，使用：
>
> `[link text](../../folder/filename.md)`
>
> 而非：
>
> `[link text](../../folder/filename)`

### <a name="absolute-links-to-other-files-in-ops"></a>OPS 中其他檔案的絕對連結

```markdown
[Azure and Linux](/articles/virtual-machines/linux/overview)
```

請不要包含副檔名 (.md)。 此為來自外部 Azure「文章」文件集的 Linux 概觀檔連結。

### <a name="links-to-external-sites"></a>外部網站的連結

```markdown
[Microsoft](https://www.microsoft.com)
```

其他網頁的 URL 連結 (必須包含 https://)。

### <a name="bookmark-links"></a>書籤連結

相同存放庫中其他檔案的標題書籤連結：

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

目前檔案中的標題書籤連結：

```markdown
[Managed Disks](#managed-disks)
```

使用主題標籤後接標題文字，移除標點符號並將空格取代為虛線。

### <a name="explicit-anchor-links"></a>明確錨點連結

除非在中樞和登陸頁面中，否則**沒有必要也不建議使用**含 `<a>` HTML 標籤的明確錨點連結。 請如上所述在一般 Markdown 檔案中使用書籤。 針對中樞和登陸頁面，請如下所示使用錨點：

`## <a id="AnchorText"> </a>Header text` 或 `## <a name="AnchorText"> </a>Header text`

若要連結至明確錨點，請使用下列語法：

```markdown
To go to a section on the same page:
[text](#AnchorText)

To go to a section on another page.
[text](FileName.md#AnchorText)
```

### <a name="xref-cross-reference-links"></a>XREF (交互參照) 連結

若要連結至目前文件集或其他文件集中自動產生的 API 參照頁面，請使用 XREF 連結與唯一識別碼 (UID)。

> [!NOTE]
> 若要參考其他文件集中的 API 參照頁面，您必須在 `docfx.json` 檔案中新增 `xrefService` 設定。
> ```
> "build": {
>   ...
>   "xrefService": [ "https://xref.docs.microsoft.com/query?uid={uid}" ]
> }
> ```

UID 等同於完整的類別和成員名稱。 如果您在 UID 之後加上 *，則連結代表多載頁面，而不是特定的 API。 例如，使用 `List<T>.BinarySearch*` 連結至 BinarySearch 方法頁面，而不是連結至特定多載，例如 `List<T>.BinarySearch(T, IComparer<T>)`。

您可以使用下列其中一個語法：

- 自動連結：`<xref:UID> or <xref:UID?displayProperty=nameWithType>`

  選用的 `displayProperty` 查詢參數會產生完整的連結文字。 根據預設，連結文字只會顯示成員或型別名稱。

- Markdown 連結：`[link text](xref:UID)`
  
  用於您要自訂顯示的連結文字時。

範例：

- `<xref:System.String>` 會轉譯為 "String"。
- `<xref:System.String?displayProperty=nameWithType>` 會轉譯為 "System.String"。
- `[String class](xref:System.String)` 會轉譯為 "String class"。

目前還沒有較輕鬆的方式可用來尋找 UID。 <!-- ? -->若要尋找 API 的 UID，最佳方法就是檢視所要連結 API 頁面的來源，然後尋找 ms.assetid 值。 個別的多載值不會顯示在來源中。 我們正努力讓系統在未來會更好。

當 UID 包含特殊字元 \`、\# 或 \* 時，UID 值必須分別以 HTML 編碼為 `%60`、`%23` 和 `%2A`。 有時候您會看到括號也會被編碼，但這並非必要。

範例：

- System.Threading.Tasks.Task\`1 變成 `System.Threading.Tasks.Task%601`
- System.Exception.\#ctor 變成 `System.Exception.%23ctor`
- System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) 變成 `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`

<!-- leave out of Contributor Guide for now
Using XREF may require some configuration. For more information, see XREF Service.
-->

## <a name="lists-numbered-bulleted-checklist"></a>清單 (編號、分項、檢查清單)

### <a name="numbered-list"></a>編號清單

若要建立編號清單，您可以全部都使用 1，系統即會在發佈時將其轉譯為連續清單。 為了讓來源更方便閱讀，您可以遞增清單。

請不要在清單中使用字母，包括巢狀清單。 透過 OPS 發佈時，字母無法正確轉譯。 如果是使用數字的巢狀清單，系統在發佈時會轉譯為小寫字母。 例如：

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

這會轉譯為：

1. 這是
1. 父代編號清單
   1. 而這是
   1. 巢狀編號清單
1. (fin)

### <a name="bulleted-list"></a>項目符號清單

若要建立項目符號清單，請在每行開頭使用 `-` 後接空格：

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

這會轉譯為：

- 這是
- 父代項目符號清單
  - 而這是
  - 巢狀項目符號清單
- 完成！

### <a name="checklist"></a>檢查清單

您可透過自訂 Markdown 延伸模組，在 docs.microsoft.com (僅限於此) 上使用檢查清單：

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

此範例在 docs.microsoft.com 上的轉譯如下：

> [!div class="checklist"]
> * 清單項目 1
> * 清單項目 2
> * 清單項目 3

您可在文章開頭或結尾使用檢查清單，以總結「您將學到什麼」或「您已學到的內容」。 請不要在整篇文章中新增隨機檢查清單。
<!-- is this guidance still accurate? -->

## <a name="next-step-action"></a>下一步動作

您可使用自訂延伸模組，將下一步動作按鈕新增至 docs.microsoft.com (僅限於此) 上的頁面。

語法如下：

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

例如：

```markdown
> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)
```

這會轉譯為：

> [!div class="nextstepaction"]
> [了解基本樣式](style-quick-start.md)

您可以在下一步動作中使用任何支援的連結，包括其他網頁的 Markdown 連結。 在大部分情況下，下一步動作連結都是相同文件集中其他檔案的相對連結。

## <a name="section-definition"></a>區段定義

<!-- more info about this would be helpful! --> 您可能需要定義區段。 此語法最常用於程式碼表格。
請參閱下列範例：

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

上述區塊引述 Markdown 文字會轉譯為：
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```

## <a name="selectors"></a>選取器

<!-- could be more clear! --> 當您想要連線到同一篇文章的不同頁面，可以使用選取器。 讀者即可在這些頁面間切換。

> [!NOTE]
> 此延伸在 docs.microsoft.com 和 MSDN 的運作方式不同。 <!-- should we keep info about MSDN? If so say how they differ?-->

### <a name="single-selector"></a>單一選取器

```
> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)
```

... 轉譯結果如下：

> [!div class="op_single_selector"]
> - [通用 Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)

### <a name="multi-selector"></a>多重選取器

```
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows universal C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows universal C# | Javascript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | Javascript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | Javascript)](how-to-write-workflows-major.md)
```

... 轉譯結果如下：

> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows 通用 C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows 通用 C# | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | JavaScript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | JavaScript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | JavaScript)](how-to-write-workflows-major.md)

<!-- uncomment and link when Cory's topic is live
## Tabbed content

Tabs are a Markdown extension for docs.microsoft.com that allow us to present different versions of content, such as procedural steps to accomplish the same task on different platforms, in a tabbed format.

Because the syntax and requirements for tabbed content are fairly complex, they are documented separately in Tabbed Content.
-->

## <a name="tables"></a>表格

在 Markdown 中建立表格的最簡單做法是使用直立線符號及線條。 若要建立含標題的標準表格，請沿著第一個線段與虛線：

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

這會轉譯為：

|這是   |簡單的   |表格標題|
|----------|-----------|------------|
|表格     |資料       |這裡        |
|其實|並不   |需要完全對齊！||

您也可以建立不含標題的表格。 例如，若要建立多重資料行清單：

```markdown
|   |   |
| - | - |
| This | table |
| has no | header |
```

這會轉譯如下：

|   |   |
| - | - |
| 此 | 表格 |
| 不含任何 | 標題 |

您可以使用冒號對齊資料行：

```markdown
|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|
```

轉譯如下：

|                  |
|------------------|
|    靠右對齊：|
|：靠左對齊     |
|：置中對齊        :|

> [!TIP]
> 適用於 VS Code 的 Docs 編寫延伸模組可讓您輕鬆新增基本 Markdown 表格！
>
> 您也可以使用[線上表格產生器](http://www.tablesgenerator.com/markdown_tables)。

### <a name="mx-tdbreakall"></a>mx-tdBreakAll

> [!IMPORTANT]
> 此功能僅適用於 docs.microsoft.com 網站。

如果您使用 Markdown 建立表格，該表格可能會擴展到右側導覽，變得難以閱讀。 您可以藉由允許 Docs 轉譯視需要切割表格，來解決此問題。 您只要使用自訂類別 `[!div class="mx-tdBreakAll"]` 加在表格前後即可。

以下是具有三列的表格 Markdown 範例，會以類別名稱為 `mx-tdBreakAll` 的 `div` 加在表格前後。

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

轉譯結果如下：

> [!div class="mx-tdBreakAll"]
> |名稱|語法|對無訊息安裝為必要？|描述|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|是|執行安裝程式，而不顯示 UI 和提示。|
> |NoRestart|/norestart|否|隱藏重新啟動的任何嘗試。 根據預設，UI 會在重新啟動前出現提示。|
> |Help|/help|否|提供說明和快速參考。 顯示安裝命令的正確用法，包括所有選項和行為的清單。|

### <a name="mx-tdcol2breakall"></a>mx-tdCol2BreakAll

> [!IMPORTANT]
> 此功能僅適用於 docs.microsoft.com 網站。

有時候，在您表格中第二欄的字詞可能會很長。 為了讓它們妥善分隔，您可以使用先前所示的 `div` 包裝函式語法來套用類別 `mx-tdCol2BreakAll`。

### <a name="html-tables"></a>HTML 表格

HTML 表格不建議用於 docs.microsoft.com。 這類表格不是使用者可看懂的來源，而這與 Markdown 主要準則抵觸。

<!--If you use HTML tables and your Markdown is not being rendered between the two tables, you need to add a closing `br` tag after the closing `table` tag.

![break HTML tables](media/break-tables.png)
-->

## <a name="videos"></a>影片

### <a name="embedding-videos-into-a-markdown-page"></a>將影片內嵌在 Markdown 頁面中

目前，OPS 可支援將影片發佈至下列三個位置之一：

- YouTube
- Channel 9
- Microsoft 專屬的 'One Player' 系統

您可以使用下列語法內嵌影片，而 OPS 會加以轉譯。

```markdown
> [!VIDEO <embedded_video_link>]
```

範例：

```markdown
> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
```

... 將會轉譯為：

```html
<iframe src="https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>

<iframe src="https://www.youtube-nocookie.com/embed/iAtwVM-Z7rY" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
<iframe src="https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
```

並在發佈頁面上顯示如下：

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

> [!IMPORTANT]
> CH9 影片 URL 應該以 `https` 開頭並以 `/player` 結尾。 否則，它會內嵌整頁而不只是影片。

### <a name="uploading-new-videos"></a>上傳新影片

您應該使用下列程序上傳任何新影片：

1. 加入 IDWEB 上的 **docs_video_users** 群組。
1. 前往 https://aka.ms/VideoUploadRequest 並填妥影片的詳細資料。 需要的項目 (請注意，這些項目都不會公開顯示)：
    1. 影片標題。
    1. 影片相關的產品/服務清單。
    1. 裝載影片的目標頁面或文件集 (如果您還沒有頁面的話)。
    1. 影片的 MP4 檔案連結 (如果您沒有位置存放檔案，可先暫時存放此處：`\\scratch2\scratch\apex`)。 MP4 檔案應該為 720p 或更高品質。
    1. 影片的描述。
1. 提交 (儲存) 該項目。
1. 在兩個工作天內，影片即可上傳。 您需要的內嵌連結會放在工作項目中，並解析後*回傳給您*。
1. 取得影片連結後，請關閉工作項目。
1. 接著，您即可使用下列語法，將影片連結新增至貼文：

   ```markdown
   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
   ```
