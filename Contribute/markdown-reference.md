---
title: docs.microsoft.com 的 Markdown 參考
description: 了解 Microsoft Docs 平台中所使用的 Markdown 功能和語法。
author: meganbradley
ms.author: mbradley
ms.date: 01/30/2020
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.openlocfilehash: c1568264c687ebaf26048f5432fdea7d5132c012
ms.sourcegitcommit: 216ef77ca2cd1eeb31c6c89d96778b178fc0d540
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/21/2020
ms.locfileid: "80070090"
---
# <a name="docs-markdown-reference"></a>Docs Markdown 參考

本文提供針對 docs.microsoft.com (Docs) 撰寫 Markdown 的參考資訊，按字母順序排列。

[Markdown](https://daringfireball.net/projects/markdown/) 是採用純文字格式語法的輕量型標記語言。 Docs 支援符合 [CommonMark](https://commonmark.org/) 規範且透過 [Markdig](https://github.com/lunet-io/markdig) 剖析引擎剖析的 Markdown。 Docs 也支援自訂 Markdown 延伸模組，可在 Docs 網站上提供更豐富的內容。

您可以使用任何文字編輯器撰寫 Markdown，但建議您使用 [Visual Studio Code](https://code.visualstudio.com/) 搭配 [Docs 編寫套件](https://aka.ms/DocsAuthoringPack)。 Docs 編寫套件提供編輯工具和預覽功能，可讓您看到您的文章在 Docs 上轉譯出來的樣子。

## <a name="alerts-note-tip-important-caution-warning"></a>警示 (附註、提示、重要、注意、警告)

警示是用來建立區塊引述的Markdown 延伸模組，在 docs.microsoft.com 中這些區塊引述會呈現出可表示內容重要性的色彩和圖示。 支援的警示類型如下：

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
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.

### <a name="angle-brackets"></a>角括號

如果您在文字中使用角括號 (例如，用來代表預留位置)，需要手動將角括號編碼。 否則 Markdown 會將它們視為 HTML 標籤。

例如，將 `<script name>` 編碼成 `&lt;script name&gt;` 或 `\<script name>`。

在格式化為內嵌程式碼或程式碼區塊的文字中，角括號不需要逸出。

## <a name="apostrophes-and-quotation-marks"></a>縮寫符號和雙引號

如果您將內容從 Word 複製到 Markdown 編輯器中，文字可能會包含「智慧」(彎曲) 縮寫符號或雙引號。 這些必須編碼或變更為基本縮寫符號或雙引號。 否則檔案發佈後可能會產生這樣的內容：Itâ€™s

以下是這些標點符號的「智慧」版本編碼：

- 左 (開頭) 雙引號：`&#8220;`
- 右 (結尾) 雙引號：`&#8221;`
- 右 (結尾) 單引號或縮寫符號：`&#8217;`
- 左 (開頭) 單引號 (很少使用)：`&#8216;`

## <a name="blockquotes"></a>區塊引述

區塊引述使用 `>` 字元建立：

```md
> This is a blockquote. It is usually rendered indented and with a different background color.
```

前述範例會如下呈現：

> This is a blockquote. It is usually rendered indented and with a different background color.

## <a name="bold-and-italic-text"></a>粗體與斜體文字

若要將文字格式設定為**粗體**，請使用兩個星號將它括住：

```markdown
This text is **bold**.
```

若要將文字格式設定為*斜體*，請使用單一星號將它括住：

```markdown
This text is *italic*.
```

若要將文字格式設定為***粗體加斜體***，請使用三個星號將它括住：

```markdown
This text is both ***bold and italic***.
```

## <a name="code-snippets"></a>程式碼片段

Docs Markdown 支援將程式碼片段內嵌在句子中，或是將「隔離」的個別區塊放在句子之間。 如需詳細資訊，請參閱[如何在 Docs 中新增程式碼](code-in-docs.md)。

## <a name="columns"></a>columns

**columns** (資料行) Markdown 延伸模組讓 Docs 作者能夠加入以資料行配置的內容，比只適用於真正表格資料的基本 Markdown 資料表更具彈性且功能強大。 您最多可以加入四個資料行，並使用選擇性的 `span` 屬性來合併兩個或更多資料行。

columns 的語法如下：

```markdown
:::row:::
   :::column span="":::
      Content...
   :::column-end:::
   :::column span="":::
      More content...
   :::column-end:::
:::row-end:::
```

資料行只能包含基本 Markdown，包括影像。 不應包含標題、資料表、索引標籤和其他複雜的結構。 資料列不能有任何內容落在資料行之外。

例如，下列 Markdown 會建立一個橫跨兩資料行寬度的資料行，以及一個標準 (無 `span`) 資料行：

```markdown
:::row:::
   :::column span="2":::
      **This is a 2-span column with lots of text.**

      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec vestibulum mollis nunc
      ornare commodo. Nullam ac metus imperdiet, rutrum justo vel, vulputate leo. Donec
      rutrum non eros eget consectetur.
   :::column-end:::
   :::column span="":::
      **This is a single-span column with an image in it.**

      ![Doc.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::
```

這會轉譯為：

:::row:::
   :::column span="2":::
      **This is a 2-span column with lots of text.**

      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec vestibulum mollis nunc ornare commodo. Nullam ac metus imperdiet, rutrum justo vel, vulputate leo. Donec rutrum non eros eget consectetur.
   :::column-end:::
   :::column span="":::
      **This is a single-span column with an image in it.**

      ![Doc.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::

## <a name="headings"></a>標題

Docs 支援六種層級的 Markdown 標題：

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- 最後一個 `#` 和標題文字之間必須有一個空格。
- 每個 Markdown 檔案都必須且只能有一個 H1 標題。
- H1 標題必須是檔案中 YML 中繼資料區塊後的第一個內容。
- H2 標題會自動顯示在已發佈檔案的瀏覽功能表右側。 較低層級的標題則不會，因此請策略性地使用 H2 以協助讀者瀏覽您的內容。
- HTML 標題 (例如 `<h1>`) 在有些情況下會造成建置警告，因此不建議使用。
- 您可以透過[書籤連結](how-to-write-links.md#links-to-anchors)連至檔案中的個別標題。

## <a name="html"></a>HTML

雖然 Markdown 支援內嵌 HTML，但仍不建議使用 HTML 來發佈至 Docs，因為除了有限的值清單以外，都會造成建置錯誤或警告。 

## <a name="images"></a>影像

以下是預設支援的影像檔案類型：

- .jpg
- .png

### <a name="standard-conceptual-images-default-markdown"></a>標準概念影像 (預設 Markdown)

用來內嵌影像的基本 Markdown 語法為：

```Markdown
![<alt text>](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

其中，`<alt text>` 是影像的簡短描述，而 `<folder path>` 是影像的相對路徑。 適用於視障者的螢幕助讀程式需要使用替代文字。 若發生影像無法轉譯的網站錯誤時，替代文字也很實用。

替代文字中的底線不會正確轉譯出來，除非您在前面加上反斜線 (`\_`) 加以逸出。 不過，請勿複製檔案名稱做為替代文字。 例如，不應使用：

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

而是寫成：

```markdown
![Active Directory extension for two-factor authentication, step 4: Configure](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="standard-conceptual-images-docs-markdown"></a>標準概念影像 (Docs Markdown)

Docs 自訂 `:::image:::` 延伸模組支援標準影像、複雜影像、圖示。

針對標準影像，較舊的 Markdown 語法仍然可以運作，但建議使用新的延伸模組，因為後者支援更強大的功能，例如指定與父系主題不同的當地語系化範圍。 未來將會提供其他先進的功能，例如從共用影像庫中選取，而不是指定本機影像。 新語法如下：

```Markdown
:::image type="content" source="<folderPath>" alt-text="<alt text>":::
```

如果 `type="content"` (預設值)，則 `source` 和 `alt-text` 都是必要的。

### <a name="complex-images-with-long-descriptions"></a>具有長描述的複雜影像

您也可以使用此延伸模組，新增具有長描述的影像，這種描述會由螢幕助讀程式朗讀，但不會視覺呈現在發佈的頁面上。 長描述是複雜影像 (例如圖形) 所必需的協助。 語法如下：

```Markdown
:::image type="complex" source="<folderPath>" alt-text="<alt text>":::
   <long description here>
:::image-end:::
```

如果 `type="complex"`，則 `source`、`alt-text`、長描述、`:::image-end:::` 標記都是必要的。

### <a name="specifying-loc-scope"></a>指定 loc-scope

有時候，影像的當地語系化範圍 (localization scope) 與包含它的文章或模組不同。 這可能會導致不良的全球體驗：例如，如果產品的螢幕擷取畫面不小心當地語系化成無法使用產品的語言。 若要避免這種情況，您可以在 `content` 和 `complex` 類型的影像中指定選擇性的 `loc-scope` 屬性。

### <a name="icons"></a>圖示

影像延伸模組支援圖示，圖示是裝飾影像，不應該有替代文字。 圖示的語法為：

```Markdown
:::image type="icon" source="<folderPath>":::
```

若 `type="icon"`，則應指定 `source`。

## <a name="included-markdown-files"></a>include 的 Markdown 檔案

在多篇文章中需要重複 Markdown 檔案的情況，您可以使用 include 檔案。 include 功能會指示 Docs 在組建階段以 include 檔案的內容取代參考。 您可以下列方式使用 include：

- 內嵌：在一個句子中重複使用常用程式碼片段內嵌。
- 區塊：您重複使用整個 Markdown 檔案作為區塊 (巢狀嵌入文章中的小節)。

內嵌或區塊 include 檔案是簡單的 Markdown (.md) 檔案。 它可以包含任何有效的 Markdown。 include 檔案通常放在通用的*includes* 子目錄中，此子目錄則位於存放庫的根目錄。 當文章發行之後，包含的檔案會直接整合到其中。

### <a name="includes-syntax"></a>include 語法

區塊 include 是自己一行：

```markdown
[!INCLUDE [<title>](<filepath>)]
```

內嵌 include 是放在一行之中：

```markdown
Text before [!INCLUDE [<title>](<filepath>)] and after.
```

其中 `<title>` 是檔案的名稱，而 `<filepath>` 是檔案的相對路徑。 `INCLUDE` 必須大寫，而且 `<title>` 前面必須有一個空格。

以下是 Include 檔案的需求與考量：

- 針對大量內容 (例如一兩個段落、共用的程序或共用的節) 使用區塊包含。 請勿將它們用在小於一個句子的內容。
- include 檔案將不會在文章的 GitHub 轉譯檢視中呈現，因為它們依靠 Docs 延伸模組。 它們將會在發行集之後才轉譯。
- 請務必將 include 檔案中的文字撰寫成完整的句子或片語，且不相依於參考 include 之文章中的上下文。 忽略此指導方針會使文章中產生無法翻譯的字串。
- 請勿將 include 檔案嵌入其他 include 檔案中。
- 將媒體檔案放在包含資料夾的特定 media 資料夾中，例如 */includes/media`<repo>`* 資料夾。 media  目錄的根目錄中不應包含任何影像。 如果 include 沒有影像，則不需要對應的 media  目錄。
- 對於一般文章，請勿在不同包含檔案之間共用媒體。 請針對每個包含檔案和文章，使用具有唯一名稱的個別檔案。 將媒體檔案儲存在與該包含檔案相關聯的 [media] 資料夾。
- 請勿將包含檔案做為文章的唯一內容。  包含檔案是設計成用來補充文章其他部分中的內容。

## <a name="links"></a>連結

如需此連結的語法詳細資訊，請參閱 [在文件中使用連結](how-to-write-links.md)。

## <a name="lists-numbered-bulleted-checklist"></a>清單 (編號、分項、檢查清單)

### <a name="numbered-list"></a>編號清單

若要建立編號清單，您可以全部使用 1。 發佈時，數字會以遞增順序轉譯為連續清單。 為了讓來源更方便閱讀，您可以手動遞增清單。

請不要在清單中使用字母，包括巢狀清單。 發佈至 Docs 時，字母無法正確轉譯。如果是使用數字的巢狀清單，系統在發佈時會轉譯為小寫字母。 例如：

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

這會轉譯為：

1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)

### <a name="bulleted-list"></a>項目符號清單

若要建立項目符號清單，請在每行開頭使用 `-` 或 `*` 後接空格：

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

這會轉譯為：

- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!

無論您使用哪種語法，`-` 或 `*`，請在同一篇文章中一致使用它。

### <a name="checklist"></a>檢查清單

您可透過自訂 Markdown 延伸模組，在 Docs 上使用檢查清單：

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

此範例在 Docs 上的轉譯如下：

> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3

您可在文章的開頭或結尾使用檢查清單，來摘要「您將學到什麼」或「您已學到的內容」。 請不要在整篇文章中新增隨機檢查清單。

## <a name="next-step-action"></a>下一步動作

您可使用自訂延伸模組，將 next step (下一步動作) 按鈕新增至 Docs 頁面。

語法如下：

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

例如：

```markdown
> [!div class="nextstepaction"]
> [Learn about adding code to articles](code-in-docs.md)
```

這會轉譯為：

> [!div class="nextstepaction"]
> [Learn about adding code to articles](code-in-docs.md)

您可以在下一步動作中使用任何支援的連結，包括其他網頁的 Markdown 連結。 在大部分情況下，下一步動作連結都是相同文件集中其他檔案的相對連結。

## <a name="non-localized-strings"></a>不可當地語系化的字串

您可以使用自訂 `no-loc` (不可當地語系化) Markdown 延伸模組，來識別您想要當地語系化過程忽略的內容字串。

所有被點名的字串都區分大小寫；也就是說，字串必須完全相同，才會被忽略不進行當地語系化。

若要將個別字串標記為不可當地語系化，請使用下列語法：

```markdown
:::no-loc text="String":::
```

例如，在下列範例中，當地語系化過程只會忽略唯一一個 `Document`：

```markdown
# Heading 1 of the Document

Markdown content within the :::no-loc text="Document":::.  The are multiple instances of Document, document, and documents.
```

> [!NOTE]
> 使用 `\` 逸出特殊字元：
> ```markdown
> Lorem :::no-loc text="Find a \"Quotation\""::: Ipsum.
> ```

您也可以使用 YAML 標頭中的中繼資料，將目前 Markdown 檔案中的所有字串例項標記為不可當地語系化：

```yml
author: cillroy
no-loc: [Global, Strings, to be, Ignored]
```

> [!NOTE]
> docfx.json  檔案中不支援以 no-loc 中繼資料做為全域中繼資料。 當地語系化管線不會讀取 docfx.json  檔案，因此必須將 non-loc 中繼資料加入每個個別來源檔案。

在下列範例中，在中繼資料 `title` 中以及在 Markdown 標頭中的 `Document`，都會在當地語系化過程中被忽略。

在中繼資料 `description` 和 Markdown 主要內容中的 `document` 都會當地語系化，因為它的開頭不是大寫 `D`。

```markdown
---
title: Title of the Document
author: author-name
description: Description for the document
no-loc: [Title, Document]
---
# Heading 1 of the Document

Markdown content within the document.
```

<!-- commenting out for now because no one knows what this means
## Section definition

You might need to define a section. This syntax is mostly used for code tables.
See the following example:

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

The preceding blockquote Markdown text will be rendered as:
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
-->

## <a name="selectors"></a>選取器

selector (選取器) 是使用者介面元素，可讓使用者在同一篇文章的多個類別之間切換。 某些文件集會使用選取器來解決跨技術或平台的實作差異。 一般而言，選取器非常適合開發人員的行動平台內容。

因為相同的選取器 Markdown 會進入使用 selector 的每個文章檔案，我們建議您將文章的選取器放在 include 檔案中。 接著，您可以在您所有使用相同選取器的文章檔案中參考該 include 檔案。

目前有兩種選擇器：single selector (單一選取器) 和 multi-selector (多重選取器)。

### <a name="single-selector"></a>單一選取器

```markdown
> [!div class="op_single_selector"]
> - [Universal Windows](../articles/notification-hubs-windows-store-dotnet-get-started/)
> - [Windows Phone](../articles/notification-hubs-windows-phone-get-started/)
> - [iOS](../articles/notification-hubs-ios-get-started/)
> - [Android](../articles/notification-hubs-android-get-started/)
> - [Kindle](../articles/notification-hubs-kindle-get-started/)
> - [Baidu](../articles/notification-hubs-baidu-get-started/)
> - [Xamarin.iOS](../articles/partner-xamarin-notification-hubs-ios-get-started/)
> - [Xamarin.Android](../articles/partner-xamarin-notification-hubs-android-get-started/)
```

... 轉譯結果如下：

> [!div class="op_single_selector"]
> - [通用 Windows](how-to-write-links.md)
> - [Windows Phone](how-to-write-links.md)
> - [iOS](how-to-write-links.md)
> - [Android](how-to-write-links.md)
> - [Kindle](how-to-write-links.md)
> - [Baidu](how-to-write-links.md)
> - [Xamarin.iOS](how-to-write-links.md)
> - [Xamarin.Android](how-to-write-links.md)

### <a name="multi-selector"></a>多重選取器

```markdown
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](./mobile-services-dotnet-backend-ios-get-started-push.md)
> - [(iOS | JavaScript)](./mobile-services-javascript-backend-ios-get-started-push.md)
> - [(Windows universal C# | .NET)](./mobile-services-dotnet-backend-windows-universal-dotnet-get-started-push.md)
> - [(Windows universal C# | Javascript)](./mobile-services-javascript-backend-windows-universal-dotnet-get-started-push.md)
> - [(Windows Phone | .NET)](./mobile-services-dotnet-backend-windows-phone-get-started-push.md)
> - [(Windows Phone | Javascript)](./mobile-services-javascript-backend-windows-phone-get-started-push.md)
> - [(Android | .NET)](./mobile-services-dotnet-backend-android-get-started-push.md)
> - [(Android | Javascript)](./mobile-services-javascript-backend-android-get-started-push.md)
> - [(Xamarin iOS | Javascript)](./partner-xamarin-mobile-services-ios-get-started-push.md)
> - [(Xamarin Android | Javascript)](./partner-xamarin-mobile-services-android-get-started-push.md)
```

... 轉譯結果如下：

> [!div class="op_multi_selector" title1="平台" title2="後端"]
> - [(iOS | .NET)](how-to-write-links.md)
> - [(iOS | JavaScript)](how-to-write-links.md)
> - [(Windows 通用 C# | .NET)](how-to-write-links.md)
> - [(Windows 通用 C# | JavaScript)](how-to-write-links.md)
> - [(Windows Phone | .NET)](how-to-write-links.md)
> - [(Windows Phone | JavaScript)](how-to-write-links.md)
> - [(Android | .NET)](how-to-write-links.md)
> - [(Android | JavaScript)](how-to-write-links.md)
> - [(Xamarin iOS | JavaScript)](how-to-write-links.md)
> - [(Xamarin Android | JavaScript)](how-to-write-links.md)

## <a name="subscript-and-superscript"></a>下標和上標

您應該只在技術正確必需時才使用下標或上標，例如撰寫數學公式時。 請勿將它們用於非標準樣式，例如註腳。

下標和上標樣式請使用 HTML：

```html
Hello <sub>This is subscript!</sub>
```

這會轉譯為：

Hello <sub>This is subscript!</sub>

```html
Goodbye <sup>This is superscript!</sup>
```

這會轉譯為：

Goodbye <sup>This is superscript!</sup>

## <a name="tables"></a>Tables

在 Markdown 中建立表格的最簡單做法是使用直立線符號及線條。 若要建立含標題的標準表格，請沿著第一個線段與虛線：

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

這會轉譯為：

|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!||

您可以使用冒號對齊資料行：

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

轉譯如下：

| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |

> [!TIP]
> 適用於 VS Code 的 Docs 編寫延伸模組可讓您輕鬆新增基本 Markdown 表格！
>
> 您也可以使用[線上表格產生器](http://www.tablesgenerator.com/markdown_tables)。

### <a name="line-breaks-within-words-in-any-table-cell"></a>任何表格儲存格中的單字內換行

Markdown 表格中的長單字可能會使表格擴展到右側導覽，變得難以閱讀。 您可以允許 Docs 轉譯視需要在單字中自動插入換行，來解決此問題。 您只要使用自訂類別 `[!div class="mx-tdBreakAll"]` 加在表格前後即可。

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
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|

### <a name="line-breaks-within-words-in-second-column-table-cells"></a>表格第二資料行儲存格中的單字內換行

您可能只想要將換行自動插入表格的第二資料行中的單字內。 若要將換行限於第二資料行，您可以如先前所述，使用 `div` 包裝函式語法來套用 `mx-tdCol2BreakAll` 類別。

### <a name="data-matrix-tables"></a>資料矩陣表格

資料矩陣表格同時具有標頭與加權第一欄，並在左上方建立具有空白儲存格的矩陣。 Docs 具有資料矩陣表格的自訂 Markdown：

```md
|                  |Header 1 |Header 2|
|------------------|---------|--------|
|**First column A**|Cell 1A  |Cell 2A |
|**First column B**|Cell 1B  |Cell 2B |
```

第一欄中的每個項目都必須將樣式設為粗體 (`**bold**`)；否則，這些表格將無法供螢幕助讀程式存取，或不適用於 Docs。

### <a name="html-tables"></a>HTML 表格

HTML 表格不建議用於 docs.microsoft.com。 這類表格不是使用者可看懂的來源，而這與 Markdown 主要準則抵觸。
