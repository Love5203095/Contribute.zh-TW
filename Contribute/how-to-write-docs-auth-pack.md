---
title: 適用於 VS Code 的 Docs 編寫套件
description: VS Code 延伸模組套件，可協助進行 docs.microsoft.com 的 Markdown 編寫。
author: meganbradley
ms.author: mbradley
manager: jemash
ms.date: 04/06/2018
ms.article: contributor-guide
ms.prod: n.a
ms.service: n.a
ms.technology: n.a
ms.openlocfilehash: 5c857deb07e28e1f6744c895a291bf78a6acf1df
ms.sourcegitcommit: dd1b4e915f4996ac029d2a0704ced785438d3484
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/23/2018
---
# <a name="docs-authoring-pack-for-vs-code"></a>適用於 VS Code 的 Docs 編寫套件

Docs 編寫套件是 VS Code 延伸模組的集合，有助於 docs.microsoft.com 的 Markdown 編寫。此套件[可在 VS Code Marketplace 中取得](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)，且包含下列延伸模組：

- **DocFx：**提供 docs.microsoft.com 特定的 Markdown 預覽。 如需詳細資訊，請參閱 [DocFx](https://marketplace.visualstudio.com/items?itemName=ms-docfx.DocFX)。
- **markdownlint：**David Anson 提供的熱門 Markdown Linter，可協助確保 Markdown 遵循最佳做法。 如需詳細資訊，請參閱 [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)。
- **Docs Markdown：**為開放式發行系統 (OPS) 中的 docs.microsoft.com 內容提供 Markdown 編寫協助，包括基本 Markdown 支援以及對 OPS 中自訂 Markdown 語法的支援。 本主題的其餘部分描述 Docs Markdown 延伸模組。

## <a name="prerequisites-and-assumptions"></a>必要條件與假設

若要使用 Docs Markdown 延伸模組準確地插入相關連結、影像及其他內嵌內容，您必須將 VS Code 工作區的範圍設為已複製之 OPS 存放庫的根目錄。

延伸模組支援的某些語法 (例如警示和程式碼片段) 是 OPS 的自訂 Markdown，除非透過 OPS 予以發行，否則無法正確呈現。

## <a name="how-to-use-the-docs-markdown-extension"></a>如何使用 Docs Markdown 延伸模組

若要存取 Docs Markdown 功能表，請鍵入 `ALT+M`。 您可以按一下或使用向上鍵/向下鍵來選取所需的函式，或鍵入以開始進行篩選，然後當所需函式在功能表中反白顯示時，點擊 `ENTER`。 下列項目可供使用：

|函式     |命令             |描述           |
|-------------|--------------------|----------------------|
|粗體         |`formatBold`        |將文字格式化為**粗體**。|
|斜體       |`formatItalic`      |將文字格式化為*斜體*。|
|程式碼         |`formatCode`        |如果選取一行以下，會將文字格式化為 `inline code`。<br><br>如果選取多行，則會將其格式化為括住的程式碼區塊，並可讓您選擇性地選取 OPS 所支援的程式設計語言。|
|警示        |`insertAlert`       |插入附註、重要事項、警告或提示。<br><br>從功能表中選取 [警示]，然後選取警示類型。 如果之前已選取文字，文字將包含在選取的警示語法中。 如果未選取文字，則會新增具有預留位置文字的新警示。|
|編號清單|`insertNumberedList` |插入新的編號清單。<br><br> 如果選取多行，每一行都是清單項目。 請注意，編號清單在 Markdown 中全都會顯示為 1，但在 docs.microsoft.com 上則會呈現為連續數字 (若為巢狀清單，則顯示為連續字母)。 若要建立巢狀編號清單，請從父清單內進行定位。|
|項目符號清單|`insertBulletedList` |插入新的項目符號清單。|
|資料表        |`insertTable`        |插入 Markdown 資料表結構。<br><br>選取資料表命令之後，請以「資料行:資料列」的格式 (例如 3:4) 指定資料行和資料列的數目。 請注意，您可以透過此延伸模組指定的資料行數目上限是 5，這是方便閱讀的最大建議值。|
|連結         |`selectLinkType`      |插入連結。 當您選取這個命令時，即會顯示下列子功能表。<br><br>`External`：透過 URI 連結至網頁。 必須包含 "http" 或 "https"。<br>`Internal`：將相關連結插入到相同存放庫中的另一個檔案。 選取此選項之後，請在命令視窗中鍵入以依名稱篩選檔案，然後選取所需的檔案。 <br>`Bookmark in this file`：從目前檔案的標題清單中進行選擇，以插入格式正確的書籤。<br>`Bookmark in another file`：首先，依檔案名稱篩選並選取要連結的檔案，接著選擇所選取檔案內的適當標題。|
|影像        |`insertImage`     |鍵入替代文字 (協助工具所需) 並選取它，然後呼叫此命令，以篩選存放庫中支援的影像清單並選取所需的影像。 如果在呼叫此命令時未選取替代文字，系統將提示您鍵入它，然後您才能選取影像。|
|包含項      |`insertInclude`   |尋找要內嵌於目前檔案的檔案。|
|程式碼片段      |`insertSnippet`   |尋找存放庫中要內嵌於目前檔案的程式碼片段。|
|影片        |`insertVideo`     |新增內嵌影片。|
|預覽      |`previewTopic`    |使用 DocFX 延伸模組，在並排視窗中預覽使用中的主題。  如果 DocFX 延伸模組未安裝或已安裝但未啟用，則不會呈現主題。


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

## <a name="how-to-show-the-legacy-gauntlet-toolbar"></a>如何顯示舊版 "Gauntlet" 工具列

"Gauntlet" 延伸模組程式碼的先前使用者將會注意到，安裝 Docs Markdown 延伸模組後，編寫工具列不再顯示於 VS Code 視窗的底端。 這是因為該工具列在 VS Code 狀態列上佔用了許多空間，且未遵循延伸模組 UX 的最佳做法，所以在新的延伸模組中已淘汰使用。 不過，您可以更新 VS Code 的 settings.json 檔案，以便選擇性地顯示工具列，如下所示：

1. 在 VS Code 中，移至 [檔案] -> [喜好設定] -> [設定] (`CTRL+Comma`)。
1. 選取 [使用者設定] 來變更所有 VS Code 工作區的設定，或選取 [工作區設定]，只變更目前工作區的設定。
1. 在 [預設設定] 窗格中，尋找 [Docs Authoring Extension Configuration] \(Docs 編寫延伸模組設定)，並選取所需設定旁的鉛筆圖示。 接下來，系統會提示您選取 `true` 或 `false`。 進行選取後，VS Code 會自動將值新增至 settings.json 檔案，並且會提示您重新載入視窗，以讓變更生效。

## <a name="known-issues"></a>已知問題

- [DocFX 預覽] MacOS 和 Linux：DocFX 預覽未正確啟動預覽 (這些平台的預覽預設為 VS Code Markdown 預覽)。
- [DocFx 預覽] 所有平台：部分語法 (例如 API 的 xref (交互參考) 連結) 未在預覽中正確呈現，在某些情況下，內容會將留白。
- [外部書籤] Linux：已顯示檔案清單，但未顯示任何標題以供選取。
- [包含項] Linux：已顯示檔案清單，但在選取後未新增任何連結。