---
title: 參與 .NET 文件存放庫
description: 本文會描述在存放庫中參與文章和程式碼的流程範例，其組成 .NET 文件。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 05/14/2020
ms.openlocfilehash: d1631f34ef9a3ceb10178792842421376fea97b0
ms.sourcegitcommit: 3774d06ddc1f92b2bdb4c1d8babbd18357229298
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/28/2020
ms.locfileid: "87264801"
---
# <a name="learn-how-to-contribute-to-the-net-docs-repositories"></a>了解如何參與 .NET 文件存放庫

感謝您對於參與 .NET 文件感到興趣！

本文件涵蓋參與 [.NET 文件網站](https://docs.microsoft.com/dotnet)上所裝載文章和程式碼範例的程序。 這些參與可以是簡單的錯字校正，也可以是複雜的新文章。

.NET 文件網站是從多個存放庫建置而來：

- [.NET 概念文章和程式碼片段](https://github.com/dotnet/docs)
- [程式碼範例和程式碼片段](https://github.com/dotnet/samples)
- [.NET Standard、.NET Core、.NET Framework API 參考](https://github.com/dotnet/dotnet-api-docs)
- [.NET Compiler Platform SDK 參考](https://github.com/dotnet/roslyn-api-docs)
- [ML.NET API 參考](https://github.com/dotnet/ml-api-docs)

這些存放庫的問題都已在 [dotnet/docs](https://github.com/dotnet/docs/issues) 存放庫中進行追蹤。

## <a name="guidelines-for-contributions"></a>參與方針

感謝社群對文件的參與。下列清單顯示參與 .NET 文件時應注意的一些指導規則：

- **請勿**出其不意地提交大量提取要求。 相反地，請提出一個問題並開始討論，先讓我們就大方向取得共識再投入大量時間。
- **務必**遵循這些指示，以及[語態和語調](dotnet-voice-tone.md)方針。
- **務必**使用[範本](dotnet-style-guide.md)檔案作為您工作的起點。
- **務必**先在您的分支上建立個別分支，再參與文章。
- **務必**遵循 [GitHub flow](https://guides.github.com/introduction/flow/)(GitHub 流程)。
- 若想要的話，請**務必**針對參與來撰寫部落格文章和推文 (或透過其他方式)！

遵循這些方針將有助於確保您與我們都有更佳的體驗。

## <a name="make-a-contribution-to-net-docs"></a>參與 .NET 文件

**步驟 1：** 如果您對撰寫新內容或全面回顧現有內容感興趣，請開啟描述您要執行之作業的[問題](https://github.com/dotnet/docs/issues)。 **文件**資料夾的內容會組織成章節並反映在目錄 (TOC) 中。 請定義主題在 TOC 中的位置。 然後取得此提案的意見反應。

-或-

選擇現有問題並加以解決。 您可查看 [open issues](https://github.com/dotnet/docs/issues) (開啟的問題) 清單，並自願參與任何感興趣的問題：

- 依照 [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) 標籤進行篩選，以取得良好或優先處理的問題。
- 依照 [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) 標籤進行篩選，以取得適合由社群進行貢獻的問題。 這些問題通常僅需要最少的內容。
- 具備經驗的參與者可處理任何其感興趣的問題。

當找到要處理的問題時，請新增註解來詢問該問題是否處於開啟狀態。

一旦選擇了要參與的工作，請遵循[入門](../get-started-setup-github.md)指南以建立 GitHub 帳戶並設定環境。

**步驟 2：** 視需要派生 `/dotnet/docs`、`dotnet/samples`、`dotnet/dotnet-api-docs`、`dotnet/roslyn-api-docs` 或 `dotnet/ml-api-docs` 存放庫，並為您的變更建立分支。

若變更不大，請參閱參與者指南[首頁](../index.md#quick-edits-to-existing-documents)上有關在 GitHub 中編輯的指示。

**步驟 3：** 在此新分支上進行變更。

如果這是新主題，您可以使用此[範本檔案](dotnet-style-guide.md)作為起點。 其中包含撰寫方針，並同時說明每篇文章所需的中繼資料，例如作者資訊。 如需 docs.microsoft.com 網站中所使用 Markdown 語法的詳細資訊，請參閱 [Markdown 參考](../markdown-reference.md)。

請巡覽至步驟 1 中針對您文章所決定 TOC 位置的相對應資料夾。 該資料夾包含該區段中所有文章的 Markdown 檔案。 如有需要，請建立新的資料夾來放置您的內容檔案。 該區段的主要文章名為 *index.md*。

針對影像和其他靜態資源，請在包含您文章的資料夾中建立名為 **media** 的子資料夾 (如果尚未存在)。 在 **media** 資料夾中，建立具有文章名稱的子資料夾 (索引檔除外)。

針對**程式碼片段**，請在包含您文章的資料夾中建立名為 **snippets** 的子資料夾 (如果尚未存在)。 在 [snippets] 資料夾內，使用文章名稱建立子資料夾。 在大部分情況下，您會有三種主要 .NET 語言的程式碼片段：C#、F# 與 Visual Basic。 在該情況下，請分別建立名為 **chsarp**、**fsharp** 和 **vb** 的子資料夾，其分別適用於三種專案。 若正在為位於 [docs/csharp](https://github.com/dotnet/docs/tree/master/docs/csharp)、[docs/fsharp](https://github.com/dotnet/docs/tree/master/docs/fsharp) 或 [docs/visual-basic](https://github.com/dotnet/docs/tree/master/docs/visual-basic) 資料夾下的文章建立程式碼片段，由於程式碼片段只會以一種語言呈現，因此可忽略語言子資料夾。

程式碼片段為一種小篇幅、重點式的程式碼範例，用以示範文章中提及的概念。 大型程式 (供使用者下載與探索) 應該放在 [dotnet/samples](https://github.com/dotnet/samples) 存放庫中。 完整範例涵蓋在[參與範例](#contribute-to-samples)一節中。

## <a name="example-folder-structure"></a>範例資料夾結構

```
docs
  /about
  /core
    /porting
      porting-overview.md
      /media
        /porting-overview
          portability_report.png
      /snippets
        /porting-overview
          /csharp
            porting.csproj
            porting-overview.cs
            Program.cs
          /fsharp
            porting.fsproj
            porting-overview.fs
            Program.fs
          /vb
            porting.vbproj
            porting-overview.vb
            Program.vb
```

如上所示的結構包含一個影像 *portability_report.png*，以及三個程式碼專案，專案中含有 *porting-overview.md* 文章中的**程式碼片段**。 可接受的替代結構是為每種語言各建立一個專案，並將所有文章的所有程式碼片段放在該資料夾中。 因為僅使用篇幅非常小的程式碼片段示範語言語法，所以語言參考區域中才會使用此替代結構。 但不建議在其他區域中使用。

為了留下歷程記錄，許多包含的程式碼片段會儲存在 *dotnet/docs* 存放庫中的 */samples* 資料夾底下。 如果要大幅變更文章內容，則這些程式碼片段應移至新的結構。 如果只是要微調，請勿移動程式碼片段。

**步驟 4：** 從您的分支提交提取要求 (PR) 至主分支。

> [!IMPORTANT]
> 目前無法在任何 .NET 文件存放庫上使用[註解自動化](../how-to-write-workflows-major.md#review-and-sign-off)功能。 .NET 文件小組成員將會審查並合併您的 PR。

每個 PR 通常一次只能解決一個問題。 PR 可修改一或多個檔案。 如果您要解決不同檔案的多個修正，最好使用個別 PR。 如果要建立範例並更新 Markdown，則需要為範例建立個別 PR。

如果您的 PR 會修正現有問題，請將 `Fixes #Issue_Number` 關鍵字新增至認可訊息或 PR 描述。 如此一來，當 PR 合併之後，就會自動關閉問題。 如需詳細資訊，請參閱 [Closing issues via commit messages](https://help.github.com/articles/closing-issues-via-commit-messages/) (透過認可訊息關閉問題)。

.NET 小組將會審查您的 PR，並讓您知道是否需要任何其他更新/變更以通過核准。

**步驟 5：** 根據與小組的討論結果，對您的分支進行任何必要的更新。

一旦套用意見反應並核准您的變更，維護人員就會將您的 PR 合併到主分支。

我們會定期從主分支將所有認可推送至即時分支，之後您將能夠在 https://docs.microsoft.com/dotnet/ 上看到您的即時參與。 我們一般會在工作週期間每天發佈。

## <a name="contribute-to-samples"></a>參與範例

我們對程式碼進行了下列區別，以支援我們的內容：

- 範例：讀者可以下載並執行範例。 所有範例都應該是完整的應用程式或程式庫。 使用範例建立程式庫時，應該包含單元測試或應用程式，讓讀者執行程式碼。 這些範例通常會使用多項技術、功能或工具組。 每個範例的 readme.md 檔案會參考一篇文章，您可以閱讀以深入了解每個範例所包含的概念。
- 程式碼片段：說明較小的概念或工作。 它們可供編譯但並非用作完整的應用程式。 它們應該會正確執行，但不是典型案例的範例應用程式。 相反地，它們設計成盡可能小到足以說明單一概念或功能。 這些程式碼片段不應該超過一個螢幕的程式碼。

範例儲存在 [dotnet/samples](https://github.com/dotnet/samples) 存放庫中。 我們將致力於建立 samples 資料夾結構符合文件資料夾結構的模型。 我們遵循下列標準：

- 最上層資料夾會對應到 *docs* 存放庫中的最上層資料夾。 例如，文件存放庫具有 *machine-learning/tutorials* 資料夾，而機器學習服務教學課程的範例會位於 *samples/machine-learning/tutorials* 資料夾中。

此外，*core* 和 *standard* 資料夾下所有範例都應該在 .NET Core 支援的所有平台上建置和執行。 我們的 CI 建置系統將會強制執行該項作業。 最上層 *framework* 資料夾包含只能在 Windows 上建置和驗證的範例。

請盡可能在適用於指定範例的一組最廣泛平台上建置和執行範例專案。 實際上，這表示盡可能建置以 .NET Core 為基礎的主控台應用程式。 Web 或 UI 架構特定的範例應該視需要新增這些工具。 範例包括 Web 應用程式、行動應用程式、WPF 或 WinForms 應用程式等。

我們將致力於開發適用於所有程式碼的 CI 系統。 當您對範例進行任何更新時，請確定每項更新都是可建置專案的一部分。 在理想情況下，也可針對範例的正確性新增測試。

您所建立的每個完整範例都應該包含一個 *readme.md* 檔案。 此檔案應該包含範例的簡短描述 (一或兩個段落)。 您的 *readme.md* 應該告訴讀者探索此範例將會學到的內容。 *readme.md* 檔案也應該包含 [.NET 文件網站](https://docs.microsoft.com/dotnet/welcome)上即時文件的連結。 若要判斷存放庫中指定檔案對應至該網站的位置，請將存放庫路徑中的 `/docs` 取代為 `https://docs.microsoft.com/dotnet`。

您的主題也會包含範例連結。 這會直接連結至 GitHub 上的範例資料夾。

### <a name="write-a-new-sample"></a>撰寫新的範例

範例為可供下載的完整程式與程式庫。 範例的範圍可能很小，但會以可讓使用者自行探索與實驗的方式來示範概念。 範例的指導方針確保讀者可下載與探索。 檢查 [Parallel LINQ (PLINQ)](https://github.com/dotnet/samples/tree/master/csharp/parallel/PLINQ) 範例，以作為每個指導方針的範例。

1. 範例**必須是可建置專案的一部分**。 請盡可能在 .NET Core 支援的所有平台上建置專案。 但示範平台特定功能或平台特定工具的範例則除外。

2. 您的範例應該遵守 [C# Coding Style](https://github.com/dotnet/corefx/blob/master/Documentation/coding-guidelines/coding-style.md) (CoreFX 編碼樣式) 以確保一致性。

   此外，當示範不需要具現化新物件的內容時，我們偏好使用 `static` 方法，而不是執行個體方法。

3. 您的範例應該包含**適當的例外狀況處理**。 它應該處理範例內容中可能擲回的所有例外狀況。 例如，呼叫 [Console.ReadLine](https://docs.microsoft.com/dotnet/api/system.console.readline) 方法以擷取使用者輸入的範例應該在輸入字串作為引數傳遞至方法時，使用適當的例外狀況處理。 同樣地，如果您的範例預期方法呼叫失敗，則必須處理產生的例外狀況。 請務必處理方法所擲回的特定例外狀況，而不是 [Exception](https://docs.microsoft.com/dotnet/api/system.exception) 或 [SystemException](https://docs.microsoft.com/dotnet/api/system.systemexception) 等基底類別例外狀況。

4. 如果您的範例建置獨立套件，除了您範例所使用的任何執行階段之外，您還必須包含 CI 建置系統所使用的執行階段：
    - `win7-x64`
    - `win8-x64`
    - `win81-x64`
    - `ubuntu.16.04-x64`

不久將有適當的 CI 系統來建置這些專案。

若要建立範例：

1. 提出[問題](https://github.com/dotnet/docs/issues)，或對您目前參與的現有問題新增註解。
2. 撰寫主題，以說明您範例中所示範的概念 (例如：`docs/standard/linq/where-clause.md`)。
3. 撰寫您的範例 (例如：`WhereClause-Sample1.cs`)。
4. 建立 Program.cs，其中包含呼叫您範例的主要進入點。 如果已有此檔案，請將呼叫新增至您的範例：

    ```csharp
    public class Program
    {
        public void Main(string[] args)
        {
            WhereClause1.QuerySyntaxExample();

            // Add the method syntax as an example.
            WhereClause1.MethodSyntaxExample();
        }
    }
    ```

請使用可透過 [.NET Core SDK](https://www.microsoft.com/net/download) 安裝的 .NET Core CLI，來建置任何 .NET Core 程式碼片段或範例。 若要建置並執行您的範例：

1. 移至範例資料夾和組建以檢查是否有錯誤：

    ```console
    dotnet build
    ```
2. 執行您的範例：

    ```console
    dotnet run
    ```

3. 將 readme.md 新增至您範例的根目錄。

   這應該包含程式碼的簡短描述，並指示使用者前往參考該範例的文章。 *readme.md* 的最上層，必須具有[範例瀏覽器](https://docs.microsoft.com/samples)所需的中繼資料。 標頭區塊應包含下欄欄位：

   ```yml
   ---
   name: "really cool sample"
   description: "Learn everything about this really cool sample."
   page_type: sample
   languages:
     - csharp
     - fsharp
     - vbnet
   products:
     - dotnet-core
     - dotnet
     - dotnet-standard
     - aspnet
     - aspnet-core
     - ef-core
   ---
   ```

   - `languages` 集合應包含僅適用於您範例的語言。
   - `products` 集合應包含僅與您範例相關的產品。

除非另有註明，否則所有範例都是在 .NET Core 支援的任何平台上透過命令列所建置。 有些 Visual Studio 特定的範例需要 Visual Studio 2017 或更新版本。 此外，有些顯示平台特定功能的範例需要特定平台。 其他範例和程式碼片段需要 .NET Framework 並將在 Windows 平台上執行，而且需要適用於目標 Framework 版本的開發人員套件。

## <a name="the-c-interactive-experience"></a>C# 互動式體驗

文章中包含的所有範例都會使用[語言標記](../code-in-docs.md)來指出來源語言。 C# 中的簡短程式碼範例可以使用 `csharp-interactive` 語言標記來指定要在瀏覽器中執行的 C# 範例 (內嵌程式碼範例使用 `csharp-interactive` 標記，若要包含來自原始程式碼的程式碼片段，請使用 `code-csharp-interactive` 標記)。這些程式碼範例會在文章中顯示程式碼視窗或輸出視窗。 輸出視窗會顯示使用者執行範例之後執行互動式程式碼的任何輸出。

C# 互動式體驗改變了我們使用範例的方式。 訪客可以執行範例來查看結果。 一些因素有助於判斷範例或對應文字是否應該包含輸出的相關資訊。

### <a name="when-to-display-the-expected-output-without-running-the-sample"></a>何時顯示預期的輸出而不需要執行範例

- 適用於初學者的文章應該提供輸出，讓讀者可以比較其工作輸出與預期的回應。
- 輸出是主題不可或缺一部分的範例應該顯示該輸出。 例如，格式化文字的相關文章應該顯示文字格式，而不需要執行範例。
- 若範例和預期的輸出很短，請考慮顯示輸出。 這會省下一些時間。
- 說明目前或不因文化特性而異的文化特性 (Culture) 如何影響輸出的文章，應該說明預期的輸出。 互動式 REPL (「讀取、求值、輸出」迴圈) 會在 Linux 主機上執行。 預設及不因文化特性而異的文化特性 (Culture) 會在不同作業系統和電腦上產生不同輸出。 該文應該說明 Windows、Linux 和 Mac 系統中的輸出。

### <a name="when-to-exclude-expected-output-from-the-sample"></a>何時從範例中排除預期的輸出

- 若文章中的範例會產生較大型輸出，則不應該在註解中包含該輸出。 這會在執行範例之後使程式碼難以閱讀。
- 若文章中的範例示範一個主題，但輸出並非了解該主題的必要項目。 例如，若程式碼會執行 LINQ 查詢來說明查詢語法，然後顯示輸出集合中的每個項目。

> [!NOTE]
> 您可能會注意到某些主題目前未遵循這裡所指定的方針。 我們將致力於達成整個網站的一致性。 請查看我們目前針對該特定目標所追蹤的[開啟問題](https://github.com/dotnet/docs/issues?q=is%3Aopen+is%3Aissue+label%3A%22%3Abookmark_tabs%3A+Information+Architecture%22)清單。

### <a name="contributing-to-international-content"></a>參與國際內容

目前不接受機器翻譯 (MT) 的內容。 為了改善 MT 內容的品質，我們已轉換成神經 MT 引擎。 我們接受並鼓勵人工翻譯 (HT) 內容的貢獻，這可用於訓練神經 MT 引擎。 經過一段時間，HT 內容的貢獻將可同時改善 HT 與 MT 的品質。 MT 主題將有免責聲明，表示部分主題可能是 MT，而當編輯功能停用時，不會顯示 [編輯] 按鈕。

## <a name="contributor-license-agreement"></a>參與者授權合約

您必須簽署 [.NET Foundation 貢獻授權合約 (CLA)](https://cla.dotnetfoundation.org)才能合併 PR。 這是 .NET Foundation 中專案的一次性要求。 您可以在 Wikipedia 上深入了解[貢獻授權合約 (CLA)](http://en.wikipedia.org/wiki/Contributor_License_Agreement)。

合約：[net-foundation-contribution-license-agreement.pdf](https://github.com/dotnet/home/blob/master/guidance/net-foundation-contribution-license-agreement.pdf)

您不需要事先簽署合約。 您可以如往常般複製、派生及提交 PR。 當您的 PR 建立之後，會由 CLA Bot 進行分類。 如果變更不大 (例如修正錯字)，則 PR 會標記為 `cla-not-required`。 否則，它會分類為 `cla-required`。 一旦您簽署了 CLA，目前和所有未來提取要求都會標記為 `cla-signed`。
