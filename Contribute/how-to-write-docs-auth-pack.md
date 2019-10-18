---
title: 適用於 Visual Studio Code 的 Docs 編寫套件
description: 本文說明 Visual Studio Code 延伸模組套件，以協助針對 docs.microsoft.com 編寫 Markdown。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: meganbradley
ms.author: mbradley
ms.date: 10/22/2018
ms.openlocfilehash: 11f18ce4f769b478108d399b780937f927e0e12d
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/12/2019
ms.locfileid: "72288317"
---
# <a name="docs-authoring-pack-for-vs-code"></a>適用於 VS Code 的 Docs 編寫套件

Docs 編寫套件是 Visual Studio Code 延伸模組的集合，以協助針對 docs.microsoft.com 編寫 Markdown。 此套件[可在 VS Code Marketplace 中取得](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)，且包含下列延伸模組：

- [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)：David Anson 提供的熱門 Markdown Linter，可協助確保您的 Markdown 遵循最佳做法。
- [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker) (拼字檢查工具)：由 Street Side Software 開發的完整離線拼字檢查工具。
- [Docs 預覽](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-preview)：使用 docs.microsoft.com CSS 來取得更精確的 Markdown 預覽，包括自訂 Markdown。
- [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown)：為開放式發行系統 (OPS) 中的 docs.microsoft.com 內容提供 Markdown 撰寫協助，包括基本 Markdown 支援以及對 OPS 中自訂 Markdown 語法的支援。 本主題的其餘部分描述 Docs Markdown 延伸模組。
- [Docs 文章範本](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-article-templates)：可讓使用者套用 Markdown 骨架內容到新檔案。

## <a name="prerequisites-and-assumptions"></a>必要條件與假設

若要使用 Docs Markdown 延伸模組準確地插入相關連結、影像與其他內嵌內容，您必須將 VS Code 工作區的範圍設為已複製之開放式發佈系統 (OPS) 存放庫的根目錄。

延伸模組支援的某些語法 (例如警示和程式碼片段) 是 OPS 的自訂 Markdown，除非透過 OPS 予以發行，否則無法正確呈現。

## <a name="how-to-use-the-docs-markdown-extension"></a>如何使用 Docs Markdown 延伸模組

若要存取 Docs Markdown 功能表，請鍵入 `ALT+M`。 您可以按一下或使用向上鍵/向下鍵來選取所需的函式，或鍵入以開始進行篩選，然後當所需函式在功能表中反白顯示時，點擊 `ENTER`。 下列項目可供使用：

|函式     |Description           |
|-------------|----------------------|
|預覽      |使用 Docs Preview 延伸模組，在並排視窗中預覽使用中的主題。 此選項僅適用於已安裝 Docs Preview 的情況。|
|粗體         |將文字格式化為**粗體**。|
|斜體       |將文字格式化為*斜體*。|
|程式碼         |如果選取一行以下，會將文字格式化為 `inline code`。<br><br>如果選取多行，則會將其格式化為括住的程式碼區塊，並可讓您選擇性地選取 OPS 所支援的程式設計語言。|
|警示        |插入附註、重要事項、警告或提示。<br><br>從功能表中選取 [警示]，然後選取警示類型。 如果之前已選取文字，文字將包含在選取的警示語法中。 如果未選取文字，則會新增具有預留位置文字的新警示。|
|編號清單|插入新的編號清單。<br><br> 如果選取多行，每一行都是清單項目。 請注意，編號清單在 Markdown 中全都會顯示為 1，但在 docs.microsoft.com 上則會呈現為連續數字 (若為巢狀清單，則顯示為連續字母)。 若要建立巢狀編號清單，請從父清單內進行定位。|
|項目符號清單|插入新的項目符號清單。|
|資料表        |插入 Markdown 資料表結構。<br><br>選取資料表命令之後，請以「資料行:資料列」的格式 (例如 3:4) 指定資料行和資料列的數目。 請注意，您可以透過此延伸模組指定的資料行數目上限是 5，這是方便閱讀的最大建議值。|
|連結到存放庫中的檔案|插入目前存放庫中另一個檔案的相對連結。 選取此選項之後，請在命令視窗中鍵入以依名稱篩選檔案，然後選取所需的檔案。 若您先前已選取文字，它將會成為連結文字。 否則，將使用目標檔案的 H1 做為連結文字。|
|連結到網頁    |插入網頁連結。 選取此選項之後，請貼上或輸入 URI 到命令視窗中。 `https://` 為必要項目。 若您先前已選取文字，它將會成為連結文字。 否則，將使用 URI 做為連結文字。|
|連結到標題     |連結到目前檔案中或存放庫中另一個檔案中的書籤。<br>`Bookmark in this file`：從目前檔案的標題清單中進行選擇，以插入格式正確的書籤。<br>`Bookmark in another file`：首先，依檔案名稱篩選並選取要連結的檔案，然後選擇所選檔案內的適當標題。|
|影像        |鍵入替代文字 (協助工具所需) 並選取它，然後呼叫此命令，以篩選存放庫中支援的影像清單並選取所需的影像。 如果在呼叫此命令時未選取替代文字，系統將提示您鍵入它，然後您才能選取影像。|
|包含項      |尋找要內嵌於目前檔案的檔案。|
|程式碼片段      |尋找存放庫中要內嵌於目前檔案的程式碼片段。|
|影片        |新增內嵌影片。|
|範本     |建立新檔案並套用 Markdown 範本。 如需詳細資訊，請參閱下面的[範本](#how-to-use-docs-templates)。|

## <a name="how-to-assign-keyboard-shortcuts"></a>如何指派鍵盤快速鍵

1. 依序鍵入 `CTRL+K` 和 `CTRL+S`，以開啟鍵盤快速鍵清單。
1. 搜尋您要建立自訂按鍵繫結關係的命令，例如 `formatBold`。
1. 按一下當您將滑鼠移至該行上時，顯示在命令名稱附近的加號。
1. 看到新的輸入方塊之後，請鍵入您要連結至該特定命令的鍵盤快速鍵。 例如，若要使用粗體的常用快速鍵，請鍵入 `ctrl+b`。
1. 最好是將 `when` 子句插入到按鍵繫結關係中，使其無法用於 Markdown 之外的檔案。 若要執行此作業，請開啟 *keybindings.json*，並在命令名稱下面插入下行 (務必在各行之間新增逗號)：
   
    `"when": "editorTextFocus && editorLangId == 'markdown'"`

    keybindings.json 中完成的自訂按鍵繫結關係應如下所示：

    ```json
    // Place your key bindings in this file to overwrite the defaults
    [
        {
            "key": "ctrl+b",
            "command": "formatBold",
            "when": "editorTextFocus && editorLangId == 'markdown'"
        }
    ]
    ```

1. 儲存 keybindings.json。

如需詳細資訊，請參閱 VS Code 文件中的[按鍵繫結關係](https://code.visualstudio.com/docs/getstarted/keybindings)。

## <a name="how-to-show-the-legacy-toolbar"></a>如何顯示舊版工具列

延伸模組發行前版本的使用者將會注意到，安裝 Docs Markdown 延伸模組後，編寫工具列不再顯示於 VS Code 視窗的底端。 這是因為該工具列在 VS Code 狀態列上佔用了許多空間，且未遵循延伸模組 UX 的最佳做法，所以在新的延伸模組中已淘汰使用。 不過，您可以更新 VS Code 的 settings.json 檔案，以便選擇性地顯示工具列，如下所示：

1. 在 VS Code 中，移至 [檔案] -> [喜好設定] -> [設定] - (`CTRL+Comma`)。
1. 選取 [使用者設定] 來變更所有 VS Code 工作區的設定，或選取 [工作區設定]，只變更目前工作區的設定。
1. 在 [預設設定] 窗格中，尋找 [Docs Authoring Extension Configuration] \(Docs 編寫延伸模組設定)，並選取所需設定旁的鉛筆圖示。 接下來，系統會提示您選取 `true` 或 `false`。 進行選取後，VS Code 會自動將值新增至 settings.json 檔案，並且會提示您重新載入視窗，以讓變更生效。

## <a name="how-to-use-docs-templates"></a>如何使用文件範本

Docs Article Templates (文件文章範本) 延伸模組可讓 VS Code 中的作者從中央存放庫提取 Markdown 範本並將它套用到檔案。 範本可以協助確保文章中包含必要中繼資料，以及遵循內容標準等等。 範本是在 GitHub 存放庫中以 Markdown 檔案方式管理。

### <a name="to-apply-a-template-in-vs-code"></a>在 VS Code 中套用範本

1. 若您沒有安裝 Docs Markdown 延伸模組，請按 F1 以開啟命令選擇區，開始輸入「範本」以篩選，然後按一下 `Docs: Template`。 若您已安裝 Docs Markdown，您可以使用命令選擇區或按一下 `Alt+M` 以帶出 Docs Markdown QuickPick 功能表，然後從清單中選取 `Template`。
1. 從出現的清單中選取想要的範本。

### <a name="to-add-your-github-id-andor-microsoft-alias-to-your-vs-code-settings"></a>將您的 GitHub ID 和/或 Microsoft 別名新增到您的 VS Code 設定

Templates (範本) 延伸模組支援三種動態中繼資料欄位：作者、ms.author 與 ms.date。 這表示若範本建立者在 Markdown 範本的中繼資料標頭中使用這些欄位，當您套用此範本時，系統將會在您的檔案中自動填入，如下所示：

|中繼資料  |值|
|----------|---------------|
|作者    |您的 GitHub 識別碼，若已在您的 VS Code 設定檔中指定。|
|ms.author |您的 GitHub 識別碼 (若已在您的 VS Code 設定檔中指定)。 若您不是 Microsoft 員工，請不要指定此項目。|
|ms.date   |Docs 支援格式的 MM/DD/YYYY 目前日期。 請注意，如果您後續更新檔案，則不會自動更新日期。 您必須手動更新 ms.date 值，指出 docs.microsoft.com 網站上的最新發佈日期。|

### <a name="to-set-author-github-id-andor-msauthor-microsoft-alias"></a>設定作者 (GitHub 識別碼) 和/或 ms.author (Microsoft 別名)

1. 在 VS Code 中，移至 [檔案] -> [喜好設定] -> [設定] - (`CTRL+Comma`)。
1. 選取 [使用者設定] 以變更所有 VS Code 工作區的設定，或選取 [工作區設定] 只變更目前工作區的設定。
1. 在左邊的 [預設設定] 窗格中，尋找 Docs Article Templates Extension Configuration (文件文章範本延伸模組設定) 並按一下想要之設定旁的鉛筆圖示，然後按一下 [在設定中取代]。
1. [使用者設定] 將會並排開啟，而且底部會顯示新項目。
1. 視需要新增您的 GitHub 識別碼或 Microsoft 電子郵件別名，然後儲存檔案。
1. 您可能需要關閉並重新啟動 VS Code，變更才會生效。
1. 現在，當您套用使用動態欄位的範本時，您的 GitHub 識別碼和/或 Microsoft 別名將會在中繼資料標頭中自動填入。
