---
title: 如何在文件中使用連結
description: 本文提供在 docs.microsoft.com 內建立內容連結的相關指引。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: gewarren
ms.author: gewarren
ms.date: 03/31/2020
ms.openlocfilehash: ca29d4b9e81f8af3b680367b210bd1734860687d
ms.sourcegitcommit: 5ef2dc72e2ff8bddf873415a3f4b816eb16029dd
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/03/2020
ms.locfileid: "80624774"
---
# <a name="use-links-in-documentation"></a>在文件中使用連結

本文描述如何在 docs.microsoft.com 上裝載的頁面中使用超連結。 使用一些不同的慣例，可以輕易地將連結新增至 Markdown。 連結可將使用者指向相同頁面、其他相鄰頁面，或外部網站與 URL 中的內容。

docs.microsoft.com 網站後端使用「開放式發行服務」(OPS)，可支援透過 [Markdig][] 剖析引擎且符合 [CommonMark][] 規範的 Markdown。 這個 Markdown 變體大多與 [GitHub 變體 Markdown (GFM)][GFM] 相容，因為大多數文件都儲存在 GitHub 中並可在該處編輯。 額外的功能可透過 Markdown 延伸模組新增。

> [!IMPORTANT]
> 只要目標有支援 (絕大部分都會支援) 安全協定，所有連結都必須使用安全協定 (`https` 相對於 `http`)。

## <a name="link-text"></a>連結文字

您包含在連結文字中的字詞應該淺顯易懂。 換句話說，它們應該是簡單的英文單字，或您要連結之網頁的標題。

> [!IMPORTANT]
> 請勿使用「按一下這裡」。 這對搜尋引擎最佳化而言並不是一個好的選擇，且沒有適當地描述目標。

**正確：**

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://docs.microsoft.com/sql/t-sql/statements/set-transaction-isolation-level-transact-sql) reference.`

**不正確：**

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a>文章之間的連結

發佈系統支援兩種超連結類型：**URL** 和**檔案連結**。

URL 連結可以是相對於 docs.microsoft.com 根目錄的 URL 路徑，或包含完整 URL 語法的絕對 URL (例如 `https://github.com/MicrosoftDocs/PowerShell-Docs`)。

- 連結到目前 _docset_ 的外部內容，或在 docset 內自動產生的參照與概念性文章之間連結時，請使用 URL 連結。
- 建立相對連結的最簡單方式，就是從瀏覽器複製 URL，然後將 `https://docs.microsoft.com/en-us` 從貼到 Markdown 的值中移除。
   - 請勿在 Microsoft 屬性的 URL 中包含地區設定 (例如，請移除 URL 中的 "/en-us")。

檔案連結是用來將 docset 內的某篇文章連結到另一篇文章。

- 所有檔案路徑都會使用正斜線 (`/`) 字元，而不是反斜線字元。
- 將文章連結到相同目錄中的另一篇文章：

  `[link text](article-name.md)`

- 將文章連結到當前目錄的父目錄中文章：

  `[link text](../article-name.md)`

- 將文章連結到當前目錄的子目錄中文章：

  `[link text](directory/article-name.md)`

- 將文章連結到當前目錄的父目錄中，其他子目錄中文章：

  `[link text](../directory/article-name.md)`

> [!NOTE]
> 上述範例均未在連結中使用 `~/`。 若要連結到從存放庫根開始的絕對路徑，請使用 `/` 來啟動連結。 瀏覽 GitHub 上的原始碼存放庫時，置入 `~/` 會產生無效的連結。 在路徑的開頭使用 `/` 即可正確解決。

### <a name="structure-of-links-on-docsmicrosoftcom"></a>docs.microsoft.com 上的連結結構

在 docs.microsoft.com 上發佈的內容具有下列 URL 結構：

```
https://docs.microsoft.com/<locale>/<product-service>/[<feature-service>]/[<subfolder>]/<topic>[?view=<view-name>]
```

範例：

```
https://docs.microsoft.com/en-us/azure/load-balancer/load-balancer-overview
https://docs.microsoft.com/en-us/powershell/azure/overview?view=azurermps-5.1.1
```

- `<locale>` - 識別文章的語言 (例如：en-us 或 de-de)
- `<product-service>` - 產品或服務的名稱 (例如：powershell、dotnet 或 azure)
- `[<feature-service>]` - (選用) 產品的功能或子服務名稱 (例如：csharp 或 load-balancer)
- `[<subfolder>]` - (選用) 功能內的子資料夾名稱
- `<topic>` - 主題的文章檔案名稱 (例如：load-balancer-overview 或 overview)
- `[?view=\<view-name>]` - (選用) 版本選取器針對具有多個可用版本的內容所使用檢視名稱 (例如：azps-3.5.0)

> [!TIP]
> 在大部分情況下，相同 _docset_ 中的文章會有相同 `<product-service>` URL 片段。 例如：
> - 相同的 docset
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/dotnet/framework/install`
> - 不同的 docset
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/visualstudio/whats-new`

## <a name="bookmark-links"></a>書籤連結

若要讓書籤連結到「目前」  檔案中的標題，請使用井字符號，後面接著小寫標題文字。 移除標題中的標點符號，並以破折號取代空格：

```markdown
[Managed Disks](#managed-disks)
```

若要連結到另一篇文章中的書籤標題，請使用檔案相對或網站相對連結加上井字符號，後面接著標題文字。 移除標題中的標點符號，並以破折號取代空格：

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

您也可以從 URL 複製書籤連結。 若要尋找 URL，請將滑鼠暫留在 docs.microsoft.com 的標題列上。 您應該會看到出現一個連結圖示：

![文章標題中的連結圖示](media/how-to-write-links/bookmark-link.png)

按一下連結圖示，然後從 URL 複製書籤錨點文字 (也就是井字符號後面的部分)。

> [!NOTE]
> Docs 延伸模組也有協助建立連結的工具。

### <a name="explicit-anchor-links"></a>明確錨點連結

除非在中樞和登陸頁面中，否則沒有必要也不建議新增使用 `<a>` HTML 標籤的明確錨點連結。 相反地，請使用自動產生的書籤，如[書籤連結](#bookmark-links)中所述。 針對中樞和登陸頁面，請如下所示宣告錨點：

```markdown
## <a id="anchortext" />Header text
```

或

```markdown
## <a name="anchortext" />Header text
```

且下列會連結到錨點：

```markdown
To go to a section on the same page:
[text](#anchortext)

To go to a section on another page.
[text](filename.md#anchortext)
```

> [!NOTE]
> 錨點文字必須一律為小寫，且不能包含空格。

## <a name="xref-cross-reference-links"></a>XRef (交互參照) 連結

XRef 連結是連結到 API 的建議方式，因為這些連結會在建置時進行驗證。 若要連結到目前 docset 或其他 docset 中自動產生的 API 參照頁面，請搭配類型或成員的唯一識別碼 ([UID](#determine-the-uid)) 來使用 XRef 連結。

> [!TIP]
> 您可使用[適用於 VS Code 的 Docs Markdown 延伸模組][docsextension] (Docs Authoring Pack 的一部分)，以插入 [.NET API 瀏覽器][]中呈現的 .NET XRref 連結。

在 [.NET API 瀏覽器][] 或 [Windows UWP][] 搜尋方塊中鍵入完整名稱或其中一部分，以檢查所要連結的 API 是否在 [docs.microsoft.com][docs] 上。 如果沒有看到任何顯示的結果，則該類型目前還不在 docs.microsoft.com 上。

您可以使用下列其中一個語法：

- 自動連結：

   ```markdown
   <xref:UID>
   <xref:UID?displayProperty=nameWithType>
   ```

   根據預設，連結文字只會顯示成員或型別名稱。 選用的 `displayProperty=nameWithType` 查詢參數會產生完整連結文字；亦即，**namespace.type** 表示類型，而 **type.member** 表示類型成員 (包括列舉類型成員)。

- Markdown 式連結：

   ```markdown
   [link text](xref:UID)
   ```

   當想要自訂顯示的連結文字時，請針對 XRef 使用 Markdown 式連結。

範例：

- **\<xref:System.String>** 會顯示為 <xref:System.String>

- **\<xref:System.String?displayProperty=nameWithType>** 會顯示為 <xref:System.String?displayProperty=nameWithType>

- **\[String 類別](xref:System.String)** 會顯示為 [String 類別](xref:System.String)。

在類別中，`displayProperty=fullName` 查詢參數的運作方式與 `displayProperty=nameWithType` 相同。 亦即，連結文字會變成 **namespace.classname**。 不過，若是成員，則連結文字會顯示為 **namespace.classname.membername**，這可能不適當。

> [!NOTE]
> UID 會區分大小寫。 例如，`<xref:System.Object>` 會正確解析，但 `<xref:system.object>` 則不會。

### <a name="xref-build-warnings-and-incremental-builds"></a>XRef 建置警告和累加建置

累加建置只會建置已變更或受變更影響的檔案。 如果看到有關 XREF 連結無效的建置警告，但此連結實際上有效，這可能是因為建置是累加的。 造成警告的檔案並未變更，因此不會建置，且會重新顯示過去的警告。 當檔案變更時，或如果觸發完整建置 (可在 ops.microsoft.com 上啟動完整建置)，警告就會消失。 這是累加建置的缺點，因為 DocFX 無法偵測到 XREF 服務內的資料更新。

### <a name="determine-the-uid"></a>判斷 UID

UID 通常是完整類別或成員名稱。 至少有兩種方式可判斷 UID：

- 以滑鼠右鍵按一下類型或成員的 [Docs][docs] 頁面，選取 [檢視原始檔]  ，然後複製 **ms.assetid** 的 **content** 值：

  ![網頁原始檔中的 ms.assetid](media/how-to-write-links/ms-assetid.png)

- 將部分或完整的類型名稱附加到 URL，以使用[自動完成網站][]。 例如，在瀏覽器的網址列中輸入 `https://xref.docs.microsoft.com/autocomplete?text=Writeline`，會顯示其名稱中包含 **Writeline** 的所有類型和方法，以及其 UID。

#### <a name="verify-the-uid"></a>驗證 UID

若要測試是否有正確的 UID，請以 UID 取代下列 URL 中的 **System.String**，然後將其貼到瀏覽器的網址列中：

`https://xref.docs.microsoft.com/query?uid=System.String`

> [!TIP]
> URL 中的 UID 會區分大小寫，且如果正在檢查方法多載 UID，請不要在參數類型之間加入空格。

如果看到類似如下的內容，表示具有正確的 UID：

```text
[{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,...xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"},{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,netframework-4.6,netframework-4.6.1,...,xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"}]
```

如果只看到頁面上顯示 `[]`，則表示具有錯誤的 UID。

### <a name="percent-encoding-of-urls"></a>URL 的百分號編碼

UID 中的特殊字元必須以 HTML 編碼，如下所示：

| 字元 | HTML 編碼 |
| --------- | ------------- |
| `` ` ``   | %60           |
| `#`       | %23           |
| `*`       | %2A           |

請參閱[百分號編碼](https://en.wikipedia.org/wiki/Percent-encoding)的完整清單。

編碼範例：

- `System.Threading.Tasks.Task``1` 會編碼為 `System.Threading.Tasks.Task%601` (請參閱[泛型型別](#generic-types)一節)

- `System.Exception.#ctor` 會編碼為 `System.Exception.%23ctor`

- `System.Object.Equals*` 會編碼為 `System.Object.Equals%2A`

### <a name="generic-types"></a>泛型型別

泛型型別是指 `System.Collections.Generic.List<T>` 之類的類型。 如果在 [.NET API 瀏覽器](https://docs.microsoft.com/dotnet/api/)中瀏覽至此類型並查看其 URL，則會看到 `<T>` 在 URL 中寫成 `-1`，這實際上代表 **`1**：

`https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1`

若要連結到泛型型別 (例如 **List\<T>** )，請將 **\`** 倒單引號字元編碼為 **%60**，如下列範例所示：

```markdown
<xref:System.Collections.Generic.List%601>
```

### <a name="methods"></a>方法

若要連結到方法，可在方法名稱後面加上星號 (`*`) 來連結到一般方法，或連結到特定多載。 例如，當想要連結到不含特定參數類型的 `<xref:System.Object.Equals%2A?displayProperty=nameWithType>` 方法時，請使用一般頁面。 星號字元會編碼為 `%2A`。 例如：

`<xref:System.Object.Equals%2a?displayProperty=nameWithType>` 會連結到 <xref:System.Object.Equals%2A?displayProperty=nameWithType>

若要連結到特定多載，請在方法名稱後面加上括弧，並包含每個參數的完整類型名稱。 請勿在類型名稱之間加入空白字元，否則連結將無法使用。 例如：

`<xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>` 會連結到 <xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>

## <a name="links-from-includes"></a>從包含檔案的連結

因為包含檔案位於另一個目錄中，所以您必須使用較長的相對路徑。 若要從包含檔案連結到文章，請使用此格式：

```markdown
[link text](../articles/folder/article-name.md)
```

> [!TIP]
> 適用於 Visual Studio Code 的 [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) 延伸模組有助於正確插入相對連結和書籤，而不需與冗長的路徑奮戰。

## <a name="links-in-selectors"></a>選取器中的連結

選取器是在文件文章中顯示為下拉式清單的導覽元件。 當讀者在下拉式清單中選取一個值時，瀏覽器會開啟選取的文章。 一般而言，選取器清單會包含密切相關的文章連結，例如多種程式設計語言的相同主題，或密切相關的系列文章。

如果您擁有內嵌在包含檔案中的選取器，則可以使用下列連結結構：

   ```markdown
   > [AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]
   - [(Text1 | Example1 )](../articles/folder/article-name1.md)
   - [(Text1 | Example2 )](../articles/folder/article-name2.md)
   - [(Text2 | Example3 )](../articles/folder/article-name3.md)
   - [(Text2 | Example4 )](../articles/folder/article-name4.md)
   ```

## <a name="reference-style-links"></a>參考風格連結

您可以使用參考風格連結，讓來源內容更容易閱讀。 參考風格連結會將內嵌連結語法取代為簡化語法，允許您將較長的 URL 移動到文章的結尾。 以下是 [Daring Fireball](https://daringfireball.net/projects/markdown/) 的範例：

內嵌文字：

   ```markdown
   I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].
   ```

文章結尾處的連結參考：

   ```markdown
   <!--Reference links in article-->
   [1]: http://google.com/
   [2]: http://search.yahoo.com/
   [3]: http://search.msn.com/
   ```

請確定您包含冒號之後的空格 (連結之前)。 當您連結到其他技術文章時，如果忘記包含空格，已發佈的文章中的連結將會中斷。

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a>連結到不屬於技術文件集的頁面

若要連結到 Microsoft 網站上的另一個頁面 (例如定價頁面、SLA 頁面或任何不屬於文件文章的頁面)，請使用絕對 URL，但省略地區設定。 此目的為本連結可於 GitHub 和轉譯的網站上運作：

   ```markdown
   [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)
   ```

## <a name="links-to-third-party-sites"></a>連結到協力廠商網站

最佳使用者體驗會減少將使用者傳送到其他網站的情況。 因此，以此資訊作為我們有時需要之任何協力廠商網站連結的基礎：

- **責任**：當所要共用的資訊是協力廠商資訊時，連結到協力廠商內容。 例如，告知大家如何使用 Android 開發人員工具，並不是 Microsoft 的立場，那是 Google 的資訊。 如果有需要，我們可以解釋如何*搭配* Azure 使用 Android 開發人員工具，但 Google 應該說明如何使用其工具。
- **PM 簽核**：要求 Microsoft 簽核協力廠商內容。 透過與之連結，表示我們對其信任以及我們在人們遵循指示時的義務。
- **時效性檢閱**：確定協力廠商資訊仍是最新、正確且相關，且連結並未變更。
- **異地**：讓使用者了解他們將前往另一個網站。 如果上下文不清楚，請加入一個限定詞組。 例如：「必要條件包括 Android 開發人員工具，其可在 Android Studio 網站上下載」。
- **後續步驟**：舉例來說，可在＜後續步驟＞一節中新增一個 MVP 部落格連結。 同樣地，請確認使用者了解他們將會離開網站。
- **法律**：在所有 microsoft.com 頁面的**使用條款**頁尾中，**第三方網站的連結**規定了相關法律事宜。

<!-- link references -->
[CommonMark]: https://commonmark.org/
[Markdig]: https://github.com/lunet-io/markdig
[GFM]: https://help.github.com/categories/writing-on-github/
[docs]: https://docs.microsoft.com
[.NET API 瀏覽器]: https://docs.microsoft.com/dotnet/api/
[Windows UWP]: https://docs.microsoft.com/uwp/api
[docsextension]: https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown
[自動完成網站]: https://xref.docs.microsoft.com/autocomplete?text=
