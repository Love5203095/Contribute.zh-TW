---
title: PowerShell 文章的範本和速查表
description: 本文包含一個方便的範本，您可以使用該範本為 PowerShell 文件建立新文章
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 073a44240b1aa4baa9e655dab069097d21cdd66d
ms.sourcegitcommit: 804a99b89785e5c8f056a9da3f0fbde9f0a56a51
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2020
ms.locfileid: "78331921"
---
# <a name="markdown-style-guide-for-powershell-docs"></a>適用於 PowerShell 文件的 Markdown 樣式指南

本文提供一些 PowerShell 文件內容特定的樣式指導。

如需其他撰寫樣式指導，請參閱 [Microsoft 樣式指南](https://docs.microsoft.com/style-guide/welcome/)。

## <a name="metadata"></a>中繼資料

此範本包含 Markdown 語法的範例，以及設定中繼資料的指導。
當建立 Markdown 檔案時，您應將包含的範本複製到新檔案中、依照如下指定來填寫中繼資料，並將以上 H1 標題設為文章標題。

所需的中繼資料區塊位於下列範例中繼資料區塊中：

```md
---
author: [GITHUB USERNAME]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
title: [ARTICLE TITLE]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- 冒號 (:) 和中繼資料項目的值之間**必須**有空格。
- 值中的冒號 (例如標題) 會中斷中繼資料解析器。 在此情況下，請使用雙引號來括住標題 (例如 `title: "Writing .NET Core console apps: An advanced step-by-step guide"`)。
- **作者**：作者欄位應包含作者的 **GitHub 使用者名稱**。
- **描述**：會摘要文章的內容。 通常會顯示於搜尋結果頁面，但不會用於搜尋排名。 長度應為 115-145 個字元，包括空格。
- **ms.date**：上次重大更新的日期。 如果您已檢閱並更新整篇文章，請在現有文章中對此進行更新。 錯字或類似內容的小修正不保證會更新。
- **標題**：會出現在搜尋引擎結果中。 標題不應與 H1 標題中的標題相同，且不應超過 60 個字元。

其他中繼資料會附加至每篇文章，但我們通常會在資料夾層級套用大多數中繼資料值 (在 **docfx.json** 中指定)。

## <a name="product-terminology"></a>產品術語

PowerShell 的變數有好幾種。 下表定義一些用來討論 PowerShell 的不同字詞。

- **PowerShell** - 此為預設值。 PowerShell 是我們的隨附產品。 PowerShell 一詞可用於描述產品的任何版本。
- **PowerShell Core** - 針對任何支援的平台，以 .NET Core Common Language Runtime (CoreCLR) 為基礎建置的 PowerShell。
- **Windows PowerShell** - 以 .NET Framework Common Language Runtime (CLR) 為基礎建置的 PowerShell。 Windows PowerShell 只隨附於 Windows，且需要完整的 .Net Framework CLR。

一般而言，文件中的 "Windows PowerShell" 參考可以變更為 "PowerShell"。
但在討論 Windows 特定技術時，**不**應該變更 "Windows PowerShell"。

## <a name="basic-markdown-gfm-and-special-characters"></a>基本 Markdown、GFM 和特殊字元

您可以透過 [Markdown 參考](../markdown-reference.md)一文了解 Markdown、GitHub Flavored Markdown (GFM) 和 OPS 特定延伸模組的基本知識。

Markdown 使用 \*、\` 和 \# 等特殊字元來格式化。 如果您希望將其中一個字元包含在內容中，則必須執行以下兩項作業之一：

- 在特殊字元前加上一個反斜線以將其「逸出」 (例如 `\*` 對於 \*)
- 為字元使用 [HTML 實體程式碼](http://www.ascii.cl/htmlcodes.htm) (例如，`&#42;` 對於 &#42;)。
- Markdown 檔案應使用 ASCII 純文字或 UTF-8 編碼。 不過，需避免使用多位元組 UTF-8 字元。 請改用 HTML 實體。 例如，若為著作權符號，請使用 `&copy;`。
  其呈現為："&copy;"。

## <a name="hyperlinks"></a>超連結

- 請避免使用裸機 URL。 連結應使用 Markdown 語法 `[friendlyname](url-or-path)`
- 連結必須具有易記名稱，通常是連結主題的標題
- 底部＜相關連結＞一節中的所有項目都應該是超連結。
- 連結至裝載於 **docs.microsoft.com** 的其他內容時，請使用相對連結。
- 請勿在超連結的括弧內使用倒引號、粗體或其他標記。

如需連結的詳細資訊，請參閱[在文件中使用連結](../how-to-write-links.md)。

## <a name="filenames"></a>檔案名稱

檔案名稱使用下列規則：

- 只包含字母、數字和連字號。
- 沒有空格或標點符號字元。 檔案名稱中使用連字號來分隔文字和數字。
- 使用特定的動作動詞，例如 develop、buy、build、troubleshoot。 沒有 -ing 字詞。
- 不包含 a、and、the、in、or 等短字。
- 必須是 Markdown 格式且使用 .md 副檔名。
- 保持檔案名稱合理簡短。 它們是您文章 URL 的一部分。

## <a name="blank-lines-spaces-and-tabs"></a>空白行、空格及索引標籤

請移除重複的空白行。 多個空白行在 HTML 中會轉譯為單一空白行，因此不會有多個空白行的用途。

空白行還表示 Markdown 中的區塊結尾。 不同類型的 Markdown 組塊之間 (例如，段落與清單或標頭之間) 應該有一個空白。

> [!NOTE]
> 間距在 Markdown 中很重要。 應一律使用空格，而不是硬性索引標籤。 請移除行尾的多餘空格。

## <a name="titles-and-headings"></a>標題 (Title) 和標題 (heading)

僅使用 [ATX 標題][atx] (# 樣式，而不是 `=` 或 `-` 樣式標頭)。

- 使用句首大寫 - 只有專有名詞與標題或標頭的第一個字母應為大寫
- `#` 與標題的第一個字母之間必須有一個空格
- 標題應該以單一空白行括住
- 每份文件只能有一個 H1
- 標頭層級應該遞增一 - 不要略過層級
- 請勿在標頭中使用倒引號、粗體或其他標記

> [!CAUTION]
> [PlatyPS][platyPS] 對 Cmdlet 參考強制執行的結構描述需要特定 H2 和 H3 標頭。 新增或移除標頭可能會中斷組建。 如需詳細資訊，請參閱 [Cmdlet 參考樣式指南](powershell-style-reference.md)。

## <a name="limit-line-length-to-100-characters"></a>將行長度限制為 100 個字元

這可簡化差異和歷程記錄的命令列輸出。

此規則不會對 PowerShell 文件中的大部分現有內容強制執行，但我們正朝著此一方向努力。 歡迎您提供協助。Visual Studio Code (VSCode) 中的[自動重排延伸模組][reflow]，可讓您輕鬆地將段落重新格式化為此限制。

## <a name="lists"></a>清單

如果您的清單包含多個句子或段落，請考慮使用子層級標頭，而不是清單。

清單應該以單一空白行括住。

### <a name="unordered-lists"></a>未排序清單

請勿以句點結束清單項目，除非它們包含多個句子。 針對清單項目的項目符號，請使用連字號字元 (`-`)。 這可避免與使用星號 `*` 的粗體或斜體標記混淆。 若要在項目符號項目下包含段落或其他項目，請插入分行符號，並與項目符號後面的第一個字元對齊縮排。

例如：

```markdown
This is a list that contain sub-elements under a bullet item.

- First bullet item

  Sentence explaining the first bullet.

  - Sub-bullet item

    Sentence explaining the sub-bullet.

- Second bullet item
- Third bullet item
```

這是一個清單，其中包含項目符號項目下的子項目。

- 第一個項目符號項目

  說明第一個項目符號的句子。

  - 子項目符號項目

    說明子項目符號的句子。

- 第二個項目符號項目
- 第三個項目符號項目

### <a name="ordered-lists"></a>排序清單

若要在編號項目下包含段落或其他項目，請與項目編號後面的第一個字元對齊縮排。

```markdown
1. For the first element, insert a single space after the 1. Long sentences should be
   wrapped to the next line and must line up with the first character after the numbered
   list marker.

   To include a second element (like this one), insert a line break after the first
   and align indentations. The indentation of the second element must line up with
   the first character after the numbered list marker. For single digit items, like
   this one, you indent to column 4. For double digits items, for example item number
   10, you indent to column 5.

1. The next numbered item starts here.
```

取得此輸出：

> 1. 針對第一個項目，在 1 之後插入一個空格。 長句子應該換行到下一行，且必須與編號清單標記之後的第一個字元對齊。
>
>    若要包含第二個項目 (例如這一個)，請在第一個項目之後插入分行符號，並對齊縮排。 第二個項目的縮排必須與編號清單標記之後第一個字元對齊。 針對單位數項目 (例如這一個)，您可以縮排到第 4 欄。 針對雙位數項目 (例如項目編號 10)，則會縮排到第 5 欄。
>
> 1. 下一個編號項目會從這裡開始。

列出編號中的所有項目都應該使用數字 `1.`，而不是針對每個項目遞增。
Markdown 轉譯會自動遞增值。 這會讓重新排列項目變得更加容易，並將附屬內容的縮排標準化。

## <a name="formatting-command-syntax-elements"></a>格式化命令語法項目

- PowerShell Cmdlet 名稱使用 [Pascal 命名法][pascal-case]。 動詞會以連字號與名詞分隔。 請針對 Cmdlet 和參數一律使用完整的 Pascal 命名法名稱。 除非您特別討論別名，否則請避免使用別名。

- 在段落內，語言關鍵字、Cmdlet 名稱及變數參考都應該包裝在倒引號 (`` ` ``) 字元中。 屬性、參數及類別名稱應該是**粗體**。

  例如：

  ~~~markdown
  The following code assigns the output of `Get-ChildItem` to the `$files` variable.

  ```powershell
  $files = Get-ChildItem C:\Windows
  ```
  ~~~

- 透過名稱參考參數時，名稱應該是**粗體**。 在說明使用含連字號前置詞的參數時，參數應包裝在倒引號中。 例如：

  ```markdown
  The parameter's name is **Name**, but it is typed as `-Name` when used on the command
  line as a parameter.
  ```

- 參考外部命令 (EXE、指令碼等) 時，命令名稱應為粗體、全部小寫 (如果在句子開頭則為大寫)，並包含適當的副檔名。 例如：

  ```markdown
  For example, on Windows systems, you can use the `net start` and `net stop` commands
  to start and stop a service. **Sc.exe** is another service control tool for Windows.
  That name does not fit into the naming pattern for the **net.exe** service commands.
  ```

- 顯示外部命令的範例使用方式時，應將此範例包裝在倒引號中。
  當名稱與別名發生衝突時，您必須在命令範例中包含副檔名。 例如：

  ```markdown
  To start the spooler service on a remote computer named DC01, you type `sc.exe \\DC01 start spooler`.
  ```

- 在撰寫概念性文章 (相對於參考內容) 時，Cmdlet 名稱的第一個執行個體應該會以超連結方式連至 Cmdlet 文件。 請勿在超連結的括弧內使用倒引號、粗體或其他標記。

  例如：

  ```markdown
  This [Write-Host](/powershell/module/Microsoft.PowerShell.Utility/Write-Host) cmdlet
  uses the **Object** parameter to ...
  ```

  如需詳細資訊，請參閱樣式指南的＜超連結＞[](#hyperlinks)一節。

## <a name="images"></a>影像

包含影像的語法如下：

```Syntax
![[alt text]](<folderPath>)
```

範例：

```markdown
![Introduction](./media/overview/Introduction.png)
```

其中，`alt text` 是影像的簡短描述，而 `<folder path>` 是影像的相對路徑。 適用於視障者的螢幕助讀程式需要使用替代文字。 若發生影像無法呈現的網站 Bug 時，替代文字也很實用。

影像應儲存在包含您文章的資料夾內 `media/<article-name>` 資料夾中。 不應在文章之間共用影像。 請在 `media` 資料夾底下，建立符合您文章檔案名稱的資料夾。 將該文章的影像複製到該新資料夾。 如果有多個文章使用某個影像，則每個影像資料夾都必須有該影像檔案的複本。 這種做法可防止某篇文章中的影像變更影響另一篇文章。

在某些情況下，您會想要跨多篇文章共用影像，例如標誌和圖示。 這些影像會儲存在存放庫根目錄的 `/media/shared` 資料夾中。

支援下列影像檔案類型：*.png"、*.gif"、*.jpeg"、*.jpg"、*.svg

<!-- External URLs -->
[platyPS]: https://github.com/PowerShell/platyPS
[markdig]: https://github.com/lunet-io/markdig
[CommonMark]: https://spec.commonmark.org/
[atx]: https://github.github.com/gfm/#atx-headings
[pascal-case]: https://en.wikipedia.org/wiki/PascalCase
[reflow]: https://marketplace.visualstudio.com/items?itemName=marvhen.reflow-markdown
