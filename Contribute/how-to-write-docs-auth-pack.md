---
title: 適用於 Visual Studio Code 的 Docs 編寫套件
description: 本文說明 Visual Studio Code 延伸模組套件，以協助針對 docs.microsoft.com 編寫 Markdown。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: meganbradley
ms.author: mbradley
ms.date: 03/05/2020
ms.openlocfilehash: 5bbf51af52069d5636715ffb2bd3f59bf459d5b9
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336412"
---
# <a name="docs-authoring-pack-for-vs-code"></a>適用於 VS Code 的 Docs 編寫套件

Docs 編寫套件是 VS Code 延伸模組的集合，有助於 docs.microsoft.com 的 Markdown 編寫。 此套件[可在 VS Code Marketplace 中取得](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)，且包含下列延伸模組：

> [!div class="checklist"]
> * [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown)：為 docs.microsoft.com (Docs) 內容提供 Markdown 撰寫協助，包括基本 Markdown 支援以及對 Docs 中自訂 Markdown 語法的支援，例如：警示、程式碼片段、不可當地語系化的文字。 現在也包含一些基本的 YAML 編寫協助，例如插入目錄項目。
> * [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)：David Anson 提供的熱門 Markdown Linter，可協助確保您的 Markdown 有效。
> * [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker) (拼字檢查工具)：由 Street Side Software 開發的完整離線拼字檢查工具。
> * [Docs 預覽](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-preview)：使用 docs.microsoft.com CSS 來取得更精確的 Markdown 預覽，包括自訂 Markdown。
> * [Docs 文章範本](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-article-templates)：可讓使用者建構學習模組，套用 Markdown 骨架內容到新檔案。
> * [Docs YAML](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-yaml)：提供 Docs YAML 架構驗證和自動完成。
> * [Docs Images](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-images)：提供資料夾和個別檔案的影像壓縮和調整大小，以協助 docs.microsoft.com 的作者。

## <a name="prerequisites-and-assumptions"></a>必要條件與假設

若要使用 Docs Markdown 延伸模組插入相關連結、影像與其他內嵌內容，您必須將 VS Code 工作區的範圍設為已複製之開放式發佈系統 (OPS) 存放庫的根目錄。 例如，如果您已將 Docs 存放庫複製到 `C:\git\SomeDocsRepo\`，請在 VS Code 中開啟該資料夾或子資料夾：[檔案]  >  [開啟資料夾] 功能表，或從命令列輸入 `code C:\git\SomeDocsRepo\`。

延伸模組支援的某些語法 (例如警示和程式碼片段) 是 OPS 的自訂 Markdown。 除非透過 OPS 發佈，否則無法正確轉譯自訂 Markdown。

## <a name="how-to-use-the-docs-markdown-extension"></a>如何使用 Docs Markdown 延伸模組

若要存取 [Docs Markdown] 功能表，輸入 <kbd>ALT+M</kbd>。 您可以按一下或使用向上鍵/向下鍵來選取您想要的命令。 或者，您可以輸入篩選條件開始進行篩選，然後當所需函式在功能表中反白顯示時，點擊 <kbd>ENTER</kbd>。

如需最新命令的清單，請參閱 [Docs Markdown 讀我檔案](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown)。

## <a name="how-to-generate-a-master-redirect-file"></a>如何產生主要重新導向檔案

Docs Markdown 延伸模組包含一個指令碼，可根據個別檔案中的 `redirect_url` 中繼資料，產生或更新存放庫的主要重新導向檔案。 此指令碼會檢查存放庫內每個 Markdown 檔案中的 `redirect_url`，將重新導向中繼資料新增至存放庫的主要重新導向檔案 (.openpublishing.redirection.json)，並將重新導向後的檔案移至存放庫外的資料夾。 執行指令碼：

1. 選取 <kbd>F1</kbd> 以開啟 VS Code 命令選擇區。
2. 開始輸入 "Docs:Generate..."
3. 選取 `Docs: Generate master redirection file` 命令。
4. 當指令碼完成執行時，重新導向結果會顯示在 VS Code 的輸出窗格中，而被移除的 Markdown 檔案將會新增至預設路徑底下的 Docs Authoring\redirects 資料夾中。
5. 檢閱結果。 如果結果如預期，請提交提取要求以更新存放庫。

## <a name="how-to-assign-keyboard-shortcuts"></a>如何指派鍵盤快速鍵

1. 按 <kbd>CTRL+K</kbd> 然後按 <kbd>Ctrl+S</kbd> 開啟 [鍵盤快速鍵] 清單。
1. 搜尋您要建立自訂按鍵繫結關係的命令，例如 `formatBold`。
1. 按一下當您將滑鼠移至該行上時，顯示在命令名稱附近的加號。
1. 看到新的輸入方塊之後，請鍵入您要連結至該特定命令的鍵盤快速鍵。 例如，若要使用粗體的常用快速鍵，請按 <kbd>Ctrl+B</kbd>。
1. 最好是將 `when` 子句插入按鍵繫結關係中，使其無法用於 Markdown 之外的檔案。 若要執行此作業，請開啟 *keybindings.json*，並在命令名稱下面插入下行 (務必在各行之間新增逗號)：

    `"when": "editorTextFocus && editorLangId == 'markdown'"`

    您在 keybindings.json 中完成的自訂按鍵繫結關係應如下所示：

    ```json
    [
        {
            "key": "ctrl+b",
            "command": "formatBold",
            "when": "editorTextFocus && editorLangId == 'markdown'"
        }
    ]
    ```

    > [!TIP]
    > 將您的按鍵繫結關係放在此檔案中以覆寫預設值

1. 儲存 keybindings.json。

如需按鍵繫結關係的詳細資訊，請參閱 [VS Code 文件](https://code.visualstudio.com/docs/getstarted/keybindings)。

## <a name="how-to-show-the-legacy-gauntlet-toolbar"></a>如何顯示舊版 "Gauntlet" 工具列

"Gauntlet" 延伸模組程式碼的先前使用者將會注意到，安裝 Docs Markdown 延伸模組後，編寫工具列不再顯示於 VS Code 視窗的底端。 這是因為該工具列在 VS Code 狀態列上佔用了大量空間，且未遵循延伸模組 UX 的最佳做法，所以在新的延伸模組中已淘汰使用。 不過，您可以更新 VS Code 的 settings.json 檔案，以便選擇性地顯示工具列，如下所示：

1. 在 VS Code 中，移至 [檔案]  >  [喜好設定]  >  [設定]，或選取<kbd>Ctrl+,</kbd>。
1. 選取 [使用者設定] 以變更所有 VS Code 工作區的設定，或選取 [工作區設定] 只變更目前工作區的設定。
1. 選取 [延伸模組]  >  [Docs Markdown 延伸模組設定]，然後選取 [在底部狀態列中顯示舊版工具列]。

   ![VS Code 中顯示舊版工具列設定](docs-authoring/media/show-gauntlet-bar.png)

完成選取之後，VS Code 會更新 settings.json 檔案。 系統會提示您重新載入視窗，讓變更生效。

延伸模組新增加的較新命令將無法從工具列取得。

## <a name="how-to-use-docs-templates"></a>如何使用文件範本

Docs Article Templates (文件文章範本) 延伸模組可讓 VS Code 中的作者從中央存放庫提取 Markdown 範本並將它套用到檔案。 範本可以協助確保文章中包含必要中繼資料，以及遵循內容標準等等。 範本是在 GitHub 存放庫中以 Markdown 檔案方式管理。

### <a name="to-apply-a-template-in-vs-code"></a>在 VS Code 中套用範本

1. 請確定已安裝並啟用 Docs 文章範本延伸模組。
1. 若您沒有安裝 Docs Markdown 延伸模組，按 <kbd>F1</kbd> 開啟命令選擇區，開始輸入 "template" 以進行篩選，然後按一下 `Docs: Template`。 若您已安裝 Docs Markdown，您可以使用命令選擇區或按 <kbd>Alt+M</kbd> 以帶出 Docs Markdown QuickPick 功能表，然後從清單中選取 `Template`。
1. 從出現的清單中選取想要的範本。

### <a name="to-add-your-github-id-andor-microsoft-alias-to-your-vs-code-settings"></a>將您的 GitHub ID 和/或 Microsoft 別名新增到您的 VS Code 設定

Templates (範本) 延伸模組支援三種動態中繼資料欄位：作者、ms.author 與 ms.date。 這表示若範本建立者在 Markdown 範本的中繼資料標頭中使用這些欄位，當您套用此範本時，系統將會在您的檔案中自動填入，如下所示：

| 中繼資料欄位 | 值 |
|--|--|
| `author` | 您的 GitHub 別名 (若已在您的 VS Code 設定檔中指定)。 |
| `ms.author` | 您的 GitHub 識別碼 (若已在您的 VS Code 設定檔中指定)。 若您不是 Microsoft 員工，請不要指定。 |
| `ms.date` | 目前日期，為Docs 支援的格式 `MM/DD/YYYY`。 如果您之後更新檔案，日期不會自動更新，您必須手動更新。 這個欄位是用來表達「文章的時效性」。 |

### <a name="to-set-author-andor-msauthor"></a>設定作者和/或 ms.author

1. 在 VS Code 中，移至 [檔案]  >  [喜好設定]  >  [設定]，或選取<kbd>Ctrl+,</kbd>。
1. 選取 [使用者] 設定以變更所有 VS Code 工作區的設定，或選取 [工作區] 設定只變更目前工作區的設定。
1. 在左邊的 [預設設定] 窗格中，尋找 [Docs 文章範本延伸模組設定]，按一下所需設定旁的鉛筆圖示，然後按一下 [在設定中取代]。
1. [使用者] 設定將會並排開啟，而且底部會顯示新項目。
1. 視需要新增您的 GitHub 識別碼或 Microsoft 電子郵件別名，然後儲存檔案。
1. 您可能需要關閉並重新啟動 VS Code，變更才會生效。
1. 現在，當您套用使用動態欄位的範本時，您的 GitHub 識別碼和/或 Microsoft 別名將會在中繼資料標頭中自動填入。

### <a name="to-make-a-new-template-available-in-vs-code"></a>在 VS Code 中提供新的範本

1. 以 Markdown 檔案的形式草擬您的範本。
1. 提交提取要求至 [MicrosoftDocs/content-templates](https://github.com/MicrosoftDocs/content-templates) 存放庫的範本資料夾。

docs.microsoft.com 小組會審查您的範本，若其符合 docs.microsoft.com 樣式指導方針便會合併 PR。 合併之後，此範本就可供 Docs 文章範本延伸模組的所有使用者使用。

## <a name="demo-several-features"></a>示範數個功能

以下的簡短影片示範 Docs 編寫套件的下列功能：

* **YAML 檔案**
  * 支援 Docs:連結到存放庫中的檔案
* **Markdown 檔案**
  * [更新 ms. date 中繼資料值] 操作功能表選項
  * 用於程式碼隔離語言識別碼的程式碼自動完成
  * 無法辨識的程式碼隔離語言識別碼警告/自動校正支援
  * 遞增排序選取項目 (A 到 Z)
  * 遞減排序選取項目 (Z 到 A)

> [!VIDEO https://www.youtube.com/embed/6zfbBRdjlw8]

## <a name="contribution-expectations"></a>參與貢獻的期望

Docs 編寫套件延伸模組為開放原始碼，能讓任何有 GitHub 帳戶的人參與貢獻。 Microsoft 內部有專門的小組正全心投入這個專案。 這個小組會監視問題和提取要求。 服務等級協定 (SLA) 和預期取得提取要求的審查時間目前為一周。 小組正在進行自動化工作，以改善此回應時間。

## <a name="next-steps"></a>下一步

探索 Docs 編寫套件 (Visual Studio Code 延伸模組) 的各種功能。

* [開發語言完成](docs-authoring/dev-lang-completion.md)
* [影像壓縮](docs-authoring/image-compression.md)
* [中繼資料更新](docs-authoring/metadata-updates.md)
* [重新格式化資料表](docs-authoring/reformat-table.md)
* [智慧引號取代](docs-authoring/smart-quote-replacement.md)
* [排序重新導向](docs-authoring/sort-redirects.md)
* [排序選取項目](docs-authoring/sort-selection.md)
